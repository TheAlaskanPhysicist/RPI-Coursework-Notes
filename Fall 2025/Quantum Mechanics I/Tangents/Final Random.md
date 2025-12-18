Suppose we start with a Harmonic Oscillator ground state:
$$\begin{align}
\ket\psi&=\ket{0}
\end{align}$$
An force applied to the system gives an addition $p_0$ of momentum.

What is the probability of the state still being in the ground state?
$$\begin{align}
\bra{0}e^{-i\frac{p_0}{\hbar}\hat{x}}\ket{0}&=\bra{0}e^{-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}(a+a^\dagger)}\ket{0}\\
&=\bra{0}e^{-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}a}e^{-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}a^\dagger}e^{+i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}[a,a^\dagger]/2}\ket{0}\\
&=\bra{0}e^{+i\frac{p_0}{2\hbar}\sqrt{\frac{\hbar}{2m\omega}}}e^{-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}a}e^{-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}a^\dagger}\ket{0}\\
&=\bra{0}e^{+i\frac{p_0}{2\hbar}\sqrt{\frac{\hbar}{2m\omega}}}e^{-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}a}\sum_{n=0}^\infty\dfrac{\left(-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}\right)^n}{\sqrt{n!}}\ket{n}\\
&=\bra{0}e^{+i\frac{p_0}{2\hbar}\sqrt{\frac{\hbar}{2m\omega}}}\sum_{n=0}^\infty\dfrac{\left(-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}\right)^n}{\sqrt{n!}}\sum_{m=0}^\infty\dfrac{\left(-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}\right)^m}{m!}\sqrt{\dfrac{n!}{(n-m)!}}\ket{n-m}\\
&=\bra{0}e^{+i\frac{p_0}{2\hbar}\sqrt{\frac{\hbar}{2m\omega}}}\sum_{n=0}^\infty\dfrac{\left(-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}\right)^n}{\sqrt{n!}}\dfrac{\left(-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}\right)^n}{n!}\sqrt{\dfrac{n!}{(n-n)!}}\ket{n-n}\\
&=\bra{0}e^{+i\frac{p_0}{2\hbar}\sqrt{\frac{\hbar}{2m\omega}}}\sum_{n=0}^\infty\dfrac{\left(-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}\right)^n}{\sqrt{n!}}\dfrac{\left(-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}\right)^n}{\sqrt{n!}}\ket{0}\\
&=\bra{0}e^{+i\frac{p_0}{2\hbar}\sqrt{\frac{\hbar}{2m\omega}}}\sum_{n=0}^\infty\dfrac{\left(-i\frac{p_0}{\hbar}\sqrt{\frac{\hbar}{2m\omega}}\right)^{2n}}{n!}\ket{0}\\
&=\bra{0}e^{+i\frac{p_0}{2\hbar}\sqrt{\frac{\hbar}{2m\omega}}}e^{-\frac{p_0^2}{\hbar^2}\frac{\hbar}{2m\omega}}\ket{0}\\
&=\bra{0}e^{-\frac{p_0^2}{2m\omega\hbar}+i\frac{p_0}{2\hbar}\sqrt{\frac{\hbar}{2m\omega}}}\ket{0}\\
\end{align}$$
So the probability is:
$$\begin{align}
p(\ket{\psi}'=\ket{0})&=e^{-2\frac{p_0^2/2m}{\hbar\omega}}\\
\end{align}$$
