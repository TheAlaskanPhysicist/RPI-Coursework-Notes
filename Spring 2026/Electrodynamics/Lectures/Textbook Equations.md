
Maxwells Equations:
$$\begin{align}
\vec\nabla\cdot\vec{D}&=\rho & 
\vec\nabla\times\vec{E}-\dfrac{\partial\vec{B}}{\partial t}&=0 && \text{(I.1)}\\
\vec\nabla\cdot\vec{B}&=0 &
\vec\nabla\times\vec{H}-\dfrac{\partial\vec{D}}{\partial t}&=\vec{J}\\
\end{align}$$
Continuity equation:
$$\begin{align}
\dfrac{\partial\rho}{\partial t}+\vec\nabla\cdot\vec{J}&=0 && \text{(I.2)}
\end{align}$$
Lorentz Force Law:
$$\begin{align}
\vec{F}&=q\left(\vec{E}+\vec{v}\times\vec{B}\right) && \text{(I.3)}
\end{align}$$


In Vacuum, $\vec{E}$ and $\vec{B}$ are linear (Maxwellian).
 - In QFT, this is not the case due to uncertainty.

For slow-varying fields, our fields can be written as:
$$\begin{align}
\dfrac{\vec{D}}{\epsilon_0}&=\sum_k\epsilon_{ik}E_k & \dfrac{\vec{B}}{\mu_0}&=\sum_k\mu_{ik}H_k && \text{(I.5)}\\
\end{align}$$
where these $\epsilon_{ik}$, $\mu_{ik}$ tensors of the vacuum:
$$\begin{align}
\epsilon_{ik}=\delta_{ik}+\dfrac{e_G^4\hbar}{45\pi m^4c^7}\left[2(\vec{E}^2-c^2\vec{B}^2)\delta_{ik}+7c^2B_iB_k\right]+\dots && \text{(I.5)}\\
\mu_{ik}=\delta_{ik}+\dfrac{e_G^4\hbar}{45\pi m^4c^7}\left[2(c^2\vec{B}^2-\vec{E}^2)\delta_{ik}+7c^2E_iE_k\right]+\dots\\
\end{align}$$
The exact results come from Electromagnetic Tensor theory.



A more generally expression for $\vec{D}$ and $\vec{H}$, as well as current density $\vec{J}$:
$$\begin{align}
\vec{D}&=\vec{D}[\vec{E},\vec{B}] & \vec{H}&=\vec{H}[\vec{E},\vec{B}] & \vec{J}&=\vec{J}[\vec{E},\vec{B}]
\end{align}$$
where $[]$ signify that the connections might not be simple and may depend on history.







---
## Chapter 1
---
### Coulomb's Law and Electric Field
Coulomb's Law and Electric Field of Point Charge:
$$\begin{align}
\vec{F}(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}qq' && \text{(1.2)} \\
\vec{F}(\vec{r})&=q\vec{E}(\vec{r}) && \text{(1.1)} \\
\vec{E}(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}q' && \text{(1.3)}
\end{align}$$
For a distribution of charge, whether discrete or continuous:
$$\begin{align}
\vec{E}(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\sum_i\dfrac{\vec{r}-\vec{r}_i}{|\vec{r}-\vec{r}_i|^3}q_i && \text{(1.4)} \\
\vec{E}(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\int_\Omega\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}\rho(\vec{r}')\ d^3r' && \text{(1.5)}
\end{align}$$
If we want to represent a charge density of point charges, we can utilize the Dirac delta function:
$$\begin{align}
\rho(\vec{r})&=\textstyle\sum_i q_i\delta(\vec{r}-\vec{r}_i) && \text{(1.6)}
\end{align}$$
---
### Gauss's Law
Gauss's Law relates electric flux (density) to charge (density):
$$\begin{align}
\oint_{\partial\Omega}\vec{E}(\vec{r})\cdot d^2\vec\Sigma&=\dfrac{1}{\epsilon_0}\int_\Omega\rho(\vec{r})\ d^3r
&\iff&&
\vec\nabla\cdot\vec{E}(\vec{r})&=\dfrac{1}{\epsilon_0}\rho(\vec{r}) && \text{(1.11, 1.13)}
\end{align}$$
---
### Scalar Potential
Knowledge of the divergence and curl of $\vec{E}$, up to the addition of a gradient of a function that is an element of the Kernel of the Laplacian, uniquely defines electric field.

For a scalar potential, when $\vec\nabla\times\vec{E}=0$, integration by parts reveals that:
$$\begin{align}
\vec{E}(\vec{r})&=-\dfrac{1}{4\pi\epsilon_0}\vec{\nabla}\int_\Omega\dfrac{1}{|\vec{r}-\vec{r}'|}\rho(\vec{r}')\ d^3r' && \text{(1.15)}\\
\vec{E}(\vec{r})&=-\vec{\nabla}\Phi(\vec{r}) && \text{(1.16)}\\
\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\int_\Omega\dfrac{1}{|\vec{r}-\vec{r}'|} \rho(\vec{r}')\ d^3r' && \text{(1.17)}
\end{align}$$
---
### Electromechanical Work
The work done in moving a charge on a path $\gamma:[a,b]\rightarrow\mathbb{R}^3$:
$$\begin{align}
W&=-\int_\gamma\vec{F}(\vec{r})\cdot d\vec{r}=-q\int_\gamma\vec{E}(\vec{r})\cdot d\vec{r} && \text{(1.18)}
\end{align}$$
For a conservative field $\vec{E}$, we can substitute our gradient of the scalar potential:
$$\begin{align}
W&=q\int_\gamma\vec{\nabla}\Phi(\vec{r})\cdot d\vec{r}=q\left[\Phi(b)-\Phi(a)\right] && \text{(1.19)}
\end{align}$$
Returning to our field integral, we have the two identities:
$$\begin{align}
\int_\gamma\vec{E}(\vec{r})\cdot d\vec{r}&=-\left[\Phi(b)-\Phi(a)\right] && \text{(1.20)} \\
\oint\vec{E}(\vec{r})\cdot d\vec{r}&=0 && \text{(1.21)} \\
\end{align}$$
---
### Electric Charge Interfaces
For an oriented surface $\partial\Omega$ with unit normal $\hat{n}$, the field discontinuity is written as:
$$\begin{align}
[\![\vec{E}(\vec{r})]\!]&\equiv\vec{E}^+(\vec{r})-\vec{E}^-(\vec{r}) & 
\vec{E}^\pm(\vec{r})&=\lim_{\epsilon\to0}\vec{E}(\vec{r}\pm\epsilon\hat{n})
\end{align}$$
Gauss's Law over this surface is then:
$$\begin{align}
\oint_{\partial\Omega}[\![\vec{E}(\vec{r})]\!]\cdot d^2\vec\Sigma&=\dfrac{1}{\epsilon_0}\int_{\partial\Omega}\sigma(\vec{r})\ d^2\Sigma
&\iff&&
[\![\vec{E}(\vec{r})]\!]\cdot\hat{n}&=\dfrac{1}{\epsilon_0}\rho(\vec{r}) && \text{(1.22)}
\end{align}$$
The potential from this surface charge is similar to before:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\int_{\partial\Omega}\dfrac{1}{|\vec{r}-\vec{r}'|} \sigma(\vec{r}')\ d^2\Sigma' && \text{(1.23)}
\end{align}$$
---
### Poisson & Laplace Equations
An electrostatic (conservative) field can be described by two differential equations:
$$\begin{align}
\vec\nabla\cdot\vec{E}(\vec{r})&=\dfrac{1}{\epsilon_0}\rho(\vec{r}) &
\vec\nabla\times\vec{E}(\vec{r})&=0 && \text{(1.13, 1.14)}
\end{align}$$
Since our field can be written as the gradient of a potential, we get the differential equation:
$$\begin{align}
\vec\nabla^2\Phi(\vec{r})&=-\dfrac{1}{\epsilon_0}\rho(\vec{r}) & 
\vec\nabla^2\Phi(\vec{r})&=0 && \text{(1.28, 1.29)}
\end{align}$$
These are the Poisson and Laplace equations respectively. The Green's function for this is:
$$\begin{align}
\vec\nabla'^2\left(\dfrac{1}{|\vec{r}-\vec{r}'|}\right)&=-4\pi\delta(\vec{r}-\vec{r}') && \text{(1.31)}
\end{align}$$
---
### Green's Theorem
We have Green's two identities:
$$\begin{align}
\int_\Omega\left[\phi(\vec{r}')\vec\nabla'^2\psi(\vec{r}')+\vec\nabla'\phi(\vec{r}')\cdot\vec\nabla'\psi(\vec{r}')\right]\ d^3r'
&=\oint_{\partial\Omega}\left[\phi(\vec{r}')\vec\nabla'\psi(\vec{r}')\right]\cdot d^2\vec\Sigma' && \text{(1.34)}\\
\int_\Omega\left[\phi(\vec{r}')\vec\nabla'^2\psi(\vec{r}')-\psi(\vec{r}')\vec\nabla'^2\phi(\vec{r}')\right]\ d^3r'
&=\oint_{\partial\Omega}\left[\phi(\vec{r}')\vec\nabla'\psi(\vec{r}')-\psi(\vec{r}')\vec\nabla'\phi(\vec{r}')\right]\cdot d^2\vec\Sigma' && \text{(1.35)}
\end{align}$$
Substituting functions that relate to the scalar potential, we get:
$$\begin{align}
\Phi(\vec{r})&=
\dfrac{1}{4\pi\epsilon_0}\int_\Omega\dfrac{1}{|\vec{r}-\vec{r}'|}\rho(\vec{r}')\ d^3r'+\dfrac{1}{4\pi}\oint_{\partial\Omega}\left[\dfrac{1}{|\vec{r}-\vec{r}'|}\vec\nabla'\Phi(\vec{r}')-\Phi(\vec{r}')\vec\nabla'\left(\dfrac{1}{|\vec{r}-\vec{r}'|}\right)\right]\cdot d^2\vec\Sigma'\ \ \ \ \text{(1.36)}\\
\end{align}$$
For both Dirichlet and Neumann boundary conditions, this potential is unique.

---
### Green's Function of the Laplacian
The potential of the point charge satisfies the equation:
$$\begin{align}
\vec\nabla'^2\left(\dfrac{1}{|\vec{r}-\vec{r}'|}\right)&=-4\pi\delta(\vec{r}-\vec{r}') && \text{(1.31)}
\end{align}$$
This is one of a class of functions called Green's functions. It takes the form:
$$\begin{align}
\vec\nabla'^2G(\vec{r},\vec{r}')&=-4\pi\delta(\vec{r}-\vec{r}') && \text{(1.39)} \\
G(\vec{r},\vec{r}')&=\dfrac{1}{|\vec{r}-\vec{r}'|}+F(\vec{r},\vec{r}') && \text{(1.40)}
\end{align}$$
Where $F(\vec{r},\vec{r}')$ is a function in the kernel of $\vec\nabla'^2$, as in $\vec\nabla'^2F(\vec{r},\vec{r}')=0$.

The scalar potential with one of these Green's functions is then:
$$\begin{align}
\Phi(\vec{r})&=
\dfrac{1}{4\pi\epsilon_0}\int_\Omega G(\vec{r},\vec{r}')\rho(\vec{r}')\ d^3r'+\dfrac{1}{4\pi}\oint_{\partial\Omega}\left[G(\vec{r},\vec{r}')\vec\nabla'\Phi(\vec{r}')-\Phi(\vec{r}')\vec\nabla'G(\vec{r},\vec{r}')\right]\cdot d^2\Sigma' && \text{(1.42)}
\end{align}$$
We can choose $F(\vec{r},\vec{r}')$ to cancel with one of the terms of the surface integral. 

For Dirichlet boundary conditions, we choose $F(\vec{r},\vec{r}')$ so that $G_D(\vec{r},\vec{r}')$ vanishes on a surface:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\int_\Omega G_D(\vec{r},\vec{r}')\rho(\vec{r}')\ d^3r'-\dfrac{1}{4\pi} \oint_{\partial\Omega}\left[\Phi(\vec{r}')\vec\nabla'G(\vec{r},\vec{r}')\right]\cdot d^2\Sigma' && \text{(1.44)}
\end{align}$$
For Neumann boundary conditions, it is a bit more complicated $\vec\nabla'G_N(\vec{r},\vec{r}')=-\dfrac{4\pi}{|\partial\Omega|}$:
$$\begin{align}
\Phi(\vec{r})&=\left\langle\Phi\right\rangle_{\partial\Omega}+
\dfrac{1}{4\pi\epsilon_0}\int_\Omega G_N(\vec{r},\vec{r}')\rho(\vec{r}')\ d^3r'+\dfrac{1}{4\pi}\oint_{\partial\Omega}\left[G_N(\vec{r},\vec{r}')\vec\nabla'\Phi(\vec{r}')\right]\cdot d^2\Sigma' && \text{(1.46)}\\
\end{align}$$
Where $|\partial\Omega|$ is the area of the surface integral.

---
### Electrostatic Potential Energy
There are many ways to write the potential energy.

In terms of charge distribution:
$$\begin{align}
W&=\dfrac{1}{8\pi\epsilon_0}\sum_{i\ne j}\dfrac{q_iq_j}{|\vec{r}_i-\vec{r}_j|} && \text{(1.51)} \\
W&=\dfrac{1}{8\pi\epsilon_0}\int_{\Omega\times\Omega}\dfrac{\rho(\vec{r})\rho(\vec{r}')}{|\vec{r}-\vec{r}'|}\ d^3r\ d^3r' && \text{(1.52)}
\end{align}$$
As a mix of charge distribution and electrostatic potential:
$$\begin{align}
W&=\dfrac{1}{2}\int_\Omega\rho(\vec{r})\Phi(\vec{r})\ d^3r && \text{(1.53)}
\end{align}$$
In terms of just electrostatic potential:
$$\begin{align}
W&=-\dfrac{\epsilon_0}{2}\int_\Omega\Phi(\vec{r})\vec\nabla^2\Phi(\vec{r})\ d^3r
\end{align}$$
By integrating by parts, we can write it terms of magnitudes:
$$\begin{align}
W&=\dfrac{\epsilon_0}{2}\int_\Omega\left|\vec\nabla\Phi(\vec{r})\right|^2\ d^3r && \text{(1.54)}\\
W&=\dfrac{\epsilon_0}{2}\int_\Omega\left|\vec{E}(\vec{r})\right|^2\ d^3r && \text{(1.54)}
\end{align}$$
Since this an integration over a volume, we can define an energy density:
$$\begin{align}
w(\vec{r})&=\dfrac{\epsilon_0}{2}\left|\vec{E}(\vec{r})\right|^2&& \text{(1.55)}
\end{align}$$
We can also write this energy density in terms of surface charge density:
$$\begin{align}
w(\vec{r})&=\dfrac{1}{2\epsilon_0}\sigma(\vec{r})^2 && \text{(1.59)}
\end{align}$$
### Capacitance
Capacitance relates the charge and potential of a surface, and energy as capacitance:
$$\begin{align}
Q_i&=\sum_{j}C_{ij}V_j && \text{(1.61)}\\
W&=\dfrac{1}{2}\sum_{i,j}C_{ij}V_iV_j && \text{(1.62)}
\end{align}$$
---
## Chapter 2
---
Something to note ahead of time, since I believe it to be very useful. The Green's function is also known as the *propagator*. In solving convolution systems for linear differential equations, effectively the correlation between two different points is represented by the Green's function, and when integrated gives a notion of "propagating" the conditional function.

The Method of Images effectively is constructing a Green's function from the original linear operator $L$ and adding extra terms for where you'd like the "propagation" to end. For example, on a surface of a conductor, the additional term is made so that $G(\text{surface})=0$.

Since this surface is encompassing, effectively any choice of propagation that starts in a region must stay within that region bounded by $G=0$, which naturally leads to having functional solutions to systems be dependent on whether you are in a particular region.

For the Laplacian operator, we have the following:
$$\begin{align}
G(\vec{r},\vec{r}')&=\dfrac{1}{|\vec{r}-\vec{r}'|}+F(\vec{r},\vec{r}') && \text{(1.40)}
\end{align}$$
To enforce boundaries where $G(\vec{r},\vec{r}')$ is zero, we must require that:
$$\begin{align}
\dfrac{1}{|\vec{r}-\vec{r}'|}+F(\vec{r},\vec{r}')&=0
\end{align}$$
The resulting function isn't a *real* charge distribution of the system, but it has the same *solution* for the potential of the system in the region we are considering.

For example, if we wanted to discontinue propagation of a point charge at the origin of charge $+Q$ with a sphere of radius $a$, we want $G(\vec{r},\vec{r}')=0$ when $|r'|=a$:
$$\begin{align}
G(\vec{r},\vec{r}')&=\dfrac{1}{|\vec{r}-\vec{r}'|}-\dfrac{a}{r'\left|\vec{r}-\dfrac{a^2}{r'^2}\vec{r}'\right|} && \text{(2.16)}
\end{align}$$
---
## Chapter 3
---
### Laplace Equation (Rectangular Coordinates)
The Laplace Equation in Rectangular Coordinates can be written as:
$$\begin{align}
\dfrac{\partial^2\Phi}{\partial x^2}+\dfrac{\partial^2\Phi}{\partial y^2}+\dfrac{\partial^2\Phi}{\partial z^2}&=0
\end{align}$$
Using separation variables, $\Phi=X(x)Y(y)Z(z)$, we get the following differential equations:
$$\begin{align}
\dfrac{1}{X}\dfrac{d^2X}{dx^2}&=-k_x^2 & X(x)&\propto e^{\pm ik_xx}\\
\dfrac{1}{Y}\dfrac{d^2Y}{dy^2}&=-k_y^2 & Y(y)&\propto e^{\pm ik_yy}\\
\dfrac{1}{Z}\dfrac{d^2Z}{dz^2}&=-k_z^2 & Z(z)&\propto e^{\pm ik_zz}
\end{align}$$
Where $|k_x|^2+|k_y|^2+|k_z|^2=0$ in order to satisfy the differential equation.

---
### Laplace Equation (Spherical Coordinates)
The Laplace Equation in Spherical Coordinates can be written as:
$$\begin{align}
\dfrac{1}{r}\dfrac{\partial^2}{\partial r^2}(r\Phi)+\dfrac{1}{r^2\sin\theta}\dfrac{\partial}{\partial\theta}\left(\sin\theta\dfrac{\partial\Phi}{\partial\theta}\right)+\dfrac{1}{r^2\sin^2\theta}\dfrac{\partial^2\Phi}{\partial\phi^2}&=0 && \text{(3.1)}
\end{align}$$
Using separation variables, $\Phi=\tfrac{1}{r}R(r)\Theta(\theta)\Phi(\phi)$, we get the following differential equations:
$$\begin{align}
\dfrac{1}{\Phi}\dfrac{\partial^2\Phi}{\partial\phi^2}&=-m^2 && \text{(3.4)} &&& \Phi(\phi)&\propto e^{im\phi} && \text{(3.5)} \\
\dfrac{\partial^2R}{\partial r^2}-\dfrac{l(l+1)}{r^2}R&=0 && \text{(3.7)} &&& R(r)&\propto r^{l+1},r^{-l} && \text{(3.8)}
\end{align}$$
$$\begin{align}
\dfrac{1}{\sin\theta}\dfrac{\partial}{\partial\theta}\left(\sin\theta\dfrac{\partial\Theta}{\partial\theta}\right)+\left[l(l+1)-\dfrac{m^2}{\sin^2\theta}\right]\Theta&=0 && \text{(3.6)}
\end{align}$$
In order to solve the polar differential equation, we can rewrite it into the following form:
$$\begin{align}
\dfrac{\partial}{\partial(\cos\theta)}\left((1-\cos^2\theta)\dfrac{\partial\Theta}{\partial(\cos\theta)}\right)+\left[l(l+1)-\dfrac{m^2}{1-\cos^2\theta}\right]\Theta&=0 && \text{(3.9)}
\end{align}$$
When we substitute $x=\cos\theta$, we get the form of the *Legendre equation*.

---
### Laplace Equation (Cylindrical Coordinates)
The Laplace Equation in Cylindrical Coordinates can be written as:
$$\begin{align}
\dfrac{1}{\rho}\dfrac{\partial}{\partial \rho}\left(\rho\dfrac{\partial\Phi}{\partial\rho}\right)+\dfrac{1}{\rho^2}\dfrac{\partial^2\Phi}{\partial\phi^2}+\dfrac{\partial^2\Phi}{\partial z^2}&=0 && \text{(3.71)}
\end{align}$$
Using separation variables, $\Phi=P(r)\Phi(\phi)Z(z)$, we get the following differential equations:
$$\begin{align}
\dfrac{1}{Z(z)}\dfrac{\partial^2Z(z)}{\partial\phi^2}&=+k^2 && \text{(3.73)} &&&
Z(z)&=A_z e^{kz}+B_z e^{-kz} && \text{(3.76)}\\
\dfrac{1}{\Phi(\phi)}\dfrac{\partial^2\Phi(\phi)}{\partial\phi^2}&=-\nu^2 && \text{(3.74)} &&& 
\Phi(\phi)&=A_\phi e^{i\nu\phi}+B_\phi e^{-i\nu\phi} && \text{(3.76)}\\
\end{align}$$
$$\begin{align}
\dfrac{\partial^2P}{\partial\rho^2}+\dfrac{1}{\rho}\dfrac{\partial P}{\partial\rho}+\left[k^2-\dfrac{\nu^2}{\rho^2}\right]P&=0 && \text{(3.75)}
\end{align}$$
In order to solve the radial differential equation, we can rewrite it into the following form:
$$\begin{align}
\dfrac{\partial^2P}{\partial(k\rho)^2}+\dfrac{1}{(k\rho)}\dfrac{\partial P}{\partial(k\rho)}+\left[1-\dfrac{\nu^2}{(k\rho)^2}\right]P&=0
\end{align}$$
When we substitute $x=k\rho$, we get the form of the *Bessel equation*.

---
### Boundary-Value Problems (Rectangular Coordinates)
Without imposing any explicit boundary conditions, we can write the potential as:
$$\begin{align}
\Phi(\vec{r})&\propto\int_{|\vec{k}|^2=0} e^{i\vec{k}\cdot\vec{r}}A(\vec{k})\ d^3k & \vec{r}\in\Omega,\ \vec{k}\in\mathbb{C}^3
\end{align}$$
The expansion around a unit point charge can be written as:
$$\begin{align}
\dfrac{1}{|\vec{r}-\vec{r}'|}&=\dfrac{1}{r_>}+\dfrac{\vec{r}\cdot\vec{r}'}{r^3_>}+\dfrac{3(\vec{r}\cdot\vec{r}')^2-r^2r'^2}{2r^5_>}+\dfrac{5(\vec{r}\cdot\vec{r}')^3-3r^2r'^2(\vec{r}\cdot\vec{r}')}{2r^7_>}+\dots
\end{align}$$
where $r_>=\max\left(r,r'\right)$ being the larger radius vector. This is the multipole expansion.

---
### Boundary-Value Problems (Spherical Coordinates)
Without imposing any explicit boundary conditions, we can write the potential as:
$$\begin{align}
\Phi(r,\theta,\phi)&=\sum_{l=0}^\infty\sum_{m=-l}^{+l} \left[A_{lm}r^l+\dfrac{B_{lm}}{r^{l+1}}\right]Y_{lm}(\theta,\phi) && \text{(3.61)}
\end{align}$$
The expansion around a unit point charge can be written as:
$$\begin{align}
\dfrac{1}{|\vec{r}-\vec{r}'|}&=\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{r^l_<}{r^{l+1}_>}\cdot\dfrac{4\pi}{2l+1}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi) && \text{(3.70)}
\end{align}$$
where $r_<,r_>$ is the smaller/larger magnitude of $r,r'$.

#### Azimuthal Symmetry
When we impose that the solution is invariant in $\phi$, $m=0$, the potential reduces to:
$$\begin{align}
\Phi(r,\theta)&=\sum_{l=0}^\infty\left[A_lr^l+\dfrac{B_l}{r^{l+1}}\right]P_l(\cos\theta) && \text{(3.33)}
\end{align}$$
The expansion around a unit point charge can be written as:
$$\begin{align}
\dfrac{1}{|\vec{r}-\vec{r}'|}&=\sum_{l=0}^\infty\dfrac{r^l_<}{r^{l+1}_>}P_l(\cos\gamma) && \text{(3.38)}
\end{align}$$
where $r_<,r_>$ is the smaller/larger magnitude of $r,r'$, and $\gamma$ is the angle between the vectors.

---
### Boundary-Value Problems (Cylindrical Coordinates)
Without imposing any explicit boundary conditions, we can write the potential as:
$$\begin{align}
\Phi(\vec{r})&=\sum_{m=-\infty}^\infty\int_{-\infty}^\infty \left[A_m(k)J_m(k\rho)+B_m(k)Y_m(k\rho)\right]e^{im\phi}\left[C(k)e^{kz}+D(k)e^{-kz}\right]\ dk
\end{align}$$
The expansion around a unit point charge can be written as:
$$\begin{align}
\dfrac{1}{|\vec{r}-\vec{r}'|}&=\dfrac{1}{\pi}\sum_{m=-\infty}^\infty e^{im(\phi-\phi')}\int_{-\infty}^\infty J_m(k\rho)J_m(k\rho')e^{-k|z-z'|}\ dk
\end{align}$$
#### Azimuthal Symmetry
When we impose that the solution is invariant in $\phi$, $m=0$, the potential reduces to:
$$\begin{align}
\Phi(\vec{r})&=\int_{-\infty}^\infty \left[A(k)J_0(k\rho)+B(k)Y_0(k\rho)\right]\left[C(k)e^{kz}+D(k)e^{-kz}\right]\ dk
\end{align}$$
The expansion around a unit point charge can be written as:
$$\begin{align}
\dfrac{1}{|\vec{r}-\vec{r}'|}&=\dfrac{1}{\pi}\int_{-\infty}^\infty J_0(k\rho)J_0(k\rho')e^{-k|z-z'|}\ dk
\end{align}$$
---
### Legendre Polynomials
The Legendre polynomials are a set of polynomials of the form:
$$\begin{align}
P_l(x)&=\dfrac{1}{2^ll!}\dfrac{d^l}{dx^l}\left(x^2-1\right)^l && \text{(3.16)}
\end{align}$$
These polynomials have the orthogonality condition:
$$\begin{align}
\int_{-1}^{+1}P_{l'}(x)P_l(x)\ dx&=\dfrac{2}{2l+1}\delta_{ll'} && \text{(3.21)}
\end{align}$$
These form a complete basis on $x\in[-1,1]$, thus any function can be written as:
$$\begin{align}
f(x)&=\sum_{l=0}^\infty c_lP_l(x) && \text{(3.23)}\\
c_l&=\dfrac{1}{\tfrac{2}{2l+1}}\int_{-1}^{+1} P_l(x)f(x)\ dx&& \text{(3.24)}
\end{align}$$
And the completeness relation for this basis is:
$$\begin{align}
\sum_{l=0}^\infty P_{l}(\cos\theta')P_{l}(\cos\theta)&=\delta(\cos\theta-\cos\theta')
\end{align}$$
Lastly, these polynomials have a reflection relation in $x$:
$$\begin{align}
P_l(-x)&=(-1)^lP_l(x)
\end{align}$$
#### Legendre Polynomial Recursion
The Legendre polynomials also have recursion relation:
$$\begin{align}
\dfrac{d}{dx}\left[P_{l+1}(x)-P_{l-1}(x)\right]-(2l+1)P_l(x)&=0 && \text{(3.28)}\\
(l+1)P_{l+1}(x)-(2l+1)xP_{l}(x)+lP_{l-1}(x)&=0 && \text{(3.29)}\\
(x^2-1)\dfrac{dP_{l}(x)}{dx}-lxP_{l}(x)+lP_{l-1}(x)&=0 && \text{(3.29)}\\
\end{align}$$
These can be used to calculate the different moments of the Legendre polynomials:
$$\begin{align}
I^{(1)}_{l,l'}&=\dfrac{2(l+1)}{(2l+1)(2l+3)}\delta_{l+1,l'}+\dfrac{2l}{(2l+1)(2l-1)}\delta_{l-1,l'} && \text{(3.31)}\\
I^{(2)}_{l,l'}&=\dfrac{2(l+1)(l+2)}{(2l+1)(2l+3)(2l+5)}\delta_{l+2,l'}+\dfrac{2(2l^2+2l-1)}{(2l-1)(2l+1)(2l+3)}\delta_{l,l'} && \text{(3.32)}\\
\end{align}$$
The general solution to a moment $p$ is:
$$\begin{align}
\int_{-1}^{+1}x^pP_{l'}(x)P_l(x)\ dx&=\dots
\end{align}$$
---
### Associated Legendre Functions
The associated Legendre polynomials are a set of polynomials of the form:
$$\begin{align}
P_l^m(x)&=(-1)^m\left(1-x^2\right)^{m/2}\dfrac{d^m}{dx^m}P_l(x) && \text{(3.49)}\\
P_l^m(x)&=\dfrac{(-1)^m}{2^ll!}\left(1-x^2\right)^{m/2}\dfrac{d^{l+m}}{dx^{l+m}}\left(x^2-1\right)^l && \text{(3.50)}
\end{align}$$
These polynomials have the orthogonality condition:
$$\begin{align}
\int_{-1}^{+1}P^m_{l'}(x)P^m_l(x)\ dx&=\dfrac{2}{2l+1}\dfrac{(l+m)!}{(l-m)!}\delta_{ll'} && \text{(3.52)}
\end{align}$$
Lastly, these polynomials have a reflection relation in $x$ and $m$:
$$\begin{align}
P_l^{-m}(x)&=(-1)^m\dfrac{(l-m)!}{(l+m)!}P_l^{m}(x) && \text{(3.51)} \\
P_l^{m}(-x)&=(-1)^lP_l^{m}(x)
\end{align}$$
For these to be more useful, we instead define a new function basis called the spherical harmonics.

---
### Spherical Harmonics
The spherical harmonics are a set of functions of the form:
$$\begin{align}
Y_{lm}(\theta,\phi)&=\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}P_l^m(\cos\theta)e^{im\phi} && \text{(3.53)}
\end{align}$$
These functions have the orthogonality condition:
$$\begin{align}
\int Y_{l'm'}^*(\theta,\phi)Y_{lm}(\theta,\phi)\ d\Omega&=\delta_{ll'}\delta_{mm'} && \text{(3.55)}
\end{align}$$
These form a complete basis on the sphere, thus any function can be written as:
$$\begin{align}
f(\theta,\phi)&=\sum_{l=0}^\infty\sum_{m=-l}^{+l} c_{lm}Y_{lm}(\theta,\phi) && \text{(3.58)}\\
c_{lm}&=\int Y_{lm}^*(\theta,\phi)f(\theta,\phi)\ d\Omega
\end{align}$$
And the completeness relation for this basis is:
$$\begin{align}
\sum_{l=0}^\infty\sum_{m=-l}^{+l}Y_{lm}^*(\theta,\phi)Y_{lm}(\theta,\phi)&=\delta(\phi-\phi')\delta(\cos\theta-\cos\theta')
\end{align}$$
Lastly, these polynomials have a reflection relation in $m$:
$$\begin{align}
Y_{l,-m}(\theta,\phi)&=(-1)^mY_{lm}^*(\theta,\phi) && \text{(3.54)}
\end{align}$$
#### Addition Theorem
We can express a Legendre polynomial as a sum of spherical harmonics as:
$$\begin{align}
P_l(\cos\gamma)&=\dfrac{4\pi}{2l+1}\sum_{m=-l}^{+l}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi) && \text{(3.62)}
\end{align}$$
where $\cos\gamma=\cos\theta\cos\theta'+\sin\theta\sin\theta'\cos\left(\phi-\phi'\right)$.

If our angle $\gamma=0$, the sum of the squares of the spherical harmonics to be:
$$\begin{align}
\sum_{m=-l}^{+l}\left|Y_{lm}(\theta,\phi)\right|^2&=\dfrac{2l+1}{4\pi} && \text{(3.69)}
\end{align}$$
---
### Bessel Functions
The Bessel functions of the first kind of order $\nu$ are a set of functions of the form:
$$\begin{align}
J_\nu(x)&=\left(\dfrac{x}{2}\right)^\nu\sum_{j=0}^\infty\dfrac{(-1)^j}{j!\ \Gamma(j+\nu+1)}\left(\dfrac{x}{2}\right)^{2j} && \text{(3.82)} \\
J_{-\nu}(x)&=\left(\dfrac{x}{2}\right)^{-\nu}\sum_{j=0}^\infty\dfrac{(-1)^j}{j!\ \Gamma(j-\nu+1)}\left(\dfrac{x}{2}\right)^{2j} && \text{(3.83)}
\end{align}$$
The Bessel functions of the second kind of order $\nu$ are a set of functions of the form:
$$\begin{align}
Y_\nu(x)&=\dfrac{J_{\nu}(x)\cos\nu\pi-J_{-\nu}(x)}{\sin\nu\pi} && \text{(3.85)}
\end{align}$$
The Bessel functions of the third kind of order $\nu$ are a set of functions of the form:
$$\begin{align}
H^{(1)}_\nu&=J_{\nu}(x)+iY_\nu(x) & H^{(2)}_\nu&=J_{\nu}(x)-iY_\nu(x) && \text{(3.86)}
\end{align}$$
These functions have the orthogonality conditions:
$$\begin{align}
\int_{0}^{a}xJ_\nu\left(\dfrac{\alpha_{\nu,m}}{a}x\right)J_\nu\left(\dfrac{\alpha_{\nu,n}}{a}x\right)\ dx&=\dfrac{a^2}{2}[J_{\nu+1}(\alpha_{\nu,m})]^2\delta_{mn}\\
\int_{a}^{b}xY_\nu\left(\dfrac{\beta_{\nu,m}}{b}x\right)Y_\nu\left(\dfrac{\beta_{\nu,n}}{b}x\right)\ dx&=\dfrac{b^2}{2}\left[Y_{\nu+1}(\beta_{\nu,n})\right]^2\delta_{mn}\\
\end{align}$$
where $\alpha_{\nu,m},\beta_{\nu,m}$ are the zeros of $J_{\nu}(x),Y_\nu(x)$ respectively.

Lastly, these polynomials have a reflection relation in $m$ (integer $\nu$):
$$\begin{align}
J_{-m}(x)&=(-1)^mJ_{m}(x) && \text{(3.84)}
\end{align}$$
#### Bessel Function Recursion
All 3 different kinds of the Bessel functions satisfy the recursion relation:
$$\begin{align}
J_{\nu-1}(x)+J_{\nu+1}(x)&=\dfrac{2\nu}{x}J_{\nu}(x) && \text{(3.87)} \\
Y_{\nu-1}(x)+Y_{\nu+1}(x)&=\dfrac{2\nu}{x}Y_{\nu}(x)\\
H^{(1,2)}_{\nu-1}(x)+H^{(1,2)}_{\nu+1}(x)&=\dfrac{2\nu}{x}H^{(1,2)}_{\nu}(x)\\
J_{\nu-1}(x)-J_{\nu+1}(x)&=2\dfrac{dJ_{\nu}(x)}{dx} && \text{(3.88)} \\
Y_{\nu-1}(x)-Y_{\nu+1}(x)&=2\dfrac{dY_{\nu}(x)}{dx} \\
H^{(1,2)}_{\nu-1}(x)-H^{(1,2)}_{\nu+1}(x)&=2\dfrac{dH^{(1,2)}_{\nu}(x)}{dx} \\
\end{align}$$
This is not often used, but could be used for different moments as well.


















### Eigenfunction Expansions for Green's Functions

---
## Chapter 4
---
### Multipole Expansion: Potential
The potential can be expanded in terms of a new quantity $q_{lm}$:
$$\begin{align}
\Phi(r,\theta,\phi)&=\dfrac{1}{4\pi\epsilon_0}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}\dfrac{q_{lm}}{r^{l+1}}Y_{lm}(\theta,\phi) && \text{(4.1)}
\end{align}$$
Outside the charge distribution, we can then write our multipole coefficient as:
$$\begin{align}
q_{l,m}&=\int Y^*_{lm}(\theta',\phi')r'^l\rho(\vec{r}')\ d^3r' && \text{(4.3)}\\
\end{align}$$
These coefficients polynomials have a reflection relation in $m$:
$$\begin{align}
q_{l,-m}&=(-1)^mq^*_{lm} && \text{(4.3)}\\
\end{align}$$
Based on above, the monopole, dipole, and quadrupole moment is given by:
$$\begin{align}
q&=\int r'^l\rho(\vec{r}')\ d^3r'\\
p_i&=\int r_i'\rho(\vec{r}')\ d^3r' && \text{(4.8)}\\
Q_{ij}&=\int (3r_i'r_j'-r'^2\delta_{ij})\rho(\vec{r}')\ d^3r' && \text{(4.9)}\\
\end{align}$$
Therefore, the potential in rectangular coordinates is then:
$$\begin{align}
\Phi(\vec{x})&=\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{q}{r}+\sum_ip_i\dfrac{x_i}{r^3}+\dfrac{1}{2}\sum_{ij}Q_{ij}\dfrac{x_ix_j}{r^5}+\dots\right] && \text{(4.10)}
\end{align}$$
---
### Multipole Expansion: Electric Field
We can take the gradient of the potential to find the electric field:
$$\begin{align}
\vec{E}(\vec{x})&=-\dfrac{1}{4\pi\epsilon_0}\vec\nabla\left[\dfrac{q}{r}+\sum_ip_i\dfrac{x_i}{r^3}+\dfrac{1}{2}\sum_{ij}Q_{ij}\dfrac{x_ix_j}{r^5}+\dots\right]
\end{align}$$
The monopole electric field is trivial, since it is the form of Coulomb's law:
$$\begin{align}
\vec{E}(\vec{r})&=\dfrac{q}{4\pi\epsilon_0}\dfrac{1}{\mathscr{r}^2}\hat{\mathscr{r}} && \text{(1.3)}
\end{align}$$
The dipole electric field takes the form:
$$\begin{align}
\vec{E}(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{3(\vec{p}\cdot\hat{\mathscr{r}})\hat{\mathscr{r}}-\vec{p}}{\mathscr{r}^3}-\dfrac{4\pi}{3}\vec{p}\delta(\vec{\mathscr{r}})\right] && \text{(4.13)}
\end{align}$$
The quadrupole electric field takes the form:
$$\begin{align}
\vec{E}(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\dots
\end{align}$$
---
### Multipole Expansion: Energy
The work associated with the multipole expansion starts with the Taylor series of potential:
$$\begin{align}
\Phi(\vec{x})&=\Phi(0)-\vec{x}\cdot\vec{E}(0)-\dfrac{1}{6}\sum_{i,j}\left(3x_ix_j-r^2\delta_{ij}\right)\dfrac{\partial E_j}{\partial x_i}(0)+\dots && \text{(4.23)}
\end{align}$$
Using the equation for work with charge density and potential, we get the series:
$$\begin{align}
W&=q\Phi(0)-\vec{p}\cdot\vec{E}(0)-\dfrac{1}{6}\sum_{i,j}Q_{ij}\dfrac{\partial E_j}{\partial x_i}(0)+\dots && \text{(4.24)}
\end{align}$$
The monopole-monopole interaction energy is trivial, since is it the potential energy of 2 charges:
$$\begin{align}
W&=\dfrac{q_1q_2}{4\pi\epsilon_0}\dfrac{1}{|\vec{r}-\vec{r}'|}
\end{align}$$
The dipole-dipole interaction energy takes the form:
$$\begin{align}
W&=\dfrac{1}{4\pi\epsilon_0}\dfrac{\vec{p}_1\cdot\vec{p}_2-3(\vec{p}_1\cdot\hat{\mathscr{r}})(\vec{p}_2\cdot\hat{\mathscr{r}})}{\mathscr{r}^3} && \text{(4.26)}
\end{align}$$
---
### Electrostatics in Macroscopic Media
...
