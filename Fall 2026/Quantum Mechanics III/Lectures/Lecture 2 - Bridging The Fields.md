**Author:** Stanley Goodwin
**Date:** September 29th, 2026
Resource Name: Spinors for Beginners 21: Intro to Quantum Field Theory
Resource URL: https://www.youtube.com/watch?v=uE6q-dxjrlA

---
## Relativistic Field Theory
We want to integrate Special Relativity into our Classical Field Theory models.
1. Maxwell's Equations are consistent with Special Relativity.
	1. The form of the equations doesn't change under a Lorentz transformation.
2. Poisson Equation for Newtonian Gravity is not consistent with Special Relativity.
	1. There are no time derivatives, only space derivatives.
	2. Equation changes form under a Lorentz transformation.
		1. Interactions occur instantaneously.
		2. Forces look different dependent on frame.
	3. To fix these issues, we'd need to invent General Relativity.

Special Relativity imposes that only certain objects can exist while remaining consistent, where these fields are of spin integer and spin half-integer fields, such as:
$$\begin{align}
\text{Klein Equation}&&
\left(\partial^\mu\partial_\mu+m^2\right)\phi&=0 && \phi:\text{Spin-}0\\
\text{Dirac Equation}&&
\left(i\gamma^\mu\partial_\mu-m\right)\psi&=0 && \psi:\text{Spin-}1/2\\
\text{Proca Equation}&&
\partial_\mu\left(\partial^\mu A^\nu+\partial^\nu A^\mu\right)+m^2 A^\nu&=0 && \psi:\text{Spin-}1\\
\dots
\end{align}$$
The important distinction between classical fields and quantum fields is
- A classical field knows exactly its positions and momenta.
- A quantum field has uncertainty in field position and momenta.

---
### Klein-Gordon Equation
Suppose we have a scalar (Spin-$0$) field $\phi$ of $N$ components. Either as an implied sum over all $n\in\{1,2,\dots, N\}$, or instead treating $\phi$ as a vector, we can write the Lagrangian Density as
$$\begin{align}
\mathcal{L}(x)&=\dfrac{1}{2}\left(\partial^\mu\phi_n^*\right)\left(\partial_\mu\phi_n\right)-\dfrac{1}{2}m_n^2\phi_n^*\phi_n
&\iff&&
\mathcal{L}(x)&=\dfrac{1}{2}\left(\partial^\mu\vec\phi^\dagger\right)\left(\partial_\mu\vec\phi\right)-\dfrac{1}{2}\vec\phi^\dagger M^2\vec\phi
\end{align}$$
Using the Euler-Lagrange equations in every component $(\phi_n,\phi_n^*)$, we find the equations of motion
$$\begin{align}
\left(\partial^\mu\partial_\mu+m_n^2\right)\phi_n&=0
=\left(\partial^\mu\partial_\mu+m_n^2\right)\phi_n^* &\iff&& \left(\partial^\mu\partial_\mu+M^2\right)\vec\phi&=0
=\left(\partial^\mu\partial_\mu+M^2\right)\vec\phi^\dagger
\end{align}$$
---
### Dirac Equation
Suppose we have a spinor (Spin-$1/2$) field $\psi$. We can write the Lagrangian Density as
$$\begin{align}
\mathcal{L}(x)&=\bar\psi\left(i\gamma^\mu\partial_\mu-m\right)\psi
\end{align}$$
Using the Euler-Lagrange equations in $\psi,\bar{\psi}$, we find the equations of motion
$$\begin{align}
\left(i\gamma^\mu\partial_\mu-m\right)\psi&=0=\left(i\gamma^\mu\partial_\mu-m\right)\bar{\psi}
\end{align}$$
---
### Maxwell's Equations
Suppose we have a vector (Spin-$1$) field $A$. We can write the Lagrangian Density as
$$\begin{align}
\mathcal{L}(x)&=-\dfrac{1}{4\mu_0}F^{\mu\nu}F_{\mu\nu}-A_\mu J^\mu & F^{\mu\nu}&\equiv\partial^\mu A^\nu-\partial^\nu A^\mu
\end{align}$$
Using the Euler-Lagrange equations in every component $A_\nu$, we find the equations of motion
$$\begin{align}
\partial_\mu F^{\mu\nu}&=\mu_0J^\nu
\end{align}$$
---
### Proca Equation
Suppose we have a vector (Spin-$1$) field $B$ that also contain mass $m$ to the field. We can write the Lagrangian Density similar to Maxwell's Equations as
$$\begin{align}
\mathcal{L}(x)&=-\dfrac{1}{4\mu_0}F^{\mu\nu}F_{\mu\nu}-\dfrac{1}{2}m^2B^\mu B_\mu & F^{\mu\nu}&\equiv\partial^\mu B^\nu-\partial^\nu B^\mu
\end{align}$$
Using the Euler-Lagrange equations in every component $A_\nu$, we find the equations of motion
$$\begin{align}
\partial_\mu F^{\mu\nu}+m^2 B^\nu&=0
\end{align}$$
---
## Relativistic Quantum Mechanics
Prior to Quantum Field Theory, physicists tried to make the position Schrodinger Equation satisfy Special Relativity. We start with the classical Schrödinger equation
$$\begin{align}
\hat{H}\ket{\Psi(t)}&=i\hbar\dfrac{d}{dt}\ket{\Psi(t)}
&\implies&&
\hat{H}\Psi(t,\vec{x})&=i\hbar\dfrac{d}{dt}\Psi(t,\vec{x})
\end{align}$$
These wavefunctions are not spacetime objects, since multiple-particle states contain the same time coordinate while including every new position vector in its inputs.

Applying the canonical quantization rules, as well as the standard kinetic and potential energies, we see that the Schrödinger equation for a single particle is
$$\begin{align}
i\hbar\dfrac{d\Psi}{dt}&=-\frac{\hbar^2}{2m}\dfrac{\partial^2\Psi}{\partial x^2}+V(x)\Psi
\end{align}$$
The derivatives in time and space are not on equal standing, and thus isn't Lorentz Invariant.

### Using Energy-Momentum
Suppose we instead start with the energy-momentum relation, and canonical quantization
$$\begin{align}
\hat{E}&=i\hbar\dfrac{\partial}{\partial t}, &
\hat{p}^j&=i\hbar\dfrac{\partial}{\partial x^j}, &
E^2-\vec{p}^2&=m^2,
&\implies&&
m^2&=-\hbar^2g^{\mu\nu}\partial_\mu\partial_\nu
\end{align}$$
This then gives us an equation of motion for a wavefunction of the form
$$\begin{align}
\left[g^{\mu\nu}\partial_\mu\partial_\nu+\left(\dfrac{mc}{\hbar}\right)^2\right]\Psi&=0
\end{align}$$
This is almost identical to the Klein-Gordon equation in classical relativistic field theory, where our original mass term $m$ is replaced by $\mu\equiv\tfrac{mc}{\hbar}$.

### Trouble with Initial Conditions
In the original Schrodinger equation, we can specify the initial statevector $\Psi(t_0,\vec{x})$ to determine the evolution of that statevector over time. The equation of motion also conserves the probability density in time and space, as well as the continuity of such probability density, given by
$$\begin{align}
\rho(t,\vec{x})=\left|\Psi(t,\vec{x})\right|^2&\ge0\\
\dfrac{\partial\rho}{\partial t}-\dfrac{i\hbar}{2m}\vec\nabla\cdot\left[\Psi^*\vec\nabla\Psi-\Psi\vec\nabla\Psi^*\right]&=0
\end{align}$$
However, the Klein-Gordon equation requires that we specify both the initiate statevector $\Psi(t_0,\vec{x})$, as well as its time derivative $\partial_t\Psi(t_0,\vec{x})$, in order to determine its evolution. Given this extra degree of freedom, there is no probability interpretation that remains consistent. The naive definition of the inner product $\Psi^*\Psi\ge0$ is not conserved. There is a quantity that is conserved,
$$\begin{align}
\rho&=\Psi^*\dfrac{\partial\Psi}{\partial t}-\Psi\dfrac{\partial\Psi^*}{\partial t}\not\ge0
\end{align}$$
but this quantity can also become negative, since we are free to choose the initial statevector and its derivative in time. To try and circumvent this issue, Paul Dirac tried to modify the Klein-Gordon equation to be first-order in time and space, thus only requiring an initial statevector only. Suppose there exists matrices $\gamma^\mu$ such that $\gamma^\mu\gamma^\nu+\gamma^\nu\gamma^\mu=0$ and $\gamma^\mu\gamma^\mu=g_{\mu\mu}$, then we can factor the Klein-Gordon equation into two parts:
$$\begin{align}
\left(\gamma^\nu\partial_\nu-i\dfrac{mc}{\hbar}\right)\left(\gamma^\mu\partial_\mu+i\dfrac{mc}{\hbar}\right)\Psi&=0
\end{align}$$
If we take the 2nd term in this expression, we get the Dirac equation. This statevector $\Psi$ now corresponds to a Dirac bispinor with 4 components total, and has probability density
$$\begin{align}
\rho&=\bar\Psi\gamma^0\Psi\ge0\text{ and is conserved.}
\end{align}$$
However, a new issue comes from there now being positive and negative energy solutions.

### The Fundamental Issue
The core idea of the Schrodinger equation is that there exists an operator $U$ that generates time-translation in the statevector such that
$$\begin{align}
U(\Delta t)&=e^{\Delta t\frac{\hat{H}}{i\hbar}}
&\implies&&
U(\Delta t)\ket{\Psi(t)}&=\ket{\Psi(t+\Delta t)}
\end{align}$$
The Schrodinger equation is something that we do want to keep in this relativistic theory, but we'll need to be more careful about the properties of such operators.

---
## Quantum Field Theory
Experimentally, we have determined that particles can be created and destroyed. We will want to develop a theory that can allow for particles to transition into different particles and quantity. Originally, the wavefunction for a single particle cannot describe changing type or number, so we instead will create a field that has creation and annihilation operators.

### Construction of Oscillators
For classical fields, we imagined an array of coupled classical oscillators. In Quantum fields, we will similarly join quantum oscillators together in a large array. Each oscillator has its own statevector, observable operators, and creation/annihilation operators:
$$\begin{align}
\ket{\Psi_{i}(t)}:(\hat{x}_i,\hat{p}_i,\hat{a}_i^\dagger,\hat{a}_i) 
\end{align}$$
The statevector of the total system is the tensor product of these statevectors
$$\begin{align}
\ket{\Psi(t)}&=\bigotimes_{i=1}^N\ket{\Psi_{i}(t)}
\end{align}$$
Importantly, the operators between each state all commute, giving the relations
$$\begin{align}
\left[\hat{x}_i,\hat{x}_j\right]&=0 &
\left[\hat{p}_i,\hat{p}_j\right]&=0 &
\left[\hat{x}_i,\hat{p}_j\right]&=i\hbar\delta_{ij}\\
\left[\hat{a}_i,\hat{a}_j\right]&=0 &
\left[\hat{a}_i^\dagger,\hat{a}_j^\dagger\right]&=0 &
\left[\hat{a}_i,\hat{a}_j^\dagger\right]&=\delta_{ij} &
\end{align}$$
### Extending to the Continuum
We now imagine that the field is now the dynamical variable. We also now define the field position operator $\hat\phi(x)$ and the field momentum operator $\hat\pi(x)$. Similarly, we now have the commutators
$$\begin{align}
\left[\hat\phi(x),\hat\phi(x')\right]&=0 &
\left[\hat\pi(x),\hat\pi(x')\right]&=0 &
\left[\hat\phi(x),\hat\pi(x')\right]&=i\hbar\delta(x-x')
\end{align}$$
The ladder operators are similarly constructed as
$$\begin{align}
\hat{a}(x)&\equiv\sqrt{\frac{m}{2\hbar}}\left(\hat\phi(x)+\frac{i}{m}\hat\pi(x)\right) & \hat{a}^\dagger(x)&\equiv\sqrt{\frac{m}{2\hbar}}\left(\hat\phi(x)-\frac{i}{m}\hat\pi(x)\right)
\end{align}$$
$$\begin{align}
\left[\hat a(x),\hat a(x')\right]&=0 &
\left[\hat a^\dagger(x),\hat a^\dagger(x')\right]&=0 &
\left[\hat a(x),\hat a^\dagger(x')\right]&=\delta(x-x')
\end{align}$$

### Klein-Gordon Field
The classical Klein-Gordon field has the Hamiltonian Density
$$\begin{align}
\mathcal{H}&=\dfrac{1}{2}\left(\partial_t\phi\right)^2+\dfrac{1}{2}\left(\vec{\nabla}\phi\right)^2+\dfrac{1}{2}m^2\phi^2
\end{align}$$
In quantum field theory, these now just become operators (Field Quantization)
$$\begin{align}
\hat{\mathcal{H}}&=\dfrac{1}{2}\left(\partial_t\hat\phi\right)^2+\dfrac{1}{2}\left(\vec{\nabla}\hat\phi\right)^2+\dfrac{1}{2}m^2\hat\phi^2
\end{align}$$
From Hamiltonian Mechanics, we also have the canonical momentum (for Klein-Gordon)
$$\begin{align}
\pi&\equiv\dfrac{\partial\mathcal{L}}{\partial(\partial_t\phi)}=\partial_t\phi
&\implies&&
\hat{\mathcal{H}}&=\dfrac{1}{2}\hat\pi^2+\dfrac{1}{2}m^2\hat\phi^2+\dfrac{1}{2}\left(\vec{\nabla}\hat\phi\right)^2
\end{align}$$
The normal modes for Klein-Gordon are the set of sinusoidal equations
$$\begin{align}
\phi_k(t,x)&=A(k)e^{i(\omega t-\vec{k}\cdot\vec{x})} & m^2=\omega^2-k^2
\end{align}$$
For the remainder of this section, we will assume all operators act at a constant time.

We can relate the field $\phi(x),\pi(x)$ to $\phi(k),\pi(k)$ by the Fourier transform, written unitarily as
$$\begin{align}
\phi(t,k)&=\dfrac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}dx\ e^{-ikx}\phi(t,x)
&\iff&&
\phi(t,x)&=\dfrac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}dk\ e^{+ikx}\phi(t,k)\\
\pi(t,k)&=\dfrac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}dx\ e^{-ikx}\pi(t,x)
&\iff&&
\pi(t,x)&=\dfrac{1}{\sqrt{2\pi}}\int_{-\infty}^{+\infty}dk\ e^{+ikx}\pi(t,k)\\
\end{align}$$
As a reminder, we have the momentum relation $p=\hbar k$. These Fourier transforms are no longer Hermitian, and thus can be complex numbers. We'll use the square magnitude in the future.

If we take the Fourier transform of the Hamiltonian density, we arrive at
$$\begin{align}
\hat{\mathcal{H}}(t,k)&=\dfrac{1}{2}\left|\hat\pi(t,k)\right|^2+\dfrac{1}{2}(m^2+k^2)\left|\hat\phi(t,k)\right|^2=\dfrac{1}{2}\left|\hat\pi(t,k)\right|^2+\dfrac{1}{2}\omega(k)^2\left|\hat\phi(t,k)\right|^2
\end{align}$$

---
## Conclusion
The Schrodinger equation still applies in Quantum Field Theory, but the wavefunction does not live in normal position space, it lives in the space of all possible fields; it also makes sure that the time evolution operator is unitary so that probability is conserved.

### Relativistic Quantum Field Theory
Based on the section about Relativistic Field Theory, we have multiple Lagrangian densities for different types of objects in our universe. We can also add components to the Lagrangian density in order to couple interactions. This often leads to non-linearities, which make solutions to be more complicated to solve, but the Schrödinger equation is still linear.
$$\begin{align}
\hat{H}\Psi\left[t,\psi,\vec{A}\right]&=i\hbar\dfrac{\partial}{\partial t}\Psi\left[t,\psi,\vec{A}\right] & \text{(for Photon-Electron Interaction)}
\end{align}$$
#### Klein-Gordon Field (Spin-$0$)
$$\begin{align}
\mathcal{L}&=\dfrac{1}{2}\left(\partial^\mu\phi^*\right)\left(\partial_\mu\phi\right)-\dfrac{1}{2}m^2\phi^*\phi &
\left[\phi(\vec{x}),\pi(\vec{x}')\right]&=i\hbar\delta^3(\vec{x}-\vec{x}')
\end{align}$$
#### Dirac Field (Spin-$1/2$)
$$\begin{align}
\mathcal{L}&=\bar\psi\left(i\gamma^\mu\partial_\mu-m\right)\psi &
\left\{\psi(\vec{x}),\pi_\psi(\vec{x}')\right\}&=i\hbar\delta^3(\vec{x}-\vec{x}')
\end{align}$$
#### Proca Field (Spin-$1$)
$$\begin{align}
\mathcal{L}&=-\dfrac{1}{4\mu_0}F^{\mu\nu}F_{\mu\nu}-\dfrac{1}{2}m^2B^\mu B_\mu &
\left[B_i(\vec{x}),\pi_{B_j}(\vec{x}')\right]&=i\hbar\delta^3(\vec{x}-\vec{x}')\delta_{ij}
\end{align}$$
### Non-Relativistic Quantum Field Theory
There are also some cases where the classical approximation still gives helpful results.
#### Schrödinger Field (Spin-$0$)
$$\begin{align}
\mathcal{L}&=\psi^\dagger\left(i\hbar\dfrac{\partial}{\partial t}+\dfrac{1}{2m}\vec\nabla^2\right)\psi & \pi&=i\hbar\psi\\
\left[\psi(\vec{x}),\pi(\vec{x}')\right]&=i\hbar\delta^3(\vec{x}-\vec{x}') &
\left(i\hbar\dfrac{\partial}{\partial t}+\dfrac{1}{2m}\vec\nabla^2\right)\psi&=0
\end{align}$$
### Path-Integral Formulation
$$\begin{align}
\int\mathcal{D}q(t)\ e^{\frac{i}{\hbar}S[q(t)]}
\end{align}$$
### Spin-Statistics Theorem
States that
- Integer spin particles are Bosons
	- Identical particles can contain the same state
	- Operators use commutation relations
	- Wavefunctions are symmetric under particle exchange
- Half-integer spin particles are Fermions
	- Identical particles cannot contain the same state
	- Operators use anti-commutation relations
	- Wavefunctions are antisymmetric under particle exchange
