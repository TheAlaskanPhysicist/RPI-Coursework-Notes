Author: Stanley Goodwin
Date: September 29th, 2025

---
## Question 1
Does the central limit theorem (CLT) really work? Consider the example of $N$ exponentially distributed random variables. Let $y=\sum_i x_i$, where $x_i$ are independent exponentially-distributed random variables, i.e., all $x_i$ has the same exponential probability density:
$$\begin{align}
\rho(x)&=\begin{cases}ae^{-ax}& x\ge 0\\0&x<0\end{cases}
\end{align}$$
---
### Question 1.A
Find the generating function for a single exponential variable, $\Phi(k)=\left\langle e^{ikx}\right\rangle$.

I was a little confused by the name, but this is the characteristic function in statistics!
$$\begin{align}
\Phi(k)&=\left\langle e^{ikx}\right\rangle\\
&=\int_{-\infty}^\infty e^{ikx}\rho(x)\ dx\\
&=\int_{0}^\infty e^{ikx}ae^{-ax}\ dx+\int_{-\infty}^0 e^{ikx}0\ dx\\
&=a\int_{0}^\infty e^{-(a-ik)x}\ dx\\
&=-a\left.\dfrac{e^{-(a-ik)x}}{a-ik}\right|_{x=0}^{x=\infty}\\
&=-a\left(\dfrac{0}{a-ik}-\dfrac{1}{a-ik}\right)\\
\Aboxed{\Phi(k)&=\dfrac{a}{a-ik}}
\end{align}$$
---
### Question 1.B
Find the generating function $\Phi_N(k)=\left\langle e^{ikx}\right\rangle$, for the sum of $N$ independent exponentially distributed random variables.

When we have the sum of $N$ independently sampled values.
$$\begin{align}
x_1+x_2+\dots x_N \rightarrow \Phi_1(k)\Phi_2(k)\dots\Phi_N(k)
\end{align}$$
So for our parameter $y$, we find that:
$$\begin{align}
y=\sum_i x_i \iff \Aboxed{\Phi_N(k)&=\left(\dfrac{a}{a-ik}\right)^N}
\end{align}$$
---
### Question 1.C
Use your mathematical skills to inverse Fourier transform $\Phi_N(k)$ and obtain $\rho_N(y)$, the exact probability density function for $y$.

Since there will be complex valued denominators, I'm going to use complex analysis to solve this.
$$\begin{align}
\rho_N(y)&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-iky}\Phi_N(k)\ dk\\
&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-iky}\left(\dfrac{a}{a-ik}\right)^N\ dk\\
&=\dfrac{a^N}{2\pi}\int_{-\infty}^\infty\dfrac{e^{-iky}}{(a-ik)^N}\ dk\\
&=\dfrac{a^N}{2\pi}\int_{\Gamma}\dfrac{e^{-iky}}{(a-ik)^N}\ dk\\
&=\dfrac{a^N}{2\pi}\cdot2\pi i\ \text{Res}\left(\dfrac{e^{-iky}}{(a-ik)^N}, k=-ia\right)\\
&=\dfrac{a^N}{2\pi}\cdot2\pi i\dfrac{1}{(N-1)!}\lim_{k\rightarrow-ia}\dfrac{d^{N-1}}{dk^{N-1}}\left((k+ia)^N\dfrac{e^{-iky}}{(a-ik)^N}\right)\\
&=\dfrac{a^N}{2\pi}\cdot2\pi i\dfrac{1}{(N-1)!}\lim_{k\rightarrow-ia}\dfrac{d^{N-1}}{dk^{N-1}}\left((k+ia)^N\dfrac{e^{-iky}}{(-i)^N(k+ia)^N}\right)\\
&=\dfrac{a^N}{2\pi}\cdot2\pi i\dfrac{1}{(N-1)!}\dfrac{1}{(-i)^N}\lim_{k\rightarrow-ia}\dfrac{d^{N-1}}{dk^{N-1}}\left(e^{-iky}\right)\\
&=\dfrac{a^N}{2\pi}\cdot2\pi i\dfrac{1}{(N-1)!}\dfrac{1}{(-i)^N}\lim_{k\rightarrow-ia}(-iy)^{N-1}\left(e^{-iky}\right)\\
&=\dfrac{a^N}{2\pi}\cdot2\pi i\dfrac{1}{(N-1)!}\dfrac{1}{(-i)^N}(-iy)^{N-1}\left(e^{-ay}\right)\\
&=a^N\dfrac{2\pi}{2\pi}\dfrac{1}{(N-1)!}\dfrac{(-i)^{N-1}}{(-i)^{N-1}}y^{N-1}e^{-ay}\\
\Aboxed{\rho_N(y)&=\dfrac{a^N}{(N-1)!}x^{N-1}e^{-ay}, y\ge0}
\end{align}$$
---
### Question 1.D
What you found in (c) is obviously not a Gaussian. How can we to reconcile it with the CLT? Write $\rho_N(y)$ as $\rho_N(y)=ae^{f(y)}$ and expand $f(y)$ about its maximum $y_0$.
#### Question 1.D.I (finding $y_0$)
Show that $y_0=\tfrac{N-1}{a}$ using Stirling's approximation.
$$\begin{align}
\rho_N(y)&=a\dfrac{a^{N-1}}{(N-1)!}y^{N-1}e^{-ay}, y\ge0\\
\rho_N(y)&=a\exp\left(\ln\left[\dfrac{a^{N-1}}{(N-1)!}y^{N-1}\right]-ay\right)\\
\Aboxed{f(y)&=\ln\left[\dfrac{a^{N-1}}{(N-1)!}y^{N-1}\right]-ay}
\end{align}$$
We can find its maximum of $f(y)$, $y=y_0$, when its slope is 0:
$$\begin{align}
f(y)&=\ln\left[\dfrac{a^{N-1}}{(N-1)!}y^{N-1}\right]-ay\\
\dfrac{df}{dy}&=\dfrac{(N-1)!}{a^{N-1}y^{N-1}}\left(\dfrac{a^{N-1}(N-1)}{(N-1)!}y^{N-2}\right)-a\\
0&=(N-1)\dfrac{1}{y_0}-a\\
a&=(N-1)\dfrac{1}{y_0}\\
\Aboxed{y_0&=\dfrac{N-1}{a}}
\end{align}$$
The value of the maximum, $f(y_0)$ is then found as:
$$\begin{align}
f(y_0)&=\ln\left[\dfrac{a^{N-1}}{(N-1)!}y_0^{N-1}\right]-ay_0\\
&=\ln\left[\dfrac{a^{N-1}}{(N-1)!}\left(\dfrac{N-1}{a}\right)^{N-1}\right]-(N-1)\\
&=\ln\left[\dfrac{a^{N-1}}{\sqrt{2\pi (N-1)}(N-1)^{(N-1)}e^{-(N-1)}}\dfrac{(N-1)^{N-1}}{(a)^{N-1}}\right]-(N-1)\\
&=\ln\left[\dfrac{e^{N-1}}{\sqrt{2\pi (N-1)}}\right]-(N-1)\\
&=\ln\left[e^{N-1}\right]-\dfrac{1}{2}\ln\left[2\pi (N-1)\right]-(N-1)\\
\Aboxed{f(y_0)&\approx-\dfrac{1}{2}\ln\left[2\pi (N-1)\right]}
\end{align}$$
---
#### Question 1.D.II (finding $f(y)$)
$$\begin{align}
f(y)&=\ln\left[\dfrac{a^{N-1}}{(N-1)!}y^{N-1}\right]-ay & \implies\\
f^{(k)}(y)&=(-1)^{k-1}(k-1)
!\dfrac{N-1}{y^k}
\end{align}$$
Except for $f'(y)$ has a $-a$ part as well. And so:
$$\begin{align}
f(y)&=\sum_{k=0}^\infty \dfrac{f^{(k)}(y_0)}{k!}(y-y_0)^k\\
&=f(y_0)+0+\sum_{k=2}^\infty\dfrac{1}{k!}\cdot(-1)^{k-1}(k-1)
!\dfrac{N-1}{y_0^k}\cdot(y-y_0)^k\\
&=f(y_0)+(N-1)\sum_{k=2}^\infty\dfrac{(-1)^{k-1}}{k}\cdot\left(\dfrac{y}{y_0}-1\right)^k\\
&=f(y_0)+\left(N-1-ay\right)+(N-1)\sum_{k=1}^\infty\dfrac{(-1)^{k-1}}{k}\cdot\left(\dfrac{y}{y_0}-1\right)^k\\
&=f(y_0)+\left(N-1-ay\right)+(N-1)\ln\left(1+\dfrac{y}{y_0}-1\right) & -1\lt\dfrac{y}{y_0}-1\le1\\
\Aboxed{&=f(y_0)+\left(N-1-ay\right)+(N-1)\ln\left(\dfrac{y}{y_0}\right) & 0\lt y\le y_0\\
f(y)&=-\dfrac{1}{2}\ln\left[2\pi (N-1)\right]+\left(N-1-ay\right)+(N-1)\ln\left(\dfrac{y}{y_0}\right)}
\end{align}$$
This does, in fact, equal the same function. However, we want to truncate after the 2nd derivative:
$$\begin{align}
f(y)&=\sum_{k=0}^2 \dfrac{f^{(k)}(y_0)}{k!}(y-y_0)^k\\
&=f(y_0)+0+\dfrac{1}{2!}\cdot(-1)^{2-1}(2-1)
!\dfrac{N-1}{y_0^2}\cdot(y-y_0)^2\\
\Aboxed{f(y)&\approx f(y_0)-\dfrac{1}{2}\dfrac{N-1}{y_0^2}\cdot(y-y_0)^2}
\end{align}$$
For future usage, we'll want it to be of the form $f(y)=f(y_0)-\dfrac{1}{2}\left(\dfrac{y-y_0}{\sigma}\right)^2$, and so:
$$\begin{align}
f(y)&=\sum_{k=0}^2 \dfrac{f^{(k)}(y_0)}{k!}(y-y_0)^k\\
&=f(y_0)+0+\dfrac{1}{2!}\cdot(-1)^{2-1}(2-1)
!\dfrac{N-1}{y_0^2}\cdot(y-y_0)^2\\
\Aboxed{f(y)&\approx f(y_0)-\dfrac{1}{2}\cdot\left(\dfrac{y-y_0}{\tfrac{y_0}{\sqrt{N-1}}}\right)^2}
\end{align}$$
---
#### Question 1.D.III
Show that in the asymptotic large $N$ limit, $\rho_N(y)$ converges to a Gaussian with mean $\mu_y=N/a$ and variance $\sigma_y^2=N/a^2$. Note: $\langle x\rangle=1/a$ and $\sigma^2_x=1/a^2$.
$$\begin{align}
\rho_N(y)&=ae^{f(y)}\\
\rho_N(y)&\approx \dfrac{a}{\sqrt{2\pi(N-1)}}\exp\left(-\dfrac{1}{2}\left(\dfrac{y-y_0}{\tfrac{y_0}{\sqrt{N-1}}}\right)^2\right)
\end{align}$$
Given the normal form of a Gaussian:
$$\begin{align}
\rho_N(y)&=A\exp\left(-\dfrac{1}{2}\left(\dfrac{y-\mu_y}{\sigma_y}\right)^2\right)
\end{align}$$
We can see that:
$$\begin{align}
\Aboxed{\mu_y&=y_0=\dfrac{N-1}{a}\approx\dfrac{N}{a}}\\
\sigma_y^2&=\left(\dfrac{y_0}{\sqrt{N-1}}\right)^2\\
&=\dfrac{1}{N-1}\left(\dfrac{N-1}{a}\right)^2\\
\Aboxed{\sigma_y^2&=\dfrac{N-1}{a^2}\approx\dfrac{N}{a^2}}
\end{align}$$
Knowing that $\braket{x}=\dfrac{1}{a}$ and $\sigma^2_x=\dfrac{1}{a^2}$, then we can see that the statistics of $y$ can be seen as:
$$\begin{align}
\mu_y&=N\braket{x} & \implies && \braket{x}&=\dfrac{\mu_y}{N}\\
\sigma_y^2&=N\sigma^2_x & \implies && \sigma_x&=\dfrac{\sigma_x}{\sqrt{N}}
\end{align}$$
These are the characteristics of a Gaussian, and therefore the proof is concluded.

---
## Question 2
Consider the microcanonical ensemble of $N$ independent classical (one-dimensional) oscillators with the same frequency $\omega$. Note that the oscillators are localized, hence *distinguishable* by construction.

---
### Question 2.A
Find the number of microstates between $E$ and $E+\delta E$, $\Omega(E,\delta E)$.

---
### Question 2.B
Find the entropy $S(E,N)$ for large values of $N$.

---
### Question 2.C
Show that $E=NkT$

---
### Question 2.D
What would be the energy for $N$ 3-dimensional classical harmonic oscillators?

---
## Question 3
he number of states in classical $N$-particle systems with energy less than $E$ can be typically written as $\Omega_<(E)=A_NE^{cN}$, where $A_N$ is an $N$-dependent prefactor, while $c$ is an N-independent constant. Using the notations from class, show that in the asymptotic large-$N$ limit, the following three expressions become approximately equal (to leading order in N):
$$\begin{align}
\ln\Omega_<(E)\approx\ln\Omega(E,\delta E)\approx\ln g_N(E)
\end{align}$$
Thus, in the microcanonical ensemble, we can use any of the above measures to obtain the entropy.


---
## Question 4
The dependence of the Hamiltonian of a classical system on a particular generalized coordinate $q$ is given by $H=H'+\alpha q^2$ , were $H'$ may depend on all other coordinates and momenta, but not $q$. Working in the canonical ensemble, show that $\langle\alpha q^2\rangle=\dfrac{1}{2}kT$.

---
## Question 5
Consider a system of $N$ independent and localized (distinguishable) magnetic dipoles in the presence of an external magnetic field $\vec{H}$ which points to the $z$ direction. The energy of an individual dipole is given by $\varepsilon=-\mu_zH$, where the possible values of $\mu_z$ are given by:
$$\begin{align}
\mu_z&=g\mu_Bm & m&=-J,-J+1,\dots,J-1,J
\end{align}$$
$J$ is a fixed integer or half-integer, related to the magnitude of the angular momentum of the atom, $g$ is the Lande factor, $\mu_B$ is the Bohr magneton, and $H$ is amplitude of the external field. Working in the canonical ensemble:

---
### Question 5.A
Find the average magnetization per dipole $\langle\mu_z\rangle=\dfrac{M}{N}$.

---
### Question 5.B
Find the magnetic susceptibility $\chi=\lim_{H\rightarrow 0}\dfrac{\partial M_z}{\partial H}$.

---
### Question 5.C
Discuss your findings in the high- and low-temperature limits.

---
