












We have the Lagrangian Density
$$\begin{align}
\mathcal{L}(x)&=\mathcal{T}(x)-\mathcal{V}(x)
\end{align}$$
where $x$ is a spacetime coordinate. These follow the Euler-Lagrange equations
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial\phi^\nu}-\partial_\mu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi^\nu)}\right)&=0
\end{align}$$
We also have the Hamiltonian Density
$$\begin{align}
\mathcal{H}(x)&=\dot{x}^\mu p_\mu-\mathcal{L}(x)
\end{align}$$





## Quantum Mechanics
The postulates of Quantum Mechanics are
1. The state of the system $\ket{\Psi}$ lives in a complex Hilbert space $\mathcal{H}$.
2. Observables $\hat{\mathcal{O}}$ are represented by Hermitian operators on $\mathcal{H}$.
3. The expectation value of an observable $\mathcal{O}$ is given by $\bra{\Psi}\hat{\mathcal{O}}\ket{\Psi}$.

### Comparison to Classical Mechanics
In Classical Mechanics
1. The state of a particle is characterized by it's position and momentum $(\vec{x},\vec{p})$.
2. The state of the particle evolves in time by Newton's Laws.
	1. Newtonian: $\vec{F}=\dfrac{d\vec{p}}{dt}$.
	2. Hamilton: $\dfrac{dx}{dt}=\dfrac{\partial H}{\partial p}$ and $\dfrac{dp}{dt}=-\dfrac{\partial H}{\partial x}$.

In Quantum Mechanics
1. The state of a particle is characterized by statevector $\ket{\Psi(t)}$.
2. The state of the particle evolves in time by Schrödinger's Equation $\hat{H}\ket{\Psi(t)}=i\hbar\dfrac{d}{dt}\ket{\Psi(t)}$.
3. The results of measurements are probabilistic.
	1. The probability of $\ket{\Psi}$ collapsing onto state $\ket{\alpha}$ is $\left|\left<\alpha\middle|\Psi\right>\right|^2$ (Born's rule).
4. There are observable quantities whose operators are Hermitian ($A^\dagger=A$).

### Generators
In Classical Mechanics, we have an operation called the Poisson bracket defined as
$$\begin{align}

\end{align}$$
The relationship between variables in these systems have the following relations:
$$\begin{align}
\dfrac{df}{dx}&=+\left\{f,p\right\}
&&&(p\text{ generates }x\text{ translation})\\
\dfrac{df}{dp}&=-\left\{f,x\right\}
&&&(x\text{ generates }p\text{ translation})\\
\dfrac{df}{dt}&=\left\{f,H\right\}+\dfrac{\partial f}{\partial t}
\end{align}$$
Similarly, in Quantum Mechanics, we also have such generators where
$$\begin{align}
\dfrac{\partial}{\partial x}&=-\dfrac{\hat{p}}{i\hbar}
&&&(p\text{ generates }x\text{ translation})\\
\dfrac{\partial}{\partial p}&=+\dfrac{\hat{x}}{i\hbar}
&&&(x\text{ generates }p\text{ translation})\\
\end{align}$$
This is called Canonical Quantization, used to turn a classical theory into a quantum theory.
### Time Evolution Operator
To generate time evolution in our statevectors, we can use the translation from Lie Theory:
$$\begin{align}
e^{a\tfrac{d}{dx}}f(x)&=f(x+a) &\implies&& e^{\Delta t\tfrac{d}{dt}}\ket{\Psi(t)}=\ket{\Psi(t+\Delta t)}
\end{align}$$
We can instead write operator, using $\frac{d}{dt}=\frac{\hat{H}}{i\hbar}$, as a matrix $U$ such that
$$\begin{align}
U(\Delta t)&=e^{\Delta t\frac{\hat{H}}{i\hbar}} &\text{where}&& U(\Delta t)\ket{\Psi(t)}=\ket{\Psi(t+\Delta t)}
\end{align}$$
To preserve the probability density of this state, we'll need to impose that inner product squared remains unchanged under an arbitrary time translation $\Delta t$ such that
$$\begin{align}
\left|\left<\Psi(t+\Delta t)\middle|\Psi(t+\Delta t)\right>\right|^2&=\left|\left<\Psi(t)\middle|\Psi(t)\right>\right|^2
\end{align}$$
This requires that the time evolution operator must have the following relationships
$$\begin{align}
U^\dagger(\Delta t)&=+U^{-1}(\Delta t)&&\text{If Hermitian}\\
U^\dagger(\Delta t)&=-U^{-1}(\Delta t)&&\text{If Anti-Hermitian}
\end{align}$$
### Commutators

$$\begin{align}
\left[\hat{x},\hat{p}\right]&=i\hbar
\end{align}$$