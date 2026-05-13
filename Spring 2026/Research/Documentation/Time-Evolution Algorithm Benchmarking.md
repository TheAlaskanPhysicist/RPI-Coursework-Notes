**Author:** Stanley Goodwin
**Date:** May 12th, 2026

---
## Preface
Given the wide range of packages and implementation schemes for statevector time evolution, we require benchmarking in order to verify the integrity of the output data while optimizing runtime. This document serves as a summary of all my work in this niche for the Quantum Hysteresis project, as well as showing a timeline of exploration and ideas.

From prior experience, I know there is a need for different algorithms in different regimes. To have a more comprehensive review than I had before, I intend to replicate and expand on the conclusions I found in an older version of my benchmarking documentation. I will also focus a lot on accuracy, precision, runtime, memory usage, cpu usage, and other typical benchmarking quantities that will be of use in moving to the RPI CCI cluster.

My simulation is build around an initial state of all-up spins in the Z direction, and that we construct the Hamiltonian as a `SparsePauliOp` for later usage with the RPI Quantum Computer later on in simulation. The packages I am considering for time evolution are `Qiskit`, `SciPy`, `NumPy`, and base `Python`. This section will detail the exploration of designing this algorithm, benchmarking their efficacy, and ultimately deciding on a choice for my system.

Lastly, in the name of experimental reduction, I will be looking at individual choices in parameters on their own to determine whether or not there is a significant enough different to warrant extra investigation. This will hopefully reduce a lot of the work I have to do, as well as make the reduction of different choices clearer as I go further along with experimentation.

---
## Choices in Implementation
There are many different ways that a statevector time evolution algorithm can be created in order to balance speed, precision, accuracy, and memory usage. However, it is usually best to start with a list of things we will want to investigate, leaving their combinatorics for later benchmarking. For this section to not take years in itself, I will be using a hierarchical elimination scheme. As small variations in benchmark data are not that important to my research, I will weed these out preemptively after simple benchmarks.

Some points of investigation I will look into are
 - Should the Hamiltonian remain sparse or dense
 - How to exponentiate the Hamiltonian
 - How to multiply the time evolution operator onto the statevector
 - Ways to combine the exponentiation and application intelligently
 - Where to change floating-point precision and maintain quality

After a lot of research, I have determined the following for each section
1. If `hamiltonian.to_matrix(sparse=False)`, then
	1. If explicitly constructing the matrix exponentiation $U=e^A$ :
		1. `scipy.linalg.expm`
		2. `scipy.sparse.linalg.expm`
		3. `scipy/numpy.linalg.eigh`
	2. If explicitly doing the matrix multiplication $U\psi$ :
		1. `U @ statevector.data`
		2. `Statevector.evolve(Operator(U))`
	3. If being clever doing both parts at once $e^A\psi$ :
		1. `scipy/numpy.linalg.eigh` with `V @ (exp_diag @ (V.conj().T @ psi))`
		2. `scipy.sparse.linalg.expm_multiply`
2. If `hamiltonian.to_matrix(sparse=True)`, then
	1. If explicitly constructing the matrix exponentiation $U=e^A$ :
		1. `scipy.sparse.linalg.expm`
	2. If explicitly doing the matrix multiplication $U\psi$ :
		1. `U @ statevector.data`
		2. `Statevector.evolve(Operator(U))`
	3. If being clever doing both parts at once $e^A\psi$ :
		1. `scipy.sparse.linalg.expm_multiply`

What was not considered due to some thought
1. Sparse Columns Matrices, since our Hamiltonian is Hermitian it shouldn't make a difference in the speed, thus is a waste of time to convert.
2. Changing of floating-point precision levels, since this can be determined way later with the most optimal algorithm if the error bars are small enough.
3. The usage of `.dot()` with matrices and vectors, as I believe those are the same operations under the hood as the matrix multiplication symbol.
4. The function `scipy.sparse.linalg.eigsh` only find the partial eigenvalue matrix, so results are wildly incorrect. This cannot be used for our simulation.

---
### Eigenvector Decomposition Algorithms
There are multiple ways that using eigenvalues has been used for calculating the statevector evolution. However, in order to simplify our search, we want to determine if all of these algorithms are effectively identical or where one is always dominant, so that we can reduce our search space.

The script for the benchmark is pretty much fully automated, and so there are a few results auto generated from the data analysis. For reference, the datapoints were generated from
```python
h_list = np.linspace(0, 10, 10+1)
f_list = np.linspace(0, 1, 10+1)
times = np.linspace(0, 100, 10+1)
```

| Max Error   | $L=2$    | $L=3$    | $L=4$    | $L=5$    | $L=6$    | $L=7$    |
| ----------- | -------- | -------- | -------- | -------- | -------- | -------- |
| NumPy       | 2.31e-16 | 2.69e-16 | 3.09e-16 | 2.89e-16 | 3.64e-16 | 4.82e-16 |
| Dense SciPy | 2.33e-16 | 2.40e-16 | 3.46e-16 | 2.99e-16 | 3.72e-16 | 3.83e-16 |
| All Dense   | 1.23e-12 | 1.50e-12 | 1.24e-12 | 1.10e-12 | 1.40e-12 | 1.30e-12 |
**Table I**: Maximum statevector distance between two outputs for different chain lengths. 

| Algorithm (avg ms) | $L=2$ | $L=3$ | $L=4$ | $L=5$ | $L=6$ | $L=7$  |
| ------------------ | ----- | ----- | ----- | ----- | ----- | ------ |
| `__dm_neigh_mm`    | 0.165 | 0.206 | 0.321 | 0.618 | 2.362 | 23.753 |
| `__dm_neigh_qe`    | 0.164 | 0.217 | 0.318 | 0.649 | 2.338 | 24.261 |
| `__dm_neigh_mult`  | 0.142 | 0.207 | 0.295 | 0.559 | 2.326 | 23.557 |
| `__dm_seigh_mm`    | 0.180 | 0.238 | 0.337 | 1.246 | 2.903 | 26.377 |
| `__dm_seigh_qe`    | 0.178 | 0.249 | 0.350 | 1.297 | 2.918 | 26.670 |
| `__dm_seigh_mult`  | 0.162 | 0.229 | 0.323 | 1.270 | 2.720 | 25.069 |
**Table II**: Algorithm runtime averaged over 10 trials of the same 1331 sample inputs.

Based on the data collected, it really doesn't matter whether or not you use the`scipy`or `numpy`implementation, nor does trying to be clever with multiplication make the algorithm statistically significantly faster. The relative error in statevector evolution is also very small, and so we can confidently say that they create the same vector up to floating point error. Therefore, for future tests, we can treat all eigenvector decomposition algorithms as identical for comparison purposes.

---
### Matrix Evaluation Methods (Dense Matrices)
For the dense matrices, we can compare the three different algorithms for constructing the evolution operator and two for calculating the time-evolved state. Running this benchmark, we get the following data tables.

| Max Error        | $L=2$    | $L=3$    | $L=4$    | $L=5$    | $L=6$    |
| ---------------- | -------- | -------- | -------- | -------- | -------- |
| 3 exp, matrix    | 1.19e-12 | 1.48e-12 | 1.23e-12 | 1.18e-12 | 1.37e-12 |
| 3 exp, qiskit    | 1.19e-12 | 1.48e-12 | 1.23e-12 | 1.18e-12 | 1.37e-12 |
| All combin.      | 1.19e-12 | 1.48e-12 | 1.23e-12 | 1.18e-12 | 1.37e-12 |
| matrix vs qiskit | 0.00e+00 | 0.00e+00 | 0.00e+00 | 0.00e+00 | 0.00e+00 |
**Table III**: Maximum statevector distance between two outputs for different chain lengths. 

| Algorithm (avg ms) | $L=2$ | $L=3$ | $L=4$ | $L=5$ | $L=6$ | $L=7$ | $L=8$ |
| ------------------ | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| `__dm_dexpm_mm`    | 0.205 | 0.323 | 0.486 | 0.697 | 2.287 |       |       |
| `__dm_sexpm_mm`    | 0.302 | 0.442 | 0.789 | 1.242 | 2.922 |       |       |
| `__dm_seigh_mm`    | 0.159 | 0.237 | 0.337 | 1.140 | 2.772 |       |       |
| `__dm_dexpm_qe`    | 0.188 | 0.317 | 0.478 | 0.774 | 2.446 |       |       |
| `__dm_sexpm_qe`    | 0.299 | 0.435 | 0.739 | 1.335 | 3.000 |       |       |
| `__dm_seigh_qe`    | 0.183 | 0.224 | 0.339 | 1.218 | 2.911 |       |       |
**Table IV**: Algorithm runtime averaged over 10 (2 for $L=7,8$) trials of the same 1331 sample inputs.

From **Table III**, it's clear to see that the actual mathematical difference between the direct matrix multiplication and the `qiskit`evaluation method are identical in their outputs. In other words, any variation in the output state is the result of the exponentiation method only. With the error between different exponentiation methods being so small, it's once again reasonable to conclude that these are all generating the same output up to a floating-point error.

From **Table IV**, we can see that the result for whether the `qiskit`evaluation or direct matrix evaluation is faster is an uncertain mix that doesn't seem to be very large and doesn't have much of a discernable pattern. However, between the exponentiation algorithms, it does appear that the eigenvalue decomposition is faster for calculating the matrix exponential by a pretty decent margin, with it only being slower for $L=5,6$, which I believe to be because of caching. It also appears that the sparse matrix exponentiation on the dense matrix is *always slower*, and thus we can also remove it from our choices.

While not listed in the table, I also ran the direct matrix exponentiation `expm_multiply`against the two best algorithms for error and runtime. It was clear very quickly that it was *extremely slow* even for small systems (20ms+ for $L=3$), and so was thrown out on that alone.

For the dense matrices going forward, we can treat the choice of matrix multiplication style as just the generic product, thus removing that degree of freedom for this case. For exponentiation, I will elect to keep `scipy.linalg.expm` in order to see if it truly is lesser in future tests.

---
### Matrix Evaluation Methods (Sparse Matrices)
Luckily, there are only two sparse matrix algorithms left. Running the benchmark, we get

| Max Error    | $L=2$    | $L=3$    | $L=4$    | $L=5$    | $L=6$    |
| ------------ | -------- | -------- | -------- | -------- | -------- |
| Between both | 2.38e-11 | 1.81e-11 | 1.34e-11 | 8.38e-12 | 6.01e-12 |
**Table V**: Maximum statevector distance between two outputs for different chain lengths. 

| Algorithm (avg ms) | $L=2$  | $L=3$  | $L=4$  | $L=5$  | $L=6$  | $L=7$  | $L=8$   |
| ------------------ | ------ | ------ | ------ | ------ | ------ | ------ | ------- |
| `__sm_sexpm_mm`    | 2.806  | 3.511  | 5.211  | 8.257  | 15.228 | 44.498 | 222.251 |
| `__sm_expm_mult`   | 15.576 | 15.776 | 17.379 | 18.076 | 19.841 | 21.038 | 40.914  |
**Table VI**: Algorithm runtime averaged over 10 (2 for $L=7,8$) trials of the same 1331 sample inputs.

Similar to the dense matrix section, we will continue on with both function implementations into the next round of methods in order to determine their efficacy with respect to each other.

---
### Time-Evolution Benchmarking (1st Round)
We have now refined our set of algorithms to the following
1. `hamiltonian.to_matrix(sparse=False)`
	1. `scipy.linalg.expm` and `U @ statevector.data`
	2. `scipy.linalg.eigh` and `U @ statevector.data`
2. `hamiltonian.to_matrix(sparse=True)`
	1. `scipy.sparse.linalg.expm` and `U @ statevector.data`
	2. `scipy.sparse.linalg.expm_multiply`

We yet again write code to benchmark these different methods. We will want to test each algorithm for different chain lengths, as well as varying which regimes we are in in order to see the time calculation time difference. As we increase chain lengths, we should sample fewer points in order to not wait weeks for results. The benchmarked data is as follows

| Max Error | $L=2$ | $L=3$ | $L=4$ | $L=5$ | $L=6$ |
| --------- | ----- | ----- | ----- | ----- | ----- |
| A, B      |       |       |       |       |       |
| A, C      |       |       |       |       |       |
| A, D      |       |       |       |       |       |
| B, C      |       |       |       |       |       |
| B, D      |       |       |       |       |       |
| C, D      |       |       |       |       |       |
**Table VII**: Maximum statevector distance between two outputs for different chain lengths. 

| L   | `__dm_seigh_mm` | `__dm_dexpm_mm` | `__sm_sexpm_mm` | `__sm_expm_mult` |
| --- | --------------- | --------------- | --------------- | ---------------- |
| 2   |                 |                 |                 |                  |
| 3   |                 |                 |                 |                  |
| 4   |                 |                 |                 |                  |
| 5   |                 |                 |                 |                  |
| 6   |                 |                 |                 |                  |
| 7   |                 |                 |                 |                  |
| 8   |                 |                 |                 |                  |
| 9   |                 |                 |                 |                  |
| 10  |                 |                 |                 |                  |
| 11  |                 |                 |                 |                  |
| 12  |                 |                 |                 |                  |
| 13  |                 |                 |                 |                  |
| 14  |                 |                 |                 |                  |
| 15  |                 |                 |                 |                  |
| 16  |                 |                 |                 |                  |
| 17  |                 |                 |                 |                  |
| 18  |                 |                 |                 |                  |
| 19  |                 |                 |                 |                  |
| 20  |                 |                 |                 |                  |
| 21  |                 |                 |                 |                  |
| 22  |                 |                 |                 |                  |
**Table VIII**: Algorithm runtime averaged between different regimes.












all below is old

---
## Dense Matrix Time-Evolution
I will start with designing the time-evolution operations for dense matrices; as they are stored directly in memory, these will serve as the operations for smaller systems. Previously, I had shown that (on my laptop) around $L=8$ is where these algorithms tend to slow down significantly.

There are many different ways I can choose to implement these algorithms. I have implemented every algorithm in python code in the repository for Quantum Hysteresis. These functions will remain in the code to be run at any time, so that anyone working on this project can determine the best algorithm for their system. Overall, the main ideas were how we implement
 - Exponentiating the Hamiltonian
 - Applying the time evolution operator to the statevector
 - To what precision we want to store/calculate data

It is assumed that this evolution function will take in a `StateVector` for the input wavefunction, a `SparsePauliOp` for a Hamiltonian, and a singular `float` for time. It should also be mentioned that the default datatype for casting the `SparsePauliOp` is `complex128`.

To find the time-evolved state from these inputs, we can work through a list of possible operations we would step through procedurally in order to optimize for our benchmark ideals. After a lot of experimentation, I have determined the following list of operations to consider.

1. Cast Hamiltonian to `complex64` *before* exponentiation?
2. ~~Cast Generator to `complex64` *before* exponentiation?~~ (Redundant)
3. Which algorithm should we use to find the evolved state?
	1. If explicitly constructing the matrix exponentiation $U=e^A$ :
		1. `scipy.linalg.expm`
		2. `scipy.sparse.linalg.expm`
		3. `scipy/numpy.linalg.eigh`
	2. If explicitly doing the matrix multiplication $U\psi$ :
		1. `Statevector(U @ psi.data)`
		2. `Statevector.evolve(Operator(U))`
	3. If being clever doing both parts at once $e^A\psi$ :
		1. `scipy/numpy.linalg.eigh` with `V @ (exp_diag @ (V.conj().T @ psi))`
		2. `scipy.sparse.linalg.expm_multiply`
		3. `PauliEvolutionGate` (Trotterization)
4. Cast Evolution Operator to `complex64` *after* its creation?
5. Cast Statevector to `complex64` before matrix multiplication?

---
### Accuracy & Precision
After implementing the functions to test, I ran a benchmark that used the norm of the difference in the statevectors as a heuristic for closeness. In theory, if the two algorithms of furthest output statevectors were within a tolerance $\epsilon$, then it's reasonable to conclude that all algorithms of that batch generated the correct and same statevector up to floating-point errors.
#### Tests without Casting
I started by ignoring the `complex64` casting and the Trotterization simulation, as getting a baseline of the standard datatypes would help later on. I ran this benchmark with the following datapoints to be generated from
```python
h_list = np.linspace(0, 10, 10+1)
f_list = np.linspace(0, 1, 10+1)
times = np.linspace(0, 100, 10+1)
```
where there are 1331 datapoints per chain length. I believe that these give a wide-enough sampling of the different regimes to make conclusive statements about their efficacy. I ran this system with chain length from 2 to 8. Results of this benchmark can be found in **Table I**.

| Error      | $L=2$        | $L=3$        | $L=4$        | $L=5$        | $L=6$        | $L=7$        | $L=8$        |
| ---------- | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
| None       | 1            | 2            | 1            | 1            | 1            | 1            | 1            |
| $10^{-16}$ | 115          | 107          | 38           | 18           | 11           | 5            | 1            |
| $10^{-15}$ | 14           | 24           | 89           | 104          | 109          | 114          | 112          |
| $10^{-14}$ | 72           | 93           | 95           | 97           | 98           | 105          | 129          |
| $10^{-13}$ | 301          | 366          | 486          | 617          | 741          | 814          | 951          |
| $10^{-12}$ | 780          | 727          | 620          | 494          | 371          | 292          | 137          |
| $10^{-11}$ | 48           | 12           | 2            | 0            | 0            | 0            | 0            |
| Max        | $2.28_{-11}$ | $1.71_{-11}$ | $1.26_{-11}$ | $2.73_{-12}$ | $3.51_{-12}$ | $3.95_{-12}$ | $6.48_{-12}$ |
**Table I**: Maximum statevector distance between two outputs for different chain lengths.

With relatively high confidence, we can conclude that these algorithms do all correctly create the same statevectors up to floating-point error. With this confidence, we can instead move onto the speed of calculation for each algorithm.

---
### Runtime Speed
Given that these algorithms all produce the same state vector within tolerance, we can now look at their average runtime speed with the same inputs as previous. The data for this benchmark can be seen in **Table II**.

| Algorithm (avg)  | $L=2$      | $L=3$      | $L=4$      | $L=5$      | $L=6$      | $L=7$     |
| ---------------- | ---------- | ---------- | ---------- | ---------- | ---------- | --------- |
| `__dexpm_mm`     | 198.822 µs | 238.760 µs | 467.926 µs | 704.420 µs | 1.951 ms   | 38.204 ms |
| `__dexpm_qe`     | 181.770 µs | 237.414 µs | 442.118 µs | 1.206 ms   | 2.143 ms   | 38.552 ms |
| `__sexpm_mm`     | 306.745 µs | 448.347 µs | 714.519 µs | 1.021 ms   | 2.023 ms   | 46.817 ms |
| `__sexpm_qe`     | 303.414 µs | 414.482 µs | 736.079 µs | 2.092 ms   | 2.732 ms   | 58.121 ms |
| `__seig_expm_mm` | 189.435 µs | 232.982 µs | 338.118 µs | 1.197 ms   | 2.322 ms   | 30.764 ms |
| `__seig_expm_qe` | 165.101 µs | 234.591 µs | 320.253 µs | 2.548 ms   | 2.682 ms   | 28.484 ms |
| `__seig_mult`    | 143.618 µs | 215.621 µs | 435.172 µs | 1.182 ms   | 3.770 ms   | 25.901 ms |
| `__neig_expm_mm` | 171.992 µs | 209.591 µs | 304.114 µs | 1.278 ms   | 2.124 ms   | 28.542 ms |
| `__neig_expm_qe` | 139.421 µs | 223.613 µs | 278.288 µs | 1.304 ms   | 2.069 ms   | 25.485 ms |
| `__neig_mult`    | 131.455 µs | 190.590 µs | 404.027 µs | 439.665 µs | 2.974 ms   | 24.970 ms |
| `__expm_mult`    | 9.965 ms   | 9.706 ms   | 12.878 ms  | 13.870 ms  | 161.207 ms | ---       |
**Table II**: Algorithm runtime averaged over 1331 inputs for different chain lengths.

