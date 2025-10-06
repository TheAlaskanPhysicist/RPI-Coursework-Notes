Author: Stanley Goodwin
Date: October 6th, 2025

Read Feynman Lectures, 3rd Volume, Chapter 16.

---
## Question 2.12
A one-dimensional simple harmonic oscillator with natural frequency $\omega$ is in initial state:
$$\begin{align}
\ket\alpha&=\dfrac{1}{\sqrt2}\ket{0}+\dfrac{e^{i\delta}}{\sqrt2}\ket{1}
\end{align}$$
where $\delta$ is a real number.
$$\begin{align}
\hat{H}&=\dfrac{\hat{p}^2}{2m}+\dfrac{1}{2}m\omega^2\hat{x}^2\\
\hat{H}\ket{n}&=\left(n+\dfrac{1}{2}\right)\hbar\omega\\
U(t)&=e^{-i\hat{H}t/\hbar}
\end{align}$$
---
### Question 2.12.A
Find the time-dependent wave function $\braket{x'|\alpha; t}$ and evaluate the (time-dependent) expectation values $\braket{x}$ and $\braket{p}$ in the state $\ket{\alpha; t}$, i.e. in the Schrödinger picture.

Not sure why we need this, but I calculated it anyways:
$$\begin{align}
\braket{x'|\alpha; t}&=\bra{x'}U(t)\ket{\alpha}\\
&=\bra{x'}e^{-i\hat{H}t/\hbar}\left(\dfrac{1}{\sqrt2}\ket{0}+\dfrac{e^{i\delta}}{\sqrt2}\ket{1}\right)\\
&=\bra{x'}\left(\dfrac{1}{\sqrt2}e^{-i(\tfrac{1}{2}\hbar\omega)t/\hbar}\ket{0}+\dfrac{e^{i\delta}}{\sqrt2}e^{-i(\tfrac{3}{2}\hbar\omega)t/\hbar}\ket{1}\right)\\
&=\dfrac{e^{-i\tfrac{1}{2}\omega t}}{\sqrt{2}}\bra{x'}\left(\ket{0}+e^{i\delta}e^{-i\omega t}\ket{1}\right)\\
\Aboxed{\braket{x'|\alpha; t}&=\dfrac{e^{i\tfrac{1}{2}\omega t}}{\sqrt{2}}\left(\braket{x'|0}+e^{i(\delta-\omega t)}\braket{x'|1}\right)}\\
\Aboxed{\braket{\alpha; t|x'}&=\dfrac{e^{-i\tfrac{1}{2}\omega t}}{\sqrt{2}}\left(\braket{0|x'}+e^{-i(\delta-\omega t)}\braket{1|x'}\right)}
\end{align}$$
We need the operators for $\hat{x}$ and $\hat{p}$, so:
$$\begin{align}
&&a&=\sqrt{\dfrac{m\omega}{2\hbar}}\left(\hat{x}+\dfrac{i}{m\omega}\hat{p}\right)\\
&&a^\dagger&=\sqrt{\dfrac{m\omega}{2\hbar}}\left(\hat{x}-\dfrac{i}{m\omega}\hat{p}\right)\\\\

\implies&&\hat{x}&=\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger+a\right)\\
\implies&&\hat{p}&=i\sqrt{\dfrac{\hbar m\omega}{2}}\left(a^\dagger-a\right)\\
\end{align}$$
We can then find the expected value of position as:
$$\begin{align}
\braket{x}(t)&=\bra{\alpha; t}\hat{x}\ket{\alpha;t}\\
&=\dfrac{e^{-i\tfrac{1}{2}\omega t}}{\sqrt{2}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger+a\right)\dfrac{e^{+i\tfrac{1}{2}\omega t}}{\sqrt{2}}\left(\ket{0}+e^{+i(\delta-\omega t)}\ket{1}\right)\\
&=\dfrac{1}{2}\sqrt{\dfrac{\hbar}{2m\omega}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)\left(a^\dagger+a\right)\left(\ket{0}+e^{+i(\delta-\omega t)}\ket{1}\right)\\
&=\dfrac{1}{2}\sqrt{\dfrac{\hbar}{2m\omega}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)\left(a^\dagger\ket{0}+e^{+i(\delta-\omega t)}a^\dagger\ket{1}+a\ket{0}+e^{+i(\delta-\omega t)}a\ket{1}\right)\\
&=\dfrac{1}{2}\sqrt{\dfrac{\hbar}{2m\omega}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)\left(\ket{1}+e^{+i(\delta-\omega t)}\sqrt{2}\ket{2}+0+e^{+i(\delta-\omega t)}\ket{0}\right)\\
&=\dfrac{1}{2}\sqrt{\dfrac{\hbar}{2m\omega}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)\left(e^{+i(\delta-\omega t)}\ket{0}+\ket{1}+e^{+i(\delta-\omega t)}\sqrt{2}\ket{2}\right)\\
&=\dfrac{1}{2}\sqrt{\dfrac{\hbar}{2m\omega}}\left(e^{+i(\delta-\omega t)}+0+0+0+e^{-i(\delta-\omega t)}+0\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\dfrac{1}{2}\left(e^{+i(\delta-\omega t)}+e^{-i(\delta-\omega t)}\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\cos\left(\delta-\omega t\right)\\
\Aboxed{\braket{x}(t)&=\sqrt{\dfrac{\hbar}{2m\omega}}\cos\left(\omega t-\delta\right)}
\end{align}$$
For momentum, it's very similar, so:
$$\begin{align}
\braket{p}(t)&=\bra{\alpha; t}\hat{p}\ket{\alpha;t}\\
&=\dfrac{e^{-i\tfrac{1}{2}\omega t}}{\sqrt{2}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)i\sqrt{\dfrac{\hbar m\omega}{2}}\left(a^\dagger-a\right)\dfrac{e^{+i\tfrac{1}{2}\omega t}}{\sqrt{2}}\left(\ket{0}+e^{+i(\delta-\omega t)}\ket{1}\right)\\
&=i\dfrac{1}{2}\sqrt{\dfrac{\hbar m\omega}{2}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)\left(a^\dagger-a\right)\left(\ket{0}+e^{+i(\delta-\omega t)}\ket{1}\right)\\
&=i\dfrac{1}{2}\sqrt{\dfrac{\hbar m\omega}{2}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)\left(a^\dagger\ket{0}+e^{+i(\delta-\omega t)}a^\dagger\ket{1}-a\ket{0}-e^{+i(\delta-\omega t)}a\ket{1}\right)\\
&=i\dfrac{1}{2}\sqrt{\dfrac{\hbar m\omega}{2}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)\left(\ket{1}+e^{+i(\delta-\omega t)}\sqrt{2}\ket{2}-0-e^{+i(\delta-\omega t)}\ket{0}\right)\\
&=i\dfrac{1}{2}\sqrt{\dfrac{\hbar m\omega}{2}}\left(\bra{0}+e^{-i(\delta-\omega t)}\bra{1}\right)\left(-e^{+i(\delta-\omega t)}\ket{0}+\ket{1}+e^{+i(\delta-\omega t)}\sqrt{2}\ket{2}\right)\\
&=i\dfrac{1}{2}\sqrt{\dfrac{\hbar m\omega}{2}}\left(-e^{+i(\delta-\omega t)}+0+0+0+e^{-i(\delta-\omega t)}+0\right)\\
&=\sqrt{\dfrac{\hbar m\omega}{2}}\dfrac{1}{2i}\left(e^{+i(\delta-\omega t)}-e^{-i(\delta-\omega t)}\right)\\
&=\sqrt{\dfrac{\hbar m\omega}{2}}\sin\left(\delta-\omega t\right)\\
\Aboxed{\braket{x}(t)&=-\sqrt{\dfrac{\hbar m\omega}{2}}\sin\left(\omega t-\delta\right)}
\end{align}$$
---
### Question 2.12.B
Now calculate $\braket{x}$ and $\braket{p}$ in the Heisenberg picture and compare the results.

We want to find the time evolution of the ladder operators:
$$\begin{align}
\dfrac{d}{dt}\hat{A}&=\dfrac{i}{\hbar}\left[\hat{H},\hat{A}\right]
\end{align}$$
We know the Hamiltonian is:
$$\begin{align}
\hat{H}&=\left(a^\dagger a+\dfrac{1}{2}\right)\hbar\omega
\end{align}$$
Then the commutator is as follows:
$$\begin{align}
\left[\hat{H},a(t)\right]&=\left[\left(a^\dagger a+\dfrac{1}{2}\right),a\right]\hbar\omega\\
&=\left[a^\dagger a,a\right]\hbar\omega+0\\
&=-\left[a,a^\dagger a\right]\hbar\omega\\
&=-\hbar\omega\left[a,a^\dagger\right]a-\hbar\omega a^\dagger\left[a, a\right]\\
\Aboxed{\left[\hat{H},a(t)\right]&=-\hbar\omega a(t)}
\end{align}$$
We can then see that it's a simple differential equation:
$$\begin{align}
&&\dfrac{d}{dt}a(t)&=\dfrac{i}{\hbar}\left(-\hbar\omega a(t)\right)\\
\implies&&a(t)&=ae^{-i\omega t}\\
\implies&&a^\dagger(t)&=a^\dagger e^{+i\omega t}\\
\end{align}$$
Therefore, the 2 real operators can be found as:
$$\begin{align}
\hat{x}(t)&=\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger e^{+i\omega t}+ae^{-i\omega t}\right)\\
\hat{p}(t)&=i\sqrt{\dfrac{\hbar m\omega}{2}}\left(a^\dagger e^{+i\omega t}-ae^{-i\omega t}\right)\\
\end{align}$$
Expected value is then found very similarly to the above:
$$\begin{align}
\braket{x}(t)&=\bra\alpha\hat{x}(t)\ket\alpha\\
&=\left(\dfrac{1}{\sqrt2}\bra{0}+\dfrac{e^{-i\delta}}{\sqrt2}\bra{1}\right)\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger e^{+i\omega t}+ae^{-i\omega t}\right)\left(\dfrac{1}{\sqrt2}\ket{0}+\dfrac{e^{i\delta}}{\sqrt2}\ket{1}\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\dfrac{1}{2}\left(\bra{0}+e^{-i\delta}\bra{1}\right)\left(a^\dagger e^{+i\omega t}+ae^{-i\omega t}\right)\left(\ket{0}+e^{i\delta}\ket{1}\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\dfrac{1}{2}\left(\bra{0}+e^{-i\delta}\bra{1}\right)\left(a^\dagger e^{+i\omega t}\ket{0}+e^{i\delta}a^\dagger e^{+i\omega t}\ket{1}+ae^{-i\omega t}\ket{0}+ae^{-i\omega t}e^{i\delta}\ket{1}\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\dfrac{1}{2}\left(\bra{0}+e^{-i\delta}\bra{1}\right)\left(e^{+i\omega t}\ket{1}+\sqrt{2}e^{i\delta}e^{+i\omega t}\ket{2}+0+e^{-i\omega t}e^{i\delta}\ket{0}\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\dfrac{1}{2}\left(\bra{0}+e^{-i\delta}\bra{1}\right)\left(e^{-i\omega t}e^{i\delta}\ket{0}+e^{+i\omega t}\ket{1}+\sqrt{2}e^{i\delta}e^{+i\omega t}\ket{2}\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\dfrac{1}{2}\left(e^{-i\omega t}e^{i\delta}+0+0+0+e^{-i\delta}e^{+i\omega t}+0\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\dfrac{1}{2}\left(e^{+i(\omega t-\delta)}+e^{-i(\omega t-\delta)}\right)\\
\Aboxed{\braket{x}(t)&=\sqrt{\dfrac{\hbar}{2m\omega}}\cos\left(\omega t-\delta\right)}
\end{align}$$
Same with the momentum:
$$\begin{align}
\braket{x}(t)&=\bra\alpha\hat{x}(t)\ket\alpha\\
&=\left(\dfrac{1}{\sqrt2}\bra{0}+\dfrac{e^{-i\delta}}{\sqrt2}\bra{1}\right)i\sqrt{\dfrac{\hbar m\omega}{2}}\left(a^\dagger e^{+i\omega t}+ae^{-i\omega t}\right)\left(\dfrac{1}{\sqrt2}\ket{0}+\dfrac{e^{i\delta}}{\sqrt2}\ket{1}\right)\\
&=i\sqrt{\dfrac{\hbar m\omega}{2}}\dfrac{1}{2}\left(\bra{0}+e^{-i\delta}\bra{1}\right)\left(a^\dagger e^{+i\omega t}-ae^{-i\omega t}\right)\left(\ket{0}+e^{i\delta}\ket{1}\right)\\
&=i\sqrt{\dfrac{\hbar m\omega}{2}}\dfrac{1}{2}\left(\bra{0}+e^{-i\delta}\bra{1}\right)\left(a^\dagger e^{+i\omega t}\ket{0}+e^{i\delta}a^\dagger e^{+i\omega t}\ket{1}-ae^{-i\omega t}\ket{0}-ae^{-i\omega t}e^{i\delta}\ket{1}\right)\\
&=i\sqrt{\dfrac{\hbar m\omega}{2}}\dfrac{1}{2}\left(\bra{0}+e^{-i\delta}\bra{1}\right)\left(e^{+i\omega t}\ket{1}+\sqrt{2}e^{i\delta}e^{+i\omega t}\ket{2}-0-e^{-i\omega t}e^{i\delta}\ket{0}\right)\\
&=i\sqrt{\dfrac{\hbar m\omega}{2}}\dfrac{1}{2}\left(\bra{0}+e^{-i\delta}\bra{1}\right)\left(-e^{-i\omega t}e^{i\delta}\ket{0}+e^{+i\omega t}\ket{1}+\sqrt{2}e^{i\delta}e^{+i\omega t}\ket{2}\right)\\
&=i\sqrt{\dfrac{\hbar m\omega}{2}}\dfrac{1}{2}\left(-e^{-i\omega t}e^{i\delta}+0+0+0+e^{-i\delta}e^{+i\omega t}+0\right)\\
&=-\sqrt{\dfrac{\hbar m\omega}{2}}\dfrac{1}{2i}\left(e^{+i(\omega t-\delta)}-e^{-i(\omega t-\delta)}\right)\\
\Aboxed{\braket{x}(t)&=-\sqrt{\dfrac{\hbar m\omega}{2}}\sin\left(\omega t-\delta\right)}
\end{align}$$
The same as was found in the Schrodinger picture!

---
## Question 2.18
Consider a function, known as the correlation function, defined by
$$\begin{align}
C(t)&=\braket{x(t)x(0)}
\end{align}$$
where $x(t)$ is the position operator in the Heisenberg picture. Evaluate the correlation function explicitly for the ground state of a one-dimensional simple harmonic oscillator.
$$\begin{align}
C(t)&=\braket{x(t)x(0)}\\
&=\bra{\psi}\hat{x}(t)\ket{\psi}\bra{\psi'}\hat{x}\ket{\psi'}\\
&=\bra{\psi}\hat{x}(t)\hat{x}\ket{\psi}\\
\end{align}$$
Substituting for our Heisenberg creation and annihilation operators, we get:
$$\begin{align}
C(t)&=\bra{\psi}\hat{x}(t)\hat{x}\ket{\psi}\\
&=\bra{\psi}\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger e^{+i\omega t}+ae^{-i\omega t}\right)\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger+a\right)\ket{\psi}\\
&=\dfrac{\hbar}{2m\omega}\bra{\psi}\left(a^\dagger e^{+i\omega t}+ae^{-i\omega t}\right)\left(a^\dagger+a\right)\ket{\psi}\\
&=\dfrac{\hbar}{2m\omega}\bra{\psi}\left[(a^\dagger)^2 e^{+i\omega t}+aa^\dagger e^{-i\omega t}+a^\dagger a e^{+i\omega t}+(a)^2e^{-i\omega t}\right]\ket\psi\\
\end{align}$$
We can use that we know $\ket{\psi}=\ket{0}$ since it's in the ground state, and so:
$$\begin{align}
C(t)&=\dfrac{\hbar}{2m\omega}\bra{\psi}\left[(a^\dagger)^2 e^{+i\omega t}+aa^\dagger e^{-i\omega t}+a^\dagger a e^{+i\omega t}+(a)^2e^{-i\omega t}\right]\ket\psi\\
&=\dfrac{\hbar}{2m\omega}\bra{0}\left[(a^\dagger)^2 e^{+i\omega t}\ket{0}+aa^\dagger e^{-i\omega t}\ket{0}+a^\dagger a e^{+i\omega t}\ket{0}+(a)^2e^{-i\omega t}\ket{0}\right]\\
&=\dfrac{\hbar}{2m\omega}\bra{0}\left[\sqrt{2}e^{+i\omega t}\ket{2}+e^{-i\omega t}\ket{0}+0+0\right]\\
&=\dfrac{\hbar}{2m\omega}\bra{0}e^{-i\omega t}\ket{0}\\
\Aboxed{C(t)&=\dfrac{\hbar}{2m\omega}e^{-i\omega t}}
\end{align}$$
---
## Question 2.21
The problem covers some fundamental concepts in quantum optics.
A coherent state of a one-dimensional simple harmonic oscillator is defined to be an eigenstate of the (non-Hermitian) annihilation operator $a$:
$$\begin{align}
a\ket\lambda&=\lambda\ket\lambda
\end{align}$$
where $\lambda$ is, in general, a complex number.

---
### Question 2.21.A
Prove that
$$\begin{align}
\ket\lambda&=e^{-|\lambda|^2/2}e^{\lambda a^\dagger}\ket{0}
\end{align}$$
is a normalized coherent state.
$$\begin{align}
\ket\lambda&=e^{-|\lambda|^2/2}e^{\lambda a^\dagger}\ket{0}\\
&=e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{n!}(a^\dagger)^n\ket{0}\\
&=e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{n!}\sqrt{n!}\ket{n}\\
\Aboxed{\ket\lambda&=e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{\sqrt{n!}}\ket{n}}
\end{align}$$
We want to find the annihilation operator of this state, and so:
$$\begin{align}
a\ket\lambda&=e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{\sqrt{n!}}a\ket{n}\\
&=e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{\sqrt{n!}}\sqrt{n}\ket{n-1}\\
&=0\ket{-1}+e^{-|\lambda|^2/2}\sum_{n=1}^\infty\dfrac{\lambda^n}{\sqrt{(n-1)!}}\ket{n-1}\\
\end{align}$$
Let $n'=n+1$, then:
$$\begin{align}
a\ket\lambda&=e^{-|\lambda|^2/2}\sum_{n=1}^\infty\dfrac{\lambda^n}{\sqrt{(n-1)!}}\ket{n-1}\\
&=e^{-|\lambda|^2/2}\sum_{n'=0}^\infty\dfrac{\lambda^{n'+1}}{\sqrt{n'!}}\ket{n'}\\
&=\lambda\cdot e^{-|\lambda|^2/2}\sum_{n'=0}^\infty\dfrac{\lambda^{n'}}{\sqrt{n'!}}\ket{n'}\\
\Aboxed{a\ket\lambda&=\lambda\ket\lambda}
\end{align}$$
Thus concludes the proof.

---
### Question 2.21.B
Prove the minimum uncertainty relation for such a state.

We need to find $\braket{x},\braket{x^2},\braket{p},\braket{p^2}$ to find the uncertainty relation.
$$\begin{align}
\hat{x}&=\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger+a\right)\\
\hat{x}^2&=\dfrac{\hbar}{2m\omega}\left[(a^\dagger)^2+aa^\dagger+a^\dagger a+a^2\right]\\
\hat{p}&=i\sqrt{\dfrac{\hbar m\omega}{2}}\left(a^\dagger-a\right)\\
\hat{p}^2&=-\dfrac{\hbar m\omega}{2}\left[(a^\dagger)^2-aa^\dagger-a^\dagger a+a^2\right]
\end{align}$$
We can also find each ladder operator of this state as:
$$\begin{align}
\Aboxed{a\ket\lambda&=\lambda\ket\lambda}
\end{align}$$
$$\begin{align}
a^\dagger\ket\lambda&=e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{\sqrt{n!}}a^\dagger\ket{n}\\
&=e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{\sqrt{n!}}\sqrt{n+1}\ket{n+1}
\end{align}$$
So we can see that:
$$\begin{align}
\Aboxed{\bra\lambda a\ket\lambda&=\bra\lambda\lambda\ket\lambda=\lambda}
\end{align}$$
$$\begin{align}
\bra\lambda a^\dagger\ket\lambda&=e^{-|\lambda|^2/2}\sum_{m=0}^\infty\dfrac{(\lambda^*)^m}{\sqrt{m!}}\bra{m}\cdot e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{\sqrt{n!}}\sqrt{n+1}\ket{n+1}\\
&=e^{-|\lambda|^2}\sum_{m=0}^\infty\sum_{n=0}^\infty\dfrac{(\lambda^*)^m}{\sqrt{m!}}\dfrac{\lambda^n}{\sqrt{n!}}\sqrt{n+1}\braket{m|n+1}\\
&=e^{-|\lambda|^2}\sum_{n=0}^\infty\dfrac{(\lambda^*)^{n+1}}{\sqrt{(n+1)!}}\dfrac{\lambda^n}{\sqrt{n!}}\sqrt{n+1}\cdot 1\\
&=e^{-|\lambda|^2}\sum_{n=0}^\infty\dfrac{(\lambda^*)^{n+1}}{\sqrt{(n+1)!}}\dfrac{\lambda^n}{\sqrt{(n+1)\cdot n!}}(n+1)\\
&=e^{-|\lambda|^2}\sum_{n=0}^\infty\dfrac{(\lambda^*)^{n+1}}{\sqrt{(n+1)!}}\dfrac{\lambda^n}{\sqrt{(n+1)!}}(n+1)\\
&=\lambda^*e^{-|\lambda|^2}\sum_{n=0}^\infty\dfrac{(|\lambda|^2)^{n}}{n!}\\
&=\lambda^*e^{-|\lambda|^2}e^{+|\lambda|^2}\\
\Aboxed{\bra\lambda a^\dagger\ket\lambda&=\lambda^*}
\end{align}$$
For the square operators, we see that:
$$\begin{align}
\Aboxed{\bra\lambda a^2\ket\lambda&=\lambda^2}
\end{align}$$
$$\begin{align}
\bra\lambda (a^\dagger)^2\ket\lambda&=e^{-|\lambda|^2/2}\sum_{m=0}^\infty\dfrac{(\lambda^*)^m}{\sqrt{m!}}\bra{m}\cdot e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{\sqrt{n!}}\sqrt{n+1}\sqrt{n+2}\ket{n+2}\\
&=e^{-|\lambda|^2}\sum_{m=0}^\infty\sum_{n=0}^\infty\dfrac{(\lambda^*)^m}{\sqrt{m!}}\dfrac{\lambda^n}{\sqrt{n!}}\sqrt{n+1}\sqrt{n+2}\braket{m|n+2}\\
&=e^{-|\lambda|^2}\sum_{n=0}^\infty\dfrac{(\lambda^*)^{n+2}}{\sqrt{(n+2)!}}\dfrac{\lambda^n}{\sqrt{n!}}\sqrt{n+1}\sqrt{n+2}\cdot 1\\
&=e^{-|\lambda|^2}\sum_{n=0}^\infty\dfrac{(\lambda^*)^{n+2}}{\sqrt{(n+2)!}}\dfrac{\lambda^n}{\sqrt{(n+2)(n+1)\cdot n!}}(n+1)(n+2)\\
&=e^{-|\lambda|^2}\sum_{n=0}^\infty\dfrac{(\lambda^*)^{n+2}}{\sqrt{(n+2)!}}\dfrac{\lambda^n}{\sqrt{(n+2)!}}(n+1)(n+2)\\
&=(\lambda^*)^2e^{-|\lambda|^2}\sum_{n=0}^\infty\dfrac{(|\lambda|^2)^{n}}{n!}\\
&=(\lambda^*)^2e^{-|\lambda|^2}e^{+|\lambda|^2}\\
\Aboxed{\bra\lambda (a^\dagger)^2\ket\lambda&=(\lambda^*)^2}
\end{align}$$
For the mixed operators:
$$\begin{align}
\Aboxed{\bra\lambda a^\dagger a\ket\lambda&=|\lambda|^2=1}\\
\Aboxed{\bra\lambda aa^\dagger \ket\lambda&=|\lambda|^2+1=2}\\
\end{align}$$
---
#### Finding $\braket{x}$
$$\begin{align}
\braket{x}&=\bra{\lambda}\hat{x}\ket{\lambda}\\
&=\bra{\lambda}\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger+a\right)\ket{\lambda}\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\left(\bra{\lambda}a^\dagger\ket{\lambda}+\bra{\lambda}a\ket{\lambda}\right)\\
&=\sqrt{\dfrac{\hbar}{2m\omega}}\left(\lambda^*\braket{\lambda|\lambda}+\lambda\braket{\lambda|\lambda}\right)\\
\Aboxed{\braket{x}&=\sqrt{\dfrac{\hbar}{2m\omega}}\left(\lambda^*+\lambda\right)}
\end{align}$$
---
#### Finding $\braket{p}$
$$\begin{align}
\braket{p}&=\bra{\lambda}\hat{p}\ket{\lambda}\\
&=\bra{\lambda}i\sqrt{\dfrac{\hbar m\omega}{2}}\left(a^\dagger-a\right)\ket{\lambda}\\
&=i\sqrt{\dfrac{\hbar m\omega}{2}}\left(\bra{\lambda}a^\dagger\ket{\lambda}-\bra{\lambda}a\ket{\lambda}\right)\\
&=i\sqrt{\dfrac{\hbar m\omega}{2}}\left(\lambda^*\braket{\lambda|\lambda}-\lambda\braket{\lambda|\lambda}\right)\\
\Aboxed{\braket{p}&=i\sqrt{\dfrac{\hbar m\omega}{2}}\left(\lambda^*-\lambda\right)}
\end{align}$$
---
For the mixed operators:
$$\begin{align}
\Aboxed{\bra\lambda a^\dagger a\ket\lambda&=|\lambda|^2=1}\\
\Aboxed{\bra\lambda aa^\dagger \ket\lambda&=|\lambda|^2+1=2}\\
\end{align}$$
---
#### Finding $\braket{x^2}$
$$\begin{align}
\braket{x^2}&=\bra{\lambda}\hat{x}^2\ket{\lambda}\\
&=\bra{\lambda}\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^\dagger+a\right)\ket{\lambda}\\
&=\dfrac{\hbar}{2m\omega}\left[\bra{\lambda}(a^\dagger)^2\ket{\lambda}+\bra{\lambda}aa^\dagger\ket{\lambda}+\bra{\lambda}a^\dagger a\ket{\lambda}+\bra{\lambda}a^2\ket{\lambda}\right]\\
&=\dfrac{\hbar}{2m\omega}\left[(\lambda^*)^2+\lambda^*\lambda+1+\lambda^*\lambda+\lambda^2\right]\\
\Aboxed{\braket{x^2}&=\dfrac{\hbar}{2m\omega}\left[(\lambda^*)^2+2\lambda^*\lambda+\lambda^2+1\right]}
\end{align}$$
---
#### Finding $\braket{p^2}$
$$\begin{align}
\braket{p^2}&=\bra{\lambda}\hat{p}^2\ket{\lambda}\\
&=-\bra{\lambda}\dfrac{\hbar m\omega}{2}\left[(a^\dagger)^2-aa^\dagger-a^\dagger a+a^2\right]\ket{\lambda}\\
&=-\bra{\lambda}\dfrac{\hbar m\omega}{2}\left[(\lambda^*)^2-\lambda^*\lambda-1-\lambda^*\lambda+\lambda^2\right]\ket{\lambda}\\
\Aboxed{\braket{p^2}&=-\dfrac{\hbar m\omega}{2}\left[(\lambda^*)^2-2\lambda^*\lambda+\lambda^2-1\right]}
\end{align}$$
---
#### Finding Variances
$$\begin{align}
\braket{(\Delta x)^2}&=\braket{x^2}-\braket{x}^2\\
&=\dfrac{\hbar}{2m\omega}\left[(\lambda^*)^2+2\lambda^*\lambda+\lambda^2+1\right]-\left(\sqrt{\dfrac{\hbar}{2m\omega}}\left(\lambda^*+\lambda\right)\right)^2\\
&=\dfrac{\hbar}{2m\omega}\left(\left[(\lambda^*)^2+2\lambda^*\lambda+\lambda^2+1\right]-\left(\lambda^*+\lambda\right)^2\right)\\
&=\dfrac{\hbar}{2m\omega}\left(\left[(\lambda^*)^2+2\lambda^*\lambda+\lambda^2+1\right]-\left((\lambda^*)^2+2\lambda^*\lambda+\lambda^2\right)\right)\\
&=\dfrac{\hbar}{2m\omega}\left(1\right)\\
\Aboxed{\braket{(\Delta x)^2}&=\dfrac{\hbar}{2m\omega}}
\end{align}$$
$$\begin{align}
\braket{(\Delta p)^2}&=\braket{p^2}-\braket{p}^2\\
&=-\dfrac{\hbar m\omega}{2}\left[(\lambda^*)^2-2\lambda^*\lambda+\lambda^2-1\right]-\left(i\sqrt{\dfrac{\hbar m\omega}{2}}\left(\lambda^*-\lambda\right)\right)^2\\
&=-\dfrac{\hbar m\omega}{2}\left(\left[(\lambda^*)^2-2\lambda^*\lambda+\lambda^2-1\right]-\left(\lambda^*-\lambda\right)^2\right)\\
&=-\dfrac{\hbar m\omega}{2}\left(\left[(\lambda^*)^2-2\lambda^*\lambda+\lambda^2-1\right]-\left((\lambda^*)^2-2\lambda^*\lambda+\lambda^2\right)\right)\\
&=-\dfrac{\hbar m\omega}{2}\left(-1\right)\\
\Aboxed{\braket{(\Delta p)^2}&=\dfrac{\hbar m\omega}{2}}
\end{align}$$
Therefore, we know that the uncertainty relation then becomes:
$$\begin{align}
\braket{(\Delta x)^2}\braket{(\Delta p)^2}&=\dfrac{\hbar}{2m\omega}\cdot\dfrac{\hbar m\omega}{2}\\
\braket{(\Delta x)^2}\braket{(\Delta p)^2}&=\dfrac{\hbar^2}{2^2}\\
\Aboxed{\sigma_x^2\sigma_p^2&=\dfrac{\hbar^2}{4}}\\
\Aboxed{\sigma_x\sigma_p&=\dfrac{\hbar}{2}}
\end{align}$$
Thus concludes the proof.

---
### Question 2.21.C
Write $\ket\lambda$ as
$$\begin{align}
\ket\lambda&=\sum_{n=0}^\infty f(n)\ket{n}
\end{align}$$
Show that the distribution of $|f(n)|^2$ with respect to $n$ is in the form of a Poisson distribution, that is $P_n(\mu)=\dfrac{\mu e^{-\mu}}{n!}$ where $\mu$ is the mean of the distribution. Find the most probable (integer) value of $n$, hence of $E$.

From earlier, we saw that this state vector can be represented as:
$$\begin{align}
\ket\lambda&=e^{-|\lambda|^2/2}\sum_{n=0}^\infty\dfrac{\lambda^n}{\sqrt{n!}}\ket{n}
\end{align}$$
So, equating both sides, we see that:
$$\begin{align}
f(n)&=e^{-|\lambda|^2/2}\dfrac{\lambda^n}{\sqrt{n!}}\\
|f(n)|^2&=e^{-|\lambda|^2/2}\dfrac{(\lambda^*)^n}{\sqrt{n!}}\cdot e^{-|\lambda|^2/2}\dfrac{\lambda^n}{\sqrt{n!}}\\
\Aboxed{|f(n)|^2&=e^{-|\lambda|^2}\dfrac{\left(|\lambda|^2\right)^n}{n!}}
\end{align}$$
Setting each side equal to each other, we see that:
$$\begin{align}
P_n(\mu)&=|f(n)|^2\\
\dfrac{\mu e^{-\mu}}{n!}&=\dfrac{\left(|\lambda|^2\right)^n}{n!}e^{-|\lambda|^2}
\end{align}$$
We can see plainly that $\boxed{\mu=\left|\lambda\right|^2}$.
To find the maximal number for $n$, then we can look at its derivative.
However, we have a $n!$, but we can just use the logarithm since it's monotonic.
$$\begin{align}
\dfrac{\partial}{\partial n}\ln|f(n)|^2&=\dfrac{\partial}{\partial n}
\ln\left(e^{-|\lambda|^2}\dfrac{\left(|\lambda|^2\right)^n}{n!}\right)\\
0&=\dfrac{\partial}{\partial n}
\ln\left(e^{-|\lambda|^2}\right)+\dfrac{\partial}{\partial n}
\ln\left(|\lambda|^{2n}\right)-\dfrac{\partial}{\partial n}
\ln\left(n!\right)\\
&=0+\ln\left(|\lambda|^2\right)\dfrac{\partial}{\partial n}
(n)-\dfrac{\partial}{\partial n}
\left(n\ln n -n\right)\\
&=\ln\left(|\lambda|^2\right)-\ln n -1+1\\
0&=\ln\left(|\lambda|^2\right)-\ln n\\
\ln n&=\ln\left(|\lambda|^2\right)\\
\Aboxed{n&=|\lambda|^2}
\end{align}$$
Therefore the mode of this distribution is basically the same as the mean.
However, Poisson Distributions have integer functionals, and so:
$$\begin{align}
\Aboxed{n&=\max\left(\lfloor\mu\rfloor, \lceil\mu\rceil\right), \ \ \ \mu=|\lambda|^2}
\end{align}$$
---
### Question 2.21.D
Show that a coherent state can also be obtained by applying the translation (finite displacement) operator $e^{-ipl/\hbar}$ (where $p$ is the momentum operator, and $l$ is the displacement distance) to the ground state.

The first thing I notice is that this operator should be written in terms of creation and annihilation.
$$\begin{align}
\exp\left(-ipl/\hbar\right)&=\exp\left(-i\cdot i\sqrt{\dfrac{\hbar m\omega}{2}}\left(a^\dagger-a\right)\cdot l/\hbar\right)\\
&=\exp\left(l\sqrt{\dfrac{m\omega}{2\hbar}}\left(a^\dagger-a\right)\right)\\
\end{align}$$
For simplified notation, let $\lambda=l\sqrt{\tfrac{m\omega}{2\hbar}}$, then:
$$\begin{align}
e^{-ipl/\hbar}&=e^{\lambda\left(a^\dagger-a\right)}\\
\end{align}$$
Since these are operators, the commutators makes this difficult, but I found in the textbook:
$$\begin{align}
e^{\lambda\left(a^\dagger-a\right)}&=e^{-|\lambda|^2}e^{\lambda a^\dagger}e^{-\lambda a}\\
\end{align}$$
We start from the ground state, so:
$$\begin{align}
\ket\lambda&=e^{-|\lambda|^2}e^{\lambda a^\dagger}e^{-\lambda a}\ket{0}\\
&=e^{-|\lambda|^2}e^{\lambda a^\dagger}\sum_{n=0}^\infty\dfrac{(-\lambda a)^n}{n!}\ket{0}\\
&=e^{-|\lambda|^2}e^{\lambda a^\dagger}\left(\dfrac{1}{1}\ket{0}+\sum_{n=1}^\infty\dfrac{(-\lambda a)^n}{n!}\ket{0}\right)\\
&=e^{-|\lambda|^2}e^{\lambda a^\dagger}\left(\dfrac{1}{1}\ket{0}+\sum_{n=1}^\infty0\right)\\
\Aboxed{\ket\lambda&=e^{-|\lambda|^2}e^{\lambda a^\dagger}\ket{0}}
\end{align}$$
This is the same expression we see for part A, and we proved this is a coherent state there.
Therefore, this does create a coherent state.

---



## Question 2.24
This exercise has to do with proving conservation laws in classical and quantum physics.
### Question 2.24.A
Show that if a quantity $Q$ with a density $\rho(x,t)$ in some region $\mathcal{R}$ can only be changed by a flux density $J(x,t)$ through the surface bordering $\mathcal{R}$, then:
$$\begin{align}
\dfrac{\partial\rho}{\partial t}+\vec\nabla\cdot\vec{J}&=0
\end{align}$$
Well I'm not sure what to do, but I can start with:
$$\begin{align}
Q(t)&=\int_\mathcal{R}\rho(x,t)\ dV
\end{align}$$
The rate change in such a quantity $Q$ should be equal to a flow outward of some flux density:
$$\begin{align}
\dfrac{d}{dt}Q(t)&=-\int_{\partial\mathcal{R}}\vec{J}(x,t)\cdot d\vec{A}
\end{align}$$
Using what we have from above, as well as the divergence theorem, then:
$$\begin{align}
\dfrac{d}{dt}Q(t)&=-\int_{\partial\mathcal{R}}\vec{J}(x,t)\cdot d\vec{A}\\
\dfrac{d}{dt}\int_\mathcal{R}\rho(x,t)\ dV&=-\int_{\mathcal{R}}\left(\vec\nabla\cdot\vec{J}(x,t)\right)\ dV\\
\int_\mathcal{R}\dfrac{\partial}{\partial t}\rho(x,t)\ dV&=-\int_{\mathcal{R}}\left(\vec\nabla\cdot\vec{J}(x,t)\right)\ dV\\
\dfrac{\partial\rho}{\partial t}(x,t)&=-\vec\nabla\cdot\vec{J}(x,t)\\
\end{align}$$
Bringing everything to 1 side, we can see that:
$$\begin{align}
\Aboxed{\dfrac{\partial\rho}{\partial t}(x,t)+\vec\nabla\cdot\vec{J}(x,t)&=0}
\end{align}$$
---
### Question 2.24.B
Prove that Maxwell's equations imply that electric charge is conserved.
$$\begin{align}
\dfrac{\partial\rho}{\partial t}+\vec\nabla\cdot\vec{J}&=0
\end{align}$$
Start with the equation for Electric-Field Charge relationship:
$$\begin{align}
\int_\mathcal{ R}\left(\vec\nabla\cdot\epsilon_0\vec{E}\right)dV&=\int_\mathcal{R}\rho(x,t)\ dV
\end{align}$$
We can find the rate-change of charge equating to an outward charge flux:
$$\begin{align}
\dfrac{d}{dt}\int_\mathcal{ R}\left(\vec\nabla\cdot\epsilon_0\vec{E}\right)dV&=\dfrac{d}{dt}\int_\mathcal{R}\rho(x,t)\ dV\\
\epsilon_0\int_\mathcal{ R}\left(\vec\nabla\cdot\dfrac{\partial\vec{E}}{\partial t}\right)dV&=\dfrac{d}{dt}\int_\mathcal{R}\rho(x,t)\ dV\\
\end{align}$$
Using Ampere's Law:
$$\begin{align}
&&\vec\nabla\times\vec{B}&=\mu_0\vec{J}+\epsilon_0\mu_0\dfrac{\partial\vec{E}}{\partial t}\\
\implies&&\dfrac{\partial\vec{E}}{\partial t}&=-\dfrac{1}{\epsilon_0}\vec{J}+\dfrac{1}{\epsilon_0\mu_0}\vec\nabla\times\vec{B}
\end{align}$$
Substituting, we get:
$$\begin{align}
\dfrac{d}{dt}\int_\mathcal{R}\rho(x,t)\ dV&=\epsilon_0\int_\mathcal{ R}\left(-\dfrac{1}{\epsilon_0}\vec\nabla\cdot\vec{J}+\dfrac{1}{\epsilon_0\mu_0}\vec\nabla\cdot(\vec\nabla\times\vec{B})\right)dV\\
&=\int_\mathcal{ R}\left(-\vec\nabla\cdot\vec{J}+\dfrac{1}{\mu_0}\cdot0\right)dV\\
\dfrac{d}{dt}\int_\mathcal{R}\rho(x,t)\ dV&=\int_\mathcal{ R}\left(-\vec\nabla\cdot\vec{J}\right)dV\\
\end{align}$$
We can swap the integral and derivative, and so:
$$\begin{align}
\int_\mathcal{R}\dfrac{\partial\rho}{\partial t}(x,t)\ dV&=\int_\mathcal{ R}\left(-\vec\nabla\cdot\vec{J}\right)dV\\
\dfrac{\partial\rho}{\partial t}(x,t)&=-\vec\nabla\cdot\vec{J}\\
\end{align}$$
Swapping sides, we then show that:
$$\begin{align}
\Aboxed{\dfrac{\partial\rho}{\partial t}(x,t)+\vec\nabla\cdot\vec{J}&=0}
\end{align}$$
Therefore, charge is conserved with Maxwell's equations.

---
### Question 2.24.C
Prove that Schrödinger's equation implies that probability is conserved, i.e. (2.190).
$$\begin{align}
i\hbar\dfrac{\partial\psi}{\partial t}&=-\dfrac{\hbar^2}{2m}\vec\nabla^2\psi+V(\vec{x},t)\psi &\implies&& \dfrac{\partial\psi}{\partial t}&=i\dfrac{\hbar}{2m}\vec\nabla^2\psi+\dfrac{1}{i\hbar}V(\vec{x},t)\psi\\
-i\hbar\dfrac{\partial\psi^*}{\partial t}&=-\dfrac{\hbar^2}{2m}\vec\nabla^2\psi^*+V(\vec{x},t)\psi^* &\implies&& \dfrac{\partial\psi^*}{\partial t}&=-i\dfrac{\hbar}{2m}\vec\nabla^2\psi^*-\dfrac{1}{i\hbar}V(\vec{x},t)\psi^*\\
\end{align}$$
Let the probability, by definition, be $\rho=\psi^*\psi$, and so:
$$\begin{align}
\dfrac{\partial\rho}{\partial t}&=\dfrac{\partial \psi^*}{\partial t}\psi+\psi^*\dfrac{\partial \psi}{\partial t}\\
&=\left(-i\dfrac{\hbar}{2m}\vec\nabla^2\psi^*-\dfrac{1}{i\hbar}V(\vec{x},t)\psi^*\right)\psi+\psi^*\left(i\dfrac{\hbar}{2m}\vec\nabla^2\psi+\dfrac{1}{i\hbar}V(\vec{x},t)\psi\right)\\
&=-i\dfrac{\hbar}{2m}(\vec\nabla^2\psi^*)\psi-\dfrac{1}{i\hbar}V(\vec{x},t)\psi^*\psi+i\dfrac{\hbar}{2m}\psi^*(\vec\nabla^2\psi)+\dfrac{1}{i\hbar}V(\vec{x},t)\psi^*\psi\\
\Aboxed{\dfrac{\partial\rho}{\partial t}&=-\dfrac{i\hbar}{2m}\left(\psi\vec\nabla^2\psi^*-\psi^*\vec\nabla^2\psi\right)}
\end{align}$$
In the form of continuity, we have that:
$$\begin{align}
\dfrac{\partial\rho}{\partial t}(x,t)+\vec\nabla\cdot\vec{J}&=0 &\implies &&\vec\nabla\cdot\vec{J}&=-\dfrac{\partial\rho}{\partial t}(x,t)
\end{align}$$
We can write the rate change equation as:
$$\begin{align}
\Aboxed{\dfrac{\partial\rho}{\partial t}&=-\dfrac{i\hbar}{2m}\vec{\nabla}\cdot\left(\psi\vec\nabla\psi^*-\psi^*\vec\nabla\psi\right)}
\end{align}$$
Then we can see that:
$$\begin{align}
\vec\nabla\cdot\vec{J}&=\dfrac{i\hbar}{2m}\vec{\nabla}\cdot\left(\psi\vec\nabla\psi^*-\psi^*\vec\nabla\psi\right)\\
\Aboxed{\vec{J}(\vec{x},t)&=\dfrac{i\hbar}{2m}\left(\psi\vec\nabla\psi^*-\psi^*\vec\nabla\psi\right)}\\
\Aboxed{\vec{J}(\vec{x},t)&=\dfrac{\hbar}{2mi}\left(\psi^*\vec\nabla\psi-\psi\vec\nabla\psi^*\right)}
\end{align}$$
