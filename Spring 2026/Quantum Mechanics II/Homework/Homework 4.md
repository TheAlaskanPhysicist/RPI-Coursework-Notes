**Author:** Stanley Goodwin
**Date:** April 7th, 2026

---
## Question 5.44
> Consider a neutron in a magnetic field, fixed at an angle $\theta$ with respect to the $z$-axis, but rotating slowly in the $\hat{\phi}$ direction. That is, the tip of the magnetic field traces out a circle on the surface of the sphere, at "latitude" $\pi-\theta$. Explicitly calculate the Berry potential $\vec{A}$ for the spin-up state from $(5.234)$, take its curl, and determine Berry's phase $\gamma_+$. Thus, verify $(5.253)$ for this particular example of a curve $C$. (For hints, see "The adiabatic theorem and Berry’s phase" by Holstein, *Am. J. Ph s.*, Pg. 57 (1989) 1079.)

We have the magnetic field of the following form:
$$\begin{align}
\vec{B}(t)&=B\left(\hat{x}\sin\theta\cos\phi(t)+\hat{y}\sin\theta\sin\phi(t)+\hat{z}\cos\theta\right)
\end{align}$$
The spin state is always aligned with this field since it changes adiabatically:
$$\begin{align}
\ket{\psi^+}&=\cos\left(\tfrac{\theta}{2}\right)\ket{\uparrow}+e^{i\phi(t)}\sin\left(\tfrac{\theta}{2}\right)\ket{\downarrow} & \left(\ket{\psi^-}=-\sin\left(\tfrac{\theta}{2}\right)\ket{\uparrow}+e^{i\phi(t)}\cos\left(\tfrac{\theta}{2}\right)\ket{\downarrow}\right)
\end{align}$$
The Berry connection is parametrized by $\theta,\phi(t)$, so we can take both differentials:
$$\begin{align}
\dfrac{\partial}{\partial\theta}\ket{\psi^+}&=\dfrac{1}{2}\left[-\sin\left(\tfrac{\theta}{2}\right)\ket{\uparrow}+e^{i\phi(t)}\cos\left(\tfrac{\theta}{2}\right)\ket{\downarrow}\right] 
&\implies&&
\dfrac{\partial}{\partial\theta}\ket{\psi^+}&=\dfrac{1}{2}\ket{\psi^-}\\
\dfrac{\partial}{\partial\phi}\ket{\psi^+}&=ie^{i\phi(t)}\sin\left(\dfrac{\theta}{2}\right)\ket{\downarrow}
&\implies&&
\dfrac{\partial}{\partial\phi}\ket{\psi^+}&=i\ket{\downarrow}\braket{\downarrow\!\lvert \psi^+}
\end{align}$$
We can then write the Berry connection in terms of the gradient of the parameters:
$$\begin{align}
\vec{A}&=i\bra{\psi^+}\vec\nabla_{\theta,\phi}\ket{\psi^+}=i\bra{\psi^+}\left(\hat{\theta}\dfrac{\partial}{\partial\theta}\ket{\psi^+}+\hat{\phi}\dfrac{\partial}{\partial\phi}\ket{\psi^+}\right)\\
&=i\bra{\psi^+}\left(\dfrac{1}{2}\hat{\theta}\ket{\psi^-}+i\hat{\phi}\ket{\downarrow}\braket{\downarrow\!\lvert \psi^+}\right)=i\dfrac{1}{2}\braket{\psi^+\lvert \psi^-}\hat{\theta}-\left|\braket{\downarrow\!\lvert \psi^+}\right|^2\hat{\phi}\\
&=0-\sin^2\left(\tfrac{\theta}{2}\right)\hat{\phi}\\
\Aboxed{\vec{A}&=-\dfrac{1-\cos\theta}{2}\hat{\phi}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


Since we only contain a $A_\phi$ term we have only one element for the curl
$$\begin{align}
\vec\nabla\times\vec{A}
&=\dfrac{\hat{r}}{r\sin\theta}\dfrac{\partial}{\partial\theta}\left(-\dfrac{1-\cos\theta}{2}\sin\theta\right)\\
&=-\dfrac{\hat{r}}{2r\sin\theta}\dfrac{\partial}{\partial\theta}\left[(1-\cos\theta)\sin\theta\right]\\
&=-\dfrac{\hat{r}}{2r\sin\theta}\left[\sin^2\theta-\cos^2\theta+\cos\theta\right]\\
\Aboxed{\vec\nabla\times\vec{A}&=\dfrac{\hat{r}}{2r}\left[\csc\theta-2\sin^2\theta-\cot\theta\right]}
\end{align}$$
The Berry phase is much easier to compute, being just a contour integral
$$\begin{align}
\gamma_+&=\oint\vec{A}\cdot d\vec{l}=\int_0^{2\pi} A_\phi(\theta)\ d\phi
\end{align}$$
Substituting our component in, we get that the Berry phase is
$$\begin{align}
\Aboxed{\gamma_+&=-\pi(1-\cos\theta)}
\end{align}$$
With the equation $5.253$, we have the relationship that
$$\begin{align}
\gamma_\pm&=\mp\dfrac{1}{2}\Omega
\end{align}$$
The solid angle we sweep out on a sphere is the surface area spanned $\theta'$ and $\phi'$ :
$$\begin{align}
\Omega&=\int_{0}^{2\pi}\!\int_{0}^\theta\sin\theta'\ d\theta'\ d\phi'=2\pi(1-\cos\theta)
\end{align}$$
Substituting, we get that:
$$\begin{align}
\gamma_\pm&=\mp\dfrac{1}{2}\cdot2\pi(1-\cos\theta)=\mp\pi(1-\cos\theta) &\implies&& \Aboxed{\gamma_+&=-\pi(1-\cos\theta)}
\end{align}$$
Exactly the same as we got from the manual calculation.

---
## Question 6.3
> Estimate the radius of the $^{40}\text{Ca}$ nucleus from the data in Figure $6.6$ and compare to that expected from the empirical value $\approx1.4A^{1/3}\text{ fm}$, where $A$ is the nuclear mass number. Check the validity of using the first-order Born approximation for these data.

The angle minimum of each datapoint relates to the effective radius:
$$\begin{align}
a\sin\theta_\text{min}\sim1\text{ fm} &\implies&& a\sin\theta_\text{min}\sim1\text{ fm}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


I've estimated the points to be approximately (in degrees):
$$\begin{align}
^{48}\text{Ca}:\theta_\text{min}&\approx7.45 & ^{44}\text{Ca}:\theta_\text{min}&\approx7.60 &
^{42}\text{Ca}:\theta_\text{min}&\approx7.75 &
^{40}\text{Ca}:\theta_\text{min}&\approx7.95
\end{align}$$
These correspond to the radii:
$$\begin{align}
^{48}\text{Ca}:a&\approx7.7\text{ fm} & 
^{44}\text{Ca}:a&\approx7.5\text{ fm} &
^{42}\text{Ca}:a&\approx7.42\text{ fm} &
^{40}\text{Ca}:a&\approx7.23\text{ fm}
\end{align}$$
Using the empirical value, we instead get:
$$\begin{align}
^{48}\text{Ca}:a&\approx5.09\text{ fm} & 
^{44}\text{Ca}:a&\approx4.94\text{ fm} &
^{42}\text{Ca}:a&\approx4.86\text{ fm} &
^{40}\text{Ca}:a&\approx4.79\text{ fm}
\end{align}$$

---
## Question 6.4
> Consider the potential where $V_0$ may be positive or negative $V(r)=\begin{cases}V_0&r<R\\0&r>R\end{cases}$

---
### Question 6.4.A
> Using the method of partial waves, show that for $|V_0|\ll E$ and $kR\ll1$ the differential cross section is isotropic and that the total cross section is given by $\sigma_\text{tot}=\left(\dfrac{16\pi}{9}\right)\dfrac{m^2V_0^2R^6}{\hbar^4}$.

For this approximation regime, we can use the $l=0$ term and $\delta_l$ is small to find that
$$\begin{align}
f(\theta)&=\sum_{l=0}^\infty(2l+1)\dfrac{e^{2i\delta_l}-1}{2ik}P_l(\cos\theta)
&\implies&&
f(\theta)&\approx\dfrac{\delta_0}{k}
\end{align}$$
Since we have a weak potential, the phase shift can be (Born) approximated as
$$\begin{align}
f(\theta)&\approx-\dfrac{2m}{\hbar^2k}\int_0^\infty V(r)\ r\sin\left(kr\right)\ dr
&\implies&&
\delta_0&\approx-\dfrac{2m}{\hbar^2}\int_0^\infty V(r)\ r\sin\left(kr\right)\ dr
\end{align}$$
The sine can be Taylor expanded since we're in the $kr\ll1$ limit and that the potential restricts the integration bounds to an upper bound of $R$.
$$\begin{align}
\delta_0&\approx-\dfrac{2m}{\hbar^2}\int_0^R V_0\ r\left(kr\right)\ dr=-\dfrac{2mV_0R^3}{3\hbar^2}k
\end{align}$$
The differential cross-section then nicely simplifies to
$$\begin{align}
\dfrac{d\sigma}{d\Omega}&=\left|f(\theta)\right|^2=\dfrac{\delta_0^2}{k^2}=\dfrac{4}{9}\dfrac{m^2V_0^2R^6}{\hbar^4}
&\implies&&
\Aboxed{\sigma_\text{tot}&=\dfrac{16\pi}{9}\dfrac{m^2V_0^2R^6}{\hbar^4}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 6.4.B
> Suppose that the energy is raised slightly. Show that the angular distribution can be written as
> $$\begin{align}
\dfrac{d\sigma}{d\Omega}&=A+B\cos\theta
\end{align}$$
> Obtain an expression for $B/A$.

Start with the general equation again
$$\begin{align}
f(\theta)&=\sum_{l=0}^\infty(2l+1)\dfrac{e^{2i\delta_l}-1}{2ik}P_l(\cos\theta)
&\implies&&
f(\theta)&\approx\dfrac{\delta_0}{k}+3\dfrac{\delta_1}{k}\cos\theta
\end{align}$$
with the differential cross-section
$$\begin{align}
\dfrac{d\sigma}{d\Omega}=\left|f(\theta)\right|^2&=\dfrac{1}{k^2}\left|\delta_0+3\delta_1\cos\theta\right|^2=\dfrac{1}{k^2}\left(\delta_0^2+6\delta_0\delta_1\cos\theta+9\delta_1^2\cos^2\theta\right)
\end{align}$$
Since the energy increased slightly, we neglect the $\delta_1^2$ term we have the approximation
$$\begin{align}
\dfrac{d\sigma}{d\Omega}&\approx\dfrac{\delta_0^2}{k^2}+6\dfrac{\delta_0}{k}\dfrac{\delta_1}{k}\cos\theta
\end{align}$$
Setting the coefficients according to the form in the problem, we have the ratio
$$\begin{align}
A&=\dfrac{\delta_0^2}{k^2} & B&=6\dfrac{\delta_0}{k}\dfrac{\delta_1}{k}
&\implies&& \Aboxed{B/A&=6\dfrac{\delta_1}{\delta_0}}
\end{align}$$
In terms of orders of $k$ and $R$, the two phase shifts contribute to the ratio
$$\begin{align}
\delta_0&\sim kR^3 & B&\sim k^3R^5
&\implies&& \Aboxed{B/A&\sim6k^2R^4}
\end{align}$$
---
## Question 6.7
> Consider the scattering of a particle by an impenetrable sphere
> $$\begin{align}
V(r)&=\begin{cases}
\infty&r<a\\0&r>a
\end{cases}
\end{align}$$


<div style="page-break-before: always;"></div>*PDF next page*

### Question 6.7.A
> Derive an expression for the $s$-wave $(l=0)$ phase shift. (You need not know the detailed properties of the spherical Bessel functions to be able to do this simple problem)

Since the wavefunction vanishes inside, and that it is continuous at $r=a$, the genera form for the radial solution must look like
$$\begin{align}
u_0(r)&=A_0\sin\left(kr+\delta_0\right)
\end{align}$$
Imposing that it must be $0$ at $r=a$, then we get that:
$$\begin{align}
0&=A_0\sin\left(ka+\delta_0\right)
&\implies&&
ka+\delta_0&=n\pi
&\implies&&
\delta_0&=-ka\ (+n\pi)
\end{align}$$
Any choice of $n\in\mathbb{Z}$ will leave the phase identical or invert the amplitude, so therefore
$$\begin{align}
\Aboxed{\delta_0&=-ka}
\end{align}$$
---
### Question 6.7.B
> What is the total cross section $\sigma$ in the extreme low-energy limit $k\to0$? Compare your answer with the geometric cross section $\pi a^2$. You may assume without proof:
> $$\begin{align}
\dfrac{d\sigma}{d\Omega}&=|f(\theta)|^2 & f(\theta)&=\dfrac{1}{k}\sum_{l=0}^\infty(2l+1)e^{i\delta_l}\sin\delta_l\ P_l(\cos\theta)
\end{align}$$

In the low-energy limit, $l=0$ dominates and $\delta_0\to0$, so our scattering amplitude is approximately
$$\begin{align}
f(\theta)&=\dfrac{1}{k}e^{i\delta_0}\sin\delta_0\ P_0(\cos\theta)\approx\dfrac{1}{k}\delta_0=-a
\end{align}$$
The differential cross-section, as well as its total, are simply
$$\begin{align}
\dfrac{d\sigma}{d\Omega}&=a^2 &\implies&& \Aboxed{\sigma_\text{tot}&=4\pi a^2}
\end{align}$$
The effect of the potential in quantum mechanics is related to the surface area of the entire sphere, as opposed to its projection onto a plane as a circle.


<div style="page-break-before: always;"></div>*PDF next page*

## Question 6.12
> Show that the differential cross section for the elastic scattering of a fast positron by the ground state of the hydrogen atom is give by:
> $$\begin{align}
\dfrac{d\sigma}{d\Omega}&=\left(\dfrac{4m^2e^4}{\hbar^4q^4}\right)\left[1-\dfrac{16}{[4+(qa_0)^2]^2}\right]^2
\end{align}$$

In space, the total potential energy is the sum of the proton and electron contribution
$$\begin{align}
V(r)&=+\dfrac{e^2}{4\pi\epsilon_0}\dfrac{1}{r}-\dfrac{e^2}{4\pi\epsilon_0}\int\dfrac{\rho_\text{1s}(r)}{|\vec{r}-\vec{r}'|}\ d^3r'
\end{align}$$
Our positron is high energy relative to the magnitude of the potential, so we can use the Born approximation we used in a previous question
$$\begin{align}
f(\theta)&=-\dfrac{2m}{\hbar^2}\dfrac{1}{4\pi}\int e^{-i\vec{q}\cdot\vec{r}}V(r)\ d^3r=-\dfrac{2m}{\hbar^2}\dfrac{1}{4\pi}V(q)
\end{align}$$
The integration is just the Fourier transform. For the $1/r$ potential, it is easily found on a Fourier transform table, but for the electron cloud, we use that convolution turns to multiplication
$$\begin{align}
\mathcal{F}\int\dfrac{1}{|\vec{r}-\vec{r}'|}\rho_\text{1s}(r)\ d^3r'&=\mathcal{F}\left[\dfrac{1}{r}\right]\cdot\mathcal{F}\left[\rho_\text{1s}(r)\right]
\end{align}$$
The Fourier transform of our potential energy is then
$$\begin{align}
V(q)&=\dfrac{e^2}{4\pi\epsilon_0}\left[\mathcal{F}\left[\dfrac{1}{r}\right]-\mathcal{F}\left[\dfrac{1}{r}\right]\cdot\mathcal{F}\left[\rho_\text{1s}(r)\right]\right]\\
\Aboxed{V(q)&=\dfrac{e^2}{4\pi\epsilon_0}\dfrac{4\pi}{q^2}\left[1-\rho_\text{1s}(q)\right]}
\end{align}$$
The probability density in momentum-space comes from the ground state of hydrogen
$$\begin{align}
\rho_\text{1s}(r)&=\dfrac{1}{\pi a_0^3}e^{-2r/a_0} &\implies&& \rho_\text{1s}(q)&=\dfrac{16}{[4+(qa_0)^2]^2}
\end{align}$$
The scattering amplitude is just then
$$\begin{align}
f(\theta)&=-\dfrac{2m}{\hbar^2}\dfrac{1}{4\pi}V(q)\\
&=-\dfrac{2m}{\hbar^2}\dfrac{1}{4\pi}\cdot\dfrac{e^2}{4\pi\epsilon_0}\dfrac{4\pi}{q^2}\left[1-\dfrac{16}{[4+(qa_0)^2]^2}\right]\\
\Aboxed{f(\theta)&=-\dfrac{1}{4\pi\epsilon_0}\dfrac{2me^2}{\hbar^2q^2}\left[1-\dfrac{16}{[4+(qa_0)^2]^2}\right]}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


The differential cross-section is the square (magnitude but it is real), and so we have:
$$\begin{align}
\dfrac{d\sigma}{d\Omega}&=\dfrac{1}{(4\pi\epsilon_0)^2}\left(\dfrac{4m^2e^4}{\hbar^4q^4}\right)\left[1-\dfrac{16}{[4+(qa_0)^2]^2}\right]^2
\end{align}$$
To prove the expected equation, we just need to convert to the to Gauss units, leading to
$$\begin{align}
\Aboxed{\dfrac{d\sigma}{d\Omega}&=\left(\dfrac{4m^2e^4}{\hbar^4q^4}\right)\left[1-\dfrac{16}{[4+(qa_0)^2]^2}\right]^2}
\end{align}$$
