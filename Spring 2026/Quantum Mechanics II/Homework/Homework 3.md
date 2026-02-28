Author: Stanley Goodwin
Date: February 27th, 2026

---
## PDF Question 1
When calculating the relativistic corrections to the kinetic energy in class, we used the trick (without going through the details) that we can relate the expectation value $\bra{nlm}\tfrac{\gamma}{r^2}\ket{nlm}$ to the expansion of the *exact* energy levels of the "modified" Hydrogen-like atom with:
$$\begin{align}
l(l+1)&&\to&&l'(l'+1)=l(l+1)+\dfrac{2m\gamma}{\hbar^2}
\end{align}$$
Find $\bra{nlm}\dfrac{\gamma}{r^2}\ket{nlm}$.

Our perturbation is of the same form as the centrifugal term:
$$\begin{align}
V_\text{CF}&=\dfrac{l(l+1)\hbar^2}{2mr^2} & H'&=\dfrac{\gamma}{r^2}
\end{align}$$
Adding these two terms together, we get that:
$$\begin{align}
V&=\dfrac{\hbar^2}{2mr^2}\left(l(l+1)+\dfrac{2m}{\hbar^2}\gamma\right)=\dfrac{\hbar^2}{2mr^2}l'(l'+1)
\end{align}$$
Assuming that this perturbation is small, when $l'=l+dl$:
$$\begin{align}
l'(l'+1)&=(l+dl)(l+dl+1)\\
l(l+1)+\dfrac{2m}{\hbar^2}\gamma&=l(l+1)+(2l+1)dl+dl^2\\
\dfrac{2m}{\hbar^2}\gamma&\approx(2l+1)dl
\end{align}$$
Our simplification for $l'$ then takes the form:
$$\begin{align}
l'=l+\dfrac{2m}{(2l+1)\hbar^2}\gamma
\end{align}$$
As we saw in class, the energy is:
$$\begin{align}
E_{n'}&=-\dfrac{mc^2\alpha^2}{2n'^2} & n'=n+l'+1
\end{align}$$
Given that $l'$ is now a small perturbation of $l$, we can expand energy as:
$$\begin{align}
E_{n'}&=-\dfrac{mc^2\alpha^2}{2(n+dl)^2}\approx-\dfrac{mc^2\alpha^2}{2n^2}+2\dfrac{mc^2\alpha^2}{2n^3}dl-\dots
\end{align}$$
The difference of this energy is exactly our perturbation, and so we have:
$$\begin{align}
\bra{nlm}\dfrac{\gamma}{r^2}\ket{nlm}
&=\dfrac{mc^2\alpha^2}{n^3}\cdot\dfrac{2m}{(2l+1)\hbar^2}\gamma\\
&=\gamma\dfrac{2m^2c^2\alpha^2}{\hbar^2}\dfrac{1}{n^3(2l+1)}\\
\end{align}$$
We can use the Bohr radius $a_0=\dfrac{\hbar}{mc\alpha}$, to simplify our expression to:
$$\begin{align}
\bra{nlm}\dfrac{\gamma}{r^2}\ket{nlm}
&=\gamma\left(\dfrac{mc\alpha}{\hbar}\right)^{2}\dfrac{2}{n^3(2l+1)}\\
\Aboxed{\bra{nlm}\dfrac{\gamma}{r^2}\ket{nlm}&=\dfrac{\gamma}{a_0^2}\dfrac{1}{n^3\left(l+\tfrac{1}{2}\right)}}
\end{align}$$
---
## PDF Question 2
We discussed in class the first-order energy shifts $\Delta_K^{(1)}$ from relativistic corrections to the *kinetic* energy. We also discussed $\Delta_{LS}^{(1)}$ from the *spin-orbit* interaction, but there was a problem in that it gave a nonzero result for $l=0$ states if we blindly let an $l=0$ in the numerator cancel an $l=0$ in the denominator. In fact, $\Delta_{LS}^{(1)}$ from (5.3.31) is invalid for $l=0$. However, if we take into account the spread of the electron wavefunction in the region of changing electric field, we are led to include the *Darwin term* in the Hamiltonian. It turns out, the corresponding perturbation is:
$$\begin{align}
V_D&=-\dfrac{1}{8m^2c^2}\left[p_i,[p_i,V_C(r)]\right]
\end{align}$$
where $V_C(r)=-Ze^2/r$ is the Coulomb potential and summation over $i$ is implied.

---
### PDF Question 2.A
Find $\Delta_D^{(1)}$ and show that it is nonzero only for $l=0$ states, and that it gives precisely the same result as blindly using (5.3.31) for $l=0$.

For both commutators applied to a state $\psi$, we can use the position representation for momentum and the chain rule for derivatives to find:
$$\begin{align}
[p_i,V]\psi&=-i\hbar\left((\partial_iV)\psi+V\partial_i\psi-V\partial_i\psi\right) &\implies&& [p_i,V]&=-i\hbar\dfrac{\partial V}{\partial x_i}\\
\left[p_i,[p_i,V]\right]\psi&=(-i\hbar)^2\left(\partial_i\left(\dfrac{\partial V}{\partial x_i}\right)\psi+\dfrac{\partial V}{\partial x_i}\partial_i\psi-\dfrac{\partial V}{\partial x_i}\partial_i\psi\right)&\implies&&
\left[p_i,[p_i,V]\right]&=-\hbar^2\dfrac{\partial^2V}{\partial x_i^2}
\end{align}$$
The implicit summation turns the differentials into a gradient, and so our Darwin term is:
$$\begin{align}
V_D&=\dfrac{\hbar^2}{8m^2c^2}\vec{\nabla}^2V
&\implies&&
V_D&=-\dfrac{\hbar^2Ze^2}{8m^2c^2}\vec\nabla^2\left(\dfrac{1}{r}\right)
\end{align}$$
I'm going to use our Laplacian identity from Jackson's electrodynamics:
$$\begin{align}
\vec\nabla^2\left(\dfrac{1}{r}\right)&=-4\pi\delta^3(\vec{r})
&\implies&&
\Aboxed{V_D&=\dfrac{\pi\hbar^2Ze^2}{2m^2c^2}\delta^3(\vec{r})}
\end{align}$$
The expected value of the Darwin term is the energy shift $\Delta_D^{(1)}$:
$$\begin{align}
\bra{nlm}V_D\ket{nlm}=\Delta_D^{(1)}&=\int\dfrac{\pi\hbar^2Ze^2}{2m^2c^2}\braket{nlm\lvert\vec{r}}\delta^3(\vec{r})\braket{\vec{r}\lvert nlm}\ dr
\end{align}$$
The Dirac Delta function makes the evaluation of the wavefunction at $\vec{r}=0$:
$$\begin{align}
\Aboxed{\Delta_D^{(1)}&=\dfrac{\pi\hbar^2Ze^2}{2m^2c^2}|\psi_{nlm}(0)|^2}
\end{align}$$
The radial wavefunction is of the form:
$$\begin{align}
R_{nl}(r)&\sim r^l &\implies&& R_{nl}(0)&\sim\begin{cases}
1&l=0\\0&l\ge1
\end{cases}
\end{align}$$
Therefore, our energy shift is non-zero only $l=0$.

The normalized wavefunction is (from [Wikipedia](https://en.wikipedia.org/wiki/Hydrogen_atom#Wavefunction)), using just mass:
$$\begin{align}
\psi_{nlm}(\vec{r})&=\sqrt{\left(\dfrac{2}{na_0}\right)^3\dfrac{(n-l-1)!}{2n(n+l)!}}e^{-\rho/2}\rho^lL^{2l+1}_{n-l-1}(\rho)Y_l^m(\theta,\phi) & \rho&=\dfrac{2r}{na_0} & a_0
\end{align}$$
For $l=0$ states ($m=0$) and evaluation at $r=0$, then:
$$\begin{align}
|\psi_{n00}(\vec{r}=0)|^2&=\dfrac{1}{\pi}\left(\dfrac{Z}{na_0}\right)^3
\end{align}$$
Substituting into our Darwin energy correction term:
$$\begin{align}
\Delta_D^{(1)}&=\dfrac{\hbar^2Z^4e^2}{2m^2c^2a_0^3}\dfrac{1}{n^3} &\implies&& \Aboxed{\Delta_D^{(1)}&=\dfrac{(Z\alpha)^4}{2n^3}mc^2\delta_{l0},\ l=0}
\end{align}$$
I did the whole problem in Gauss units, btw, hence why there is no $\epsilon_0$ stuff.

---
### PDF Question 2.B
Then show that:
$$\begin{align}
\Delta_{nj}^{(1)}\equiv\Delta_K^{(1)}+\Delta_{LS}^{(1)}+\Delta_{D}^{(1)}=\dfrac{mc^2(Z\alpha)^4}{2n^3}\left(\dfrac{3}{4n}-\dfrac{2}{2j+1}\right)
\end{align}$$
Later on in this course, we will compare this expression to the result of solving the Dirac equation in the presence of Coulomb potential.

From previous sections, we have the energy corrections:
$$\begin{align}
\Delta_K^{(1)}&=\dfrac{(Z\alpha)^4}{2n^3}mc^2\left(\dfrac{3}{4n}-\dfrac{2}{2l+1}\right) \\
\Delta_{LS}^{(1)}&=\dfrac{(Z\alpha)^4}{2n^3}mc^2\left(\dfrac{1}{2l+1}-\dfrac{1}{2j+1}\right) \\
\Delta_{D}^{(1)}&=\dfrac{(Z\alpha)^4}{2n^3}mc^2\delta_{l0}
\end{align}$$
Adding the first two terms together, we have:
$$\begin{align}
\Delta_K^{(1)}+\Delta_{LS}^{(1)}&=\dfrac{(Z\alpha)^4}{2n^3}mc^2\left(\dfrac{3}{4n}-\dfrac{1}{2l+1}-\dfrac{1}{2j+1}\right)
\end{align}$$
Since we have the angular momentum $j=l\pm\tfrac{1}{2}\implies 2j=2l\pm1$, then we see:
$$\begin{align}
\dfrac{1}{2l+1}+\dfrac{1}{2j+1}&=\dfrac{2}{2j+1}\pm\dfrac{1}{(2l+1)(2j+1)}
\end{align}$$
Substituting back in, the two sum is:
$$\begin{align}
\Delta_K^{(1)}+\Delta_{LS}^{(1)}&=\dfrac{(Z\alpha)^4}{2n^3}mc^2\left(\dfrac{3}{4n}-\dfrac{2}{2j+1}\mp\dfrac{1}{(2l+1)(2j+1)}\right)
\end{align}$$
Adding in the Darwin term, for $l=0\implies j=\pm\tfrac{1}{2}$, we get:
$$\begin{align}
\Delta_K^{(1)}+\Delta_{LS}^{(1)}+\Delta_{D}^{(1)}&=\dfrac{(Z\alpha)^4}{2n^3}mc^2\left(\dfrac{3}{4n}-\dfrac{2}{2j+1}\mp\dfrac{1}{(1)(1\pm1)}+1\right)\\
&=\dfrac{(Z\alpha)^4}{2n^3}mc^2\left(\dfrac{3}{4n}-\dfrac{2}{2j+1}-1+1\right)\\
\Aboxed{\Delta_{nj}^{(1)}&=\dfrac{(Z\alpha)^4}{2n^3}mc^2\left(\dfrac{3}{4n}-\dfrac{2}{2j+1}\right)}
\end{align}$$
---
## Question 5.25
Work out the *quadratic* Zeeman effect for the ground-state hydrogen atom due to the usually neglected $e^2\vec{A}^2/2m_ec^2$ term in the Hamiltonian taken to the first order. Write the energy shift as:
$$\begin{align}
\Delta=-\dfrac{1}{2}\chi\vec{B}^2
\end{align}$$
and obtain an expression for *diamagnetic susceptibility* $\chi$.

Suppose a perturbative Hamiltonian with the form of the neglected term:
$$\begin{align}
H'&=\dfrac{e^2\vec{A}^2}{2m_ec^2}
\end{align}$$
The vector potential relates to the magnetic field by $\vec{B}=\vec\nabla\times\vec{A}$. It would be convenient if we choose a gauge that is rotationally symmetric about the $z$-axis:
$$\begin{align}
\text{Let }\vec{A}&\propto\vec{B}\times\vec{r}\\
\vec\nabla\times\vec{A}&\propto\vec\nabla\times\left(\vec{B}\times\vec{r}\right)\\
\vec{B}&\propto2\vec{B}\\
\Aboxed{\vec{A}&=\dfrac{1}{2}\vec{B}\times\vec{r}}
\end{align}$$
Since our magnetic field is $\vec{B}=B\hat{z}$, and $\hat{z}\times\hat{r}=\sin\theta$, we get that:
$$\begin{align}
H'&=\dfrac{e^2}{2m_ec^2}\cdot\left(\dfrac{1}{2}Br\sin\theta\right)^2=\dfrac{e^2B^2}{8m_ec^2}r^2\sin^2\theta
\end{align}$$
We'll need both these expected values at some point, so we can notice that:
$$\begin{align}
\sin^2\theta&=1-\cos^2\theta=1-\dfrac{z^2}{r^2} &\implies&& r^2\sin^2\theta &=r^2-z^2
\end{align}$$
Therefore we can write our Hamiltonian as:
$$\begin{align}
H'&=\dfrac{e^2}{2m_ec^2}\cdot\left(\dfrac{1}{2}Br\sin\theta\right)^2=\dfrac{e^2B^2}{8m_ec^2}\left(r^2-z^2\right)
\end{align}$$
For the expected value for the Hamiltonian (Energy Shift), we can see that:
$$\begin{align}
\braket{r^2}=\braket{x^2}+\braket{y^2}+\braket{z^2}=3\braket{z^2}
\end{align}$$
The Hamiltonian expectation value then reduces to:
$$\begin{align}
\braket{H'}&=\dfrac{e^2}{2m_ec^2}\cdot\left(\dfrac{1}{2}Br\sin\theta\right)^2=\dfrac{e^2B^2}{8m_ec^2}\cdot\dfrac{2}{3}\braket{r^2}
\end{align}$$
The expectation value can be calculated pretty simply because the ground state is simple:
$$\begin{align}
\braket{r^2}
&=\int_S\int_0^\infty r^2\left(\dfrac{e^{-r/a_0}}{\sqrt{\pi a_0^3}}\right)^2r^2\ dr\ d\Omega\\
&=\dfrac{4\pi}{\pi a_0^3}\int_0^\infty r^4e^{-2r/a_0}\ dr\\
&=\dfrac{4}{a_0^3}\left(\dfrac{a_0}{2}\right)^5\int_0^\infty u^{4}e^{-u}\ du\\
\Aboxed{\braket{r^2}&=3a_0^2}
\end{align}$$
Substituting this expression in and simplifying, we get:
$$\begin{align}
\Aboxed{\Delta&=\dfrac{e^2a_0^2}{4m_ec^2}B^2}
\end{align}$$
We know the form of the susceptibility, and so finally:
$$\begin{align}
\Delta&=-\dfrac{1}{2}\chi\vec{B}^2 &\implies && \Aboxed{\chi&=-\dfrac{e^2a_0^2}{2m_ec^2}}
\end{align}$$
---
## Question 5.27
Estimate the ground-state energy of a one-dimensional simple harmonic oscillator using:
$$\begin{align}
\braket{x\lvert\tilde{0}}&=e^{-\beta|x|}
\end{align}$$
as a trial function with $\beta$ to be varied.

Well firstly we can normalize this function:
$$\begin{align}
\int_{-\infty}^\infty\left|e^{-\beta|x|}\right|^2\ dx&=\dfrac{1}{\beta}
&\implies&&
\psi(\beta; x)&=\sqrt{\beta}e^{-\beta|x|}
\end{align}$$
The Hamiltonian in position representation is:
$$\begin{align}
H&=-\dfrac{\hbar^2}{2m}\dfrac{\partial^2}{\partial x^2}+\dfrac{1}{2}m\omega^2x^2
\end{align}$$
The expected value of each component is calculated pretty simply as:
$$\begin{align}
\left\langle T\right\rangle
&=-\dfrac{\hbar^2}{2m}\int_{-\infty}^\infty \sqrt{\beta}e^{-\beta|x|}\dfrac{\partial^2}{\partial x^2}\sqrt{\beta}e^{-\beta|x|}\ dx=+\dfrac{\hbar^2\beta^2}{2m}\\
\left\langle V\right\rangle
&=\dfrac{1}{2}m\omega^2\int_{-\infty}^\infty \sqrt{\beta}e^{-\beta|x|}x^2\sqrt{\beta}e^{-\beta|x|}\ dx=+\dfrac{m\omega^2}{4\beta^2}
\end{align}$$
Just some standard integrals that we've used many times before. The Hamiltonian is then:
$$\begin{align}
\left\langle H\right\rangle&=\dfrac{\hbar^2\beta^2}{2m}+\dfrac{m\omega^2}{4\beta^2}
\end{align}$$
We can differentiate this by beta in order to find the extrema of the system:
$$\begin{align}
\dfrac{d\left\langle H\right\rangle}{d\beta}&=\dfrac{\hbar^2\beta}{m}-\dfrac{m\omega^2}{2\beta^3}\\
0&=2\hbar^2\beta^4-m^2\omega^2\\
\Aboxed{\beta&=\sqrt{\dfrac{m\omega}{\sqrt{2}\hbar}}}
\end{align}$$
Substituting it back in for the expected energy, we approximate the ground state energy as:
$$\begin{align}
\left\langle H\right\rangle
&=\dfrac{\hbar^2}{2m}\dfrac{m\omega}{\sqrt{2}\hbar}+\dfrac{m\omega^2}{4}\dfrac{\sqrt{2}\hbar}{m\omega}\\
&=\dfrac{1}{2\sqrt{2}}\hbar\omega+\dfrac{\sqrt{2}}{4}\hbar\omega\\
\Aboxed{\left\langle H\right\rangle&=\dfrac{1}{\sqrt{2}}\hbar\omega\sim0.707\ \hbar\omega}
\end{align}$$
Seems to be a pretty decent approximation, with the true ground state having coefficient $0.5$.

---
## Question 5.30
A one-dimensional harmonic oscillator is in its ground state for $t<0$. For $t\ge0$ it is subjected to a time-dependent but spatially uniform force (not potential!) in the x-direction:
$$\begin{align}
\vec{F}(t)&=F_0e^{-t/\tau}
\end{align}$$
---
### Question 5.30.A
Using time-dependent perturbation theory to first order, obtain the probability of finding the oscillator in its first excited state for $t>0$. Show that the $t\to\infty$ ($\tau$ finite) limit of your expression is independent of time. Is this reasonable or surprising?

The (first-order) transition amplitude from notes is:
$$\begin{align}
c_n^{(1)}(t)&=\dfrac{1}{i\hbar}\int_0^t \bra{n}V\ket{i}e^{i\omega_{ni}t'}\ dt' & \omega_{ni}&=\dfrac{E_n-E_i}{\hbar}
\end{align}$$
We can write the time-dependent potential from the force integrated a displacement:
$$\begin{align}
-\dfrac{\partial V}{\partial x}&=F_0e^{-t/\tau} &\implies&& \Delta V&=-F_0e^{-t/\tau}x
\end{align}$$
Our Hamiltonian and potential is then expressible as:
$$\begin{align}
H_0&=\dfrac{p^2}{2m}+\dfrac{1}{2}m\omega^2x^2 & V(t)=-F_0e^{-t/\tau}x
\end{align}$$
We start in the ground state and want to find the transition to first-excited state, and so:
$$\begin{align}
c_1^{(1)}(t)&=-\dfrac{F_0}{i\hbar}\bra{1}x\ket{0}\int_0^te^{-t'/\tau}e^{i\omega t'}\ dt'
\end{align}$$
The cross-term of the expectation value of position can be found as the following:
$$\begin{align}
\bra{1}x\ket{0}&=\left(a^\dagger\ket{0}\right)^\dagger\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger+a\right)\ket{0}\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\bra{0}a\left(a^\dagger+a\right)\ket{0}\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\bra{0}\left(aa^\dagger\ket{0}+a^2\ket{0}\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\braket{0\lvert 0}+0\\
\Aboxed{\bra{1}x\ket{0}&=\sqrt{\dfrac{\hbar}{2m\omega}}}
\end{align}$$
The probability of transitioning to the first excited state, using the above, is then:
$$\begin{align}
P_{0\to1}(t)&=\dfrac{F_0^2}{2m\hbar\omega}\left|\int_0^te^{-t'/\tau}e^{i\omega t'}\ dt'\right|^2
\end{align}$$
This integral is a standard integration of an exponential:
$$\begin{align}
I=\int_0^te^{-(1/\tau+i\omega )t'}\ dt'
&=\dfrac{1-e^{-(1/\tau+i\omega )t}}{1/\tau+i\omega} & I^*=\dfrac{1-e^{-(1/\tau-i\omega )t}}{1/\tau-i\omega}
\end{align}$$
The magnitude squared is the product of $I$ and its complex conjugate, and so:
$$\begin{align}
|I|^2&=\dfrac{1}{1/\tau^2+\omega^2}\left(1-2e^{-t/\tau}\cos\left(\omega t\right)+e^{-2t/\tau}\right)
\end{align}$$
Substituting this expression back in, the transition probability is:
$$\begin{align}
\Aboxed{P_{0\to1}(t)&=\dfrac{F_0^2}{2m\hbar\omega}\dfrac{1-2e^{-t/\tau}\cos\left(\omega t\right)+e^{-2t/\tau}}{1/\tau^2+\omega^2}}
\end{align}$$
If we take the limit as $t\to\infty$ is pretty simple with the exponential decays:
$$\begin{align}
\Aboxed{\lim_{t\to\infty}P_{0\to1}(t)&=\dfrac{F_0^2}{2m\hbar\omega}\dfrac{1}{1/\tau^2+\omega^2}}
\end{align}$$
This makes sense since the amount of energy added to the system is finite, and so effectively the probability should scale as to have the average over all different state transfers to become steady.

Also interestingly, as we let $1/\tau\ll\omega$ in the long-time limit, we get that:
$$\begin{align}
\Aboxed{\lim_{\omega\gg 1/\tau}\lim_{t\to\infty}P_{0\to1}(t)&=\dfrac{F_0^2}{2m\hbar\omega^3}}
\end{align}$$
It's mildly surprising that is it inversely proportional to the cube of the angular frequency.

---
### Question 5.30.B
Can we find higher excited states?

We can write the transition amplitude out more explicitly as:
$$\begin{align}
c_n^{(1)}(t)&=-\dfrac{F_0}{i\hbar}\bra{n}x\ket{0}\int_0^te^{-t'/\tau}e^{in\omega t'}\ dt'
\end{align}$$
The cross-expectation on linear position is:
$$\begin{align}
\bra{n}x\ket{0}&=\left(\dfrac{a^{\dagger n}}{\sqrt{n!}}\ket{0}\right)^\dagger\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger+a\right)\ket{0}\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\bra{0}a^n\left(a^\dagger+a\right)\ket{0}\\
\bra{n}x\ket{0}&=\sqrt{\dfrac{\hbar}{2m\omega}}\delta_{n1}
\end{align}$$
So *no*, we cannot see any other transitions to higher excited states, at least in the 1st-order approx.

---
## Question 5.35
A hydrogen atom in its ground state is placed between the plates of a capacitor. A time-dependent but spatial uniform electric field (not potential!) is applied as follows:
$$\begin{align}
\vec{E}&=\begin{cases}
0&t<0\\
E_0e^{-t/\tau}\hat{z}&t\ge0
\end{cases}
\end{align}$$
Using first-order time-dependent perturbation theory, compute the probability for the atom to be found at $t\gg\tau$ in each of the three $2p$ states. Repeat the problem for the $2s$ state. Consider the 
limit $\tau\to\infty$.

Our transition amplitude for this system is:
$$\begin{align}
c_{nlm}^{(1)}(t)&=\dfrac{1}{i\hbar}\int_0^t \bra{nlm}V\ket{100}e^{i\omega_{n1}t'}\ dt' & \omega_{n1}&=\dfrac{E_n-E_1}{\hbar}
\end{align}$$
Similar to the previous part, we can write the potential in terms of the field:
$$\begin{align}
-\dfrac{\partial V}{\partial z}&=eE_0e^{-t/\tau} &\implies&& \Delta V&=-eE_0e^{-t/\tau}z
\end{align}$$
Using the known energy of bound states of hydrogen, we get that:
$$\begin{align}
c_{2lm}^{(1)}(t)&=-\dfrac{qE_0}{i\hbar}\bra{2lm}z\ket{100}\int_0^te^{-t/\tau}e^{i\omega_{21}t'}\ dt' & \omega_{21}&=\dfrac{3mc^2\alpha^2}{8\hbar}
\end{align}$$
Looking at a table of spherical harmonics, and using $z=r\cos\theta$, we find that:
$$\begin{align}
z&=r\sqrt{\dfrac{4\pi}{3}}Y_{10}(\theta,\phi)
\end{align}$$
If we write those states in a position basis, the inner product becomes:
$$\begin{align}
\bra{2lm}z\ket{100}
&=\int\int_0^\infty R_{2l}^*(r)Y_{lm}^*(\theta,\phi)\cdot r\sqrt{\dfrac{4\pi}{3}}Y_{10}(\theta,\phi)\cdot R_{10}(r)Y_{00}(\theta,\phi)\ r^2\ dr\ d\Omega\\
&=\sqrt{\dfrac{4\pi}{3}}\int_0^\infty r^3R_{2l}^*(r)R_{10}(r)\ dr\int Y_{lm}^*(\theta,\phi)\cdot Y_{10}(\theta,\phi)\ d\Omega\cdot\sqrt{\dfrac{1}{4\pi}}\\
&=\dfrac{1}{\sqrt{3}}\delta_{l1}\delta_{m0}\int_0^\infty r^3R_{21}^*(r)R_{10}(r)\ dr\\
\end{align}$$
Using the radial wavefunctions from a [table](https://quantummechanics.ucsd.edu/ph130a/130_notes/node233.html):
$$\begin{align}
\bra{2lm}z\ket{100}
&=\dfrac{1}{\sqrt{3}}\delta_{l1}\delta_{m0}\int_0^\infty r^3\left(\dfrac{1}{\sqrt{3}}\left[\dfrac{1}{2a_0}\right]^{3/2}\left[\dfrac{r}{a_0}\right]e^{-r/2a_0}\right)\left(2\left[\dfrac{1}{a_0}\right]^{3/2}e^{-r/a_0}\right)\ dr\\
&=\dfrac{1}{\sqrt{3}}\delta_{l1}\delta_{m0}\dfrac{1}{a_0^4\sqrt{6}}\int_0^\infty r^4e^{-3r/2a_0}\ dr\\
&=\dfrac{2^5a_0}{3^6\sqrt{2}}\delta_{l1}\delta_{m0}\int_0^\infty \left(\dfrac{3r}{2a_0}\right)^4e^{-3r/2a_0}\ d\left(\dfrac{3r}{2a_0}\right)\\
&=\dfrac{2^5a_0}{3^6\sqrt{2}}\delta_{l1}\delta_{m0}\cdot 4!\\
\Aboxed{\bra{2lm}z\ket{100}&=\dfrac{2^8}{3^5\sqrt{2}}a_0\delta_{l1}\delta_{m0}}
\end{align}$$
The probability of transition is then just:
$$\begin{align}
P_{100\to210}(t)&=\dfrac{2^{15}}{3^{10}}\dfrac{e^2E_0^2a_0^2}{\hbar^2}\left|\int_0^te^{-t/\tau}e^{i\omega_{21}t'}\ dt'\right|^2 & \omega_{21}&=\dfrac{3mc^2\alpha^2}{8\hbar}\\
P_{100\to200}(t)&=P_{100\to21,+1}(t)=P_{100\to21,-1}(t)=0
\end{align}$$
The integral can be evaluated pretty much identically to the previous question:
$$\begin{align}
|I|^2&=\dfrac{1}{1/\tau^2+\omega_{21}^2}\left(1-2e^{-t/\tau}\cos\left(\omega_{21} t\right)+e^{-2t/\tau}\right)
\end{align}$$
Substituting back in, we get the following 4 probabilities of transition:
$$\begin{align}
\Aboxed{P_{1s\to2p^z}(t)&=\dfrac{2^{15}}{3^{10}}\dfrac{e^2E_0^2a_0^2}{\hbar^2}\dfrac{1}{1/\tau^2+\tfrac{9m^2c^4\alpha^4}{64\hbar^2}}\left(1-2e^{-t/\tau}\cos\left(\tfrac{3mc^2\alpha^2}{8\hbar}t\right)+e^{-2t/\tau}\right)}
\end{align}$$
$$\begin{align}
\Aboxed{P_{1s\to2s}(t)&=0} & \Aboxed{P_{1s\to2p^x}(t)&=0} & \Aboxed{P_{1s\to2p^y}(t)&=0}
\end{align}$$
If we take the limit as $t\to\infty$ is pretty simple with the exponential decays:
$$\begin{align}
\Aboxed{\lim_{t\to\infty}P_{1s\to2p^z}(t)&=\dfrac{2^{15}}{3^{10}}\dfrac{e^2E_0^2a_0^2}{\hbar^2}\dfrac{1}{1/\tau^2+\tfrac{9m^2c^4\alpha^4}{64\hbar^2}}}
\end{align}$$
Also interestingly, as we let $1/\tau\ll\omega_{12}$ in the long-time limit, we get that:
$$\begin{align}
\Aboxed{\lim_{\omega_{12}\gg 1/\tau}\lim_{t\to\infty}P_{1s\to2p^z}(t)&=\left(\dfrac{4}{3}\right)^{12}\dfrac{\pi(\hbar c)^3}{(mc^2)^4\alpha^5}\left(\dfrac{1}{2}\epsilon_0E_0^2\right)}
\end{align}$$
In our case here, the transition probability looks to be proportional to the energy density of the field in our system, which is pretty cool.

Taking some rough approximation of our numbers, we see that:
$$\begin{align}
\lim_{\omega_{12}\gg 1/\tau}\lim_{t\to\infty}P_{1s\to2p^z}(t)
&\sim\left(\dfrac{4}{3}\right)^{12}\dfrac{\pi(\hbar c)^3}{(mc^2)^4\alpha^5}\left(\dfrac{1}{2}\epsilon_0E_0^2\right)\\
&=\left(\dfrac{4}{3}\right)^{12}\dfrac{\pi(197.3\text{ MeV}\cdot\text{fm})^3}{(0.511 \text{ MeV})^4(1/137)^5}\left(\dfrac{1}{2}\epsilon_0E_0^2\right)\\
\lim_{\omega_{12}\gg 1/\tau}\lim_{t\to\infty}P_{1s\to2p^z}(t)&\sim 5.392\cdot10^{20}\left(\dfrac{1}{2}\epsilon_0E_0^2\right)
\end{align}$$
This definitely shows that the field has to be *extremely weak* because probabilities have to be between 0 and 1, so as a rough boundary we can say this is somewhat acceptable for:
$$\begin{align}
\Aboxed{E_0\sim 10^{-5}\text{ F}/\text{m}}
\end{align}$$
This was just extra because I was curious about the super large number.

---
