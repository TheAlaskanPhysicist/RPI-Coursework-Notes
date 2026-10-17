



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


















## Operator Duality
Start with a field $\phi(x)$ and $\phi(k)$ who represent the same field, then
$$\begin{align}
S_x[\phi]&=\int d^4x\ \mathcal{L}_x\left(\phi,\dfrac{\partial\phi}{\partial x^\mu}\right) &&&
S_k[\phi]&=\int d^4k\ \mathcal{L}_k\left(\phi,\dfrac{\partial\phi}{\partial k_\mu}\right)
\end{align}$$
Under an infinitesimal translation $x^\mu\to x^\mu+a^\mu$ or $k_\mu\to k_\mu+b_\mu$, the field changes by
$$\begin{align}
\delta\phi&=-a^\nu\dfrac{\partial\phi}{\partial x^\nu} &&&
\delta\phi&=-b_\nu\dfrac{\partial\phi}{\partial p_\nu}
\end{align}$$
Noethers Theorem then gives us
$$\begin{align}
T^\mu_\nu(x)&=\dfrac{\partial\mathcal{L}_x}{\partial\left(\tfrac{\partial\phi}{\partial x^\mu}\right)}\dfrac{\partial\phi}{\partial x^\nu}-\delta^\mu_\nu\mathcal{L}_x &&&
\mathcal{T}_\nu^\mu(k)&=\dfrac{\partial\mathcal{L}_k}{\partial\left(\tfrac{\partial\phi}{\partial k_\mu}\right)}\dfrac{\partial\phi}{\partial k_\nu}-\delta^\mu_\nu\mathcal{L}_k
\end{align}$$
We also have a conservation law
$$\begin{align}
\dfrac{\partial}{\partial x^\mu}T^\mu_\nu(x)&=0 &&&
\dfrac{\partial}{\partial k_\mu}\mathcal{T}^\mu_\nu(p)&=0
\end{align}$$
We can get the conserved conjugate variable as
$$\begin{align}
P_\nu&=\int d^3x\ T^0_\nu &&&
X^\nu&=\int d^3k\ T^{0\nu}
\end{align}$$




## Action Symmetry in Spacetime Frequency Coordinates
To go more in-depth, I will follow similar derivations as textbooks often do for Spacetime Position coordinates, but instead using the frequency coordinates. Define action as
$$\begin{align}
S_k[\Psi]&=\int d^4k\ \mathcal{L}_k(\Psi,\partial_{k_\mu}\Psi)
\end{align}$$
Varying the field gives us the Euler-Lagrange equation
$$\begin{align}
\dfrac{\partial\mathcal{L}_k}{\partial\Psi}-\dfrac{\partial}{\partial k_\mu}\left(\dfrac{\partial\mathcal{L}_k}{\partial(\partial_{k_\mu}\Psi)}\right)&=0
\end{align}$$
Suppose we want to change the frequency configuration $k_\mu\to k_\mu-b_\mu$, then
$$\begin{align}
\delta\Psi(k)&=b_\nu\dfrac{\partial\Psi}{\partial k_\nu}
\end{align}$$
If the action is invariant under this transformation, Noether's theorem gives
$$\begin{align}
\mathcal{T}^\mu_\nu&=\dfrac{\partial\mathcal{L}_k}{\partial(\partial_{k_\mu}\Psi)}\dfrac{\partial\Psi}{\partial k_\nu}-\delta^\mu_\nu\mathcal{L}_k &&&
\dfrac{\partial}{\partial k_\mu}\mathcal{T}^\mu_\nu&=0
\end{align}$$
### Klein-Gordon Example

























## Quantum Mechanics Operators
Start with the canonical commutator relationship
$$\begin{align}
[\hat{x},\hat{k}]&=i
\end{align}$$
The operators in each representation are
$$\begin{align}
\hat{k}&=-i\dfrac{\partial}{\partial x} & \hat{x}&=+i\dfrac{\partial}{\partial k}
\end{align}$$
And that the Fourier coefficient is
$$\begin{align}
\left<x\middle|p\right>&=\dfrac{1}{\sqrt{2\pi\hbar}}e^{ikx}
\end{align}$$
We also have the translation operations
$$\begin{align}
U_x(a)\ket{x_0}=e^{-ia\hat{k}}\ket{x_0}&=\ket{x_0+a} & 
U_k(b)\ket{k_0}=e^{+ib\hat{x}}\ket{k_0}&=\ket{k_0+b}
\end{align}$$
These operators act on the observable operators as
$$\begin{align}
U^\dagger_x(a)\hat{x}U_x(a)&=\hat{x}+a &
U^\dagger_k(b)\hat{k}U_k(b)&=\hat{k}+b
\end{align}$$
## Bivariate Translation Operators
Suppose we wanted to translate a state in position and momentum simultaneously
$$\begin{align}
U(a,b)&=e^{i(b\hat{x}-a\hat{k})} &\implies&&
U^\dagger(a,b)\ \hat{{x}}\ U(a,b)=\hat{x}+a, &&
U^\dagger(a,b)\ \hat{{k}}\ U(a,b)=\hat{k}+b
\end{align}$$
We'll need to be careful about commutators. We can do the operation in 2 ways
$$\begin{align}
U_x(a)U_k(b)&=e^{-ia\hat{k}+ib\hat{x}-\tfrac{1}{2}iab}=e^{-\tfrac{1}{2}iab}U(a,b)\\
U_k(b)U_x(a)&=e^{ib\hat{x}-ia\hat{k}+\tfrac{1}{2}iab}=e^{+\tfrac{1}{2}iab}U(a,b)
\end{align}$$
Suppose we have coordinate-dependent displacements $dx(k)$ and $dk(x)$. For a path in phase space $\Gamma\to(x(\Gamma),k(\Gamma))$, we have the infinitesimal displacement operator as
$$\begin{align}
U(dx,dk)&=e^{i(\hat{x}\ dk-\hat{k}\ dx)}
\end{align}$$
For a continuum displacement of these transformations, we have that
$$\begin{align}
U[\gamma]&=\mathcal{P}\exp\left[\frac{i}{\hbar}\int_\gamma(\hat{x}\ dk-\hat{k}\ dx)\right]
\end{align}$$
For spacetime, we can represent it with 4-vectors as
$$\begin{align}
U(dx,dk)&=e^{i(\hat{X}^\mu\ dk_\mu-\hat{K}_\mu\ dx^\mu)}
\end{align}$$









For spacetime position coordinates, we have the operators
$$\begin{align}
\hat{\omega}&=+i\dfrac{\partial}{\partial t} &&&
\hat{k}_j&=-i\dfrac{\partial}{\partial x_j}
\end{align}$$
Alternatively, in the spacetime frequency coordinates, we have the operators
$$\begin{align}
\hat{t}&=-i\dfrac{\partial}{\partial\omega} &&&
\hat{x}_j&=+i\dfrac{\partial}{\partial k_j}
\end{align}$$
There also exists 4 translation operators
$$\begin{align}
e^{-i\hat{\omega}t}\ket{0}&=\ket{t} & e^{+i\hat{k}x}\ket{0}&=\ket{x} \\
e^{+i\hat{t}\omega}\ket{0}&=\ket{\omega} & e^{-i\hat{x}k}\ket{0}&=\ket{k}
\end{align}$$
For translations in one of the coordinates, the operators commute since one of them remains a constant. But suppose we had an operator that actually didn't commute.

Suppose we have a spatial translation first, then a momentum translation
$$\begin{align}
e^{+i\hat{k}(x_0)dx(k)}\ket{x_0}&=\ket{x_0+dx(k)}\\
e^{-i\hat{x}(k)dk(x_0+dx(k))}e^{+i\hat{k}(x_0)dx(k)}\ket{x_0}
&=e^{-i\hat{x}(k)dk(x_0+dx(k))}\ket{x_0+dx(k)}\\
&=e^{-i\hat{x}(k)dk(x_0+dx(k))}\int d^4 k'e^{-ik'\cdot(x_0+dx(k))}\ket{k'}\\
&=\int d^4 k'e^{-ik'\cdot(x_0+dx(k))}\ket{k'+dk(x_0+dx(k))}\\
&=\int d^4 k'e^{-i(k'-dk(x))\cdot x}\ket{k'}\\
&=e^{ix\cdot dk(x)}\int d^4 k'e^{-ik'\cdot x}\ket{k'}\\
U(dk,dx)\ket{x_0}&=e^{i(x_0+dx(k_0))\cdot dk(x_0+dx(k_0))}\ket{x_0+dx(k_0)}
\end{align}$$
For the opposite, we have
$$\begin{align}
e^{+i\hat{x}(k_0)dk(x_0)}\ket{x_0}
&=\int d^4k \ e^{-ik\cdot x_0}e^{+i\hat{x}(k_0)dk(x_0)}\ket{k}\\
&=e^{ix_0\cdot dk(x_0)}\int d^4k \ e^{-ik\cdot x_0}\ket{k}\\
&=e^{ix_0\cdot dk(x_0)}\ket{x_0}\\
U(dx,dk)\ket{x_0}&=e^{ix_0\cdot dk(x_0)}\ket{x_0+dx(k+dk(x_0))}
\end{align}$$






$$\begin{align}
U(dk,dx)\ket{x_0}&=e^{i(x_0+dx(k_0))\cdot dk(x_0+dx(k_0))}\ket{x_0+dx(k_0)}\\
-U(dx,dk)\ket{x_0}&=-e^{ix_0\cdot dk(x_0)}\ket{x_0+dx(k+dk(x_0))}\\
U(dk,dx)\ket{x_0}\ket{x_0}-U(dx,dk)\ket{x_0}&=
\end{align}$$


$$\begin{align}
e^{ix_0\cdot dk(x_0)}\left(e^{i[x_0+dx(k_0)]dx(k_0)dk'(x_0)+idx(k_0)\cdot dk(x_0)}\ket{x_0+dx(k_0)}-\ket{x_0+dx(k_0)+dx'(k_0)dk(x_0)}\right)\\
\approx 2ie^{-idx(k_0)\cdot dk(x_0)/2}e^{ix_0\cdot dk(x_0)}\left(\frac{e^{idx(k_0)\cdot dk(x_0)/2}-e^{-idx(k_0)\cdot dk(x_0)/2}}{2i}\right)\ket{x_0+dx(k_0)}\\
\approx 2ie^{i(x_0-dx(k_0)/2)dk(x_0)}\sin\left(dx(k_0)\cdot dk(x_0)/2)\right)\ket{x_0+dx(k_0)}\\
\end{align}$$









$$\begin{align}
e^{+i\hat{k}dx}e^{-i\hat{x}dk}\ket{0}_x
&=e^{+i\hat{k}dx}e^{-i\hat{x}dk}\int d^4k\ \left<k\middle|x_0\right>\ket{k}\\

\end{align}$$




$$\begin{align}
e^{+i\hat{k}dx}e^{-i\hat{x}dk}&=\exp\left(i\hat{k}dx-i\hat{x}dk-\dfrac{1}{2}\left[\hat{x},\hat{k}\right]dx\ dk+0+0+\dots\right)\\
e^{-i\hat{x}dk}e^{+i\hat{k}dx}&=\exp\left(i\hat{k}dx-i\hat{x}dk+\dfrac{1}{2}\left[\hat{x},\hat{k}\right]dx\ dk+0+0+\dots\right)\\
\end{align}$$












Suppose you have a general state vector $\ket{\Psi}$, then we can choose an observable $\hat{Q}$ with eigenvalues $q$ for each state, then projecting we get
$$\begin{align}
\ket{\Psi}&=\int d^4q\ \ket{q}\left<q\middle|\Psi\right>
\end{align}$$
Then suppose we have an operator $\hat{P}$ so that it is the generator of $q$, then
$$\begin{align}
\ket{\Psi}&=\int d^4q\ e^{-i\hat{P}q}\ket{0}\bra{0}e^{+i\hat{P}q}\ket{\Psi}
\end{align}$$
But for the inverse transformation we found earlier, then 






This can also be shown for all the others. The general expression is that
$$\begin{align}
\ket{0}&=e^{+i\hat{\omega}\hat{t}}\ket{t}
\end{align}$$























## Background
In most typical systems, we start with a state $\ket\Psi$ represented in spacetime coordinates
$$\begin{align}
\ket{\Psi}&=\int d^4x\ket{x}\left<x\middle|\Psi\right>.
\end{align}$$
For these position eigenstates, we have the Lie Theory translation operator
$$\begin{align}
e^{a\tfrac{d}{dx}}f(x)&=f(x+a) &\implies&& e^{\Delta x\frac{d}{dx}}\ket{x}&=\ket{x+\Delta x}
\end{align}$$
In Quantum Mechanics, we represent these operators as
$$\begin{align}
e^{\Delta t\left(-\tfrac{i}{\hbar}\hat{H}\right)}&=e^{\Delta t\tfrac{d}{dt}} 
&\implies&&
\hat{H}&=+i\hbar\dfrac{d}{dt}\\
e^{\Delta x\left(\tfrac{i}{\hbar}\hat{P}\right)}&=e^{\Delta x\tfrac{d}{dx}} 
&\implies&&
\hat{P}&=-i\hbar\dfrac{d}{dx}
\end{align}$$
The original translation operator is spanned by anti-Hermitian basis elements, but the inclusion of the imaginary number $i$ makes the physical operators Hermitian. Suppose we set the spacetime origin, then to translate from this origin to any other point takes the form
$$\begin{align}
\ket{x}&=\lim_{dt\to0}\prod_{n=0}^{\tfrac{x^0}{dt}-1}\exp\left(-\dfrac{i}{\hbar}\hat{H}(n\cdot dt) dt+\dfrac{i}{\hbar}\hat{P}(n\cdot dt) \frac{dx}{dt}(n\cdot dt)\cdot dt\right)\ket{0}\\
&=\lim_{dt\to0}\prod_{n=0}^{\tfrac{x^0}{dt}-1}\exp\left(-\dfrac{i}{\hbar}\left(\hat{H}(n\cdot dt)-\hat{P}(n\cdot dt)\dot{x}(n\cdot dt)\right)dt\right)\ket{0}
\end{align}$$
In order to simplify these systems without endless commutators, we impose
$$\begin{align}
\left[\hat{H}(t),\hat{H}(t')\right]&=0 &
\left[\hat{H}(t),\hat{P}(t')\right]&=0 &
\left[\hat{P}(t),\hat{P}(t')\right]&=0 &
\end{align}$$
Thus we can bring the product into the exponential as a sum
$$\begin{align}
\ket{x}
&=\lim_{dt\to0}\exp\left(-\dfrac{i}{\hbar}\sum_{n=0}^{\tfrac{x^0}{dt}-1}\left(\hat{H}(n\cdot dt)-\hat{P}(n\cdot dt)\dot{x}(n\cdot dt)\right)dt\right)\ket{0}\\
&=\exp\left(-\dfrac{i}{\hbar}\int_0^{x^0}\left(\hat{H}(t)-\hat{P}(t)\dot{x}(t)\right)dt\right)\ket{0}\\
&=\exp\left(+\dfrac{i}{\hbar}\int_0^{x^0}L(t)\ dt\right)\ket{0}\\
\Aboxed{\ket{x}&=\exp\left(+\dfrac{i}{\hbar}S(x^0)\right)\ket{0}}
\end{align}$$


## Conjugate Formalism
Instead, we start with $\ket\Psi$ represented in spacetime frequency coordinates
$$\begin{align}
\ket{\Psi}&=\int\dfrac{d^4p}{(2\pi)^4}\ket{p}\left<p\middle|\Psi\right>.
\end{align}$$
For these momentum eigenstates, we have the Lie Theory translation operator
$$\begin{align}
e^{a\tfrac{d}{dp}}f(p)&=f(p+a) &\implies&& e^{\Delta p\frac{d}{dp}}\ket{p}&=\ket{p+\Delta p}
\end{align}$$
In Quantum Mechanics, we represent these operators as
$$\begin{align}
e^{\Delta E\left(-\tfrac{i}{\hbar}\hat{T}\right)}&=e^{\Delta E\tfrac{d}{dE}} 
&\implies&&
\hat{T}&=+i\hbar\dfrac{d}{dE}\\
e^{\Delta p\left(\tfrac{i}{\hbar}\hat{X}\right)}&=e^{\Delta p\tfrac{d}{dp}} 
&\implies&&
\hat{X}&=-i\hbar\dfrac{d}{dp}
\end{align}$$
Suppose we set the spacetime frequency origin (no momentum or energy), then to translate from this origin to any other point takes the form
$$\begin{align}
\ket{p}&=\lim_{dE\to0}\prod_{n=0}^{\tfrac{p^0}{dE}-1}\exp\left(-\dfrac{i}{\hbar}\hat{T}(n\cdot dE) dE+\dfrac{i}{\hbar}\hat{X}(n\cdot dE) \frac{dp}{dE}(n\cdot dE)\cdot dE\right)\ket{0}\\
&=\lim_{dE\to0}\prod_{n=0}^{\tfrac{p^0}{dE}-1}\exp\left(-\dfrac{i}{\hbar}\left(\hat{T}(n\cdot dE)-\hat{X}(n\cdot dE)\dot{p}(n\cdot dt)\right)dE\right)\ket{0}
\end{align}$$
In order to simplify these systems without endless commutators, we impose
$$\begin{align}
\left[\hat{X}(E),\hat{X}(E)\right]&=0 &
\left[\hat{X}(E),\hat{T}(E)\right]&=0 &
\left[\hat{T}(E),\hat{T}(E)\right]&=0 &
\end{align}$$
Thus we can bring the product into the exponential as a sum
$$\begin{align}
\ket{p}
&=\lim_{dE\to0}\exp\left(-\dfrac{i}{\hbar}\sum_{n=0}^{\tfrac{p^0}{dE}-1}\left(\hat{T}(n\cdot dE)-\hat{X}(n\cdot dE)\dot{p}(n\cdot dE)\right)dE\right)\ket{0}\\
&=\exp\left(-\dfrac{i}{\hbar}\int_0^{p^0}\left(\hat{T}(E)-\hat{X}(E)\dot{p}(E)\right)dE\right)\ket{0}\\
&=\exp\left(+\dfrac{i}{\hbar}\int_0^{p^0}\Gamma(E)\ dE\right)\ket{0}\\
\Aboxed{\ket{p}&=\exp\left(+\dfrac{i}{\hbar}\mathcal{S}(p^0)\right)\ket{0}}
\end{align}$$



## Generalize Translation (first attempt)
From typical quantum mechanics, we write the translation in spacetime as a displacement in that spacetime times the associated generator of that motion. In the alternative formalism, we instead write the translation in spacetime frequency as a displacement in that frequency times the associated generator of *that* motion. In reality, we shouldn't be limited to translation in just one or the other, as these are conjugates of each other.

For time/temporal frequency translation, we have the operators
$$\begin{align}
\ket{t+dt}&=e^{-i\hat{\Omega}(t)dt}\ket{t} & \ket{\omega+d\omega}&=e^{-i\hat{T}(\omega)d\omega}\ket{\omega}
\end{align}$$
The infinitesimal translations, in some way, reduce a problem into moving a statevector in one "axis" so to speak, and so a more generalized operation would be needed since they are functions of one another. Suppose we translate time, then temporal frequency, then
$$\begin{align}
e^{-i\hat{T}(\omega)d\omega}e^{-i\hat{\Omega}(t)dt}\ket{t}
&=e^{-i\hat{T}(\omega)d\omega}\ket{t+dt}\\
&=e^{-i\hat{T}(\omega)d\omega}\int\dfrac{d\omega}{2\pi}\ket{\omega}\left<\omega\middle|t+dt\right>\\
&=e^{-i\hat{T}(\omega)d\omega}\int\dfrac{d\omega}{2\pi}\ket{\omega}e^{-i\omega(t+dt)}\\
&=\int\dfrac{d\omega}{2\pi}e^{-i\omega(t+dt)}\ket{\omega+d\omega}\\
e^{-i\hat{T}(\omega)d\omega}e^{-i\hat{\Omega}(t)dt}\ket{t}&=\int\dfrac{d\omega}{2\pi}e^{-i(\omega-d\omega)(t+dt)}\ket{\omega}
\end{align}$$
Reversing the orders of operations, we get
$$\begin{align}
e^{-i\hat{\Omega}(t)dt}e^{-i\hat{T}(\omega)d\omega}\ket{t}
&=e^{-i\hat{\Omega}(t)dt}e^{-i\hat{T}(\omega)d\omega}\int\dfrac{d\omega}{2\pi}\ket{\omega}e^{-i\omega t}\\
&=e^{-i\hat{\Omega}(t)dt}\int\dfrac{d\omega}{2\pi}\ket{\omega+d\omega}e^{-i\omega t}\\
&=e^{-i\hat{\Omega}(t)dt}\iint dt'\dfrac{d\omega}{2\pi}e^{i(\omega+d\omega)t'}e^{-i\omega t}\ket{t'}\\
&=\iint dt'\dfrac{d\omega}{2\pi}e^{i(\omega+d\omega)t'}e^{-i\omega t}\ket{t'+dt}\\
&=\iint dt'\dfrac{d\omega}{2\pi}e^{i(\omega+d\omega)(t'-dt)}e^{-i\omega t}\ket{t'}\\
\end{align}$$


## Generalize Translation (Second attempt)
Between any two operators through the exponential, we need the relation
$$\begin{align}
e^Ae^B&=\exp\left(A+B+\dfrac{1}{2}\left[A,B\right]+\frac{1}{12}[A,[A,B]]+\frac{1}{12}[B,[B,A]]+\dots\right)
\end{align}$$
Luckily, in Quantum Mechanics, the relationships between spacetime and spacetime frequency is a scalar with the commutator
$$\begin{align}
[X^\mu,P_\nu]&=-i\hbar g^\mu_\nu & [X^\mu,X^\nu]&=0 & [P_\mu,P_\nu]&=0
\end{align}$$
For the higher order commutators, we nicely have
$$\begin{align}
[X^{\mu_1},[X^{\mu_2},[\dots, [X^{\mu_{N-1}},[X^{\mu_N},P_\nu]]]]]&=[X,[X,[\dots, [X,[-i\hbar g^{\mu_N}_\nu]]]]]=0\\
[P^{\mu_1},[P^{\mu_2},[\dots, [P^{\mu_{N-1}},[P^{\mu_N},X_\nu]]]]]&=[P,[P,[\dots, [P,[+i\hbar g^{\mu_N}_\nu]]]]]=0\\
\end{align}$$
All higher order commutators will vanish, and so our relationships becomes
$$\begin{align}
e^Ae^B&=\exp\left(A+B+\dfrac{1}{2}\left[A,B\right]\right)
\end{align}$$
For an infinitesimal translation in $x\to x+dx$ and $p\to p+dp$, consider the two ways one could operate on a statevector. Note that $x,dx$ are functions of $p$ and $p,dp$ are functions of $x$. Then
$$\begin{align}
e^{i\hat{P}dx/\hbar}e^{i\hat{X}dp/\hbar}&=\exp\left(\dfrac{i}{\hbar}\left(\hat{P}dx+\hat{X}dp-\dfrac{i}{2\hbar}\left[\hat{X},\hat{P}\right]dx\ dp\right)\right)\\
e^{i\hat{X}dp/\hbar}e^{i\hat{P}dx/\hbar}&=\exp\left(\dfrac{i}{\hbar}\left(\hat{X}dp+\hat{P}dx+\dfrac{i}{2\hbar}\left[\hat{X},\hat{P}\right]dx\ dp\right)\right)
\end{align}$$
This is almost the translation operator we want, but there's this extra commutator term. Suppose we concatenate these translations, then there are 2 ways to operate. If you use the expression for the product of exponentials again, you'll find all the annoying terms cancel, thus
$$\begin{align}
U(dx,dp,dp,dx)&=\exp\left(\dfrac{i}{\hbar}\left(2\hat{P}dx+2\hat{X}dp\right)\right)\\
U(dp,dx,dx,dp)&=\exp\left(\dfrac{i}{\hbar}\left(2\hat{P}dx+2\hat{X}dp\right)\right)
\end{align}$$
These expressions are identical, as one would expect. All extra commutators between the two exponential terms cancel because of our relationship that $\left[X,P\right]\propto1$. Therefore, if we want a general simultaneous infinitesimal translation, we define the operator
$$\begin{align}
e^{\tfrac{i}{\hbar}\left(\hat{P}dx+\hat{X}dp\right)}&=e^{i\hat{P}dx/2\hbar}e^{i\hat{X}dp/2\hbar}e^{i\hat{X}dp/2\hbar}e^{i\hat{P}dx/2\hbar}=e^{i\hat{X}dp/2\hbar}e^{i\hat{P}dx/2\hbar}e^{i\hat{P}dx/2\hbar}e^{i\hat{X}dp/2\hbar}
\end{align}$$


## Generalize Translation (Third attempt)
For some statevector $\ket{\Psi}$, we can project it onto some coordinate basis
$$\begin{align}
\ket{\Psi}&=\dfrac{1}{(2\pi)^{4/2}}\int d^4q\ \ket{q}\left<q\middle|\Psi\right>,
\end{align}$$
where $q$ is an eigenstate of an observable $\hat{Q}$. There also exists a conjugate coordinate basis with eigenstates $p$ of an observable $\hat{P}$. The statevector can also be written then as
$$\begin{align}
\ket{\Psi}&=\dfrac{1}{(2\pi)^{4/2}}\int d^4p\ \ket{p}\left<p\middle|\Psi\right>.
\end{align}$$
Suppose that these observables $\hat{Q},\hat{P}$ are the generators of $p,q$ respectively, given
$$\begin{align}
U(a)\ket{q}=e^{-i\hat{P}a}&=\ket{q+a} &&& V(b)\ket{p}=e^{-i\hat{Q}b}&=\ket{p+b}
\end{align}$$





## Heisenberg Interaction Picture
For the typical interaction picture of Quantum Mechanics, you have
$$\begin{align}
\bra{x,t}\hat{\mathcal{O}}\ket{x,t}
&=\bra{x,0}e^{+iHt/\hbar}\cdot\hat{\mathcal{O}}\cdot e^{-iHt/\hbar}\ket{x,0}\\
&=\bra{x,0}\left(e^{+iHt/\hbar}\hat{\mathcal{O}}e^{-iHt/\hbar}\right)\ket{x,0}\\
\left\langle\mathcal{O}\right\rangle(x,t)&=\bra{x,0}\hat{\mathcal{O}}(t)\ket{x,0}
\end{align}$$
Now suppose that for the spacetime position representation, we have that
$$\begin{align}
\bra{x,t}\hat{\mathcal{O}}\ket{x,t}
&=\bra{0,0}e^{+i(\hat{H}t-\hat{p}x)/\hbar}\cdot\hat{\mathcal{O}}\cdot e^{-i(\hat{H}t-\hat{p}x)/\hbar}\ket{0,0}\\
&=\bra{0,0}\left(e^{+i(\hat{H}t-\hat{p}x)/\hbar}\hat{\mathcal{O}}e^{-i(\hat{H}t-\hat{p}x)/\hbar}\right)\ket{0,0}\\
\bra{x,t}\hat{\mathcal{O}}\ket{x,t}&=\bra{0,0}\mathcal{O}(x,t)\ket{0,0}
\end{align}$$
Instead of just in time, we now have an observable in spacetime
$$\begin{align}
\hat{\mathcal{O}}(x,t)&=e^{+i(\hat{H}t-\hat{p}x)/\hbar}\ \hat{\mathcal{O}}\ e^{-i(\hat{H}t-\hat{p}x)/\hbar}
\end{align}$$
What if instead we had a statevector in spacetime frequency representation, then
$$\begin{align}
\bra{p,E}\hat{\mathcal{O}}\ket{p,E}
&=\bra{0,0}e^{-i(\hat{T}E-\hat{x}p)/\hbar}\cdot\hat{\mathcal{O}}\cdot e^{+i(\hat{T}E-\hat{x}p)/\hbar}\ket{0,0}\\
&=\bra{0,0}\left(e^{-i(\hat{T}E-\hat{x}p)/\hbar}\hat{\mathcal{O}}e^{+i(\hat{t}E-\hat{x}p)/\hbar}\right)\ket{0,0}\\
\bra{p,E}\hat{\mathcal{O}}\ket{p,E}&=\bra{0,0}\mathcal{O}(p,E)\ket{0,0}
\end{align}$$
We'd instead have the observable in terms of energy-momentum
$$\begin{align}
\hat{\mathcal{O}}(p,E)&=e^{-i(\hat{T}E-\hat{x}p)/\hbar}\hat{\mathcal{O}}e^{+i(\hat{t}E-\hat{x}p)/\hbar}
\end{align}$$
In order to accommodate for this change, we'll need new definitions for these operators.

## New Conjugate Operators
In typical classical mechanics, we have the operators
$$\begin{align}
U(t,t_0)\ket{t_0}=e^{-i\hat{H}(t-t_0)/\hbar}\ket{t_0}&=\ket{t} & U(x,x_0)\ket{x_0}=e^{+i\hat{P}(x-x_0)/\hbar}\ket{x_0}&=\ket{x}
\end{align}$$
These operators relate to the derivatives of the coordinates as
$$\begin{align}
\hat{H}&=+i\hbar\dfrac{d}{dt} & \hat{P}_j&=-i\hbar\dfrac{d}{dx_j}
\end{align}$$
Suppose now we have two new operators $\hat{T}$ and $\hat{X}$ who act similarly to the above but for spacetime frequency coordinates instead of position
$$\begin{align}
U(E,E_0)\ket{E_0}=e^{+i\hat{T}(E-E_0)/\hbar}\ket{E_0}&=\ket{E} & U(p,p_0)\ket{p_0}=e^{-i\hat{X}(p-p_0)/\hbar}\ket{p_0}&=\ket{p}
\end{align}$$
These operators relate to the derivatives of the coordinates as
$$\begin{align}
\hat{T}&=-i\hbar\dfrac{d}{dE} & \hat{X}_j&=+i\hbar\dfrac{d}{dp_j}
\end{align}$$

### Coordinate-Dependent Operators
From a previous section, we can write each operator in terms of the alternate formulation
$$\begin{align}
\hat{T}(p,E)&=e^{+i\hat{X}p/\hbar}\ \hat{T}\ e^{-i\hat{X}p/\hbar}\\
\hat{X}(p,E)&=e^{-i\hat{T}E/\hbar}\ \hat{X}\ e^{+i\hat{T}E/\hbar}\\
\hat{\mathcal{H}}(x,t)&=e^{-i\hat{P}x/\hbar}\ \hat{H}\ e^{+i\hat{P}x/\hbar}\\
\hat{\mathcal{P}}(x,t)&=e^{+i\hat{H}t/\hbar}\ \hat{P}\ e^{-i\hat{H}t/\hbar}\\
\end{align}$$
Suppose I have a general statevector $\ket{\Psi}$ and I want to apply the time-displacement operator, then
$$\begin{align}
\ket{t}&=\lim_{dt\to0}\prod_{n=0}^{t/dt-1}\exp\left(-\frac{i}{\hbar}\hat{H}(x(n\cdot dt),n\cdot dt)dt\right)\ket{0}
\end{align}$$






Suppose I have a general statevector $\ket{\Psi}$ and I want to apply the time-displacement operator, then
$$\begin{align}
\ket{t}&=\lim_{dt\to0}\prod_{n=0}^{t/dt-1}\exp\left(-\frac{i}{\hbar}\hat{H}(n\cdot dt)dt\right)\ket{0}
\end{align}$$
If we calculate the product of the exponential of two Hamiltonians separated by $dt$, we get that
$$\begin{align}
H(t+dt)dt+H(t)dt+\dfrac{1}{2}dt^2\left[H(t+dt),H(t)\right]+\mathcal{O}(dt^3)
\end{align}$$
In the limit as $dt\to0$, we expect that the contribution from the commutators to be exceedingly small relative to the Hamiltonians themselves. Thus we can bring the product into the exponent as a summation to find
$$\begin{align}
\ket{t}&=\exp\left(-\frac{i}{\hbar}\int_{t_0}^t\hat{H}(t')\ dt'\right)\ket{t_0}
\end{align}$$
If we instead rewrite the Hamiltonian as a Hamiltonian density in $x$, we have that















## Dual-Interaction Picture
For the typical interaction picture of Quantum Mechanics, you have
$$\begin{align}
\ket{\psi_I(t)}&=e^{iH_0t/\hbar}\ket{\psi_S(t)}\\
A_I(t)&=e^{iH_0t/\hbar}A_S(t)e^{-iH_0t/\hbar}\\
\end{align}$$





$$\begin{align}
\bra{\Psi}\hat{\mathcal{O}}\ket{\Psi}
&=\bra{x,0}e^{+iHt/\hbar}\cdot\hat{\mathcal{O}}\cdot e^{-iHt/\hbar}\ket{x,0}\\
&=\bra{x,0}\left(e^{+iHt/\hbar}\hat{\mathcal{O}}e^{-iHt/\hbar}\right)\ket{x,0}\\
&=\bra{x,0}\hat{\mathcal{O}}(t)\ket{x,0}\\
\end{align}$$








Suppose you want to find the expected value of an operator $\mathcal{O}$, then you would want to find
$$\begin{align}
\left\langle\mathcal{O}\right\rangle&=\bra{\Psi}\hat{\mathcal{O}}\ket{\Psi}
\end{align}$$
In spacetime position representation, if we choose an origin to be our zero point, then the state can be represented as a translation from that zero point as
$$\begin{align}
\left\langle\mathcal{O}\right\rangle&=\iint d^4x\ d^4x'\left<\Psi\middle|x'\right>\left<x\middle|\Psi\right>\bra{x'}\hat{\mathcal{O}}\ket{x}
\end{align}$$
There exists a basis where $\hat{\mathcal{O}}$ is diagonal, so we can expand in this basis
$$\begin{align}
\left\langle\mathcal{O}\right\rangle&=\iint\iint d^4x\ d^4x'\ d^4y\ d^4y'\left<\Psi\middle|x'\right>\left<x\middle|\Psi\right>\left<x'\middle|y'\right>\bra{y'}\hat{\mathcal{O}}\ket{y}\left<y\middle|x\right>\\
&=\iint\int d^4x\ d^4x'\ d^4y\ \Psi^*(x')\Psi(x)\left<x'\middle|y\right>\left<y\middle|x\right>\bra{y}\hat{\mathcal{O}}\ket{y}\\
\end{align}$$












&=\dfrac{1}{(2\pi)^{4/2}}\int d^4q\ e^{i\hat{P}\hat{Q}}\ket{q}\left<q\middle|\Psi\right>\\

















$$\begin{align}
\ket{x}&=e^{-i\left(\hat{H}(x^0-\mathcal{O}^0)+\vec{P}\cdot(\vec{x}-\vec{\mathcal{O}})\right)/\hbar}\ket{\mathcal{O}}
\end{align}$$
If we instead define a spacetime operator for energy-momentum as
$$\begin{align}
K_\mu&=\dfrac{1}{\hbar}P_\mu &\implies&& 
K_0&=\dfrac{1}{\hbar}\hat{H},&K_i&=\dfrac{1}{\hbar}\hat{P}_i,
\end{align}$$
Then the spacetime translation operator then has the form
$$\begin{align}
\ket{x}&=e^{-i\hat{P}_\mu(x-\mathcal{O})^\mu}\ket{\mathcal{O}} &&&
\bra{x}&=\bra{\mathcal{O}}e^{+i\hat{P}_\mu(x-\mathcal{O})^\mu}
\end{align}$$










Traditionally, we start with a statevector in terms of spacetime coordinates.
$$\begin{align}
G(x,x')&=\left<\Psi(x)\middle|\Psi(x')\right>
\end{align}$$

To generate the transition between spacetime $x_0$ to $x$, we have the generators
$$\begin{align}
\ket{\Psi(x)}&=e^{-i\hat{P}_\mu(x-x')^\mu}\ket{\Psi(x')}
\end{align}$$
Substituting back into our 2-point function, we have
$$\begin{align}
G(x,x')&=\bra{\Psi(x')}e^{+i\hat{P}_\mu(x-x')^\mu}\ket{\Psi(x')}
\end{align}$$
Suppose now we represent our statevector in terms of the conjugate variable
$$\begin{align}
\ket{\Psi(x)}&=\int\dfrac{d^4p}{(2\pi)^4}e^{-ip_\mu x^\mu}\ket{\Psi(p)}\\
\bra{\Psi(x')}&=\int\dfrac{d^4p'}{(2\pi)^4}e^{+ip_\mu' x'^\mu}\bra{\Psi(p')}\\
\end{align}$$
Substituting into the Green's function, we get
$$\begin{align}
G(x,x')&=\iint\dfrac{d^4p}{(2\pi)^4}\dfrac{d^4p'}{(2\pi)^4}e^{-ip_\mu x^\mu}e^{+ip_\mu' x'^\mu}\bra{\Psi(p')}e^{+i\hat{P}_\mu(x-x')^\mu}\ket{\Psi(p)}\\
&=\iint\dfrac{d^4p}{(2\pi)^4}\dfrac{d^4p'}{(2\pi)^4}e^{-i(p_\mu x^\mu-p_\mu' x'^\mu)}e^{+iP_\mu(x-x')^\mu}\delta(p-p')\\
&=\int\dfrac{d^4p}{(2\pi)^4}e^{-i(p_\mu-P_\mu)(x^\mu-x'^\mu)}\\
&=\int\dfrac{d^4p}{(2\pi)^4}e^{-ip_\mu(x^\mu-x'^\mu)}\\
G(x,x')&=\delta^{(4)}(x-x')
\end{align}$$











For the sake of using this later, we'll instead use operators
$$\begin{align}
\hat{\Omega}&=-\frac{i}{\hbar}\hat{H} &
\hat{K}_j&=+\frac{i}{\hbar}\hat{P}_j
&\implies&&
\hat{K}_\mu&=-\frac{i}{\hbar}\hat{P}_\mu
\end{align}$$

Substituting back into our 2-point function, we have
$$\begin{align}
G(x,x')&=\bra{\Psi(x')}e^{\hat{K}_\mu^*(x-x')^\mu}\ket{\Psi(x')}
\end{align}$$
Suppose now we represent our statevector in terms of the conjugate variable
$$\begin{align}
\ket{\Psi(x)}&=(i\hbar)^4\int\dfrac{d^4k}{(2\pi)^4}e^{k_\mu x^\mu}\ket{\Psi(k)}
& k_\mu&=-\frac{i}{\hbar}p_\mu
\end{align}$$






Substituting, this expression in, we get
$$\begin{align}
G(x,x')&=\bra{\Psi(x')}e^{\hat{K}_\mu^*(x-x')^\mu}\ket{\Psi(x')}\\
&=\hbar^8\int\dfrac{d^4k}{(2\pi)^4}\dfrac{d^4k'}{(2\pi)^4}e^{k_\mu'^* x'^\mu}e^{k_\mu x^\mu}\left<\Psi(k')\middle|e^{\hat{K}_\mu^*(x-x')^\mu}\middle|\Psi(k)\right>\\
&=\hbar^8\iint\dfrac{d^4k}{(2\pi)^4}\dfrac{d^4k'}{(2\pi)^4}e^{k_\mu'^* x'^\mu}e^{k_\mu x^\mu}e^{k_\mu^*(x-x')^\mu}\left<\Psi(k')\middle|\Psi(k)\right>\\
&=\hbar^8\int\dfrac{d^4k}{(2\pi)^4}e^{-k_\mu0^\mu}\\
&=\hbar^8\int\dfrac{d^4k}{(2\pi)^4}e^{-k_\mu0^\mu}\\
\end{align}$$






