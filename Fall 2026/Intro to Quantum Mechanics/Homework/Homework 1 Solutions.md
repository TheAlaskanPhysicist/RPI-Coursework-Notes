**Author:** Stanley Goodwin
**Date:** September 26th, 2026

---
## Question 1.2
> Consider a particle who's Hamiltonian $\hat{H}$ is$$\begin{align}
\hat{H}&=-\dfrac{\hbar^2}{2m}\dfrac{d^2}{dx^2}-\alpha\delta(x)
\end{align}$$where $\alpha$ is a positive constant whose dimensions are to be found.

### Question 1.2.A
> Integrate the eigenvalue equation of $\hat{H}$ on $x\in\left(-\epsilon,+\epsilon\right)$. Letting $\epsilon\to0$, show that the derivative of the eigenfunction $\psi(x)$ presents a discontinuity at $x=0$ and determine it in terms of $\alpha$, $m$, and $\psi(0)$.

Our Hamiltonian equation represents the total energy of the system
$$\begin{align}
\hat{H}\psi(x)&=E\psi(x) &\implies&& 
-\dfrac{\hbar^2}{2m}\dfrac{d^2\psi}{dx^2}-\alpha\delta(x)\psi(x)&=E\psi(x)
\end{align}$$
Integrating both sides over the interval $x\in\left(-\epsilon,+\epsilon\right)$, we get
$$\begin{align}
-\dfrac{\hbar^2}{2m}\int_{-\epsilon}^{+\epsilon}\dfrac{d}{dx}\left(\dfrac{d\psi}{dx}\right)\ dx-\alpha\int_{-\epsilon}^{+\epsilon}\delta(x)\psi(x)\ dx&=E\int_{-\epsilon}^{+\epsilon}\psi(x)\ dx
\end{align}$$
The FTC can be used to evaluate the first term, the infinity of the delta function is contained over the integration domain and so gets evaluated at $x=0$, and thus simplifies to
$$\begin{align}
-\dfrac{\hbar^2}{2m}\left.\dfrac{d\psi}{dx}\right|_{-\epsilon}^{+\epsilon}-\alpha\psi(0)&=E\int_{-\epsilon}^{+\epsilon}\psi(x)\ dx
\end{align}$$
In the limit as $\epsilon\to0$, integration of $\psi(x)$ also approaches zero. Rearranging the terms, we arrive to
$$\begin{align}
&&\lim_{\epsilon\to0}\left[-\dfrac{\hbar^2}{2m}\left.\dfrac{d\psi}{dx}\right|_{-\epsilon}^{+\epsilon}-\alpha\psi(0)\right]&=\lim_{\epsilon\to0}E\int_{-\epsilon}^{+\epsilon}\psi(x)\ dx=0\\
&\implies&
-\dfrac{\hbar^2}{2m}\lim_{\epsilon\to0}\left[\dfrac{d\psi}{dx}(+\epsilon)-\dfrac{d\psi}{dx}(-\epsilon)\right]&=\alpha\psi(0)
\end{align}$$
Lastly, we can divide by the extra term on the limit side, as well as using prime notation for spatial derivatives, to arrive to our discontinuity condition:
$$\begin{align}
\Aboxed{\lim_{\epsilon\to0}\left[\psi'(+\epsilon)-\psi'(-\epsilon)\right]&=-\dfrac{2m\alpha}{\hbar^2}\psi(0)}
\end{align}$$
While the derivative of $\psi(x)$ has a discontinuity at $x=0$, the difference in the derivative from either side is equal to a scale factor times the value of the wavefunction at $x=0$.

---
### Question 1.2.B
