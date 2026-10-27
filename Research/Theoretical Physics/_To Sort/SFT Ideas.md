
Some ideas I had for Statistical Field Theory are:
1. Non-Linear Modes: Might explain things like generations of particles as the sum of linear modes cannot reconstruct these new modes.
2. Coordinates parametrized by fields (as opposed to fields parametrized by coordinates)




Suppose we have a partition function
$$\begin{align}
\mathcal{Z}&=\int e^{-H/kT}
\end{align}$$
Using the definition of temperature
$$\begin{align}
\frac{1}{T}&=\left(\dfrac{\partial S}{\partial E}\right)_{V,N}
\end{align}$$
Then in a way, the partition functions is
$$\begin{align}
\mathcal{Z}&=\int\left.\exp\left(-\dfrac{1}{k}\dfrac{\partial S}{\partial E}E\right)\right|_{V,N}
\end{align}$$
If we introduce the chemical potential as well, we get a similar system
$$\begin{align}
\mathcal{Z}&=\int\exp\left(-\dfrac{1}{k}\left.\dfrac{\partial S}{\partial E}\right|_{V,N}E-\dfrac{1}{k}\left.\dfrac{\partial S}{\partial N}\right|_{E,V}N\right)
\end{align}$$
Interestingly, what you effectively get is an expression of some quantity in terms of a Legendre Transform. Supposing we want a quantity parametrized by $E,N,V$, then it relates to Entropy by
$$\begin{align}
\dfrac{1}{kT}X&=\dfrac{1}{k}\dfrac{\partial S}{\partial E}E+\dfrac{1}{k}\dfrac{\partial S}{\partial N}N+\dfrac{1}{k}\dfrac{\partial S}{\partial V}V-\dfrac{1}{k}S
\end{align}$$
We know by Thermodynamic identities that
$$\begin{align}
\dfrac{\partial S}{\partial E}&=\dfrac{1}{T} &
\dfrac{\partial S}{\partial N}&=-\frac{\mu}{T} &
\dfrac{\partial S}{\partial V}&=\frac{P}{T}
\end{align}$$
Substituting, we get that
$$\begin{align}
X&=E-\mu N+PV-TS
\end{align}$$











Suppose you have a Klein-Gordon Field
$$\begin{align}
\mathcal{L}(\phi,\partial_\mu\phi)&=(\partial_\mu\phi^*)(\partial^\mu\phi)-m^2\phi^*\phi
\end{align}$$
It has conjugate momenta
$$\begin{align}
\pi&=\dfrac{\partial\mathcal{L}}{\partial\dot\phi}=\dot\phi^* &
\pi^*&=\dfrac{\partial\mathcal{L}}{\partial\dot\phi^*}=\dot\phi 
\end{align}$$
And Hamiltonian density
$$\begin{align}
\mathcal{H}&=\dfrac{\partial\mathcal{L}}{\partial\dot\phi}\dot\phi+\dfrac{\partial\mathcal{L}}{\partial\dot\phi^*}\dot\phi^*\\
&=\left|\dot\phi\right|^2+\left|\vec\nabla\phi\right|^2+m^2\left|\phi\right|^2\\
\mathcal{H}&=\pi^*\pi+\vec\nabla\phi^*\cdot\vec\nabla\phi+m^2\phi^*\phi\\
\end{align}$$
For a conserved $\mathrm{U}(1)$ charge, the grand canonical operator is
$$\begin{align}
K&=H-\mu Q=\int d^3 x\left[\pi^*\pi+\vec\nabla\phi^*\cdot\vec\nabla\phi+m^2\phi^*\phi-\mu i\left(\phi^*\pi^*-\pi\phi\right)\right]
\end{align}$$
In terms of creation and annihilation operators $a_\vec{p}^\dagger,a_\vec{p}$ (particles) and $b_\vec{p}^\dagger,b_\vec{p}$ (anti-particles) respectively, we can write this operator instead as
$$\begin{align}
K&=\int\dfrac{d^3p}{(2\pi)^3}\left[(E_\vec{p}-\mu)a_\vec{p}^\dagger a_\vec{p}+(E_\vec{p}+\mu)b_\vec{p}^\dagger b_\vec{p}\right]
\end{align}$$

