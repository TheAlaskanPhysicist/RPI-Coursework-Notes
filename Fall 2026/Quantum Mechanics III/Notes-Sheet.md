## Classical Field Theory
Action
$$\begin{align}
S&=\int L\ dt=\int\mathcal{L}(\phi,\partial_\mu\phi)\ d^4x\\
\end{align}$$
Variational Action
$$\begin{align}
\delta S&=0
&\implies&&
\dfrac{\partial\mathcal{L}}{\partial\phi}-\partial_\mu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}\right)&=0
\end{align}$$
Conjugate Momentum & Hamiltonian
$$\begin{align}
\pi&\equiv\dfrac{\partial\mathcal{L}}{\partial\dot\phi}
&\text{and}&&
\mathcal{H}&=\dfrac{\partial\mathcal{L}}{\partial\dot\phi}\dot\phi-\mathcal{L}=\pi\dot\phi-\mathcal{L}
\end{align}$$
### Noether
Suppose that we have a field transformation $U$ on a field $\phi(x)$, then an infinitesimal field transformation can be written as the linearized operation


$$\begin{align}
U(x')\phi&=\sum_{n=0}^\infty \frac{U^{(n)}(x)}{n!}(x-x')
\end{align}$$



$$\begin{align}
f(x+dx)=f(x)+\left.\dfrac{\partial f}{\partial x}\right|_{x=x}dx
\end{align}$$



$$\begin{align}
\phi&\to\phi'=\phi+\alpha\dfrac{\partial U}{\partial\alpha}d\phi\\
\end{align}$$




Suppose we have a field transformation $U$ on $\phi$ such that
$$\begin{align}
\phi(x)&\to U\phi(x)
\end{align}$$








$$\begin{align}
\phi(x)&\to\phi'(x)=\phi(x)+\alpha\cdot\delta\phi(x)\\
\mathcal{L}(x)&\to\mathcal{L}'(x)=\mathcal{L}(x)+\alpha\partial_\mu\mathcal{J}^\mu(x)
\end{align}$$

$$\begin{align}
j^\mu(x)&=\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}\delta\phi-\mathcal{J}^\mu\\
\partial_\mu j^\mu(x)&=0
\end{align}$$



$$\begin{align}
\delta\mathcal{L}
&=\dfrac{\partial\mathcal{L}}{\partial\phi}\delta\phi(x)
+\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}\partial_\mu\delta\phi(x)\\
&=\partial_\mu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}\delta\phi(x)\right)
+\left[\dfrac{\partial\mathcal{L}}{\partial\phi}-\partial_\mu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}\right)\right]\delta\phi(x)\\
\delta\mathcal{L}&=\partial_\mu\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}\delta\phi(x)\right)=\alpha\partial_\mu\mathcal{J}^\mu(x)\\
\end{align}$$








## Klein-Gordon Field ($\phi\in\mathbb{R}$)
Lagrangian & Hamiltonian:
$$\begin{align}
\frac{1}{2}\left(\partial_\mu\phi\right)^2-\frac{1}{2}m^2\phi^2
=\mathcal{L}
&=\frac{1}{2}\dot\phi^2-\frac{1}{2}\left(\vec\nabla\phi\right)^2-\frac{1}{2}m^2\phi^2\\
\mathcal{H}
&=\frac{1}{2}\pi^2+\frac{1}{2}\left(\vec\nabla\phi\right)^2+\frac{1}{2}m^2\phi^2
\end{align}$$
Equation of Motion:
$$\begin{align}
\left(\partial^\mu\partial_\mu+m^2\right)\phi&=0=\left(\dfrac{\partial^2}{\partial t^2}-\vec\nabla^2+m^2\right)\phi
\end{align}$$


