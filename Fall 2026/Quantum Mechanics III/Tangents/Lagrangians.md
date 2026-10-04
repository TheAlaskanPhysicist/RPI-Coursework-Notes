


## Klein-Gordon Field (Spin-0, $\mathbb{C}$)
Suppose we have a set of $N$, non-interacting, scalar (Spin-$0$), massive fields $\phi_a\in\mathbb{C}$. The Lagrangian density of this system is then
$$\begin{align}
-2\mathcal{L}&=\phi^\dagger\left(M^2-\overleftarrow{\partial^\mu}g_{\mu\nu} \overrightarrow{\partial^\nu}\right)\phi
\end{align}$$
where $M$ is a diagonal matrix $M_{aa}=m_a$. In component form, this is equal to
$$\begin{align}
-2\mathcal{L}&=\sum_a\phi_a^*\left(m_a^2-\overleftarrow{\partial^\mu}g_{\mu\nu} \overrightarrow{\partial^\nu}\right)\phi_a
\end{align}$$
Using the Euler-Lagrange equations in every component $(\phi_n,\phi_n^*)$, we find the equations of motion
$$\begin{align}
\left(\partial^\mu\partial_\mu+m_a^2\right)\phi_a&=0 &
\left(\partial^\mu\partial_\mu+m_a^2\right)\phi_a^*&=0
\end{align}$$





## Klein-Gordon Field (Spin-0, $\mathbb{C}$)
Suppose we have a massive field $\phi\in\mathbb{C}$ with Lagrangian density
$$\begin{align}
\mathcal{L}&=\dfrac{1}{2}\left(\partial^\mu\phi^*\right)\left(\partial_\mu\phi\right)-\dfrac{1}{2}\phi^*m^2\phi
\end{align}$$
Now impose a translational invariance in the Lagrangian such that
$$\begin{align}
\phi(X)&\to\phi(X+a) &\implies&& \mathcal{L}&=\mathcal{L}'
\end{align}$$
The operator to achieve this translation is
$$\begin{align}
U(a)&=e^{a\frac{d}{dX}} &\implies&& U(a)\phi(X)&=\phi(X+a)
\end{align}$$
However, this differential is in 3+1 spacetime, and so we need to use the chain rule to find
$$\begin{align}
\dfrac{d}{dX}&=\dfrac{dt}{dX}\dfrac{d}{dt}+\dfrac{dx_i}{dX}\dfrac{d}{dx_i}
\end{align}$$
Using this translation operator, we can evaluate the Lagrangian density as
$$\begin{align}
\mathcal{L}'
&=\dfrac{1}{2}\left(\partial^\mu\left(U\phi\right)^*\right)\left(\partial_\mu\left(U\phi\right)\right)-\dfrac{1}{2}\left(U\phi\right)^*m^2\left(U\phi\right)\\
\mathcal{L}'-\mathcal{L}&=\dfrac{1}{2}\left(\phi^*(\partial^\mu U^\dagger)(\partial_\mu U)\phi\right)+\dfrac{1}{2}\left[\phi^*(\partial_\mu\phi)(\partial^\mu U^\dagger) U+\text{h.c.}\right]
\end{align}$$
We can evaluate these extra derivatives as
$$\begin{align}
\partial_\mu U&=\partial_\mu e^{a\frac{d}{dX}}\\
&=e^{a\frac{d}{dX}}\partial_\mu\left(a\frac{d}{dX}\right)\\
\partial_\mu U&=\left(\partial_\mu a\right)U(a)\frac{d}{dX}
+aU(a)\partial_\mu\left(\frac{d}{dX}\right)\\
\partial^\mu U^\dagger&=\left(\partial^\mu a\right)U^\dagger(a)\frac{d}{dX}
+aU^\dagger(a)\partial^\mu\left(\frac{d}{dX}\right)
\end{align}$$
Substituting back in, we get that
$$\begin{align}
0&=\left(\partial^\mu a\right)\left(\partial_\mu a\right)\frac{d}{dX}\frac{d}{dX}
+a\left(\partial_\mu a\right)\frac{d}{dX}\partial^\mu\left(\frac{d}{dX}\right)+a\left(\partial^\mu a\right)\frac{d}{dX}\partial_\mu\left(\frac{d}{dX}\right)
+a^2\partial^\mu\left(\frac{d}{dX}\right)\partial_\mu\left(\frac{d}{dX}\right)

\\

&+\left[\phi^*(\partial_\mu\phi)\left(\partial^\mu a\right)\frac{d}{dX}
+\phi^*(\partial_\mu\phi)a\partial^\mu\left(\frac{d}{dX}\right) +\text{h.c.}\right]
\end{align}$$
Assuming these generators are constant with respect to the coordinates, we reduce to
$$\begin{align}
0&=\left(\partial^\mu a\right)\left(\partial_\mu a\right)\frac{d}{dX}\frac{d}{dX}
+\left[\phi^*(\partial_\mu\phi)\left(\partial^\mu a\right)\frac{d}{dX}
+\text{h.c.}\right]\\
0&=\partial_\mu\left[\phi^*\phi+a\frac{d}{dX}
\right]\partial^\mu a
\end{align}$$
So we have the following conditions
$$\begin{align}
\partial_\mu\left[\phi^*\phi+a\frac{d}{dX}\right]&=0 &\text{or}&&
\partial^\mu a&=0
\end{align}$$
In terms of the canonical momentum (generator of translation), we have that
$$\begin{align}
\partial_\mu\left[\phi^*\phi-\frac{a}{i\hbar}\dfrac{\delta\mathcal{L}}{\delta\phi}\cdot\hat{X}\right]&=0
\end{align}$$



So in Differential Geometry, we have the idea of the exterior derivative $\mathrm{d}$, which when applied to a function has the following chain rule effect
$$\begin{align}
f(x,y,z,\dots) &&\implies&& \mathrm{d}f&=\dfrac{df}{dx}\mathrm{d}x+\dfrac{df}{dy}\mathrm{d}y+\dfrac{df}{dz}\mathrm{d}z+\dots
\end{align}$$
The effect of the exterior is that it maps a scalar field into a 1-form (covector). However, notice that all of the components of the covector are of the form $\frac{d}{dx_i}$. This is because the derivative in these coordinates form a basis that are 1-vectors. In terms of a vector basis $e_\mu$ and covector basis $e^\mu$ :
$$\begin{align}
e_\mu&\equiv\dfrac{\partial}{\partial x^\mu} & e^\mu\equiv dx^\mu
\end{align}$$




To make the point a little clearer, if we take the product of these two on a function $f$ :
$$\begin{align}
e^\mu e_\nu f&=dx^\mu\dfrac{\partial f}{\partial x^\nu}
\end{align}$$
This should look familiar (chain rule) but it's also actually just a projection!
$$\begin{align}
\bra{f}\to\left<f\middle|x\right>\bra{x}
\end{align}$$
The operation is saying "project $f$ onto this coordinate basis, then multiply by that basis element"
$$\begin{align}
p_\mu&=\dfrac{\partial\mathcal{L}}{\partial\dot x^\mu}
\end{align}$$



I know that some people here are bundle maxxers so an alternative way to think about this is if we define position coordinate $q\in Q$, then the velocity $\dot{q}\in T_qQ$ is an element of the tangent space of $Q$, so in coordinates we write that as
$$\begin{align}
\dot{q}&=\dot{q}^i\dfrac{\partial}{\partial q^i}
\end{align}$$
By contrast, the canonical momentum is naturally an element of the cotangent space of $Q$, and so we can write it as
$$\begin{align}
p&\in T_q^*Q &\implies&& p&=p_i dq^i
\end{align}$$
The Lagrangian is a function on the **tangent** bundle
$$\begin{align}
L:TQ\to\mathbb{R} && L=L(q,\dot{q},t)
\end{align}$$
The derivative of this Lagrangian by the time-derivative of the contravariant position is then
$$\begin{align}
p_i&=\dfrac{\partial L}{\partial\dot{q}_i}
&\implies&&
p&=\dfrac{\partial L}{\partial\dot{q}}\in T^*_qQ
\end{align}$$
The Hamiltonian is a function on the **cotangent** bundle
$$\begin{align}
H:T^*Q\to\mathbb{R} && H=H(q,p,t)
\end{align}$$




$$\begin{align}
g_{\mu\nu}&\equiv e_\mu\cdot e_\nu
\end{align}$$
