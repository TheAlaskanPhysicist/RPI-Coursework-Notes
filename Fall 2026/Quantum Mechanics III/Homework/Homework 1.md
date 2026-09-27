**Author:** Stanley Goodwin
**Date:** September 10th, 2026

---
## Question 2.1
> Classical electromagnetism (with no sources) follows from the action$$\begin{align}
S&=\int d^4 x\left(-\frac{1}{4}F_{\mu\nu}F^{\mu\nu}\right),
&\text{where}\ \ F_{\mu\nu}&=\partial_\mu A_\nu-\partial_\nu A_\mu
\end{align}$$

---
### Question 2.1.A
> Derive Maxwell's equations as the Euler-Lagrange equations of this action, treating the components $A_\mu(x)$ as the dynamical variables. Write the equations in standard form by identifying $E^i=-F^{0i}$ and $\epsilon^{ijk}B^k=-F^{ij}$.

From the action integral above, we can note that the Lagrangian density is...
$$\begin{align}
\mathcal{L}&=-\frac{1}{4}F_{\mu\nu}F^{\mu\nu}=-\dfrac{1}{4}\left(\partial_\mu A_\nu\partial^\mu A^\nu-\partial_\nu A_\mu\partial^\mu A^\nu-\partial_\mu A_\nu\partial^\nu A^\mu+\partial_\nu A_\mu\partial^\nu A^\mu\right)
\end{align}$$
The Euler-Lagrange equations with $A_\mu(x)$ as the dynamical variables is
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial A_\mu}-\partial_\nu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\nu A_\mu)}\right)&=0
\end{align}$$
Since the Lagrangian density is only dependent on derivatives of the 4-potential, the derivative with respect to that 4-potential is always zero
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial A_\mu}&=0 &\implies&& \partial_\nu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\nu A_\mu)}\right)&=0
\end{align}$$


<div style="page-break-before: always;"></div>*PDF next page*

If we now substitute our definition for the Lagrangian density into this equation of motion, and realizing that the chain-ruled components are equal by the construction of $F_{\mu\nu}$, we get that
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial(\partial_\nu A_\mu)}
&=-\frac{1}{4}\dfrac{\partial F_{\alpha\beta}}{\partial(\partial_\nu A_\mu)}F^{\alpha\beta}-\frac{1}{4}F_{\alpha\beta}\dfrac{\partial F^{\alpha\beta}}{\partial(\partial_\nu A_\mu)}\\
&=-\frac{1}{2}\dfrac{\partial F_{\alpha\beta}}{\partial(\partial_\nu A_\mu)}F^{\alpha\beta}\\
&=-\frac{1}{2}\dfrac{\partial\left(\partial_\alpha A_\beta-\partial_\beta A_\alpha\right)}{\partial(\partial_\nu A_\mu)}F^{\alpha\beta}\\
&=-\frac{1}{2}\left(\delta_\alpha^\nu\delta_\beta^\mu-\delta_\beta^\nu\delta_\alpha^\mu\right)F^{\alpha\beta}\\
&=-\frac{1}{2}\left(F^{\nu\mu}-F^{\mu\nu}\right)\\
\dfrac{\partial\mathcal{L}}{\partial(\partial_\nu A_\mu)}&=+F^{\mu\nu}=-F^{\nu\mu}
\end{align}$$
Substituting this back into the equation of motion, we then get that
$$\begin{align}
\Aboxed{\partial_\nu F^{\mu\nu}&=0}
\end{align}$$
If we use our expressions for electric and magnetic field to start, this equation satisfies
$$\begin{align}
\Aboxed{\partial_i F^{0i}&=0\implies\vec\nabla\cdot\vec{E}=0} &
\Aboxed{\partial_j F^{ij}&=0\implies \epsilon^{ijk}\partial_j B^k=\vec\nabla\times\vec{B}=0} \\
\Aboxed{\partial_0 F^{i0}&=0\implies\dfrac{\partial}{\partial t}\vec{E}=0}
\end{align}$$
The last equation is no magnetic monopoles, which is trivial.

---
### Question 2.1.B
> Construct the energy-momentum tensor for this theory. Note that the usual procedure does not result in a symmetric tensor. To remedy that, we can add to $T^{\mu\nu}$ a term of the form $\partial_\lambda K^{\lambda\mu\nu}$, where $K^{\lambda\mu\nu}$ is antisymmetric in its first two indices. Such an object is automatically divergenceless, so$$\begin{align}
\widehat{T}^{\mu\nu}&=T^{\mu\nu}+\partial_\lambda K^{\lambda\mu\nu}
\end{align}$$is an equally good energy-momentum tensor with the same globally conserved energy and momentum. Show that this construction, with$$\begin{align}
K^{\lambda\mu\nu}&=F^{\mu\lambda}A^\nu
\end{align}$$leads to an energy-momentum tensor $\widehat{T}$ that is symmetric and yields the standard formulae for the electromagnetic energy and momentum densities:$$\begin{align}
\mathcal{E}&=\frac{1}{2}\left(\vec{E}^2+\vec{B}^2\right); & \vec{S}&=\vec{E}\times\vec{B}
\end{align}$$

Start with the general canonical energy-momentum tensor expression from Noether
$$\begin{align}
T^{\mu\nu}&=\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu A_\alpha)}\partial^\nu A_\alpha-g^{\mu\nu}\mathcal{L}
\end{align}$$
From [[#Question 2.1.A|part a]], we can write the derivative term of the Lagrangian density as
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial(\partial_\nu A_\mu)}&=-F^{\nu\mu} &\implies&&
T^{\mu\nu}&=-F^{\mu\alpha}\partial^\nu A_\alpha+\frac{1}{4}g^{\mu\nu}F_{\beta\gamma}F^{\beta\gamma}
\end{align}$$
From the special tensor from before, we can take its derivative as
$$\begin{align}
\partial_\lambda K^{\lambda\mu\nu}&=\partial_\lambda\left(F^{\mu\lambda}A^\nu\right)=\left(\partial_\lambda F^{\mu\lambda}\right)A^\nu+F^{\mu\lambda}\left(\partial_\lambda A^\nu\right)
\end{align}$$
The first term becomes $0$ for our system as per [[#Question 2.1.A|part a]], and so
$$\begin{align}
\partial_\lambda K^{\lambda\mu\nu}&=F^{\mu\lambda}\partial_\lambda A^\nu
\end{align}$$
If we add this expression to both sides of the energy-momentum tensor, we get
$$\begin{align}
\widehat{T}^{\mu\nu}&=F^{\mu\lambda}\partial_\lambda A^\nu-F^{\mu\alpha}\partial^\nu A_\alpha+\frac{1}{4}g^{\mu\nu}F_{\beta\gamma}F^{\beta\gamma}
\end{align}$$
Using the metric tensor, we can adjust the first two terms to
$$\begin{align}
\widehat{T}^{\mu\nu}&=g^{\nu\alpha}F^{\mu\lambda}\partial_\lambda A_\alpha-g^{\nu\lambda}F^{\mu\alpha}\partial_\lambda A_\alpha+\frac{1}{4}g^{\mu\nu}F_{\beta\gamma}F^{\beta\gamma}\\
&=g^{\nu\lambda}F^{\mu\alpha}\left(\partial_\alpha A_\lambda-\partial_\lambda A_\alpha\right)+\frac{1}{4}g^{\mu\nu}F_{\beta\gamma}F^{\beta\gamma}\\
\Aboxed{\widehat{T}^{\mu\nu}&=g^{\nu\lambda}F^{\mu\alpha}F_{\alpha\lambda}+\frac{1}{4}g^{\mu\nu}F_{\beta\gamma}F^{\beta\gamma}}
\end{align}$$
---
## Question 2.2
> Consider the field theory of a complex-valued scalar field obeying the Klein-Gordon equation. The action of this theory is$$\begin{align}
S&=\int d^4 x\left(\partial_\mu\phi^*\partial^\mu\phi-m^2\phi^*\phi\right)
\end{align}$$It is easiest to analyze this theory by considering $\phi(x)$ and $\phi^*(x)$, rather than the real and imaginary parts of $\phi(x)$, as the basic dynamical variables.


<div style="page-break-before: always;"></div>*PDF next page*

### Question 2.2.A
> Find the conjugate momenta to $\phi(x)$ and $\phi^*(x)$ and the canonical commutation relations. Show that the Hamiltonian is$$\begin{align}
H&=\int d^3x\left(\pi^*\pi+\nabla\phi^*\cdot\nabla\phi+m^2\phi^*\phi\right)
\end{align}$$Compute the Heisenberg equation of motion for $\phi(x)$ and show that it is indeed the Klein-Gordon equation.

The Lagrangian density of this system is
$$\begin{align}
\mathcal{L}&=\partial_\mu\phi^*\partial^\mu\phi-m^2\phi^*\phi
\end{align}$$
The conjugate momenta is then just the partial with respect to the field components
$$\begin{align}
\Aboxed{\pi(x)&=\dfrac{\partial\mathcal{L}}{\partial(\partial_0\phi)}=\dot\phi^*}
&&&
\Aboxed{\pi^*(x)&=\dfrac{\partial\mathcal{L}}{\partial(\partial_0\phi^*)}=\dot\phi}
\end{align}$$
The canonical commutation relations for infinite resolution uses the Dirac delta function such that
$$\begin{align}
[q(t,\vec{x}),p(t,\vec{x}')]=i\delta^3(\vec{x}-\vec{x}')
\end{align}$$
In our case, $q(t,\vec{x})=\phi(t,\vec{x})$ and $p(t,\vec{x})=\pi(t,\vec{x})$, so for the two canonical pairs we have that
$$\begin{align}
\Aboxed{[\phi(t,\vec{x}),\pi(t,\vec{x}')]=i\delta^3(\vec{x}-\vec{x}')} &
\Aboxed{[\phi^*(t,\vec{x}),\pi^*(t,\vec{x}')]=i\delta^3(\vec{x}-\vec{x}')}
\end{align}$$
All other commutators are $0$ since they are effectively independent coordinate axes.

To find the Hamiltonian density, we use the Legendre transformation
$$\begin{align}
\mathcal{H}&=\pi\dot\phi+\pi^*\dot\phi^*-\mathcal{L}
\end{align}$$
Substituting the field for the first expression and the momentum for the second, this simplifies to
$$\begin{align}
\mathcal{H}&=\dot\phi^*\dot\phi+\pi^*\pi-\left(\dot\phi^*\dot\phi-\vec{\nabla}\phi^*\cdot\vec{\nabla}\phi-m^2\phi^*\phi\right)\\
&=\cancel{\dot\phi^*\dot\phi}+\pi^*\pi-\cancel{\dot\phi^*\dot\phi}+\vec{\nabla}\phi^*\cdot\vec{\nabla}\phi+m^2\phi^*\phi\\
\mathcal{H}&=\pi^*\pi+\vec{\nabla}\phi^*\cdot\vec{\nabla}\phi+m^2\phi^*\phi
\end{align}$$
Now we integrate this Hamiltonian density over space to get the total Hamiltonian
$$\begin{align}
\Aboxed{H&=\int d^3x\left(\pi^*\pi+\nabla\phi^*\cdot\nabla\phi+m^2\phi^*\phi\right)}
\end{align}$$
Lastly, the Heisenberg equation of motion comes from the commutator of the Hamiltonian and the canonical variables. None of these quantities depend on time, so this simplifies to
$$\begin{align}
\dfrac{d\mathcal{O}}{dt}&=\dfrac{\partial\mathcal{O}}{\partial t}+\frac{i}{\hbar}\left[H,\mathcal{O}\right]
&\implies&&
\dfrac{d\mathcal{O}}{dt}&=\frac{i}{\hbar}\left[H,\mathcal{O}\right]
\end{align}$$
For $(\phi,\pi)$ and $(\phi^*,\pi^*)$, using also $\hbar=1$, we have that
$$\begin{align}
\dfrac{d\phi}{dt}&=i\left[H,\phi\right]
&\implies&&
\dot\phi&=i\left[H,\phi\right]\\
\dfrac{d\phi^*}{dt}&=i\left[H,\phi^*\right]
&\implies&&
\dot\phi^*&=i\left[H,\phi^*\right]\\
\dfrac{d\pi}{dt}&=i\left[H,\pi\right]
&\implies&&
\ddot\phi^*&=\left(\vec\nabla^2\phi^*-m^2\phi^*\right)\\
\dfrac{d\pi^*}{dt}&=i\left[H,\pi^*\right]
&\implies&&
\ddot\phi&=\left(\vec\nabla^2\phi-m^2\phi\right)
\end{align}$$
Taking the 4th equation, we have to satisfy
$$\begin{align}
\ddot\phi-\vec\nabla^2\phi+m^2\phi&=0 &\implies&&
\Aboxed{\left(\partial_\mu\phi\cdot\partial_\mu\phi+m^2\right)\phi&=0}
\end{align}$$
---
### Question 2.2.B
> Diagonalize $H$ by introducing creation and annihilation operators. Show that the theory contains two sets of particles of mass $m$.

Start with the Klein-Gordon equation where
$$\begin{align}
\left(\partial_\mu\phi\ \partial^\mu\phi+m^2\right)\phi&=0
\end{align}$$
Since this is a linear differential equation, we can decompose the field into a Fourier space
$$\begin{align}
\phi(t,x)&=\int d^3p\ e^{i\vec{p}\cdot\vec{x}}c_\vec{p}(t)
\end{align}$$
Substituting into the Klein-Gordon equation again, we get the condition
$$\begin{align}
\ddot{c}_\vec{p}(t)+(\vec{p}^2+m^2)c_\vec{p}(t)&=0
\end{align}$$
The solution to this coefficient is harmonic in $\omega_\vec{p}^2=\vec{p}^2+m^2$, and so our field can be written as
$$\begin{align}
\phi(t,x)&=\int\left(a_\vec{p}e^{-i\omega_\vec{p}t+i\vec{p}\cdot\vec{x}}+b_\vec{p}^\dagger e^{+i\omega_\vec{p}t+i\vec{p}\cdot\vec{x}}\right)\ d^3p
\end{align}$$
The momentum state is the time derivative of the complex conjugate of this field, and so
$$\begin{align}
\pi(t,x)&=i\int \omega_\vec{p}\left(a_\vec{p}^\dagger e^{+i\omega_\vec{p}t-i\vec{p}\cdot\vec{x}}-b_\vec{p} e^{-i\omega_\vec{p}t-i\vec{p}\cdot\vec{x}}\right)\ d^3p
\end{align}$$
We can then find the commutator between these two functions, and simplify since we can swap the dummy variables for $\vec{p}$ and $\vec{p}'$
$$\begin{align}
\left[a_\vec{p},a_\vec{p'}^\dagger\right]e^{+i(\vec{p}-\vec{p}')\cdot\vec{x}}+\left[a_\vec{p}^\dagger, b_\vec{p'}^\dagger\right]e^{+2i\omega_\vec{p}t-i(\vec{p}-\vec{p}')\cdot\vec{x}}-\left[a_\vec{p},b_\vec{p'}\right]e^{-2i\omega_\vec{p}t+i(\vec{p}-\vec{p}')\cdot\vec{x}}-\left[b_\vec{p},b_\vec{p'}^\dagger\right] e^{-i(\vec{p}-\vec{p}')\cdot\vec{x}}
\end{align}$$
The correct commutator is $[\phi(t,\vec{x}),\pi(t,\vec{x}')]=i\delta^3(\vec{x}-\vec{x}')$, so there can be no time dependence. This then requires that the cross commutators must be zero, and that the other two commutators are delta functions in the momenta, and so we get
$$\begin{align}
\left[a_\vec{p}^\dagger, b_{\vec{p}'}^\dagger\right]=\left[a_\vec{p},b_{\vec{p}'}\right]&=0  &&&\left[a_\vec{p},a_{\vec{p}'}^\dagger\right]=\left[b_\vec{p},b_{\vec{p}'}^\dagger\right] &=\delta^3(\vec{p}-\vec{p}')
\end{align}$$
Using these new commutators and the integral expression for $\phi$, the Hamiltonian becomes
$$\begin{align}
\Aboxed{H&=H_0+\int d^3p \ \sqrt{p^2+m^2}\left(a_\vec{p}^\dagger a_\vec{p}+b_\vec{p}^\dagger b_\vec{p}\right)}
\end{align}$$
where $H_0$ is some energy offset for zero-point energy, but removed because I don't want to explicitly calculate it.

---
### Question 2.2.C
> Rewrite the conserved charge$$\begin{align}
Q&=\int d^3x\ \frac{i}{2}\left(\phi^*\pi^*-\pi\phi\right)
\end{align}$$in terms of creation and annihilation operators, and evaluate the charge of the particles of each type.

After a lot of arithmetic like [[#Question 2.2.B|part b]], you get that
$$\begin{align}
\Aboxed{Q&=Q_0+\int d^3p \left(a_\vec{p}^\dagger a_\vec{p}-b_\vec{p}^\dagger b_\vec{p}\right)}
\end{align}$$
These creation-annihilation pairs looks like the number operator, and so we can write it as
$$\begin{align}
N_a&=\int d^3p\ a_\vec{p}^\dagger a_\vec{p}, & N_b&=\int d^3p\ b_\vec{p}^\dagger b_\vec{p} &\implies&& Q&=N_a-N_b
\end{align}$$
For the single-particle states, we have
$$\begin{align}
Q\ket{a,\vec{p}}&=\int d^3p \left(a_\vec{p}^\dagger a_\vec{p}-b_\vec{p}^\dagger b_\vec{p}\right)\ket{a,\vec{p}}=\left(1-0\right)\ket{a,\vec{p}}=+1\ket{a,\vec{p}}
&\implies&& \Aboxed{Q\ket{a,\vec{p}}&=+1\ket{a,\vec{p}}}\\
Q\ket{b,\vec{p}}&=\int d^3p \left(a_\vec{p}^\dagger a_\vec{p}-b_\vec{p}^\dagger b_\vec{p}\right)\ket{b,\vec{p}}=\left(0-1\right)\ket{b,\vec{p}}=-1\ket{b,\vec{p}} &\implies&& \Aboxed{Q\ket{b,\vec{p}}&=-1\ket{b,\vec{p}}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 2.2.D
> Consider the case of two complex Klein-Gordon fields with the same mass. Label the fields $\phi_a(x)$, where $a=1,2$. Show that there are now four conserved charges, one given by the generalization of [[#Question 2.2.C|part c]], and the other three given by $$\begin{align}
Q^i&=\int d^3x\ \frac{i}{2}\left(\phi_a^*(\sigma^i)_{ab}\pi_b^*-\pi_a(\sigma^i)_{ab}\phi_b\right)
\end{align}$$where $\sigma^i$ are the Pauli sigma matrices. Show that these three charges have the commutation relations of angular momentum $\mathrm{SU}(2)$. Generalize these results to the case of $n$ identical complex scalar fields.

Suppose we have $n$ complex scalar fields of identical mass, then the Lagrangian density is
$$\begin{align}
\mathcal{L}&=\sum_{a=1}^n\partial_\mu\phi_a^*\partial^\mu\phi_a-m^2\phi_a^*\phi_a
\end{align}$$
We can arrange the fields into a vector $\phi$, and we impose a unitary transformation $U$. The physics of the system must remain unchanged by this transformation, and so we have
$$\begin{align}
\mathcal{L}'&=\partial_\mu\left(\phi^\dagger U^\dagger\right)\partial^\mu\left(U\phi\right)-m^2\left(\phi^\dagger U^\dagger\right)\left(U\phi\right)\\
&=\left(\partial_\mu\phi^\dagger U^\dagger+\phi^\dagger \partial_\mu U^\dagger\right)\left(\partial^\mu U\phi+U\partial^\mu\phi\right)-m^2 \phi^\dagger\left(U^\dagger U\right)\phi\\
&=\partial_\mu\phi^\dagger (U^\dagger U)\partial^\mu\phi+\phi^\dagger \partial_\mu U^\dagger\partial^\mu U\phi+\partial_\mu\phi^\dagger U^\dagger\partial^\mu U\phi+\phi^\dagger \partial_\mu U^\dagger U\partial^\mu\phi-m^2 \phi^\dagger\phi\\
\mathcal{L}'-\mathcal{L}&=\phi^\dagger \partial_\mu U^\dagger\partial^\mu U\phi+\partial_\mu\phi^\dagger U^\dagger\partial^\mu U\phi+\phi^\dagger \partial_\mu U^\dagger U\partial^\mu\phi\\
0&=\phi^\dagger(\partial_\mu U^\dagger)(\partial^\mu U)\phi+(\partial_\mu\phi^\dagger) U^\dagger(\partial^\mu U\phi)+\phi^\dagger(\partial_\mu U^\dagger)U(\partial^\mu\phi)
\end{align}$$
To simplify further, we can use that for $U=\mathrm{SU}(n)$ the operation can be represented as an exponential of a linear combination of generators of $\mathrm{su}(n)$. Mathematically,
$$\begin{align}
U(x)&=e^{i\alpha^A(x)T^A}\simeq I+i\alpha^AT^A
\end{align}$$
The differentials associated with this operation around the linearization are
$$\begin{align}
\partial_\mu U&=iT^A\partial_\mu\alpha^A & \partial_\mu U^\dagger&=-iT^A\partial_\mu\alpha^A
\end{align}$$
Substituting back into our Lagrangian density, we have that
$$\begin{align}
0&=\phi^\dagger(T^A\partial_\mu\alpha^A)(T^B\partial_\mu\alpha^B)\phi+i(\partial_\mu\phi^\dagger) (T^A\partial_\mu\alpha^A)\phi-iT^A\phi^\dagger(\partial_\mu\alpha^A)(\partial^\mu\phi)
\end{align}$$
We can ignore the 2nd order differential component for linearization, and so becomes
$$\begin{align}
0&=i(\partial_\mu\phi^\dagger)T^A\phi\ \partial_\mu\alpha^A-i\phi^\dagger T^A(\partial^\mu\phi)\ \partial_\mu\alpha^A
\end{align}$$
Adjusting the indices, we eventually arrive to
$$\begin{align}
0&=i[\phi^\dagger T^A(\partial^\mu\phi)-(\partial^\mu\phi^\dagger)T^A\phi]\partial_\mu\alpha^A
\end{align}$$
The part out the front is the Noether current, with the conservation law
$$\begin{align}
j^{\mu A}&=i[\phi^\dagger T^A(\partial^\mu\phi)-(\partial^\mu\phi^\dagger)T^A\phi] &&& \partial_\mu j^{\mu A}&=0
\end{align}$$
The corresponding conserved charge is then just the integration
$$\begin{align}
Q^A&=\int dx^3\ j^{0A}\\
&=\int dx^3\ i[\phi^\dagger T^A\dot\phi-\dot\phi^\dagger T^A\phi]\\
Q^A&=\int dx^3\ i[\phi^\dagger T^A\pi^*-\pi\  T^A\phi]
\end{align}$$
Since every element of $\mathrm{su}(n)$ can be represented by $n\times n$ matrices with $n^2-1$ generators, we will have $n^2-1$ conserved charges other than the default identity charge ($n^2$ total). We can then write the charges in terms of the index of the element in $\mathrm{su}(n)$ as
$$\begin{align}
Q^i&=\int dx^3\ i[\phi_a^*(T^i)_{ab}\pi_b^*-\pi_a(T^i)_{ab}\phi_b]\text{ or}\\
\Aboxed{Q^i&=2\int dx^3\ \mathrm{Im}\left(\pi_a(T^i)_{ab}\phi_b\right),\ n\in[1,2,\dots,n^2-1]}
\end{align}$$
where $a,b$ are implicitly summed over to get all the contributions. The trivial charge is the one with the identity operator instead of the Lie algebra elements, and thus we can let that be the $0$ element
$$\begin{align}
Q^0&=\int dx^3\ i[\phi_a^*\pi_a^*-\pi_a\phi_a]
&\text{or}&&
\Aboxed{Q^0&=2\int dx^3\ \mathrm{Im}\left(\pi_a\phi_a\right)}
\end{align}$$
For the $n=2$ case, corresponding to $U=\mathrm{SU}(2)$ and $T^A=\sigma^i\in\mathrm{su}(2)$, means that we have the Pauli Matrices for $T^A$ and corresponding charges to each. Therefore, we have that
$$\begin{align}
\Aboxed{Q^i&=\int dx^3\ i[\phi_a^*(\sigma^i)_{ab}\pi_b^*-\pi_a(\sigma^i)_{ab}\phi_b]}\\
\Aboxed{Q^0&=\int dx^3\ i[\phi_a^*\pi_a^*-\pi_a\phi_a]}
\end{align}$$
exactly as the question was expecting.

<div style="page-break-before: always;"></div>*PDF next page*

## Problem 1.3
Here we will consider scattering by arguments very similar to what we find in Peskin and Schroeder Chapter 1, except that the particles in the in state and out state have $J=3/2$ (each) and the mediator has $J=2$. This could be a hadronic process involving the baryon decuplet in the initial and final states with a higher spin boson at resonance in the intermediate state. Alternatively, this could be gravitino scattering in supergravity. That is because the gravitinos have spin $3/2$ and the graviton has spin $2$. In Chapter 1, we saw that each piece of the amplitude $\left<e^-e^+\middle|\gamma\right>^\mu$ corresponded to a polarization vector for the photon. Similarly here we will have two factors in the amplitude that are of the form $\left<\psi\psi\middle|g\right>^{\mu\nu}$ which has a tensor form corresponding to the spin two particle polarization tensor $\epsilon^{\mu\nu}$. We learn from textbook discussions of gravity waves that the two transverse tensors are (we will ignore the longitudinal tensors for a massive hadron with spin $2$):
$$\begin{align}
\epsilon_{(+)}^{\mu\nu}&=\left[\begin{array}{}0&0&0&0\\0&1&0&0\\0&0&-1&0\\0&0&0&0\end{array}\right] &&&
\epsilon_{(\times)}^{\mu\nu}&=\left[\begin{array}{}0&0&0&0\\0&0&1&0\\0&1&0&0\\0&0&0&0\end{array}\right]
\end{align}$$
if the motion is in the $\pm z$ direction. We will assume that this is the case for the incoming
particles. For the outgoing particles we will have rotate by an angle $\theta$ in the $xz$ plane, as in Chapter 1. This then involves the rotation matrix
$$\begin{align}
R^{\mu\nu}&=\left[\begin{array}{}1&0&0&0\\0&\cos\theta&0&\sin\theta\\0&0&1&0\\0&-\sin\theta&0&\cos\theta\end{array}\right]
\end{align}$$
To rotate the polarization tensors you just do matrix multiplication:
$$\begin{align}
\epsilon(\mathrm{out})&=R\cdot\epsilon(\mathrm{in})\cdot R^T
\end{align}$$
where $\epsilon(\mathrm{in})$ corresponds to either of the polarization tensors above.

The matrix elements are then proportional to
$$\begin{align}
_\mathrm{out}\left<(\alpha)\middle|(\beta)\right>_\mathrm{in}\propto
\epsilon_{(\alpha)}^{\mu\nu}(\mathrm{out})\epsilon_{\mu\nu(\beta)}(\mathrm{in})&=
\operatorname{tr}\left(\epsilon_{(\alpha)}(\mathrm{out})\epsilon_{(\beta)}(\mathrm{in})\right)
\end{align}$$
where $\alpha$ and $\beta$ take the two possibilities $+$ and $\times$.

Thus find the angular dependence of the differential cross section
$$\begin{align}
\dfrac{\partial\sigma}{\partial\Omega}\propto\sum_{\alpha,\beta\in\left\{+,\times\right\}}\left|_\mathrm{out}\left<(\alpha)\middle|(\beta)\right>_\mathrm{in}\right|^2
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

The rotation of the polarization tensors are
$$\begin{align}
\epsilon_{(+),\text{ out}}^{\mu\nu}&=\left[\begin{array}{}1&0&0&0\\0&\cos\theta&0&\sin\theta\\0&0&1&0\\0&-\sin\theta&0&\cos\theta\end{array}\right]\left[\begin{array}{}0&0&0&0\\0&1&0&0\\0&0&-1&0\\0&0&0&0\end{array}\right]\left[\begin{array}{}1&0&0&0\\0&\cos\theta&0&-\sin\theta\\0&0&1&0\\0&\sin\theta&0&\cos\theta\end{array}\right]\\
\epsilon_{(\times),\text{ out}}^{\mu\nu}&=\left[\begin{array}{}1&0&0&0\\0&\cos\theta&0&\sin\theta\\0&0&1&0\\0&-\sin\theta&0&\cos\theta\end{array}\right]\left[\begin{array}{}0&0&0&0\\0&0&1&0\\0&1&0&0\\0&0&0&0\end{array}\right]\left[\begin{array}{}1&0&0&0\\0&\cos\theta&0&-\sin\theta\\0&0&1&0\\0&\sin\theta&0&\cos\theta\end{array}\right]
\end{align}$$
After simplifying, we get that
$$\begin{align}
\epsilon_{(+),\text{ out}}^{\mu\nu}&=\left[\begin{array}{}0&0&0&0\\0&\cos^2\theta&0&-\sin\theta\cos\theta\\0&0&-1&0\\0&-\sin\theta\cos\theta&0&\sin^2\theta\end{array}\right]\\
\epsilon_{(\times),\text{ out}}^{\mu\nu}&=\left[\begin{array}{}0&0&0&0\\0&0&\cos\theta&0\\0&\cos\theta&0&-\sin\theta\\0&0&-\sin\theta&0\end{array}\right]
\end{align}$$
There are 4 polarization amplitudes, which are
$$\begin{align}
\mathcal{M}_{++}&\propto1+\cos^2\theta & \mathcal{M}_{\times\times}&\propto2\cos\theta & \mathcal{M}_{+\times}=\mathcal{M}_{\times+}&=0  
\end{align}$$
The differential cross section is then just the sum of all these transition amplitudes squared
$$\begin{align}
\dfrac{\partial\sigma}{\partial\Omega}
&\propto\sum_{\alpha,\beta\in\left\{+,\times\right\}}\left|_\mathrm{out}\left<(\alpha)\middle|(\beta)\right>_\mathrm{in}\right|^2\\
&\propto\left(1+\cos^2\theta\right)^2+\left(2\cos\theta\right)^2+0^2+0^2\\
\Aboxed{\dfrac{\partial\sigma}{\partial\Omega}&\propto1+6\cos^2\theta+\cos^4\theta}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

## Problem 1.4
> Here we have a theory with Lagrangian $$\begin{align}
\mathcal{L}&=\dfrac{1}{2g^2}\partial_\mu\phi\cdot\partial^\mu\phi
\end{align}$$where $\phi$ is a real scalar field with $N$ components. However, it is subject to the constraint$$\begin{align}
\phi\cdot\phi&=1
\end{align}$$This is known at the nonlinear $\sigma$ model. We will shortly see how it gets that name.

---
### Problem 1.4.A
> Without loss of generality, we can satisfy the constraint by taking$$\begin{align}
\phi^N&=\sigma=\sqrt{1-\pi\cdot\pi}\\
\left(\phi^1,\phi^2,\dots,\phi^{N-1}\right)&=\left(\pi^1,\pi^2,\dots,\pi^{N-1}\right)
\end{align}$$That is, $\pi$ is an $N-1$ component, unconstrained real field. On the other hand, the $\sigma$ field is a nonlinear function of $\pi$. Using this information, rewrite the Lagrangian in terms of the pions $\pi$. Do not forget to express the term $\partial_\mu\sigma\ \partial^\mu\sigma$ in terms of the pions!

Start with the Lagrangian density
$$\begin{align}
\mathcal{L}&=\dfrac{1}{2g^2}\partial_\mu\phi\cdot\partial^\mu\phi\\
&=\dfrac{1}{2g^2}\partial_\mu\phi_N\cdot\partial^\mu\phi_N+\sum_{a=1}^{N-1}\dfrac{1}{2g^2}\partial_\mu\phi_a\cdot\partial^\mu\phi_a\\
&=\dfrac{1}{2g^2}(\partial_\mu\sqrt{1-\pi\cdot\pi})\cdot(\partial^\mu\sqrt{1-\pi\cdot\pi})+\sum_{a=1}^{N-1}\dfrac{1}{2g^2}\partial_\mu\pi_a\cdot\partial^\mu\pi_a\\
&=\dfrac{1}{2g^2}\frac{1}{2\sqrt{1-\pi\cdot\pi}}\partial_\mu\left(1-\pi\cdot\pi\right)\cdot\frac{1}{2\sqrt{1-\pi\cdot\pi}}\partial^\mu\left(1-\pi\cdot\pi\right)+\sum_{a=1}^{N-1}\dfrac{1}{2g^2}\partial_\mu\pi_a\cdot\partial^\mu\pi_a\\
&=\dfrac{1}{8(1-\pi\cdot\pi)g^2}2\pi(\partial_\mu\pi)\cdot2\pi(\partial^\mu\pi)+\sum_{a=1}^{N-1}\dfrac{1}{2g^2}\partial_\mu\pi_a\cdot\partial^\mu\pi_a\\
\Aboxed{\mathcal{L}&=\dfrac{1}{2g^2}\left[\partial_\mu\pi\cdot\partial^\mu\pi+\dfrac{(\pi\cdot\partial_\mu\pi)(\pi\cdot\partial^\mu\pi)}{(1-\pi\cdot\pi)}\right]}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Problem 1.4.B
> Find the Euler-Lagrange equations of motion for the pions.

For $\left(\pi^1,\pi^2,\dots,\pi^{N-1}\right)$, the Euler-Lagrange equations are
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial \pi^i}-\partial_\nu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\nu \pi^i)}\right)&=0
\end{align}$$
We can calculate the first derivative from the $\sigma$ contribution term as
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial \pi^i}&=\dfrac{1}{2g^2}\left[\dfrac{2(\pi\cdot\partial_\mu\pi)\ \partial^\mu\pi^i}{1-\pi\cdot\pi}+\dfrac{2\pi^i(\pi\cdot\partial_\mu\pi)^2}{(1-\pi\cdot\pi)^2}\right]
\end{align}$$
The other derivative piece then is as follows
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial(\partial_\nu \pi^i)}&=\dfrac{1}{2g^2}\left[2\delta^\nu_\mu\partial^\mu\pi^i+\dfrac{2\pi^i(\pi\cdot\delta^\nu_\mu\partial^\mu\pi)}{(1-\pi\cdot\pi)}\right]\\
\partial_\nu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\nu \pi^i)}\right)&=\dfrac{1}{g^2}\partial_\nu\left[\partial^\nu\pi^i+\dfrac{\pi^i(\pi\cdot\partial^\nu\pi)}{(1-\pi\cdot\pi)}\right]
\end{align}$$
Substituting and simplifying, the equation of motion for this system is
$$\begin{align}
\Aboxed{\dfrac{(\pi\cdot\partial_\mu\pi)\ \partial^\mu\pi^i}{1-\pi\cdot\pi}+\dfrac{\pi^i(\pi\cdot\partial_\mu\pi)^2}{(1-\pi\cdot\pi)^2}-\partial_\nu\left[\partial^\nu\pi^i+\dfrac{\pi^i(\pi\cdot\partial^\nu\pi)}{(1-\pi\cdot\pi)}\right]&=0}
\end{align}$$
---
### Problem 1.4.C
> Find the energy-momentum tensor for the pions.

Start with the general canonical energy-momentum tensor expression from Noether
$$\begin{align}
T^{\mu\nu}&=\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi^i)}\partial^\nu \pi^i-g^{\mu\nu}\mathcal{L}
\end{align}$$
The derivative expression can be found from [[#Problem 1.4.B|part b]], and combined with the Lagrangian density gives the expression for energy-momentum as
$$\begin{align}
\Aboxed{T^{\mu\nu}&=\dfrac{1}{g^2}\left[\partial^\mu\pi^i+\dfrac{\pi^i(\pi\cdot\partial^\mu\pi)}{(1-\pi\cdot\pi)}\right]\partial^\nu \pi^i-g^{\mu\nu}\dfrac{1}{2g^2}\left[\partial_\alpha\pi\cdot\partial^\alpha\pi+\dfrac{(\pi\cdot\partial_\alpha\pi)(\pi\cdot\partial^\alpha\pi)}{(1-\pi\cdot\pi)}\right]}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Problem 1.4.D
> Show that the energy-momentum tensor is conserved by taking the four-divergence and using the equations of motion.

Taking the 4-divergence of the original tensor expression, we have
$$\begin{align}
\partial_\mu T^{\mu\nu}
&=\partial_\mu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi^i)}\partial^\nu \pi^i\right)-\partial_\mu\left(g^{\mu\nu}\mathcal{L}\right)\\
&=\partial_\mu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi^i)}\right)\partial^\nu \pi^i+\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi^i)}\partial_\mu\left(\partial^\nu \pi^i\right)-\partial^\nu\mathcal{L}\\
&=\partial_\mu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi^i)}\right)\partial^\nu \pi^i+\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi^i)}\partial_\mu\left(\partial^\nu \pi^i\right)-\left[\dfrac{\partial\mathcal{L}}{\partial\pi^i}\partial^\nu \pi^i+\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi^i)}\partial^\nu \partial_\mu\pi^i\right]\\
\partial_\mu T^{\mu\nu}&=-\left[\dfrac{\partial\mathcal{L}}{\partial\pi^i}-\partial_\mu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi^i)}\right)\right]\partial^\nu \pi^i\\
\Aboxed{\partial_\mu T^{\mu\nu}&=0}
\end{align}$$
Therefore the energy-momentum tensor is conserved.
