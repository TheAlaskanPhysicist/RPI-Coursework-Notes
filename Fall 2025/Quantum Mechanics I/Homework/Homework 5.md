Author: Stanley Goodwin
Date: October 16th, 2025

---
## Question 2.10
Let $\ket{a'}$ and $\ket{a''}$ be eigenstates of a Hermitian operator $A$ with eigenvalues $a'$ and $a''$, respectively ($a'=a''$). The Hamiltonian operator is given by:
$$\begin{align}
\hat{H}&=\delta\ket{a'}\bra{a''}+\delta\ket{a''}\bra{a'}
\end{align}$$
where $\delta$ is just a real number.

---
### Question 2.10.A
Clearly, $\ket{a'}$ and $\ket{a''}$ are not eigenstates of the Hamiltonian. Write down the eigenstates of the Hamiltonian. What are their energy eigenvalues?

We can express this Hamiltonian as the following matrix expression:
$$\begin{align}
\hat{H}&=\begin{bmatrix}0&\delta\\\delta&0\end{bmatrix}
\end{align}$$
This has the same decomposition as the $S_x$ matrix:
$$\begin{align}
\lambda_1&=-\delta & \vec{\lambda_1}&=\dfrac{1}{\sqrt2}\ket{a'}-\dfrac{1}{\sqrt2}\ket{a''}\\
\lambda_2&=+\delta & \vec{\lambda_2}&=\dfrac{1}{\sqrt2}\ket{a'}+\dfrac{1}{\sqrt2}\ket{a''}
\end{align}$$
Therefore, the energy eigenvalues are:
$$\begin{align}
\Aboxed{E\in\{-\delta,+\delta\}}
\end{align}$$
---
### Question 2.10B
Suppose the system is known to be in state $\ket{a'}$ at $t = 0$. Write down the state vector in the Schrödinger picture for $t < 0$.
$$\begin{align}
U(t;0)\ket{a'}
&=e^{-\tfrac{i}{\hbar}\hat{H}t}\dfrac{\ket{\lambda_1}+\ket{\lambda_2}}{\sqrt{2}}\\
&=\dfrac{1}{\sqrt{2}}e^{-\tfrac{i}{\hbar}\hat{H}t}\ket{\lambda_1}+\dfrac{1}{\sqrt{2}}e^{-\tfrac{i}{\hbar}\hat{H}t}\ket{\lambda_2}\\
&=\dfrac{1}{\sqrt{2}}e^{-\tfrac{i}{\hbar}E_-t}\ket{\lambda_1}+\dfrac{1}{\sqrt{2}}e^{-\tfrac{i}{\hbar}E_+t}\ket{\lambda_2}\\
\Aboxed{\ket{a'; t}&=\dfrac{1}{\sqrt2}e^{+\tfrac{i}{\hbar}\delta t}\ket{\lambda_1}+\dfrac{1}{\sqrt2}e^{-\tfrac{i}{\hbar}\delta t}\ket{\lambda_2}}
\end{align}$$
---
### Question 2.10.C
What is the probability for finding the system in $\ket{a''}$ for $t < 0$ if the system is known to be in state $\ket{a'}$ at $t = 0$?
$$\begin{align}
\left|\braket{a''|a'; t}\right|^2&=\left|\left(\dfrac{1}{\sqrt2}\bra{\lambda_1}-\dfrac{1}{\sqrt2}\bra{\lambda_2}\right)\left(\dfrac{1}{\sqrt2}e^{+\tfrac{i}{\hbar}\delta t}\ket{\lambda_1}+\dfrac{1}{\sqrt2}e^{-\tfrac{i}{\hbar}\delta t}\ket{\lambda_2}\right)\right|^2\\
&=\left|\left(\dfrac{1}{2}e^{+\tfrac{i}{\hbar}\delta t}-\dfrac{1}{2}e^{-\tfrac{i}{\hbar}\delta t}\right)\right|^2\\
&=\dfrac{1}{4}\left(e^{-\tfrac{i}{\hbar}\delta t}-e^{+\tfrac{i}{\hbar}\delta t}\right)\left(e^{+\tfrac{i}{\hbar}\delta t}-e^{-\tfrac{i}{\hbar}\delta t}\right)\\
&=\dfrac{1}{4}\left(2-2\dfrac{e^{+2\tfrac{i}{\hbar}\delta t}+e^{-2\tfrac{i}{\hbar}\delta t}}{2}\right)\\
&=\dfrac{1}{2}\left(1-\cos\left(\tfrac{2\delta t}{\hbar}\right)\right)\\
\Aboxed{P(\ket{a'; t}&=\sin^2\left(\tfrac{\delta}{\hbar}t\right)}
\end{align}$$
---
### Question 2.10.D
Can you think of a physical situation corresponding to this problem?

This looks like the $S_x$ matrix, and so a spin-$1/2$ particle in a uniform, static, magnetic field pointed in the X-axis is probably a system of these characteristics.

At $t=0$, it's in the Z Spin-Up ($\chi_+^z$) state, and our measurements are happening in the $X$ basis.

I.e. A particle with spin in a magnetic field $\vec{B}=B_0\hat{x}$, with the $t=0$ state being $\ket{\chi_+^z}$.

---
## Question 2.14
Consider a particle subject to a one-dimensional simple harmonic oscillator potential. Suppose at $t=0$ the state vector is given by:
$$\begin{align}
\ket{\psi(0)}&=\exp\left(-i\dfrac{\hat{p}}{\hbar}a\right)\ket{0}
\end{align}$$
where $p$ is the momentum operator, $a$ is some number with dimension of length, and the state $\ket0$ is the one for which $\braket{x}=\braket{p}=0$. Using the Heisenberg picture, evaluate the expectation value $\braket{x}$ for $t\ge 0$.

The Heisenberg picture is when the operator itself is time-evolved, and from lecture, we know that:
$$\begin{align}
\hat{x}(t)&=\cos(\omega t)\hat{x}+\dfrac{1}{m\omega}\sin(\omega t)\hat{p}
\end{align}$$
To find the expected value of $x(t)$, we have the expression:
$$\begin{align}
\braket{x}(t)&=\bra{\psi}\hat{x}\ket{\psi}\\
&=\left(\bra{0}e^{+i\tfrac{\hat{p}}{\hbar}a}\right)\left(\cos(\omega t)\hat{x}+\dfrac{1}{m\omega}\sin(\omega t)\hat{p}\right)\left(e^{-i\tfrac{\hat{p}}{\hbar}a}\ket{0}\right)\\
&=\cos(\omega t)\bra{0}\left(e^{+i\tfrac{\hat{p}}{\hbar}a}\right)\hat{x}\left(e^{-i\tfrac{\hat{p}}{\hbar}a}\right)\ket{0}+\dfrac{1}{m\omega}\sin(\omega t)\bra{0}\left(e^{+i\tfrac{\hat{p}}{\hbar}a}\right)\hat{p}\left(e^{-i\tfrac{\hat{p}}{\hbar}a}\right)\ket{0}\\
\end{align}$$
We need to show the translation operators acting on $\hat{x}$ and $\hat{p}$, and so:
$$\begin{align}
T^\dagger\hat{x} T&=e^{+i\tfrac{\hat{p}}{\hbar}a}\hat{x}e^{-i\tfrac{\hat{p}}{\hbar}a}\\
&=e^{+i\tfrac{\hat{p}}{\hbar}a}\cdot\left(\left[\hat{x},e^{-i\tfrac{\hat{p}}{\hbar}a}\right]+e^{-i\tfrac{\hat{p}}{\hbar}a}\hat{x}\right)\\
&=e^{+i\tfrac{\hat{p}}{\hbar}a}\cdot ae^{-i\tfrac{\hat{p}}{\hbar}a}+e^{+i\tfrac{\hat{p}}{\hbar}a}e^{-i\tfrac{\hat{p}}{\hbar}a}\hat{x}\\
\Aboxed{T^\dagger\hat{x} T&=\hat{x}+a}
\end{align}$$
$$\begin{align}
T^\dagger\hat{p} T&=e^{+i\tfrac{\hat{p}}{\hbar}a}\hat{p}e^{-i\tfrac{\hat{p}}{\hbar}a}\\
&=e^{+i\tfrac{\hat{p}}{\hbar}a}\cdot\left(\left[\hat{p},e^{-i\tfrac{\hat{p}}{\hbar}a}\right]+e^{-i\tfrac{\hat{p}}{\hbar}a}\hat{p}\right)\\
&=e^{+i\tfrac{\hat{p}}{\hbar}a}\cdot\left(0+e^{-i\tfrac{\hat{p}}{\hbar}a}\hat{p}\right)\\
&=e^{+i\tfrac{\hat{p}}{\hbar}a}e^{-i\tfrac{\hat{p}}{\hbar}a}\cdot\hat{p}\\
\Aboxed{T^\dagger\hat{p} T&=\hat{p}}
\end{align}$$
Therefore, we can then continue the derivation:
$$\begin{align}
\braket{x}(t)&=\cos(\omega t)\bra{0}\left(e^{+i\tfrac{\hat{p}}{\hbar}a}\right)\hat{x}\left(e^{-i\tfrac{\hat{p}}{\hbar}a}\right)\ket{0}+\dfrac{1}{m\omega}\sin(\omega t)\bra{0}\left(e^{+i\tfrac{\hat{p}}{\hbar}a}\right)\hat{p}\left(e^{-i\tfrac{\hat{p}}{\hbar}a}\right)\ket{0}\\
&=\cos(\omega t)\bra{0}(T^\dagger\hat{x}T)\ket{0}+\dfrac{1}{m\omega}\sin(\omega t)\bra{0}(T^\dagger\hat{p}T)\ket{0}\\
&=\cos(\omega t)\bra{0}(\hat{x}+a)\ket{0}+\dfrac{1}{m\omega}\sin(\omega t)\bra{0}\hat{p}\ket{0}\\
&=a\cos(\omega t)\braket{0|0}+\cos(\omega t)\bra{0}\hat{x}\ket{0}+\dfrac{1}{m\omega}\sin(\omega t)\bra{0}\hat{p}\ket{0}\\
&=a\cos(\omega t)+\cos(\omega t)\braket{\hat{x}}+\dfrac{1}{m\omega}\sin(\omega t)\braket{\hat{p}}\\
&=a\cos(\omega t)+\cos(\omega t)\cdot0+\dfrac{1}{m\omega}\sin(\omega t)\cdot0\\
\Aboxed{\braket{x}(t)&=a\cos(\omega t), t\ge0}
\end{align}$$
---
## Question 2.15
### Question 2.15.A
Write down the wave function (in coordinate space) for the state specified in Problem 2.14 at $t = 0$. You may use:
$$\begin{align}
\braket{x'|0}&=\pi^{-1/4}x_0^{-1/2}\exp\left[-\dfrac{1}{2}\left(\dfrac{x'}{x_0}\right)^2\right] & x_0&\equiv\left(\dfrac{\hbar}{m\omega}\right)^{1/2}
\end{align}$$
The good old trick of inserting an identity matrix $\mathbb{I}$ comes in handy:
$$\begin{align}
\braket{x'|\psi(0)}&=\bra{x'}T(a)\ket{0}\\
&=\int\bra{x'}T(a)\ket{x}\braket{x|0}\ dx\\
&=\int\braket{x'|x+a}\braket{x|0}\ dx\\
&=\int\delta_{x',x+a}\braket{x|0}\ dx\\
&=\braket{x'-a|0}\\
\end{align}$$
Rearrangement also works (applying the translation backwards):
$$\begin{align}
\braket{x'|\psi(0)}&=\bra{x'}T(a)\ket{0}\\
&=\left(\bra{x'}T(a)\right)^{\dagger\dagger}\ket{0}\\
&=\left(T^\dagger(a)\ket{x'}\right)^{\dagger}\ket{0}\\
&=\left(\ket{x'-a}\right)^{\dagger}\ket{0}\\
&=\braket{x'-a|0}\\
\end{align}$$
We know the form of the solution given to us by the question, and so using $x'\rightarrow x'-a$, then:
$$\begin{align}
\Aboxed{\braket{x'|\psi(0)}&=\pi^{-1/4}x_0^{-1/2}\exp\left[-\dfrac{1}{2}\left(\dfrac{x'-a}{x_0}\right)^2\right]}
\end{align}$$
---
### Question 2.15.B
Obtain a simple expression for the probability that the state is found in the ground state at $t = 0$. Does this probability change for $t > 0$?
$$\begin{align}
\ket{\psi(t)}&=U(t)T(a)\ket{0}
\end{align}$$
We can use a clever trick to get this inner product:
$$\begin{align}
\braket{0|\psi(t)}&=\bra{0}U(t)T(a)\ket{0}\\
&=\bra{0}e^{-i\hat{H}t/\hbar}e^{-i\hat{p}a/\hbar}\ket{0}\\
&=\bra{0}e^{-iE_0t/\hbar}e^{-i\hat{p}a/\hbar}\ket{0}\\
&=\iint\braket{0|x'}\bra{x'}e^{-iE_0t/\hbar}e^{-i\hat{p}a/\hbar}\ket{x''}\braket{x''|0}\ dx' dx''\\
&=\iint\braket{0|x'}\bra{x'}e^{-iE_0t/\hbar}\ket{x''+a}\braket{x''|0}\ dx' dx''\\
&=(\pi^{-1/4}x_0^{-1/2})^2\iint\exp\left[-\dfrac{1}{2}\left(\dfrac{x'-a}{x_0}\right)^2\right]\bra{x'}e^{-iE_0t/\hbar}\ket{x'+a}\exp\left[-\dfrac{1}{2}\left(\dfrac{x''-a}{x_0}\right)^2\right]\ dx' dx''\\
&=\dfrac{1}{x_0\sqrt\pi}\iint e^{-iE_0t/\hbar}\exp\left[-\dfrac{1}{2}\left(\dfrac{x'-a}{x_0}\right)^2-\dfrac{1}{2}\left(\dfrac{x''-a}{x_0}\right)^2\right]\braket{x'|x''+a}\ dx' dx''\\
&=\dfrac{1}{x_0\sqrt\pi}\iint e^{-iE_0t/\hbar}\exp\left[-\dfrac{1}{2}\left(\dfrac{x''+a-a}{x_0}\right)^2-\dfrac{1}{2}\left(\dfrac{x''-a}{x_0}\right)^2\right]\ dx''\\
&=\dfrac{1}{x_0\sqrt\pi}\iint e^{-iE_0t/\hbar}\exp\left[-\dfrac{1}{2}\left(\dfrac{x''}{x_0}\right)^2-\dfrac{1}{2}\left(\dfrac{x''-a}{x_0}\right)^2\right]\ dx''\\
&=\dfrac{1}{x_0\sqrt\pi}e^{-iE_0t/\hbar}\sqrt{\dfrac{\pi}{2\tfrac{1}{2x_0^2}}}\exp\left[-\dfrac{a^2}{4x_0^2}\right]\\
&=e^{-iE_0t/\hbar}\exp\left[-\dfrac{a^2}{4x_0^2}\right]\\
\Aboxed{\braket{0|\psi(t)}&=e^{-iE_0t/\hbar}\exp\left[-\dfrac{m\omega a^2}{4\hbar}\right]}
\end{align}$$
To find the probability of the state in $\ket{0}$, we take its inner product squared, and so:
$$\begin{align}
\braket{0|\psi(t)}&=e^{-iE_0t/\hbar}\exp\left[-\dfrac{m\omega a^2}{4\hbar}\right]\\
|\braket{0|\psi(t)}|^2&=\left|e^{-iE_0t/\hbar}\right|^2\exp\left[-\dfrac{m\omega a^2}{4\hbar}\cdot 2\right]\\
\Aboxed{P_{\psi=\ket{0}}(t)&=\exp\left[-\dfrac{m\omega a^2}{2\hbar}\right]}
\end{align}$$
---
## Question 2.34
A particle of mass $m$ moves in one dimension $x$ under a potential energy $V(x)$.
### Question 2.34.A
For $V(x)=-V_0b\ \delta(x)$, $V_0>0$, $b > 0$, find the bound-state eigenvalue $E$.
$$\begin{align}
-\dfrac{\hbar^2}{2m}\dfrac{\partial^2}{\partial x^2}\psi(x,t) + V(x)\psi(x,t)&=E\psi(x,t)
\end{align}$$
Substituting our potential, we get:
$$\begin{align}
-\dfrac{\hbar^2}{2m}\dfrac{\partial^2}{\partial x^2}\psi(x,t) -V_0b\ \delta(x)\psi(x,t)&=E\psi(x,t)
\end{align}$$
For the case where $x\ne0$, then $\psi$ is that of a free particle, and so:
$$\begin{align}
-\dfrac{\hbar^2}{2m}\dfrac{\partial^2}{\partial x^2}\psi(x,t)&=E\psi(x,t)\\
\dfrac{\partial^2}{\partial x^2}\psi(x,t)&=-\dfrac{2mE}{\hbar^2}\psi(x,t)\\
\end{align}$$
This is an ODE with a very simple solution. Let $k=\sqrt{\dfrac{2mE}{\hbar^2}}$, and so:
$$\begin{align}
\psi(x,t)&=Ae^{ikx}+Be^{-ikx}
\end{align}$$
To classify the behavior between both sides, we can see that:
$$\begin{align}
\psi_+(x,t)&=A_+e^{ikx}+B_+e^{-ikx}\\
\psi_-(x,t)&=A_-e^{ikx}+B_-e^{-ikx}\\
\end{align}$$
Over the discontinuity, we have to do a bit of a trick. Integrate both sides over a small domain around the discontinuity, $x=x_0-\epsilon$ and $x=x_0+\epsilon$. This might have a discontinuous derivative, but we can still find a continuity in $\psi(x,t)$:
$$\begin{align}
-\dfrac{\hbar^2}{2m}\int_{-\epsilon}^{+\epsilon}\dfrac{\partial^2}{\partial x^2}\psi(x,t)\ dx + \int_{-\epsilon}^{+\epsilon}V(x)\psi(x,t)\ dx&=E\int_{-\epsilon}^{+\epsilon}\psi(x,t)\ dx\\
-\dfrac{\hbar^2}{2m}\left.\dfrac{\partial\psi(x,t)}{\partial x}\right|_{-\epsilon}^{+\epsilon}-V_0b\int_{-\epsilon}^{+\epsilon}\delta(x)\ \psi(x,t)\ dx&=E\int_{-\epsilon}^{+\epsilon}\psi(x,t)\ dx
\end{align}$$
We can extend the integral for the delta function, since it's adding a bunch of zeros, and so:
$$\begin{align}
-\dfrac{\hbar^2}{2m}\left.\dfrac{\partial\psi(x,t)}{\partial x}\right|_{-\epsilon}^{+\epsilon}-V_0b\ \psi(0,t)&=E\int_{-\epsilon}^{+\epsilon}\psi(x,t)\ dx
\end{align}$$
Take the limit of both sides for $\epsilon\rightarrow0$, then:
$$\begin{align}
-\dfrac{\hbar^2}{2m}\lim_{\epsilon\rightarrow0}\left.\dfrac{\partial\psi(x,t)}{\partial x}\right|_{-\epsilon}^{+\epsilon}-V_0b\ \psi(0,t)&=\lim_{\epsilon\rightarrow0}E\int_{-\epsilon}^{+\epsilon}\psi(x,t)\ dx\\
-\dfrac{\hbar^2}{2m}\left(\left.\dfrac{\partial\psi(x,t)}{\partial x}\right|_{x=\epsilon}-\left.\dfrac{\partial\psi(x,t)}{\partial x}\right|_{x=-\epsilon}\right)-V_0b\ \psi(0,t)&=0\\
\left.\dfrac{\partial\psi(x,t)}{\partial x}\right|_{x=\epsilon}-\left.\dfrac{\partial\psi(x,t)}{\partial x}\right|_{x=-\epsilon}&=-\dfrac{2mV_0}{\hbar^2}b\ \psi(0,t)\\
\Aboxed{\lim_{x\rightarrow 0^+}\dfrac{\partial\psi(x,t)}{\partial x}-\lim_{x\rightarrow 0^-}\dfrac{\partial\psi(x,t)}{\partial x}&=-\dfrac{2mV_0}{\hbar^2}b\ \psi(0,t)}
\end{align}$$
Using our expressions for both sides, we can then see:









$$\begin{align}
\lim_{x\rightarrow 0^+}\dfrac{\partial\psi(x,t)}{\partial x}-\lim_{x\rightarrow 0^-}\dfrac{\partial\psi(x,t)}{\partial x}&=-\dfrac{2mV_0}{\hbar^2}b\ \psi(0,t)\\
\lim_{x\rightarrow 0^+}\dfrac{\partial}{\partial x}\left(A_+e^{ikx}+B_+e^{-ikx}\right)-\lim_{x\rightarrow 0^-}\dfrac{\partial}{\partial x}\left(A_-e^{ikx}+B_-e^{-ikx}\right)&=-\dfrac{2mV_0}{\hbar^2}b\ \psi(0,t)\\
ik\lim_{x\rightarrow 0^+}\left(A_+e^{ikx}-B_+e^{-ikx}\right)-ik\lim_{x\rightarrow 0^-}\left(A_-e^{ikx}-B_-e^{-ikx}\right)&=-\dfrac{2mV_0}{\hbar^2}b\ \psi(0,t)\\
ik\left(A_+-B_+\right)-ik\left(A_--B_-\right)&=-\dfrac{2mV_0}{\hbar^2}b\ \psi(0,t)\\
A_+-B_+-A_-+B_-&=i\dfrac{2mV_0}{\hbar^2k}b\ \psi(0,t)\\
\end{align}$$








### Question 2.34.B
Generalize this to the double delta-function potential:
$$\begin{align}
V(x)&=-V_0\dfrac{b}{2}\left[\delta\left(x+\dfrac{a}{2}\right)+\delta\left(x-\dfrac{a}{2}\right)\right]
\end{align}$$
and bound the bound-state energy eigenvalues and plot the corresponding eigenfunctions. Also show that you get the expected results as $a\rightarrow0$.


