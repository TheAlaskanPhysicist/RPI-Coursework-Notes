## 2.1 : Time Evolution and the Schrödinger Equation
Time is a parameter in quantum mechanics, not an operator.
Time is not an observable in the language of chapter 1.

### 2.1.1 : Time-Evolution Operator
For time translations, we can define an operator:
$$\begin{align}
U(t;t_0)\ket{\alpha,t_0}=\ket{\alpha,t_0; t}
\end{align}$$
We can represent the state vectors as the following form:
$$\begin{align}
\ket{\alpha,t_0}=\ket{\alpha,t_0; t_0}&=\sum_{a'}c_{a'}(t_0)\ket{a'}\\
\ket{\alpha,t_0; t}&=\sum_{a'}c_{a'}(t)\ket{a'}
\end{align}$$
States who are normalized initially remain normalized under unitary transformations:
$$\begin{align}
\bra{\alpha,t_0; t_0}\ket{\alpha,t_0; t_0}&=1 &\implies&& \bra{\alpha,t_0; t}\ket{\alpha,t_0; t}&=1
\end{align}$$
For the time translation, it must then be unitary:
$$\begin{align}
U^\dagger(t;t_0)U(t;t_0)=\mathbb{I}
\end{align}$$
Such operators must also compose, and so:
$$\begin{align}
U(t_2;t_0)=U(t_2;t_1)U(t_1;t_0)
\end{align}$$
The infinitesimal generator of time translation is written as:
$$\begin{align}
\ket{\alpha,t_0; t_0+dt}&=U(t_0+dt;t_0)\ket{\alpha,t_0}
\end{align}$$
This unitary transform forms a Lie Group of time translation (symmetry).
The relation to the Lie Algebra is then:
$$\begin{align}
U(t_0+dt;t_0)&=e^{-i\omega\ dt}
\end{align}$$
In quantum mechanics, we know that temporal frequency is related to the energy (Hamiltonian):
$$\begin{align}
\hat{H}&=\hbar\hat\omega &\implies && U(t_0+dt;t_0)&=e^{-i\hat{H}dt/\hbar}
\end{align}$$
This means that, in quantum mechanics, Energy is the generator of time translation.
By Noether's Theorem, a time translation invariance leads to conservation of energy.
### 2.1.2 : The Schrödinger Equation
To find the calculus of dynamics of the wavefunction, we want to construct an infinitesimal change in the values of $U$ on a static wavefunction $\psi$.
$$\begin{align}
U(t+dt;t_0)&=U(t+dt;t)U(t;t_0)\\
&=e^{-i\hat{H}dt/\hbar}U(t;t_0)
\end{align}$$
For small values $dt\ll1$, we can linearize about the null (identity) transformation:
$$\begin{align}
U(t+dt;t_0)&=\left(1-i\dfrac{\hat{H}}{\hbar}dt +O(dt^2)\right)U(t;t_0)\\
U(t+dt;t_0)-U(t;t_0)&=-i\dfrac{\hat{H}}{\hbar}dt\ U(t;t_0)\\
\lim_{dt\rightarrow0}\dfrac{U(t+dt;t_0)-U(t;t_0)}{dt}&=\lim_{dt\rightarrow0}-i\dfrac{\hat{H}}{\hbar}\ U(t;t_0)\\
\dfrac{\partial}{\partial t}U(t;t_0)&=-i\dfrac{\hat{H}}{\hbar}\ U(t;t_0)\\
i\hbar\dfrac{\partial}{\partial t}U(t;t_0)&=\hat{H}U(t;t_0)\\
\end{align}$$
Since the initial state $\ket{\alpha,t_0}$ is constant (unchanging in time), then:
$$\begin{align}
i\hbar\dfrac{\partial}{\partial t}U(t;t_0)\ket{\alpha,t_0}&=\hat{H}U(t;t_0)\ket{\alpha,t_0} & \implies\\
\Aboxed{i\hbar\dfrac{\partial}{\partial t}\ket{\alpha,t_0;t}&=\hat{H}\ket{\alpha,t_0;t}}
\end{align}$$
Partially unrelated, to solve the accumulated operation on the initial state, we see:
$$\begin{align}
U(t;t_0)&=\exp\left(-\dfrac{i}{\hbar}\int_{t_0}^tH(t')\ dt\right)
\end{align}$$
This is just the concept of the "integration factor" for solving differential equations. There's a deep connection here and I'm glad I understand things conceptually, not memorized.

For the case where the Hamiltonian does not commute over time, we need the Dyson Series:
$$\begin{align}
U(t;t_0)&=\mathbb{I}+\sum_{n=1}^\infty\left(\dfrac{-i}{\hbar}\right)^n\int_{t_0}^t\int_{t_0}^{t_1}\cdots\int_{t_0}^{t_{n-1}}\hat{H}(t_1)\hat{H}(t_2)\cdots\hat{H}(t_n)\ dt_n\ dt_{n-1}\cdots \ dt_1
\end{align}$$
### 2.1.3 : Energy Eigenstates
To model the effect of the time-evolution operator on $\ket\psi$, we need to project onto a new basis.

If $[\hat{A},\hat{H}]=0$, the eigenbasis is the same as the energy eigenstate basis:
$$\begin{align}
\hat{H}\ket{a'}&=E_{a'}\ket{a'}
\end{align}$$
For non-commutative operators with the Hamiltonian, then:
$$\begin{align}
U(t;0)&=\sum_{a'}\sum_{a''}\ket{a''}\bra{a''}\exp\left(-\dfrac{i}{\hbar}\hat{H}t\right)\ket{a'}\bra{a'}\\
&=\sum_{a'}\ket{a'}\exp\left(-\dfrac{i}{\hbar}E_{a'}t\right)\bra{a'}\\
\end{align}$$
We can quite simply apply this to a general state $\ket{\psi}$ to change-of-basis into $a'$.

If we have a general initial state $\ket{\psi}$, then:
$$\begin{align}
U(t;0)\ket{\psi;0}&=\sum_{a'}\ket{a'}\exp\left(-\dfrac{i}{\hbar}E_{a'}t\right)\bra{a'}\cdot c_{a''}(0)\ket{a''}\\
&=\sum_{a'}\ket{a'}\exp\left(-\dfrac{i}{\hbar}E_{a'}t\right)c_{a'}(0)\\
\Aboxed{\ket{\psi;t}&=\sum_{a'}c_{a'}(0)\exp\left(-\dfrac{i}{\hbar}E_{a'}t\right)\ket{a'}}
\end{align}$$
### 2.1.4 : Time Dependence of Expected Values
To find expected value, we write the following:
$$\begin{align}
\braket{A}(t)&=\bra{\psi;t}\hat{A}\ket{\psi;t}\\
&=\bra{\psi;0}\cdot U^\dagger(t;0)\hat{A}U(t;0)\cdot\ket{\psi;0}\\
&=\sum_{a'}c_{a'}^*(0)\exp\left(\dfrac{i}{\hbar}E_{a'}t\right)\bra{a'}\hat{A}\sum_{a''}c_{a''}(0)\exp\left(-\dfrac{i}{\hbar}E_{a''}t\right)\ket{a''}\\
&=\sum_{a'}c_{a'}^*(0)c_{a''}(0)\exp\left(\dfrac{i}{\hbar}E_{a'}t\right)\sum_{a''}\exp\left(-\dfrac{i}{\hbar}E_{a''}t\right)\braket{a'|\hat{A}|a''}\\
&=\sum_{a'}c_{a'}^*(0)c_{a''}(0)\braket{a'|\hat{A}|a''}\exp\left(-i\dfrac{E_{a''}-E_{a'}}{\hbar}t\right)\\
\braket{A}(t)&=\sum_{a'}c_{a'}^*(0)c_{a''}(0)\braket{a'|\hat{A}|a''}e^{-i\omega_{a''a'}t}\\
\end{align}$$
When represented in an energy eigenbasis, we see that:
$$\begin{align}
\braket{A}(t)&=\bra{a'}\cdot U^\dagger(t;0)\hat{A}U(t;0)\cdot\ket{a'}\\
&=\bra{a'}\cdot\hat{A}U^\dagger(t;0)U(t;0)\cdot\ket{a'}\\
\Aboxed{\braket{A}&=\bra{a'}\hat{A}\ket{a'}}
\end{align}$$
### 2.1.5 : Spin Precession
For an external magnetic field and a spin-$1/2$ system the Hamiltonian is:
$$\begin{align}
\hat{H}&=-\left(\dfrac{e}{m_ec}\right)\vec{S}\cdot\vec{B}
\end{align}$$
For a uniform, static, $z$-pointing magnetic field, we can write it as:
$$\begin{align}
\hat{H}&=-\left(\dfrac{eB}{m_ec}\right)S_z
\end{align}$$
We see, for this system, that $[H,S_z]=0$, so they share an energy eigenstate basis with eigenvalues:
$$\begin{align}
E_\pm&=\mp\dfrac{e\hbar B}{2m_ec}
\end{align}$$
If we define $\omega=\tfrac{|e|B}{m_ec}$, we can also write the Hamiltonian as:
$$\begin{align}
\hat{H}&=\omega S_z
\end{align}$$
With the time-evolution operator being:
$$\begin{align}
U(t;0)&=\exp\left(-\dfrac{i}{\hbar}\hat{H}t\right)=\exp\left(-\dfrac{i}{\hbar}\omega S_zt\right)
\end{align}$$
We apply it to an initial state:
$$\begin{align}
\ket{\psi; 0}&=c_+(0)\ket{\chi_+^z}+c_-(0)\ket{\chi_-^z}\\
\ket{\psi; t}&=c_+(0)e^{\tfrac{i\omega t}{2}}\ket{\chi_+^z}+c_-(0)e^{+\tfrac{i\omega t}{2}}\ket{\chi_-^z}\\
\end{align}$$
### 2.1.6 : Neutrino Oscillations
Lets represent the real neutrinos as a linear combination of some eigenstate neutrino.
$$\begin{align}
\ket{\nu_e}&=\cos\theta\ \ket{\nu_1}-\sin\theta\ \ket{\nu_2}\\
\ket{\nu_\mu}&=\sin\theta\ \ket{\nu_1}+\cos\theta\ \ket{\nu_2}\\
\end{align}$$
This mixing angle $\theta$ is a degree of freedom (free parameter) in QFT.

Suppose we had a relativistic electron neutrino source (initial condition):
$$\begin{align}
E^2-(\vec{p}c)^2&=(mc^2)^2\implies E\approx pc\left(1+\dfrac{(mc)^2}{2p^2}\right)
\end{align}$$
We can then see that:
$$\begin{align}
p(\nu_e\rightarrow \nu_e)&=1-\sin^2(2\theta)\sin^2\left(\Delta m^2c^4\dfrac{L}{4E\hbar c}\right)\\
\end{align}$$
Where $\Delta m^2=m_1^2-m_2^2$, and $L=ct$ the flight distance, and $E=pc$ for massless.

### 2.1.7 : Correlation Amplitude and the Energy-Time Uncertainty Relation
Suppose we want to know the correlation between a wavefunction at $t=0$ and some time $t$, then:
$$\begin{align}
C(t)&=\braket{\psi;0|\psi;t}\\
&=\bra{\psi;0}U(t;0)\ket{\psi;0}\\
\end{align}$$
This is the correlation amplitude. For the sum of energy eigenstates, then:
$$\begin{align}
C(t)&=\sum_{a'}\bra{a';0}U(t;0)\ket{a';0}\\
&=\sum_{a'}\bra{a;0}e^{-iE_{a'}t/\hbar}\ket{a;0}\\
C(t)&=\sum_{a'}|c_{a'}(0)|^2e^{-iE_{a'}t/\hbar}
\end{align}$$
For a constant Hamiltonian system, the coefficients just change phase, but same amplitude.

For a quasi-continuous system of energy, we can parametrize in terms of energy instead as:
$$\begin{align}
C(t)&=\int_{E_{a'}\approx E}\rho(E)\ dE=\int\left|g(E)\right|^2\rho(E)e^{-iEt/\hbar}\ dE
\end{align}$$
Under the normalization condition:
$$\begin{align}
\int\left|g(E)\right|^2\rho(E)\ dE&=1
\end{align}$$
For large ensembles, we expect the energy clustered around $E_0$ with variance $\Delta E$:
$$\begin{align}
C(t)&=e^{-iE_0t/\hbar}\int\left|g(E)\right|^2\rho(E)e^{-i(E-E_0)t/\hbar}\ dE
\end{align}$$
This leads to the uncertainty principle:
$$\begin{align}
\Delta t\Delta E\approxeq\hbar
\end{align}$$
## 2.2 : The Schrödinger Versus the Heisenberg Picture
### 2.2.1 : Unitary Operators
These special operators conserve the inner product on the Hilbert Space:
$$\begin{align}
\ket{\psi'}&=U\ket{\psi} &\iff&& \bra{\phi'}&=\bra{\phi}U^\dagger
\end{align}$$
Therefore we see that:
$$\begin{align}
\braket{\phi'|\psi'}&=\bra{\phi}U^\dagger U\ket{\psi}=\braket{\phi|\psi}
\end{align}$$
For an arbitrary operator, we can see 2 different choices of associativity:
$$\begin{align}
&&\bra{\phi'}\hat{A}\ket{\psi'}&=\bra{\phi}U^\dagger \hat{A}U\ket{\psi}\\
\implies&&\bra{\phi'}\hat{A}\ket{\psi'}&=\left(\bra{\phi}U^\dagger\right) \hat{A}\left(U\ket{\psi}\right)\\
\implies&&\bra{\phi'}\hat{A}\ket{\psi'}&=\bra{\phi}\left(U^\dagger \hat{A}U\right)\ket{\psi}
\end{align}$$
So what we see is 2 different approaches to the system:
$$\begin{align}
\ket{\psi}&\rightarrow U\ket{\psi} & \text{(Schodinger Picture)}\\
\hat{A}(t)&\rightarrow U^\dagger \hat{A}U & \text{(Heisenberg Picture)}
\end{align}$$
### 2.2.3 : The Heisenberg Equation of Motion
Similar to Schrodinger's equation being the EOM of a wavefunction, we can write a similar EOM for the dynamical operators over time:
$$\begin{align}
\dfrac{\partial}{\partial t}\hat{A}(t)&=\dfrac{\partial}{\partial t}\left(U^\dagger \hat{A}U\right)\\
&=\dfrac{\partial U^\dagger}{\partial t}\hat{A}U+U^\dagger\dfrac{\partial \hat{A}(0)}{\partial t}U+U^\dagger \hat{A}\dfrac{\partial U}{\partial t}\\
\Aboxed{\dfrac{\partial\hat{A}}{\partial t}(t)&=\dfrac{1}{i\hbar}\left[\hat{A}(t),\hat{H}(t)\right]}
\end{align}$$
In classical mechanics, we find the Poisson Brackets have the form:
$$\begin{align}
\dfrac{\partial\hat{A}}{\partial t}(t)&=\left[\hat{A}(t),\hat{H}(t)\right]_\text{classical}
\end{align}$$
What's apparent is that classical mechanics can be derived from quantum mechanics,
however quantum mechanics cannot be derived from classical mechanics.
### 2.2.4 Free Particles: Ehrenfest's Theorem
For the sake of simplicity, we'll want the 2 following relations:
$$\begin{align}
\left[x_i,G(\vec{p})\right]&=+i\hbar\dfrac{\partial G}{\partial p_i}\\
\left[p_i,F(\vec{x})\right]&=-i\hbar\dfrac{\partial F}{\partial x_i}\\
\end{align}$$
For a free particle, we know the Hamiltonian:
$$\begin{align}
\hat{H}(t)&=\hat{H}=\dfrac{\vec{p}^2}{2m}
\end{align}$$
Under the Heisenberg EOM, we can see that:
$$\begin{align}
\dfrac{\partial\vec{p}}{\partial t}&=\dfrac{1}{i\hbar}\left[\vec{p}(t),\hat{H}(t)\right]\\
\dfrac{\partial\vec{x}}{\partial t}&=\dfrac{1}{i\hbar}\left[\hat{x}(t),\hat{H}(t)\right]
\end{align}$$
For a free particle in a momentum eigenstate, we can then see that:
$$\begin{align}
\dfrac{1}{i\hbar}\left[\vec{p},\hat{H}(t)\right]&=0 & \implies && \dfrac{\partial\vec{p}}{\partial t}&=0\\
\dfrac{1}{i\hbar}\left[\hat{x}(t),\hat{H}(t)\right]&=0 &\implies && \dfrac{\partial\vec{x}}{\partial t}&=\dfrac{\vec{p}}{m}
\end{align}$$
This is just basically Classical Mechanics, so expected values lead to classical observations.

If we add a spatial-dependent potential, then:
$$\begin{align}
\hat{H}&=\dfrac{\vec{p}^2}{2m}+V(\vec{x})
\end{align}$$
Similarly from the EOM:
$$\begin{align}
\dfrac{\partial\vec{p}}{\partial t}&=-\vec\nabla V(\vec{x})\\
\dfrac{\partial\vec{x}}{\partial t}&=\dfrac{\vec{p}}{m}
\end{align}$$
Differentiating the velocity again and rearranging, we see that:
$$\begin{align}
\Aboxed{m\dfrac{\partial^2\vec{x}}{\partial t^2}&=-\vec\nabla V(\vec{x})}
\end{align}$$
By taking the expected value of both sides, the state does not move with time, and so:
$$\begin{align}
\Aboxed{m\dfrac{\partial^2\braket{\vec{x}}}{\partial t^2}&=\dfrac{\partial\braket{\vec{p}}}{\partial t}=-\left\langle\vec\nabla V(\vec{x})\right\rangle}
\end{align}$$
This here is Ehrenfest's Theorem.




