Author: Stanley Goodwin
Date: April 7th, 2026

---
## Question 5.44
> Consider a neutron in a magnetic field, fixed at an angle $\theta$ with respect to the $z$-axis, but rotating slowly in the $\hat{\phi}$ direction. That is, the tip of the magnetic field traces out a circle on the surface of the sphere, at "latitude" $\pi-\theta$. Explicitly calculate the Berry potential $\vec{A}$ for the spin-up state from $(5.234)$, take its curl, and determine Berry's phase $\gamma_+$. Thus, verify $(5.253)$ for this particular example of a curve $C$. (For hints, see "The adiabatic theorem and Berry’s phase" by Holstein, *Am. J. Ph s.*, Pg. 57 (1989) 1079.)

We have the magnetic field of the following form:
$$\begin{align}
\vec{B}(t)&=B\left(\hat{x}\sin\theta\cos\phi(t)+\hat{y}\sin\theta\sin\phi(t)+\hat{z}\cos\theta\right)
\end{align}$$
The spin state is always aligned with this field since it changes adiabatically:
$$\begin{align}
\ket{\psi^+}&=\cos\left(\tfrac{\theta}{2}\right)\ket{\uparrow}+e^{i\phi(t)}\sin\left(\tfrac{\theta}{2}\right)\ket{\downarrow}
\end{align}$$
The Berry connection is parametrized by $\theta,\phi(t)$, so we can take both differentials:
$$\begin{align}
\dfrac{\partial}{\partial\theta}\ket{\psi^+}&=-\dfrac{1}{2}\sin\left(\dfrac{\theta}{2}\right)\ket{\uparrow}+\dfrac{1}{2}e^{i\phi(t)}\cos\left(\dfrac{\theta}{2}\right)\ket{\downarrow}\\
\dfrac{\partial}{\partial\phi}\ket{\psi^+}&=ie^{i\phi(t)}\sin\left(\dfrac{\theta}{2}\right)\ket{\downarrow}
\end{align}$$
We can then complete the relation by projecting onto the original state:
$$\begin{align}
\bra{\psi^+}\dfrac{\partial}{\partial\theta}\ket{\psi^+}&=0 & \bra{\psi^+}\dfrac{\partial}{\partial\phi}\ket{\psi^+}&=i\sin^2\left(\dfrac{\theta}{2}\right)
\end{align}$$



We can then write the Berry connection in terms of the gradient of the parameters:
$$\begin{align}
\vec{A}&=i\bra{\psi^+}\vec\nabla_{\theta,\phi}\ket{\psi^+}\\
&=i\bra{\psi^+}\left(\right)\\
\end{align}$$







$$\begin{align}
\vec{S}(t)&=\dfrac{\hbar}{2}\left(\hat{x}\sin\theta\cos\phi(t)+\hat{y}\sin\theta\sin\phi(t)+\hat{z}\cos\theta\right)
\end{align}$$
 which can be written in spherical:











---
## Question 6.3
> Estimate the radius of the $^{40}\text{Ca}$ nucleus from the data in Figure $6.6$ and compare to that expected from the empirical value $\approx1.4A^{1/3}\text{ fm}$, where $A$ is the nuclear mass number. Check the validity of using the first-order Born approximation for these data.

The angle minimum of each datapoint relates to the effective radius:
$$\begin{align}
a\sin\theta_\text{min}\sim1\text{ fm} &\implies&& a\sin\theta_\text{min}\sim1\text{ fm}
\end{align}$$
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
Looks close enough. I don't know, I'm exhausted from this semester.

---
## Question 6.4
> Consider the potential where $V_0$ may be positive or negative.
> $$\begin{align}
V(r)&=\begin{cases}
V_0&r<R\\0&r>R
\end{cases}
\end{align}$$
---
### Question 6.4.A
> Using the method of partial waves, show that for $|V_0|\ll E$ and $kR\ll1$ the differential cross section is isotropic and that the total cross section is given by:
> $$\begin{align}
\sigma_\text{tot}&=\left(\dfrac{16\pi}{9}\right)\dfrac{m^2V_0^2R^6}{\hbar^4}
\end{align}$$

---
### Question 6.4.B
> Suppose that the energy is raised slightly. Show that the angular distribution can be written as:
> $$\begin{align}
\dfrac{d\sigma}{d\Omega}&=A+B\cos\theta
\end{align}$$
> Obtain an expression for $B/A$.




---
## Question 6.7
> Consider the scattering of a particle by an impenetrable sphere
> $$\begin{align}
V(r)&=\begin{cases}
\infty&r<a\\0&r>a
\end{cases}
\end{align}$$
### Question 6.7.A
> Derive an expression for the $s$-wave $(l=0)$ phase shift. (You need not know the detailed properties of the spherical Bessel functions to be able to do this simple problem)


### Question 6.7.B
> What is the total cross section $\sigma$ in the extreme low-energy limit $k\to0$? Compare your answer with the geometric cross section $\pi a^2$. You may assume without proof:
> $$\begin{align}
\dfrac{d\sigma}{d\Omega}&=|f(\theta)|^2 & f(\theta)&=\dfrac{1}{k}\sum_{l=0}^\infty(2l+1)e^{i\delta_l}\sin\delta_l\ P_l(\cos\theta)
\end{align}$$


## Question 6.12
> Show that the differential cross section for the elastic scattering of a fast positron by the ground state of the hydrogen atom is give by:
> $$\begin{align}
\dfrac{d\sigma}{d\Omega}&=\left(\dfrac{4m^2e^4}{\hbar^4q^4}\right)\left[1-\dfrac{16}{[4+(qa_0)^2]^2}\right]^2
\end{align}$$

