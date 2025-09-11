Author: Stanley Goodwin
Date: August XX, 2025

---
### Elementary Particle Dynamics

#### The Four forces of nature
At low energy (long distance):
 - Electromagnetism
 - Weak force
 - Strong Nuclear force
 - Gravity
At high energy (short distance)
 - Weak hypercharge $\text{U}(1)_\gamma$
 - Weak isospin $\text{SU}(2)_L$
 - Color Charge $\text{SU}(3)_c$
 - Gravity?
The force carriers:
 - Hypercharge $\text{U}(1)_\gamma$ boson $B_\mu(x)$
 - Isospin $\text{SU}(2)_L$ bosons $W_\mu^a(x)$
 - Gluons $G_\mu^A(x)$
 - Gravitons $h_{\mu\nu}(x)$

### Propagator Theory
Green's functions are important in a lot of physics.
They take a source on some surface and generate a solution everywhere else.

In QFT, Green's functions are often called propagators.
They tell us how probability for a disturbance in a vacuum (particles) propagate out from an initial state to other place and states in spacetime.
We represent these propagators as lines (components of a Feynman Diagram).

#### Example
Suppose a free Hamiltonian $H_0$ and a potential $V(t,\vec{x})$ that is turned off in the distant past.
In the past, we have a free particle solution:
$$\begin{align}
\left(i\dfrac{\partial}{\partial t}-H_0\right)\psi_0(t,\vec{x})&=0
\end{align}$$
At later times, we have the solutions of:
$$\begin{align}
\left(i\dfrac{\partial}{\partial t}-H_0\right)\psi(t,\vec{x})&=V(t,\vec{x})\psi(t,\vec{x})
\end{align}$$
The general solution is given in terms of the free-particle green's function $G_0$:
$$\begin{align}
\psi(t,\vec{x})&=\psi_0(t,\vec{x})+\int G_0(t,\vec{x};t',\vec{x}')V(t',\vec{x}')\psi(t',\vec{x}')\ dt'd^3x'
\end{align}$$


In relativistic theories, particles can get created and destroyed.
We'll have rules (called vertices) where propagators end and others begin.

#### Quantum Electrodynamics
QED is a theory of electrons, positrons, and photons. It starts from the Dirac Field and enforcing a $\text{U}(1)$ symmetry on the field. The symmetry results in Electromagnetism.
#### Quantum Chromodynamics
Quarks and Gluons are color-charged. The only valid interactions are:
 - 3 Gluon interaction
 - 4 Gluon interaction
 - Quark emitting Gluon
The self-interaction leads to flux tubes.
#### Quantum Weak Dynamics
It's called weak because the timescales of decay are significantly longer than electromagnetism.
The weak force doesn't have immediately-obvious charges.
 - This is from the spontaneous symmetry break in the field.
With electroweak theory, we'll see that the weak force is in terms of weak isospin and weak hypercharge.
There are also self-interactions since it's non-abelian.

### Electroweak Unification
The electroweak theory starts with 4 massless exchange particles:
$$\begin{align}
W^+,W^-, W^3, B
\end{align}$$
The electroweak symmetry is broken and the $W^\pm$ gains mass, as done a linear combination of $W^3$ and $B$. We can write this as:
$$\begin{align}
Z^0&=\cos\theta_w W^3-\sin\theta_w B
\end{align}$$
The other linear combination remains massless:
$$\begin{align}
A&=\sin\theta_w W^3+\cos\theta_w B
\end{align}$$
This is what we call the photon.
