# Waves and Particles

## Historical Precedent
There are many experiments in early modern physics that influenced the the trajectory of quantum mechanics; such examples are Planck's quantization of thermal radiation, Einstein's quantization of photoelectron emission determined by energy, and Young's double-slit experiment. All together, these describe that electromagnetic waves are wave-like and particle-like dependent on the specifics of the experiment. The field of *quantum mechanics* is the physics of how material particles are wave-like, as opposed to the classical mechanics assertion of particles being point-like and overtly deterministic in nature.

## Quantization of Electromagnetic Radiation
The emission of electromagnetic radiation takes place when a quantum system transitions from one energy state to another, with the difference in the energy proportional to the frequency of the radiation. The total energy must remain conserved, leading to the requirement
$$\begin{align}
E_\text{final}-E_\text{initial}+\hbar\omega&=0,&E_\text{initial}\gt E_\text{final}
\end{align}$$
where $E_\text{initial}$ is the initial energy of the system, $E_\text{final}$ is the final energy of the system, $\omega$ is the frequency of electromagnetic radiation, and $\hbar$ is the reduced Planck's constant $h/2\pi$. Importantly, the transition must take place from a higher energy state to a lower one, so that the photon always has positive definite energy.

## Quantization of Momentum
Historically, de Broglie had conjectured that matter and light would have similar mechanics in terms of momentum, energy, space, etc. The relationship between momentum and spatial frequency is written in terms of the wavevector $\vec{k}$ such that
$$\begin{align}
\vec{p}&=\hbar\vec{k}
\end{align}$$
For particles with mass, he conjectured that they also have a wavevector that corresponds to its momentum as well. For the photon, the momentum is a consequence of the energy of the photon, in contract to classical particles having momentum from mass. For massive particles, the wavevector that corresponds to it is
$$\begin{align}
\vec{k}&=\frac{m}{\hbar}\vec{v} &\iff&& \vec{p}&=\hbar\vec{k}=m\vec{v}
\end{align}$$

## Wavefunctions & The Schrodinger Equation
For the classical concept of a trajectory, we must substitute it for a time-varying wavefunction representing the state of a particle, typically written as $\psi(\vec{r},t)$. This wavefunction is interpreted as effectively a "square root" of a probability density, where
$$\begin{align}
\rho(\vec{r},t)&=\left|\psi(\vec{r},t)\right|^2
\end{align}$$
To determine the probability of a particle's existence within a volume $V$ at time $t$, we integrate this probability density over this regime, written as
$$\begin{align}
p(t)&=\int_V\left|\psi(\vec{r},t)\right|^2 d^3r
\end{align}$$
Importantly, the particle must exist somewhere in space, so if we integrate this density over all space, it must have a probability of $1$, leading to the normalization condition:
$$\begin{align}
\int_{\mathbb{R}^3}\left|\psi(\vec{r},t)\right|^2 d^3r&=1
\end{align}$$
The principle of spectral decomposition requires that a state can be represented in terms of an appropriate choice of basis, often the eigenbasis of a system. Using vector projection, we can write any arbitrary state such that
$$\begin{align}
\ket{\psi(\vec{r},t)}&=\int\ket{\phi(\vec{r},t)}\left<\phi(\vec{r},t)\middle|\psi(\vec{r},t)\right>
\end{align}$$
Where the integration is done over all elements of $\phi$ so this effectively becomes a vector sum of this new basis. This should be familiar to any student who has learned linear algebra.

The Schödinger Equation in differential form is
$$\begin{align}
i\hbar\dfrac{\partial}{\partial t}\ket{\psi(\vec{r},t)}&=-\dfrac{\hbar^2}{2m}\vec\nabla^2\ket{\psi(\vec{r},t)}+V(\vec{r},t)\ket{\psi(\vec{r},t)}
\end{align}$$











## Tangent Section
Start with the evolution operator and approximate it to the first order
$$\begin{align}
\ket{\psi(\vec{r},t+dt)}=e^{-i\hat{H}dt/\hbar}\ket{\psi(\vec{r},t)}&\approx\left(1-\frac{i}{\hbar}\hat{H} dt\right)\ket{\psi(\vec{r},t)}
\end{align}$$
We can take this and rewrite it as a first-order differential of the form
$$\begin{align}
\ket{\psi(\vec{r},t+dt)}&=\ket{\psi(\vec{r},t_0)}-\frac{i}{\hbar}\hat{H} \ket{\psi(\vec{r},t)}dt\\
\hat{H} \ket{\psi(\vec{r},t_0)}&=i\hbar\frac{\ket{\psi(\vec{r},t+dt)}-\ket{\psi(\vec{r},t)}}{dt}
\end{align}$$
In the limit as $dt\to0$, the fraction becomes the definition of the derivative, and so
$$\begin{align}
\ket{\psi(\vec{r},t+dt)}&=\ket{\psi(\vec{r},t)}-\frac{i}{\hbar}\hat{H} \ket{\psi(\vec{r},t)}dt\\
\hat{H} \ket{\psi(\vec{r},t)}&=i\hbar\dfrac{\partial}{\partial t}\ket{\psi(\vec{r},t)}
\end{align}$$
This is the Time-Dependent Schrodinger Equation, which comes from the linearization of the exponential around a small time displacement, as all other factors are of higher order, and thus can be neglected. The non-linearity of finite-time evolution shows up in how the Hamiltonian at each time are not simultaneous operators, and have commutators.

Evolving twice we have
$$\begin{align}
\ket{\psi(\vec{r},t+2dt)}&=e^{-i\hat{H}(t+dt)dt/\hbar}e^{-i\hat{H}(t)dt/\hbar}\ket{\psi(\vec{r},t)}
\end{align}$$
We can linearize both operators to be
$$\begin{align}
\ket{\psi(\vec{r},t+2dt)}&=\left(1-\frac{i}{\hbar}\hat{H}(t+dt) dt\right)\left(1-\frac{i}{\hbar}\hat{H}(t) dt\right)\ket{\psi(\vec{r},t)}\\
\dfrac{\partial^2}{\partial t^2}\ket{\psi(\vec{r},t)}&=-\frac{i}{\hbar}\left(\dfrac{\partial}{\partial t}-i\dfrac{\hat{H}(t+dt)}{\hbar}\right)\hat{H}(t)\ket{\psi(\vec{r},t)}
\end{align}$$



