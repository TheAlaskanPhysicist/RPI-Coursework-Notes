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

The general equation for the (homogenous) Laplacian in cylindrical coordinates is:
$$\begin{align}
\Phi(\rho,\phi,z)&=\sum_{m=-\infty}^\infty\int_{0}^\infty\left(A_{km}J_m(k\rho)+B_{km}Y_m(k\rho)\right)\left(A_k' e^{-kz}+B_k' e^{kz}\right)\left(A_m'' e^{-im\phi}+B_m'' e^{im\phi}\right)\ dk
\end{align}$$
However, since our system is convenient, we can simplify this expression.

The system is independent of $\phi$, and thus $m=0$ and becomes a constant scale factor:
$$\begin{align}
\Phi(\rho,\phi,z)&=\text{const.}\int_{0}^\infty\left(A_{k0}J_0(k\rho)+B_{k0}Y_0(k\rho)\right)\left(A_k' e^{-kz}+B_k' e^{kz}\right)\ dk
\end{align}$$
Our system is in the region $z\ge0$, so $B_k'=0$ for finite solutions:
$$\begin{align}
\Phi(\rho,\phi,z)&=\text{const.}\int_{0}^\infty \left(A_{k0}J_0(k\rho)+B_{k0}Y_0(k\rho)\right)\cdot A_k'e^{-kz}\ dk
\end{align}$$
Lastly, since there is no singular at $\rho=0$, the Bessel Function of the second kind is unneeded:
$$\begin{align}
\Phi(\rho,\phi,z)&=\text{const.}\int_{0}^\infty (A_{k0}A_k')J_0(k\rho)e^{-kz}\ dk
\end{align}$$
Lastly, we just combine both of these $A$ and the constant factors into a new function $A(k)$:
$$\begin{align}
\Aboxed{\Phi(\rho,\phi,z)&=\int_{0}^\infty A(k)J_0(k\rho)e^{-kz}\ dk}
\end{align}$$
Our boundary condition lies within a circle of radius $a$ on $z=0$, so we know that:
$$\begin{align}
\int_{0}^\infty A(k)J_0(k\rho)\ dk=\begin{cases}V&\rho\le a\\0&\rho>a\end{cases}
\end{align}$$
I had to go find documentation on the inverse of this function:
$$\begin{align}
A(k)&=\int_{0}^\infty k\rho\left\{\begin{array}{}V&\rho\le a\\0&\rho>a\end{array}\right\}J_0(\rho k)\ d\rho\\
&=\int_{0}^a k\rho VJ_0(\rho k)\ d\rho+\int_{a}^\infty k\rho\cdot0\cdot J_0(\rho k)\ d\rho\\
A(k)&=kV\int_{0}^a \rho J_0(\rho k)\ d\rho\\
\Aboxed{A(k)&=\dfrac{V}{k}\int_{0}^{ka} x J_0(x)\ dx}
\end{align}$$
Using the definition of $J_\alpha(x)$:
$$\begin{align}
J_\alpha(x)&=\sum_{m=0}^\infty\dfrac{(-1)^m}{m!\Gamma(m+\alpha+1)}\left(\dfrac{x}{2}\right)^{2m+\alpha}\\
J_0(x)&=\sum_{m=0}^\infty\dfrac{\left(-1/4\right)^{m}}{(m!)^2}x^{2m}\\
\end{align}$$
We can write this in the form of $A(k)$ so that:
$$\begin{align}
\dfrac{V}{k}\int_{0}^{ka}xJ_0(x)\ dx&=\dfrac{V}{k}\sum_{m=0}^\infty\int_{0}^{ka}\dfrac{\left(-1/4\right)^{m}}{(m!)^2}x^{2m+1}\ dx\\
&=\dfrac{V}{k}\sum_{m=0}^\infty\dfrac{\left(-1/4\right)^{m}}{(m!)^2(2m+2)}\left.x^{2m+2}\right|_{0}^{ka}\\
A(k)&=V\dfrac{1}{2k}\sum_{m=0}^\infty\dfrac{\left(-1/4\right)^{m}}{m!(m+1)!}(ka)^{2m+2}\\
\end{align}$$
With a bit of rearrangement, we can see that the $J_{1}(x)$ function looks similar:
$$\begin{align}
J_1(ka)&=\sum_{m=0}^\infty\dfrac{(-1)^m}{m!\Gamma(m+1+1)}\left(\dfrac{ka}{2}\right)^{2m+1}\\
aJ_1(ka)&=\dfrac{1}{2k}\sum_{m=0}^\infty\dfrac{(-1/4)^m}{m!(m+1)!}\left(ka\right)^{2m+2}
\end{align}$$
Substituting, we get:
$$\begin{align}
A(k)&=V\dfrac{1}{2k}\sum_{m=0}^\infty\dfrac{\left(-1/4\right)^{m}}{m!(m+1)!}(ka)^{2m+2}\\
\Aboxed{A(k)&=VaJ_1(ka)}
\end{align}$$
Thus, the final potential equation for this system takes the form:
$$\begin{align}
\Aboxed{\Phi(\rho,\phi,z)&=Va\int_{0}^\infty J_1(ka)J_0(k\rho)e^{-kz}\ dk}
\end{align}$$











### Question 2.7.C
Show that, along the axis of the circle ($\rho=0$), the potential is given by:
$$\begin{align}
\Phi&=V\left(1-\dfrac{z}{\sqrt{a^2+z^2}}\right)
\end{align}$$


### Question 2.7.D
Show that at large distances $\rho^2+z^2\gg a^2$, the potential can be expanded in a power series in $(\rho^2+z^2)^{-1}$, and that the leading terms are:
$$\begin{align}
\Phi&=\dfrac{Va^2}{2}\dfrac{z}{(\rho^2+z^2)^{3/2}}\left[1-\dfrac{3a^2}{4(\rho^2+z^2)}+\dfrac{5(3\rho^2a^2+a^4)}{8(\rho^2+z^2)^2}+\dots\right]
\end{align}$$
Verify that the result of parts C and D are consistent with each-other in their common range of validity.



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
For the region $r\in[a,b]$, we expect the solution to be of the form:
$$\begin{align}
\Phi(r,\theta)&=\sum_{l=0}^\infty\left(A_lr^l+B_lr^{-l-1}\right)P_l(\cos\theta)
\end{align}$$
The boundary conditions then become:
$$\begin{align}
A_la^l+B_la^{-l-1}&=c_l^{r=a} & A_lb^l+B_lb^{-l-1}&=c_l^{r=b}
\end{align}$$
This becomes a system of equations we can invert:
$$\begin{align}
\begin{bmatrix}a^l&a^{-l-1}\\b^l&b^{-l-1}\end{bmatrix}\begin{bmatrix}A_l\\B_l\end{bmatrix}&=\begin{bmatrix}c_l^{r=a}\\c_l^{r=b}\end{bmatrix} &\implies&&
\dfrac{1}{a^{2l+1}-b^{2l+1}}\begin{bmatrix}a^{l+1}&-b^{l+1}\\-a^{l+1}b^{2l+1}&a^{2l+1}b^{l+1}\end{bmatrix}\begin{bmatrix}c_l^{r=a}\\c_l^{r=b}\end{bmatrix}&=\begin{bmatrix}A_l\\B_l\end{bmatrix}
\end{align}$$
More explicitly, we get:
$$\begin{align}
\Aboxed{A_l&=\dfrac{a^{l+1}c_l^{r=a}-b^{l+1}c_l^{r=b}}{a^{2l+1}-b^{2l+1}}} & \Aboxed{B_l&=\dfrac{-a^{l+1}b^{2l+1}c_l^{r=a}+a^{2l+1}b^{l+1}c_l^{r=b}}{a^{2l+1}-b^{2l+1}}}
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
$$\begin{align}
c_0^{r=b}&=V\dfrac{1}{2}\int_{-1}^0 \left(1\right)\ dx &
c_0^{r=b}&=\dfrac{1}{2}V\\
c_1^{r=b}&=V\dfrac{3}{2}\int_{-1}^0 \left(x\right)\ dx &
c_1^{r=b}&=-\dfrac{3}{4}V\\
c_2^{r=b}&=V\dfrac{5}{2}\int_{-1}^0 \dfrac{1}{2}\left(3x^2-1\right)\ dx &
c_2^{r=b}&=0\\
c_3^{r=b}&=V\dfrac{7}{2}\int_{-1}^0 \dfrac{1}{2}\left(5x^3-3x\right)\ dx &
c_3^{r=b}&=\dfrac{7}{16}V\\
c_4^{r=b}&=V\dfrac{9}{2}\int_{-1}^0 \dfrac{1}{8}\left(35x^4-30x^2+3\right)\ dx &
c_4^{r=b}&=0
\end{align}$$
We can then substitute this in for $A_l$ and $B_l$:
$$\begin{align}
A_0&=\dfrac{1}{2}V & 
B_0&=0\\
A_1&=+\dfrac{3}{4}\dfrac{a^{2}+b^{2}}{a^{3}-b^{3}}V & 
B_1&=-\dfrac{3}{4}\dfrac{a^{2}b^{3}+a^{3}b^{2}}{a^{3}-b^{3}}V\\
A_2&=0 & 
B_2&=0\\
A_3&=-\dfrac{7}{16}\dfrac{a^{4}+b^{4}}{a^{7}-b^{7}}V & 
B_3&=+\dfrac{7}{16}\dfrac{a^{4}b^{7}+a^{7}b^{4}}{a^{7}-b^{7}}V\\
A_4&=0 & 
B_4&=0\\
\end{align}$$
Taking a guess at the form of this equation, I'd conjecture:
$$\begin{align}
A_{k}&=(-1)^{k-1}V\dfrac{4k-1}{2}\dfrac{a^{2k}+b^{2k}}{a^{4k-1}-b^{4k-1}}\\
B_{k}&=(-1)^{k}V\dfrac{4k-1}{2}\dfrac{a^{2k}b^{4k-1}+a^{4k-1}b^{2k}}{a^{4k-1}-b^{4k-1}}\\
\Phi(r,\theta)&=\dfrac{1}{2}V+\sum_{k=1}^\infty\left(A_kr^{2k-1}+B_kr^{-2k}\right)P_l(\cos\theta)\\
\Aboxed{\Phi(r,\theta)&=\dfrac{1}{2}V+V\sum_{k=1}^\infty(-1)^{k}\dfrac{4k-1}{2}\left(\dfrac{a^{2k}b^{4k-1}+a^{4k-1}b^{2k}}{a^{4k-1}-b^{4k-1}}r^{-2k}-\dfrac{a^{2k}+b^{2k}}{a^{4k-1}-b^{4k-1}}r^{2k-1}\right)P_{2k-1}(\cos\theta)}
\end{align}$$
However, for terms up until $l=4$, we have:
$$\begin{align}
\Phi(r,\theta)&\approx\dfrac{1}{2}V+\dfrac{3}{4}V\left(\dfrac{a^{2}+b^{2}}{a^{3}-b^{3}}r-\dfrac{a^{2}b^{3}+a^{3}b^{2}}{a^{3}-b^{3}}r^{-2}\right)\cos\theta\\
&-\dfrac{7}{16}V\left(\dfrac{a^{4}+b^{4}}{a^{7}-b^{7}}r^3-\dfrac{a^{4}b^{7}+a^{7}b^{4}}{a^{7}-b^{7}} r^{-4}\right)\dfrac{(5\cos^3\theta-3\cos\theta)}{2}
\end{align}$$
I'm not sure this is the right answer because there were plenty of places I could have made mistakes, but the general form should looks somewhat like this.
### Limiting Cases
In the limit as $b\rightarrow\infty$, we see that:
$$\begin{align}
\lim_{b\rightarrow\infty}\Phi(r,\theta)&\approx\dfrac{1}{2}V+\dfrac{3}{4}V\dfrac{a^{4}}{r^2}\cos\theta-\dfrac{7}{16}V\dfrac{a^{4}}{r^4}\dfrac{(5\cos^3\theta-3\cos\theta)}{2}
\end{align}$$
In the limit as $a\rightarrow0$, we see that:
$$\begin{align}
\lim_{a\rightarrow0}\Phi(r,\theta)&\approx\dfrac{1}{2}V-\dfrac{3}{4}V\dfrac{r}{b}\cos\theta+\dfrac{7}{16}V\dfrac{r^3}{b^{3}}\dfrac{(5\cos^3\theta-3\cos\theta)}{2}
\end{align}$$
I had to look up the equations for the solutions of these limit cases, but they do seem to match.

---
## Question 3.2
A spherical surface of radius $R$ has charge uniformly distributed over its surface with a density $Q/4\pi R^2$, except for a spherical cap at the north pole, defined by the cone $\theta=\alpha$.


### Question 3.2.A
Show that the potential inside the spherical surface can be expressed as:
$$\begin{align}
\Phi&=\dfrac{Q}{8\pi\epsilon_0}\sum_{l=0}^\infty\dfrac{1}{2l+1}\left[P_{l+1}(\cos\alpha)-P_{l-1}(\cos\alpha)\right]\dfrac{r^l}{R^{l+1}}P_{l}(\cos\theta)
\end{align}$$
where, for $l=0$, $P_{l-1}(\cos\alpha)=-1$. What is the potential outside?

### Question 3.2.B
Find the magnitude and the direction of the electric field at the origin.


### Question 3.2.C
Discuss the limiting forms of the potential (part A) and the electric field (part B)...

#### Question 3.2.C.I
As the spherical cap becomes very small

#### Question 3.2.C.II
As the spherical cap becomes so large that the area with the charge on it becomes a very small cap at the south pole.



---