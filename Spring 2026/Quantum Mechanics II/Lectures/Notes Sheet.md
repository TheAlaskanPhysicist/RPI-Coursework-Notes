

## 4. Symmetry of Quantum Mechanics
### 4.1 Symmetries, Conservation Laws, and Degeneracies
For the Coulomb potential, we have a constant:
$$\begin{align}
\vec{M}&=\dfrac{\vec{p}\times\vec{L}}{m}-\dfrac{Ze^2}{r}\vec{x} && \text{(Classical)}\\
\vec{M}&=\dfrac{\vec{p}\times\vec{L}-\vec{L}\times\vec{p}}{2m}-\dfrac{Ze^2}{r}\vec{x} && \text{(Quantum)}
\end{align}$$
This commutes with the Hamiltonian and is orthogonal to $\vec{L}$.
### 4.2 Discrete Symmetries, Parity, or Space Inversion
The operator $\pi$ applied twice returns our system to identity, and so:
$$\begin{align}
\pi=\pi^\dagger=\pi^{-1}
\end{align}$$
This space parity operator has the following commutators:
$$\begin{align}
\pi^\dagger\vec{x}\pi&=-\vec{x} &\iff&& \left\{\pi,\vec{x}\right\}&=0\\
\pi^\dagger\vec{p}\pi&=-\vec{p} &\iff&& \left\{\pi,\vec{p}\right\}&=0\\
\pi^\dagger\vec{L}\pi&=\vec{L} &\iff&& \left[\pi,\vec{L}\right]&=0\\
\pi^\dagger\vec{S}\pi&=\vec{S} &\iff&& \left[\pi,\vec{S}\right]&=0\\
\pi^\dagger\vec{J}\pi&=\vec{J} &\iff&& \left[\pi,\vec{J}\right]&=0\\
\end{align}$$
For a central potential wavefunction, parity gives us the following:
$$\begin{align}
\pi\ket{n,l,m}&=(-1)^l\ket{n,l,m}
\end{align}$$
### 4.3 Lattice Translation as a Discrete Symmetry
For a periodic potential, we have the translation operator:
$$\begin{align}
\tau^\dagger(l)x\tau(l)&=x+l & \tau(l)\ket{x'}&=\ket{x'+l}
\end{align}$$
This commutes with the Hamiltonian when the potential is also periodic:
$$\begin{align}
\tau^\dagger(l)H\tau(l)&=H &\iff&& \left[\tau(l),H\right]&=0
\end{align}$$
### 4.4 The Time-Reversal Discrete Symmetry
Let there be a $\Theta$ that is our time-reversal operator. Such operator has the following properties:
$$\begin{align}
-iH\Theta&=\Theta iH & \left\{\Theta,iH\right\}&=0\\
H\Theta&=\Theta H & \left[\Theta,H\right]&=0
\end{align}$$
For spherical harmonics, we have the relations:
$$\begin{align}
\Theta\ket{n,l,m}&=(-1)^m\ket{n,l,-m} & \Theta\ket{j,m}&=i^{2m}\ket{j,-m}
\end{align}$$
## 5. Approximation Methods
### 5.1 Time-Independent Perturbation Theory: Non-Degenerate
Define a system's Hamiltonian to be the sum of a neutral Hamiltonian and a perturbation:

The system can then be expressed in terms of order $\lambda$:
$$\begin{align}
(H_0+\lambda V)\left(\ket{n^{(0)}}+\lambda\ket{n^{(1)}}+\dots\right)&=\left(E_n^{(0)}+\lambda E_n^{(1)}+\dots\right)\left(\ket{n^{(0)}}+\lambda\ket{n^{(1)}}+\dots\right)
\end{align}$$
The first few order perturbations for energy are:
$$\begin{align}
E_n^{(1)}&=\bra{n^{(0)}}V\ket{n^{(0)}} & 
E_n^{(2)}&=\sum_{k\neq n}\dfrac{\left|\bra{k^{(0)}}V\ket{n^{(0)}}\right|^2}{E_n^{(0)}-E_k^{(0)}}
\end{align}$$
For the perturbation of states, the first few order corrections are:
$$\begin{align}
\ket{n^{(1)}}&=\sum_{k\ne n}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{n^{(0)}}}{E_n^{(0)}-E_k^{(0)}}\\
\ket{n^{(2)}}&=\sum_{k\ne n}\sum_{l\ne n}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{l^{(0)}}}{E_n^{(0)}-E_k^{(0)}}\dfrac{\bra{l^{(0)}}V\ket{n^{(0)}}}{E_n^{(0)}-E_l^{(0)}}-\sum_{k\ne n}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{n^{(0)}}\bra{n^{(0)}}V\ket{n^{(0)}}}{\left(E_n^{(0)}-E_k^{(0)}\right)^2}
\end{align}$$
### 5.2 Time-Independent Perturbation Theory: Degenerate
The first few order perturbations for energy are:
$$\begin{align}
E_{n,\alpha}^{(1)}&=\text{Eigenvalues of }\bra{n,a}V\ket{n,b}\\
E_{n,\alpha}^{(2)}&=\sum_{k\not\in D}\dfrac{\left|\bra{k^{(0)}}V\ket{n,\alpha^{(0)}}\right|^2}{E_n^{(0)}-E_k^{(0)}}
\end{align}$$
For the perturbation of states, the first few order corrections are:
$$\begin{align}
\ket{n,\alpha^{(1)}}&=\sum_{k\not\in D}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{n,\alpha^{(0)}}}{E_n^{(0)}-E_k^{(0)}}\\
\ket{n,\alpha^{(2)}}&=\sum_{k\not\in D}\sum_{l\not\in D}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{l^{(0)}}}{E_n^{(0)}-E_k^{(0)}}\dfrac{\bra{l^{(0)}}V\ket{n,\alpha^{(0)}}}{E_n^{(0)}-E_l^{(0)}}-\sum_{k\not\in D}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{n,\alpha^{(0)}}\bra{n,\alpha^{(0)}}V\ket{n,\alpha^{(0)}}}{\left(E_n^{(0)}-E_k^{(0)}\right)^2}
\end{align}$$
### 5.3 Hydrogen-like Atoms
The hydrogen atom starts with the Hamiltonian:
$$\begin{align}
H_0&=-\dfrac{\hbar^2}{2m}\vec\nabla^2-\dfrac{Ze^2}{r}
\end{align}$$
Suppose we add an electric field $\vec{E}=\text{E}\hat{z}$, then we have our new system:
$$\begin{align}
V&=-e\text{E}z=-e\text{E}\cdot r\cos\theta
\end{align}$$
For a hydrogen atom, we have our states and energy of them form:
$$\begin{align}
\ket{nlm}&=R_{nl}(r)Y_{lm}(\theta,\phi) & E=E_n
\end{align}$$
We will exploit the normalization of these wavefunctions, where:
$$\begin{align}
\int r^2R_{nl}(r)R_{n'l'}(r)dr&=\delta_{nn'}\delta_{ll'} & \int Y_{l'm'}^*(\theta,\phi)Y_{lm}(\theta,\phi)\ d\Omega&=\delta_{ll'}\delta_{mm'}
\end{align}$$
Thus we need to diagonalize our potential among the states $n=n'$, and so:
$$\begin{align}
\bra{nl'm'}V\ket{nlm}&=-e\text{E}\int rR_{nl}(r)R_{nl'}(r)\ r^2\ dr\int Y_{l'm'}^*(\theta,\phi)Y_{lm}(\theta,\phi)\cos\theta\sin\theta\ d\theta\ d\phi
\end{align}$$







The integral of interest:
$$\begin{align}
I&=\int_0^\infty r^{k+2}R_{n'l'}(r)R_{nl}(r)\ dr\\
&=\delta_{nn'}\delta_{ll'}\dfrac{(n-l-1)!}{2n\cdot(n+l)!}\left(\dfrac{n}{2Z}\right)^{k}\int_0^\infty u^{k+2l+2}e^{-u}\left[L_{n-l-1}^{2l+1}\left(u\right)\right]^2\ du\\
&=\delta_{nn'}\delta_{ll'}\dfrac{(n-l-1)!}{2n\cdot(n+l)!}\left(\dfrac{n}{2Z}\right)^{k}\sum_{m,m'=0}^{n-l-1} (-1)^{m+m'}\dfrac{(2l+1+m)!}{(2l+1)!m!}\dfrac{(2l+1+m')!}{(2l+1)!m'!}\Gamma\left(k+m+m'+2l+3\right)\\
&=\delta_{nn'}\delta_{ll'}\dfrac{(n-l-1)!}{2n\cdot(n+l)!}\left(\dfrac{n}{2Z}\right)^{k}\sum_{a=0}^{2(n-l-1)}\sum_{m=0}^{a} (-1)^{a}\dfrac{(2l+1+m)!}{[(2l+1)!]^2}\dfrac{(2l+1+a-m)!}{m!(a-m)!}\left(2l+2+a+k\right)!\\
\end{align}$$





---
### Non-Degenerate, Time Dependent
Define a system's Hamiltonian to be the sum of a neutral Hamiltonian and a perturbation:
$$\begin{align}
H(t)&=H_0+\lambda V(t)
\end{align}$$
We have the unperturbed eigenstates, and can use it as a basis:
$$\begin{align}
H_0\ket{n}&=E_n\ket{n} & \ket{\psi;t}&=\sum_{n}c_n(t)e^{-iE_nt/\hbar}\ket{n}
\end{align}$$
The coefficients for a general wavefunction come from solving:
$$\begin{align}
i\hbar\dfrac{dc_n}{dt}&=\sum_{m}\bra{n}V(t)\ket{m}\ e^{i\omega_{nm}t}c_m(t) & \omega_{nm}&=\dfrac{E_n-E_m}{\hbar}
\end{align}$$
Each coefficient can be expanded as a series with initial conditions:
$$\begin{align}
c_n(t)&=c_n^{(0)}(t)+c_n^{(1)}(t)+c_n^{(2)}(t)+\dots & c_{n=I}(t)&=1 & c_{n\neq I}(t)&=0
\end{align}$$
The first-order transition amplitude and probability is:
$$\begin{align}
c_F^{(1)}(t)&=\dfrac{1}{i\hbar}\int_{0}^t dt'\ V_{FI}(t')e^{i\omega_{FI}t'}\\
P^{(1)}_{I\to F}(t)&=\left|c_F^{(1)}(t)\right|^2
\end{align}$$
The second-order transition amplitude and probability is:
$$\begin{align}
c_F^{(2)}(t)&=\dfrac{1}{(i\hbar)^2}\sum_{m}\int_{0}^tdt'\int_{0}^{t'}dt''\ V_{Fm}(t')V_{mI}(t'')e^{i\omega_{Fm}t'}e^{i\omega_{mI}t''}\\
P^{(2)}_{I\to F}(t)&=\left|c_F^{(2)}(t)\right|^2
\end{align}$$
More generally, we see the following Dyson series:
$$\begin{align}
c_{S_N}^{(N)}(t_0)&=\dfrac{1}{(i\hbar)^N}\prod_{k=1}^{N}\int_{0}^{t_{k-1}}dt_k\ V_{S_kS_{k-1}}(t_{N-k+1})e^{i\omega_{S_kS_{k-1}}t_{N-k+1}}\\
P^{(N)}_{S_0\to S_N}(t)&=\left|c_{S_N}^{(N)}(t_0)\right|^2
\end{align}$$
Where $\ket{S_0}=\ket{I}$ and $\ket{S_N}=\ket{F}$, providing a complete picture of the perturbation.

---
#### Adiabatic Perturbation
Perturbation changes very slowly, as in:
$$\begin{align}
\left|\dfrac{\bra{m}\dot{H}\ket{n}}{(E_n-E_m)^2}\right|&\ll 1 &\implies&& \ket{n}_\text{old}\to\ket{n}_\text{new}
\end{align}$$
Eigenstates stays in a particular eigenstate, even if the eigenstate itself it changing.

---
#### Periodic Perturbation
Suppose we have a perturbation of the form $V(t)=Ve^{-i\omega t}$, then our transition amplitudes are:
$$\begin{align}
c_F^{(1)}(t)&=\dfrac{V_{FI}}{i\hbar}\int_{0}^t dt'\ e^{i(\omega_{FI}-\omega)t'}
\end{align}$$
Resonance is found when $\omega\approx\omega_{FI}$, as in most likely to transition when near resonance.

---
#### Fermi's Golden Rule
For a continuum of final states (typical in large ensembles) at equilibrium $(t\to\infty)$:
$$\begin{align}
\Gamma_{I\to F}&=\dfrac{2\pi}{\hbar}\left|V_{FI}\right|^2\rho\left(E_F\right)
\end{align}$$
Where $\rho$ is the density of states in state space.

