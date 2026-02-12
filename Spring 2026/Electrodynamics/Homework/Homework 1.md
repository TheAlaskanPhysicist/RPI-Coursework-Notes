Author: Stanley Goodwin
Date: January 29th, 2026

Apologies for the late submission.

---
## Question 1.3
Using the Dirac delta functions in the appropriate coordinates, express the following charge distributions as three-dimensional charge densities $\rho(\vec{x})$.

---
### Question 1.3.A
In spherical coordinates, a charge $Q$ uniformly distributed over a spherical shell of radius $R$.
$$\begin{align}
\Aboxed{\rho(\vec{r})&=\dfrac{Q}{4\pi}\dfrac{\delta(r-R)}{r^2}=\dfrac{Q}{4\pi R^2}\delta(r-R)}
\end{align}$$
The extra factors come from the Jacobian determinant of the basis.

---
### Question 1.3.B
In cylindrical coordinates, a charge per unit length $\lambda$ uniformly distributed over a cylinder surface of radius $b$.

The difficulty is the charge per unit length in what axis? The $z$ axis or $\phi$ axis. Assuming $z$:
$$\begin{align}
\Aboxed{\rho(\vec{r})&=\dfrac{Q}{2\pi z}\dfrac{\delta(r-b)}{r}=\dfrac{\lambda}{2\pi b}\delta(r-b)}
\end{align}$$
If the length is instead *around* the circle, then we have:
$$\begin{align}
\rho(\vec{r})&=\dfrac{Q}{2\pi z}\dfrac{\delta(r-b)}{r}=\dfrac{\lambda}{z}\delta(r-b)
\end{align}$$
I'm going to guess it was asking for the $z$ length, and is boxed above.
<div style="page-break-before: always;"></div>

### Question 1.3.C
In cylindrical coordinates, a charge $Q$ spread uniformly over a flat, circular, disc of negligible thickness and radius $R$.
$$\begin{align}
\Aboxed{\rho(\vec{r})&=\dfrac{Q}{\pi R^2}\delta(z),\ 0\le r\le R}
\end{align}$$
Since this is the limit of an infinitely-thin charge, there is no factor of 2.

---
### Question 1.3.D
The same as [[#Question 1.3.C]], but using spherical coordinates.
$$\begin{align}
\Aboxed{\rho(\vec{r})&=\dfrac{Q}{\pi R^2}\dfrac{\delta(\cos\theta)}{r},\ 0\le r\le R}
\end{align}$$
Our spherical encoding enforces that the disk is infinitesimally thick.

---
## Question 1.5
The time-averaged potential of a neutral hydrogen atom is given by:
$$\begin{align}
\Phi\equiv\dfrac{q}{4\pi\epsilon_0}\dfrac{e^{-\alpha r}}{r}\left(1+\dfrac{\alpha r}{2}\right)
\end{align}$$
where $q$ is the magnitude of the electric charge, and $\alpha^{-1}=a_0/2$, $a_0$ being the Bohr radius. Find the distribution of charge (both continuous and discrete) that will give this potential and interpret your result physically.
<div style="page-break-before: always;"></div>

The spherical Laplacian operation is the following (since it is spherically symmetric):
$$\begin{align}
\vec\nabla^2\Phi&=\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial\Phi}{\partial r}\right)
\end{align}$$
Substituting our potential, we get:
$$\begin{align}
\vec\nabla^2\Phi&=\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial}{\partial r}\dfrac{q}{4\pi\epsilon_0}\dfrac{e^{-\alpha r}}{r}\left(1+\dfrac{\alpha r}{2}\right)\right)\\
&=\dfrac{q}{4\pi\epsilon_0}\dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\left[-\alpha\dfrac{e^{-\alpha r}}{r}\left(1+\dfrac{\alpha r}{2}\right)-\dfrac{e^{-\alpha r}}{r^2}\left(1+\dfrac{\alpha r}{2}\right)+\dfrac{e^{-\alpha r}}{r}\left(\dfrac{\alpha}{2}\right)\right]\right)\\
&=-\dfrac{q}{4\pi\epsilon_0}\dfrac{1}{r^2}\dfrac{\partial}{\partial r}e^{-\alpha r}\left(\dfrac{\alpha^2r^2}{2}+\alpha r+1\right)\\
&=-\dfrac{q}{4\pi\epsilon_0}\dfrac{1}{r^2}e^{-\alpha r}\left(\alpha^2r+\alpha\right)+\dfrac{q}{4\pi\epsilon_0}\dfrac{1}{r^2}\alpha e^{-\alpha r}\left(\dfrac{\alpha^2r^2}{2}+\alpha r+1\right)\\
&=\dfrac{q}{4\pi\epsilon_0}\dfrac{1}{r^2} e^{-\alpha r}\dfrac{\alpha^3r^2}{2}\\
-\dfrac{\rho}{\epsilon_0}&=\dfrac{q\alpha^3}{8\pi\epsilon_0}e^{-\alpha r}\\
\Aboxed{\rho_{r>0}&=-\dfrac{q\alpha^3}{8\pi}e^{-\alpha r}}
\end{align}$$
The discrete charge comes from the relation:
$$\begin{align}
\vec\nabla^2\left(\dfrac{1}{r}\right)&=-4\pi\delta(r) &\implies&& \dfrac{1}{r^2}\dfrac{\partial}{\partial r}\left(r^2\dfrac{\partial}{\partial r}\left(\dfrac{1}{r}\right)\right)&=-4\pi\delta(r)
\end{align}$$
At the origin, we require that we can allow a positive charge for the proton, and thus:
$$\begin{align}
\Aboxed{\rho(r)&=-\dfrac{q\alpha^3}{8\pi}e^{-\alpha r}+q\delta(r)}
\end{align}$$
The delta function corresponds to a positive elementary charge (nucleus), and the exponential is a cloud of negative elementary charge that decays exponentially as $r\to\infty$.

---
## Question 1.7
Two long, cylindrical, capacitors of radii $a_1$ and $a_2$ are parallel and separated by distance $d$, which is large compared with either radius. 
<div style="page-break-before: always;"></div>

### Question 1.7.A
Show that the capacitance per unit length is given approximately by:
$$\begin{align}
C\simeq\pi\epsilon_0\left(\ln\dfrac{d}{a}\right)^{-1}
\end{align}$$
where $a$ is the geometric mean of the two radii.

The electric field in the plane between the two cylinders:
$$\begin{align}
\vec{E}(\vec{r})&=\dfrac{Q}{2\pi\epsilon_0 L}\dfrac{\vec{r}}{|\vec{r}|^2}-
\dfrac{Q}{2\pi\epsilon_0 L}\dfrac{\vec{r}-d\hat{x}}{|\vec{r}-d\hat{x}|^2}\end{align}$$
Expanding this in $x,y,z$, we have:
$$\begin{align}
\vec{E}(x,y)&=\dfrac{Q}{2\pi\epsilon_0 L}\dfrac{x\hat{x}+y\hat{y}}{x^2+y^2}-
\dfrac{Q}{2\pi\epsilon_0 L}\dfrac{(x-d)\hat{x}+y\hat{y}}{(x-d)^2+y^2}\end{align}$$
Since we're going on a line (for simplicity $y=0$), we can find the potential:
$$\begin{align}
E_x(x,0)&=\dfrac{Q}{2\pi\epsilon_0 L}\dfrac{1}{x}-
\dfrac{Q}{2\pi\epsilon_0 L}\dfrac{1}{x-d}\\
\dfrac{\partial\Phi}{\partial x}(x,0)&=
\dfrac{Q}{2\pi\epsilon_0 L}\dfrac{1}{x-d}-\dfrac{Q}{2\pi\epsilon_0 L}\dfrac{1}{x}\\
\end{align}$$
Integrate along this line of the differential, and the voltage is:
$$\begin{align}
\int_{a_1}^{d-a_2}\dfrac{\partial\Phi}{\partial x}\ dx&=
\dfrac{Q}{2\pi\epsilon_0 L}\int_{a_1}^{d-a_2}\left[\dfrac{1}{x-d}-\dfrac{1}{x}\right]\ dx=\dfrac{Q}{2\pi\epsilon_0 L}\left[\ln\left|x-d\right|-\ln\left|x\right|\right|_{a_1}^{d-a_2}\\
&=\dfrac{Q}{2\pi\epsilon_0 L}\left[\ln\left|d-a_2-d\right|-\ln\left|d-a_2\right|-\ln\left|a_1-d\right|+\ln\left|a_1\right|\right]\\
\Delta V&=\dfrac{Q}{2\pi\epsilon_0 L}\ln\left|\dfrac{a_2a_1}{(d-a_1)(d-a_2)}\right|\\
\end{align}$$
Since $a_1,a_2\ll d$, the extra factor of $2$ gives a square root, and using $a=\sqrt{a_1a_2}$:
$$\begin{align}
\dfrac{1}{L}\left(\dfrac{Q}{\Delta V}\right)&=\pi\epsilon_0\left(\ln\left|\dfrac{d}{a}\right|\right)^{-1}
\end{align}$$
From there, it's apparent the capacitance per unit length is:
$$\begin{align}
\Aboxed{C&=\pi\epsilon_0\left(\ln\left|\dfrac{d}{a}\right|\right)^{-1}}
\end{align}$$
.

.
### Question 1.7.B
Approximately what gauge wire (state diameter in millimeters) would be necessary to make a two-wire transmission like with a capacitance of $1.2\times10^{-11}\mathrm{ F/m}$ if the separation of the wires was...

We can rearrange the above equation for the geometric mean of the wire radii:
$$\begin{align}
2a&=2d\exp\left(-\dfrac{\pi\epsilon_0}{C}\right)
\end{align}$$
This actually becomes very easy to calculate:
$$\begin{align}
\text{Diameter}(d)
&=2d\exp\left(-\pi\dfrac{8.9\times10^{-12}\mathrm{ F/m}}{1.2\times10^{-11}\mathrm{ F/m}}\right)\\
&=2d\cdot0.0973\\
\text{Diameter}(d)&=1.946\cdot\dfrac{d}{\text{cm}}\text{mm}\\
\end{align}$$
For the different distances between the cylinders:
$$\begin{align}
\Aboxed{\text{Diameter}(0.5\text{ cm})&\approx1\text{ mm}} & 
\Aboxed{\text{Diameter}(1.5\text{ cm})&\approx3\text{ mm}} & 
\Aboxed{\text{Diameter}(5.0\text{ cm})&\approx10\text{ mm}}
\end{align}$$
---
## Question 1.14
Consider the electrostatic Green's functions of *Section 1.10* for Dirichlet and Neumann boundary conditions on the surface $S$ bounding the volume $V$. Apply Green's theorem (1.35) with integration variable $\vec{y}$ and $\phi=G(\vec{x},\vec{y})$, $\psi=G(\vec{x}',\vec{y})$, with $\nabla_y^2G(\vec{z},\vec{y})=-4\pi\delta(\vec{y}-\vec{z})$. Find an expression for the difference $\left[G(\vec{x},\vec{x}')-G(\vec{x}',\vec{x})\right]$ in terms of an integral over the boundary $S$.

For reference, 1.35 is the following:
$$\begin{align}
\int_V\left(\phi\vec\nabla^2\psi-\psi\vec\nabla^2\phi\right)\ d^3x&=\oint_S\left[\phi\dfrac{\partial\psi}{\partial n}-\psi\dfrac{\partial\phi}{\partial n}\right]\ da
\end{align}$$
Substituting the integration variables, we have:
$$\begin{align}
\int_V\left(G(\vec{x},\vec{y})\vec\nabla^2_yG(\vec{x}',\vec{y})-G(\vec{x}',\vec{y})\vec\nabla^2_yG(\vec{x},\vec{y})\right)\ d^3y&=\oint_S\left[G(\vec{x},\vec{y})\dfrac{\partial G(\vec{x}',\vec{y})}{\partial n}-G(\vec{x}',\vec{y})\dfrac{\partial G(\vec{x},\vec{y})}{\partial n}\right]\ da_y
\end{align}$$
We use the Laplacian identity given in the problem:
$$\begin{align}
&-4\pi\int_V\left(G(\vec{x},\vec{y})\delta(\vec{y}-\vec{x}')-G(\vec{x}',\vec{y})\delta(\vec{y}-\vec{x})\right)\ d^3y=\oint_S\left[G(\vec{x},\vec{y})\dfrac{\partial G(\vec{x}',\vec{y})}{\partial n}-G(\vec{x}',\vec{y})\dfrac{\partial G(\vec{x},\vec{y})}{\partial n}\right]\ da_y\\
\Aboxed{&\left[G(\vec{x},\vec{x}')-G(\vec{x}',\vec{x})\right]=-\dfrac{1}{4\pi}\oint_S\left[G(\vec{x},\vec{y})\dfrac{\partial G(\vec{x}',\vec{y})}{\partial n}-G(\vec{x}',\vec{y})\dfrac{\partial G(\vec{x},\vec{y})}{\partial n}\right]\ da_y}
\end{align}$$
### Question 1.14.A
For Dirichlet boundary conditions on the potential and the associated boundary condition on the Green's function, show that $G_D(\vec{x},\vec{x}')$ must be symmetric in $\vec{x}$ and $\vec{x}'$.

The Green's function for Dirichlet boundary condition is:
$$\begin{align}
\Phi(\vec{x})&=\dfrac{1}{4\pi\epsilon_0}\int_V\rho(\vec{x}')G(\vec{x}-\vec{x}')\ d^3x'-\dfrac{1}{4\pi}\oint_{S}\Phi(\vec{x}')\dfrac{\partial G(\vec{x}-\vec{x}')}{\partial n'}\ da'
\end{align}$$
The Green's function is $0$ at the surface, so using our equation from [[#Question 1.14]]:
$$\begin{align}
\left[G(\vec{x},\vec{x}')-G(\vec{x}',\vec{x})\right]&=-\dfrac{1}{4\pi}\oint_S\left[0\cdot\dfrac{\partial(0)}{\partial n}-0\cdot\dfrac{\partial (0)}{\partial n}\right]\ da_y=0\\
\Aboxed{G(\vec{x},\vec{x}')&=G(\vec{x}',\vec{x})}
\end{align}$$
---
### Question 1.14.B
For Neumann boundary conditions, use the boundary condition (1.45) for $G_N(\vec{x},\vec{x}')$ to show that $G_N(\vec{x},\vec{x}')$ is **not** symmetric in general, but that $G_N(\vec{x},\vec{x}')-F(\vec{x})$ **is** symmetric in $\vec{x}$ and $\vec{x}'$, where:
$$\begin{align}
F(\vec{x})&=\dfrac{1}{S}\oint_SG_N(\vec{x},\vec{y})\ da_y
\end{align}$$
Equation 1.45 is the following:
$$\begin{align}
\dfrac{\partial G_N}{\partial n'}(\vec{x},\vec{x}')&=-\dfrac{4\pi}{S} &\text{for }\vec{x}'\text{ on }S
\end{align}$$
Substituting this into our equation from [[#Question 1.14]]:
$$\begin{align}
\left[G(\vec{x},\vec{x}')-G(\vec{x}',\vec{x})\right]
&=-\dfrac{1}{4\pi}\oint_S\left[G(\vec{x},\vec{y})\cdot-\dfrac{4\pi}{S}-G(\vec{x}',\vec{y})\cdot-\dfrac{4\pi}{S}\right]\ da_y\\
G(\vec{x},\vec{x}')-G(\vec{x}',\vec{x})&=\dfrac{1}{S}\oint_S\left[G(\vec{x},\vec{y})-G(\vec{x}',\vec{y})\right]\ da_y
\end{align}$$
If we separate the two different permutations, we have:
$$\begin{align}
G(\vec{x},\vec{x}')+\dfrac{1}{S}\oint_SG(\vec{x}',\vec{y})\ da_y&=G(\vec{x}',\vec{x})+\dfrac{1}{S}\oint_SG(\vec{x},\vec{y})\ da_y\\
\Aboxed{G(\vec{x},\vec{x}')+F(\vec{x}')&=G(\vec{x}',\vec{x})+F(\vec{x})}
\end{align}$$
If we swap $\vec{x}\leftrightarrow\vec{x}'$, this relation does hold.
<div style="page-break-before: always;"></div>

### Question 1.14.C
Show that the addition of $F(\vec{x})$ to the Green's function does not affect the potential $\Phi(\vec{x})$. See problem 3.26 for an example of the Neumann Green's function.

The Green's function for Neumann boundary condition is:
$$\begin{align}
\Phi(\vec{x})&=\dfrac{1}{4\pi\epsilon_0}\int_V\rho(\vec{x}')G(\vec{x},\vec{x}')\ d^3x'+\dfrac{1}{4\pi}\oint_{S}G(\vec{x},\vec{x}')\dfrac{\partial\Phi(\vec{x}')}{\partial n'}\ da'+\left\langle\Phi\right\rangle_S
\end{align}$$
We can make the substitution of $G(\vec{x},\vec{x}')\to G(\vec{x},\vec{x}')+F(\vec{x})$:
$$\begin{align}
\Phi_\text{new}(\vec{x})
&=\dfrac{1}{4\pi\epsilon_0}\int_V\rho(\vec{x}')\left[G(\vec{x},\vec{x}')+F(\vec{x})\right]\ d^3x'+\dfrac{1}{4\pi}\oint_{S}\left[G(\vec{x},\vec{x}')+F(\vec{x})\right]\dfrac{\partial\Phi(\vec{x}')}{\partial n'}\ da'+\left\langle\Phi\right\rangle_S\\
\Phi_\text{new}(\vec{x})&=\Phi(\vec{x})+\dfrac{1}{4\pi\epsilon_0}\int_V\rho(\vec{x}')F(\vec{x})\ d^3x'+\dfrac{1}{4\pi}\oint_{S}F(\vec{x})\dfrac{\partial\Phi(\vec{x}')}{\partial n'}\ da'\\
\end{align}$$
Our function $F(\vec{x})$ is independent of the bounds of integration, and thus:
$$\begin{align}
\Phi_\text{new}(\vec{x})-\Phi(\vec{x})&=\dfrac{F(\vec{x})}{4\pi}\left(\int_V\dfrac{\rho(\vec{x}')}{\epsilon_0}\ d^3x'+\oint_{S}\dfrac{\partial\Phi(\vec{x}')}{\partial n'}\ da'\right)
\end{align}$$
The 2nd integral looks like a flux, so we want to write the other in that form:
$$\begin{align}
\dfrac{1}{\epsilon_0}\int_V\rho(\vec{x}')\ d^3x'&=
\end{align}$$
Substituting back in, and combining the integrals:
$$\begin{align}
\Phi_\text{new}(\vec{x})-\Phi(\vec{x})&=\dfrac{F(\vec{x})}{4\pi}\oint_{S}\left(\vec{E}(\vec{x}')\cdot\hat{n}'+\dfrac{\partial\Phi(\vec{x}')}{\partial n'}\right)\ da'
\end{align}$$
We can use the relationship between $\vec{E}$ and $\Phi$ to show that:
$$\begin{align}
\vec{E}&=-\vec{\nabla}\Phi &\implies&& \vec{E}\cdot\hat{n}'&=-\vec{\nabla}\Phi\cdot\hat{n}'=-\dfrac{\partial\Phi(\vec{x}')}{\partial n'}
\end{align}$$
This is exactly the same term with a negative, thus:
$$\begin{align}
\Phi_\text{new}(\vec{x})-\Phi(\vec{x})&=\dfrac{F(\vec{x})}{4\pi}\oint_{S}\left(0\right)\ da'\\
\Aboxed{\Phi_\text{new}(\vec{x})&=\Phi(\vec{x})}
\end{align}$$
The transformation $G(\vec{x},\vec{x}')\to G(\vec{x},\vec{x}')+F(\vec{x})$ preserves the potential of the system.
