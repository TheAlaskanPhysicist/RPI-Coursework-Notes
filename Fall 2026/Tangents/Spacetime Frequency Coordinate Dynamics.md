# Guiding Idea
The idea is that if in normal systems, we tend to want to look at systems at equal times, and in some way we integrate over all position space. We also have the idea of a spacetime interval being constant for spacetime position coordinates. What I was thinking is that systems at equal energies (constant E) and we integrate over all frequency space. The spacetime interval equivalent then becomes mass. I find this idea interesting because it means in a way that if you represent a system in spacetime position coordinates you get Lorentz-Invariant spacetime intervals, while representing that system in spacetime frequency coordinates gets you Lorentz-Invariant mass.
$$\begin{align}
(ct)^2-\vec{x}^2&=s^2 &\iff&& (E/c)^2-p^2&=(mc)^2\\
t^2-(\vec{x}/c)^2&=t_\mathcal{O}^2 &\iff&& (E)^2-(pc)^2&=E_\mathcal{O}^2
\end{align}$$

# Klein-Gordon Representations
To make the parallels clearer, we'll be using the following notation

| Object               | Position Coordinates                             | Frequency Coordinates                              |
| -------------------- | ------------------------------------------------ | -------------------------------------------------- |
| Scalar Field         | $\phi=\phi(x)$                                   | $\Pi=\Pi(k)$                                       |
| Conjugate Field      | $\pi=\pi(x)$                                     | $\Phi=\Phi(k)$                                     |
| Action               | $A[\phi(x)]$                                     | $B[\Pi(k)]$                                        |
| Lagrangian Density   | $\mathcal{L}=\mathcal{L}(\phi,\partial_\mu\phi)$ | $\mathscr{L}=\mathscr{L}(\Pi,\partial_{k_\mu}\Pi)$ |
| Evolution Parameter  | $t=x^0$                                          | $\omega=k_0$                                       |
| Evolution Generator  | $\mathcal{H}(\phi,\pi)$ and $H(t)$               | $\mathcal{T}(\Pi,\Phi)$ and $T(\omega)$            |
| Canonical Coordinate | $\hat{X}^\mu$                                    | $\hat{K}_\mu$                                      |
| Canonical Conjugate  | $\hat{P}_\mu$                                    | $\hat{\chi}^\mu$                                   |
## Euler-Lagrange Equations
Let $\phi(x),\Phi(k)$ be real scalar fields, where $x^\mu(t,\vec{x})$, $k_\mu=(\omega,-\vec{k})$. The actions are
$$\begin{align}
A[\phi]&=\int d^4x\ \mathcal{L}(\phi,\partial_\mu\phi) &&&
\mathcal{L}&=\dfrac{1}{2}\partial_\mu\phi\ \partial^\mu\phi-\dfrac{1}{2}m^2\phi^2\\
B[\Pi]&=\int d^4k\ \mathscr{L}(\Pi,\partial_{k_\mu}\Pi) &&&
\mathscr{L}&=\dfrac{1}{2}\partial_{k_\mu}\Pi\ \partial_{k^\mu}\Pi-\dfrac{1}{2}\mu^2\Pi^2
\end{align}$$
We can vary both actions to find that the Euler-Lagrange equations are
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial\phi}-\partial_\mu\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}&=0, &
\dfrac{\partial\mathcal{L}}{\partial\phi}&=-m^2\phi, &
\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}&=\partial^\mu\phi\\
\dfrac{\partial\mathscr{L}}{\partial\Pi}-\dfrac{\partial}{\partial k_\mu}\dfrac{\partial\mathscr{L}}{\partial(\partial_{k_\mu}\Pi)}&=0, &
\dfrac{\partial\mathscr{L}}{\partial\Pi}&=-\mu^2\Pi, &
\dfrac{\partial\mathscr{L}}{\partial(\partial_{k_\mu}\Pi)}&=\partial_{k^\mu}\Pi
\end{align}$$
## Hamilton Form
To find constant hypersurfaces, let $t=x^0$ and $\omega=k_0$ be the evolution parameters. These are akin to having constant time and constant energy hypersurfaces. We can define the canonical coordinates to each field to be
$$\begin{align}
\pi(x)&=\dfrac{\partial\mathcal{L}}{\partial(\partial_t\phi)}
&\implies&& 
\pi&=\partial_t\phi && \text{(In KG)}\\
\Phi(k)&=\dfrac{\partial\mathscr{L}}{\partial(\partial_\omega\Pi)}
&\implies&&
\Phi&=\partial_\omega\Pi && \text{(In KG)}
\end{align}$$
We can then do the Legendre transform to find the Hamiltonian and alternate operators
$$\begin{align}
\mathcal{H}&=\pi\cdot\partial_t\phi-\mathcal{L} &\implies&&
\mathcal{H}&=\dfrac{1}{2}\pi^2+\dfrac{1}{2}(\nabla\phi)^2+\dfrac{1}{2}m^2\phi^2\\
\mathcal{T}&=\Phi\cdot\partial_\omega\Pi-\mathscr{L} &\implies&&
\mathcal{T}&=\dfrac{1}{2}\Phi^2+\dfrac{1}{2}(\nabla_{\vec{k}}\Pi)^2+\dfrac{1}{2}\mu^2\Pi^2
\end{align}$$
Lastly we can integrate these over their non-evolution parameter to get
$$\begin{align}
H(t)&=\int d^3x\ \mathcal{H} &&& T(\omega)&=\int d^3k\ \mathcal{T}
\end{align}$$
## Commutators
On the constant-parameter hypersurface, we have the commutators
$$\begin{align}
\left[\hat\phi(t,\vec{x}),\hat\pi(t,\vec{x}')\right]&=i\hbar\delta^{3}(\vec{x}-\vec{x}') &&&
\left[\hat\phi(t,\vec{x}),\hat\phi(t,\vec{x}')\right]&=0=\left[\hat\pi(t,\vec{x}),\hat\pi(t,\vec{x}')\right]\\
\left[\hat\Pi(\omega,\vec{k}),\hat\Phi(\omega,\vec{k}')\right]&=i\hbar\delta^{3}(\vec{k}-\vec{k}') &&& \left[\hat\Pi(\omega,\vec{k}),\hat\Pi(\omega,\vec{k}')\right]&=0=\left[\hat\Phi(\omega,\vec{k}),\hat\Phi(\omega,\vec{k}')\right]
\end{align}$$
The evolution operators we found also generate time and frequency respectively
$$\begin{align}
\dfrac{\partial\hat\phi}{\partial t}&=\frac{i}{\hbar}\left[\hat{H},\hat\phi\right]
&&&
\dfrac{\partial\hat\Pi}{\partial\omega}&=\frac{i}{\hbar}\left[\hat{T},\hat\Pi\right]
\end{align}$$
## Canonical Coordinates
We can define canonical coordinate operators for $\psi(x)$ and $\Gamma(k)$. Define
$$\begin{align}
\hat{X}^\mu\psi(x)&=x^\mu\psi(x) &&& \hat{K}^\mu\Gamma(k)&=k^\mu\Gamma(k)
\end{align}$$
The translation generators are then written as the differentials
$$\begin{align}
\hat{P}_\mu&=-i\hbar\dfrac{\partial}{\partial x^\mu} &&&
\hat{\chi}^\mu&=+i\hbar\dfrac{\partial}{\partial k_\mu}
\end{align}$$
which satisfy the commutators
$$\begin{align}
[\hat{X}^\mu,\hat{P}_\nu]&=i\hbar\delta^\mu_\nu &&&
[\hat{\chi}^\mu,\hat{K}_\nu]&=i\hbar\delta^\mu_\nu
\end{align}$$
and create the evolution operators
$$\begin{align}
U(a)&=e^{-ia^\mu\hat{P}_\mu/\hbar} &&&
U(b)&=e^{+ib_\mu\hat{\chi}^\mu/\hbar}
\end{align}$$
## Noether Current & Charge
We also have the ability to find the Noether currents and charges, resulting in
$$\begin{align}
\mathrm{T}^\mu_\nu&=\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}\partial_\nu\phi-\delta_\nu^\mu\mathcal{L}
&\implies&&
\mathrm{T}^\mu_\nu&=\partial^\mu\phi\ \partial_\nu\phi-\delta_\nu^\mu\mathcal{L}\\
\mathcal{T}^\mu_\nu&=\dfrac{\partial\mathscr{L}}{\partial(\partial_{k_\mu}\Pi)}\partial_{k_\nu}\Pi-\delta_\nu^\mu\mathscr{L}
&\implies&&
\mathcal{T}^\mu_\nu&=\partial_{k^\mu}\Pi\ \partial_{k_\nu}\Pi-\delta_\nu^\mu\mathscr{L}
\end{align}$$
These also have conservation laws and conserved charges on the hypersurface
$$\begin{align}
\partial_\mu\mathrm{T}^\mu_\nu&=0
&\implies&&
\mathrm{P}_\nu=\int d^3x \ T^0_\nu\\
\partial_{k_\mu}\mathcal{T}^\mu_\nu&=0
&\implies&&
\mathrm{X}^\mu=\int d^3x \ \mathcal{T}_0^\mu
\end{align}$$

## Time and Frequency Evolution
In ordinary quantum mechanics, the Hamiltonian $H$ is the generator of time evolution
$$\begin{align}
\ket{\psi(t)}&=e^{-i\hat{H}(t-t_0)/\hbar}\ket{\psi(t_0)}
&\iff&&
i\hbar\dfrac{\partial}{\partial t}\ket{\psi(t)}&=\hat{H}\ket{\psi(t)}
\end{align}$$
In spacetime frequency coordinates, we postulate the corresponding equation
$$\begin{align}
\ket{\Psi(\omega)}&=e^{-i\hat{T}(\omega-\omega_0)/\hbar}\ket{\Psi(\omega_0)}
&\iff&&
i\hbar\dfrac{\partial}{\partial\omega}\ket{\Psi(\omega)}&=\hat{T}\ket{\Psi(\omega)}
\end{align}$$
## The Heisenberg Equation
In ordinary quantum mechanics, an observable $\hat{\mathcal{O}}$ evolves according to
$$\begin{align}
\dfrac{d\hat{\mathcal{O}}_H}{dt}&=\frac{i}{\hbar}\left[\hat{H}_H,\hat{\mathcal{O}}_H\right]+\left(\dfrac{\partial\hat{\mathcal{O}}}{\partial t}\right)_H
\end{align}$$
The corresponding observable evolution equation would then be
$$\begin{align}
\dfrac{d\hat{\mathcal{O}}_H}{d\omega}&=\frac{i}{\hbar}\left[\hat{T}_H,\hat{\mathcal{O}}_H\right]+\left(\dfrac{\partial\hat{\mathcal{O}}}{\partial\omega}\right)_H
\end{align}$$
For observables with no explicit dependence on $t$ or $\omega$, we have
$$\begin{align}
\dfrac{d}{dt}\left\langle\hat{\mathcal{O}}\right\rangle&=\frac{i}{\hbar}\left\langle \left[\hat{H},\hat{\mathcal{O}}\right]\right\rangle
&&&
\dfrac{d}{d\omega}\left\langle\hat{\mathcal{O}}\right\rangle&=\frac{i}{\hbar}\left\langle \left[\hat{T},\hat{\mathcal{O}}\right]\right\rangle
\end{align}$$
If the Hamiltonian has no explicit time dependence, then energy is conserved. Likewise, if we substitute our operator $\hat{T}_H$ into our EOM, we get
$$\begin{align}
\dfrac{d\hat{T}_H}{d\omega}&=\frac{i}{\hbar}\left[\hat{T}_H,\hat{T}_H\right]=0
&\implies&&
\dfrac{d}{d\omega}\left\langle\hat{T}\right\rangle&=0
\end{align}$$
