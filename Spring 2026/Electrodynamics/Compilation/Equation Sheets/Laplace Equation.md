We want to construct the general solutions for Laplace's equation in Electromagnetism.

## Cartesian Coordinates
Suppose we have the Laplacian:
$$\begin{align}
\vec\nabla^2\Phi&=\dfrac{\partial^2\Phi}{\partial x^2}+\dfrac{\partial^2\Phi}{\partial y^2}+\dfrac{\partial^2\Phi}{\partial z^2}=0
\end{align}$$
Let $\Phi(x,y,z)=X(x)Y(y)Z(z)$, then:
$$\begin{align}
\dfrac{X''}{X}+\dfrac{Y''}{Y}+\dfrac{Z''}{Z}&=0
\end{align}$$
Each term must be a constant, so we let $\alpha,\beta,\gamma$ to exist such that:
$$\begin{align}
\dfrac{X''}{X}&=\alpha^2 & \dfrac{Y''}{Y}&=\beta^2 & \dfrac{Z''}{Z}&=\gamma^2 & \alpha^2+\beta^2+\gamma^2&=0
\end{align}$$
Each equation can be solved to find:
$$\begin{align}
\Phi_{\alpha\beta\gamma}(x,y,z)&=\left(A_xe^{\alpha x}+B_xe^{-\alpha x}\right)\left(A_ye^{\beta y}+B_ye^{-\beta y}\right)\left(A_ze^{\gamma z}+B_ze^{-\gamma z}\right)
\end{align}$$
Or in terms of waves, we get:
$$\begin{align}
\Phi(x,y,z)&=\sum_{\alpha,\beta,\gamma}^{\alpha^2+\beta^2+\gamma^2=0}\left(A'_x\sin(i\alpha)+B'_x\cos(i\alpha)\right)\left(A'_y\sin(i\beta)+B'_y\cos(i\beta)\right)\left(A'_z\sin(i\gamma)+B'_x\cos(i\gamma)\right)
\end{align}$$
If we explicitly impose the condition for $\gamma$, then we get:
$$\begin{align}
\Phi(x,y,z)&=\sum_{\alpha,\beta}\left(A'_x\sin(i\alpha)+B'_x\cos(i\alpha)\right)\left(A'_y\sin(i\beta)+B'_y\cos(i\beta)\right)\left(A'_z\sin(i\sqrt{\alpha^2+\beta^2})+B'_x\cos(i\gamma)\right)
\end{align}$$









## Cylindrical Coordinates
Suppose we have the Laplacian:
$$\begin{align}
\vec\nabla^2\Phi&=\dfrac{1}{\rho}\dfrac{\partial}{\partial\rho}\left(\rho\dfrac{\partial\Phi}{\partial\rho}\right)+\dfrac{1}{\rho^2}\dfrac{\partial^2\Phi}{\partial\phi^2}+\dfrac{\partial^2\Phi}{\partial z^2}=0
\end{align}$$
Let $\Phi(\rho,\phi,z)=P(\rho)\Phi(\phi)Z(z)$, then:
$$\begin{align}
\dfrac{1}{P(\rho)}\dfrac{1}{\rho}\dfrac{\partial}{\partial\rho}\left(\rho\dfrac{\partial}{\partial\rho}P(\rho)\right)+\dfrac{1}{\Phi(\phi)}\dfrac{1}{\rho^2}\dfrac{\partial^2}{\partial\phi^2}\Phi(\phi)+\dfrac{1}{Z(z)}\dfrac{\partial^2}{\partial z^2}Z(z)&=0
\end{align}$$
We start with the angular part:
$$\begin{align}
\dfrac{1}{\Phi(\phi)}\dfrac{\partial^2\Phi(\phi)}{\partial\phi^2}&=-m^2 &\implies&& \Phi(\phi)&=e^{\pm_\phi im\phi}
\end{align}$$
For the z-component:
$$\begin{align}
\dfrac{1}{Z(z)}\dfrac{\partial^2Z(z)}{\partial z^2}&=k^2 &\implies&& Z(z)&=e^{\pm_z kz}
\end{align}$$
The radial equation simplifies to:
$$\begin{align}
\rho^2P''(\rho)+\rho P'(\rho)+\left(\rho^2k^2-m^2\right)P(\rho)&=0
\end{align}$$
The solutions to these are just the Bessel functions:
$$\begin{align}
P_{km}(\rho)&=AJ_m(k\rho)+BY_m(k\rho)
\end{align}$$
In total, the general solution is just:
$$\begin{align}
\Phi(\rho,\phi,z)&=\sum_{m=-\infty}^\infty\int_{0}^\infty\left(A_{km}J_m(k\rho)+B_{km}Y_m(k\rho)\right)\left(A_k' e^{-kz}+B_k' e^{kz}\right)\left(A_m'' e^{-im\phi}+B_m'' e^{im\phi}\right)\ dk
\end{align}$$
















