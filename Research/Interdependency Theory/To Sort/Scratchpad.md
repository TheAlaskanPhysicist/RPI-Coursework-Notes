QAOA, Markov Chain

Look at up to N=3 or 4 explicit matrix

See higher order interactions summation 
Is there a relationship between N-1 and 1 interactions and N-2 and 2 interactions.

Spinodal Theory

HS-transform turns non-local to local
We transform from Non-Local, then simulate Quantum system on computer, then convert back to non-local 

Traveling Salesman: Take a network matrix, then total time is like sudoku. One per row one per column

Make a network of all natural numbers
Have weights be related to the fraction of the two values (1->4 being 1/4)
Transition from N to 1, including 1 to 1, you get the harmonic series

Andrew Damon: Sys Admin

DMRG: compute ground states of 1D gapped Hamiltonians efficiently

Avenue of potential interest: Tensor network comes from Hamiltonian.


OTOC, correlation
Odd of Time Order Correlator




## Theory
Suppose we have a spin chain of length $L$ with a transverse field defined for $x$ and spin in $z$.
Our Hamiltonian in this simplified case is:
$$\begin{align}
H&=E_0+h\sigma^x+\sum_{i<j} J_{ij}\sigma^z_i\sigma^z_j
\end{align}$$


$$\begin{align}
H&=E_0+\sum_{i}\left(h_i\sigma^x_i+h_i\sigma^y_i+h_i\sigma^z_i\right)\\
&+\sum_{i<j}J_{ij}^{zz}\sigma^z_i\sigma^z_j\\
&+\sum_{i<j} \left(J_{ij}^{zx}+J_{ij}^{xz}\right)\sigma^z_i\sigma^x_j\\
\end{align}$$







For 1 particle
$$\begin{align}
H&=E_0+C_x\sigma_x+C_y\sigma_y+C_z\sigma_z
\end{align}$$
For 2 particles
$$\begin{align}
H&=E_0\\
&+C_x\sigma_x^1+C_y\sigma_y^1+C_z\sigma_z^1\\
&+C_x\sigma_x^2+C_y\sigma_y^2+C_z\sigma_z^2\\
&+C_{xx}\sigma_x^1\sigma_x^2+C_{yy}\sigma_y^1\sigma_y^2+C_{zz}\sigma_z^1\sigma_z^2\\
&+C_{xy}\sigma_x^1\sigma_y^2+C_{yz}\sigma_y^1\sigma_z^2+C_{zx}\sigma_z^1\sigma_x^2\\
&+C_{xz}\sigma_x^1\sigma_z^2+C_{yx}\sigma_y^1\sigma_x^2+C_{zy}\sigma_z^1\sigma_y^2\\
\end{align}$$


Basic concept
$$\begin{align}
(C_x\sigma_x^1+C_y\sigma_y^1+C_z\sigma_z^1)(C_x\sigma_x^2+C_y\sigma_y^2+C_z\sigma_z^2)
\end{align}$$

$$\begin{align}
(\vec{C}^1\cdot\vec\sigma^1+\vec{C}^2\cdot\vec\sigma^2)^2&=\\
&+|\vec{C}^1|^2+|\vec{C}^2|^2\\
(C_xC_y-C_yC_x)\sigma_z^1\\
(C_zC_x-C_xC_z)\sigma_y^1\\
(C_yC_z-C_zC_y)\sigma_x^1\\
\\
(C_xC_y-C_yC_x)\sigma_z^2\\
(C_zC_x-C_xC_z)\sigma_y^2\\
(C_yC_z-C_zC_y)\sigma_x^2\\
\\
2(C_x^1\sigma_x^1+C_y^1\sigma_y^1+C_z^1\sigma_z^1)(C_x^2\sigma_x^2+C_y^2\sigma_y^2+C_z^2\sigma_z^2)
\end{align}$$






For a system of $N$ particle spins, we can represent the Hamiltonian as
$$\begin{align}
H&=
\end{align}$$



$$\begin{align}
H&=E_0+\sum_{k=1}^N\ \sum_{i_1=1}^{N}\sum_{i_2=1}^{N}\dots\sum_{i_k=1}^{N}\ \prod_{l=1}^k\sigma_{i_l}
\end{align}$$
This becomes more simplified with the following relationships:
$$\begin{align}
\sigma^i_a\sigma^j_b&=\sigma^i_a\sigma^j_b & i\ne j, a\ne b\\
\sigma^i_a\sigma^j_b&= & i\ne j, a=b\\
\sigma^i_a\sigma^j_b&= & i= j, a\ne b\\
\sigma^i_a\sigma^j_b&= & i= j, a= b\\
\end{align}$$







3-particle system
$$\begin{align}
H&=E_0\\
&+h_x\sigma_x^{1}+h_x\sigma_x^{2}+h_x\sigma_x^{3}+h_y^1\sigma_y+h_y^2\sigma_y+h_y^3\sigma_y+h_z^1\sigma_z+h_z^2\sigma_z+h_z^3\sigma_z\\
&+J_{xx}\sigma_x^{1}\sigma_x^{1}+J_{xx}\sigma_x^{1}\sigma_x^{1}
\end{align}$$






For $N$ spins, we have the general equation for all interactions
$$\begin{align}
H&=E+\sum_{i}h_i^x\sigma^x_i+h_i^y\sigma^y_i+h_i^z\sigma^z_i
\end{align}$$