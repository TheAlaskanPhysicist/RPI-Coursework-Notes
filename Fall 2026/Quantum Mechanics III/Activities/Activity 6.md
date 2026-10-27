**Author:** Stanley Goodwin
**Date:** October 5th, 2026

---
## Question 1
> Compute $\left[\phi(x^0,\vec{x}),\pi(y^0,\vec{y})\right]$ to the leading non-vanishing order in $\lambda$ for the $\lambda\phi^4$ theory, where the above as the Heisenberg picture operators.

We start with the Lagrangian density
$$\begin{align}
\mathcal{L}&=\dfrac{1}{2}\left(\partial_\mu\phi\right)\left(\partial^\mu\phi\right)-\dfrac{1}{2}m^2\phi^2-\dfrac{\lambda}{4!}\phi^4
\end{align}$$
For the Heisenberg picture operator $\phi_H(x)$, we can expand the field about the free Klein-Gordon field solution, and this will be in orders of $\lambda$ as
$$\begin{align}
\phi_H(x^0,\vec{x})&=\phi_0(x^0,\vec{x})-\frac{\lambda}{3!}\iint\ dt\ d^3x'\ G_R(x^0,\vec{x};x'^0,\vec{x}')\ \phi_0^3
\end{align}$$
Where the Green's function here is the retarded version satisfying the Klein-Gordon equation.

Since the canonical momentum is $\pi_H(y^0,\vec{y})=\partial_{y^0}\phi_H(y^0,\vec{y})$
$$\begin{align}
\left[\phi_H(x^0,\vec{x}),\pi_H(y^0,\vec{y})\right]
=&\ \partial_{y^0}\left[\phi_0(x^0,\vec{x}),\phi_0(y^0,\vec{y})\right]\\
&-\dfrac{\lambda}{2}\int d^4z\ G_R(x-z)\phi_0^2(z)\partial_{y^0}\left[\phi_0(z^0,\vec{z}),\phi_0(y^0,\vec{y})\right]\\
&-\dfrac{\lambda}{2}\partial_{y^0}\int d^4z\ G_R(y-z)\phi_0^2(z)\left[\phi_0(x^0,\vec{x}),\phi_0(z^0,\vec{z})\right]\\
&+\mathcal{O}(\lambda^2)
\end{align}$$

---
## Question 2
> Express the components of the energy-momentum tensor $T^{\mu\nu}$ for the Klein-Gordon field in terms of creation and annihilation operators in the conventions of Peskin & Schroeder.

We have the Lagrangian density
$$\begin{align}
\mathcal{L}&=\dfrac{1}{2}\left(\partial_\mu\phi\right)\left(\partial^\mu\phi\right)-\dfrac{1}{2}m^2\phi^2
\end{align}$$
with the energy-momentum tensor
$$\begin{align}
T^{\mu\nu}&=\left(\partial^\mu\phi\right)\left(\partial^\nu\phi\right)-g^{\mu\nu}\mathcal{L}
\end{align}$$
We can expand the field in terms of the creation and annihilation operators (at equal time) as
$$\begin{align}
\phi(x)&=\int\dfrac{d^3p}{(2\pi)^3}\dfrac{1}{\sqrt{2E_\vec{p}}}\left(a_\vec{p}e^{-ip^\mu x_\mu}+a_\vec{p}^\dagger e^{+ip^\mu x_\mu}\right)
\end{align}$$
We can take the derivative of this field in terms of $p^\mu=(E_\vec{p},\vec{p})$ to find that
$$\begin{align}
\partial^\mu\phi(x)&=-i\int\dfrac{d^3p}{(2\pi)^3}\dfrac{p^\mu}{\sqrt{2E_\vec{p}}}\left(a_\vec{p}e^{-ip^\mu x_\mu}-a_\vec{p}^\dagger e^{+ip^\mu x_\mu}\right)
\end{align}$$
If we substitute the Lagrangian density into the energy-momentum tensor, we get
$$\begin{align}
T^{\mu\nu}
&=\left(\partial^\mu\phi\right)\left(\partial^\nu\phi\right)-g^{\mu\nu}\mathcal{L}\\
&=\left(\partial^\mu\phi\right)\left(\partial^\nu\phi\right)-g^{\mu\nu}\dfrac{1}{2}\left(\partial_\rho\phi\right)\left(\partial^\rho\phi\right)+g^{\mu\nu}\dfrac{1}{2}m^2\phi^2\\
\end{align}$$




Substituting into the energy-momentum tensor, we get







$$\begin{align}
T^{\mu\nu}=&-\dfrac{1}{2}\iint\dfrac{d^3p}{(2\pi)^3}\dfrac{d^3p'}{(2\pi)^3}\dfrac{p^\mu p'^\nu}{\sqrt{E_\vec{p}E_{\vec{p}'}}}\left(a_\vec{p}e^{-ip^\mu x_\mu}-a_\vec{p}^\dagger e^{+ip^\mu x_\mu}\right)\left(a_{\vec{p}'}e^{-ip'^\nu x'_\nu}-a_{\vec{p}'}^\dagger e^{+ip'^\nu x'_\nu}\right)\\
&-\frac{g^{\mu\nu}}{4}m^2\iint\dfrac{d^3p}{(2\pi)^3}\dfrac{d^3p'}{(2\pi)^3}\dfrac{1}{\sqrt{E_\vec{p}E_{\vec{p}'}}}\left(a_\vec{p}e^{-ip^\mu x_\mu}+a_\vec{p}^\dagger e^{+ip^\mu x_\mu}\right)\left(a_{\vec{p}'}e^{-ip'^\mu x'_\mu}+a_{\vec{p}'}^\dagger e^{+ip'^\mu x'_\mu}\right)\\

\end{align}$$