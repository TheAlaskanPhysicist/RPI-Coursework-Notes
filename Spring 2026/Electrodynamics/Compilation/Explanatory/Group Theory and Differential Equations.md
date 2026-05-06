


## Part 1: The Laplacian
In the case where we have a much simpler system, being a linear operator $\vec\nabla^2$, we have:
$$\begin{align}
\vec\nabla^2\Phi&=\dfrac{1}{\sqrt{|g|}}\dfrac{\partial}{\partial x^i}\left(\sqrt{|g|}g^{ij}\dfrac{\partial}{\partial x^j}\right)
\end{align}$$





### Cartesian Laplacian $(N=3)$, Normally
We start with the Poisson's equation in rectangular coordinates:
$$\begin{align}
\vec\nabla^2\Phi(\vec{x})&=\dfrac{\partial^2\Phi}{\partial x^2}+\dfrac{\partial^2\Phi}{\partial y^2}+\dfrac{\partial^2\Phi}{\partial z^2}=-\dfrac{1}{\epsilon_0}\rho(\vec{x})
\end{align}$$
Since the coordinate basis is orthogonal, we can decompose the function as individual functions of the different coordinate directions:
$$\begin{align}
\Phi(x,y,z)&=X(x)Y(y)Z(z)
\end{align}$$
Solutions to which are of the following form:
$$\begin{align}
X(x)&=A_xe^{ik_xx}+B_xe^{-ik_xx} & Y(y)&=A_ye^{ik_yy}+B_ye^{-ik_yy} & Z(z)&=A_ze^{ik_zz}+B_ze^{-ik_zz}
\end{align}$$
While not proper notation, it will be convenient to write this for only 1 term of each:
$$\begin{align}
\Phi_H(\vec{x})&=\int_{k_x^2+k_y^2+k_z^2=0}J\ d^3k\ A(k_x,k_y,k_z)e^{ik_xx}e^{ik_yy}e^{ik_zz}
\end{align}$$
We can invert this equation to find find the components:
$$\begin{align}
A(k_x,k_y,k_z)&=\int_{k_x^2+k_y^2+k_z^2=0}J\ d^3x\ e^{-ik_xx}e^{-ik_yy}e^{-ik_zz} \ \Phi_H(\vec{x})
\end{align}$$
To make it clearer we're doing group theory, lets define represent the functions more generally.


### Laplacian as Functional Groups (with Position Basis)
Let scalar fields $\Phi$ and $\rho$ be defined on domain $\Omega$ with boundary $\partial\Omega$.
$$\begin{align}
\Phi,\rho&\in\mathcal{F}(\Omega) & \Omega\subseteq\mathbb{R}^N
\end{align}$$
The Laplacian of $\Phi$ is proportional to source field $\rho$:
$$\begin{align}
\vec\nabla^2\Phi&=-\dfrac{1}{\epsilon_0}\rho
\end{align}$$
Assume there exists a complete set of orthogonal eigenfunctions of the Laplacian, thus it is separatable in $N$ coordinates $x_1,x_2,\dots,x_N$:
$$\begin{align}
\Phi_{\vec{k}}(\vec{x})&=\prod_{i=1}^N X_{k_i}(x_i)
\end{align}$$
Each one-dimensional function $X_{k_i}$ satisfies boundary conditions along $x_i$. Orthogonality implies:
$$\begin{align}
\int_\Omega J(\vec{x})\ d^Nx\ \Phi^*_{\vec{k}'}(\vec{x})\Phi_{\vec{k}}(\vec{x})=\left|\Phi_{\vec{k}}\right|^2\delta_{\vec{k},\vec{k}'}
\end{align}$$
where $J(\vec{x})$ is the (diagonal) Jacobian associated with the coordinate system.

The scalar field $\Phi$ can be expanded in this basis:
$$\begin{align}
\Phi(\vec{x})&=\int d^Nk\ \Phi_{\vec{k}}(\vec{x})\ \dfrac{1}{\left|\Phi_{\vec{k}}\right|^2}\int_\Omega J(\vec{x}')\ d^Nx'\ \Phi^*_{\vec{k}}(\vec{x}')\Phi(\vec{x}')
\end{align}$$
In the homogenous case ($\rho=0$), the eigenfunctions of the Laplacian takes the form:
$$\begin{align}
\vec\nabla^2\Phi_{\vec{k}}&=-\lambda(\vec{k})\Phi_{\vec{k}} & \implies &&
-\lambda(\vec{k})\int_\Omega J(\vec{x}')\ d^Nx'\ \Phi^*_{\vec{k}}(\vec{x}')\Phi(\vec{x}')&=0
\end{align}$$
For the non-homogenous case ($\rho\ne0$), we expand both $\Phi,\rho$ in the eigenbasis:
$$\begin{align}
\Phi(\vec{x})&=\int d^Nk\ \Phi_{\vec{k}}(\vec{x})\ \dfrac{1}{\left|\Phi_{\vec{k}}\right|^2}\int_\Omega J(\vec{x}')\ d^Nx'\ \Phi^*_{\vec{k}}(\vec{x}')\Phi(\vec{x}')\\
\rho(\vec{x})&=\int d^Nk\ \Phi_{\vec{k}}(\vec{x})\ \dfrac{1}{\left|\Phi_{\vec{k}}\right|^2}\int_\Omega J(\vec{x}')\ d^Nx'\ \Phi^*_{\vec{k}}(\vec{x}')\rho(\vec{x}')\\
\end{align}$$
The eigenfunctions reduce the Laplace equation to the following:
$$\begin{align}
\lambda(\vec{k})\int_\Omega J(\vec{x}')\ d^Nx'\ \Phi^*_{\vec{k}}(\vec{x}')\Phi(\vec{x}')&=\dfrac{1}{\epsilon_0}\int_\Omega J(\vec{x}')\ d^Nx'\ \Phi^*_{\vec{k}}(\vec{x}')\rho(\vec{x}')
\end{align}$$
It's actually easier to use braket notation for this relation, where:
$$\begin{align}
\lambda(\vec{k})\braket{\Phi_{\vec{k}}|\Phi}&=\dfrac{1}{\epsilon_0}\braket{\Phi_{\vec{k}}|\rho} &\implies&&
\braket{\Phi_{\vec{k}}|\Phi}&=\dfrac{1}{\epsilon_0\lambda(\vec{k})}\braket{\Phi_{\vec{k}}|\rho}
\end{align}$$


---
## Laplacian (Orthogonal Coordinates)
Let $\Omega\subseteq\mathbb{R}^N$ be a domain with boundary $\partial\Omega$. 
Let $\vec{x}=(x_1,x_2,\dots,x_N)$ be **any orthogonal coordinate basis**.
Define the *Jacobian* of the coordinate system $J(\vec{x})$, and let the scales factors be $h_i(\vec{x})$ so that:
$$\begin{align}
\vec\nabla^2\Phi(\vec{x})&=\dfrac{1}{J(\vec{x})}\sum_{i=1}^N\dfrac{\partial}{\partial x_i}\left(\dfrac{J(\vec{x})}{|h_i|^2}\dfrac{\partial}{\partial x_i}\right)\Phi(\vec{x})
\end{align}$$
where $h_i^2$ are the metric coefficients along each coordinate.

The Poisson equation with Dirichlet boundary conditions are:
$$\begin{align}
\vec\nabla^2\Phi(\vec{x})&=-\dfrac{1}{\epsilon_0}\rho(\vec{x})
& \Phi_{\partial\Omega}&=V(\vec{x})
& \vec{x}&\in\Omega 
\end{align}$$
The Green's function $G(\vec{x},\vec{x}')$ is the propagator of the Laplacian in $\Omega$, satisfying:
$$\begin{align}
\vec\nabla^2G(\vec{x},\vec{x}')&=-4\pi\delta^N(\vec{x}-\vec{x}')
& \left.G(\vec{x},\vec{x}')\right|_{\vec{x}\in\partial\Omega}&=0
& \vec{x},\vec{x}'&\in\Omega
\end{align}$$
For any source $\rho(\vec{x})$ and boundary $V(\vec{x})$:
$$\begin{align}
\Phi(\vec{x})&=\dfrac{1}{4\pi\epsilon_0}\int_{\Omega}J(\vec{x})\ d^Nx'\ \rho(\vec{x}')G(\vec{x},\vec{x}')+V(\vec{x})
\end{align}$$
where the boundary condition is:
$$\begin{align}
V(\vec{x})&=\dfrac{1}{4\pi}\int_{\partial\Omega}dS'\left[G(\vec{x},\vec{x}')\dfrac{\partial\Phi(\vec{x}')}{\partial n'}-\Phi(\vec{x}')\dfrac{\partial G(\vec{x},\vec{x}')}{\partial n'}\right]
\end{align}$$
If we want to find the Green's function, we will need to expand in terms of Eigenfunctions.

Let $\left\{\Phi_{\vec{k}}(\vec{x})\right\}$ be any complete orthogonal set of eigenfunctions of the Laplacian in $\Omega$ with B.C.:
$$\begin{align}
\vec\nabla^2\Phi_{\vec{k}}(\vec{x})&=-\lambda(\vec{k})\Phi_{\vec{k}}(\vec{x})
& \Phi_{\vec{k}}(\vec{x}\in\partial\Omega)&=0
\end{align}$$
with orthogonality defined by the Jacobian:
$$\begin{align}
\int_\Omega J(\vec{x})\ d^Nx\ \Phi^*_{\vec{k}'}(\vec{x})\Phi_{\vec{k}}(\vec{x})&=\left|\Phi_{\vec{k}}\right|^2\delta_{\vec{k},\vec{k}'}
\end{align}$$
Then the Green's function is:
$$\begin{align}
G(\vec{x},\vec{x}')&=\sum_{\vec{k}}\dfrac{\Phi^*_{\vec{k}}(\vec{x}')\Phi_{\vec{k}}(\vec{x})}{\lambda(\vec{k})} && (\Omega\text{ Finite, Nice Boundary})\\
G(\vec{x},\vec{x}')&=\int_{\mathbb{R}^N}\dfrac{d^Nk}{(2\pi)^N}\ \dfrac{e^{i\vec{k}\cdot(\vec{x}-\vec{x}')}}{|\vec{k}|^2} && (\Omega=\mathbb{R}^N)
\end{align}$$
---
### Laplacian (Rectangular Coordinates)
In rectangular coordinates, we have the following orthonormal coordinate basis:
$$\begin{align}
\vec{x}&=(x_1,x_2,\dots,x_N) & x_i\in\mathbb{R}
\end{align}$$
Both the Jacobian and the scale factors are just $1$, and thus the Laplacian reduces to:
$$\begin{align}
\vec\nabla^2\Phi(\vec{x})&=\dfrac{1}{J(\vec{x})}\sum_{i=1}^N\dfrac{\partial}{\partial x_i}\left(\dfrac{J(\vec{x})}{|h_i|^2}\dfrac{\partial}{\partial x_i}\right)
&\implies&&
\vec\nabla^2\Phi(\vec{x})&=\sum_{i=1}^N\dfrac{\partial^2}{\partial x_i^2}\Phi(\vec{x})
\end{align}$$
The Poisson equation with Dirichlet boundary conditions is then:
$$\begin{align}
\vec\nabla^2\Phi(\vec{x})&=-\dfrac{1}{\epsilon_0}\rho(\vec{x})
& \Phi_{\partial\Omega}&=V(\vec{x})
& \vec{x}&\in\Omega\subseteq\mathbb{R}^N
\end{align}$$
The Green's function satisfies:
$$\begin{align}
\vec\nabla^2G(\vec{x},\vec{x}')&=-4\pi\delta^N(\vec{x}-\vec{x}')
& \left.G(\vec{x},\vec{x}')\right|_{\vec{x}\in\partial\Omega}&=0
& \vec{x},\vec{x}'&\in\Omega
\end{align}$$
Then the solution to Poisson's equation is:
$$\begin{align}
\Phi(\vec{x})&=\dfrac{1}{4\pi\epsilon_0}\int_{\Omega}d^Nx' G(\vec{x},\vec{x}')\rho(\vec{x}')+V(\vec{x})
\end{align}$$
with the boundary contribution:
$$\begin{align}
V(\vec{x})&=\dfrac{1}{4\pi}\int_{\partial\Omega}dS'\left[G(\vec{x},\vec{x}')\dfrac{\partial\Phi(\vec{x}')}{\partial n'}-\Phi(\vec{x}')\dfrac{\partial G(\vec{x},\vec{x}')}{\partial n'}\right]
\end{align}$$
Let $\left\{\Phi_{\vec{k}}(\vec{x})\right\}$ be any complete set of Laplacian eigenfunctions on $\Omega$ with Dirichlet boundary:
$$\begin{align}
\vec\nabla^2\Phi_{\vec{k}}(\vec{x})&=-\lambda(\vec{k})\Phi_{\vec{k}}(\vec{x})
& \Phi_{\vec{k}}(\vec{x}\in\partial\Omega)&=0
\end{align}$$
with orthogonality:
$$\begin{align}
\int_\Omega\ d^Nx\ \Phi^*_{\vec{k}'}(\vec{x})\Phi_{\vec{k}}(\vec{x})&=\left|\Phi_{\vec{k}}\right|^2\delta_{\vec{k},\vec{k}'}
\end{align}$$
### Finite-Volume Box
Suppose we have a finite-volume box, with a domain equal to the following:
$$\begin{align}
\Omega&=[0,L_1]\times[0,L_2]\times\dots\times[0,L_N] & \vec{x}&=(x_1,x_2,\dots,x_N)
\end{align}$$
The Laplacian eigenfunctions/eigenvalues that satisfy Dirichlet boundaries at all faces are:
$$\begin{align}
\Phi_{\vec{n}}(\vec{x})&=\prod_{i=1}^N\sqrt{\dfrac{2}{L_i}}\sin\left(\dfrac{n_i\pi x_i}{L_i}\right) & \lambda_{\vec{n}}&=\sum_{i=1}^N\left(\dfrac{n_i\pi}{L_i}\right)^2 & \vec{n}&\in\mathbb{N}^N
\end{align}$$
The Green's function in the finite box is then explicitly:
$$\begin{align}
G(\vec{x},\vec{x}')&=\dfrac{4^N\pi}{\prod_i L_i}\sum_{\vec{n}\in\mathbb{N}^N}\dfrac{\prod_{i=1}^N\sin\left(\tfrac{n_i\pi x_i}{L_i}\right)\sin\left(\tfrac{n_i\pi x_i'}{L_i}\right)}{\sum_{i=1}^N\left(\tfrac{n_i\pi}{L_i}\right)^2}
\end{align}$$
### Infinite-Volume Box
Suppose we instead have an infinite-volume box:
$$\begin{align}
\Omega&=\mathbb{R}^N & \vec{x}&=(x_1,x_2,\dots,x_N)
\end{align}$$
The Laplacian eigenfunctions/eigenvalues are then plane waves:
$$\begin{align}
\Phi_{\vec{k}}(\vec{x})&=e^{i\vec{k}\cdot\vec{x}} & \lambda_{\vec{k}}&=|\vec{k}|^2 &
\vec{k}\in\mathbb{R}^N
\end{align}$$
The Green's function in the whole space is then explicitly:
$$\begin{align}
G(\vec{x},\vec{x}')&=\int_{\mathbb{R}^N}\dfrac{d^Nk}{(2\pi)^N}\dfrac{e^{i\vec{k}\cdot(\vec{x}-\vec{x}')}}{|\vec{k}|^2}
\end{align}$$
The Green's function evaluation is dependent on the number dimensions:
$$\begin{align}
N&=1 & G(\vec{x},\vec{x}')&=2\pi|\vec{x}-\vec{x}'|\\
N&=2 & G(\vec{x},\vec{x}')&=\dfrac{1}{2\pi}\ln\left(\dfrac{1}{|\vec{x}-\vec{x}'|}\right)\\
N&\ge3 & G(\vec{x},\vec{x}')&=\dfrac{\Gamma\left(\tfrac{N}{2}-1\right)}{4\pi^{N/2}}\dfrac{1}{|\vec{x}-\vec{x}'|^{N-2}}
\end{align}$$
For a general potential, we then get:
$$\begin{align}
\Phi(\vec{x})&=\dfrac{1}{2\epsilon_0}\int_{-\infty}^\infty dx'\ \rho(x')|x-x'|
&& N=1\\
\Phi(\vec{x})&=\dfrac{1}{8\pi^2\epsilon_0}\int_{\mathbb{R}^2}d^2x'\rho(\vec{x}')\ln\left(\dfrac{1}{|\vec{x}-\vec{x}'|}\right)
&& N=2\\
\Phi(\vec{x})&=\dfrac{1}{4\pi\epsilon_0}\dfrac{\Gamma\left(\tfrac{N}{2}-1\right)}{4\pi^{N/2}}\int_{\mathbb{R}^N}d^Nx'\ \dfrac{\rho(\vec{x}')}{|\vec{x}-\vec{x}'|^{N-2}}
&& N\ge3
\end{align}$$
Since $V(x)$ decays to $0$ at infinity, thus no contribution.

---
### Laplacian (Spherical Coordinates, 3D)
In $3$-dimensional spherical coordinates, we define:
$$\begin{align}
\vec{r}&=(r,\theta,\phi) & r&\ge0,\ \theta\in[0,\pi],\ \phi\in[0,2\pi)
\end{align}$$
The Laplacian, after substitution, reduces to:
$$\begin{align}
\vec\nabla^2\Phi(\vec{r})&=\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial\Phi(\vec{r})}{\partial r}\right)+\dfrac{1}{r^2\sin\theta}\dfrac{\partial}{\partial\theta}\left(\sin\theta\dfrac{\partial\Phi(\vec{r})}{\partial\theta}\right)+\dfrac{1}{r^2\sin^2\theta}\dfrac{\partial^2\Phi(\vec{r})}{\partial\phi^2}
\end{align}$$
The Poisson equation with Dirichlet boundary conditions is then:
$$\begin{align}
\vec\nabla^2\Phi(\vec{r})&=-\dfrac{1}{\epsilon_0}\rho(\vec{r})
& \Phi_{\partial\Omega}&=V(\vec{r})
& \vec{r}&\in\Omega\subseteq\mathbb{R}^3
\end{align}$$
The Green's function satisfies:
$$\begin{align}
\vec\nabla^2G(\vec{r},\vec{r}')&=-4\pi\delta^N(\vec{r}-\vec{r}')
& \left.G(\vec{r},\vec{r}')\right|_{\vec{r}\in\partial\Omega}&=0
& \vec{r},\vec{r}'&\in\Omega
\end{align}$$
Then the solution to Poisson's equation is:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\int_{\Omega}d^3r'\  G(\vec{r},\vec{r}')\rho(\vec{r}')+V(\vec{r})
\end{align}$$
with the boundary contribution:
$$\begin{align}
V(\vec{r})&=\dfrac{1}{4\pi}\int_{\partial\Omega}dS'\left[G(\vec{r},\vec{r}')\dfrac{\partial\Phi(\vec{r}')}{\partial n'}-\Phi(\vec{r}')\dfrac{\partial G(\vec{r},\vec{r}')}{\partial n'}\right]
\end{align}$$
Let $\left\{\Phi_{klm}(\vec{r})\right\}$ be a complete set of Laplacian eigenfunctions on $\Omega$ with Dirichlet boundary:
$$\begin{align}
\vec\nabla^2\Phi_{klm}(\vec{r})&=-\lambda_{klm}\Phi_{klm}(\vec{r})
& \Phi_{klm}(\vec{r}\in\partial\Omega)&=0
\end{align}$$
with orthogonality:
$$\begin{align}
\int_\Omega\ d^3r\ \Phi^*_{k'l'm'}(\vec{r})\Phi_{klm}(\vec{r})&=\left|\Phi_{klm}\right|^2\delta_{kk'}\delta_{ll'}\delta_{mm'}
\end{align}$$
### Finite-Volume Sphere
Suppose we have a finite-volume sphere, with a domain equal to the following:
$$\begin{align}
\Omega&=[0,R]\times[0,\pi]\times[0,2\pi) & \vec{r}&=(r,\theta,\phi)
\end{align}$$
The Green's function in the finite sphere is:
$$\begin{align}
G(\vec{r},\vec{r}')&=\sum_{k,l,m}\dfrac{\Phi^*_{klm}(\vec{r}')\Phi_{klm}(\vec{r})}{\lambda_{klm}}
\end{align}$$
We can simplify this Green's function by assuming a functional decomposition:
$$\begin{align}
\Phi_{klm}(\vec{r})&=R_{kl}(r)Y_{lm}(\theta,\phi)
\end{align}$$
where $R_{kl}(r)$ is the radial function and $Y_{lm}(\theta,\phi)$ are the spherical harmonics.

Substituting into the Laplacian, we find that:
$$\begin{align}
\dfrac{1}{r^2R_{kl}(r)}\dfrac{d}{dr}\left(r^2\dfrac{dR_{kl}(r)}{dr}\right)+\dfrac{1}{r^2Y_{lm}(\theta,\phi)}\vec\nabla^2_{\mathbb{S}^2}Y_{lm}(\theta,\phi)&=-\lambda_{klm}
\end{align}$$
We can then separate these equations into the following:
$$\begin{align}
\Phi_{klm}(\vec{r})&=R_{kl}(r)Y_{lm}(\theta,\phi) & \lambda_{klm}&=\lambda_{kl}^{(r)}+\lambda_{lm}^{(\theta,\phi)}
\end{align}$$
These two new functions satisfy:
$$\begin{align}
\dfrac{1}{r^2}\dfrac{d}{dr}\left(r^2\dfrac{dR_{kl}(r)}{dr}\right)-\dfrac{\lambda_{lm}^{(\theta,\phi)}}{r^2}R_{kl}(r)&=-\lambda_{kl}^{(r)}R_{kl}(r)\\
\vec\nabla^2_{\mathbb{S}^2}Y_{lm}(\theta,\phi)&=-\lambda_{lm}^{(\theta,\phi)}Y_{lm}(\theta,\phi)
\end{align}$$
The Green's function of the finite sphere is then explicitly:
$$\begin{align}
G(\vec{r},\vec{r}')&=\sum_{k=1}^\infty\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{R^*_{kl}(r')R_{kl}(r)Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)}{\lambda_{kl}^{(r)}+l(l+1)}
\end{align}$$
... continue later when not starving.




### Infinite-Volume Sphere
DO LATER


Suppose we instead have an infinite-volume sphere:
$$\begin{align}
\Omega&=\mathbb{R}^3 & \vec{r}&=(r,\theta,\phi)
\end{align}$$
The Laplacian eigenfunctions/eigenvalues are separated into two functions:
$$\begin{align}
\Phi_{\vec{k}}(\vec{x})&=e^{i\vec{k}\cdot\vec{x}} & \lambda_{\vec{k}}&=|\vec{k}|^2 &
\vec{k}\in\mathbb{R}^N
\end{align}$$
The Green's function in the whole space is then explicitly:
$$\begin{align}
G(\vec{x},\vec{x}')&=\int_{\mathbb{R}^N}\dfrac{d^Nk}{(2\pi)^N}\dfrac{e^{i\vec{k}\cdot(\vec{x}-\vec{x}')}}{|\vec{k}|^2}
\end{align}$$
The Green's function evaluation is dependent on the number dimensions:
$$\begin{align}
N&=1 & G(\vec{x},\vec{x}')&=2\pi|\vec{x}-\vec{x}'|\\
N&=2 & G(\vec{x},\vec{x}')&=\dfrac{1}{2\pi}\ln\left(\dfrac{1}{|\vec{x}-\vec{x}'|}\right)\\
N&\ge3 & G(\vec{x},\vec{x}')&=\dfrac{\Gamma\left(\tfrac{N}{2}-1\right)}{4\pi^{N/2}}\dfrac{1}{|\vec{x}-\vec{x}'|^{N-2}}
\end{align}$$
For a general potential, we then get:
$$\begin{align}
\Phi(\vec{x})&=\dfrac{1}{2\epsilon_0}\int_{-\infty}^\infty dx'\ \rho(x')|x-x'|
&& N=1\\
\Phi(\vec{x})&=\dfrac{1}{8\pi^2\epsilon_0}\int_{\mathbb{R}^2}d^2x'\rho(\vec{x}')\ln\left(\dfrac{1}{|\vec{x}-\vec{x}'|}\right)
&& N=2\\
\Phi(\vec{x})&=\dfrac{1}{4\pi\epsilon_0}\dfrac{\Gamma\left(\tfrac{N}{2}-1\right)}{4\pi^{N/2}}\int_{\mathbb{R}^N}d^Nx'\ \dfrac{\rho(\vec{x}')}{|\vec{x}-\vec{x}'|^{N-2}}
&& N\ge3
\end{align}$$
Since $V(x)$ decays to $0$ at infinity, thus no contribution.
