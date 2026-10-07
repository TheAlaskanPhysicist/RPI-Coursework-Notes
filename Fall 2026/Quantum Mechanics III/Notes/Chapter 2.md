
## Example of Time Evolution
Consider the propagator
$$\begin{align}
U(t)&=\bra{\vec{x}}e^{-i\hat{H}t/\hbar}\ket{\vec{x}_0}
\end{align}$$
In nonrelativistic quantum mechanics, $E=p^2/2m$, and so
$$\begin{align}
U(t)
&=\bra{\vec{x}}\left[\int\dfrac{d^3p}{(2\pi)^3}\ket{\vec{p}}\bra{\vec{p}}\right]e^{-i\hat{H}t/\hbar}\ket{\vec{x}_0}\\
&=\dfrac{1}{(2\pi)^3}\int d^3p\ \left<\vec{x}\middle|\vec{p}\right>e^{-i(t/2m\hbar)p^2}\left<\vec{p}\middle|\vec{x}_0\right>\\
&=\dfrac{1}{(2\pi)^3}\int d^3p\ e^{+i\vec{p}\cdot(\vec{x}-\vec{x}_0)}\ e^{-i(t/2m\hbar)p^2}\\
U(t)&=\left(\dfrac{m\hbar}{2\pi i t}\right)^{3/2}e^{-i(m\hbar/2t)(\vec{x}-\vec{x}_0)^2}
\end{align}$$
This expression is non-zero for all $\vec{x}$ and $t$, thus a particle can propagate between any 2 points in an arbitrarily short time. This breaks causality. If we instead use the relativistic energy $E=\sqrt{(pc)^2+(mc^2)^2}$, the propagator becomes:
$$\begin{align}
U(t)
&=\bra{\vec{x}}\left[\int\dfrac{d^3p}{(2\pi)^3}\ket{\vec{p}}\bra{\vec{p}}\right]e^{-i\hat{H}t/\hbar}\ket{\vec{x}_0}\\
&=\dfrac{1}{(2\pi)^3}\int d^3p\ \left<\vec{x}\middle|\vec{p}\right>e^{-i(ct/\hbar)\sqrt{p^2+(mc)^2}}\left<\vec{p}\middle|\vec{x}_0\right>\\
U(t)&=\dfrac{1}{(2\pi)^3}\int d^3p\ e^{+i\vec{p}\cdot(\vec{x}-\vec{x}_0)}e^{-i(ct/\hbar)\sqrt{p^2+(mc)^2}}
\end{align}$$
The solution to this is given in terms of Bessel functions. While this does maintain causality, it is much more complicated of an expression. QFT makes this much simpler.




## Classical Field Theory
### Lagrangian Fields
The construction of Lagrangian Fields start with the definition of action
$$\begin{align}
S=\int d^4x\ \mathcal{L}
\end{align}$$
Suppose we want to vary this action in terms of a field $\phi(x)$, then
$$\begin{align}
\delta S=\int d^4x\left(\dfrac{\partial\mathcal{L}}{\partial\phi}\delta\phi+\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}\delta(\partial_\mu\phi)+\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\partial_\nu\phi)}\delta(\partial_\mu\partial_\nu\phi)+\dots\right)
\end{align}$$
Using integration by parts, we can find that each of the components are of the form
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial(\partial_{N}\phi)}\delta\left(\partial_N\phi\right)&=\sum_{n=0}^N(-1)^{N-n}\binom{N}{n}\partial_{n}\left(\partial_{N-n}\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_{N}\phi)}\right)\delta\phi\right)
\end{align}$$
Substituting back into our variational action, we have that
$$\begin{align}
\delta S=\int d^4x\sum_{N=0}^\infty\sum_{n=0}^N(-1)^{N-n}\binom{N}{n}\partial_{n}\left(\partial_{N-n}\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_{N}\phi)}\right)\delta\phi\right)
\end{align}$$
If we separate out the terms who has no outer derivative, then we can write it as
$$\begin{align}
\delta S&=
\int d^4x\left[\sum_{N=0}^\infty(-1)^{N}\partial_{N}\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_{N}\phi)}\right)\right]\delta\phi\\

&+\int d^4x\ \partial_\mu\left[\sum_{N=1}^\infty\sum_{n=0}^{N-1}(-1)^{N-n-1}\binom{N}{n+1}\partial_{n}\left(\partial_{N-n-1}\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_{N}\phi)}\right)\delta\phi\right)\right]
\end{align}$$
We can write two functions and return our notation back to standard notation as
$$\begin{align}
\mathcal{E}[\phi]&=\sum_{N=0}^\infty(-1)^{N}\partial_{\mu_1}\partial_{\mu_2}\dots\partial_{\mu_N}\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_{\mu_1}\partial_{\mu_2}\dots\partial_{\mu_N}\phi)}\right)\\
\Theta^\mu[\phi;\delta\phi]&=\sum_{N=1}^\infty\sum_{n=0}^{N-1}(-1)^{N-n-1}\binom{N}{n+1}\partial_{\mu_1}\partial_{\mu_2}\dots\partial_{\mu_n}\left(\partial_{\mu_{n+1}}\partial_{\mu_{n+2}}\dots\partial_{\mu_{N-n-1}}\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_{\mu_1}\partial_{\mu_2}\dots\partial_{\mu_N}\phi)}\right)\delta\phi\right)\\
\delta S&=\int_\Omega d^4x\ \mathcal{E}[\phi]\ \delta\phi+\int_\Omega d^4x\ \partial_\sigma\Theta^\sigma[\phi;\delta\phi]
\end{align}$$
Then define the boundary integral as a new functional
$$\begin{align}
\mathcal{I}[\phi;\delta\phi]&=-\int_\Omega d^4x\ \partial_\rho\Theta^\rho=-\int_{\partial\Omega} d^3\Sigma_\rho\Theta^\rho[\phi;\delta\phi]
\end{align}$$
For the first variation of action $\delta S=0$, the equation becomes
$$\begin{align}
\int_\Omega d^4x\ \mathcal{E}[\phi]\ \delta\phi&=\mathcal{I}[\phi;\delta\phi]
\end{align}$$
When the boundary contribution vanishes for all allowed variations, we get that
$$\begin{align}
\int_{\partial\Omega} d^3\Sigma_\rho\Theta^\rho&=0
&\implies&&
\mathcal{E}[\phi]=0
\end{align}$$
Since this condition must hold for any variation $\delta\phi$, then we get the Euler-Lagrange equations:
$$\begin{align}
\Aboxed{\sum_{N=0}^\infty(-1)^{N}\partial_{\mu_1}\partial_{\mu_2}\dots\partial_{\mu_N}\left(\dfrac{\partial\mathcal{L}}{\partial(\partial_{\mu_1}\partial_{\mu_2}\dots\partial_{\mu_N}\phi)}\right)&=0}
\end{align}$$
### Noethers Theorem (Charge)
Suppose we have the variation in a Lagrangian density
$$\begin{align}
\delta\mathcal{L}&=\mathcal{E}[\phi]\ \delta\phi+\partial_\mu\Theta^\mu
\end{align}$$
Equating this to a current density, we get the condition
$$\begin{align}
\mathcal{E}[\phi]\ \delta\phi+\partial_\mu\left(\Theta^\mu-\mathcal{J}^\mu\right)&=0
\end{align}$$
Therefore the generalized Noether current is
$$\begin{align}
j^\mu&=\Theta^\mu-\mathcal{J}^\mu &&&\partial_\mu j^\mu&=-\mathcal{E}[\phi]\ \delta\phi
\end{align}$$
This conserves charge of the form
$$\begin{align}
Q(t)\equiv\int d^3x\ j^0=\int d^3x\left(\Theta^0-\mathcal{J}^0\right)
\end{align}$$
When the boundary contribution vanishes, we have that
$$\begin{align}
\mathcal{E}[\phi]&=0
&\implies&&
\Theta^\mu-\mathcal{J}^\mu\text{ conserved}
\end{align}$$
### Noethers Theorem (Spacetime Translation)
Suppose we have an infinitesimal translation $x^\mu\to x^\mu-a^\mu$, then our variation becomes
$$\begin{align}
\delta\phi&=a^\nu\partial_\nu\phi
&\implies&&
\Theta^\mu[\phi;\delta\phi]\to\Theta^\mu[\phi;a^\nu\partial_\nu\phi]
\end{align}$$
The variation in the Lagrangian density, then the Noether current is
$$\begin{align}
\delta\mathcal{L}&=a^\nu\partial_\nu\mathcal{L}=\partial_\mu(a^\mu\mathcal{L})
&\implies&&
j^\mu&=a^\nu\left(\Theta^\mu[\phi,\partial_\nu\phi]-\delta^\mu_\nu\mathcal{L}\right)
\end{align}$$
We can then define the energy-momentum tensor as the interior such that
$$\begin{align}
T^{\mu}_\nu&=\Theta^\mu[\phi,\partial_\nu\phi]-\delta^\mu_\nu\mathcal{L}
\end{align}$$
Now we have the general Noether identity
$$\begin{align}
\partial_\mu j^\mu&=-\mathcal{E}[\phi]a^\nu\partial_\nu\phi &\implies&& \partial_\mu T^\mu_\nu&=-\mathcal{E}[\phi]\ \partial_\nu\phi
\end{align}$$
When the boundary contribution vanishes, any allowed choice for $\phi$ implies
$$\begin{align}
\mathcal{E}[\phi]&=0
&\implies&&
\partial_\mu T^{\mu\nu}&=0
\end{align}$$
The conserved charges for the time and space are the Hamiltonian and the physical momentum:
$$\begin{align}
H&=\int d^3x\ T^{0}_0 & P_i&=\int d^3x\ T^{0}_i
\end{align}$$
### Hamiltonian Fields
For a Lagrangian that depends on all time derivatives, we define the generalized coordinates
$$\begin{align}
\phi,\dot\phi,\ddot\phi,\phi^{(3)},\dots
\end{align}$$
The generalized momenta are then
$$\begin{align}
\pi_k&=\sum_{r=0}^\infty(-1)^{r}\dfrac{\partial\mathcal{L}}{\partial\phi^{(k+r+1)}}
\end{align}$$
We can also express the Hamiltonian density using a Legendre transform
$$\begin{align}
\mathcal{H}&=\sum_{r=0}^\infty(-1)^{r}\dfrac{\partial\mathcal{L}}{\partial\phi^{(k+1+r)}}\phi^{(k+1)}-\mathcal{L}
\end{align}$$
The Hamiltonian can conveniently be found by variation like previously. If we vary the Lagrangian density with the time derivative of the field, we get that
$$\begin{align}
\delta\phi&=\partial_0\phi
&\implies&&
T^{0}_0&=\Theta^0[\phi,\partial_0\phi]-\mathcal{L}
\end{align}$$
Therefore the generalized Hamiltonian is just
$$\begin{align}
\delta\phi&=\partial_0\phi
&\implies&&
H&=\int d^3x\left(\Theta[\phi,\dot\phi]-\mathcal{L}\right)
\end{align}$$
This process is identical to integrating over the hypersurface of equal time, thus
$$\begin{align}
\delta\phi&=\partial_0\phi
&\implies&&
H(t)&=\int_{\Sigma(t)} d^3x\left(\Theta[\phi,\dot\phi]\right)-L(t)
\end{align}$$
Relating back to the Legendre transform, therefore these can be equated as
$$\begin{align}
\Theta[\phi,\dot\phi]&=\sum_{r=0}^\infty(-1)^{r}\dfrac{\partial\mathcal{L}}{\partial\phi^{(k+1+r)}}\phi^{(k+1)}
\end{align}$$
The temporal component of the variational boundary current is the generalized Legendre term. Thus the more compact way of writing the Legendre transform is using this functional
$$\begin{align}
\Aboxed{\mathcal{H}&=\Theta[\phi,\dot\phi]-\mathcal{L}}
\end{align}$$
### Noethers Theorem (Spacetime Scaling)
Suppose we have an infinitesimal scaling $x^\mu\to (1+\epsilon)x^\mu$, then our variation is
$$\begin{align}
\delta\phi&=\epsilon x^\nu\partial_\nu\phi
&\implies&&
\Theta^\mu[\phi;\delta\phi]\to\Theta^\mu[\phi;\epsilon x^\nu\partial_\nu\phi]
\end{align}$$
The Noether current is
$$\begin{align}
j^\mu&=\Theta^\mu[\phi,\epsilon x^\nu\partial_\nu\phi]-\mathcal{J}^\mu
\end{align}$$
We can define a dilation current such that
$$\begin{align}
D^\mu&=\Theta^\mu[\phi,x^\nu\partial_\nu\phi]-\dfrac{1}{\epsilon}\mathcal{J}^\mu
&j^\mu=\epsilon D^\mu
\end{align}$$
For a scaling transformation, the Noether identity is
$$\begin{align}
\partial_\mu D^\mu&=-\mathcal{E}[\phi]x^\nu\partial_\nu\phi
\end{align}$$
When the boundary contribution vanishes, any allowed choice for $\phi$ implies
$$\begin{align}
\mathcal{E}[\phi]&=0
&\implies&&
\partial_\mu D^\mu=0
\end{align}$$
The corresponding dilation charge is
$$\begin{align}
Q_D(t)&=\int_{\Sigma_t} d^3x\ D^{0}
\end{align}$$
The Hamiltonian and the physical momentum are also still present under a scaling dimension with transformation $\delta\phi=\epsilon\left(x^\nu\partial_\nu+\Delta\right)\phi$.
$$\begin{align}
H&=\int d^3x\ T^{0}_0 & P_i&=\int d^3x\ T^{0}_i
\end{align}$$


