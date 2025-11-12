
Let an information field $\rho=\rho(x^\mu)$, the density matrix field, exist.
Von Neumann showed that:
$$\begin{align}
S[\rho]&=-\text{Tr}\left(\rho\log\rho\right)
\end{align}$$
where $\rho$ is Hermitian, positive semi-definite, and normalized $\text{Tr}(\rho)=1$
This density matrix contains probabilities. However, when we write this in the wave equation form:
$$\begin{align}
\left(D_\mu D^\mu+\dfrac{m^2c^2}{\hbar^2}\right)\rho&=0
\end{align}$$
The probability current is analogous to Klein-Gordon's and written as:
$$\begin{align}
j^\mu&=\dfrac{i\hbar}{2m}\left(\rho^\dagger D^\mu\rho-\rho D^\mu\rho^\dagger\right)
\end{align}$$
Similarly, the current is not necessarily positive just like Klein-Gordon.




### The "Dirac Entropy" Field
To restore the phase factor, let:
$$\begin{align}
\Pi&=\Pi(x^\mu)\\
\rho&=\Pi\Pi^\dagger
\end{align}$$
The field $\Pi$ is dynamical, analogous to the Dirac spinor.
It encodes all information about $\rho$ while allowing for first-order dynamics.
It also must be unitless, since $\rho$ is also unitless.


### Entropic Gauge Field
Let's define some unitary transformation $\Pi'=U(x)\Pi$.
To preserve invariance under local unitary operations:
$$\begin{align}
\Pi&=\Pi(x^\mu)\\
D_\mu\Pi&=\partial_\mu\Pi+[B_\mu,\Pi]
\end{align}$$
We can also define a field strength tensor:
$$\begin{align}
S_{\mu\nu}&=\partial_\mu B_\nu-\partial_\nu B_\mu+[B_\mu,B_\nu]
\end{align}$$
With the transformation rule:
$$\begin{align}
B_\mu'&=UB_\mu U^\dagger-\left(\partial_\mu U\right)U^\dagger
\end{align}$$
### The "Dirac Entropy" Equation
We must satisfy the property that:
$$\begin{align}
\{\Gamma^\mu,\Gamma^\nu\}=2g^{\mu\nu}\mathbb{I}
\end{align}$$
Which means we can write a Dirac Entropy equation as:
$$\begin{align}
\left(i\hbar\Gamma^\mu D_\mu-mc\right)\Pi&=0
\end{align}$$
In the case we square it, we recover the Klein Gordon equation again.


### The Entropic Lagrangian Density
We finally can then write an analogue to the Lagrange Density as:
$$\begin{align}
\mathcal{L}&=\text{Tr}\left[\left(i\hbar\Gamma^\mu D_\mu-mc\right)\Pi-\dfrac{1}{4}S_{\mu\nu}S^{\mu\nu}\right]
\end{align}$$
And it's associated conserved information current:
$$\begin{align}
J^\mu&=\text{Tr}\left(\Pi^\dagger\Gamma^\mu\Pi\right)\\
\partial_\mu J^\mu&=0
\end{align}$$

### Examples
Let's start with a 1+1 spacetime, using mostly-minus convention.
We can see, for this case, that:
$$\begin{align}
\Gamma^0&=\sigma_z & \Gamma^1=i\sigma_y
\end{align}$$
With the case of no gauge fields, we can write the Dirac-Entropy equation as:
$$\begin{align}
\left(i\hbar\Gamma^\mu D_\mu-mc\right)\Pi&=0\\
\left(i\hbar\Gamma^0 \partial_t+i\hbar\Gamma^1 \partial_x-mc\right)\Pi&=\\
\left(i\hbar\sigma_z\dfrac{\partial}{\partial t}-\hbar\sigma_y\dfrac{\partial}{\partial x}-mc\right)\Pi&=0\\
\end{align}$$
Let's start with $\Pi=u(p)\exp\left(-i\dfrac{Et}{\hbar}+i\dfrac{px}{\hbar}\right)$, then we find that:
$$\begin{align}
\left(i\hbar\sigma_z(-iE/\hbar)-\hbar\sigma_y(ip/\hbar)-mc\right)\Pi&=0\\
\left(\sigma_zE-i\sigma_yp-mc\mathbb{I}\right)\cdot u(p)&=0\\
\end{align}$$
Which then leads to:
$$\begin{align}
E^2-p^2=(mc)^2
\end{align}$$
We can then find the current density as:
$$\begin{align}
J^\mu&=\text{Tr}\left(\Pi^\dagger\Gamma^\mu\Pi\right)\\
&=\text{Tr}\left(u^\dagger(p)\exp\left(i\dfrac{Et}{\hbar}-i\dfrac{px}{\hbar}\right)\Gamma^\mu u(p)\exp\left(-i\dfrac{Et}{\hbar}+i\dfrac{px}{\hbar}\right)\right)\\
\Aboxed{J^\mu&=\text{Tr}\left(u^\dagger\Gamma^\mu \right)}\\
\Aboxed{J^0&=\text{Tr}\left(u^\dagger\sigma_zu\right)}\\
\Aboxed{J^1&=i\text{Tr}\left(u^\dagger\sigma_yu\right)}\\
\end{align}$$
We can find the density matrix as:
$$\begin{align}
\rho&=\Pi^\dagger\Gamma^\mu\Pi\\
&=u^\dagger(p)\exp\left(i\dfrac{Et}{\hbar}-i\dfrac{px}{\hbar}\right)u(p)\exp\left(-i\dfrac{Et}{\hbar}+i\dfrac{px}{\hbar}\right)\\
\Aboxed{\rho&=u^\dagger(p)u(p)}\\
\end{align}$$
And who's entropy...


