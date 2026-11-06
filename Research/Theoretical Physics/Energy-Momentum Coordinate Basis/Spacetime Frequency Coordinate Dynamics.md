# Guiding Idea
The idea is that if in normal systems, we tend to want to look at systems at equal times, and in some way we integrate over all position space. We also have the idea of a spacetime interval being constant for spacetime position coordinates. What I was thinking is that systems at equal energies (constant E) and we integrate over all frequency space. The spacetime interval equivalent then becomes mass. I find this idea interesting because it means in a way that if you represent a system in spacetime position coordinates you get Lorentz-Invariant spacetime intervals, while representing that system in spacetime frequency coordinates gets you Lorentz-Invariant mass.
$$\begin{align}
(ct)^2-\vec{x}^2&=s^2 &\iff&& (E/c)^2-p^2&=(mc)^2\\
t^2-(\vec{x}/c)^2&=t_\mathcal{O}^2 &\iff&& (E)^2-(pc)^2&=E_\mathcal{O}^2
\end{align}$$


# Spacetime Frequency Theory
In typical QFT, we parametrize operators in spacetime position coordinates $x^\mu=(t,\vec{x})$; the consequences of this choice have been well-studied in literature with respect to the mathematics of these systems, as well as their physical implications. The aim of this section is to explore an alternative parametrization for QFT in terms of spacetime frequency coordinates $k_\mu=(\omega,\vec{k})$ to determine parallels in their dynamics and develop solution methods for certain kinds of systems.

For the sake of simplicity, we will be using natural units $(\hbar=c=k_B=1)$. One of the first things to note is that for a spacetime theory these solutions and methods must remain Lorentz invariant. For example, in position space, we have the spacetime interval
$$\begin{align}
ds^2=g_{\mu\nu}(x)dx^\mu dx^\nu &\implies&&
ds=\int_\Gamma\sqrt{g_{\mu\nu}(x)dx^\mu dx^\nu}=\int_\Gamma\sqrt{g_{\mu\nu}(x(\tau))\frac{dx^\mu}{d\tau} \frac{dx^\nu}{d\tau}}d\tau
\end{align}$$
Similarly, for frequency space, we have an analogous conserved quantity
$$\begin{align}
d\mu^2&=g^{\mu\nu}dk_\mu dk_\nu &\implies&&
d\mu=\int_{\Gamma'}\sqrt{g^{\mu\nu}(k)dk_\mu dk_\nu}=\int_{\Gamma'}\sqrt{g^{\mu\nu}(k(\Omega))\frac{dk_\mu}{d\Omega}\frac{dk_\nu}{d\Omega}}d\Omega
\end{align}$$
The spacetime interval effectively calculates the arc-length between 2 points in spacetime position coordinates, using $\tau$ as the proper time to parametrize the coordinates along $\Gamma$. This alternative spacetime frequency interval calculates the arc-length between 2 points in spacetime frequency coordinates, using $\Omega$ as the "proper frequency" to parametrize the coordinates along $\Gamma'$. The quantity that this calculates is related to the rest mass of an object, where even under a Lorentz transform, the arc-length from $(\omega,k)\to(\omega',k')$ preserves a constant. The proper time is generally understood as to be the time that an observer would measure when standing exactly where they are, when the position and its derivatives are zero since they are unmoving in their own reference frame. Similarly, the rest frequency would be analogous to a frame where they do not perceive any spatial frequency, and that there is only temporal frequency.


## Quantum Field Theory (Spacetime Position)
Suppose there exists a real scalar field $\hat\phi(x)$ who is parametrized by *spacetime position coordinates*. We then define the *action* of this field to be written in terms of a *Lagrangian density*. By calculus of variations, we also get the *Euler-Lagrange equations*
$$\begin{align}
S[\hat\phi]&=\int d^4x\ \mathcal{L}\left(\hat\phi,\tfrac{\partial\hat\phi}{\partial x^\mu}\right), &&&
\delta S&=0
&\implies&&
\dfrac{\partial\mathcal{L}}{\partial\hat\phi}-\dfrac{\partial}{\partial x^\mu}\dfrac{\partial\mathcal{L}}{\partial\left(\tfrac{\partial\hat\phi}{\partial x^\mu}\right)}&=0.
\end{align}$$
For a theory of this nature to make sense to humans, we generally want to write this kind of system to be parametrized by an evolutionary parameter. For spacetime position, we define this parameter to be *time* $(t=x^0)$. This allows us to construct a constant-time hypersurface, which represents the configuration of the field and related operators at a singular point in time. If we now define a canonical conjugate field $\hat\pi(x)$ to our field $\hat\phi(x)$, we can also define the *Hamiltonian density* by a Legendre transform of the Lagrangian density
$$\begin{align}
\hat\pi(\vec{x})&\equiv\dfrac{\partial\mathcal{L}}{\partial\left(\tfrac{\partial\hat\phi}{\partial t}(\vec{x})\right)},
&\implies&&
\hat{\mathcal{H}}&=\hat\pi(\vec{x})\cdot\dfrac{\partial\hat\phi}{\partial t}(\vec{x})-\mathcal{L}
\end{align}$$
If we then integrate this Hamiltonian density over all space, we'll have a Hamiltonian parametrized solely by our new evolution parameter over time. Such an operator can then be used for many applications in Statistical Mechanics and quantum field time evolution.


### Noether's Theorem
For every system that has a continuous symmetry, there also exists a conservation law. Depending on the symmetry, a lot of simplifications can be made for our quantum fields.

Suppose we have a transformation of the field $\hat\phi(x)\to\hat\phi'(x)=\hat\phi(x)+\alpha\Delta\hat\phi(x)$ that leaves the action unchanged, then we expect (by the Euler-Lagrange equations) that the Lagrangian density remains invariant up to a four-divergence $\mathcal{L}(x)\to\mathcal{L}'(x)=\mathcal{L}(x)+\alpha\tfrac{\partial}{\partial x^\mu}\hat{\mathcal{J}}^\mu(x)$, and thus has current
$$\begin{align}
\hat{j}^\mu(x)&=\dfrac{\partial\mathcal{L}}{\partial\left(\tfrac{\partial\hat\phi}{\partial x^\mu}\right)}\Delta\hat\phi-\hat{\mathcal{J}}^\mu(x) &&&
\dfrac{\partial\hat{j}^\mu}{\partial x^\mu}(x)&=0
\end{align}$$
This conservation law can then be expressed as an integral over all space of the time component of the current to create a Noether charge $Q=\int d^3x\ \hat{j}^0(x)$. 

Now instead suppose we have a transformation of the *coordinates* $x^\mu\to x^\mu-a^\mu$, then this infinitesimal translation can be expressed as a transformation of the field
$$\begin{align}
\hat\phi(x)&\to\hat\phi(x+a)=\hat\phi(x)+a^\mu\dfrac{\partial\hat\phi}{\partial x^\mu}(x)
\end{align}$$
The Lagrangian is a scalar and so we expect it to transform as
$$\begin{align}
\mathcal{L}(x)\to\mathcal{L}'(x)=\mathcal{L}(x)+a^\mu\dfrac{\partial\mathcal{L}}{\partial x^\mu}=\mathcal{L}(x)+a^\nu\dfrac{\partial}{\partial x^\mu}\left(\delta_\nu^\mu\mathcal{L}\right)
\end{align}$$
This now has a non-zero $\hat{\mathcal{J}}^\mu(x)$, so we can then define the *energy-momentum tensor* as
$$\begin{align}
T^{\mu\nu}&\equiv\dfrac{\partial\mathcal{L}}{\partial\left(\tfrac{\partial\hat\phi}{\partial x^\mu}\right)}\dfrac{\partial\hat\phi}{\partial x_\nu}-\delta^{\mu\nu}\mathcal{L}
\end{align}$$
Over the equal-time hypersurfaces (integration over all space), the components of this tensor become the conserved charges of time and space translations
$$\begin{align}
\hat{H}&=\int d^3x\ T^{00} &\iff&& T^{00}&=\mathcal{H}\\
\hat{P}^i&=\int d^3x\ T^{0i} &\iff&& T^{0i}&=-\hat\pi(x)\cdot\dfrac{\partial\hat\phi}{\partial x^i}
\end{align}$$











Since our field is parametrized in spacetime position, we can define an operators who are eigenvalues of position, as well as canonical momentum operators as 
$$\begin{align}
\hat{x}^\mu\psi(x)&=x^\mu\psi(x) &\text{and}&& \hat{p}_\mu&=-i\hbar\dfrac{\partial}{\partial x^\mu}
\end{align}$$
Moreover, these operators have the commutation relation
$$\begin{align}
[\hat{x}^\mu,\hat{p}_\nu]&=i\hbar\delta^\mu_\nu &\iff&&
\hat{x}^\mu\hat{p}_\nu&=i\hbar\delta^\mu_\nu-\hat{p}_\nu\hat{x}^\mu
\end{align}$$
For an infinitesimal translation of the field in spacetime for all 4 coordinates, the associated generators of the translation are the canonical momentum operators previously defined, however upon evaluation, we get that
$$\begin{align}
\psi(x+dx)&=\exp\left(-i\hat{p}_\mu dx^\mu\right)\psi(x)\\
&=\exp\left(-i(\hat{p}_0 dt-\hat{p}\cdot d\vec{x}(t))\right)\psi(x)\\
\psi(x+dx)&=\exp\left(-i\left(\hat{p}_0-\hat{p}\cdot\frac{d\vec{x}}{dt}(t) \right)dt\right)\psi(x)
\end{align}$$
To have a proper time-evolution generator, we want this entire in terms of a displacement in the time coordinate $dt$, and thus the inside is the *generator of time evolution*. The canonical momentum operators are then instead the generators of the spacetime position coordinates. They are fundamentally different objects since the canonical momentum only translates the individual coordinates, while the generator of time evolution has the complete time evolution picture.
$$\begin{align}
\hat{H}&\equiv\hat{p}_0-\hat{p}\cdot\frac{d\vec{x}}{dt}  &\implies&&
\psi(x+dx)&=e^{-i\hat{H}dt}\psi(x)
\end{align}$$
This translation operator can be written as the exponential term
$$\begin{align}
U(\hat{P};a)&=e^{-i\hat{P}_\mu a^\mu/\hbar} &&&
U(\hat{H};t)&=e^{-i\hat{H}t/\hbar}
\end{align}$$
More explicitly, the Hamiltonian is the generator of time evolution, with the Schrödinger equation:
$$\begin{align}
\ket{\psi(t)}&=e^{-i\hat{H}(t-t_0)/\hbar}\ket{\psi(t_0)}
&\iff&&
i\hbar\dfrac{\partial}{\partial t}\ket{\psi(t)}&=\hat{H}\ket{\psi(t)}
\end{align}$$






## Quantum Field Theory (Spacetime Frequency)
*










# Spacetime Frequency Theory
Define the *spacetime frequency coordinates* as $k_\mu=(\omega,-\vec{k})$ in the typical fashion from QFT. 
Suppose there is a real scalar field $\hat\Pi$ parametrized by these coordinates. The action is
$$\begin{align}
B[\Pi]&=\int d^4k\ \mathscr{L}\left(\hat\Pi,\tfrac{\partial\hat\Pi}{\partial k_\mu}\right).
\end{align}$$
By calculus of variations, we get the Euler-Lagrange equations
$$\begin{align}
\delta B[\Pi]&=0
&\implies&&
\dfrac{\partial\mathscr{L}}{\partial\hat\Pi}-\dfrac{\partial}{\partial k_\mu}\dfrac{\partial\mathscr{L}}{\partial\left(\tfrac{\partial\hat\Pi}{\partial k_\mu}\right)}&=0.
\end{align}$$
Define the evolutionary parameter $\omega=k^0$ for frequency to construct a constant-frequency hypersurface. We can then define the canonical conjugate field to $\hat\Pi(k)$ to be
$$\begin{align}
\hat\Phi(k)&=\dfrac{\partial\mathscr{L}}{\partial\left(\tfrac{\partial\hat\Pi}{\partial k_0}\right)}.
\end{align}$$
We can then do the Legendre transform to find the frequency evolution operator
$$\begin{align}
\hat{\mathcal{Q}}&=\dfrac{\partial\mathscr{L}}{\partial\left(\tfrac{\partial\hat\Pi}{\partial k_0}\right)}\dfrac{\partial\hat\Pi}{\partial k_0}-\mathscr{L}=\hat\Phi\dfrac{\partial\hat\Pi}{\partial k_0}-\mathscr{L} &&&
\hat{Q}(\omega)&=\int d^3k\ \hat{\mathcal{Q}}
\end{align}$$
In our coordinate basis, we can define the frequency and canonical displacement operators as
$$\begin{align}
\hat{k}_\mu\Gamma(k)&=k_\mu\Gamma(k) &&& \hat{\chi}^\mu&=+i\hbar\dfrac{\partial}{\partial k_\mu}
\end{align}$$
where the canonical momentum operator is the generator of spacetime position translation, where
$$\begin{align}
U(\hat{\chi};b)&=e^{+i\hat{\chi}^\mu b_\mu/\hbar} &&&
[\hat{k}_\mu,\hat{\chi}^\nu]&=-i\hbar\delta^\mu_\nu
\end{align}$$











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





## Consequences
In position space, translation invariance means that physics is identical regardless of when $(t)$ or where $(x)$ you evaluate the system. In contract, translation invariance in frequency space means that physics is identical regardless of the base temporal frequency $(\omega)$ or spatial frequency $(k)$ scale of the system. Like how a wavepacket's energy and momentum remains constant as it moves through time, a wavepacket evolving in frequency space maintains a fixed center of spatial position and constant total-frequency density parameter $\hat{T}$.

Lorentz transforms on position space preserve the spacetime interval, conserve angular momentum and boost vectors. In frequency space, it preserves the mass shell, conserves a dual angular momentum, and a dual boost. Rotational symmetry in frequency space implies that the distribution of field excitations across directional frequency states $k$ is conserved as the system evolves in $\omega$.

In position space, the Klein-Gordon plane-wave solutions give us the dispersion relation
$$\begin{align}
E^2-(pc)^2=(mc^2)^2
\end{align}$$
While in the dual equation for frequency space $e^{-i(\tau\omega-X\cdot k)}$ gives the dispersion relation
$$\begin{align}
(c\tau)^2-X^2=c^2L^2
\end{align}$$
The mass shell restricts the energy $E(p)$, while the spatial shell restricts field response $\tau(X)$. There also exists group velocities
$$\begin{align}
v_g&=\dfrac{\partial\omega}{\partial k}=\frac{pc^2}{E}\le c
&\text{and}&&
\dfrac{\partial\tau}{\partial X}&=\frac{X}{c^2\tau}\le\frac{1}{c}
\end{align}$$
The dual of the typical group velocity forces the spacetime interval to only allow for causality since the square root will also be positive in this case, identical to how the group velocity must be slower than $c$ to preserve causality. 
























## Making Connections
Suppose we hypothesize that the time and frequency evolution generators are related as
$$\begin{align}
\hat{T}&=-i\alpha\hat{H}
\end{align}$$
This is inspired by the way that position and momentum are related by an imaginary number.

For the frequency evolution operator, we then get that
$$\begin{align}
U(\hat{T};\Delta\omega)
&=e^{-i\hat{T}\Delta\omega/\hbar}=e^{-(\alpha/\hbar)\hat{H}\Delta\omega}
\end{align}$$
In Statistical Mechanics, we have $e^{-\beta\hat{H}}$, and so if we equate them, we get that
$$\begin{align}
\beta=\dfrac{1}{kT}&=(\alpha/\hbar)\Delta\omega
&\implies&&
T&=\dfrac{\hbar}{k}\dfrac{1}{\alpha\Delta\omega}
\end{align}$$
Alternatively, we can connect Temperature to the identity
$$\begin{align}
\dfrac{1}{T}&=\dfrac{\partial S}{\partial E} &\implies&&
\dfrac{\partial S}{\partial E}&=\frac{k\alpha}{\hbar}\Delta\omega
\end{align}$$








## Creation and Annihilation Operators
For the Klein-Gordon Lagrangian in spacetime-position coordinates, we have that
$$\begin{align}
\phi(\vec{x})&=\int\dfrac{d^3p}{(2\pi)^3}\dfrac{1}{\sqrt{2E_\vec{p}}}\left(a_\vec{p}e^{-i\vec{p}\cdot\vec{x}}+a_\vec{p}^\dagger e^{+i\vec{p}\cdot\vec{x}}\right)
\end{align}$$





## Interesting Observations
I've noticed this a bunch but I really have a hard time trying to understand the meaning.

For a typical system, we can generate changes in the coordinates as
$$\begin{align}
\ket{\psi(t)}&=e^{-i\hat{H}(t-t_0)/\hbar}\ket{\psi(t_0)}
\end{align}$$
The exponent associated with statistical mechanics is
$$\begin{align}
e^{-\hat{H}/kT}=e^{-\tfrac{1}{k}\hat{H}\tfrac{1}{T}}=e^{-i\hat{H}\left(\tfrac{1}{iT}\right)/k}
\end{align}$$
The relationship between how the Hamiltonian, when integrated, generates the partition function in evolutionary parameter $T$, I wonder if a system can effectively change its temperature by a transformation that is also generated by the Hamiltonian.

Suppose a general transformation for a statevector
$$\begin{align}
\ket{\psi(\hbar\beta)}&=e^{-i\hat{H}\beta}\ket{\psi(0)}
\end{align}$$




What if we instead started in a momentum space?
$$\begin{align}
\ket{\Psi(\omega)}&=e^{-i\hat{T}(\omega-\omega_0)/\hbar}\ket{\Psi(\omega_0)}
&\iff&&
i\hbar\dfrac{\partial}{\partial\omega}\ket{\Psi(\omega)}&=\hat{T}\ket{\Psi(\omega)}
\end{align}$$
Then perhaps we have the relationship (for Klein-Gordon)
$$\begin{align}
-\frac{i}{\hbar}\hat{T}\Delta\omega&=\frac{\hat{H}}{kT}
&\implies&&
\hat{T}&=i\frac{\hbar^2}{kT\cdot\Delta E}\hat{H}
\end{align}$$






What if the idea behind Einstein's Field Equations
$$\begin{align}
R_{\mu\nu}-\dfrac{1}{2}Rg_{\mu\nu}+\Lambda g_{\mu\nu}&=\frac{8\pi G}{c^4}T_{\mu\nu}
\end{align}$$
is that the energy-stress tensor expressed in Spacetime Position Coordinates relating to the Geometry of the Spacetime Position Coordinates. There could be a dual of this.
$$\begin{align}
G_{\mu\nu}(x)&=\frac{8\pi G}{c^4}T_{\mu\nu}(x)
\end{align}$$
Instead of local spacetime curvature, suppose we have a dispersion curvature
$$\begin{align}
\mathcal{G}^{\mu\nu}(k)&=\kappa \mathcal{T}^{\mu\nu}(k)
\end{align}$$

### Spacetime Position Construction
We have a metric $g_{\mu\nu}(x)$ such that $ds^2=g_{\mu\nu}(x)\ dx^\mu\ dx^\nu$. We have Christoffel Symbols
$$\begin{align}
\Gamma_{\mu\nu}^\lambda(x)&=\dfrac{1}{2}g^{\lambda\alpha}\left(\dfrac{\partial}{\partial x^\mu}g_{\nu\alpha}+\dfrac{\partial}{\partial x^\nu}g_{\mu\alpha}-\dfrac{\partial}{\partial x^\alpha}g_{\mu\nu}\right)
\end{align}$$
and Riemann Curvature
$$\begin{align}
R_{\sigma\mu\nu}^\rho&=\dfrac{\partial}{\partial x^\mu}\Gamma_{\nu\sigma}^\rho-\dfrac{\partial}{\partial x^\nu}\Gamma_{\mu\sigma}^\rho+\Gamma_{\mu\lambda}^\rho\Gamma_{\nu\sigma}^\lambda-\Gamma_{\nu\lambda}^\rho\Gamma_{\mu\sigma}^\lambda
\end{align}$$
and Ricci tensor and scalar
$$\begin{align}
R_{\mu\nu}(x)&=R_{\mu\lambda\nu}^\lambda(x) &&& R(x)&=g^{\mu\nu}(x)R_{\mu\nu}(x)
\end{align}$$
### Spacetime Frequency Construction
We have a metric $g^{\mu\nu}(k)$ such that $ds^2=g^{\mu\nu}(k)\ dk_\mu\ dk_\nu$. We have Christoffel Symbols
$$\begin{align}
\Upsilon^{\mu\nu}_\lambda(k)&=\dfrac{1}{2}g_{\lambda\alpha}\left(\dfrac{\partial}{\partial k_\mu}g^{\nu\alpha}+\dfrac{\partial}{\partial k_\nu}g^{\mu\alpha}-\dfrac{\partial}{\partial k_\alpha}g^{\mu\nu}\right)
\end{align}$$
and Riemann Curvature
$$\begin{align}
\mathcal{R}^{\sigma\mu\nu}_\rho&=\dfrac{\partial}{\partial k_\mu}\Upsilon^{\nu\sigma}_\rho-\dfrac{\partial}{\partial k_\nu}\Upsilon^{\mu\sigma}_\rho+\Upsilon^{\mu\lambda}_\rho\Upsilon^{\nu\sigma}_\lambda-\Upsilon^{\nu\lambda}_\rho\Upsilon^{\mu\sigma}_\lambda
\end{align}$$
and Ricci tensor and scalar
$$\begin{align}
\mathcal{R}^{\mu\nu}(k)&=\mathcal{R}^{\mu\lambda\nu}_\lambda(k) &&& \mathcal{R}(x)&=g_{\mu\nu}(k)\mathcal{R}^{\mu\nu}(k)
\end{align}$$
