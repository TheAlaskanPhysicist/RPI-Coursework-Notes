Author: Stanley Goodwin
Date: February 5th, 2026

**Note for the Professor:** I removed a lot of the in-between steps of arithmetic since this PDF was originally 29 pages long. Let me know if I had done too much in terms of simplification and I'll adjust future homework accordingly.

---
## Question 2.1
A point charge $q$ is brought to a position a distance $d$ away from an infinite-plane conductor held at zero potential. Using the method of images, find...
![[Homework 2.2.1.png]]
**Pictured:** The induced charge on the plane can be represented as a ghost charge equidistant to the plane on the other side, of opposite charge, because the electric field must be perpendicular to a conducting surface (at equilibrium).
<div style="page-break-before: always;"></div>

### Question 2.1.A
The surface-charge density induced on the plane, and plot it;

The potential of this system is the superposition of the point charge $q$ and the image charge $-q$:
$$\begin{align}
\Phi(x,y,z)&=\dfrac{q}{4\pi\epsilon_0}\left(\dfrac{1}{\sqrt{x^2+y^2+(z-d)^2}}-\dfrac{1}{\sqrt{x^2+y^2+(z+d)^2}}\right)
\end{align}$$
We can find the electric field, then take the limit as $z\rightarrow0$ as:
$$\begin{align}
-\vec\nabla\Phi(x,y,z)&=-\dfrac{q}{4\pi\epsilon_0}\left(\dfrac{-\tfrac{1}{2}\left(2x+2y+2(z-d)\right)}{\left(x^2+y^2+(z-d)^2\right)^{3/2}}-\dfrac{-\tfrac{1}{2}\left(2x+2y+2(z+d)\right)}{\left(x^2+y^2+(z+d)^2\right)^{3/2}}\right)\\
\left.\vec{E}(x,y,z)\right|_{z=0}&=-\dfrac{q}{4\pi\epsilon_0}\left.\left(-\dfrac{\left(x+y+z-d\right)}{\left(x^2+y^2+(z-d)^2\right)^{3/2}}+\dfrac{\left(x+y+z+d\right)}{\left(x^2+y^2+(z+d)^2\right)^{3/2}}\right)\right|_{z=0}\\
\vec{E}(x,y,0)&=-\dfrac{q}{2\pi\epsilon_0}\dfrac{d}{\left(x^2+y^2+d^2\right)^{3/2}}
\end{align}$$
Surface charge distribution (free due to conductor) is directly related to a difference in the perpendicular electric field above and below an interface (more generally this is $\vec{D}^\perp$):
$$\begin{align}
\sigma_\text{free}&=\epsilon_0\vec{E}_\text{above}^\perp-\epsilon_0\vec{E}_\text{below}^\perp
\end{align}$$
Below the surface has no electric field since electrostatics doesn't have a $\vec{E}$ field in the conductor:
$$\begin{align}
\sigma_\text{free}&=\epsilon_0\lim_{z\rightarrow0^+}\vec{E}(x,y,z)-\epsilon_0\lim_{z\rightarrow0^-}\vec{E}(x,y,z)\\
\Aboxed{\sigma(x,y)&=-\dfrac{q}{2\pi}\dfrac{d}{\left(x^2+y^2+d^2\right)^{3/2}}}
\end{align}$$
We could also write this to be in cylindrical coordinates to be:
$$\begin{align}
\Aboxed{\sigma(r)&=-\dfrac{qd}{2\pi}\dfrac{1}{\left(r^2+d^2\right)^{3/2}}}
\end{align}$$
Where $r$ is the radial distance from the origin within the plane $z=0$.

![[Homework 2.2.1.A.png]]
**Pictured:** A graph of the surface charge on the conductor with respect to a **normalized radius** $r/d$ from the origin, and without loss of generality, scale factor $\tfrac{q}{2\pi d^2}=1$.

---
### Question 2.1.B
The force between the plane and the charge by using Coulomb's law for the force between a charge and its image;

The image charge is a charge of opposite sign at an equal distance from the plane $z=0$. 
$$\begin{align}
\vec{F}_{\pm}&=\dfrac{1}{4\pi\epsilon_0}\dfrac{q(-q)}{(d-(-d))^2}(\pm\hat{z})
\end{align}$$
The force can be written as acting on the charge, the plane, or just the magnitude:
$$\begin{align}
\Aboxed{\vec{F}^\text{charge}&=-\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}\hat{z}} & \Aboxed{\vec{F}^\text{plane}&=+\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}\hat{z}} &
\Aboxed{\left|\vec{F}\right|&=\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}}
\end{align}$$
Where the superscript on force is the object feeling this force.
<div style="page-break-before: always;"></div>

### Question 2.1.C
The total force acting on the plane by integrating $\sigma^2/2\epsilon_0$ over the whole plane;
$$\begin{align}
\left|\vec{F}\right|&=\int\dfrac{\sigma^2}{2\epsilon_0}da
\end{align}$$
We can use our charge distribution from [[#Question 2.1.A]], and split the integral in components:
$$\begin{align}
\left|\vec{F}\right|&=\dfrac{1}{2\epsilon_0}\left(\dfrac{qd}{2\pi}\right)^2\int_0^\infty\dfrac{1}{\left(r^2+d^2\right)^{3}}\ r\ dr\int_0^{2\pi}d\phi
\end{align}$$
Let $u=r^2+d^2$, then $du/2=r\ dr$, and the new bounds $u=d^2$ to $u=\infty$:
$$\begin{align}
\left|\vec{F}\right|
&=\dfrac{1}{2\epsilon_0}\dfrac{q^2d^2}{(2\pi)^2}\int_{d^2}^\infty\dfrac{1}{u^{3}}\cdot\dfrac{1}{2}du\cdot2\pi\\
&=\dfrac{q^2d^2}{8\pi\epsilon_0}\left.\dfrac{1}{-2u^2}\right|^{\infty}_{d^2}=\dfrac{q^2d^2}{8\pi\epsilon_0}\dfrac{1}{2(d^2)^2}\\
\Aboxed{\left|\vec{F}\right|&=\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}}
\end{align}$$
Lastly, since we know that the force is radially symmetric, the net force only points $+\hat{z}$, and so:
$$\begin{align}
\Aboxed{\vec{F}&=+\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}\hat{z}}
\end{align}$$
---
### Question 2.1.D
The work necessary to remove the charge $q$ from its position to infinity;

The work moving the charge from $z=d$ to $z\rightarrow\infty$ takes the following form:
$$\begin{align}
W&=\int\vec{F}_\text{ext}\cdot d\vec{x}=-\int\vec{F}^\text{charge}(z)\cdot d\vec{x}
\end{align}$$
Our force and displacement both align on the $z$-axis, and so our work is:
$$\begin{align}
W&=-\int^{\infty}_d\vec{F}^\text{charge}_z(z)\ dz=-\dfrac{q^2}{16\pi\epsilon_0}\int^{\infty}_d-\dfrac{1}{z^2}\ dz\\
&=-\dfrac{q^2}{16\pi\epsilon_0}\left.\dfrac{1}{z}\right|^{\infty}_d=\dfrac{q^2}{16\pi\epsilon_0}\dfrac{1}{d}\\
\Aboxed{W&=\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d}}
\end{align}$$
.
### Question 2.1.E
The potential energy between the charge $q$ and its image (compare to part D and discuss);

Since $q$ and it's image are point charges, the potential energy is simply:
$$\begin{align}
U&=\dfrac{1}{4\pi\epsilon_0}\dfrac{q(-q)}{|d-(-d)|} &\implies && \Aboxed{U&=-\dfrac{1}{8\pi\epsilon_0}\dfrac{q^2}{d}}
\end{align}$$
The potential energy of charge-image pair is double that of the work to remove the charge.
I believe this to be expected since the energy required to "move" the image charge isn't actually real, and thus since charge moves freely on the conductor, only half the work is needed.

---
### Question 2.1.F
Find the answer to part D in electron volts for an electron originally one angstrom from the surface.

Special thanks to [Wikipedia](https://en.wikipedia.org/wiki/Vacuum_permittivity) for the super convenient value for $\epsilon_0$:
$$\begin{align}
W&=\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d}=\dfrac{1}{16\pi\left(55.263\text{ e}^2\cdot\text{eV}^{-1}\cdot\mu\text{m}^{-1}\right)}\dfrac{\text{e}^2}{10^{-4}\mu\text{m}}\\
\Aboxed{W&=3.600\text{ eV}}
\end{align}$$
---
## Question 2.7
Consider a potential problem in the half-space defined by $z\ge0$, with (homogenous) Dirichlet boundary conditions on the plane $z=0$ (and at infinity).
![[Homework 2.2.7.png]]

### Question 2.7.A
Write down an appropriate Green's function $G(\vec{x},\vec{x}')$.

We would like a Green's function that vanishes on the $z=0$ plane and at infinity. The homogenous Green's function already decays at infinity. To force it to vanish at $z=0$, we can add an image charge of opposite polarity similar to [[#Question 2.1]]:
$$\begin{align}
G(\vec{x},\vec{x}')&=\dfrac{1}{|\vec{x}-\vec{x}'|}-\dfrac{1}{|\vec{x}-R_z\vec{x}'|}=G(\vec{x}-\vec{x}')
\end{align}$$
where if $\vec{x}'=(\rho',\phi',z')$, then $R_z\vec{x}'=(\rho',\phi',-z')$. I.e. reflected about the $xy$-plane.

We can explicitly expand this in terms of cylindrical coordinates to be:
$$\begin{align}
G(\vec{r},\vec{r}')&=\dfrac{1}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi-\phi')+(z-z')^2)^{1/2}}-\dfrac{1}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi-\phi')+(z+z')^2)^{1/2}}
\end{align}$$
Where the difference $\vec{x}-\vec{x}'$ uses the law of cosines of the angle between them in the $xy$-plane.

---
### Question 2.7.B
If the potential on the plane $z=0$ is specified to be $\Phi=V$ inside a circle of radius $a$ centered at the origin, and $\Phi=0$ outside that circle, find an integral expression for the potential at a point $P$ specified in cylindrical coordinates $(\rho,\phi,z)$.

From Green's equations, and that "potential problem"$\implies\rho(\vec{x})=0$, we get:
$$\begin{align}
\Phi(\vec{x})&=-\dfrac{1}{4\pi}\oint_{\partial\Omega}\Phi(\vec{x}')\dfrac{\partial G(\vec{x},\vec{x}')}{\partial\hat{n}'}\ dS'+0
\end{align}$$
The normal of the surface at the $xy$-plane points outward, in the $-\hat{z}$ direction, thus:
$$\begin{align}
\Phi(\rho,\phi,z)&=+\dfrac{1}{4\pi}\oint_{\partial\Omega}\Phi(\rho',\phi',0)\left.\dfrac{\partial G(\vec{x},\vec{x}')}{\partial z'}\right|_{z'=0}\ dS'
\end{align}$$
From [[#Question 2.7.A]], we know the Green's function takes the form of:
$$\begin{align}
G(\vec{x},\vec{x}')&=\dfrac{1}{(\dots+(z-z')^2)^{1/2}}-\dfrac{1}{(\dots+(z+z')^2)^{1/2}}
\end{align}$$
<div style="page-break-before: always;"></div>

Differentiating with represent to $z'$ in the $z'\rightarrow0$ limit, we get:
$$\begin{align}
\left.\dfrac{\partial G(\vec{x},\vec{x}')}{\partial z'}\right|_{z'=0}
&=\left.\dfrac{-\tfrac{1}{2}\cdot2(z-z')\cdot-1}{(\dots+(z-z')^2)^{3/2}}\right|_{z'=0}-\left.\dfrac{-\tfrac{1}{2}\cdot2(z+z')\cdot1}{(\dots+(z+z')^2)^{3/2}}\right|_{z'=0}\\
&=\dfrac{z}{(\dots+z^2)^{3/2}}+\dfrac{z}{(\dots+z^2)^{3/2}}\\
\Aboxed{\left.\dfrac{\partial G(\vec{x},\vec{x}')}{\partial z'}\right|_{z'=0}&=\dfrac{2z}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi-\phi')+z^2)^{3/2}}}
\end{align}$$
Substituting for our potential integral, and using appropriate bounds for $\Phi(\rho',\phi',0)$:
$$\begin{align}
\Phi(\rho,\phi,z)&=\dfrac{Vz}{2\pi}\int_0^{2\pi}\int_0^a\dfrac{\rho'\ d\rho'\ d\phi'}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi-\phi')+z^2)^{3/2}}
\end{align}$$
Since $\cos(\phi-\phi')$ goes over its whole cycle, and is an even function, we can use $\phi-\phi'\rightarrow\phi'$:
$$\begin{align}
\Aboxed{\Phi(\rho,\phi,z)&=\dfrac{Vz}{2\pi}\int_0^{2\pi}\int_0^a\dfrac{\rho'\ d\rho'\ d\phi'}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi')+z^2)^{3/2}}}
\end{align}$$
---
### Question 2.7.C
Show that, along the axis of the circle ($\rho=0$), the potential is given by:
$$\begin{align}
\Phi&=V\left(1-\dfrac{z}{\sqrt{a^2+z^2}}\right)
\end{align}$$
Using our equation from [[#Question 2.7.B]], using $\rho=0$, and separating integrals, we get:
$$\begin{align}
\Phi(0,\phi,z)&=\dfrac{Vz}{2\pi}\int_0^a\dfrac{\rho'}{(\rho'^2+z^2)^{3/2}}\ d\rho'\int_0^{2\pi} d\phi'
\end{align}$$
Let $u=\rho'^2+z^2$, then $du/2=\rho'\ d\rho'$, and the new bounds $u=z^2$ to $u=a^2+z^2$:
$$\begin{align}
\Phi(0,\phi,z)&=\dfrac{Vz}{2\pi}\int_{z^2}^{a^2+z^2}\dfrac{1}{u^{3/2}}\dfrac{du}{2}\cdot2\pi\\
&=\dfrac{Vz}{2}\left.\dfrac{-2}{\sqrt{u}}\right|_{z^2}^{a^2+z^2}=Vz\left(\dfrac{1}{\sqrt{z^2}}-\dfrac{1}{\sqrt{a^2+z^2}}\right)\\
\Aboxed{\Phi(0,\phi,z)&=V\left(1-\dfrac{z}{\sqrt{a^2+z^2}}\right)}
\end{align}$$
<div style="page-break-before: always;"></div>

### Question 2.7.D
Show that at large distances $\rho^2+z^2\gg a^2$, the potential can be expanded in a power series in $(\rho^2+z^2)^{-1}$, and that the leading terms are:
$$\begin{align}
\Phi(\rho,\phi,z)&=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}\left[1-\dfrac{3a^2}{4(\rho^2+z^2)}+\dfrac{5(3\rho^2a^2+a^4)}{8(\rho^2+z^2)^2}+\dots\right]
\end{align}$$
Verify that the result of parts C and D are consistent in their common range of validity.

Start with the equation found in [[#Question 2.7.B]], and we can factor out $(\rho^2+z^2)^{3/2}$:
$$\begin{align}
\Phi(\rho,\phi,z)&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\dfrac{\rho'}{\left(1+\dfrac{\rho'^2-2\rho\rho'\cos(\phi')}{\rho^2+z^2}\right)^{3/2}}\ d\rho'\ d\phi'
\end{align}$$
In the limit of $\rho^2+z^2\gg a^2$, consequently $\rho^2+z^2\gg \rho'^2$, and $\rho^2+z^2\gg \rho\rho'$. The denominator can be expanded using a Taylor series, where $\epsilon=\epsilon(\rho,\rho',\phi',z)=\dfrac{\rho'^2-2\rho\rho'\cos(\phi')}{\rho^2+z^2}$.
$$\begin{align}
\Phi(\rho,\phi,z)
&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\rho'\left[1+\epsilon\right]^{-3/2}\ d\rho'\ d\phi'\\
&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\rho'\left[1-\dfrac{3}{2}\epsilon+\dfrac{\tfrac{3}{2}\tfrac{5}{2}}{2}\epsilon^2+\dots\right]\ d\rho'\ d\phi'
\end{align}$$
The 0th order term:
$$\begin{align}
\Phi^{(0)}(\rho,\phi,z)
&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^a\rho'\ d\rho' \int_0^{2\pi}d\phi'\\
\Phi^{(0)}(\rho,\phi,z)&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\left.\dfrac{\rho'^2}{2}\right|_0^a \cdot2\pi=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}
\end{align}$$
The 1st order term:
$$\begin{align}
\Phi^{(1)}(\rho,\phi,z)
&=-\dfrac{3}{2}\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\rho'\left[\dfrac{\rho'^2-2\rho\rho'\cos(\phi')}{\rho^2+z^2}\right]\ d\rho'\ d\phi'\\
&=-\dfrac{3Vz}{4\pi}\dfrac{1}{(\rho^2+z^2)^{5/2}}\left(\int_0^a\rho'^3\ d\rho'\int_0^{2\pi}d\phi'-2\rho\int_0^a\rho'^2\ d\rho'\int_0^{2\pi}\cos(\phi')\ d\phi'\right)\\
&=-\dfrac{3Vz}{4\pi}\dfrac{1}{(\rho^2+z^2)^{5/2}}\left(\left.\dfrac{\rho'^4}{4}\right|_0^a\cdot2\pi-2\rho\left.\dfrac{\rho'^3}{3}\right|_0^a\cdot-\left.\sin(\phi')\right|_0^{2\pi}\right)\\
\Phi^{(1)}(\rho,\phi,z)&=-\dfrac{3Vz}{2}\dfrac{1}{(\rho^2+z^2)^{5/2}}\dfrac{a^4}{4}=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}\left(-\dfrac{3a^2}{4(\rho^2+z^2)}\right)
\end{align}$$
<div style="page-break-before: always;"></div>

The 2nd order term:
$$\begin{align}
\Phi^{(2)}(\rho,\phi,z)
&=\dfrac{\tfrac{3}{2}\tfrac{5}{2}}{2}\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\rho'\left[\dfrac{\rho'^2-2\rho\rho'\cos(\phi')}{\rho^2+z^2}\right]^2\ d\rho'\ d\phi'\\
&=\dfrac{15Vz}{16\pi}\dfrac{1}{(\rho^2+z^2)^{7/2}}\int_0^{2\pi}\int_0^a\left[\rho'^5-4\rho\rho'^4\cos(\phi')+4\rho^2\rho'^3\cos^2(\phi')\right]\ d\rho'\ d\phi'\\
&=\dfrac{15Vz}{16\pi}\dfrac{1}{(\rho^2+z^2)^{7/2}}\left(\int_0^a\rho'^5\ d\rho'\int_0^{2\pi}d\phi'-4\rho\int_0^a\rho'^4\ d\rho'\int_0^{2\pi}\cos(\phi')+4\rho^2\int_0^a\rho'^3\ d\rho'\int_0^{2\pi}\cos^2(\phi')\ d\phi'\right)\\
&=\dfrac{15Vz}{16\pi}\dfrac{1}{(\rho^2+z^2)^{7/2}}\left(\left.\dfrac{\rho'^6}{6}\right|_0^a\cdot2\pi-4\rho\left.\dfrac{\rho'^5}{5}\right|_0^a\cdot-\left.\sin(\phi')\right|_0^{2\pi}+4\rho^2\left.\dfrac{\rho'^4}{4}\right|_0^a\cdot\left.\dfrac{\phi'+\sin\phi'\cos\phi'}{2}\right|_0^{2\pi}\right)\\
\Phi^{(2)}(\rho,\phi,z)&=\dfrac{15Vz}{16\pi}\dfrac{1}{(\rho^2+z^2)^{7/2}}\left(\dfrac{\pi a^6}{3}+0+\pi\rho^2a^4\right)=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}\left(\dfrac{5(3\rho^2a^2+a^4)}{8(\rho^2+z^2)^2}\right)
\end{align}$$
An approximation of the $\rho^2+z^2\gg a^2$ limit to the 2nd order is then:
$$\begin{align}
\Aboxed{\Phi&\approx\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}\left[1-\dfrac{3a^2}{4(\rho^2+z^2)}+\dfrac{5(3\rho^2a^2+a^4)}{8(\rho^2+z^2)^2}-\dots\right]}
\end{align}$$
To check for consistency in the $\rho\rightarrow 0$ limit, with knowledge of the Taylor expansion of $(1+\epsilon)^{-1/2}$:
$$\begin{align}
\lim_{\rho\rightarrow0}\Phi(\rho,\phi,z)
&=\dfrac{Va^2}{2}\dfrac{z}{(z^2)^{3/2}}\left[1-\dfrac{3}{4}\left(\dfrac{a}{z}\right)^{2}+\dfrac{5}{8}\left(\dfrac{a}{z}\right)^{4}-\dots\right]\\
&=V\left[1-1+\dfrac{1}{2}\left(\dfrac{a}{z}\right)^{2}-\dfrac{3}{8}\left(\dfrac{a}{z}\right)^{4}+\dfrac{5}{16}\left(\dfrac{a}{z}\right)^{6}-\dots\right]\\
&=V-V\left[1-\dfrac{1}{2}\left(\dfrac{a}{z}\right)^{2}+\dfrac{3}{8}\left(\dfrac{a}{z}\right)^{4}-\dfrac{5}{16}\left(\dfrac{a}{z}\right)^{6}+\dots\right]\\
\Aboxed{\Phi(0,\phi,z)&=V-V\left[1+\left(\dfrac{a}{z}\right)^2\right]^{-\tfrac{1}{2}}=V\left(1-\dfrac{z}{\sqrt{a^2+z^2}}\right)}
\end{align}$$
---
## Question 3.1
Two concentric spheres have radii $a,b$ $(b>a)$ and each is divided into two hemispheres by the same horizontal plane. The upper hemisphere of the inner sphere and the lower hemisphere of the outer sphere are maintained at potential $V$. The other hemispheres are at zero potential.
<div style="page-break-before: always;"></div>

### Question 3.1.A
Determined the potential in the region $a\le r\le b$ as a series of Legendre polynomials. Include terms at least up to $l=4$.

The problem gives us the potentials on these surfaces to be:
$$\begin{align}
\Phi(a,\theta)&=\begin{cases}V&\theta\in[0,\pi/2)\\0&\theta\in(\pi/2,\pi]\end{cases} & \Phi(b,\theta)&=\begin{cases}0&\theta\in[0,\pi/2)\\V&\theta\in(\pi/2,\pi]\end{cases} 
\end{align}$$
Thankfully, we have azimuthal symmetry, which simplifies the general solution to:
$$\begin{align}
\Phi(r,\theta)&=\sum_{l=0}^\infty\left(A_lr^l+B_lr^{-l-1}\right)P_l(\cos\theta)
\end{align}$$
This solution must work on the spheres, and the polynomial coefficients can be determined:
$$\begin{align}
\Phi(a,\theta)&=\sum_{l=0}^\infty c_l^{r=a}P_l(\cos\theta) & c_l^{r=a}&=\dfrac{2l+1}{2}\int_0^\pi P_l(\cos\theta)\Phi(a,\theta)\sin\theta\ d\theta\\
\Phi(b,\theta)&=\sum_{l=0}^\infty c_l^{r=b}P_l(\cos\theta) & c_l^{r=b}&=\dfrac{2l+1}{2}\int_0^\pi P_l(\cos\theta)\Phi(b,\theta)\sin\theta\ d\theta\\
\end{align}$$
Since $\Phi(a,\theta)$ and $\Phi(b,\theta)$ is non-zero only on part of its interval:
$$\begin{align}
c_l^{r=a}&=V\dfrac{2l+1}{2}\int_0^{\pi/2} -P_l(\cos\theta)\cdot(-\sin\theta\ d\theta)\\
c_l^{r=b}&=V\dfrac{2l+1}{2}\int_{\pi/2}^\pi -P_l(\cos\theta)\cdot(-\sin\theta\ d\theta)
\end{align}$$
Let $x=\cos\theta$, then $dx=-\sin\theta\ d\theta$, and the new bounds $x(0)=1$, $x(\pi/2)=0$, $x(\pi)=-1$:
$$\begin{align}
c_l^{r=a}&=V\dfrac{2l+1}{2}\int_0^{1} P_l(x)\ dx &c_l^{r=b}&=V\dfrac{2l+1}{2}\int_{-1}^0 P_l(x)\ dx
\end{align}$$
For $c_l^{r=b}$, if we invert the sign for $x$ and bounds, use can use $P_l(-x)=(-1)^lP_l(x)$:
$$\begin{align}
c_l^{r=a}&=(-1)^lc_l^{r=b}=V\dfrac{2l+1}{2}\int_0^{1} P_l(u)\ du
\end{align}$$
For the region $r\in[a,b]$, we expect the general solution to be of the form:
$$\begin{align}
\Phi(r,\theta)&=\sum_{l=0}^\infty\left(A_lr^l+B_lr^{-l-1}\right)P_l(\cos\theta)
\end{align}$$
<div style="page-break-before: always;"></div>

Equating terms on the two surfaces, this becomes a system of equations we can invert:
$$\begin{align}
\begin{bmatrix}a^l&a^{-l-1}\\b^l&b^{-l-1}\end{bmatrix}\begin{bmatrix}A_l\\B_l\end{bmatrix}&=c_l^{r=a}\begin{bmatrix}1\\(-1)^l\end{bmatrix} &\implies&&
\dfrac{c_l^{r=a}}{a^{2l+1}-b^{2l+1}}\begin{bmatrix}a^{l+1}&-b^{l+1}\\-a^{l+1}b^{2l+1}&a^{2l+1}b^{l+1}\end{bmatrix}\begin{bmatrix}1\\(-1)^l\end{bmatrix}&=\begin{bmatrix}A_l\\B_l\end{bmatrix}
\end{align}$$
More explicitly, we get:
$$\begin{align}
\Aboxed{A_l&=\dfrac{a^{l+1}-(-1)^lb^{l+1}}{a^{2l+1}-b^{2l+1}}c_l^{r=a}} & \Aboxed{B_l&=\dfrac{-a^{l+1}b^{2l+1}+(-1)^la^{2l+1}b^{l+1}}{a^{2l+1}-b^{2l+1}}c_l^{r=a}}
\end{align}$$
Substituting back into the potential, the final solution is then:
$$\begin{align}
\Aboxed{\Phi(r,\theta)&=\sum_{l=0}^\infty\left(\dfrac{a^{l+1}-(-1)^lb^{l+1}}{a^{2l+1}-b^{2l+1}}r^l-\dfrac{a^{l+1}b^{2l+1}-(-1)^la^{2l+1}b^{l+1}}{a^{2l+1}-b^{2l+1}}r^{-l-1}\right)c_l^{r=a}P_l(\cos\theta)}
\end{align}$$
This can be further simplified by noticing that the integral of $P_l(x)$ on $x\in(0,1)$, even $l$ except $0$ evaluate to be zero, and so the whole summation term goes to zero. The potential becomes:
$$\begin{align}
\Aboxed{\Phi(r,\theta)&=\dfrac{V}{2}+\sum_{k=1}^\infty\left(\dfrac{a^{2k}+b^{2k}}{a^{4k-1}-b^{4k-1}}r^{2k-1}-\dfrac{a^{2k}b^{4k-1}+a^{4k-1}b^{2k}}{a^{4k-1}-b^{4k-1}}r^{-2k}\right)c_{2k-1}^{r=a}P_{2k-1}(\cos\theta)}\\
c_{2k-1}^{r=a}&=V\dfrac{2(2k-1)+1}{2}\int_0^{1} P_{2k-1}(x)\ dx
\end{align}$$
Inspired by [[#Question 3.2]], I can use the Legendre integral identity, which in my case is:
$$\begin{align}
\int_0^{1} P_{2k-1}(x)\ dx&=\dfrac{\left(P_{2k}(1)-P_{2k-2}(1)\right)-\left(P_{2k}(0)-P_{2k-2}(0)\right)}{4k-1}=\dfrac{P_{2k-2}(0)-P_{2k}(0)}{4k-1}
\end{align}$$
Putting that into $c_{2k-1}^{r=a}$, it simplifies to:
$$\begin{align}
c_{2k-1}^{r=a}&=\dfrac{V}{2}\left(P_{2k-2}(0)-P_{2k}(0)\right)
\end{align}$$
Let $A'_k=\dfrac{a^{2k}+b^{2k}}{a^{4k-1}-b^{4k-1}}$ and $B_k'=\dfrac{a^{2k}b^{4k-1}+a^{4k-1}b^{2k}}{a^{4k-1}-b^{4k-1}}$ to save space, then the potential is:
$$\begin{align}
\Aboxed{\Phi(r,\theta)&=\dfrac{V}{2}\left[1+\sum_{k=1}^\infty\left(A_k'r^{2k-1}-B_kr^{-2k}\right)\left[P_{2k-2}(0)-P_{2k}(0)\right]P_{2k-1}(\cos\theta)\right]}
\end{align}$$
Using the Legendre Polynomial table on [Wikipedia](https://en.wikipedia.org/wiki/Associated_Legendre_polynomials), and doing the arithmetic for each term, since we want to get to $l=4\implies k=2$ term, sparing the arithmetic:
$$\begin{align}
\Phi(r,\theta)&\approx\dfrac{V}{2}+\dfrac{V}{2}\left[\dfrac{3}{2}\dfrac{a^{2}+b^{2}}{a^{3}-b^{3}}r-\dfrac{3}{2}\dfrac{a^{2}b^{3}\\+a^{3}b^{2}}{a^{3}-b^{3}}r^{-2}\right]\cos\theta\\
&+\dfrac{V}{2}\left[-\dfrac{7}{16}\dfrac{a^{4}+b^{4}}{a^{7}-b^{7}}r^3+\dfrac{7}{16}\dfrac{a^{4}b^{7}+a^{7}b^{4}}{a^{7}-b^{7}}r^{-4}\right]\left(5\cos^3\theta-3\cos\theta\right)+\dots
\end{align}$$
<div style="page-break-before: always;"></div>

### Question 3.2.B
Check your solution against the know results in the limiting cases $b\rightarrow\infty$ and $a\rightarrow 0$.
In the limit as $b\rightarrow\infty$, we see that:
$$\begin{align}
\lim_{b\rightarrow\infty}\Phi(r,\theta)&\approx\dfrac{V}{2}\left[1+\dfrac{3}{2}\dfrac{a^{2}}{r^2}\cos\theta-\dfrac{7}{16}\dfrac{a^{4}}{r^4}(5\cos^3\theta-3\cos\theta)+\dots\right]
\end{align}$$
In the limit as $a\rightarrow0$, we see that:
$$\begin{align}
\lim_{a\rightarrow0}\Phi(r,\theta)&\approx\dfrac{V}{2}\left[1-\dfrac{3}{2}\dfrac{r}{b}\cos\theta+\dfrac{7}{16}V\dfrac{r^3}{b^{3}}(5\cos^3\theta-3\cos\theta)+\dots\right]
\end{align}$$
In these limits, we know that:
$$\begin{align}
\lim_{b\rightarrow\infty}\Phi(r,\theta)&=\Phi_{\text{outside, }R=a}(r,\theta)\\
\lim_{a\rightarrow0}\Phi(r,\theta)&=\Phi_{\text{inside, }R=b}(r,\theta)\\
\end{align}$$
The $b\rightarrow\infty$ potential has the expansion for the potential outside a ball of radius $a$, and the $a\rightarrow0$ potential has the expansion for the potential inside a ball of radius $b$, as expected.

---
## Question 3.2
A spherical surface of radius $R$ has charge uniformly distributed over its surface with a density $Q/4\pi R^2$, except for a spherical cap at the north pole, defined by the cone $\theta=\alpha$.

We can write the charge density as the following:
$$\begin{align}
\sigma(\theta,\phi)&=\begin{cases}0&0\le\theta\le\alpha\\\dfrac{Q}{4\pi R^2}&\alpha\lt\theta\le\pi\end{cases}
\end{align}$$
It took me a bit to understand what he meant by "except".
<div style="page-break-before: always;"></div>

### Question 3.2.A
Show that the potential **inside** the spherical surface can be expressed as:
$$\begin{align}
\Phi&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{1}{2l+1}\left[P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right]\dfrac{r^l}{R^{l+1}}P_{l}(\cos\theta)
\end{align}$$
where, for $l=0$, $P_{l-1}(\cos\alpha)=-1$. What is the potential outside?

Since the inside cannot contain singularities and the outside must approach zero:
$$\begin{align}
\Phi_\text{in}(r,\theta,\phi)&=\sum_{l=0}^\infty A_lr^lP_l(\cos\theta)\\
\Phi_\text{out}(r,\theta,\phi)&=\sum_{l=0}^\infty B_lr^{-l-1}P_l(\cos\theta)
\end{align}$$
First condition: the potential must be continuous between the inside and outside:
$$\begin{align}
\Phi_\text{in}(R,\theta,\phi)&=\Phi_\text{out}(R,\theta,\phi)\\
\sum_{l=0}^\infty A_lR^lP_l(\cos\theta)&=\sum_{l=0}^\infty B_lR^{-l-1}P_l(\cos\theta)\\
\Aboxed{B_l&=A_lR^{2l+1}}
\end{align}$$
Because of the charge at the interface, we must also have the follow field condition:
$$\begin{align}
\dfrac{\sigma}{\epsilon_0}&=
\left(\vec{E}_\text{out}-\vec{E}_\text{in}\right)\cdot\hat{r}\\
-\dfrac{\sigma}{\epsilon_0}&=
\left.\dfrac{\partial\Phi_\text{out}}{\partial r}\right|_{r=R}-\left.\dfrac{\partial\Phi_\text{in}}{\partial r}\right|_{r=R}\\
\dfrac{\sigma}{\epsilon_0}&=
\sum_{l=0}^\infty\left[(l+1)(A_lR^{2l+1})R^{-l-2}+lA_lR^{l-1}\right]P_l(\cos\theta)\\
\sigma&=2\epsilon_0\sum_{l=0}^\infty A_lR^{l-1}\dfrac{(2l+1)}{2}P_l(\cos\theta)
\end{align}$$
We can invert to find $A_l$ in terms of $\sigma$:
$$\begin{align}
\int_0^\pi\sigma P_{l'}(\cos\theta)\sin\theta\ d\theta&=
2\epsilon_0\sum_{l=0}^\infty A_lR^{l-1}\int_0^\pi\dfrac{(2l+1)}{2}P_l(\cos\theta)P_{l'}(\cos\theta)\sin\theta\ d\theta\\
2\epsilon_0 A_lR^{l-1}&=
\int_0^\pi\sigma P_{l}(\cos\theta)\sin\theta\ d\theta\\
 A_l&=\dfrac{1}{2\epsilon_0}R^{1-l}\int_0^\pi\sigma P_{l}(\cos\theta)\sin\theta\ d\theta
\end{align}$$
<div style="page-break-before: always;"></div>

We can substitute our charge distribution and reduce it to a simpler expression:
$$\begin{align}
A_l&=\dfrac{1}{2\epsilon_0}R^{1-l}\dfrac{Q}{4\pi R^2}\int_\alpha^\pi P_{l}(\cos\theta)\sin\theta\ d\theta+0\\
&=\dfrac{1}{2\epsilon_0}R^{1-l}\dfrac{Q}{4\pi R^2}\int_{-1}^{\cos\alpha} P_{l}(x)\ dx\\
&=\dfrac{1}{2\epsilon_0}R^{1-l}\dfrac{Q}{4\pi R^2}\int_{-1}^{\cos\alpha}\dfrac{d}{dx}\left(\dfrac{P_{l+1}(x)-P_{l-1}(x)}{2l+1}\right)\ dx\\
&=\dfrac{1}{2\epsilon_0}R^{1-l}\dfrac{Q}{4\pi R^2}\left(\dfrac{P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)}{2l+1}-\dfrac{(-1)^{l+1}P_{l+1}(+1)-(-1)^{l-1}P_{l-1}(+1)}{2l+1}\right)\\
&=\dfrac{Q}{8\pi R^2\epsilon_0}\dfrac{R^{1-l}}{2l+1}\left(P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)-(0-0)\right)\\
A_l&=\dfrac{Q}{8\pi R^2\epsilon_0}\dfrac{R^{1-l}}{2l+1}\left(P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right)\\
\end{align}$$
Substituting $A_l$, and $B_l=A_lR^{2l+1}$ into our original equation, the two potential functions are:
$$\begin{align}
\Aboxed{\Phi_\text{in}(r,\theta,\phi)&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{1}{2l+1}\dfrac{r^l}{R^{l+1}}\left(P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right)P_l(\cos\theta)}\\
\Aboxed{\Phi_\text{out}(r,\theta,\phi)&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{1}{2l+1}\dfrac{R^{l}}{r^{l+1}}\left(P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right)P_l(\cos\theta)}
\end{align}$$
---
### Question 3.2.B
Find the magnitude and the direction of the electric field at the origin.

The electric field can be found from the general equation (ignoring $\phi$ by symmetry):
$$\begin{align}
\vec{E}(\vec{r})&=-\left(\dfrac{\partial\Phi_\text{in}}{\partial r}\hat{r}+\dfrac{1}{r}\dfrac{\partial\Phi_\text{in}}{\partial\theta}\hat{\theta}\right)
\end{align}$$
The radial derivative is:
$$\begin{align}
\dfrac{\partial\Phi_\text{in}}{\partial r}&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=1}^\infty\dfrac{1}{2l+1}\dfrac{lr^{l-1}}{R^{l+1}}\left(P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right)P_l(\cos\theta)
\end{align}$$
And the polar derivative is:
$$\begin{align}
\dfrac{\partial\Phi_\text{in}}{\partial\theta}&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=1}^\infty\dfrac{1}{2l+1}\dfrac{r^{l}}{R^{l+1}}\left(P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right)\dfrac{dP_l(\cos\theta)}{d\theta}
\end{align}$$
<div style="page-break-before: always;"></div>

I had to go find the the following online, but I assume it comes from the recursion relation:
$$\begin{align}
\dfrac{dP_l(\cos\theta)}{d\theta}&=\dfrac{l\cos\theta P_l(\cos\theta)-l P_{l-1}(\cos\theta)}{\sin\theta}
\end{align}$$
Returning to the electric field, we get:
$$\begin{align}
\vec{E}(\vec{r})&=-\dfrac{Q}{8\pi\epsilon_0}\sum_{l=1}^\infty\dfrac{1}{2l+1}\dfrac{lr^{l-1}}{R^{l+1}}\left(P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right)P_l(\cos\theta)\hat{r}\\
&\ \ \ \ \ -\dfrac{Q}{8\pi\epsilon_0}\sum_{l=1}^\infty\dfrac{1}{2l+1}\dfrac{r^{l-1}}{R^{l+1}}\left(P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right)\dfrac{dP_l(\cos\theta)}{d\theta}\hat{\theta}\\\\
\vec{E}(r=0)&=-\dfrac{Q}{8\pi\epsilon_0}\dfrac{1}{2+1}\dfrac{1r^{1-1}}{R^{1+1}}\left(P_{1+1}(\cos\alpha)-P_{1-1}(\cos\alpha)\right)P_1(\cos\theta)\hat{r}+0+\dots\\
&\ \ \ \ \ -\dfrac{Q}{8\pi\epsilon_0}\dfrac{1}{2+1}\dfrac{r^{1-1}}{R^{1+1}}\left(P_{1+1}(\cos\alpha)-P_{1-1}(\cos\alpha)\right)\dfrac{dP_1(\cos\theta)}{d\theta}\hat{\theta}+0+\dots\\\\
&=-\dfrac{Q}{24\pi\epsilon_0R^{2}}\left(\dfrac{3\cos^2\alpha-1}{2}-1\right)\cos\theta\ \hat{r}+\dfrac{Q}{24\pi\epsilon_0 R^2}\left(\dfrac{3\cos^2\alpha-1}{2}-1\right)\sin\theta\ \hat{\theta}\\
&=-\dfrac{Q}{16\pi\epsilon_0R^{2}}\left(\cos^2\alpha-1\right)\cos\theta\ \hat{r}+\dfrac{Q}{16\pi\epsilon_0 R^2}\left(\cos^2\alpha-1\right)\sin\theta\ \hat{\theta}\\
&=\dfrac{Q}{16\pi\epsilon_0R^{2}}\sin^2\alpha\left(\cos\theta\ \hat{r}-\sin\theta\ \hat{\theta}\right)\\
\Aboxed{\vec{E}(r=0)&=\dfrac{Q\sin^2\alpha}{16\pi\epsilon_0R^{2}}\hat{z}}
\end{align}$$
---
### Question 3.2.C
Discuss the limiting forms of the potential (part A) and the electric field (part B)...
$$\begin{align}
\Phi_\text{in}(r,\theta,\phi)&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{1}{2l+1}\dfrac{r^l}{R^{l+1}}\left(P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right)P_l(\cos\theta)\\
\vec{E}(r=0)&=\dfrac{Q\sin^2\alpha}{16\pi\epsilon_0R^{2}}\hat{z}
\end{align}$$
<div style="page-break-before: always;"></div>

#### Question 3.2.C.I
As the spherical cap becomes very small ($\alpha\ll1$);

We can expand the polynomials about the point $x=1$ for our upcoming potential:
$$\begin{align}
P_{l}(\cos\alpha)&\approx P_{l}(1)-\dfrac{\alpha^2}{2}\left.\dfrac{dP_{l}(x)}{dx}\right|_{x=1}=1-\dfrac{\alpha^2}{2}\left.\dfrac{dP_{l}(x)}{dx}\right|_{x=1}\\
P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)&\approx-\dfrac{\alpha^2}{2}\left(\left.\dfrac{dP_{l+1}(x)}{dx}\right|_{x=1}-\left.\dfrac{dP_{l-1}(x)}{dx}\right|_{x=1}\right)\\
P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)&\approx-\dfrac{\alpha^2}{2}\left(2l+1\right)
\end{align}$$
However, for $l=0$, we actually get instead:
$$\begin{align}
P_{+1}(\cos\alpha)-P_{-1}(\cos\alpha)&=\cos\alpha+1\approx2-\dfrac{\alpha^2}{2}
\end{align}$$
Using these for the internal potential limits, we get:
$$\begin{align}
\lim_{\alpha\ll1}\Phi_\text{in}(r,\theta,\phi)&=\dfrac{Q}{8\pi\epsilon_0R}\left(2-\dfrac{\alpha^2}{2}\right)P_0(\cos\theta)+\dfrac{Q}{8\pi\epsilon_0}\sum_{l=1}^\infty\dfrac{1}{2l+1}\dfrac{r^l}{R^{l+1}}\left(-\dfrac{\alpha^2}{2}\left(2l+1\right)\right)P_l(\cos\theta)\\
&=\dfrac{Q}{4\pi\epsilon_0R}\left(1-\dfrac{\alpha^2}{4}\right)P_0(\cos\theta)-\dfrac{Q\alpha^2}{16\pi\epsilon_0}\sum_{l=1}^\infty\dfrac{r^l}{R^{l+1}}P_l(\cos\theta)\\
\Aboxed{\lim_{\alpha\ll1}\Phi_\text{in}(r,\theta,\phi)&=\dfrac{Q}{4\pi\epsilon_0R}P_0(\cos\theta)-\dfrac{Q\alpha^2}{16\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{r^l}{R^{l+1}}P_l(\cos\theta)}
\end{align}$$
I was looking at the Wikipedia for Legendre Polynomials and the 2nd term almost looks exactly like the generating function, so I can change the form of it:
$$\begin{align}
-\dfrac{Q\alpha^2}{16\pi\epsilon_0 R}\sum_{l=0}^\infty\left(\dfrac{r}{R}\right)^{l}P_l(\cos\theta)&=-\dfrac{Q\alpha^2}{16\pi\epsilon_0}\dfrac{1}{\sqrt{r^2+R^2-2rR\cos\theta}}
\end{align}$$
This looks like the magnitude of the difference of $\vec{r}$ and $R\hat{z}$, because of the $\cos\theta$:
$$\begin{align}
\lim_{\alpha\ll1}\Phi_\text{in}(r,\theta,\phi)&=\dfrac{Q}{8\pi\epsilon_0R}\left(2-\dfrac{\alpha^2}{2}\right)P_0(\cos\theta)+\dfrac{Q}{8\pi\epsilon_0}\sum_{l=1}^\infty\dfrac{1}{2l+1}\dfrac{r^l}{R^{l+1}}\left(-\dfrac{\alpha^2}{2}\left(2l+1\right)\right)P_l(\cos\theta)\\
&=\dfrac{Q}{4\pi\epsilon_0R}\left(1-\dfrac{\alpha^2}{4}\right)-\dfrac{Q\alpha^2}{16\pi\epsilon_0}\sum_{l=1}^\infty\dfrac{r^l}{R^{l+1}}P_l(\cos\theta)\\
\Aboxed{\lim_{\alpha\ll1}\Phi_\text{in}(r,\theta,\phi)&=\dfrac{Q}{4\pi\epsilon_0R}-\dfrac{Q\alpha^2}{16\pi\epsilon_0}\dfrac{1}{|\vec{r}-R\hat{z}|}}
\end{align}$$
So this is the potential due to a closed charged sphere and a potential of an opposite charge located exactly at the north pole of the sphere.

The external potential under this limit is pretty much the same (swapping $r$ and $R$):
$$\begin{align}
\Aboxed{\lim_{\alpha\ll1}\Phi_\text{out}(r,\theta,\phi)&=\dfrac{Q}{4\pi\epsilon_0r}-\dfrac{Q\alpha^2}{16\pi\epsilon_0}\dfrac{1}{|\vec{r}-R\hat{z}|}}
\end{align}$$
The electric field at the origin is really simple ($\sin\alpha\approx\alpha$):
$$\begin{align}
\Aboxed{\lim_{\alpha\ll1}\vec{E}(r=0)&=\dfrac{Q\alpha^2}{16\pi\epsilon_0R^{2}}\hat{z}}
\end{align}$$
---
#### Question 3.2.C.II
As the spherical cap becomes so large that the area with the charge on it becomes a very small cap at the south pole $(\alpha\sim\pi)$. Let the new angle be $\beta=\pi-\alpha$

We can use the same expansions as previous, so long as we include a factor $(-1)^l$:
$$\begin{align}
P_{l}(\cos\alpha)&\approx(-1)^l\left(1-\dfrac{\beta^2}{2}\left.\dfrac{dP_{l}(x)}{dx}\right|_{x=1}\right)\\
P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)&\approx(-1)^l\dfrac{\beta^2}{2}\left(2l+1\right)
\end{align}$$
Substituting into the internal potential, we get:
$$\begin{align}
\lim_{\beta\ll1}\Phi_\text{in}(r,\theta,\phi)
&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{1}{2l+1}\dfrac{r^l}{R^{l+1}}\dfrac{\beta^2}{2}\left(2l+1\right)(-1)^lP_l(\cos\theta)\\
&=\dfrac{Q\beta^2}{16\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{r^l}{R^{l+1}}P_l(-\cos\theta)
\end{align}$$
This almost has the same structure as the other limit, but with the point at $-R\hat{z}$:
$$\begin{align}
\Aboxed{\lim_{\pi-\alpha\ll1}\Phi_\text{in}(r,\theta,\phi)&=\dfrac{Q\alpha^2}{16\pi\epsilon_0}\dfrac{1}{|\vec{r}+R\hat{z}|}}
\end{align}$$
So this is the potential due to a charge located exactly at the south pole of the sphere, which makes sense, since all the charge will be there as $\alpha\rightarrow\pi$.

The external potential is once again very similar and simple (swapping $r$ and $R$), and the electric field at the origin is identical since $\sin\beta=\sin(\pi-\alpha)=\pi-\alpha$, so:
$$\begin{align}
\Aboxed{\lim_{\pi-\alpha\ll1}\Phi_\text{out}(r,\theta,\phi)&=\dfrac{Q\alpha^2}{16\pi\epsilon_0}\dfrac{1}{|\vec{r}+R\hat{z}|}} & \Aboxed{\lim_{\pi-\alpha\ll1}\vec{E}(r=0)&=\dfrac{Q(\pi-\alpha)^2}{16\pi\epsilon_0R^{2}}\hat{z}}
\end{align}$$
