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
The $N-1\rightarrow N$ comes from a sample statistic vs a population statistic, but they're approximately the same for large sample sizes.

Knowing that $\braket{x}=\dfrac{1}{a}$ and $\sigma^2_x=\dfrac{1}{a^2}$, then we can see that the statistics of $y$ can be seen as:
$$\begin{align}
\mu_y&=N\braket{x} & \implies && \braket{x}&=\dfrac{\mu_y}{N}\\
\sigma_y^2&=N\sigma^2_x & \implies && \sigma_x&=\dfrac{\sigma_x}{\sqrt{N}}
\end{align}$$
These are the characteristics of a Gaussian, and therefore the proof is concluded.

---
## Question 2
Consider the microcanonical ensemble of $N$ independent classical (one-dimensional) oscillators with the same frequency $\omega$. Note that the oscillators are localized, hence *distinguishable* by construction.
$$\begin{align}
\hat{H}(p,q)&=\sum_n\dfrac{p_n^2}{2m}+\dfrac{1}{2}kq_n^2=\dfrac{p_n^2}{2m}+\dfrac{1}{2}m\omega^2q_n^2
\end{align}$$
---
### Question 2.A
Find the number of microstates between $E$ and $E+\delta E$, $\Omega(E,\delta E)$.
$$\begin{align}
\Omega_<(E)&=\int_{\hat{H}<E}\dfrac{d^{N}p\ d^{N}q}{h^{N}}\\
\end{align}$$
We can see this form an ellipse with semi-axes:
$$\begin{align}
p_\text{max}&=\sqrt{2mE}\\
x_\text{max}&=\sqrt{\dfrac{2E}{m\omega^2}}
\end{align}$$
For a constant energy $E$, we can see:
$$\begin{align}
E&=\sum_n\dfrac{p_n^2}{2m}+\dfrac{1}{2}m\omega^2q_n^2 & \implies && \sum_n\dfrac{1}{2mE}p_n^2+\sum_n\dfrac{m\omega^2}{2E}q_n^2&=1
\end{align}$$
This is just a 2N ellipsoidal object (also that each coefficient is constant), then:
$$\begin{align}
\Omega_<(E)&=\dfrac{1}{h^N}\dfrac{\pi^{2N/2}}{\Gamma(\tfrac{2N}{2}+1)}\left(p_\text{max}\right)^N\left(q_\text{max}\right)^N\\
&=\dfrac{1}{h^N}\dfrac{\pi^{N}}{\Gamma(N+1)}\left(\sqrt{2mE}\right)^N\left(\sqrt{\dfrac{2E}{m\omega^2}}\right)^N\\
&=\dfrac{1}{h^N}\dfrac{\pi^{N}}{N!}\left(\sqrt{\dfrac{2^2E^2}{\omega^2}}\right)^N\\
&=\dfrac{1}{h^N}\dfrac{\pi^{N}}{N!}\left(\dfrac{2E}{\omega}\right)^N\\
&=\dfrac{1}{N!}\left(\dfrac{2\pi}{h\omega}E\right)^N\\
\Aboxed{\Omega_<(E)&=\dfrac{1}{N!}\left(\dfrac{E}{\hbar\omega}\right)^N}
\end{align}$$
We can then find by differentiating all states below $E$ to get:
$$\begin{align}
\Omega(E,\delta E)&=\dfrac{d}{dE}\Omega_<(E)\ \delta E\\
&=\dfrac{1}{N!}\left(\dfrac{1}{\hbar\omega}\right)^N\dfrac{d}{dE}\left(E\right)^N\delta E\\
&=\dfrac{N}{N!}\left(\dfrac{1}{\hbar\omega}\right)^NE^{N-1}\delta E\\
&=\dfrac{1}{(N-1)!}\left(\dfrac{1}{\hbar\omega}\right)^NE^{N-1}\delta E\\
\Aboxed{\Omega(E,\delta E)&=\dfrac{1}{(N-1)!}\left(\dfrac{E}{\hbar\omega}\right)^N\dfrac{\delta E}{E}}
\end{align}$$
---
### Question 2.B
Find the entropy $S(E,N)$ for large values of $N$.
$$\begin{align}
S(E,N)/k&=\ln\Omega(E,\delta E)\\
&=N\ln\left(\dfrac{E}{\hbar\omega}\right)+\ln\left(\dfrac{\delta E}{E}\right)-\ln(N!)+\ln(N)\\
&=N\ln\left(\dfrac{E}{\hbar\omega}\right)+\ln\left(\dfrac{\delta E}{E}\right)-\dfrac{1}{2}\ln\left(2\pi N\right)-N\ln N+N+\ln(N)\\
\end{align}$$
Since $N$ is large, we'll neglect the terms who are exclusively $\ln N$, and so:
$$\begin{align}
S(E,N)/k
&=N\ln\left(\dfrac{E}{\hbar\omega}\right)+\ln\left(\dfrac{\delta E}{E}\right)-N\ln N+N\\
&=(N-1)\ln\left(\dfrac{E}{\hbar\omega}\right)+\ln\left(\dfrac{\delta E}{\hbar\omega}\right)-N\ln N+N\\
\end{align}$$
We can also say that $N-1=N$ in large limits, and so:
$$\begin{align}
S(E,N)/k
&=N\ln\left(\dfrac{E}{\hbar\omega}\right)+\ln\left(\dfrac{\delta E}{\hbar\omega}\right)-N\ln N+N\\
&=N\left[\ln\left(\dfrac{E}{\hbar\omega}\right)-\ln N+1\right]+\ln\left(\dfrac{\delta E}{\hbar\omega}\right)\\
\Aboxed{S(E,N)&\approx Nk\left[\ln\left(\dfrac{E}{N\hbar\omega}\right)+1\right]+k\ln\left(\dfrac{\delta E}{\hbar\omega}\right)}
\end{align}$$
One last thing, entropy is relative, and so we can drop constants who are not inputs to the function, since they'll be cancelled after finding a difference, and so:
$$\begin{align}
\Aboxed{\Delta S(E,N)&\approx Nk\left[\ln\left(\dfrac{E}{N\hbar\omega}\right)+1\right]}
\end{align}$$
---
### Question 2.C
Show that $E=NkT$
$$\begin{align}
\dfrac{1}{T}&=\left(\dfrac{\partial S}{\partial E}\right)_N\\
&=\dfrac{\partial}{\partial E}\left(Nk\left[\ln\left(\dfrac{E}{N\hbar\omega}\right)+1\right]\right)\\
&=Nk\dfrac{\partial}{\partial E}\left(\ln\left(E\right)-\ln\left(N\hbar\omega\right)\right)\\
\dfrac{1}{T}&=Nk\dfrac{1}{E}\\
\Aboxed{E&=NkT}
\end{align}$$
---
### Question 2.D
What would be the energy for $N$ 3-dimensional classical harmonic oscillators?

State space is exponential, so $\ln$ of that turns it linear. Therefore, it should be $3\times$ the energy.
$$\begin{align}
\Aboxed{E_\text{3D}&=3NkT}
\end{align}$$
---
## Question 3
The number of states in classical $N$-particle systems with energy less than $E$ can be typically written as $\Omega_<(E)=A_NE^{cN}$, where $A_N$ is an $N$-dependent prefactor, while $c$ is an N-independent constant. Using the notations from class, show that in the asymptotic large-$N$ limit, the following three expressions become approximately equal (to leading order in N):
$$\begin{align}
\ln\Omega_<(E)\approx\ln\Omega(E,\delta E)\approx\ln g_N(E)
\end{align}$$
Thus, in the microcanonical ensemble, we can use any of the above measures to obtain the entropy.
$$\begin{align}
\Aboxed{\Omega_<(E)&=A_NE^{cN}}\\
\Omega(E,\delta E)&=\dfrac{d}{dE}\Omega_<(E)\\
&=cNA_NE^{cN-1}\delta E\\
\Aboxed{\Omega(E,\delta E)&=cN\Omega_<(E)\dfrac{\delta E}{E}}\\
g(E)&=\Omega(E,\delta E)/\delta E\\
\Aboxed{g(E)&=\dfrac{cN}{E}\Omega_<(E)}
\end{align}$$
Taking the natural log of all these, we see:
$$\begin{align}
\Aboxed{\ln\Omega_<(E)&=cN\ln E+\ln A_N}\\
\Aboxed{\ln\Omega(E,\delta E)&=\ln\Omega_<(E)+\ln(c)+\ln(N)+\ln\left(\delta E\right)-\ln(E)}\\
\Aboxed{g(E)&=\ln\Omega_<(E)+\ln(c)+\ln(N)-\ln(E)}
\end{align}$$
Logarithms grow really slowly, so for large N's, we see that:
$$\begin{align}
\ln\Omega(E,\delta E)&=\ln\Omega_<(E)+\ln\left(\dfrac{c\delta E}{E}N\right)\approx\ln\Omega_<(E)\\
g(E)&=\ln\Omega_<(E)+\ln\left(\dfrac{c}{E}N\right)\approx\ln\Omega_<(E)
\end{align}$$
Therefore, all of them are similar in scale, since the dominating terms are all the same.

---
## Question 4
The dependence of the Hamiltonian of a classical system on a particular generalized coordinate $q$ is given by $H=H'+\alpha q^2$ , were $H'$ may depend on all other coordinates and momenta, but not $q$. Working in the canonical ensemble, show that $\langle\alpha q^2\rangle=\dfrac{1}{2}kT$.
Start with the probability density:
$$\begin{align}
\rho(p,q)&=\dfrac{e^{-\beta H}}{Z}=\dfrac{e^{-\beta H'}}{Z'}\dfrac{e^{-\beta\alpha q^2}}{Z_q}
\end{align}$$
This works because we have 2 entirely independent coordinate systems. 
$$\begin{align}
Z&=\int e^{-\beta\left(H'+\alpha q^2\right)}\ dq\\
&=\int e^{-\beta H'}dp\int e^{-\beta\alpha q^2}dq\\
Z&=Z'\cdot Z_\alpha\\
\end{align}$$
The expected value calculation is then:
$$\begin{align}
\braket{\alpha q^2}&=\dfrac{1}{Z}\int\alpha q^2e^{-\beta\left(H'+\alpha q^2\right)}\ dp\ dq\\
&=\dfrac{1}{Z'\cdot Z_\alpha}\int e^{-\beta H'}dp\int \alpha q^2e^{-\beta\alpha q^2}dq\\
&=\dfrac{\alpha Z'}{Z'\cdot Z_\alpha}\int q^2e^{-\beta\alpha q^2}dq\\
&=\dfrac{\int_{-\infty}^{-\infty} \alpha q^2e^{-\beta\alpha q^2}dq}{\int_{-\infty}^{\infty} e^{-\beta\alpha q^2}dq}\\
&=\alpha \dfrac{\tfrac{1}{2\beta\alpha}\sqrt{\tfrac{\pi}{\beta\alpha}}}{\sqrt{\tfrac{\pi}{\beta\alpha}}}\\
&=\alpha\dfrac{1}{2\beta\alpha}\\
\Aboxed{\braket{\alpha q^2}&=\dfrac{1}{2\beta}}
\end{align}$$
Substituting $\beta=1/kT$, then:
$$\begin{align}
\Aboxed{\braket{\alpha q^2}&=\dfrac{1}{2}kT}
\end{align}$$
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

Since they're all independent, lets solve it for 1 dipole first.
$$\begin{align}
Z_1&=\sum_{m={-J}}^Je^{-\beta \varepsilon}\\
&=\sum_{m={-J}}^Je^{\beta H g\mu_Bm}\\
&=e^{-(\beta H g\mu_B)J}\sum_{m={-J}}^Je^{(\beta H g\mu_B)m}e^{(\beta H g\mu_B)J}\\
&=e^{-(\beta H g\mu_B)J}\sum_{m={-J}}^Je^{(\beta H g\mu_B)(m+J)}\\
&=e^{-(\beta H g\mu_B)J}\sum_{m={0}}^{2J}e^{(\beta H g\mu_B)m}\\
\Aboxed{Z_1&=e^{-(\beta H g\mu_B)J}\cdot\dfrac{1-e^{(\beta H g\mu_B)(2J+1)}}{1-e^{(\beta H g\mu_B)}}}
\end{align}$$
This almost looks reducible. After a bit of trial and error:
$$\begin{align}
Z_1&=e^{-(\beta H g\mu_B)J}\cdot\dfrac{1-e^{(\beta H g\mu_B)(2J+1)}}{1-e^{(\beta H g\mu_B)}}\cdot\dfrac{e^{-(\beta H g\mu_B)(J+1/2)}}{e^{-(\beta H g\mu_B)(J+1/2)}}\\
&=-e^{-(\beta H g\mu_B)J}\cdot\dfrac{e^{+(\beta H g\mu_B)(J+1/2)}-e^{-(\beta H g\mu_B)(J+1/2)}}{2(1-e^{(\beta H g\mu_B)})}\cdot\dfrac{2}{e^{-(\beta H g\mu_B)(J+1/2)}}\\
&=-\cdot\dfrac{\sinh\left(\beta H g\mu_B\cdot\tfrac{2J+1}{2}\right)}{1-e^{(\beta H g\mu_B)}}\cdot\dfrac{2}{e^{-(\beta H g\mu_B)(1/2)}}\\
&=\dfrac{\sinh\left(\beta H g\mu_B\cdot\tfrac{2J+1}{2}\right)}{e^{+(\beta H g\mu_B)(1/2)}-e^{-(\beta H g\mu_B)(1/2)}}\cdot\dfrac{2}{1}\\
\Aboxed{Z_1&=\dfrac{\sinh\left(\beta H g\mu_B\cdot\tfrac{2J+1}{2}\right)}{\sinh\left(\beta H g\mu_B/2\right)}}
\end{align}$$
We can now calculate the magnetization average. Let $u=\beta H g\mu_B$:
$$\begin{align}
\braket{\mu_z}&=\dfrac{1}{Z_1}\sum_{m={-J}}^J\mu^z_m e^{um}\\
&=\dfrac{1}{Z_1}\sum_{m={-J}}^Jg\mu_Bm\cdot e^{um}\\
&=\dfrac{g\mu_B}{Z_1}\sum_{m={-J}}^J\dfrac{\partial}{\partial u}e^{um}\\
&=\dfrac{g\mu_B}{Z_1}\dfrac{\partial}{\partial u}\sum_{m={-J}}^Je^{um}\\
\Aboxed{\braket{\mu_z}&=\dfrac{g\mu_B}{Z_1}\dfrac{\partial Z_1}{\partial u}}
\end{align}$$
To find it explicitly, we substitute in and find that:
$$\begin{align}
\braket{\mu_z}&=\dfrac{g\mu_B}{Z_1}\dfrac{\partial Z_1}{\partial u}\\
&=\dfrac{g\mu_B}{Z_1}\dfrac{\partial}{\partial u}\left(\dfrac{\sinh\left(\tfrac{2J+1}{2}u\right)}{\sinh\left(u/2\right)}\right)\\
&=\dfrac{g\mu_B}{Z_1}\left(\dfrac{2J+1}{2}\dfrac{\sinh\left(u/2\right)\cosh\left(\tfrac{2J+1}{2}u\right)}{\sinh^2\left(u/2\right)}-\dfrac{1}{2}\dfrac{\sinh\left(\tfrac{2J+1}{2}u\right)\cosh\left(u/2\right)}{\sinh^2\left(u/2\right)}\right)\\
&=g\mu_B\left(\dfrac{\sinh\left(u/2\right)}{\sinh\left(\tfrac{2J+1}{2}u\right)}\right)\left(\dfrac{2J+1}{2}\dfrac{\cosh\left(\tfrac{2J+1}{2}u\right)}{\sinh\left(u/2\right)}-\dfrac{1}{2}\dfrac{\sinh\left(\tfrac{2J+1}{2}u\right)\cosh\left(u/2\right)}{\sinh^2\left(u/2\right)}\right)\\
&=g\mu_B\left(\dfrac{2J+1}{2}\coth\left(\tfrac{2J+1}{2}u\right)-\dfrac{1}{2}\coth\left(u/2\right)\right)
\end{align}$$
Substituting back $u=\beta H g\mu_B=\tfrac{H g\mu_B}{kT}$, then:
$$\begin{align}
\Aboxed{\braket{\mu_z}
&=g\mu_B\left[\dfrac{2J+1}{2}\coth\left(\tfrac{2J+1}{2}\tfrac{H g\mu_B}{kT}\right)-\dfrac{1}{2}\coth\left(\tfrac{1}{2}\tfrac{H g\mu_B}{kT}\right)\right]}
\end{align}$$
---
### Question 5.B
Find the magnetic susceptibility $\chi=\lim_{H\rightarrow 0}\dfrac{\partial M_z}{\partial H}$.
I'm bringing back $u=\beta g\mu_B$ because this is just getting annoying.
$$\begin{align}
\braket{M_z}&=N\braket{\mu_z}\\
&=Ng\mu_B\left[\tfrac{2J+1}{2}\coth\left(\tfrac{2J+1}{2}uH\right)-\tfrac{1}{2}\coth\left(\tfrac{1}{2}uH\right)\right]\\
&\approx Ng\mu_B\left[\tfrac{2J+1}{2}\left(\tfrac{2}{2J+1}\tfrac{1}{uH}+\tfrac{2J+1}{2}\tfrac{uH}{3}\right)-\tfrac{1}{2}\left
(\tfrac{2}{1}\tfrac{1}{uH}+\tfrac{1}{2}\tfrac{uH}{3}\right)\right]\\
&= Ng\mu_B\left[\tfrac{1}{uH}+\left(\tfrac{2J+1}{2}\right)^2\tfrac{uH}{3}-\tfrac{1}{uH}-\tfrac{uH}{12}\right]\\
&= \dfrac{Ng\mu_BuH}{12}\left[\left(2J+1\right)^2-1\right]\\
&= \dfrac{Ng\mu_BuH}{12}\left[4J^2+4J+1-1\right]\\
&= \dfrac{Ng\mu_B\beta g\mu_BH}{3}\left[J^2+J\right]\\
\Aboxed{\braket{M_z}&=\dfrac{N(g\mu_B)^2}{3kT}J(J+1)H}
\end{align}$$
This is the average magnetization excluding $O(H^3)$. We can then differentiate to get:
$$\begin{align}
\chi&=\lim_{H\rightarrow 0}\dfrac{\partial M_z}{\partial H}\\
&=\lim_{H\rightarrow 0}\dfrac{\partial}{\partial H}\left(\dfrac{N(g\mu_B)^2}{3kT}J(J+1)H\right)\\
&=\lim_{H\rightarrow 0}\left(\dfrac{N(g\mu_B)^2}{3kT}J(J+1)\right)\\
\Aboxed{\chi&=\dfrac{N(g\mu_B)^2}{3kT}J(J+1)}
\end{align}$$
Had we included higher powers $O(H^3)$, the limit would have sent those to 0.

---
### Question 5.C
Discuss your findings in the high- and low-temperature limits.

I can't tell if it's asking "discuss the limit" or "describe the characteristics at high/low temp."

#### High-Temperature Limit
$$\begin{align}
\lim_{T\rightarrow\infty}\braket{\mu_z}
&=\lim_{T\rightarrow\infty}\dfrac{(g\mu_B)^2}{3kT}J(J+1)H\\
&=\dfrac{H(g\mu_B)^2}{3k}J(J+1)\lim_{T\rightarrow\infty}\dfrac{1}{T}\\
\Aboxed{\lim_{T\rightarrow\infty}\braket{\mu_z}&=0}
\end{align}$$
The average magnetization goes to $0$ since there's so much energy that spins are randomly oriented, instead of any uniform structure. It's just Curie's law.
$$\begin{align}
\lim_{T\rightarrow\infty}\chi&=\lim_{T\rightarrow\infty}\dfrac{N(g\mu_B)^2}{3kT}J(J+1)\\
&=\dfrac{N(g\mu_B)^2}{3k}J(J+1)\lim_{T\rightarrow\infty}\dfrac{1}{T}\\
\Aboxed{\lim_{T\rightarrow\infty}\chi&=0}
\end{align}$$
As temperature increases, magnetic fields have a harder time polarizing dipoles.

---
#### Low-Temperature Limit
$$\begin{align}
\lim_{T\rightarrow0^+}\braket{\mu_z}
&=\lim_{T\rightarrow0^+}g\mu_B\left[\dfrac{2J+1}{2}\coth\left(\tfrac{2J+1}{2}\tfrac{H g\mu_B}{kT}\right)-\dfrac{1}{2}\coth\left(\tfrac{1}{2}\tfrac{H g\mu_B}{kT}\right)\right]\\
&=g\mu_B\left[\dfrac{2J+1}{2}\lim_{T\rightarrow0^+}\coth\left(\tfrac{2J+1}{2}\tfrac{H g\mu_B}{kT}\right)-\dfrac{1}{2}\lim_{T\rightarrow0^+}\coth\left(\tfrac{1}{2}\tfrac{H g\mu_B}{kT}\right)\right]\\
&=g\mu_B\left[\dfrac{2J+1}{2}\cdot1-\dfrac{1}{2}\cdot1\right]\\
&=g\mu_B\left[J+\dfrac{1}{2}-\dfrac{1}{2}\right]\\
\Aboxed{\lim_{T\rightarrow0^+}\braket{\mu_z}&=g\mu_BJ}
\end{align}$$
The average magnetization maximizes when the temperature goes to $0$, since $J$ is the magnitude of maximal magnetization, and all particles will have the same amount.
$$\begin{align}
\lim_{T\rightarrow0}\chi&=\lim_{T\rightarrow0}\dfrac{N(g\mu_B)^2}{3kT}J(J+1)\\
&=\dfrac{N(g\mu_B)^2}{3k}J(J+1)\lim_{T\rightarrow0}\dfrac{1}{T}\\
\Aboxed{\lim_{T\rightarrow0}\chi&=\infty}
\end{align}$$
As temperature approaches $0$, any amount of magnetic field strongly polarizes the dipoles, and thus it diverges at $T=0$ since any infinitesimal field instantly polarizes.