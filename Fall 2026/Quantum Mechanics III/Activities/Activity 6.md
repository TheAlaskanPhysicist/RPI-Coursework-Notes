**Author:** Stanley Goodwin
**Date:** October 5th, 2026

---
## Question 1
> Compute $\left[\phi(x^0,\vec{x}),\pi(y^0,\vec{y})\right]$ to the leading non-vanishing order in $\lambda$ for the $\lambda\phi^4$ theory, where the above as the Heisenberg picture operators.

We start from the Lagrangian density
$$\begin{align}
\mathcal{L}&=\dfrac{1}{2}\left(\partial_\mu\phi\right)\left(\partial^\mu\phi\right)-\dfrac{1}{2}m^2\phi^2-\dfrac{\lambda}{4!}\phi^4
\end{align}$$
We then have the Equation of Motion with a perturbed field
$$\begin{align}
\left(\partial^\mu\partial_\mu+m^2\right)\phi_H(x)&=-\dfrac{\lambda}{3!}\phi_H^3(x) &
\phi_H(x)&=\phi_0(x)+\lambda\phi_1(x)+\mathcal{O}(\lambda^2)
\end{align}$$
With the retarded Green's function, we can solve the differential equation as
$$\begin{align}
\left(\partial^\mu\partial_\mu+m^2\right)G_R(x-z)&=\delta^4(x-z)
\end{align}$$
Also using that the canonical momentum is $\pi_H(y^0,\vec{y})=\partial_{y^0}\phi_H(y^0,\vec{y})$, we can write it as
$$\begin{align}
\pi_H(y^0,\vec{y})&=\partial_{y^0}\phi_0(x)+\lambda\partial_{y^0}\phi_1(x)+\mathcal{O}(\lambda^2)\\
&\simeq\partial_{y^0}\phi_0(x)-\dfrac{\lambda}{3!}\int d^4z\ \partial_{y^0}G_R(y-z)\phi_0^3(z)
\end{align}$$
The commutator we're looking then becomes
$$\begin{align}
\left[\phi_H(x^0,\vec{x}),\pi_H(y^0,\vec{y})\right]
=&\left[\phi_0(x^0,\vec{x}),\partial_{y^0}\phi_0(y^0,\vec{y})\right]+\mathcal{O}(\lambda^2)\\
&-\dfrac{\lambda}{3!}\int d^4z\ G_R(y-z)\left[\phi_0^3(z),\partial_{y^0}\phi_0(y)\right]\\
&-\dfrac{\lambda}{3!}\int d^4z\ G_R(y-z)\left[\phi_0(x),\phi_0^3(z)\right]
\end{align}$$
Define the commutator of the free-field to be
$$\begin{align}
C_0(x,x')&=\left[\phi_0(x),\phi_0(x)\right]
\end{align}$$
Then the two eccentric commutators that we have can be expressed as
$$\begin{align}
\left[\phi_0^3(z),\partial_{y^0}\phi_0(y)\right]
=3\phi_0^2(z)\left[\phi_0(z),\partial_{y^0}\phi_0(y)\right]
&=3\phi_0^2(z)C_0(z,y)\\
\left[\phi_0(x),\phi_0^3(z)\right]
=3\phi_0^2(z)\left[\phi_0(x),\phi_0(z)\right]
&=3\phi_0^2(z)C_0(x,z)
\end{align}$$
Substituting back into the expression, we get that
$$\begin{align}
\left[\phi_H(x),\pi_H(y)\right]
&=\partial_{y^0}C_0(x,y)-\dfrac{\lambda}{2}\int d^4z\ \phi_0^2(z)\left[G_R(y-z)C_0(z,y)+G_R(y-z)C_0(x,z)\right]+\mathcal{O}(\lambda^2)
\end{align}$$
I can break this commutator into the order of $\lambda$ :
$$\begin{align}
\Aboxed{\left[\phi_H(x),\pi_H(y)\right]_0
&=i\int\dfrac{d^3p}{(2\pi)^3}\cos\left(E_\vec{p}(x^0-y^0)-\vec{p}\cdot(\vec{x}-\vec{y})\ \right)}\\
\Aboxed{\left[\phi_H(x),\pi_H(y)\right]_1&=-\dfrac{\lambda}{2}\int d^4z\ \phi_0^2(z)\left[G_R(y-z)C_0(z,y)+G_R(y-z)C_0(x,z)\right]}
\end{align}$$
---
## Question 2
> Express the components of the energy-momentum tensor $T^{\mu\nu}$ for the Klein-Gordon field in terms of creation and annihilation operators in the conventions of Peskin & Schroeder.

The commutator of the creation and annihilation operators is
$$\begin{align}
\left[a_\vec{p},a_\vec{q}^\dagger\right]&=(2\pi)^3\delta(\vec{p}-\vec{q})
\end{align}$$
From our typical Lagrangian density, we have the energy-momentum tensor
$$\begin{align}
T^{\mu\nu}&=\left(\partial^\mu\phi\right)\left(\partial^\nu\phi\right)-\dfrac{1}{2}g^{\mu\nu}\left(\partial_\rho\phi\ \partial^\rho\phi-m^2\phi^2\right)
\end{align}$$
We can expand the field in terms of the creation and annihilation operators (at equal time) as
$$\begin{align}
\phi(x)&=\int\dfrac{d^3p}{(2\pi)^3}\dfrac{1}{\sqrt{2E_\vec{p}}}\left(a_\vec{p}e^{-ip^\mu x_\mu}+a_\vec{p}^\dagger e^{+ip^\mu x_\mu}\right)
\end{align}$$
Then we can express the derivative of the field as
$$\begin{align}
\partial^\mu\phi(x)&=-i\int\dfrac{d^3p}{(2\pi)^3}\dfrac{p^\mu}{\sqrt{2E_\vec{p}}}\left(a_\vec{p}e^{-ip^\mu x_\mu}-a_\vec{p}^\dagger e^{+ip^\mu x_\mu}\right)
\end{align}$$
For convenience, define the operators
$$\begin{align}
A_\vec{p}&=a_\vec{p}e^{-ip^\mu x_\mu}+a_\vec{p}^\dagger e^{+ip^\mu x_\mu}
&\implies&&
\phi(x)&=\int\dfrac{d^3p}{(2\pi)^3}\dfrac{1}{\sqrt{2E_\vec{p}}}A_\vec{p}\\
B_\vec{p}&=a_\vec{p}e^{-ip^\mu x_\mu}-a_\vec{p}^\dagger e^{+ip^\mu x_\mu}
&\implies&&
\partial^\mu\phi(x)&=-i\int\dfrac{d^3p}{(2\pi)^3}\dfrac{p^\mu}{\sqrt{2E_\vec{p}}}B_\vec{p}
\end{align}$$
Substituting into the energy-momentum tensor, we get
$$\begin{align}
T^{\mu\nu}
&=\left(\partial^\mu\phi\right)\left(\partial^\nu\phi\right)-\dfrac{1}{2}g^{\mu\nu}\left(\partial_\rho\phi\ \partial^\rho\phi-m^2\phi^2\right)\\
&=(-i)^2\iint\dfrac{d^3p}{(2\pi)^3}\dfrac{d^3q}{(2\pi)^3}\dfrac{p^\mu}{\sqrt{2E_\vec{p}}}\dfrac{q^\nu}{\sqrt{2E_\vec{q}}}B_\vec{p}B_\vec{q}\\
&-\dfrac{1}{2}g^{\mu\nu}(-i)^2\iint\dfrac{d^3p}{(2\pi)^3}\dfrac{d^3q}{(2\pi)^3}\dfrac{p_\sigma}{\sqrt{2E_\vec{p}}}\dfrac{q^\sigma}{\sqrt{2E_\vec{q}}}B_\vec{p}B_\vec{q}\\
&+\dfrac{1}{2}g^{\mu\nu}m^2\iint\dfrac{d^3p}{(2\pi)^3}\dfrac{d^3q}{(2\pi)^3}\dfrac{1}{\sqrt{2E_\vec{p}}}\dfrac{1}{\sqrt{2E_\vec{q}}}A_\vec{p}A_\vec{q}\\
\Aboxed{T^{\mu\nu}&=\iint\dfrac{d^3p}{(2\pi)^3}\dfrac{d^3q}{(2\pi)^3}\dfrac{1}{\sqrt{2E_\vec{p}}}\dfrac{1}{\sqrt{2E_\vec{q}}}\left(-p^\mu q^\nu B_\vec{p}B_\vec{q}+\dfrac{1}{2}g^{\mu\nu}\left[p_\sigma q^\sigma B_\vec{p}B_\vec{q}+m^2A_\vec{p}A_\vec{q}\right]\right)}
\end{align}$$
If we use $\mu=\nu=0$ for energy density, we get...







