

## Symmetries

### Coulomb Potential
For the Coulomb potential, we have a constant:
$$\begin{align}
\vec{M}&=\dfrac{\vec{p}\times\vec{L}}{m}-\dfrac{Ze^2}{r}\vec{x} && \text{(Classical)}\\
\vec{M}&=\dfrac{\vec{p}\times\vec{L}-\vec{L}\times\vec{p}}{2m}-\dfrac{Ze^2}{r}\vec{x} && \text{(Quantum)}
\end{align}$$
This commutes with the Hamiltonian and is orthogonal to $\vec{L}$.
### Space Parity
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
### Lattice Transform Symmetry
For a periodic potential, we have the translation operator:
$$\begin{align}
\tau^\dagger(l)x\tau(l)&=x+l & \tau(l)\ket{x'}&=\ket{x'+l}
\end{align}$$
This commutes with the Hamiltonian when the potential is also periodic:
$$\begin{align}
\tau^\dagger(l)H\tau(l)&=H &\iff&& \left[\tau(l),H\right]&=0
\end{align}$$
### Time-Reversal Symmetry
Let there be a $\Theta$ that is our time-reversal operator. Such operator has the following properties:
$$\begin{align}
-iH\Theta&=\Theta iH & \left\{\Theta,iH\right\}&=0\\
H\Theta&=\Theta H & \left[\Theta,H\right]&=0\\
\end{align}$$
## Perturbation Theory
---
### Non-Degenerate, Time Independent
Define a system's Hamiltonian to be the sum of a neutral Hamiltonian and a perturbation:
$$\begin{align}
H&=H_0+\lambda V
\end{align}$$
The system can then be expressed in terms of order $\lambda$:
$$\begin{align}
(H_0+\lambda V)\left(\ket{n^{(0)}}+\lambda\ket{n^{(1)}}+\dots\right)&=\left(E_n^{(0)}+\lambda E_n^{(1)}+\dots\right)\left(\ket{n^{(0)}}+\lambda\ket{n^{(1)}}+\dots\right)
\end{align}$$
The first few order perturbations for energy are:
$$\begin{align}
E_n^{(0)}&=\bra{n^{(0)}}H_0\ket{n^{(0)}}\\
E_n^{(1)}&=\bra{n^{(0)}}V\ket{n^{(0)}}\\
E_n^{(2)}&=\sum_{k\neq n}\dfrac{\left|\bra{k^{(0)}}V\ket{n^{(0)}}\right|^2}{E_n^{(0)}-E_k^{(0)}}\\
E_n^{(3)}&=\sum_{k\neq n}\sum_{l\neq n}\dfrac{\bra{n^{(0)}}V\ket{l^{(0)}}\bra{l^{(0)}}V\ket{k^{(0)}}\bra{k^{(0)}}V\ket{n^{(0)}}}{\left(E_n^{(0)}-E_l^{(0)}\right)\left(E_n^{(0)}-E_k^{(0)}\right)}\\
&-\bra{n^{(0)}}V\ket{n^{(0)}}\sum_{k\neq n}\dfrac{\left|\bra{n^{(0)}}V\ket{k^{(0)}}\right|^2}{\left(E_n^{(0)}-E_k^{(0)}\right)^2}
\end{align}$$
For the perturbation of states, the first few order corrections are:
$$\begin{align}
\ket{n^{(1)}}&=\sum_{k\ne n}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{n^{(0)}}}{E_n^{(0)}-E_k^{(0)}}\\
\ket{n^{(2)}}&=\sum_{k\ne n}\sum_{l\ne n}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{l^{(0)}}}{E_n^{(0)}-E_k^{(0)}}\dfrac{\bra{l^{(0)}}V\ket{n^{(0)}}}{E_n^{(0)}-E_l^{(0)}}\\
&-\sum_{k\ne n}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{n^{(0)}}\bra{n^{(0)}}V\ket{n^{(0)}}}{\left(E_n^{(0)}-E_k^{(0)}\right)^2}\\
&-\dfrac{1}{2}\ket{n^{(0)}}\sum_{k\ne n}\dfrac{\left|\bra{k^{(0)}}V\ket{n^{(0)}}\right|^2}{\left(E_n^{(0)}-E_k^{(0)}\right)^2}
\end{align}$$
---
### Degenerate, Time Independent
Identical to before, but over a smaller state space.

The first few order perturbations for energy are:
$$\begin{align}
E_{n}^{(0)}&=\bra{n,\alpha}H_0\ket{n,\alpha}\\
E_{n,\alpha}^{(1)}&=\text{Eigenvalues of }\bra{n,a}V\ket{n,b}\\
E_{n,\alpha}^{(2)}&=\sum_{k\not\in D}\dfrac{\left|\bra{k^{(0)}}V\ket{n,\alpha^{(0)}}\right|^2}{E_n^{(0)}-E_k^{(0)}}\\
E_{n,\alpha}^{(3)}&=\sum_{k\not\in D}\sum_{l\not\in D}\dfrac{\bra{n,\alpha^{(0)}}V\ket{l^{(0)}}\bra{l^{(0)}}V\ket{k^{(0)}}\bra{k^{(0)}}V\ket{n,\alpha^{(0)}}}{\left(E_n^{(0)}-E_l^{(0)}\right)\left(E_n^{(0)}-E_k^{(0)}\right)}\\
&-\bra{n,\alpha^{(0)}}V\ket{n,\alpha^{(0)}}\sum_{k\not\in D}\dfrac{\left|\bra{n,\alpha^{(0)}}V\ket{k^{(0)}}\right|^2}{\left(E_n^{(0)}-E_k^{(0)}\right)^2}
\end{align}$$
For the perturbation of states, the first few order corrections are:
$$\begin{align}
\ket{n,\alpha^{(1)}}&=\sum_{k\not\in D}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{n,\alpha^{(0)}}}{E_n^{(0)}-E_k^{(0)}}\\
\ket{n,\alpha^{(2)}}&=\sum_{k\not\in D}\sum_{l\not\in D}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{l^{(0)}}}{E_n^{(0)}-E_k^{(0)}}\dfrac{\bra{l^{(0)}}V\ket{n,\alpha^{(0)}}}{E_n^{(0)}-E_l^{(0)}}\\
&-\sum_{k\not\in D}\ket{k^{(0)}}\dfrac{\bra{k^{(0)}}V\ket{n,\alpha^{(0)}}\bra{n,\alpha^{(0)}}V\ket{n,\alpha^{(0)}}}{\left(E_n^{(0)}-E_k^{(0)}\right)^2}
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

