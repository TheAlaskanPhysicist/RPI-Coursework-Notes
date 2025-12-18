This chapter is about the basis of angular momentum and related topics.



## Chapter 3 - Intelligently unlike Sakurai
Angular momentum operators are elements of the Lie Algebra $SU(2)$, denoted $\mathfrak{su}(2)$.
These are the generators of rotation in quantum mechanics.

**Commutator relations**
$$\begin{align}
[J_i,J_j]&=i\hbar\epsilon_{ijk}J_k
\end{align}$$
**Casimir Operator** (not a generator of the Lie Algebra)
$$\begin{align}
J^2&=J_x^2+J_y^2+J_z^2 & [J^2,J_i]&=0
\end{align}$$
**Eigenvalues**
$$\begin{align}
J^2\ket{j,m}&=j(j+1)\hbar^2\ket{j,m} & J_z\ket{j,m}&=m\hbar\ket{j,m}\\
[J_+,J_-]&=2\hbar J_z & [J_z,J_\pm]&=\pm\hbar J_\pm
\end{align}$$
**Ladder Operators**
$$\begin{align}
J_\pm&=J_x\pm iJ_y & J_{\pm}\ket{j,m}&=\sqrt{j(j+1)-m(m\pm1)}\ket{j,m\pm1}
\end{align}$$














## 3.1 Rotations and Angular Momentum Commutation Relations
---
### 3.1.1 Finite Versus Infinitesimal Rotations
Rotations around the same axis commute. Rotations about different axes do not.
The measure of how much they fail to commute is the commutator.
Rotation matrices satisfy $RR^T=R^TR=\mathbb{I}$ (preserves length).

The 3 Cartesian rotation matrices are:
$$\begin{align}
R_x(\phi)&=\begin{bmatrix}
1 & 0 & 0\\
0 & \cos\phi & -\sin\phi\\
0 & \sin\phi & \cos\phi
\end{bmatrix} & 
R_y(\phi)&=\begin{bmatrix}
\cos\phi & 0 & \sin\phi\\
0 & 1 & 0\\
-\sin\phi & 0 & \cos\phi
\end{bmatrix} & 
R_z(\phi)&=\begin{bmatrix}
\cos\phi & -\sin\phi & 0\\
\sin\phi & \cos\phi & 0\\
0&0&1
\end{bmatrix}
\end{align}$$
As $\phi\rightarrow\varepsilon\sim0$, we get the limiting commutator for infinitesimals:
$$\begin{align}
[R_x(\varepsilon),R_y(\varepsilon)]=\begin{bmatrix}
0&-\varepsilon^2&0\\\varepsilon^2&0&0\\0&0&0
\end{bmatrix}+O(\varepsilon^3)=R_z(\varepsilon^2)-\mathbb{I}
\end{align}$$
The commutator gets messy for finite rotations, and thus we want to express these as infinitesimal rotations using Lie Algebras.

---
### 3.1.2 Infinitesimal Rotations in Quantum Mechanics
For state vectors, we define the operator $\mathscr{D}(R)$ such that $\ket\psi_R=\mathscr{D}(R)\ket\psi$.
Rotations on state vectors are unitary operators that satisfy $UU^\dagger=U^\dagger U=\mathbb{I}$ (preserves length).

For infinitesimal rotations, we can approximate (linearize) the rotation operator
$$\begin{align}
U_\epsilon=\mathbb{I}-iG\epsilon
\end{align}$$
where $G$ is a Hermitian operator appropriate for the infinitesimal variable. For example:
$$\begin{align}
\epsilon&\rightarrow dx_\hat{r} & G&\rightarrow\dfrac{\vec{p}\cdot\hat{r}}{\hbar}\\
\epsilon&\rightarrow d\phi_{\hat{n}} & G&\rightarrow\dfrac{\hat{J}\cdot\hat{n}}{\hbar}\\
\epsilon&\rightarrow dt & G&\rightarrow\dfrac{\hat{H}}{\hbar}\\
\end{align}$$
The relationship between $G$ and $\epsilon$ is that they are Fourier duals of each other, with an dividing factor of $\hbar$ so that the product remains unitless.

---
### 3.1.3 Finite Rotations in Quantum Mechanics
To approach finite rotations, we can add the contribution of each infinitesimal rotation, as described by the Lie Algebra of rotations.

For an operator $G/\hbar$ that is Hermitian and satisfies $U(\epsilon)^n=U(n\epsilon)$, then this forms a group that has the relation between the algebra and group such that:
$$\begin{align}
U(G;a)&=e^{-iGa/\hbar}
\end{align}$$
This operator $G$ is a vector in the Lie Algebra of the Lie Group of the translation. For example:
$$\begin{align}
U(p_x,\Delta x)&=e^{-ip_x\Delta x/\hbar} & U(p_x,\Delta x)\ket{x}&=\ket{x+\Delta x} & \text{(Space Translation)}\\
U(\hat{H},\Delta t)&=e^{-i\hat{H}\Delta t/\hbar} & U(\hat{H},\Delta t)\ket{\psi(t)}&=\ket{\psi(t+\Delta t)} & \text{(Time Translation)}\\
\end{align}$$
---
### 3.1.4 Commutation Relations for Angular Momentum
In this framework, we see that the commutator relations for the angular momentum operator are:
$$\begin{align}
[J_i,J_j]&=i\hbar\epsilon_{ijk}J_k
\end{align}$$
Here, $J_k$ is the generator of rotation about the $k$ axis, and are not commutative.

For difference choices of the operators, we can see:
$$\begin{align}
\braket{J_x}&=_R\bra\psi J_x\ket\psi_R\\
&=\bra\psi e^{iJ_z\phi/\hbar}J_xe^{-iJ_z\phi/\hbar}\ket\psi\\
&=\bra\psi\left(J_x\cos\phi-J_y\sin\phi\right)\ket\psi\\
\braket{J_x}&=\braket{J_x}\cos\phi-\braket{J_y}\sin\phi\\
\Aboxed{J_x&=J_x\cos\phi-J_y\sin\phi}
\end{align}$$
The operation is not trivial since $J_x$ and $J_z$ do not commute, giving us the above.

---
## 3.2 Spin $\tfrac{1}{2}$ Systems and Finite Rotations
---
### 3.2.1 Rotation Operator for Spin $\tfrac{1}{2}$
The smallest matrices for angular momentum commutation relations is $2\times2$.

For spin-1/2 systems, the 4 basis operator elements are:
$$\begin{align}
S_x&=\dfrac{\hbar}{2}\left(\ket{\chi_{-}^Z}\bra{\chi_{+}^Z}+\ket{\chi_{+}^Z}\bra{\chi_{-}^Z}\right)\\
S_y&=\dfrac{\hbar}{2}i\left(\ket{\chi_{-}^Z}\bra{\chi_{+}^Z}-\ket{\chi_{+}^Z}\bra{\chi_{-}^Z}\right)\\
S_z&=\dfrac{\hbar}{2}\left(\ket{\chi_{+}^Z}\bra{\chi_{+}^Z}-\ket{\chi_{-}^Z}\bra{\chi_{-}^Z}\right)\\
S_\mathbb{I}&=\dfrac{\hbar}{2}\left(\ket{\chi_{+}^Z}\bra{\chi_{+}^Z}+\ket{\chi_{-}^Z}\bra{\chi_{-}^Z}\right)\\
\end{align}$$
which all but $S_\mathbb{I}$ satisfy the commutator relations since $S_\mathbb{I}$ isn't traceless.

For expected value calculations, we can find (by non-commutability), that:
$$\begin{align}
\braket{S_x}&\rightarrow\braket{S_x}\cos\phi-\braket{S_y}\sin\phi\\
\braket{S_y}&\rightarrow\braket{S_y}\cos\phi+\braket{S_x}\sin\phi\\
\braket{S_z}&\rightarrow\braket{S_z}
\end{align}$$
Under a rotation of $\phi$ in the $z$-axis, where $J_z$ is unchanged because $[J_z,J_z]=0$.
It should also be noted that the same holds for $S_\mathbb{I}$.

Something of note, suppose we rotate $\ket\psi$ by $2\pi$ radians, then:
$$\begin{align}
\ket\psi\rightarrow-\ket\psi
\end{align}$$
It requires $\phi=4\pi$ to return back to our original state, which is different than vectors. These objects of spin-1/2 are called *spinors*, and they rotate half as slowly than vectors.

---
### 3.2.2 Spin Precession Revisited
Under the effect of a magnetic field, dipoles have a phase that oscillates differently from the precession frequency:
$$\begin{align}
\tau_\text{precession}&=\dfrac{2\pi}{\omega}\\
\tau_\text{state vector}&=\dfrac{4\pi}{\omega}\\
\end{align}$$
This arises from the Hamiltonian having a term dependent on the spin of the state vector, and thus gaining a 1/2 in the phase factor term accordingly.

---
### 3.2.3 Neutron Interferometry Experiment to Study 2π Rotations
Not relevant, no notes.

---
### 3.2.4 Pauli Two-Component Formalism

---
### 3.2.5 Rotations in the Two-Component Formalism

---
## 3.3 SO(3), SU(2), and Euler Rotations
---
### 3.3.1 Orthogonal Group

---
### 3.3.2 Unitary Unimodular Group

---
### 3.3.3 Euler Rotations

---
## 3.4 Density Operators and Pure Versus Mixed Ensembles
---
### 3.4.1 Polarized Versus Unpolarized Beams

---
### 3.4.2 Ensemble Averages and Density Operator

---
### 3.4.3 Time Evolution of Ensembles

---
### 3.4.4 Continuum Generalizations

---
### 3.4.5 Quantum Statistical Mechanics

---
## 3.5 Eigenvalues and Eigenstates of Angular Momentum

---
### 3.5.1 Commutation Relations and the Ladder Operators

---
### 3.5.2 Eigenvalues of $J^2$ and $J_z$

---
### 3.5.3 Matrix Elements of Angular-Momentum Operators

---
### 3.5.4 Representations of the Rotation Operator

---
## 3.6 Orbital Angular Momentum

---
### 3.6.1 Orbital Angular Momentum as Rotation Generator

---
### 3.6.2 Spherical Harmonics

---
### 3.6.3 Spherical Harmonics as Rotation Matrices

---
## 3.7 Schrödinger’s Equation for Central Potentials

---
### 3.7.1 The Radial Equation

---
### 3.7.2 The Free Particle and Infinite Spherical Well

---
### 3.7.3 The Isotropic Harmonic Oscillator

---
### 3.7.4 The Coulomb Potential

---
## 3.8 Addition of Angular Momenta

---
### 3.8.1 Simple Examples of Angular-Momentum Addition

---
### 3.8.2 Formal Theory of Angular-Momentum Addition

---
### 3.8.3 Recursion Relations for the Clebsch–Gordan Coefficients

---
### 3.8.4 Clebsch–Gordan Coefficients and Rotation Matrices

---
## 3.9 Schwinger’s Oscillator Model of Angular Momentum

---
### 3.9.1 Angular Momentum and Uncoupled Oscillators

---
### 3.9.2 Explicit Formula for Rotation Matrices

---
## 3.10 Spin Correlation Measurements and Bell’s Inequality
---
### 3.10.1 Correlations in Spin-Singlet States

---
### 3.10.2 Einstein’s Locality Principle and Bell’s Inequality

---
### 3.10.3 Quantum Mechanics and Bell’s Inequality

---
## 3.11 Tensor Operators

---
### 3.11.1 Vector Operator

---
### 3.11.2 Cartesian Tensors Versus Irreducible Tensors

---
### 3.11.3 Product of Tensors

---
### 3.11.4 Matrix Elements of Tensor Operators; the Wigner-Eckart Theorem
