
## Notation and Conventions
### Relativity
Metric Tensor (Minkowski Space)
$$\begin{align}
g_{\mu\nu}\equiv\left[\begin{array}{}
1&0&0&0\\0&-1&0&0\\0&0&-1&0\\0&0&0&-1
\end{array}\right]
\end{align}$$
Spacetime components
$$\begin{align}
x^\mu&=(ct,\vec{x}) & x_\mu&=(ct,-\vec{x})\\
p^\mu&=(E/c,\vec{p}) & p_\mu&=(E/c,-\vec{p})\\
\end{align}$$
Dot products
$$\begin{align}
x\cdot x&=c^2t^2-\vec{x}\cdot\vec{x} &&&
p\cdot x&=Et-\vec{p}\cdot\vec{x} &&&
p\cdot p&=E^2/c^2-\vec{p}\cdot\vec{p}=m^2
\end{align}$$
Derivative operator
$$\begin{align}
\partial_\mu=\dfrac{\partial}{\partial x^\mu}&=\left(\dfrac{\partial}{\partial(ct)},\vec\nabla\right) & 
\partial^\mu&=\left(\dfrac{\partial}{\partial(ct)},-\vec\nabla\right)
\end{align}$$
### Quantum Mechanics
Energy and Momentum operators
$$\begin{align}
\hat{E}&\equiv i\hbar\dfrac{\partial}{\partial t} &
\vec{p}&\equiv-i\vec\nabla
&\implies&&
p_\mu&=i\partial_\mu,\ p^\mu=i\partial^\mu
\end{align}$$
Pauli matrices
$$\begin{align}
\sigma^i\sigma^j&=\delta^{ij}+i\epsilon^{ijk}\sigma^k
\end{align}$$
### Fourier Transforms & Distributions
Heaviside step function
$$\begin{align}
\theta(x)&=\begin{cases}0&x<0\\1&x>0\end{cases} & \delta(x)&=\dfrac{d}{dx}\theta(x)
\end{align}$$
Dirac delta function
$$\begin{align}
\int d^nx\ \delta^{(4)}(\vec{x})&=1
\end{align}$$
Fourier transform
$$\begin{align}
f(x)&=\int\dfrac{d^4x}{(2\pi)^4}e^{-ik\cdot x}\tilde{f}(k)
&\iff&&
f(x)&=\int d^4x\ e^{+ik\cdot x}f(x)
\end{align}$$
$$\begin{align}
\int d^4x\ e^{+ik\cdot x}&=(2\pi)^4\delta^{(4)}(k)
\end{align}$$

