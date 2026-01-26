Stanley Goodwin, 1/25/2026

---
### Question 1
Show that the time-reversal operator $\Theta$ commutes with the rotation operator $\mathcal{D}(R)$, i.e.
$$\begin{align}
\Theta\ \mathcal{D}(R)\ \Theta^{-1}&=\mathcal{D}(R)
\end{align}$$
Hint: start with $\mathcal{D}(R)=e^{-i(\vec{J}\cdot{n})\phi/\hbar}$ and exploit $\Theta\ \vec{J}\ \Theta^{-1}=-\vec{J}$.

Starting with our generator representation of $\mathcal{D}(R)$, we get:
$$\begin{align}
\Theta\ \mathcal{D}(R)\ \Theta^{-1}&=\Theta\ e^{-i(\vec{J}\cdot\vec{n})\phi/\hbar}\ \Theta^{-1}\\
&=\sum_{n\ge0}\Theta\ \dfrac{(-i(\vec{J}\cdot\vec{n})\phi/\hbar)^n}{n!}\ \Theta^{-1}\\
&=\sum_{n\ge0}\Theta(-i\vec{J})^n\Theta^{-1}\dfrac{(\cdot\vec{n}\ \phi/\hbar)^n}{n!}\\
&=\sum_{n\ge0}\underbrace{\Theta(-i\vec{J})\Theta^{-1}\Theta(-i\vec{J})\Theta^{-1}\dots\Theta(-i\vec{J})\Theta^{-1}}_{n\text{ times}}\dfrac{(\cdot\vec{n}\ \phi/\hbar)^n}{n!}\\
&=\sum_{n\ge0}\underbrace{(+i\Theta\vec{J})\Theta^{-1}(+i\Theta\vec{J})\Theta^{-1}\dots(+i\Theta\vec{J})\Theta^{-1}}_{n\text{ times}}\dfrac{(\cdot\vec{n}\ \phi/\hbar)^n}{n!}\\
&=\sum_{n\ge0}(+i)^n\left(\Theta\vec{J}\Theta^{-1}\right)^n\dfrac{(\cdot\vec{n}\ \phi/\hbar)^n}{n!}\\
&=\sum_{n\ge0}(+i)^n\left(-\vec{J}\right)^n\dfrac{(\cdot\vec{n}\ \phi/\hbar)^n}{n!}\\
&=\sum_{n\ge0}\dfrac{(-i\vec{J}\cdot\vec{n}\ \phi/\hbar)^n}{n!}\\
&=e^{-i\vec{J}\cdot\vec{n}\ \phi/\hbar}\\
\Aboxed{\Theta\ \mathcal{D}(R)\ \Theta^{-1}&=\mathcal{D}(R)}
\end{align}$$
---
### Question 2
The momentum-space wave function of state $\ket\alpha$ is $\phi\left(\vec{p}'\right)=\braket{\vec{p}'|\alpha}$. What is the momentum-space wave function of its time-reversed transform $\Theta\ket\alpha$, i.e. $\bra{\vec{p}'}\Theta\ket{\alpha}$? Hint: start with the expansion of $\ket\alpha$ in momentum eigenkets and exploit what you know about $\Theta\ket{\vec{p}'}$.

We can represent an arbitrary state in a complete basis, such as momentum, as:
$$\begin{align}
\ket\alpha&=\int\ket{\vec{p}'}\braket{\vec{p}'|\alpha}\ d\vec{p}'\\
\end{align}$$
When applying the time-reversal operator, we then get:
$$\begin{align}
\Theta\ket\alpha&=\int\Theta\left(\ket{\vec{p}'}\braket{\vec{p}'|\alpha}\right)\ d\vec{p}'\\
&=\int\braket{\vec{p}'|\alpha}^*\Theta\ket{\vec{p}'}\ d\vec{p}'\\
&=\int\braket{\vec{p}'|\alpha}^*\ket{-\vec{p}'}\ d\vec{p}'\\
&=\int\braket{-\vec{p}'|\alpha}^*\ket{\vec{p}'}\ d\vec{p}'\\
\Theta\ket\alpha&=\int\phi^*\left(-\vec{p}'\right)\ket{\vec{p}'}\ d\vec{p}'\\
\Aboxed{\bra{\vec{p}'}\Theta\ket\alpha&=\phi^*\left(-\vec{p}'\right)}
\end{align}$$
