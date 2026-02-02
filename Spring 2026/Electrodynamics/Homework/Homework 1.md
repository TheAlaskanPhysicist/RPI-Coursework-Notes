Author: Stanley Goodwin
Date: February 5th, 2026

---
## Question 2.1
A point charge $q$ is brought to a position a distance $d$ away from an infinite-plane conductor held at zero potential. Using the method of images, find:
### Question 2.1.A
The surface-charge density induced on the plane, and plot it;
![[Homework 1.2.1.A.png]]
**Pictured:** The induced charge on the plane can be represented as a ghost charge equidistant to the plane on the other side, of opposite charge, because the electric field must be perpendicular to a conducting surface (at equilibrium).

The potential of this system is the superposition of the point charge $q$ and the image charge $-q$:
$$\begin{align}
\Phi(x,y,z)&=\dfrac{1}{4\pi\epsilon_0}\dfrac{q}{\sqrt{x^2+y^2+(z-d)^2}}+\dfrac{1}{4\pi\epsilon_0}\dfrac{-q}{\sqrt{x^2+y^2+(z+d)^2}}\\
&=\dfrac{q}{4\pi\epsilon_0}\left(\dfrac{1}{\sqrt{x^2+y^2+(z-d)^2}}-\dfrac{1}{\sqrt{x^2+y^2+(z+d)^2}}\right)
\end{align}$$
We can find the electric field, then take the limit as $z\rightarrow0$ as:
$$\begin{align}
\vec{E}(x,y,z)&=-\vec\nabla\Phi(x,y,z)\\
&=-\dfrac{q}{4\pi\epsilon_0}\left(\dfrac{-\tfrac{1}{2}\left(2x+2y+2(z-d)\right)}{\left(x^2+y^2+(z-d)^2\right)^{3/2}}-\dfrac{-\tfrac{1}{2}\left(2x+2y+2(z+d)\right)}{\left(x^2+y^2+(z+d)^2\right)^{3/2}}\right)\\
\left.\vec{E}(x,y,z)\right|_{z=0}&=-\dfrac{q}{4\pi\epsilon_0}\left.\left(-\dfrac{\left(x+y+z-d\right)}{\left(x^2+y^2+(z-d)^2\right)^{3/2}}+\dfrac{\left(x+y+z+d\right)}{\left(x^2+y^2+(z+d)^2\right)^{3/2}}\right)\right|_{z=0}\\
&=-\dfrac{q}{4\pi\epsilon_0}\left(-\dfrac{\left(x+y-d\right)-\left(x+y+d\right)}{\left(x^2+y^2+d^2\right)^{3/2}}\right)\\
&=-\dfrac{q}{4\pi\epsilon_0}\left(\dfrac{2d}{\left(x^2+y^2+d^2\right)^{3/2}}\right)\\
\vec{E}(x,y,0)&=-\dfrac{q}{2\pi\epsilon_0}\dfrac{d}{\left(x^2+y^2+d^2\right)^{3/2}}
\end{align}$$
To find the surface charge distribution, we know that the density of electric field lines perpendicular to the surface can only change when there is a net charge on the interface:
$$\begin{align}
\epsilon_0\vec{E}_\text{above}^\perp-\epsilon_0\vec{E}_\text{below}^\perp&=\sigma
\end{align}$$
The bottom size of the plate has no electric field, thus all of the top field is generated from charge:
$$\begin{align}
\sigma&=\epsilon_0\lim_{z\rightarrow0^+}\vec{E}(x,y,z)-\epsilon_0\lim_{z\rightarrow0^-}\vec{E}(x,y,z)\\
&=\epsilon_0\left(-\dfrac{q}{2\pi\epsilon_0}\dfrac{d}{\left(x^2+y^2+d^2\right)^{3/2}}\right)-\epsilon_0(0)\\
\Aboxed{\sigma(x,y)&=-\dfrac{q}{2\pi}\dfrac{d}{\left(x^2+y^2+d^2\right)^{3/2}}}
\end{align}$$
We could also write this to be in cylindrical coordinates to be:
$$\begin{align}
\Aboxed{\sigma(r,\phi)&=-\dfrac{q}{2\pi}\dfrac{d}{\left(r^2+d^2\right)^{3/2}}}
\end{align}$$
Where $r$ is the radial distance from the origin within the plane $z=0$.

---
### Question 2.1.B
The force between the plane and the charge by using Coulomb's law for the force between a charge and its image;

The image charge is a charge of opposite sign at an equal distance to the plane. The force between them is then as follows:
$$\begin{align}
\vec{F}&=\dfrac{1}{4\pi\epsilon_0}\dfrac{q(-q)}{(2d)^2}\hat{z}\\
\Aboxed{\vec{F}_\text{charge}&=-\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}\hat{z}}\\
\Aboxed{\vec{F}_\text{plane}&=+\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}\hat{z}}\\
\end{align}$$
Where the subscript on force is the object feeling this force. Magnitude-wise:
$$\begin{align}
\Aboxed{\left|\vec{F}\right|&=\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}}
\end{align}$$
---
### Question 2.1.C
The total force acting on the plane by integrating $\sigma^2/2\epsilon_0$ over the whole plane;

Assuming the textbook isn't messing with me, we have:
$$\begin{align}
\left|\vec{F}\right|&=\int\dfrac{\sigma^2}{2\epsilon_0}\ dA
\end{align}$$
Using our equation (in the cylinder form), we get that:
$$\begin{align}
\left|\vec{F}\right|
&=\int_0^{2\pi}\int_0^\infty\dfrac{1}{2\epsilon_0}\left(-\dfrac{q}{2\pi}\dfrac{d}{\left(r^2+d^2\right)^{3/2}}\right)^2\ r\ dr\ d\phi\\
&=\dfrac{1}{2\epsilon_0}\left(\dfrac{qd}{2\pi}\right)^2\int_0^{2\pi}\int_0^\infty\dfrac{r}{\left(r^2+d^2\right)^{3}}\ dr\ d\phi
\end{align}$$
Let $u=r^2+d^2$, then $du=2r\ dr$, and so:
$$\begin{align}
\left|\vec{F}\right|
&=\dfrac{1}{2\epsilon_0}\left(\dfrac{qd}{2\pi}\right)^2\dfrac{1}{2}\int_0^{2\pi}\int_0^\infty\dfrac{2r}{\left(r^2+d^2\right)^{3}}\ dr\ d\phi\\
&=\dfrac{1}{4\epsilon_0}\dfrac{q^2d^2}{4\pi^2}\int_0^{2\pi}\int_{d^2}^\infty\dfrac{1}{u^{3}}\ du\ d\phi\\
&=\dfrac{q^2d^2}{16\pi^2\epsilon_0}\int_0^{2\pi}\left.\dfrac{1}{-2u^2}\right|_{d^2}^\infty\ d\phi\\
&=-\dfrac{q^2d^2}{32\pi^2\epsilon_0}\left.\dfrac{1}{u^2}\right|_{d^2}^\infty\int_0^{2\pi}\ d\phi\\
&=-\dfrac{q^2d^2}{32\pi^2\epsilon_0}\left(0-\dfrac{1}{(d^2)^2}\right)\cdot2\pi\\
&=\dfrac{2\pi q^2d^2}{32\pi^2\epsilon_0d^4}\\
\Aboxed{\left|\vec{F}\right|&=\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}}
\end{align}$$
This is is the same result found in part B. The force on the plane has a direction of $\hat{z}$, and so:
$$\begin{align}
\Aboxed{\vec{F}&=\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d^2}\hat{z}}
\end{align}$$
---
### Question 2.1.D
The work necessary to remove the charge $q$ from its position to infinity;

The work moving from $z=d$ to $z\rightarrow\infty$ can be done by integrating the force over displacement:
$$\begin{align}
W&=\int\vec{F}_\text{ext}\cdot d\vec{x}=-\int\vec{F}_\text{field}\cdot d\vec{x}\\
\end{align}$$
$$\begin{align}
\vec{F}_\text{charge}&=-\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{z^2}\hat{z}
\end{align}$$
In our case, $\vec{F}$ and $d\vec{x}$ both point in the $\hat{z}$ direction, so our work is:
$$\begin{align}
W&=-\int^{\infty}_d\left(-\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{z^2}\right)\ dz\\
&=-\dfrac{q^2}{16\pi\epsilon_0}\int^{\infty}_d\left(-\dfrac{1}{z^2}\right)\ dz\\
&=-\dfrac{q^2}{16\pi\epsilon_0}\left.\dfrac{1}{z}\right|^{\infty}_d\\
&=-\dfrac{q^2}{16\pi\epsilon_0}\left(0-\dfrac{1}{d}\right)\\
\Aboxed{W&=+\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d}}
\end{align}$$
---
### Question 2.1.E
The potential energy between the charge $q$ and its image (compare to part D and discuss);

For point charges, we have:
$$\begin{align}
U&=\dfrac{1}{4\pi\epsilon}\sum_{i<j}\dfrac{q_iq_j}{r_{ij}}
\end{align}$$
We have 2 effective point charges, with $r=d-(-d)=2d$ distance, and so:
$$\begin{align}
U&=\dfrac{1}{4\pi\epsilon_0}\dfrac{(+q)(-q)}{2d}\\
\Aboxed{U&=-\dfrac{1}{8\pi\epsilon_0}\dfrac{q^2}{d}}
\end{align}$$
Normally, we'd expect that $W=-U$. I believe this is an artifact of the image charge not actually being a real charge, and that the conductor with its free-moving charges requires no energy differential, and thus half the energy for work doesn't exist.

---
### Question 2.1.F
Find the answer to part D in electron volts for an electron originally one angstrom from the surface.

Special thanks to [Wikipedia](https://en.wikipedia.org/wiki/Vacuum_permittivity) for the super convenient value for $\epsilon_0$:
$$\begin{align}
W&=+\dfrac{1}{16\pi\epsilon_0}\dfrac{q^2}{d}\\
&=\dfrac{1}{16\pi\left(55.263\text{ e}^2\cdot\text{eV}^{-1}\cdot\mu\text{m}^{-1}\right)}\dfrac{\text{e}^2}{1\cdot10^{-4}\mu\text{m}}\\
&=\dfrac{1}{16\pi\left(55.263\right)\cdot10^{-4}}\text{eV}\\
\Aboxed{W&=3.600\text{ eV}}
\end{align}$$
---
## Question 2.7
Consider a potential problem in the half-space defined by $z\ge0$, with (homogenous) Dirichlet boundary conditions on the plane $z=0$ (and at infinity).
![[Homework 1.2.7.png]]
### Question 2.7.A
Write down an appropriate Green's function $G(\vec{x},\vec{x}')$.

The typical Green's function for the Laplacian is as follows (Eq 1.40):
$$\begin{align}
G(\vec{x},\vec{x}')&=\dfrac{1}{|\vec{x}-\vec{x}'|}+F(\vec{x},\vec{x}') & \vec\nabla'^2F(\vec{x},\vec{x}')&=0
\end{align}$$
We would like the Green's function to vanish on the plane $z=0$ and at infinity.
To have $z=0$ also make the Green's function, we can add a reflected anti-charge like that through the method of images to give us:
$$\begin{align}
G(\vec{x},\vec{x}')&=\dfrac{1}{|\vec{x}-\vec{x}'|}-\dfrac{1}{|\vec{x}-\vec{x}_r'|}=G(\vec{x}-\vec{x}')
\end{align}$$
where $\vec{x}_r'$ is $\vec{x}'$ reflected across the $xy$-plane. As in: $\vec{x}_r'=(x',y',-z')$. I am unsure how to do this in general, but for this case it is relatively simple. This satisfies what we would like:
$$\begin{align}
\lim_{z'\rightarrow0}G(\vec{x}-\vec{x}')&=\dfrac{1}{|\vec{x}-\vec{x}'|}-\dfrac{1}{|\vec{x}-\vec{x}'|}=0
\end{align}$$
Since the next part is in cylindrical coordinates, we can transform the Green's Function into:
$$\begin{align}
G(\vec{r},\vec{r}')&=\dfrac{1}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi-\phi')+(z-z')^2)^{1/2}}-\dfrac{1}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi-\phi')+(z+z')^2)^{1/2}}
\end{align}$$
Where we use the law of cosines to find the magnitude of the non-$z$ components.

---
### Question 2.7.B
If the potential on the plane $z=0$ is specified to be $\Phi=V$ inside a circle of radius $a$ centered at the origin, and $\Phi=0$ outside that circle, find an integral expression for the potential at a point $P$ specified in cylindrical coordinates $(\rho,\phi,z)$.

The general form the equation we need is:
$$\begin{align}
\Phi(\vec{x})&=-\dfrac{1}{4\pi}\oint_{\partial\Omega}\Phi(\vec{x}')\left(\hat{n}\cdot\nabla' G(\vec{x},\vec{x}')\right)\ dS'+\dfrac{1}{4\pi}\int_\Omega G(\vec{x},\vec{x}')\nabla^2\Phi(\vec{x}')\ dV'
\end{align}$$
Assuming by "potential problem" it means that $\rho(\vec{x})=0$, then:
$$\begin{align}
\Phi(\vec{x})&=-\dfrac{1}{4\pi}\oint_{\partial\Omega}\Phi(\vec{x}')\left(\hat{n}\cdot\nabla' G(\vec{x},\vec{x}')\right)\ dS'
\end{align}$$
The normal at the boundary of $z=0$ points in the $-\hat{z}$ direction, thus:
$$\begin{align}
\Phi(\vec{x})&=+\dfrac{1}{4\pi}\oint_{\partial\Omega}\Phi(\rho',\phi',0)\left.\dfrac{\partial G(\vec{x},\vec{x}')}{\partial z'}\right|_{z'=0}\ dS'
\end{align}$$
We know the Green's function in cylindrical form, from part A, to be:
$$\begin{align}
G(\vec{x},\vec{x}')&=\dfrac{1}{(\dots+(z-z')^2)^{1/2}}-\dfrac{1}{(\dots+(z+z')^2)^{1/2}}
\end{align}$$
The derivative with respect to $z'$ is then:
$$\begin{align}
\left.\dfrac{\partial G(\vec{x},\vec{x}')}{\partial z'}\right|_{z'=0}
&=\left.\dfrac{\partial}{\partial z'}\dfrac{1}{(\dots+(z-z')^2)^{1/2}}\right|_{z'=0}-\left.\dfrac{\partial}{\partial z'}\dfrac{1}{(\dots+(z+z')^2)^{1/2}}\right|_{z'=0}\\
&=\left.\dfrac{-\tfrac{1}{2}\cdot2(z-z')\cdot-1}{(\dots+(z-z')^2)^{3/2}}\right|_{z'=0}-\left.\dfrac{-\tfrac{1}{2}\cdot2(z+z')\cdot1}{(\dots+(z+z')^2)^{3/2}}\right|_{z'=0}\\
&=\dfrac{z}{(\dots+z^2)^{3/2}}+\dfrac{z}{(\dots+z^2)^{3/2}}\\
\Aboxed{\left.\dfrac{\partial G(\vec{x},\vec{x}')}{\partial z'}\right|_{z'=0}&=\dfrac{2z}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi-\phi')+z^2)^{3/2}}}
\end{align}$$
Substituting back in for the potential, we get:
$$\begin{align}
\Phi(\vec{x})
&=\dfrac{1}{4\pi}\oint_{\partial\Omega}\Phi(\rho',\phi',0)\left.\dfrac{\partial G(\vec{x},\vec{x}')}{\partial z'}\right|_{z'=0}\ dS'\\
&=\dfrac{1}{4\pi}\int_0^{2\pi}\int_0^\infty V(\rho\le a)\dfrac{2z}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi-\phi')+z^2)^{3/2}}\ \rho'\ d\rho'\ d\phi'\\
\Aboxed{\Phi(\vec{x})&=\dfrac{Vz}{2\pi}\int_0^{2\pi}\int_0^a \dfrac{\rho'\ d\rho'\ d\phi'}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi')+z^2)^{3/2}}}
\end{align}$$
The $\phi-\phi'\rightarrow\phi'$ comes from the integration happing over the whole cyclic interval and even.

---
### Question 2.7.C
Show that, along the axis of the circle ($\rho=0$), the potential is given by:
$$\begin{align}
\Phi&=V\left(1-\dfrac{z}{\sqrt{a^2+z^2}}\right)
\end{align}$$
Using our equation for the potential above, we can substitute $\rho=0$:
$$\begin{align}
\Phi(\vec{x})
&=\dfrac{Vz}{2\pi}\int_0^{2\pi}\int_0^a \dfrac{\rho'\ d\rho'\ d\phi'}{(\rho'^2+z^2)^{3/2}}
\end{align}$$
Let $x=\rho'^2+z^2$, $dx=2\rho'd\rho'$:
$$\begin{align}
\Phi(\vec{x})
&=\dfrac{Vz}{2\pi}\int_0^a \dfrac{\tfrac{1}{2}\cdot(2\rho'\ d\rho')}{(\rho'^2+z^2)^{3/2}}\int_0^{2\pi} d\phi'\\
&=\dfrac{Vz}{4\pi}\int_{\rho=0}^{\rho=a} \dfrac{dx}{x^{3/2}}\cdot 2\pi\\
&=\dfrac{Vz}{2}\left.\dfrac{\left(\rho'^2+z^2\right)^{-1/2}}{-1/2}\right|_{\rho=0}^{\rho=a}\\
&=V\left(\dfrac{z}{\sqrt{0^2+z^2}}-\dfrac{z}{\sqrt{a^2+z^2}}\right)\\
\Aboxed{\Phi(\vec{x})&=V\left(1-\dfrac{z}{\sqrt{a^2+z^2}}\right)}
\end{align}$$
---
### Question 2.7.D
Show that at large distances $\rho^2+z^2\gg a^2$, the potential can be expanded in a power series in $(\rho^2+z^2)^{-1}$, and that the leading terms are:
$$\begin{align}
\Phi&=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}\left[1-\dfrac{3a^2}{4(\rho^2+z^2)}+\dfrac{5(3\rho^2a^2+a^4)}{8(\rho^2+z^2)^2}+\dots\right]
\end{align}$$
Verify that the result of parts C and D are consistent with each-other in their common range of validity.

We start with our equation from part B:
$$\begin{align}
\Phi(\vec{x})
&=\dfrac{Vz}{2\pi}\int_0^{2\pi}\int_0^a \dfrac{\rho'\ d\rho'\ d\phi'}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi')+z^2)^{3/2}}\\
&=\dfrac{Vz}{2\pi}\int_0^{2\pi}\int_0^a \dfrac{1}{\tfrac{(\rho^2+z^2)^{3/2}}{(\rho^2+z^2)^{3/2}}}\dfrac{\rho'\ d\rho'\ d\phi'}{(\rho^2+\rho'^2-2\rho\rho'\cos(\phi')+z^2)^{3/2}}\\
&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\dfrac{\rho'\ d\rho'\ d\phi'}{\left(1+\dfrac{\rho'^2-2\rho\rho'\cos(\phi')}{(\rho^2+z^2)}\right)^{3/2}}
\end{align}$$
In the case that $\rho^2+z^2\gg a^2$, we also know that $\rho^2+z^2\gg \rho'^2$, and $\rho^2+z^2\gg \rho\rho'$.
For the sake of space, let $\epsilon=\epsilon(\rho,\rho',\phi',z)=\dfrac{\rho'^2-2\rho\rho'\cos(\phi')}{\rho^2+z^2}$.
$$\begin{align}
\lim_{\rho^2+z^2\gg a^2}\Phi(\vec{x})
&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\lim_{\rho^2+z^2\gg a^2}\rho'\left(1+\epsilon\right)^{-3/2}\ d\rho'\ d\phi'\\
&\approx\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\rho'\left[1-\dfrac{3}{2}\epsilon+\dfrac{\tfrac{3}{2}\tfrac{5}{2}}{2}\epsilon^2+\dots\right]\ d\rho'\ d\phi'\\
\end{align}$$
The 0th order term:
$$\begin{align}
\Phi^{0}(\vec{x})
&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\rho'\ d\rho'\ d\phi'\\
&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\dfrac{a^2}{2}\ d\phi'\\
\Phi^{0}(\vec{x})&=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}
\end{align}$$
The 1st order term:
$$\begin{align}
\Phi^1(\vec{x})
&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\rho'\left[-\dfrac{3}{2}\dfrac{\rho'^2-2\rho\rho'\cos(\phi')}{\rho^2+z^2}\right]\ d\rho'\ d\phi'\\
&=-\dfrac{3Vz}{4\pi}\dfrac{1}{(\rho^2+z^2)^{5/2}}\int_0^{2\pi}\int_0^a\left[\rho'^3-2\rho\rho'^2\cos(\phi')\right]\ d\rho'\ d\phi'\\
&=-\dfrac{3Vz}{4\pi}\dfrac{1}{(\rho^2+z^2)^{5/2}}\int_0^{2\pi}\left[\dfrac{a^4}{4}-2\rho\dfrac{a^3}{3}\cos(\phi')\right]\ d\phi'\\
&=-\dfrac{3Vz}{4\pi}\dfrac{1}{(\rho^2+z^2)^{5/2}}\left[2\pi\dfrac{a^4}{4}+0\right]\\
&=-\dfrac{3Va^4}{8}\dfrac{z}{(\rho^2+z^2)^{5/2}}\\
\Phi^1(\vec{x})&=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}\left(-\dfrac{3a^2}{4}\dfrac{1}{(\rho^2+z^2)}\right)
\end{align}$$
The 2nd order term:
$$\begin{align}
\Phi^2(\vec{x})
&=\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\rho'\left[\dfrac{\tfrac{3}{2}\tfrac{5}{2}}{2}\epsilon^2\right]\ d\rho'\ d\phi'\\
&=\dfrac{15}{8}\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{3/2}}\int_0^{2\pi}\int_0^a\rho'\left[\dfrac{\rho'^2-2\rho\rho'\cos(\phi')}{\rho^2+z^2}\right]^2\ d\rho'\ d\phi'\\
&=\dfrac{15}{8}\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{7/2}}\int_0^{2\pi}\int_0^a\rho'\left[\rho'^4-4\rho\rho'^3\cos(\phi')+4\rho^2\rho'^2\cos(\phi')^2\right]\ d\rho'\ d\phi'\\
&=\dfrac{15}{8}\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{7/2}}\int_0^{2\pi}\left[\dfrac{a^6}{6}-4\rho\dfrac{a^5}{5}\cos(\phi')+4\rho^2\dfrac{a^4}{4}\cos(\phi')^2\right]\ d\phi'\\
&=\dfrac{15}{8}\dfrac{Vz}{2\pi}\dfrac{1}{(\rho^2+z^2)^{7/2}}\left[2\pi\dfrac{a^6}{6}-0+4\rho^2\dfrac{a^4}{4}\pi\right]\\
\Phi^2(\vec{x})&=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}\left[\dfrac{5(3\rho^2a^2+a^4)}{8(\rho^2+z^2)^{2}}\right]\\
\end{align}$$
Together, we can see that:
$$\begin{align}
\Aboxed{\Phi&=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}\left[1-\dfrac{3a^2}{4(\rho^2+z^2)}+\dfrac{5(3\rho^2a^2+a^4)}{8(\rho^2+z^2)^2}+\dots\right]}
\end{align}$$
In the limit as $\rho\rightarrow 0$, we can see that:
$$\begin{align}
\lim_{\rho\rightarrow0}\Phi
&=\dfrac{Va^2}{2}\dfrac{z}{(z^2)^{3/2}}\left[1-\dfrac{3a^2}{4(z^2)}+\dfrac{5(a^4)}{8(z^2)^2}+\dots\right]\\
&=\dfrac{Va^2}{2}\dfrac{1}{z^2}\left[1-\dfrac{3}{4}\left(\dfrac{a}{z}\right)^2+\dfrac{5}{8}\left(\dfrac{a}{z}\right)^4+\dots\right]\\
&=V\left[(1-1)+\dfrac{1}{2}\left(\dfrac{a}{z}\right)^2-\dfrac{3}{8}\left(\dfrac{a}{z}\right)^4+\dfrac{5}{16}\left(\dfrac{a}{z}\right)^6+\dots\right]\\
&=V-V\left[1-\dfrac{1}{2}\left(\dfrac{a}{z}\right)^2+\dfrac{3}{8}\left(\dfrac{a}{z}\right)^4-\dfrac{5}{16}\left(\dfrac{a}{z}\right)^6+\dots\right]\\
&=V-V\left[1+\left(\dfrac{a}{z}\right)^2\right]^{-\tfrac{1}{2}}\\
&=V\left(1-\dfrac{1}{\sqrt{1+\left(\tfrac{a}{z}\right)^2}}\right)\\
\Aboxed{\lim_{\rho\rightarrow0}\Phi&=V\left(1-\dfrac{z}{\sqrt{z^2+a^2}}\right)}
\end{align}$$
---
## Question 3.1
Two concentric spheres have radii $a,b$ $(b>a)$ and each is divided into two hemispheres by the same horizontal plane. The upper hemisphere of the inner sphere and the lower hemisphere of the outer sphere are maintained at potential $V$. The other hemispheres are at zero potential.

Determined the potential in the region $a\le r\le b$ as a series of Legendre polynomials. Include terms at least up to $l=4$. Check your solution against the know results in the limiting cases $b\rightarrow\infty$ and $a\rightarrow 0$.

### Solution to Equation
I'm not really even sure where to start, so I'll write out the boundary conditions:
$$\begin{align}
\Phi(a,\theta)&=\begin{cases}V&\theta\in[0,\pi/2)\\0&\theta\in(\pi/2,\pi]\end{cases} & \Phi(b,\theta)&=\begin{cases}0&\theta\in[0,\pi/2)\\V&\theta\in(\pi/2,\pi]\end{cases} 
\end{align}$$
Since there is azimuthal symmetry, we can use:
$$\begin{align}
\Phi(r,\theta)&=\sum_{l=0}^\infty\left(A_lr^l+B_lr^{-l-1}\right)P_l(\cos\theta)
\end{align}$$
The boundary conditions must also take this form at $r=a$ and $r=b$, and so we get:
$$\begin{align}
\Phi(a,\theta)&=\sum_{l=0}^\infty c_l^{r=a}P_l(\cos\theta) & c_l^{r=a}&=\dfrac{2l+1}{2}\int_0^\pi P_l(\cos\theta)\Phi(a,\theta)\sin\theta\ d\theta\\
\Phi(b,\theta)&=\sum_{l=0}^\infty c_l^{r=b}P_l(\cos\theta) & c_l^{r=b}&=\dfrac{2l+1}{2}\int_0^\pi P_l(\cos\theta)\Phi(b,\theta)\sin\theta\ d\theta\\
\end{align}$$
Lets start with $r=a$:
$$\begin{align}
c_l^{r=a}
&=\dfrac{2l+1}{2}\int_0^\pi P_l(\cos\theta)\Phi(a,\theta)\sin\theta\ d\theta\\
&=\dfrac{2l+1}{2}\int_0^{\pi/2} P_l(\cos\theta)V\sin\theta\ d\theta+0\\
&=-V\dfrac{2l+1}{2}\int_0^{\pi/2} P_l(\cos\theta)\cdot(-\sin\theta\ d\theta)\\
\end{align}$$
Let $u=\cos\theta$, then $du=-\sin\theta\ d\theta$ from $u=1$ to $u=0$:
$$\begin{align}
c_l^{r=a}
&=-V\dfrac{2l+1}{2}\int_0^{\pi/2} P_l(\cos\theta)\cdot(-\sin\theta\ d\theta)\\
&=-V\dfrac{2l+1}{2}\int_1^{0} P_l(u)\ du\\
\Aboxed{c_l^{r=a}&=V\dfrac{2l+1}{2}\int_0^{1} P_l(u)\ du}
\end{align}$$
Likewise, for $r=b$:
$$\begin{align}
c_l^{r=b}
&=\dfrac{2l+1}{2}\int_0^\pi P_l(\cos\theta)\Phi(b,\theta)\sin\theta\ d\theta\\
&=\dfrac{2l+1}{2}\int_{\pi/2}^{\pi} P_l(\cos\theta)V\sin\theta\ d\theta+0\\
&=-V\dfrac{2l+1}{2}\int_{\pi/2}^{\pi} P_l(\cos\theta)\cdot(-\sin\theta\ d\theta)\\
&=-V\dfrac{2l+1}{2}\int_{0}^{-1} P_l(u)\ du\\
\Aboxed{c_l^{r=b}&=V\dfrac{2l+1}{2}\int_{-1}^{0} P_l(u)\ du}
\end{align}$$
We can use the knowledge that under $u\rightarrow -u$, $P_l(-u)=(-1)^lP_l(u)$, and so we have:
$$\begin{align}
\Aboxed{c_l^{r=a}&=V\dfrac{2l+1}{2}\int_0^{1} P_l(u)\ du} & \Aboxed{c_l^{r=b}&=(-1)^lc_l^{r=a}=V\dfrac{2l+1}{2}(-1)^l\int_{0}^{1} P_l(u)\ du}
\end{align}$$
For the region $r\in[a,b]$, we expect the solution to be of the form:
$$\begin{align}
\Phi(r,\theta)&=\sum_{l=0}^\infty\left(A_lr^l+B_lr^{-l-1}\right)P_l(\cos\theta)
\end{align}$$
The boundary conditions then become:
$$\begin{align}
A_la^l+B_la^{-l-1}&=c_l^{r=a} & A_lb^l+B_lb^{-l-1}&=c_l^{r=b}=(-1)^lc_l^{r=a}
\end{align}$$
This becomes a system of equations we can invert:
$$\begin{align}
\begin{bmatrix}a^l&a^{-l-1}\\b^l&b^{-l-1}\end{bmatrix}\begin{bmatrix}A_l\\B_l\end{bmatrix}&=c_l^{r=a}\begin{bmatrix}1\\(-1)^l\end{bmatrix} &\implies&&
\dfrac{c_l^{r=a}}{a^{2l+1}-b^{2l+1}}\begin{bmatrix}a^{l+1}&-b^{l+1}\\-a^{l+1}b^{2l+1}&a^{2l+1}b^{l+1}\end{bmatrix}\begin{bmatrix}1\\(-1)^l\end{bmatrix}&=\begin{bmatrix}A_l\\B_l\end{bmatrix}
\end{align}$$
More explicitly, we get:
$$\begin{align}
\Aboxed{A_l&=\dfrac{a^{l+1}-(-1)^lb^{l+1}}{a^{2l+1}-b^{2l+1}}c_l^{r=a}} & \Aboxed{B_l&=\dfrac{-a^{l+1}b^{2l+1}+(-1)^la^{2l+1}b^{l+1}}{a^{2l+1}-b^{2l+1}}c_l^{r=a}}
\end{align}$$
The solution then is the following:
$$\begin{align}
\Phi(r,\theta)&=\sum_{l=0}^\infty\left(\dfrac{a^{l+1}-(-1)^lb^{l+1}}{a^{2l+1}-b^{2l+1}}r^l-\dfrac{a^{l+1}b^{2l+1}-(-1)^la^{2l+1}b^{l+1}}{a^{2l+1}-b^{2l+1}}r^{-l-1}\right)c_l^{r=a}P_l(\cos\theta)\\
c_l^{r=a}&=V\dfrac{2l+1}{2}\int_0^{1} P_l(x)\ dx
\end{align}$$
Some useful term parametrizations are:
$$\begin{align}
l&=0 &&
1 &&
0\\
l&=2k &&
\dfrac{a^{2k+1}-b^{{2k}+1}}{a^{4k+1}-b^{4k+1}} &&
\dfrac{a^{4k+1}b^{2k+1}-a^{2k+1}b^{4k+1}}{a^{4k+1}-b^{4k+1}}\\
l&=2k-1 &&
\dfrac{a^{2k}+b^{2k}}{a^{4k-1}-b^{4k-1}} &&
-\dfrac{a^{2k}b^{4k-1}+a^{4k-1}b^{2k}}{a^{4k-1}-b^{4k-1}}\\
\end{align}$$
Using the Legendre Polynomial table on Wikipedia and lots of editing later:
$$\begin{align}
c_0^{r=a}&=V\dfrac{1}{2}\int_0^{1} \left(1\right)\ dx &
c_0^{r=a}&=\dfrac{1}{2}V\\
c_1^{r=a}&=V\dfrac{3}{2}\int_0^{1} \left(x\right)\ dx &
c_1^{r=a}&=\dfrac{3}{4}V\\
c_2^{r=a}&=V\dfrac{5}{2}\int_0^{1} \dfrac{1}{2}\left(3x^2-1\right)\ dx &
c_2^{r=a}&=0\\
c_3^{r=a}&=V\dfrac{7}{2}\int_0^{1} \dfrac{1}{2}\left(5x^3-3x\right)\ dx &
c_3^{r=a}&=-\dfrac{7}{16}V\\
c_4^{r=a}&=V\dfrac{9}{2}\int_0^{1} \dfrac{1}{8}\left(35x^4-30x^2+3\right)\ dx &
c_4^{r=a}&=0
\end{align}$$
We can also write a table for each addition to the potential term:
$$\begin{align}
\Phi^0(r,\theta)&=\left(1r^0-0r^{-1}\right)\cdot\dfrac{1}{2}V\cdot 1\\
\Phi^1(r,\theta)&=\left(\dfrac{a^{2}+b^{2}}{a^{3}-b^{3}}r-\dfrac{a^{2}b^{3}+a^{3}b^{2}}{a^{3}-b^{3}}r^{-2}\right)\cdot\dfrac{3}{4}V\cdot \cos\theta\\
\Phi^2(r,\theta)&=\left(\dfrac{a^{3}-b^{3}}{a^{5}-b^{5}}r^2-\dfrac{a^{3}b^{5}-a^{5}b^{3}}{a^{5}-b^{5}}r^{-3}\right)\cdot0V\cdot\dfrac{1}{2}\left(3\cos^2\theta-1\right)\\
\Phi^3(r,\theta)&=\left(\dfrac{a^{4}+b^{4}}{a^{7}-b^{7}}r^3-\dfrac{a^{4}b^{7}+a^{7}b^{4}}{a^{7}-b^{7}}r^{-4}\right)\cdot-\dfrac{7}{16}V\cdot \dfrac{1}{2}\left(5\cos^3\theta-3\cos\theta\right)\\
\Phi^4(r,\theta)&=\left(\dfrac{a^{5}-b^{5}}{a^{9}-b^{9}}r^4-\dfrac{a^{5}b^{9}-a^{9}b^{5}}{a^{9}-b^{9}}r^{-5}\right)\cdot0V\cdot \dfrac{1}{8}\left(35\cos^4\theta-30\cos^2\theta+3\right)
\end{align}$$
All together, the approximation to $l=4$ is:
$$\begin{align}
\Phi(r,\theta)&\approx\dfrac{V}{2}+\dfrac{V}{2}\left[\dfrac{3}{2}\dfrac{a^{2}+b^{2}}{a^{3}-b^{3}}r-\dfrac{3}{2}\dfrac{a^{2}b^{3}\\+a^{3}b^{2}}{a^{3}-b^{3}}r^{-2}\right]\cos\theta\\
&+\dfrac{V}{2}\left[-\dfrac{7}{16}\dfrac{a^{4}+b^{4}}{a^{7}-b^{7}}r^3+\dfrac{7}{16}\dfrac{a^{4}b^{7}+a^{7}b^{4}}{a^{7}-b^{7}}r^{-4}\right]\left(5\cos^3\theta-3\cos\theta\right)+\dots
\end{align}$$
### Limiting Cases
In the limit as $b\rightarrow\infty$, we see that:
$$\begin{align}
\lim_{b\rightarrow\infty}\Phi(r,\theta)&\approx\dfrac{V}{2}\left[1+\dfrac{3}{2}\dfrac{a^{2}}{r^2}\cos\theta-\dfrac{7}{16}\dfrac{a^{4}}{r^4}(5\cos^3\theta-3\cos\theta)+\dots\right]
\end{align}$$
In the limit as $a\rightarrow0$, we see that:
$$\begin{align}
\lim_{a\rightarrow0}\Phi(r,\theta)&\approx\dfrac{V}{2}\left[1-\dfrac{3}{2}\dfrac{r}{b}\cos\theta+\dfrac{7}{16}V\dfrac{r^3}{b^{3}}(5\cos^3\theta-3\cos\theta)+\dots\right]
\end{align}$$
I looked up the equations for the real limit cases and they match. I'm exhausted of arithmetic.

---
## Question 3.2
A spherical surface of radius $R$ has charge uniformly distributed over its surface with a density $Q/4\pi R^2$, except for a spherical cap at the north pole, defined by the cone $\theta=\alpha$.

We can write the charge density as the following:
$$\begin{align}
\sigma(\theta,\phi)&=\begin{cases}0&0\le\theta\le\alpha\\\dfrac{Q}{4\pi R^2}&\alpha\lt\theta\le\pi\end{cases}
\end{align}$$
It took me a bit to understand what he meant by "except".
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










$$\begin{align}
\Phi&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{1}{2l+1}\left[P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right]\dfrac{r^l}{R^{l+1}}P_{l}(\cos\theta)
\end{align}$$







Inside the surface$\implies$no charge, so this is the much simpler case:
$$\begin{align}
\Phi_\text{in}(r,\theta,\phi)&=\sum_{l=0}^\infty A_lr^lP_l(\cos\theta)
\end{align}$$
The outside potential is similar, but of the diverging terms:
$$\begin{align}
\Phi_\text{out}(r,\theta,\phi)&=\sum_{l=0}^\infty B_lr^{-l-1}P_l(\cos\theta)
\end{align}$$
However, we still require a boundary condition. Similar to previous, we know that:
$$\begin{align}
\epsilon_0\vec{E}_\text{above}^\perp-\epsilon_0\vec{E}_\text{below}^\perp&=\sigma
\end{align}$$
Our system is a sphere which makes this significantly easier, and so:

Writing in terms of the potential, we see that:
$$\begin{align}
\left.\dfrac{\partial\Phi_\text{out}}{\partial r}-\dfrac{\partial\Phi_\text{in}}{\partial r}\right|_{r=R}&=-\dfrac{1}{\epsilon_0}\begin{cases}0&0\le\theta\le\alpha\\\dfrac{Q}{4\pi R^2}&\alpha\lt\theta\le\pi\end{cases}\\
\end{align}$$
Substituting our general forms for the potential, we get:
$$\begin{align}
\left.\dfrac{\partial}{\partial r}\sum_{l=0}^\infty B_lr^{-l-1}P_l(\cos\theta)\right|_{r=R}-\left.\dfrac{\partial}{\partial r}\sum_{l=0}^\infty A_lr^lP_l(\cos\theta)\right|_{r=R}&=\left.\dfrac{\partial\Phi_\text{out}}{\partial r}-\dfrac{\partial\Phi_\text{in}}{\partial r}\right|_{r=R}\\
-\left.\sum_{l=0}^\infty B_l(l+1)r^{-l-2}P_l(\cos\theta)\right|_{r=R}-\left.\sum_{l=0}^\infty lA_lr^{l-1}P_l(\cos\theta)\right|_{r=R}&=
-\dfrac{1}{\epsilon_0}\begin{cases}0&0\le\theta\le\alpha\\\dfrac{Q}{4\pi R^2}&\alpha\lt\theta\le\pi\end{cases}\\
\sum_{l=0}^\infty\left(B_l(l+1)r^{-l-2}+lA_lr^{l-1}\right)P_l(\cos\theta)&=\dfrac{1}{\epsilon_0}\begin{cases}0&0\le\theta\le\alpha\\\dfrac{Q}{4\pi R^2}&\alpha\lt\theta\le\pi\end{cases}
\end{align}$$
Not sure where to go from here, so I'll calculate charge instead:
$$\begin{align}
Q_\text{real}
&=\int_0^{2\pi}\int_0^{\pi}\int_0^\infty\sigma(\theta,\phi)\delta(r-R)\ r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=\int_0^\infty\delta(r-R)\ r^2\ dr\ \int_0^{\pi}\sin\theta\begin{cases}0&0\le\theta\le\alpha\\\dfrac{Q}{4\pi R^2}&\alpha\lt\theta\le\pi\end{cases}\ d\theta\ \int_0^{2\pi}d\phi\\
&=\dfrac{Q}{4\pi R^2}\int_0^\infty\delta(r-R)\ r^2\ dr\ \int_\alpha^{\pi}\sin\theta\ d\theta\ \int_0^{2\pi}d\phi\\
&=\dfrac{Q}{4\pi R^2}\cdot R^2\cdot\left.-\cos\theta\right|_\alpha^{\pi}\cdot2\pi\\
&=-\dfrac{Q}{2}\cdot\left(\cos\pi-\cos\alpha\right)\\
&=Q\dfrac{1+\cos\alpha}{2}\\
Q_\text{real}&=Q\cos^2\left(\dfrac{\alpha}{2}\right)
\end{align}$$
When we go $r\rightarrow\infty$:
$$\begin{align}
\lim_{r\rightarrow\infty}\sum_{l=0}^\infty B_lr^{-l-1}P_l(\cos\theta)&=\lim_{r\rightarrow\infty}\Phi_\text{out}(r,\theta,\phi)\\
B_0r^{-1}P_0(\cos\theta)&=\dfrac{1}{4\pi\epsilon_0}\dfrac{Q_\text{real}}{r}\\
B_0&=\dfrac{Q}{4\pi\epsilon_0}\cos^2\left(\dfrac{\alpha}{2}\right)\\
\end{align}$$
The potential must be continuous from both sides, so:
$$\begin{align}
\sum_{l=0}^\infty B_lR^{-l-1}P_l(\cos\theta)&=\sum_{l=0}^\infty A_lR^lP_l(\cos\theta)\\
B_lR^{-l-1}&=A_lR^l\\
B_l&=A_lR^{2l+1}
\end{align}$$
The potentials are then:
$$\begin{align}
\Phi_\text{in}(r,\theta,\phi)&=\dfrac{Q}{4\pi\epsilon_0R}\cos^2\left(\dfrac{\alpha}{2}\right)+\sum_{l=1}^\infty A_lr^lP_l(\cos\theta)\\
\Phi_\text{out}(r,\theta,\phi)&=\dfrac{Q}{4\pi\epsilon_0r}\cos^2\left(\dfrac{\alpha}{2}\right)+\sum_{l=1}^\infty B_lr^{-l-1}P_l(\cos\theta)
\end{align}$$
Apply the boundary condition again?
$$\begin{align}
\left.\dfrac{\partial\Phi_\text{out}}{\partial r}\right|_{r=R}-\left.\dfrac{\partial\Phi_\text{in}}{\partial r}\right|_{r=R}&=-\dfrac{1}{\epsilon_0}\sigma(\theta,\phi)\\
-\dfrac{Q}{4\pi\epsilon_0R^2}\cos^2\left(\dfrac{\alpha}{2}\right)-\sum_{l=1}^\infty A_lR^{2l+1}(l+1)R^{-l-2}P_l(\cos\theta)-\sum_{l=1}^\infty lA_lR^{l-1}P_l(\cos\theta)&=\\
\dfrac{Q}{4\pi\epsilon_0R^2}\cos^2\left(\dfrac{\alpha}{2}\right)+\sum_{l=1}^\infty A_l\left(R^{2l+1}(l+1)R^{-l-2}+lR^{l-1}\right)P_l(\cos\theta)&=\dfrac{1}{\epsilon_0}\sigma(\theta,\phi)\\
\dfrac{Q}{4\pi R^2}\cos^2\left(\dfrac{\alpha}{2}\right)+\epsilon_0\sum_{l=1}^\infty \left(2l+1\right)A_lR^{l-1}P_l(\cos\theta)&=\sigma(\theta,\phi)
\end{align}$$
If I exploit the orthonormality condition, I can do the following:
$$\begin{align}
\sigma(\theta,\phi)&=
\dfrac{Q}{4\pi R^2}\cos^2\left(\dfrac{\alpha}{2}\right)+\epsilon_0\sum_{l=1}^\infty \left(2l+1\right)A_lR^{l-1}P_l(\cos\theta)\\
\int_0^\pi\sigma(\theta,\phi)P_{l'}(\cos\theta)\sin\theta\ d\theta&=
\int_0^\pi\left[\epsilon_0\sum_{l=1}^\infty \left(2l+1\right)A_lR^{l-1}P_l(\cos\theta)\right]P_{l'}(\cos\theta)\sin\theta\ d\theta\\
\int_0^\pi\sigma(\theta,\phi)P_{l}(\cos\theta)\sin\theta\ d\theta&=\epsilon_0\left(2l+1\right)A_lR^{l-1}\\
A_l&=\dfrac{1}{\epsilon_0\left(2l+1\right)R^{l-1}}\int_0^\pi\sigma(\theta,\phi)P_{l}(\cos\theta)\sin\theta\ d\theta
\end{align}$$
Using our expression for $\sigma$:
$$\begin{align}
A_l&=\dfrac{1}{\epsilon_0\left(2l+1\right)R^{l-1}}\int_0^\pi\sigma(\theta,\phi)P_{l}(\cos\theta)\sin\theta\ d\theta\\
&=\dfrac{1}{\epsilon_0\left(2l+1\right)R^{l-1}}\dfrac{Q}{4\pi R^2}\int_\alpha^\pi P_{l}(\cos\theta)\sin\theta\ d\theta\\
&=\dfrac{1}{\epsilon_0\left(2l+1\right)R^{l-1}}\dfrac{Q}{4\pi R^2}\int_{-1}^{\cos\alpha} P_{l}(x)\ dx\\
\end{align}$$








$$\begin{align}
\Phi&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{1}{2l+1}\left[P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right]\dfrac{r^l}{R^{l+1}}P_{l}(\cos\theta)
\end{align}$$









### Question 3.2.B
Find the magnitude and the direction of the electric field at the origin.


### Question 3.2.C
Discuss the limiting forms of the potential (part A) and the electric field (part B)...

#### Question 3.2.C.I
As the spherical cap becomes very small

#### Question 3.2.C.II
As the spherical cap becomes so large that the area with the charge on it becomes a very small cap at the south pole.



---