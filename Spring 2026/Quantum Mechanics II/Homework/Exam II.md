**Author:** Stanley Goodwin
**Date:** April 25th, 2026

---
## Problem 1
> Consider scattering in *one dimension* by a general potential $V(x)$ localized near $x=0$. The initial state is a plane wave coming from the "left", that is $\phi(x)=\left<x\middle|i\right>=\tfrac{1}{\sqrt{2\pi}}e^{ikx}$ (properly normalized in the infinite system-size limit).

---
### Problem 1.A
> Find the scattering Green’s function $G(x,x')$ defined in one dimension analogously to Eq. $(6.37)$. Here, focus only on scattering from the past to the future (just as we did in class for the three-dimensional case).

Starting from equation $(6.35)$, we consider only the forward scattering $\ket{\psi^{(+)}}$ state
$$\begin{align}
\ket{\psi^{(+)}}&=\ket{i}+\dfrac{1}{E-H_0+i\varepsilon}V\ket{\psi^{(+)}}
\end{align}$$
Multiplying on the left by $\bra{x}$ and inserting a completeness relation in $x'$ between the fraction and the potential energy, we can write this in the form
$$\begin{align}
\left<x\middle|\psi^{(+)}\right>&=\left<x\middle|i\right>+\int_{-\infty}^\infty dx'\ \bra{x}\dfrac{1}{E-H_0+i\varepsilon}\ket{x'}\bra{x'}V\ket{\psi^{(+)}}
\end{align}$$
This is of the form of a convolution with a Greens function, and so we have that
$$\begin{align}
\Aboxed{G(x,x')&=\dfrac{\hbar^2}{2m}\bra{x}\dfrac{1}{E-H_0+i\varepsilon}\ket{x'}}
&\text{and}&&
\left<x\middle|\psi^{(+)}\right>&=\left<x\middle|i\right>+\dfrac{2m}{\hbar^2}\int_{-\infty}^\infty G(x,x')\bra{x'}V\ket{\psi^{(+)}}\ dx'
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


To make the Green's function more helpful, we can insert completeness relations in $k',k''$ just before and after the fraction respectively, since $E,H_0$ are much easier represented in $k$ space.
$$\begin{align}
G(x,x')&=\dfrac{\hbar^2}{2m}\iint_{-\infty}^\infty dk'\ dk''\left<x\middle|k'\right>\bra{k'}\dfrac{1}{E-H_0+i\varepsilon}\ket{k''}\left<k''\middle|x'\right>\\
&=\dfrac{\hbar^2}{2m}\iint_{-\infty}^\infty dk'\ dk''\left<x\middle|k'\right>\dfrac{1}{\tfrac{\hbar^2}{2m}k^2-\tfrac{\hbar^2}{2m}k'^2+i\varepsilon}\delta_{k'k''}\left<k''\middle|x'\right>\\
&=\dfrac{\hbar^2}{2m}\dfrac{2m}{\hbar^2}\int_{-\infty}^\infty\dfrac{dk'}{k^2-k'^2+i\varepsilon}\left<x\middle|k'\right>\left<k'\middle|x'\right> & (\tfrac{2m}{\hbar^2}\varepsilon\to\varepsilon\ll1)\\
&=\int_{-\infty}^\infty\dfrac{dk'}{k^2-k'^2+i\varepsilon}\cdot\dfrac{1}{\sqrt{2\pi}}e^{ik'x}\cdot\dfrac{1}{\sqrt{2\pi}}e^{-ik'x'}\\
\Aboxed{G(x,x')&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{ik'(x-x')}\dfrac{1}{k^2-k'^2+i\varepsilon}dk'}
\end{align}$$
This is just the (inverse) Fourier transform of the Lorentz distribution as $\epsilon\to0$. I don't remember the solution to it, so I'll have to derive it myself. To make it a little simpler, we can rearrange the denominator to make it clear where the singularities are:
$$\begin{align}
G(x,x')&=-\dfrac{1}{2\pi}\int_{-\infty}^\infty\dfrac{e^{ik'(x-x')}}{k'^2-(k^2+i\varepsilon)}dk'
\end{align}$$
The singularity is slightly below the imaginary axis for $\mathrm{Re}(k')<0$ and slightly above the imaginary axis for $\mathrm{Re}(k')>0$. To integrate over the real axis as $\epsilon\to0$, we must circumvent these singularities.

To find the integral over the real axis, we must break this into component contours and exploit Jordan's lemma since our bounds are infinite. We only need encapsulate one singularity, the positive solution, to get the proper answer. Construct the following parametrization
$$\begin{align}
\oint_\Gamma f(z)\ dz&=\lim_{R\to\infty}\lim_{\epsilon\to0^+}\left(\int_{-R}^{k-\epsilon} f(z)\ dz+\int_{\pi}^{2\pi} f(k+\epsilon e^{i\phi})\cdot i\epsilon e^{i\phi}d\phi\right.\\
&\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ +\left.\int_{k+\epsilon}^{R} f(z)\ dz+\int_{0}^{\pi} f(Re^{i\phi})\cdot iRe^{i\phi}d\phi\right)
\end{align}$$
Substituting $f(z)=\lim_{\varepsilon\to0}\dfrac{e^{iz(x-x')}}{z^2-(k^2+i\varepsilon)}=\dfrac{e^{iz(x-x')}}{z^2-k^2}$, we can evaluate each part one by one.
In the limits provided, integrals $(1)$ and $(3)$ become the principle part integral
$$\begin{align}
\lim_{R\to\infty}\lim_{\epsilon\to0}\left(\int_{-R}^{k-\epsilon} f(z)\ dz+\int_{k+\epsilon}^{R} f(z)\ dz\right)&=\mathcal{P}\int_{-\infty}^{\infty} \dfrac{e^{iz(x-x')}}{z^2-k^2}\ dz
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


Integral $(2)$, that keeps the singularity contained within the contour integral, is
$$\begin{align}
\left|\lim_{\epsilon\to0^+}\int_{\pi}^{2\pi} \dfrac{e^{i(x-x')\left(k+\epsilon e^{i\phi}\right)}}{\left(k+\epsilon e^{i\phi}\right)^2-k^2}\cdot i\epsilon e^{i\phi}d\phi\right|
&=\left|\lim_{\epsilon\to0^+}\int_{\pi}^{2\pi}\dfrac{1}{k^2+2k\epsilon e^{i\phi}+e^{2i\phi}-k^2}\cdot i\epsilon e^{i\phi}d\phi\right|\\
&=\left|\lim_{\epsilon\to0^+}\int_{\pi}^{2\pi}\dfrac{\epsilon}{2k\epsilon+e^{i\phi}}d\phi\right|=\left|\int_{\pi}^{2\pi}\dfrac{0}{2k\cdot0+e^{i\phi}}d\phi\right|\\
\lim_{\epsilon\to0^+}\int_{\pi}^{2\pi} \dfrac{e^{i(x-x')\left(k+\epsilon e^{i\phi}\right)}}{\left(k+\epsilon e^{i\phi}\right)^2-k^2}\cdot i\epsilon e^{i\phi}d\phi&=0
\end{align}$$
Integral $(4)$ can be written in the form of Jordan's lemma to find that
$$\begin{align}
(z=Re^{i\phi}) &&
\lim_{R\to\infty}\int_{0}^{\pi}\dfrac{e^{iz(x-x')}}{z^2-k^2}\ dz(\phi)
&=\lim_{R\to\infty}\int_{0}^{\pi}e^{i(x-x')z}\dfrac{1}{z^2-k^2}\ dz(\phi)\\
(x-x'>0) &&
\left|\lim_{R\to\infty}\int_{0}^{\pi}\dfrac{e^{iz(x-x')}}{z^2-k^2}\ dz(\phi)\right|&\le\lim_{R\to\infty}\dfrac{\pi}{x-x'}\max_{\phi\in[0,\pi]}\left|\dfrac{1}{(Re^{i\phi})^2-k^2}\right|\\
&&
\lim_{R\to\infty}\int_{0}^{\pi}\dfrac{e^{iz(x-x')}}{z^2-k^2}\ dz(\phi)&=0
\end{align}$$
All together, and using that close contour integrals are proportional to residue, we have that
$$\begin{align}
\int_{-\infty}^{\infty} \dfrac{e^{iz(x-x')}}{z^2-k^2}\ dz&=2\pi i\operatorname{Res}\left(\dfrac{e^{iz(x-x')}}{z^2-k^2}, z=k\right)
\end{align}$$
Fortunately, this is a difference of squares, so the singularity is a simple pole. Such a residue is
$$\begin{align}
\operatorname{Res}\left(\dfrac{e^{iz(x-x')}}{z^2-k^2}, z=k\right)
&=(z-k)\lim_{z\to k}\dfrac{e^{iz(x-x')}}{(z+k)(z-k)}=\dfrac{e^{ik(x-x')}}{2k}
\end{align}$$
The integral we have been solving is then just
$$\begin{align}
\int_{-\infty}^{\infty} \dfrac{e^{iz(x-x')}}{z^2-k^2}\ dz&=i\pi\dfrac{e^{ik(x-x')}}{k}
\end{align}$$
Therefore, our Green's function equation in one dimension is then just
$$\begin{align}
\Aboxed{\lim_{\varepsilon\to0}G(x,x')&=\dfrac{e^{ik(x-x')}}{2ik}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 1.B
> Consider the special case of an attractive delta-function potential $$V(x)=-\dfrac{\gamma\hbar^2}{2m}\delta(x), \ \ \ \gamma>0$$Use the Lippmann-Schwinger equation to find the outgoing wave function $\psi(x)=\left<x\middle|\psi^{(+)}\right>$.

The Lippmann-Schwinger equation is as follows (had to use the Textbook to know what it was)
$$\begin{align}
\ket{\psi^{(+)}}&=\ket{i}+\dfrac{1}{E-H_0+i\varepsilon}V\ket{\psi^{(+)}}
\end{align}$$
We can use the Green's function result from [[#Problem 1.A|part A]], as well as inserting another completely relation after the potential energy since it is diagonal in space, to get that
$$\begin{align}
\left<x\middle|\psi^{(+)}\right>
&=\left<x\middle|i\right>+\dfrac{2m}{\hbar^2}\iint_{-\infty}^\infty G(x,x')\left<x'\middle|V\middle|x''\right>\left<x''\middle|\psi^{(+)}\right>\ dx'\ dx''\\
&=\left<x\middle|i\right>-\dfrac{i}{2}\dfrac{e^{ikx}}{k}\dfrac{2m}{\hbar^2}\iint_{-\infty}^\infty e^{-ikx'}\left(-\dfrac{\gamma\hbar^2}{2m}\delta(x')\right)\delta_{x'x''}\left<x''\middle|\psi^{(+)}\right>\ dx'\ dx''\\
&=\left<x\middle|i\right>+\dfrac{\gamma\hbar^2}{2m}\dfrac{im}{\hbar^2k}e^{ikx}\int_{-\infty}^\infty e^{-ikx'}\delta(x')\left<x'\middle|\psi^{(+)}\right>\ dx'\\
&=\left<x\middle|i\right>+i\dfrac{\gamma}{2k}e^{ikx}e^{-ik\cdot0}\left<0\middle|\psi^{(+)}\right>\\
\Aboxed{\psi(x)&=\left<x\middle|i\right>+i\dfrac{\gamma}{2k}e^{ikx}\psi(0)}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 1.C
> Determine the transmission and reflection coefficients $T(k)$ and $R(k)$, defined as $$\psi(x)=\begin{cases}
T(k)\phi(x),&x>0\\\phi(x)+\tfrac{1}{\sqrt{2\pi}}R(k)e^{-ikx},&x<0
\end{cases}$$Show that $\left|T(k)\right|^2+\left|R(k)\right|^2=1$.

I'm not sure where to start, despite doing [[#Question 1.D|part D]] first. From [[#Problem 1.A|part A]] and [[#Problem 1.A|part B]], we have that
$$\begin{align}
\psi(x)&=\phi(x)+i\dfrac{\gamma}{2k}e^{ikx}\psi(0)
&\text{and}&&
\phi(x)&=\dfrac{1}{\sqrt{2\pi}}e^{ikx}
\end{align}$$
We can rewrite this first equation in terms of $\phi(x)$ as
$$\begin{align}
\psi(x)&=\phi(x)\left(1+i\dfrac{\gamma\sqrt{2\pi}}{2k}\psi(0)\right)
\end{align}$$
For our two different sides of the potential, we have the relationships
$$\begin{align}
T(k)&=\left(1+i\dfrac{\gamma\sqrt{2\pi}}{2k}\psi(0)\right)
&\text{and}&&
\tfrac{1}{\sqrt{2\pi}}R(k)e^{-ikx}&=i\dfrac{\gamma}{2k}e^{ikx}\psi(0)
\end{align}$$
At $x=0$, we can rearrange to find the wavefunction
$$\begin{align}
\psi(0)&=\dfrac{1}{\sqrt{2\pi}}e^{ik0}+i\dfrac{\gamma}{2k}e^{ik0}\psi(0)
&\implies&&
\psi(0)&=\dfrac{1}{\sqrt{2\pi}}\dfrac{1}{1-i\tfrac{\gamma}{2k}}
\end{align}$$
Our transmission coefficient is then
$$\begin{align}
\Aboxed{T(k)&=1+i\dfrac{\gamma}{2k-i\gamma}=\dfrac{2k}{2k-i\gamma}=2k\dfrac{2k+i\gamma}{4k^2+\gamma^2}}
\end{align}$$
Our reflection coefficient is a little more complicated since $x<0$, but solving we have that
$$\begin{align}
\Aboxed{R(k)&=i\gamma\dfrac{2k+i\gamma}{4k^2+\gamma^2}}
\end{align}$$
Taking the magnitude squared of each quantity and adding them together, we see that
$$\begin{align}
\Aboxed{|T(k)|^2+|R(k)|^2&=4k^2\dfrac{|2k+i\gamma|^2}{(4k^2+\gamma^2)^2}+\gamma^2\dfrac{|2k+i\gamma|^2}{(4k^2+\gamma^2)^2}=1}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 1.D
> Confirm that you get the same results by using "elementary" quantum mechanics and matching right- and left-going waves on the left with a right-going wave on the right at $x=0$. You'll need to integrate the Schrödinger equation across $x=0$ to find the discontinuity of the derivative.

Suppose we have a system with the following three functions
$$\begin{align}
\psi_\text{I}(x)&=A_\text{I}e^{ik_\text{I}x} & 
\psi_\text{I}'(x)&=A_\text{I}'e^{-ik_\text{I}x} &
\psi_\text{II}(x)&=A_\text{II}e^{ik_\text{II}x}
\end{align}$$
Since both sides of $x=0$ are probably the same medium, then $k_\text{I}=k_\text{II}=k$. Our potential is time-independent, and so we can use the TISE
$$\begin{align}
\left(-\dfrac{\hbar^2}{2m}\dfrac{\partial^2}{\partial x^2}-\dfrac{\gamma\hbar^2}{2m}\delta(x)\right)\psi&=E\psi
\end{align}$$
At the origin, we expect that the wavefunction will remain continuous. As limits, we have
$$\begin{align}
\lim_{x\to0^+}\psi(x)&=\lim_{x\to0^-}\psi(x)
\end{align}$$
We have the contributions from both sides, thus
$$\begin{align}
\lim_{x\to0^+}\left(A_\text{II}e^{ikx}\right)&=\lim_{x\to0^-}\left(A_\text{I}e^{ikx}+A_\text{I}'e^{-ikx}\right)
\end{align}$$
Evaluating both limits, we have the constraint that
$$\begin{align}
\Aboxed{A_\text{II}&=A_\text{I}+A_\text{I}'}
\end{align}$$
We require another condition to find a unique solution for this system.

Suppose we would like to integrate the TISE over the interval $x\in(-\delta,\delta)$. We then get that
$$\begin{align}
-\left.\dfrac{\hbar^2}{2m}\dfrac{\partial\psi}{\partial x}\right|_{x=-\delta}^{x=+\delta}-\dfrac{\gamma\hbar^2}{2m}\psi(0)&=E(2\delta)
\end{align}$$
In the limit of $\delta\to0$, we can rearrange and divide to have a difference in derivatives
$$\begin{align}
\lim_{\delta\to0^+}\left.\dfrac{\partial\psi}{\partial x}\right|_{x=\delta}-\lim_{\delta\to0^-}\left.\dfrac{\partial\psi}{\partial x}\right|_{x=\delta}&=\lim_{\delta\to0}\dfrac{2mE}{\hbar^2}(2\delta)-\gamma\psi(0)
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


If we substitute our wavefunctions for each limit side, we get that
$$\begin{align}
\lim_{x\to0^+}\dfrac{\partial}{\partial x}\left(A_\text{II}e^{ikx}\right)-\lim_{x\to0^-}\dfrac{\partial}{\partial x}\left(A_\text{I}e^{ikx}+A_\text{I}'e^{-ikx}\right)&=0-\gamma\psi(0)\\
\lim_{x\to0^+}ikA_\text{II}e^{ikx}-\lim_{x\to0^-}\left(ikA_\text{I}e^{ikx}-ikA_\text{I}'e^{-ikx}\right)&=-\lim_{x\to0}\gamma A_\text{II}e^{ikx}\\
ikA_\text{II}-ikA_\text{I}+ikA_\text{I}'&=-\gamma A_\text{II}\\
\Aboxed{A_\text{II}-A_\text{I}+A_\text{I}'&=-\dfrac{\gamma}{ik}A_\text{II}}
\end{align}$$
With our $A_\text{I}$ being a known input amplitude, we want to solve for the other two parameters
$$\begin{align}
A_\text{II}-A_\text{I}'&=A_\text{I} &
\left(1+\dfrac{\gamma}{ik}\right)A_\text{II}+A_\text{I}'&=A_\text{I}
\end{align}$$
After rearranging, we solve for the ratio of the amplitude to the incoming amplitude
$$\begin{align}
\dfrac{A_\text{I}'}{A_\text{I}}&=-\dfrac{\tfrac{\gamma}{2ik}}{1+\tfrac{\gamma}{2ik}} &
\dfrac{A_\text{II}}{A_\text{I}}&=\dfrac{1}{1+\tfrac{\gamma}{2ik}}
\end{align}$$
For my own sake, we can rationalize the denominator as well
$$\begin{align}
\dfrac{A_\text{I}'}{A_\text{I}}&=i\gamma\dfrac{2k+i\gamma}{4k^2+\gamma^2} &
\dfrac{A_\text{II}}{A_\text{I}}&=2k\dfrac{2k+i\gamma}{4k^2+\gamma^2}
\end{align}$$
These are exactly the transmission and reflection coefficients
$$\begin{align}
R(k)&=i\gamma\dfrac{2k+i\gamma}{4k^2+\gamma^2} &
T(k)&=2k\dfrac{2k+i\gamma}{4k^2+\gamma^2}
\end{align}$$
The probability of transmission/reflection are the magnitude squared of these ratios
$$\begin{align}
p_R(k)&=\dfrac{\gamma^2}{\gamma^2+4k^2} &
p_T(k)&=\dfrac{4k^2}{\gamma^2+4k^2}
\end{align}$$
It's very clear to see from here that the sum of the two probabilities is $1$, and so
$$\begin{align}
\Aboxed{\left|T(k)\right|^2+\left|R(k)\right|^2=1}
\end{align}$$
---
## Problem 2
> Consider scattering in three dimensions by a spherical delta-shell potential, $$V(r)=\dfrac{\hbar^2}{2m}\lambda\delta(r-R_0)$$

**Note:** I did this problem as my in-class turn-in, but wanted to at least finish the whole problem.


<div style="page-break-before: always;"></div>*PDF next page*

### Problem 2.A
> Find the exact phase shift for S-waves $(l=0)$, $\delta_0(k)$.

I realize now my approximation was not good enough and that I could have determined it exactly when I was doing the problem in-class. The radial Schrödinger equation is
$$\begin{align}
\dfrac{d^2u_l}{dr^2}+\dfrac{2m}{\hbar^2}\left[E-V(r)-\dfrac{l(l+1)\hbar^2}{2mr^2}\right]u_l&=0
\end{align}$$
Our system is for $l=0$, so this reduces much more nicely to
$$\begin{align}
\dfrac{d^2u_l}{dr^2}+\dfrac{2m}{\hbar^2}\left[E-\dfrac{\hbar^2}{2m}\lambda\delta(r-R_0)\right]u_l&=0
\end{align}$$
For an S-wave, I think I recall that our incoming and outgoing waves are identical except for a phase offset in the outgoing (from the plots we had during one of our lectures). Since the behavior of wavefunctions usually is that they are zero at boundaries, we will use $\sin$ to write
$$\begin{align}
u_\text{I}(r)&=A_\text{I}\sin\left(kr\right) & (r&<R_0)\\
u_\text{II}(r)&=A_\text{II}\sin\left(kr+\delta_0\right) & (r&>R_0)
\end{align}$$
Similar to [[#Problem 1|problem 1]], we find the continuity of the function and the discontinuity of the derivative since there is a delta function potential
$$\begin{align}
A_\text{II}\sin\left(kR_0+\delta_0\right)&=A_\text{I}\sin\left(kR_0\right)\\
A_\text{II}\cos\left(kR_0+\delta_0\right)&=A_\text{I}\cos\left(kR_0\right)+\dfrac{\lambda}{k}A_\text{I}\sin\left(kR_0\right)
\end{align}$$
Dividing the second equation by the first, we get that
$$\begin{align}
\cot\left(kR_0+\delta_0\right)&=\cot\left(kR_0\right)+\dfrac{\lambda}{k}
\end{align}$$
I will use a trick with inverse tangent, namely $\tan^{-1}(x)+\tan^{-1}(1/x)=\pi/2$.
$$\begin{align}
\tan\left(kR_0+\delta_0\right)&=\dfrac{1}{\cot\left(kR_0\right)+\dfrac{\lambda}{k}}\\
kR_0+\delta_0&=\tan^{-1}\left(\dfrac{1}{\cot\left(kR_0\right)+\dfrac{\lambda}{k}}\right)\\
\Aboxed{\delta_0(k)&=\dfrac{\pi}{2}-kR_0-\tan^{-1}\left(\cot\left(kR_0\right)+\dfrac{\lambda}{k}\right)}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Problem 2.B
> Obtain the limiting behavior of $\delta_0(k)$ for small $kR_0$ values.

For $kR_0\ll1$, we can make a series of approximations. Since the argument is small, cotangent can be written approximately as
$$\begin{align}
\cot\left(x\right)\approx\dfrac{1}{x}-\dfrac{x}{3}+\dots
\end{align}$$
Substituting into our expression from [[#Problem 2.A|part a]], we get that
$$\begin{align}
\lim_{kR_0\ll1}\delta_0(k)&=\dfrac{\pi}{2}-kR_0-\tan^{-1}\left(\dfrac{1+\lambda R_0}{kR_0}\right)
\end{align}$$
The approximation for the inverse tangent around this extreme limit is that
$$\begin{align}
\tan^{-1}(a/x)&\approx\dfrac{\pi}{2}-\dfrac{x}{a}
&\implies&&
\Aboxed{\lim_{kR_0\ll1}\delta_0(k)&=-kR_0\dfrac{\lambda R_0}{1+\lambda R_0}}
\end{align}$$
There are two limits to we can consider for our phase shift approximation
$$\begin{align}
\Aboxed{\lim_{kR_0\ll1}\delta_0(k)&=-kR_0^2\lambda}
& (\lambda R_0&\ll1)
&&&
\Aboxed{\lim_{kR_0\ll1}\delta_0(k)&=-kR_0}
& (\lambda R_0&\gg1)
\end{align}$$

---
### Problem 2.C
> Find the approximate total cross section $\sigma$ in the low-energy limit $(kR_0\ll1)$.

The method of partial waves is of the form
$$\begin{align}
\sigma&=\dfrac{4\pi}{k^2}(2l+1)\sin^2\delta_l &\rightarrow_{kR_0\ll1}&& \sigma&\approx\dfrac{4\pi}{k^2}\sin^2\delta_0(k)
\end{align}$$
For the phase shift being small, $\sin\left(x\right)\approx x$, so we can use our result from [[#Problem 2.B|part b]] to get
$$\begin{align}
\sin^2\left(\delta_0(k)\right)\approx\left(-kR_0\dfrac{\lambda R_0}{1+\lambda R_0}\right)^2=\dfrac{k^2\lambda^2R_0^4}{(1+\lambda R_0)^2}
\end{align}$$
So, for the low-energy limit, the total cross section is
$$\begin{align}
\Aboxed{\sigma&\approx\dfrac{4\pi\lambda^2R_0^4}{(1+\lambda R_0)^2}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Problem 2.D
> Find the scattering length.

For low-energy scattering, $\delta_0\approx-ka_0$. From [[#Problem 2.B|part b]], we set these two equal
$$\begin{align}
-ka_0=\lim_{kR_0\ll1}\delta_0(k)&=-kR_0\dfrac{\lambda R_0}{1+\lambda R_0}
&\implies&&
\Aboxed{a_0\approx R_0\dfrac{\lambda R_0}{1+\lambda R_0}}
\end{align}$$
---
## Problem 3
> This problem is taken from Landau (1996). A spinless electron is bound by a Coulomb potential $V(r)=-Ze^2/r$ in a stationary state of total energy $E\le m$. You can incorporate this interaction into the Klein-Gordon equation by using the covariant derivative with $V=-e\Phi$ and $\vec{A}=0$.

---
### Problem 3.A
> Assume that the radial and angular parts of the equation separate, and that the wave function can be written as $e^{-iEt}\dfrac{u_l(r)}{r}Y_{lm}(\theta,\phi)$ and show that the radial equation becomes $$\dfrac{d^2u_l}{d\rho^2}+\left[\dfrac{2EZ\alpha}{\gamma\rho}-\dfrac{1}{4}-\dfrac{l(l+1)-(Z\alpha)^2}{\rho^2}\right]u_l(\rho)=0$$where $\alpha=e^2$, $\gamma^2=4(m^2-E^2)$, and $\rho=\gamma r$.

The Klein-Gordon equation in flat spacetime is
$$\begin{align}
\left[\partial_\mu\partial^\mu+m^2\right]\psi&=0
\end{align}$$
We want to use the covariant derivative $\partial_\mu\to\partial_\mu+ieA_\mu$, and using that $A_0=\Phi$ and $\vec{A}=0$,
$$\begin{align}
\left[\left(\partial_t+ie\Phi\right)^2-\vec\nabla^2+m^2\right]\psi&=0
&\implies&&
\left[\left(\partial_t-i\dfrac{Ze^2}{r}\right)^2-\vec\nabla^2+m^2\right]\psi&=0
\end{align}$$
The question gives us the stationary state
$$\begin{align}
\psi&=e^{-iEt}\dfrac{u_l(r)}{r}Y_{lm}(\theta,\phi)
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


The time-derivative component of this equation reduces to
$$\begin{align}
\left(\partial_t-i\dfrac{Ze^2}{r}\right)^2\psi&=\left(-iE-i\dfrac{Ze^2}{r}\right)^2\psi=-\left(E+\dfrac{Ze^2}{r}\right)^2\psi
\end{align}$$
The space-derivative component is something that I had a lot of trouble with. From what I could see, knowing the solution, it should take the form
$$\begin{align}
\vec\nabla^2\psi
&=\dfrac{1}{u_l}\left[\dfrac{\partial^2 u_l}{\partial r^2}-\dfrac{l(l+1)}{r^2}u_l\right]\psi
\end{align}$$
Substituting back into the Klein-Gordon equation, we have that (after multiplying by $-1$)
$$\begin{align}
\left(E+\dfrac{Ze^2}{r}\right)^2\psi+\dfrac{1}{u_l}\left[\dfrac{\partial^2 u_l}{\partial r^2}-\dfrac{l(l+1)}{r^2}u_l\right]\psi-m^2\psi&=0
\end{align}$$
We can expand and combine terms to get it in a similar form to the solution
$$\begin{align}
\dfrac{\partial^2 u_l}{\partial r^2}+\left[E^2+\dfrac{2EZe^2}{r}+\dfrac{Z^2e^4}{r^2}-\dfrac{l(l+1)}{r^2}-m^2\right]u_l&=0
\end{align}$$
Using and $\alpha=e^2$ and $\gamma^2=4(m^2-E^2)$, this becomes
$$\begin{align}
\dfrac{\partial^2 u_l}{\partial r^2}+\left[\dfrac{2EZ\alpha}{r}-\dfrac{l(l+1)-(Z\alpha)^2}{r^2}-\dfrac{\gamma^2}{4}\right]u_l&=0\\
\dfrac{\partial^2 u_l}{\partial (r^2\gamma^2/\gamma^2)}+\gamma^2\left[\dfrac{2EZ\alpha}{\gamma^2r}-\dfrac{l(l+1)-(Z\alpha)^2}{\gamma^2r^2}-\dfrac{1}{4}\right]u_l&=0\\
\Aboxed{\dfrac{\partial^2 u_l}{\partial\rho^2}+\left[\dfrac{2EZ\alpha}{\gamma\rho}-\dfrac{1}{4}-\dfrac{l(l+1)-(Z\alpha)^2}{\rho^2}\right]u_l&=0}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Problem 3.B
> Assume that this equation has a solution of the usual form of a power series times the $\rho\to\infty$ and $\rho\to0$ solutions. That is, $$u_l(\rho)=\rho^k\left(1+c_1\rho+c_2\rho^2+\dots\right)e^{-\rho/2}=\sum_{n=0}^\infty c_n\rho^{n+k}e^{-\rho/2}$$and show that $$k=k_\pm=\dfrac{1}{2}\pm\sqrt{\left(l+\dfrac{1}{2}\right)^2-\left(Z\alpha\right)^2}$$and that only for $k_+$ is the expectation value of kinetic energy finite and that this solution has a nonrelativistic limit which agrees with the solution found for the Schrödinger equation.

I really don't know where to go here with this, so I'll just solve this the way I would. We have the radial equation from [[#Problem 3.A|part A]] of the form
$$\dfrac{d^2u_l}{d\rho^2}+\left[\dfrac{2EZ\alpha}{\gamma\rho}-\dfrac{1}{4}-\dfrac{l(l+1)-(Z\alpha)^2}{\rho^2}\right]u_l(\rho)=0$$
For $\rho\to0$, the $\rho^2$ term dominates, and so we can approximate it as
$$\begin{align}
\dfrac{d^2u_l}{d\rho^2}-\left[\dfrac{l(l+1)-(Z\alpha)^2}{\rho^2}\right]u_l(\rho)&\approx0
\end{align}$$
Suppose $u_l=\rho^{k}$, then
$$\begin{align}
k(k-1)\rho^{k-2}-\left[l(l+1)-(Z\alpha)^2\right]\rho^{k-2}&=0
&\implies&&
k^2-k-\left[l(l+1)-(Z\alpha)^2\right]&=0
\end{align}$$
Using the quadratic equation, the condition for $k$ is that
$$\begin{align}
k&=\dfrac{1}{2}\pm\sqrt{\dfrac{1}{4}+\left[l(l+1)-(Z\alpha)^2\right]}
\end{align}$$
Lastly, $l^2+l+\tfrac{1}{4}=\left(l+\tfrac{1}{2}\right)^2$, and so finally we have
$$\begin{align}
\Aboxed{k=k_\pm=\dfrac{1}{2}\pm\sqrt{\left(l+\dfrac{1}{2}\right)^2-\left(Z\alpha\right)^2}}
\end{align}$$
Using this equation in conjunction with the wavefunction ansatz, we see that
$$\begin{align}
\psi&\sim\dfrac{u_l(r)}{r}=\dfrac{r^{k}}{r}=r^{\tfrac{1}{2}\pm\sqrt{\left(l+\tfrac{1}{2}\right)^2-\left(Z\alpha\right)^2}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


The probability density in the radial component scales as $r^2|\psi|^2$, of order
$$\begin{align}
p\sim r^2(r^{k-1})^2\sim r^{2k}
\end{align}$$
For this to be finite, $2k>-1$. From our equation for $k$, $k_+$ is minimally $1/2$, which means it satisfies so long as $Z\alpha\not\ge l+1/2$. However, for $k_-$, its maximum value is $1/2$, so it will fail to converge for any choice of our system parameters. Thus, only $k_+$ is physically relevant.

For the Kinetic energy, however, this scales by $r^2|\vec\nabla\psi|^2$, of order
$$\begin{align}
K\sim r^2(r^{k-2})^2\sim r^{2k-2}
\end{align}$$
So for Kinetic energy to converge to reality, we have that $2k>+1$ which, for the same reasons as above, only $k_+$ can satisfy to converge so long as not in the extremal limit.

As for the non-relativistic limit, $Z\alpha\ll1$. If we rewrite $k_+$ in the form
$$\begin{align}
k_+=\dfrac{1}{2}+\left(l+\dfrac{1}{2}\right)\sqrt{1-\left(\dfrac{Z\alpha}{l+\tfrac{1}{2}}\right)^2}
\end{align}$$
Then in the small $Z\alpha$ limit, we have the approximation
$$\begin{align}
k_+\approx\dfrac{1}{2}+\left(l+\dfrac{1}{2}\right)=l+1
&\implies&&
\Aboxed{u_l(\rho)\sim \rho^{l+1}e^{-\rho/2}}
\end{align}$$
This has the same form as the hydrogen atom from non-relativistic quantum mechanics, and so will have the same form for the kinetic energy (or at least is proportional to it).


<div style="page-break-before: always;"></div>*PDF next page*

### Problem 3.C
> Determine the recurrence relation among the $c_i$ for this to be a solution of the Klein-Gordon equation, and show that unless the power series terminates, the wave function will have an incorrect asymptotic form.

Assume that we have the equation
$$\begin{align}
\dfrac{d^2u_l}{d\rho^2}+\left[\dfrac{2EZ\alpha}{\gamma\rho}-\dfrac{1}{4}-\dfrac{l(l+1)-(Z\alpha)^2}{\rho^2}\right]u_l(\rho)&=0
\end{align}$$
The associated derivatives from the power series sequence are
$$\begin{align}
\dfrac{du_l}{d\rho}=\dfrac{d}{d\rho}\sum_{n=0}^\infty c_n\rho^{n+k}e^{-\rho/2}
&=\sum_{n=0}^\infty c_n\left(\dfrac{n+k}{\rho}-\dfrac{1}{2}\right)\rho^{n+k}e^{-\rho/2}\\
\dfrac{d^2u_l}{d\rho^2}=\dfrac{d^2}{d\rho^2}\sum_{n=0}^\infty c_n\rho^{n+k}e^{-\rho/2}
&=\sum_{n=0}^\infty c_n\left(\dfrac{(n+k)(n+k-1)}{\rho^2}-\dfrac{n+k}{\rho}+\dfrac{1}{4}\right)\rho^{n+k}e^{-\rho/2}
\end{align}$$
The second derivative as a series is
$$\begin{align}
u_l''(\rho)&=\sum_{n=0}^\infty c_n(n+k)(n+k-1)\rho^{n+k-2}e^{-\rho/2}-\sum_{n=0}^\infty c_n(n+k)\rho^{n+k-1}e^{-\rho/2}+\dfrac{1}{4}u_l(\rho)
\end{align}$$
Substituting this into our radial equation, we have the series summation expansion
$$\begin{align}
\sum_{n=0}^\infty c_n(n+k)(n+k-1)\rho^{n+k-2}e^{-\rho/2}-\sum_{n=0}^\infty c_n(n+k)\rho^{n+k-1}e^{-\rho/2}+\left[\dfrac{a}{\rho}-\dfrac{b}{\rho^2}\right]\sum_{n=0}^\infty c_n\rho^{n+k}e^{-\rho/2}=0
\end{align}$$
$$\begin{align}
a&=\dfrac{2EZ\alpha}{\gamma} & b&=l(l+1)-(Z\alpha)^2
\end{align}$$
Reindexing the summations to be of the same power in $\rho$ and diving the exponential terms, we get
$$\begin{align}
\sum_{n=0}^\infty c_n(n+k)(n+k-1)\rho^{n+k-2}
&=\sum_{n=-2}^\infty c_{n+2}(n+k+2)(n+k+1)\rho^{n+k}\\
\sum_{n=0}^\infty c_n(n+k)\rho^{n+k-1}
&=\sum_{n=-1}^\infty c_{n+1}(n+k+1)\rho^{n+k}\\
\dfrac{a}{\rho}\sum_{n=0}^\infty c_n\rho^{n+k}
&=\sum_{n=-1}^\infty ac_{n+1}\rho^{n+k}\\
\dfrac{b}{\rho^2}\sum_{n=0}^\infty c_n\rho^{n+k}
&=\sum_{n=-2}^\infty bc_{n+2}\rho^{n+k}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


All together, dividing all $\rho^{n+k}$ and removing the summations, we get the following recursions
$$\begin{align}
\left[k(k-1)-b\right]c_{0}&=0\\
c_{n+2}\left[(n+k+2)(n+k+1)-b\right]
-c_{n+1}\left[(n+k+1)-a\right]&=0
\end{align}$$
We can do one last reindexing, $n\to n-1$, and $b=k(k-1)$ to get the recursion relation
$$\begin{align}
c_{n+1}
&=\dfrac{(n+k)-a}{(n+k+1)(n+k)-k(k-1)}c_{n}
\end{align}$$
We also have that $k(k-1)=l(l+1)-(Z\alpha)^2$, but substituting that in makes the system pretty hard to work with, so it is left in its form with $k$. Instead, if we expand, collect, and recontract, we actually get an easier expression of the form
$$\begin{align}
\Aboxed{c_{n+1}&=\dfrac{(n+k)-a}{(n+1)(n+2k)}c_{n}} & a&=\dfrac{2EZ\alpha}{\gamma} & b&=l(l+1)-(Z\alpha)^2
\end{align}$$
Asymptotically, as $n\to\infty$, the term approaches the ratio
$$\begin{align}
\lim_{n\to\infty}c_{n+1}&=\lim_{n\to\infty}\dfrac{(n+k)-a}{(n+1)(n+2k)}c_{n}\sim\dfrac{n}{n^2}c_{n}\sim\dfrac{1}{n}c_{n}
\end{align}$$
Therefore, at large values of $n$, it scales as $c_n\sim\tfrac{1}{n!}$. Replacing this into our power series equation, we have that our radial equation scales like
$$\begin{align}
u_l\sim\sum_{n=0}^\infty\left(\dfrac{1}{n!}\right)\rho^{n+k}e^{-\rho/2}=e^{\rho}e^{-\rho/2}\sim\Aboxed{e^{+\rho/2}}
\end{align}$$
Thus it will not converge when integrating from $0$ to $\infty$. In order for it to converge, it must have a finite expansion (series terminates) in order to converge to a real number.


<div style="page-break-before: always;"></div>*PDF next page*

### Problem 3.D
> Where the series terminates, show that the energy eigenvalue for the $k_+$ solution is $$E=m\left[1+\dfrac{(Z\alpha)^2}{\left(n-l-\tfrac{1}{2}+\sqrt{\left(l+\tfrac{1}{2}\right)^2-(Z\alpha)^2}\right)^2}\right]^{-1/2}$$where $n$ is the principal quantum number.

From [[#Problem 3.C|part C]], the series terminates when
$$\begin{align}
n'+k-a=n'+k-\dfrac{2EZ\alpha}{\gamma}&=0
&\implies&&
n'+k&=\dfrac{2EZ\alpha}{\gamma}
\end{align}$$
Using the definition of $\gamma=2\sqrt{m^2-E^2}$, we can do some arithmetic to solve for energy.
$$\begin{align}
\dfrac{2EZ\alpha}{2\sqrt{m^2-E^2}}&=n'+k
&\implies&&
\Aboxed{E&=m\left[1+\dfrac{(Z\alpha)^2}{(n'+k)^2}\right]^{-1/2}}
\end{align}$$
From [[#Problem 3.B|part B]], we know the form for $k=k_+$, which gives us
$$\begin{align}
k_+&=\dfrac{1}{2}+\sqrt{\left(l+\dfrac{1}{2}\right)^2-\left(Z\alpha\right)^2}
\end{align}$$
In order for it to match the solution we want to see, let $n=n'+l+1$. Therefore
$$\begin{align}
n'+k_+&=n-l-1+\dfrac{1}{2}+\sqrt{\left(l+\dfrac{1}{2}\right)^2-\left(Z\alpha\right)^2}=n-l-\dfrac{1}{2}+\sqrt{\left(l+\dfrac{1}{2}\right)^2-\left(Z\alpha\right)^2}
\end{align}$$
All together, the energy is
$$\begin{align}
\Aboxed{E=m\left[1+\dfrac{(Z\alpha)^2}{\left(n-l-\tfrac{1}{2}+\sqrt{\left(l+\tfrac{1}{2}\right)^2-(Z\alpha)^2}\right)^2}\right]^{-1/2}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Problem 3.E
> Expand $E$ in powers of $(Z\alpha)^2$ and show that the first-order term yields the Bohr formula. Connect the higher-order terms with relativistic corrections, and discuss the degree to which the degeneracy in $l$ is removed.

The equation for energy is
$$\begin{align}
E&=m\left(1+(Z\alpha)^2\left[n-l-\tfrac{1}{2}+\sqrt{(l+\tfrac{1}{2})^2-(Z\alpha)^2}\right]^{-2}\right)^{-1/2}
\end{align}$$
The first 3 terms of the Taylor series expansion of  $\dfrac{1}{\sqrt{1+x}}$ expanding around $x=0$ are
$$\begin{align}
\dfrac{1}{\sqrt{1+x}}&=1-\dfrac{1}{2}x+\dfrac{3}{8}x^2-\dfrac{5}{16}x^3+O(x^3)
\end{align}$$
In these expansions, $Z\alpha$ tends to be small. We will neglect the term inside the square root in the denominator. Applying both to our energy, we get that
$$\begin{align}
E&\approx m-\dfrac{1}{2}m\left(\dfrac{Z\alpha}{n}\right)^2+\dfrac{3}{8}m\left(\dfrac{Z\alpha}{n}\right)^4-\dfrac{5}{16}m\left(\dfrac{Z\alpha}{n}\right)^6
\end{align}$$
The first-order term is familiar. Writing it more explicitly
$$\begin{align}
\Aboxed{E^{(1)}&\approx-\dfrac{1}{2}\dfrac{mZ^2\alpha^2}{n^2}=-\dfrac{me^4}{32\pi^2\epsilon_0^2\hbar^2}\dfrac{Z^2}{n^2}}
\end{align}$$
This looks familiar and I think it is exactly the same as the Bohr formula.


<div style="page-break-before: always;"></div>*PDF next page*

### Problem 3.F
> After obtaining the theoretical exact formula, at the end of the problem, to be specific, for comparison with experimental numbers of a $\pi$-mesonic atom for $^{59}\text{Co}$ use these values: $Z=27$, $m=139.57\text{ MeV}$, and consider the $3\text{d}\to\text{2p}$ transition. 
> 
> Keep everything in MeV (and express your final numerical answer in KeV) believe me it's the easiest. To get the most accurate theoretical prediction using your exact Klein-Gordon result, you should employ the reduced mass of the $\pi$-meson & nucleus system; the mass of the nucleus is $M=54895.9392\text{ MeV}$.

We start with the energy equation
$$\begin{align}
E=m\left[1+\dfrac{(Z\alpha)^2}{\left(n-l-\tfrac{1}{2}+\sqrt{\left(l+\tfrac{1}{2}\right)^2-(Z\alpha)^2}\right)^2}\right]^{-1/2}
\end{align}$$
For mass $m=139.57\text{ MeV}$, the energy of each state is
$$\begin{align}
E_\text{3d}=E_{n=3}^{l=2}&=139.2682\text{ MeV} &&&
E_\text{2p}=E_{n=2}^{l=1}&=138.8885\text{ MeV}
\end{align}$$
The energy of transition is the difference of these energies
$$\begin{align}
\Aboxed{E_{\text{3d}\to\text{2p}}&=379.7446\text{ KeV}}
\end{align}$$
If instead we use the reduced mass (harmonic mean mass), where $m=139.22\text{ MeV}$, we get
$$\begin{align}
E_\text{3d}=E_{n=3}^{l=2}&=138.9151\text{ MeV} &&&
E_\text{2p}=E_{n=2}^{l=1}&=138.5363\text{ MeV}
\end{align}$$
With the new energy of transition being, instead,
$$\begin{align}
\Aboxed{E_{\text{3d}\to\text{2p}}&=378.7815\text{ KeV}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

## Problem 4
> Expand the energy eigenvalues given by $(8.150)$ in powers of $(Z\alpha)^2$ and show that the result is equivalent to including the relativistic correction to kinetic energy $(5.104)$ and the spin-orbit interaction $(5.125)$ to the nonrelativistic energy eigenvalues for the one electron atom $(8.151)$.

The energy given in the problem is
$$\begin{align}
E&=mc^2\left[1+\dfrac{(Z\alpha)^2}{\left(n'+\sqrt{\left(j+\tfrac{1}{2}\right)^2-(Z\alpha)^2}\right)^2}\right]^{-1/2}
\end{align}$$
Our three results we want to see have a highest order of $(Z\alpha)^4$, so can truncate expansion earlier. I will also use $\lambda=j+\tfrac{1}{2}$ to simplify the expression a little, and keep $n'=n-\lambda$. We first expand the square root on the inside
$$\begin{align}
\sqrt{\lambda^2-(Z\alpha)^2}=\lambda\sqrt{1-\dfrac{(Z\alpha)^2}{\lambda^2}}\approx\lambda-\dfrac{(Z\alpha)^2}{2\lambda}-\dfrac{(Z\alpha)^4}{8\lambda^3}
\end{align}$$
Adding in $n'=n-\lambda$ with its value, we get that
$$\begin{align}
n'+\sqrt{\lambda^2-(Z\alpha)^2}&\approx n-\dfrac{(Z\alpha)^2}{2\lambda}-\dfrac{(Z\alpha)^4}{8\lambda^3}
\end{align}$$
We need to now invert the denominator as an expansion as well
$$\begin{align}
\dfrac{1}{\left(n-\dfrac{(Z\alpha)^2}{2\lambda}-\dfrac{(Z\alpha)^4}{8\lambda^3}\right)^2}&\approx\dfrac{1}{n^2}+\dfrac{(Z\alpha)^2}{\lambda n^3}
\end{align}$$
This is then multiplied by another $(Z\alpha)^2$ (hence the 1st order approximation), to give us
$$\begin{align}
E&=mc^2\left[1+\dfrac{(Z\alpha)^2}{n^2}+\dfrac{(Z\alpha)^4}{\lambda n^3}\right]^{-1/2}
\end{align}$$
Lastly we need one more expansion for this one-over-square-root function
$$\begin{align}
\left[1+\dfrac{(Z\alpha)^2}{n^2}+\dfrac{(Z\alpha)^4}{\lambda n^3}\right]^{-1/2}\approx 1-\dfrac{1}{2}\left(\dfrac{(Z\alpha)^2}{n^2}+\dfrac{(Z\alpha)^4}{\lambda n^3}\right)+\dfrac{3}{8}\left(\dfrac{(Z\alpha)^2}{n^2}\right)^2+O\left((Z\alpha)^6\right)
\end{align}$$
Combining like terms, this approximation becomes
$$\begin{align}
\approx 1-\dfrac{1}{2}\dfrac{(Z\alpha)^2}{n^2}-\dfrac{(Z\alpha)^4}{2n^3}\left[\dfrac{1}{\lambda}-\dfrac{3}{4n}\right]
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


Replacing this back into our energy equation, we get our final approximation
$$\begin{align}
E&=mc^2-\dfrac{1}{2}\dfrac{mc^2(Z\alpha)^2}{n^2}-\dfrac{mc^2(Z\alpha)^4}{2\lambda n^3}+\dfrac{3}{8}\dfrac{mc^2(Z\alpha)^4}{n^4}
\end{align}$$
The first two terms are the non-relativistic energy contributions
$$\begin{align}
\Aboxed{E_\text{non-rel}&=mc^2-\dfrac{1}{2}\dfrac{mc^2(Z\alpha)^2}{n^2}}
\end{align}$$
The kinetic energy term has a pretty clear $\tfrac{3}{8}$ contribution, which can be found as well
$$\begin{align}
\Aboxed{E_\text{1st-kinetic}&=\dfrac{3}{8}\dfrac{mc^2(Z\alpha)^4}{n^4}}
\end{align}$$
The last term is then just the Darwin + Spin-Orbit coupling term
$$\begin{align}
\Aboxed{E_\text{remaining}&=-\dfrac{mc^2(Z\alpha)^4}{2(j+\tfrac{1}{2})n^3}}
\end{align}$$
I forget exactly how to show the individual parts, but I know there's an "add $x$ and subtract $x$" and the two terms come out as the spin-orbit and Darwin terms respectively.
