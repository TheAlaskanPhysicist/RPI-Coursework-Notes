
## Inspiration
One of the first things we learn with the Klein-Gordon Lagrangian,
$$\begin{align}
\mathcal{L}&=\left(\partial_\mu\phi^*\right)\left(\partial^\mu\phi\right)-m^2\phi^*\phi,
\end{align}$$
is that the equation of motion in spatial coordinates is
$$\begin{align}
\left(\partial^\mu\partial_\mu+m^2\right)\phi(x)&=0.
\end{align}$$
We tend to solve these systems by using the Fourier-transformed field
$$\begin{align}
\phi(x)&=\int\dfrac{d^4p}{(2\pi)^4}e^{-ip_\mu x^\mu}\phi(p),
\end{align}$$
since after substituting into the equation of motion, we get
$$\begin{align}
\int\dfrac{d^4p}{(2\pi)^4}\left(-p^\mu p_\mu+m^2\right)e^{-ip_\mu x^\mu}\phi(p)&=0,
\end{align}$$
and thus to hold for any particular choice of field, it must satisfy
$$\begin{align}
-p^\mu p_\mu+m^2&=0
&\implies&&
E^2-\vec{p}\cdot\vec{p}&=m^2.
\end{align}$$
This means that in the momentum basis, the equation of motion is
$$\begin{align}
\left(-p^\mu p_\mu+m^2\right)\phi(p)&=0,
\end{align}$$
which effectively transforms the differential equation into an algebraic equation. However, what if we wanted to choose a coordinate system such that the it is agnostic to either coordinate choice that are related by Fourier transforms? This would mean that the differential equation would look the same regardless of such a transform. For the Fourier transform, this would be a *gaussian* wavefunction in both position and momentum.


## Gaussian Systems
Suppose we have a wavefunction $\phi$, then for a Gaussian in position we have that
$$\begin{align}
\left<x\middle|\phi\right>=\phi(x)&=\dfrac{1}{\sigma_x\sqrt{2\pi}}e^{-(x-\mu_x)^2/2\sigma_x^2}
\end{align}$$
Upon a Fourier transform, we get that
$$\begin{align}
\phi(p)=\mathcal{F}\left[\phi(x)\right]&=e^{-(p-\mu_p)^2/2\sigma_x^{-2}}
\end{align}$$
Suppose we have a system who is a sum of Gaussians in spacetime
$$\begin{align}
\phi(x)&=\sum_{i=1}^N\dfrac{a_n}{\sqrt{2\pi\sigma_{x,n}^2}}e^{-\pi(x-\mu_{x,n})^2/2\pi\sigma_{x,n}^2}
\end{align}$$
The typical normalization condition isn't what we would expect since the Gaussians do not form a linearly independent basis, nor orthogonal in any way. However, the inner product is still normal.

The partial derivative in space for this field is
$$\begin{align}
\partial_\nu\phi(x)&=-\sum_{i=1}^N\dfrac{a_n}{\sigma_{x,n}^2\sqrt{2\pi\sigma_{x,n}^2}}(x-\mu_{x,n})^\nu e^{-\pi(x-\mu_{x,n})^2/2\pi\sigma_{x,n}^2}\\
\partial^\nu\partial_\nu\phi(x)&=-g^{\nu\nu}\sum_{i=1}^N\dfrac{a_n}{\sigma_{x,n}^2\sqrt{2\pi\sigma_{x,n}^2}}e^{-\pi(x-\mu_{x,n})^2/2\pi\sigma_{x,n}^2}+\sum_{i=1}^N\dfrac{a_n}{\sigma_{x,n}^4\sqrt{2\pi\sigma_{x,n}^2}}g^{\nu\mu}(x-\mu_{x,n})^\nu(x-\mu_{x,n})_\mu e^{-\pi(x-\mu_{x,n})^2/2\pi\sigma_{x,n}^2}
\end{align}$$
And so substituting into the equation of motion, we get
$$\begin{align}
\sum_{i=1}^N\left[-g^{\nu\nu}\dfrac{1}{\sigma_{x,n}^2}+\dfrac{1}{\sigma_{x,n}^4}g^{\nu\mu}(x-\mu_{x,n})^\nu(x-\mu_{x,n})_\mu+m^2\right]\dfrac{a_n}{\sqrt{2\pi\sigma_{x,n}^2}}e^{-\pi(x-\mu_{x,n})^2/2\pi\sigma_{x,n}^2}&=0
\end{align}$$
This isn't as simple as setting the coefficient inside to zero since, once again, the gaussians do not form a complete basis, and so we have to stop here. It's entirely possible that something like Hermite polynomials might be helpful.



## Hermite Systems
Suppose we have a wavefunction who is a product of Hermite functions in space
$$\begin{align}
\phi_\vec{n}(x)&=\prod_{\mu=0}^3\psi_{n_\mu}(x^\mu)
\end{align}$$
The normalized Hermite functions can be written out in terms of Hermite polynomials as
$$\begin{align}
\phi_\vec{n}(x)&=\frac{1}{\pi\sqrt{\prod_{\mu=0}^32^{n_\mu}n_\mu!}}\prod_{\mu=0}^3H_{n_\mu}(x^\mu)e^{-(x^\mu)^2/2}
\end{align}$$






$$\begin{align}
\mathcal{L}&=i\bar\nu_L\gamma^\mu\partial_\mu\nu_L+i\bar\nu_L^c\gamma^\mu\partial_\mu\nu_L^c+m_A\bar\nu_L\nu_L+m_B\left(\bar\nu_L\nu_L^c+\bar\nu_L^c\nu_L\right)+m_C\bar\nu_L^c\nu_L^c
\end{align}$$