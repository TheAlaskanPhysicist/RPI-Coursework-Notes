**Author:** Stanley Goodwin
**Date:** April 12th, 2026

---
## Choosing an Evolution Operator
In implementing different evolution mechanisms for an initial all-spin-up state, there we multiple different ways with different assumptions and cheats to get around computation. In constructing the Hamiltonian, we keep it as a `SparsePauliOperator`.

The naive approach is to calculate the evolution operator using
```python
from scipy.linalg import expm
expm(-1j * sparse_matrix.to_matrix() * t)
```
This becomes slow pretty quickly, at $0.315\text{s/state}$ at $L=12$. Instead using the sparse linear algebra from `scipy.sparse.linalg` actually increases the time per state since our `to_matrix()` casts our sparse matrix into a dense matrix. There also exists a flag `sparse=True` for `.to_matrix`, but the cost of exponentiation is still about the same.

Instead, to increase the speed of computation speed, there is another function
```python
from scipy.sparse.linalg import expm_multiply
expm_multiply(-1j * sparse_matrix.to_matrix() * t, psi.data)
```
This implementation requires the state as an input, but massively shortcuts a lot of the computation, since our initial state of evolution is all-up spins. This does improve performance a bit, but drops off pretty similarly to previous implementations due to the `.to_matrix` creating a dense matrix in memory. However, the flag `sparse=True` does make a difference
```python
from scipy.sparse.linalg import expm_multiply
expm_multiply(-1j * sparse_matrix.to_matrix(sparse=True) * t, psi.data)
```
Previously, our fastest calculation was $0.315\text{s/state}$ at $L=12$; with this new implementation, we instead have $0.417\text{s/state}$ at $L=20$, and the rate at which the computation time increases seems to only $\sim2\times$ for $L\to L+1$, instead of $\sim4\times$ of the alternative, as well as being faster as a baseline for chain lengths $L\ge8$.

---
### Prototyping Benchmarking Implementations
For the implementations mentioned in [[#Choosing an Evolution Operator]], I made a table of the time each algorithm required to calculate $101$ state evolutions per chain length $L$.

| L   | `expm`     | `sparse.expm` | `expm_multiply` | `expm_multiply(sparse=true)` |
| --- | ---------- | ------------- | --------------- | ---------------------------- |
| 2   | 30.513 ms  | 52.733 ms     | 47.801 ms       | 123.533 ms                   |
| 3   | 44.153 ms  | 61.976 ms     | 58.018 ms       | 144.108 ms                   |
| 4   | 50.341 ms  | 73.991 ms     | 68.984 ms       | 119.283 ms                   |
| 5   | 59.355 ms  | 169.347 ms    | 77.771 ms       | 114.457 ms                   |
| 6   | 60.336 ms  | 226.638 ms    | 227.100 ms      | 115.037 ms                   |
| 7   | 77.795 ms  | 416.738 ms    | 310.254 ms      | 129.969 ms                   |
| 8   | 270.656 ms | 2.064 s       | 542.760 ms      | 118.990 ms                   |
| 9   | 736.168 ms | 6.920 s       | 1.327 s         | 136.970 ms                   |
| 10  | 2.348 s    | 33.221 s      | 3.997 s         | 158.772 ms                   |
| 11  | 8.055 s    | -             | 13.730 s        | 173.241 ms                   |
| 12  | 31.840 s   | -             | 57.948 s        | 217.209 ms                   |
| 13  |            |               |                 | 298.042 ms                   |
| 14  |            |               |                 | 492.460 ms                   |
| 15  |            |               |                 | 1.063 s                      |
| 16  |            |               |                 | 2.581 s                      |
| 17  |            |               |                 | 5.377 s                      |
| 18  |            |               |                 | 10.532 s                     |
| 19  |            |               |                 | 21.165 s                     |
| 20  |            |               |                 | 42.137 s                     |
| 21  |            |               |                 | 91.707 s                     |
| 22  |            |               |                 | 184.157 s                    |
The table very clearly outlines that there is a benefit in using sparse `expm_multiply` for chain lengths $L\ge8$, while smaller chains are faster brute-forced as dense matrices. 

---
### Further Benchmarking
To refine our initial findings, I wrote code that exclusively benchmarks each implementation, and compares their outputs to make sure that all implementations produce the same state-vector.

We will change 4 different parameters. They are the following:
1. Exponentiation type
	1. Dense exponentiation `scipy.linalg.expm(A)`
	2. Sparse exponentiation `scipy.sparse.linalg.expm(A)`
	3. Action exponentiation `scipy.sparse.linalg.expm_multiply(A, v)`
2. Matrix type
	1. Dense `.to_matrix(sparse=False)`
	2. CSR `.to_matrix(sparse=True)`
	3. CSC `.to_matrix(sparse=True).tocsc()`
3. Evolving type
	1. Qiskit `psi.evolve(operator)`
	2. Raw `operator @ psi.data`
	3. Integrated `expm_multiply`
4. Precision
	1. `np.complex128`
	2. `np.complex64

I ran the benchmarks up to $L=18$ at the maximum. A table of the difference choices is below

| Algorithm | Max $L\le1\text{ s}$ |     |
| --------- | -------------------- | --- |
| dedmqehp  | 10                   |     |
| dedmqelp  | 10                   |     |
| dedmrehp  | 10                   |     |
| dedmrelp  | 10                   |     |
| sedmqehp  | 10                   |     |
| sedmqelp  | 10                   |     |
| sedmrehp  | 10                   |     |
| sedmrelp  | 10                   |     |
| sermrehp  | 8                    |     |
| sermrelp  | 8                    |     |
| secmrehp  | 8                    |     |
| secmrelp  | 8                    |     |
| medmhp    | 11                   |     |
| medmlp    | 11                   |     |
| mermhp    | 15                   |     |
| mermlp    | 15                   |     |
| mecmhp    | 15                   |     |
| mecmlp    | 15                   |     |
Some algorithms are missing, but that is because they are (slower) duplicates of another algorithm, or their parameters are incompatible with each other, so they are omitted.

---
### Further Benchmarking Analysis
This dataset was constructed for systems up to a chain length of $L=18$. I stopped simulating an algorithm once the average time per state was greater than $1$ second. A summary of my findings from the dataset, in terms of time optimization, are as follows:
 - `expm_multiply` is always better for $N\ge8$.
 - `expm_multiply` with `sparse=True` is always better for $N\ge7$.
 - There is little difference between `complex128` and `complex64`.
 - Qiskit's `.evolve()` tends to be faster for $N\ge7$.

For simulating lots of states, we will want to consider two regimes since the most optimal algorithm for large $N$ is awful at smaller $N$.
$$\begin{align}
&\text{scipy.linalg.expm} && \text{sparse=false} && \text{operator @ psi.data} & N\le6 \\
&\text{scipy.linalg.expm\_multiply} && \text{sparse=true} && \text{N/A} & N\ge7 \\
\end{align}$$
---
