Author: Stanley Goodwin
Date: February 12th, 2026

---
## Question 3.10
For the cylinder in Problem 3.9, the cylindrical surface is made of two equal half-cylinders, one at potential $V$ and the other at potential $-V$, so that:
$$\begin{align}
\Phi(\rho=b,\phi,z)&=\begin{cases}
+V,&-\tfrac{\pi}{2}<\phi<+\tfrac{\pi}{2}\\
-V,&+\tfrac{\pi}{2}<\phi<+\tfrac{3\pi}{2}
\end{cases}\\
\Phi(\rho,\phi,z\in\{0,L\})&=0
\end{align}$$
Where the cylinder is $\rho\in[0,b)$, $z\in(0,L)$.

---
### Question 3.10.A
Find the potential inside the cylinder.

Start with the general solution coefficients of the Laplace equation:
$$\begin{align}
\Phi_{km}(\rho,\phi,z)&=\left(A_{km}J_m(k\rho)+B_{km}Y_m(k\rho)\right)\left(C_m\sin(m\phi)+D_m\cos(m\phi)\right)\left(E_k\sin(kz)+F_k\cos(kz)\right)
\end{align}$$
Some observations and consequences:
$$\begin{align}
\Phi_{km}(\rho,\phi,z=0)&=0 &\implies && F_k&=0 && \text{Boundary Potential}\\
\Phi_{km}(\rho,\phi,z=L)&=0 &\implies && kL&=n\pi && \text{Boundary Potential}\\
\Phi_{km}(\rho=b,\phi,z)&=\Phi_{km}(\rho=b,-\phi,z) &\implies && C_{km}&=0 && \text{Boundary Potential}\\
\Phi_{km}(\rho<b,\phi,z)&\ne\infty &\implies && B_{km}&=0 && \text{No Singularies Inside}
\end{align}$$
Imposing these new conditions, each component of the Laplace equation reduces to:
$$\begin{align}
\Phi_{nm}(\rho,\phi,z)&=A_{nm}J_m\left(\tfrac{n\pi}{L}\rho\right)\cdot D_m\cos(m\phi)\cdot E_n\sin\left(\tfrac{n\pi}{L}z\right)
\end{align}$$
Define a new coefficient $A'_{nm}$, and solve for it using the $\rho=b$ boundary condition:
$$\begin{align}
\Phi(b,\phi,z)&=\sum_{n=1}^\infty\sum_{m=0}^\infty A'_{nm}J_m\left(\tfrac{n\pi}{L}b\right)\cos(m\phi)\sin\left(\tfrac{n\pi}{L}z\right)
\end{align}$$
<div style="page-break-before: always;"></div>

I saw a neat trick for expressing the potential, since it is effectively the $\operatorname{sign}\left(\cos\phi\right)$ function:
$$\begin{align}
\operatorname{sign}\left(\cos\theta\right)&=\dfrac{4}{\pi}\sum_{m=1}^\text{odd}\dfrac{(-1)^{\tfrac{m-1}{2}}}{m}\cos\left(m\phi\right)
\end{align}$$
The potential is just $V$ times this function, thus we can equate both sides:
$$\begin{align}
\sum_{n=1}^\infty\sum_{m=0}^\infty A'_{nm}J_m\left(\tfrac{n\pi}{L}b\right)\cos(m\phi)\sin\left(\tfrac{n\pi}{L}z\right)&=\dfrac{4V}{\pi}\sum_{m=1}^\text{odd}\dfrac{(-1)^{\tfrac{m-1}{2}}}{m}\cos\left(m\phi\right)
\end{align}$$
Since cosines over a full period form an orthogonal basis, non-zero terms for $m$ are odd:
$$\begin{align}
\sum_{n=1}^\infty A'_{nm}J_m\left(\tfrac{n\pi}{L}b\right)\sin\left(\tfrac{n\pi}{L}z\right)&=\dfrac{4V}{m\pi}(-1)^{\tfrac{m-1}{2}} & m\text{ odd}
\end{align}$$
Another trick is a constant can also be expressed in terms of sine waves:
$$\begin{align}
1&=\dfrac{4}{\pi}\sum_{n=1}^\text{odd}\dfrac{1}{n}\sin\left(\tfrac{n\pi}{L}z\right) & 0<z<L
\end{align}$$
Similar to above, we equate both sides again:
$$\begin{align}
\sum_{n=1}^\infty A'_{nm}J_m\left(\tfrac{n\pi}{L}b\right)\sin\left(\tfrac{n\pi}{L}z\right)&=\dfrac{4V}{m\pi}(-1)^{\tfrac{m-1}{2}}\dfrac{4}{\pi}\sum_{n=1}^\text{odd}\dfrac{1}{n}\sin\left(\tfrac{n\pi}{L}z\right) & m\text{ odd}
\end{align}$$
The sine also form a full period over an orthogonal basis, non-zero terms for $n$ are odd:
$$\begin{align}
A'_{nm}J_m\left(\tfrac{n\pi}{L}b\right)&=\dfrac{4V}{m\pi}(-1)^{\tfrac{m-1}{2}}\dfrac{4}{\pi}\dfrac{1}{n} & m,n\text{ odd}
\end{align}$$
Rearranging, the coefficient is then:
$$\begin{align}
A'_{nm}&=\dfrac{16V}{mn\pi^2}\dfrac{(-1)^{\tfrac{m-1}{2}}}{J_m\left(\tfrac{n\pi}{L}b\right)} & m,n\text{ odd}
\end{align}$$
Substituting back to find the potential for the inside of the cylinder, we get:
$$\begin{align}
\Aboxed{\Phi_\text{inside}(\rho,\phi,z)&=\dfrac{16V}{\pi^2}\sum_{n=1}^\text{odd}\sum_{m=1}^\text{odd}\dfrac{(-1)^{\tfrac{m-1}{2}}}{mn}\dfrac{J_m\left(\tfrac{n\pi}{L}\rho\right)}{J_m\left(\tfrac{n\pi}{L}b\right)}\cos(m\phi)\sin\left(\tfrac{n\pi}{L}z\right)}
\end{align}$$
<div style="page-break-before: always;"></div>

### Question 3.10.B
Assuming $L\gg b$, consider the potential at $z=\tfrac{L}{2}$ as a function of $\rho$ and $\phi$, and compare it with the two-dimensional Problem 2.13.

We want to consider the limit process $\rho,b\ll L$, the super long and skinny cylinder:
$$\begin{align}
\lim_{\rho,b\ll L}\Phi_\text{inside}(\rho,\phi,z)
&=\dfrac{16V}{\pi^2}\sum_{n=1}^\text{odd}\sum_{m=1}^\text{odd}\dfrac{(-1)^{\tfrac{m-1}{2}}}{mn}\lim_{\rho,b\ll L}\left(\dfrac{J_m\left(\tfrac{n\pi}{L}\rho\right)}{J_m\left(\tfrac{n\pi}{L}b\right)}\right)\cos(m\phi)\sin\left(\tfrac{n\pi}{L}z\right)
\end{align}$$
The Bessel functions about $0$ have the behavior of:
$$\begin{align}
J_m\left(\tfrac{n\pi}{L}\rho\right)&=\dfrac{1}{m!}\left(\dfrac{n\pi}{L}\dfrac{\rho}{2}\right)^m & J_m\left(\tfrac{n\pi}{L}b\right)&=\dfrac{1}{m!}\left(\dfrac{n\pi}{L}\dfrac{b}{2}\right)^m
\end{align}$$
Substituting back in, and simplifying the ratio, the potential becomes:
$$\begin{align}
\lim_{\rho,b\ll L}\Phi_\text{inside}(\rho,\phi,z)
&=\dfrac{16V}{\pi^2}\sum_{n=1}^\text{odd}\sum_{m=1}^\text{odd}\dfrac{(-1)^{\tfrac{m-1}{2}}}{mn}\left(\dfrac{\rho}{b}\right)^m\cos(m\phi)\sin\left(\tfrac{n\pi}{L}z\right)
\end{align}$$
To simplify further, when $z=L/2$, $\sin\left(\tfrac{n\pi}{2}\right)\rightarrow(-1)^{\tfrac{n-1}{2}}$ for odd $n$ and $0$ otherwise:
$$\begin{align}
\lim_{\rho,b\ll L}\Phi_\text{inside}\left(\rho,\phi,\tfrac{L}{2}\right)
&=\dfrac{16V}{\pi^2}\sum_{n=1}^\text{odd}\sum_{m=1}^\text{odd}\dfrac{(-1)^{\tfrac{m-1}{2}}}{mn}\left(\dfrac{\rho}{b}\right)^m\cos(m\phi)\cdot(-1)^{\tfrac{n-1}{2}}
\end{align}$$
We can split this equation in terms of $n$ and $m$:
$$\begin{align}
\lim_{\rho,b\ll L}\Phi_\text{inside}\left(\rho,\phi,\tfrac{L}{2}\right)
&=\dfrac{16V}{\pi^2}\sum_{m=1}^\text{odd}\dfrac{(-1)^{\tfrac{m-1}{2}}}{m}\left(\dfrac{\rho}{b}\right)^m\cos(m\phi)\cdot\sum_{n=1}^\text{odd}\dfrac{(-1)^{\tfrac{n-1}{2}}}{n}
\end{align}$$
If we reindex $m\to 2k+1$, we see this is just the inverse tangent:
$$\begin{align}
\sum_{m=1}^\text{odd}(-1)^{\tfrac{m-1}{2}}\dfrac{x^m}{m}=\sum_{k=0}^\infty(-1)^{k}\dfrac{x^{2k+1}}{2k+1}&=\tan^{-1}(x)\\
\end{align}$$
If we use that $\mathrm{Re}\left(e^{im\phi}\right)=\cos\left(m\phi\right)$, we can pull the exponential into the power, and so:
$$\begin{align}
\lim_{\rho,b\ll L}\Phi_\text{inside}\left(\rho,\phi,\tfrac{L}{2}\right)
&=\dfrac{16V}{\pi^2}\mathrm{Re}\sum_{m=1}^\text{odd}\dfrac{(-1)^{\tfrac{m-1}{2}}}{m}\left(\dfrac{\rho}{b}e^{i\phi}\right)^m\cdot\sum_{n=1}^\text{odd}\dfrac{(-1)^{\tfrac{n-1}{2}}}{n}\\
&=\dfrac{16V}{\pi^2}\mathrm{Re}\left[\tan^{-1}\left(\dfrac{\rho}{b}e^{i\phi}\right)\cdot\tan^{-1}\left(1\right)\right]\\
\Aboxed{\lim_{\rho,b\ll L}\Phi_\text{inside}\left(\rho,\phi,\tfrac{L}{2}\right)&=\dfrac{4V}{\pi}\mathrm{Re}\left[\tan^{-1}\left(\dfrac{\rho}{b}e^{i\phi}\right)\right]}
\end{align}$$
<div style="page-break-before: always;"></div>

This is as far as I got, and I required looking up a particular relation to find the real component:
$$\begin{align}
\mathrm{Re}\left[\tan^{-1}\left(re^{i\phi}\right)\right]&=\dfrac{1}{2}\tan^{-1}\left(\dfrac{2r\cos\phi}{1-r^2}\right)
\end{align}$$
If we now substitute this into our equation, we get something that looks like Problem 2.13:
$$\begin{align}
\Aboxed{\lim_{\rho,b\ll L}\Phi_\text{inside}\left(\rho,\phi,\tfrac{L}{2}\right)&=\dfrac{2V}{\pi}\tan^{-1}\left(\dfrac{2b\rho}{b^2-\rho^2}\cos\phi\right)}
\end{align}$$
Problem 2.13 has the solution:
$$\begin{align}
\Phi\left(\rho,\phi\right)&=\dfrac{V_1+V_2}{2}+\dfrac{V_1-V_2}{\pi}\tan^{-1}\left(\dfrac{2b\rho}{b^2-\rho^2}\cos\phi\right)
\end{align}$$
This is identical since our problem uses $V_1=V$ and $V_2=-V$.

---
## Question 3.14
A line charge of length $2d$ with a total charge $Q$ has a linear charge density varying as $(d^2-z^2)$, where $z$ is the distance from the midpoint. A grounded, conducting, spherical shell of inner radius $b>d$ is centered at the midpoint of the line charge.

For usage later, the charge density should take something like the following form:
$$\begin{align}
\rho(\vec{r})&=\dfrac{A}{2\pi r^2}\left(d^2-r^2\right)\dfrac{\delta\left(\cos\theta-1\right)+\delta\left(\cos\theta+1\right)}{2} & 0\le r<d
\end{align}$$
Since the $z$-axis is when $\left|\cos\theta\right|=1$, for $0\le r\le d$, a factor of $2\pi$ from $\phi$, and $1/r^2$ for the Jacobian.

If we integrate this over the whole the whole volume, where the density is $0$ outside $r=d$, then:
$$\begin{align}
Q&=\int_0^{2\pi}\int_0^\pi\int_0^d\dfrac{A}{2\pi r^2}\left(d^2-r^2\right)\left(d^2-r^2\right)\dfrac{\delta\left(\cos\theta-1\right)+\delta\left(\cos\theta+1\right)}{2}\ r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=\dfrac{A}{2\pi}\int_0^d\left(d^2-r^2\right)\ dr\int_0^\pi\dfrac{\delta\left(\cos\theta-1\right)+\delta\left(\cos\theta+1\right)}{2}\ d\theta\int_0^{2\pi}d\phi=\dfrac{A}{2\pi}\left[rd^2-\dfrac{r^3}{3}\right|_0^d\cdot1\cdot2\pi\\
Q&=\dfrac{2d^3}{3}A
\end{align}$$
This renormalizes the charge density to be:
$$\begin{align}
\Aboxed{\rho(\vec{r})&=\dfrac{3Q}{4\pi d^3}\left(\dfrac{d^2}{r^2}-1\right)\dfrac{\delta\left(\cos\theta-1\right)+\delta\left(\cos\theta+1\right)}{2}} & 0\le r<d
\end{align}$$
<div style="page-break-before: always;"></div>

### Question 3.14.A
Find the potential everywhere inside the spherical shell as an expansion of Legendre polynomials.

The Green's function that vanishes at the boundary of a sphere is Equation 2.16 with $a\to b$:
$$\begin{align}
G(\vec{r},\vec{r}')&=\dfrac{1}{|\vec{r}-\vec{r}'|}-\dfrac{b}{r'\left|\vec{r}-\tfrac{b^2}{r'^2}\vec{r}'\right|}
\end{align}$$
The potential with the boundary conditions is then:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{1}{4\pi\epsilon_0}\int\rho(\vec{r}')G(\vec{r},\vec{r}')\ d^3r'
\end{align}$$
Substituting the charge distribution, we get that:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{3Q}{4\pi d^3}\left(d^2-r'^2\right)\dfrac{\delta\left(\cos\theta-1\right)+\delta\left(\cos\theta+1\right)}{2}\sin\theta'\ G(r,\theta,\phi;r,\theta',\phi')\ dr'\ d\theta'\ d\phi'\\
&=\dfrac{3Q}{16\pi\epsilon_0d^3}\int_0^d\left(d^2-r'^2\right)\left[G(\theta'=0)+G(\theta'=\pi)\right]\ dr'\\
\end{align}$$
We can expand the Green's function as a series:
$$\begin{align}
G(\vec{r},\vec{r}')&=4\pi\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{1}{2l+1}\left[\dfrac{r_<^l}{r_>^{l+1}}-\dfrac{(rr')^l}{b^{2l+1}}\right]Y_{lm}^*(\theta',\phi')Y_{lm}(\theta,\phi)
\end{align}$$
There is Azimuthal symmetry so we can set $m=0$:
$$\begin{align}
G(\vec{r},\vec{r}')&=\sum_{l=0}^\infty\left[\dfrac{r_<^l}{r_>^{l+1}}-\dfrac{(rr')^l}{b^{2l+1}}\right]P_{l}^*(\cos\theta')P_{l}(\cos\theta)
\end{align}$$
We can substitute in the 2 polar angles we have, $\theta=0$ and $\theta=\pi$, which becomes:
$$\begin{align}
G(\theta'=0)&=\sum_{l=0}^\infty\left[\dfrac{r_<^l}{r_>^{l+1}}-\dfrac{(rr')^l}{b^{2l+1}}\right]P_{l}(\cos\theta) & 
G(\theta'=\pi)&=\sum_{l=0}^\infty\left[\dfrac{r_<^l}{r_>^{l+1}}-\dfrac{(rr')^l}{b^{2l+1}}\right](-1)^lP_{l}(\cos\theta)
\end{align}$$
Back to the potential, these simplify to:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{3Q}{16\pi\epsilon_0d^3}\int_0^d\left(d^2-r'^2\right)\sum_{l=0}^\infty\left[\dfrac{r_<^l}{r_>^{l+1}}-\dfrac{(rr')^l}{b^{2l+1}}\right]P_{l}(\cos\theta)\left[1+(-1)^l\right]\ dr'\\
\Aboxed{\Phi(\vec{r})&=\dfrac{3Q}{8\pi\epsilon_0d^3}\sum_{l=0}^\text{even}P_{l}(\cos\theta)\int_0^d\left(d^2-r'^2\right)\left[\dfrac{r_<^l}{r_>^{l+1}}-\dfrac{(rr')^l}{b^{2l+1}}\right]\ dr'}
\end{align}$$
<div style="page-break-before: always;"></div>

If $r>d$, the potential becomes:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{3Q}{8\pi\epsilon_0d^3}\sum_{l=0}^\text{even}P_{l}(\cos\theta)\int_0^d\left(d^2-r'^2\right)\left[\dfrac{r'^l}{r^{l+1}}-\dfrac{(rr')^l}{b^{2l+1}}\right]\ dr'\\
\Aboxed{\Phi(\vec{r})&=\dfrac{3Q}{4\pi\epsilon_0}\sum_{l=0}^\text{even}P_{l}(\cos\theta)\dfrac{d^l}{(l+1)(l+3)b^{l+1}}\left[\left(\dfrac{b}{r}\right)^{l+1}-\left(\dfrac{r}{b}\right)^{l}\right],\ r>d}
\end{align}$$
If $r<d$, the integral breaks into $r'\in(0,r)$ and $r'\in(r,d)$:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{3Q}{8\pi\epsilon_0d^3}\sum_{l=0}^\text{even}P_{l}(\cos\theta)\left(\int_0^r\left(d^2-r'^2\right)\left[\dfrac{r'^l}{r^{l+1}}-\dfrac{(rr')^l}{b^{2l+1}}\right]\ dr'+\int_r^d\left(d^2-r'^2\right)\left[\dfrac{r^l}{r'^{l+1}}-\dfrac{(rr')^l}{b^{2l+1}}\right]\ dr'\right)
\end{align}$$
The two different integral expressions evaluate to the following:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{3Q}{8\pi\epsilon_0d^3}\sum_{l=0}^\text{even}P_{l}(\cos\theta)\left[d^2\dfrac{2l+1}{l(l+1)}-\dfrac{2l+1}{(l-2)(l+3)}r^2\right.\\
&\ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ \ +\left.\left(\dfrac{1}{d^{l+2}}\dfrac{2}{l(l-2)}-\dfrac{d^{l+3}}{b^{2l+1}}\dfrac{2}{(l+1)(l+3)}\right)r^l\right]
\end{align}$$
This was extremely painful... For the sake of writing the final solution:
$$\begin{align}
A_l&=-\dfrac{d^l}{(l+1)(l+3)b^{2l+1}} & B_l&=\dfrac{d^l}{(l+1)(l+3)}\\
C_l&=\dfrac{1}{2d}\dfrac{2l+1}{l(l+1)} & D_l&=-\dfrac{1}{2d^3}\dfrac{2l+1}{(l-2)(l+3)}\\
E_l&=\left(\dfrac{1}{2d^{l+5}}\dfrac{2}{l(l-2)}-\dfrac{d^{l}}{b^{2l+1}}\dfrac{1}{(l+1)(l+3)}\right)
\end{align}$$
The final potential is just then:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{3Q}{4\pi\epsilon_0}\sum_{l=0}^\text{even}\begin{cases}
\left(A_lr^l+B_lr^{-l-1}\right)P_{l}(\cos\theta),& \ r>d\\
\left(E_lr^l+C_l+D_lr^{2}\right)P_{l}(\cos\theta),& \ r<d\\
\end{cases}
\end{align}$$

### Question 3.14.B
Calculate the surface-charge density induced on the shell.

We can use the surface-charge equation, and $\vec{n}=-r\hat{r}$ for the inside charge distribution, then:
$$\begin{align}
\sigma&=-\epsilon_0\left.\dfrac{\partial\Phi}{\partial n}\right|_{r=b}=\epsilon_0\left.\dfrac{\partial\Phi}{\partial r}\right|_{r=b}
\end{align}$$
Since $b>d$, then we use the simpler potential (thank goodness):
$$\begin{align}
\sigma
&=\epsilon_0\left.\dfrac{\partial}{\partial r}\left(\dfrac{3Q}{4\pi\epsilon_0}\sum_{l=0}^\text{even}P_{l}(\cos\theta)\dfrac{d^l}{(l+1)(l+3)b^{l+1}}\left[\left(\dfrac{b}{r}\right)^{l+1}-\left(\dfrac{r}{b}\right)^{l}\right]\right)\right|_{r=b}\end{align}$$
$$\begin{align}&=\dfrac{3Q}{4\pi}\left.\sum_{l=0}^\text{even}P_{l}(\cos\theta)\dfrac{d^l}{(l+1)(l+3)b^{l+1}}\dfrac{\partial}{\partial r}\left[\left(\dfrac{b}{r}\right)^{l+1}-\left(\dfrac{r}{b}\right)^{l}\right]\right|_{r=b}\\
&=\dfrac{3Q}{4\pi}\left.\sum_{l=0}^\text{even}P_{l}(\cos\theta)\dfrac{d^l}{(l+1)(l+3)b^{l+1}}\left[-l\dfrac{b^{l+1}}{r^{l+2}}-(l-1)\dfrac{r^{l-1}}{b^{l}}\right]\right|_{r=b}\\
&=-\dfrac{3Q}{4\pi}\sum_{l=0}^\text{even}P_{l}(\cos\theta)\dfrac{(2l+1)}{(l+1)(l+3)}\dfrac{d^l}{b^{l+2}}\\
\Aboxed{\sigma(\theta,\phi)&=-\dfrac{3Q}{4\pi b^2}\sum_{l=0}^\text{even}\dfrac{(2l+1)}{(l+1)(l+3)}\left(\dfrac{d}{b}\right)^lP_{l}(\cos\theta)}
\end{align}$$
---
### Question 3.14.C
Discuss your answers to parts A and B in the limit that $d\ll b$.

In the limit of $\tfrac{d}{b}\ll1$, we can apply this to the potential:
$$\begin{align}
\lim_{d\ll b}\Phi(\vec{r})
&=\lim_{d\ll b}\dfrac{3Q}{4\pi\epsilon_0b}\sum_{l=0}^\text{even}P_{l}(\cos\theta)\dfrac{1}{(l+1)(l+3)}\dfrac{d^l}{b^{l}}\left[\left(\dfrac{b}{r}\right)^{l+1}-\left(\dfrac{r}{b}\right)^{l}\right]\\
&=\dfrac{3Q}{4\pi\epsilon_0b}P_{0}(\cos\theta)\dfrac{1}{(0+1)(0+3)}\left[\left(\dfrac{b}{r}\right)^{0+1}-\left(\dfrac{r}{b}\right)^{0}\right]+0+0+\dots\\
&=\dfrac{3Q}{4\pi\epsilon_0b}\dfrac{1}{3}\left[\dfrac{b}{r}-1\right]P_{0}(\cos\theta)\\
\Aboxed{\lim_{d\ll b}\Phi(\vec{r})&=\dfrac{Q}{4\pi\epsilon_0}\left[\dfrac{1}{r}-\dfrac{1}{b}\right]}
\end{align}$$
This is exactly what we would expect for the potential of a point charge in the center of a sphere.

For the charge density:
$$\begin{align}
\lim_{d\ll b}\sigma(\theta,\phi)
&=\lim_{d\ll b}-\dfrac{3Q}{4\pi b^2}\sum_{l=0}^\text{even}\dfrac{(2l+1)}{(l+1)(l+3)}\left(\dfrac{d}{b}\right)^lP_{l}(\cos\theta)\\
&=-\dfrac{3Q}{4\pi b^2}\dfrac{(2\cdot0+1)}{(0+1)(0+3)}P_{0}(\cos\theta)+0+0+\dots\\
&=-\dfrac{3Q}{4\pi b^2}\dfrac{1}{3}\\
\Aboxed{\lim_{d\ll b}\sigma(\theta,\phi)&=-\dfrac{Q}{4\pi b^2}}
\end{align}$$
This is exactly a uniform distribution of conjugate charge $-Q$ over the surface of the sphere.
<div style="page-break-before: always;"></div>

## Question 4.1
### Question 4.1.A
Calculate the multipole moments $q_{lm}$ for figure A.

Our charge density can be written in terms of delta functions in spherical coordinates:
$$\begin{align}
\rho(\vec{r})&=\dfrac{q}{r^2}\delta(r-a)\delta(\cos\theta)\left[\delta(\phi)+\delta(\phi-\tfrac{\pi}{2})-\delta(\phi-\pi)-\delta(\phi-\tfrac{3\pi}{2})\right]
\end{align}$$
Our density picks out specific $(r,\theta,\phi)$ values when the integral for $q_{lm}$ is generated:
$$\begin{align}
q_{lm}&=\int Y_{lm}^*(\theta,\phi)r^l\rho(\vec{r})\ d^3r
\end{align}$$
All of our radii are $r=a$, polar angle $\theta=\tfrac{\pi}{2}$, with 4 different values for $\phi$:
$$\begin{align}
q_{lm}&=qa^{l}\sin\tfrac{\pi}{2}Y_{lm}^*(\tfrac{\pi}{2},0)+qa^{l}\sin\tfrac{\pi}{2}Y_{lm}^*(\tfrac{\pi}{2},\tfrac{\pi}{2})\\
&-qa^{l}\sin\tfrac{\pi}{2}Y_{lm}^*(\tfrac{\pi}{2},\pi)-qa^{l}\sin\tfrac{\pi}{2}Y_{lm}^*(\tfrac{\pi}{2},\tfrac{3\pi}{2})\\\\
q_{lm}&=qa^{l}\left[Y_{lm}^*(\tfrac{\pi}{2},0)+Y_{lm}^*(\tfrac{\pi}{2},\tfrac{\pi}{2})-Y_{lm}^*(\tfrac{\pi}{2},\pi)-Y_{lm}^*(\tfrac{\pi}{2},\tfrac{3\pi}{2})\right]
\end{align}$$
These conjugated spherical harmonics can be written as:
$$\begin{align}
Y_{lm}^*(\theta,\phi)=\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}P^m_l(\cos\theta)e^{-im\phi}
\end{align}$$
All $l,m,\theta$ are equal, and so only the exponential term is unique for each:
$$\begin{align}
q_{lm}&=qa^{l}\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}P^m_l(0)\left(e^{-im0}+e^{-im\tfrac{\pi}{2}}-e^{-im\pi}-e^{-im\tfrac{3\pi}{2}}\right)\\
&=qa^{l}\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}P^m_l(0)\left(1+(-i)^m-(-1)^m-(+i)^m\right)\\
&=qa^{l}\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}P^m_l(0)\left(1-(-1)^m\right)(1-i^m)\\
\Aboxed{q_{lm}&=2qa^{l}\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}P^m_l(0)(1-i^m),\ m\text{ odd, else }0}
\end{align}$$
<div style="page-break-before: always;"></div>

The first 2 non-trivially-zero terms are for $l=1$ and $l=3$:
$$\begin{align}
q_{1m}&=2qa^1\sqrt{\dfrac{2\cdot1+1}{4\pi}\dfrac{(1-m)!}{(1+m)!}}P^m_1(0)(1-i^m)\\
q_{1,-1}&=+qa\sqrt{\dfrac{3}{2\pi}}(1+i) \ \ \ \ \ q_{1,+1}=-qa\sqrt{\dfrac{3}{2\pi}}(1-i)\\\\
q_{3m}&=2qa^{3}\sqrt{\dfrac{2\cdot 3+1}{4\pi}\dfrac{(3-m)!}{(3+m)!}}P^m_3(0)(1-i^m)\\
q_{3,-3}&=+qa^{3}\sqrt{\dfrac{35}{16\pi}}(1-i) \ \ \ \ \ q_{3,-1}=-qa^{3}\sqrt{\dfrac{21}{16\pi}}(1+i)\\
q_{3,+1}&=+qa^{3}\sqrt{\dfrac{21}{16\pi}}(1-i) \ \ \ \ \ q_{3,+3}=-qa^{3}\sqrt{\dfrac{35}{16\pi}}(1+i)\\
\end{align}$$
The terms $a_{0,0},a_{1,0},a_{2,m},a_{3,-2},a_{3,0},a_{3,+2}$ are all zero.

---
### Question 4.1.B
Calculate the multipole moments $q_{lm}$ for figure B.

Our charge density can be written in terms of delta functions in spherical coordinates:
$$\begin{align}
\rho(\vec{r})&=\dfrac{q}{2\pi r^2}\delta(r-a)\left[\delta(\cos\theta-1)+\delta(\cos\theta+1)\right]-\dfrac{2q}{4\pi r^2}\delta(r)
\end{align}$$
Our density picks out specific $(r,\theta,\phi)$ values when the integral for $q_{lm}$ is generated:
$$\begin{align}
q_{lm}&=\int Y_{lm}^*(\theta,\phi)r^l\rho(\vec{r})\ d^3r
\end{align}$$
Using our charge density, we get 2 different integrals:
$$\begin{align}
q_{lm}^1&=+\dfrac{qa^l}{2\pi}\int Y_{lm}^*(\theta,\phi)\left[\delta(\cos\theta-1)+\delta(\cos\theta+1)\right]\sin\theta\ d\theta\ d\phi\\
q_{lm}^2&=-\dfrac{2q}{4\pi}\int Y_{lm}^*(\theta,\phi)r^l\delta(r)\sin\theta\ dr\ d\theta\ d\phi\\
\end{align}$$
<div style="page-break-before: always;"></div>

If we substitute the spherical harmonic equations, we get:
$$\begin{align}
q_{lm}^1&=+\dfrac{qa^l}{2\pi}\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}\int P^m_l(\cos\theta)e^{-im\phi}\left[\delta(\cos\theta-1)+\delta(\cos\theta+1)\right]\sin\theta\ d\theta\ d\phi\\
&=+\dfrac{qa^l}{2\pi}\sqrt{\dfrac{2l+1}{4\pi}}\cdot2\pi\delta_{0m}\cdot\left[P^0_l(1)+(-1)^lP^0_l(1)\right]\\
q_{lm}^1&=+qa^l\sqrt{\dfrac{2l+1}{4\pi}}\left[1+(-1)^l\right]\delta_{0m}\\
\end{align}$$
$$\begin{align}
q_{lm}^2&=-\dfrac{2q}{4\pi}\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}\int P^m_l(\cos\theta)e^{-im\phi} r^l\delta(r)\sin\theta\ d\theta\ d\phi\\
&=-\dfrac{2q}{4\pi}\sqrt{\dfrac{1}{4\pi}}\cdot\delta_{0l}\cdot2\pi\delta_{0m}\int_0^\pi\sin\theta\ d\theta\\
q_{lm}^2&=-q\sqrt{\dfrac{1}{\pi}}\delta_{0l}\delta_{0m}\\
\end{align}$$
Together, we get that the multipole moments are generated by:
$$\begin{align}
\Aboxed{q_{lm}&=+qa^l\sqrt{\dfrac{2l+1}{4\pi}}\left[1+(-1)^l\right]\delta_{0m}-q\sqrt{\dfrac{1}{\pi}}\delta_{0l}\delta_{0m}}
\end{align}$$
The first term accounts for all behavior except for the $l,m=0,0$ case:
$$\begin{align}
q_{lm}&=qa^l\sqrt{\dfrac{2l+1}{\pi}} & m=0\text{ and }l\text{ is even }(l\ne0), && q_{lm}=0\text{ otherwise}
\end{align}$$
Some (non-zero) terms are as follows:
$$\begin{align}
q_{20}&=qa^2\sqrt{\dfrac{5}{\pi}} & q_{40}&=qa^4\sqrt{\dfrac{9}{\pi}} & q_{60}&=qa^6\sqrt{\dfrac{13}{\pi}}
\end{align}$$
All other terms not of this form are $0$ (such as $q_{00},q_{1,-1},q_{1,0},q_{1,+1},\dots)$

---
### Question 4.1.C
For the charge distribution of [[#Question 4.1.B]], write down the multipole expansion for the potential. Keeping only the lowest-order term in the expansion, plot the potential in the $xy$-plane as a function of the distance from the origin for distances greater than $a$.

Start with the general case for multipole expansion:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}q_{lm}r^{-l-1}Y_{lm}(\theta,\phi)
\end{align}$$
Our previous solution for $q_{lm}$ helps reduce our system. Let $l=2k, k\ge1$ and $m=0$:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\sum_{k=1}^\infty\dfrac{4\pi}{4k+1}\cdot qa^{2k}\sqrt{\dfrac{4k+1}{\pi}}\cdot r^{-(2k+1)}Y_{2k,0}(\theta,\phi)\\
\end{align}$$
We can also use the following substitution for the spherical harmonics:
$$\begin{align}
Y_{2k,0}(\theta,\phi)=\sqrt{\dfrac{4k+1}{4\pi}}P^0_{2k}(\cos\theta)
\end{align}$$
We can do some rearranging to arrive to the following infinite expression:
$$\begin{align}
\Aboxed{\Phi(\vec{r})&=\dfrac{2q}{4\pi\epsilon_0a}\sum_{k=1}^\infty\left(\dfrac{a}{r}\right)^{2k+1}P_{2k}(\cos\theta)}
\end{align}$$
Our leading order term is our $k=1$ charge term, thus:
$$\begin{align}
\lim_{a/r\to0}\Phi(\vec{r})&\simeq\dfrac{2q}{4\pi\epsilon_0a}\left(\dfrac{a}{r}\right)^{3}P_{2}(\cos\theta)=\dfrac{q}{4\pi\epsilon_0a}\left(\dfrac{a}{r}\right)^{3}\left(3\cos^2\theta-1\right)
\end{align}$$
In the $xy$-plane, $\theta=\tfrac{\pi}{2}$, so the equation simplifies to:
$$\begin{align}
\Aboxed{\lim_{a/r\to0}\Phi(r,\tfrac{\pi}{2},\phi)&\simeq-\dfrac{q}{4\pi\epsilon_0a}\left(\dfrac{a}{r}\right)^{3}}
\end{align}$$
We can then plot this graph with respect to $r/a$ normalized distance and unit height as:
![[Homework 3.4.1.C.png]]
Since this is our potential at $r>a$, the graph is over the domain $1<\tfrac{r}{a}<\infty$.
<div style="page-break-before: always;"></div>

### Question 4.1.D
Calculate directly from Coulomb's law the exact potential for [[#Question 4.1.B]] in the $xy$-plane. Plot it as a function of distance and compare with the result found in [[#Question 4.1.C]].

The exact potential is really simple since it is just three point charges:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{q}{4\pi\epsilon_0}\left(\dfrac{1}{|\vec{r}-a\hat{z}|}-\dfrac{2}{|\vec{r}|}+\dfrac{1}{|\vec{r}+a\hat{z}|}\right)
\end{align}$$
For a point in the $xy$-plane, $\theta=\tfrac{\pi}{2}$ once again, and thus:
$$\begin{align}
\Phi(r,\tfrac{\pi}{2},\phi)&=\dfrac{q}{4\pi\epsilon_0}\left(\dfrac{1}{\sqrt{r^2+a^2}}-\dfrac{2}{r}+\dfrac{1}{\sqrt{r^2+a^2}}\right)\\
&=-\dfrac{q}{4\pi\epsilon_0a}\left(\dfrac{2}{r/a}-\dfrac{2}{\sqrt{1+(r/a)^2}}\right)
\end{align}$$
I've plotted both, where blue is coulomb, and red is our multipole expansion:
![[Homework 3.4.1.D.png]]
They look to have very similar asymptotic behavior, but are different near $r=a$.

---
## Question 4.7
A localized distribution of charge has a charge density:
$$\begin{align}
\rho(\vec{r})&=\dfrac{1}{64\pi}r^2e^{-r}\sin^2\theta
\end{align}$$
<div style="page-break-before: always;"></div>

### Question 4.7.A
Make a multipole expansion of the potential due to this charge density and determine all the non-vanishing multipole moments. Write down the potential at large distances as a finite expansions in Legendre polynomials.

Start with the definition of $q_{lm}$, we have:
$$\begin{align}
q_{lm}&=\int Y_{lm}^*(\theta,\phi)r^l\rho(\vec{r})\ d^3r
\end{align}$$
Substitute our expressions for both $Y_{lm}^*(\theta,\phi)$ and $\rho(\vec{r})$, then:
$$\begin{align}
q_{lm}&=\int Y_{lm}^*(\theta,\phi)r^l\dfrac{1}{64\pi}r^2e^{-r}\sin^2\theta\ r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=\dfrac{1}{64\pi}\int_0^\infty r^{(l+5)-1}e^{-r}\ dr\int_0^{2\pi}\int_0^\pi Y_{lm}^*(\theta,\phi)\sin^3\theta\ d\theta\ d\phi\\
&=\dfrac{\Gamma(l+5)}{64\pi}\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}\int_0^\pi P^m_l(\cos\theta)\sin^3\theta\ d\theta\int_0^{2\pi}e^{-im\phi}\ d\phi\\
&=\dfrac{\Gamma(l+5)}{64\pi}\sqrt{\dfrac{2l+1}{4\pi}}\int_0^\pi P^0_l(\cos\theta)\sin^3\theta\ d\theta\cdot2\pi\delta_{0m}\\
\end{align}$$
We need an expression to reduce the polar integral. Looking at the table:
$$\begin{align}
\sin^2\theta&=\dfrac{2}{3}P_0^0(\cos\theta)-\dfrac{2}{3}P_2^0(\cos\theta)\\
\end{align}$$
Substituting, we get that:
$$\begin{align}
q_{lm}&=\dfrac{\Gamma(l+5)}{32}\sqrt{\dfrac{2l+1}{4\pi}}\delta_{0m}\int_0^\pi P^0_l(\cos\theta)\left[\dfrac{2}{3}P_0^0(\cos\theta)-\dfrac{2}{3}P_2^0(\cos\theta)\right]\sin\theta\ d\theta\\
&=\dfrac{\Gamma(l+5)}{48}\sqrt{\dfrac{2l+1}{4\pi}}\delta_{0m}\left[\int_{-1}^1 P^0_l(x)P_0^0(x)\ dx-\int_{-1}^1 P^0_l(x)P_2^0(x)\ dx\right]\\
&=\dfrac{\Gamma(l+5)}{48}\sqrt{\dfrac{2l+1}{4\pi}}\delta_{0m}\left[\dfrac{2(l+0)!}{(2l+1)(l-0)!}\delta_{0l}-\dfrac{2(l+0)!}{(2l+1)(l-0)!}\delta_{2l}\right]\\
&=\dfrac{\Gamma(l+5)}{48}\sqrt{\dfrac{2l+1}{4\pi}}\delta_{0m}\left[2\delta_{0l}-\dfrac{2}{5}\delta_{2l}\right]\\
\Aboxed{q_{lm}&=\sqrt{\dfrac{1}{4\pi}}\delta_{0m}\delta_{0l}-6\sqrt{\dfrac{5}{4\pi}}\delta_{0m}\delta_{2l}}
\end{align}$$
Thus there are only 2 terms of $q_{lm}$ that are non-zero:
$$\begin{align}
\Aboxed{q_{00}&=\sqrt{\dfrac{1}{4\pi}}} & \Aboxed{q_{20}&=-6\sqrt{\dfrac{5}{4\pi}}}
\end{align}$$
Using the equation for potential from $q_{lm}$, we have:
$$\begin{align}
&&\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}q_{lm}r^{-l-1}Y_{lm}(\theta,\phi)\\
\implies&&\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{4\pi}{1}\sqrt{\dfrac{1}{4\pi}}r^{-1}Y_{00}(\theta,\phi)-6\dfrac{4\pi}{5}\sqrt{\dfrac{5}{4\pi}}r^{-3}Y_{20}(\theta,\phi)\right]
\end{align}$$
We can use the known equations for $Y_{00}$ and $Y_{20}$, and find that:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\left[r^{-1}P^0_0(\cos\theta)-6r^{-3}P^0_2(\cos\theta)\right]
\end{align}$$
Lastly, we know these Legendre polynomials, so the final potential takes the form:
$$\begin{align}
\Aboxed{\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{1}{r}+\dfrac{3-9\cos^2\theta}{r^3}\right]=\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{P^0_0(\cos\theta)}{r}-6\dfrac{P^0_2(\cos\theta)}{r^3}\right]}
\end{align}$$
---
### Question 4.7.B
Determine the potential explicitly, and show that near the origin, correct to $r^2$ inclusive:
$$\begin{align}
\Phi(\vec{r})&\simeq\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{1}{4}-\dfrac{r^2}{120}P_2(\cos\theta)\right]
\end{align}$$
To find the solution exactly, we can use Coulomb's law:
$$\begin{align}
\Phi(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{1}{|\vec{r}-\vec{r}'|}\rho(\vec{r}')\ d^3r'\\
&=\dfrac{1}{4\pi\epsilon_0}\dfrac{1}{64\pi}\int\dfrac{1}{|\vec{r}-\vec{r}'|}r'^2e^{-r'}\sin^2\theta'\ r'^2\sin\theta'\ dr'\ d\theta'\ d\phi'\\
\end{align}$$
We need to expand the the pole using the series solution:
$$\begin{align}
\dfrac{1}{|\vec{r}-\vec{r}'|}&=4\pi\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{1}{2l+1}\dfrac{r^l_<}{r^{l+1}_>}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)
\end{align}$$
Substituting back in:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{1}{4\pi\epsilon_0}\dfrac{1}{64\pi}\int\dfrac{1}{|\vec{r}-\vec{r}'|}r'^4e^{-r'}\sin^3\theta'\ dr'\ d\theta'\ d\phi'\\
&=\dfrac{1}{4\pi\epsilon_0}\dfrac{1}{64\pi}\int4\pi\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{1}{2l+1}\dfrac{r^l_<}{r^{l+1}_>}Y^*_{lm}(\theta',\phi')Y_{lm}(\theta,\phi)r'^4e^{-r'}\sin^3\theta'\ dr'\ d\theta'\ d\phi'\\
&=\dfrac{1}{4\pi\epsilon_0}\dfrac{1}{16}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{1}{2l+1}Y_{lm}(\theta,\phi)\int_0^\infty\dfrac{r^l_<}{r^{l+1}_>}r'^4e^{-r'}\ dr'\int_0^{2\pi}\int_0^\pi Y^*_{lm}(\theta',\phi')\sin^3\theta'\ d\theta'\ d\phi'\\
\end{align}$$
We need to split the radius into 2 different cases, and simplify $Y_{lm}^*$ since it is azimuthally symmetric:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{1}{64\pi\epsilon_0}\sum_{l=0}^\infty P_l(\cos\theta)\left[\dfrac{1}{r^{l+1}}\int_0^rr'^{l+4}e^{-r'} dr'+r^l\int_r^\infty r'^{-l+3}e^{-r'}dr'\right]\int_0^\pi P_l(\cos\theta')\sin^3\theta'\ d\theta'
\end{align}$$
The polar integral is pretty much identical to before:
$$\begin{align}
\int_0^\pi P_l(\cos\theta')\sin^3\theta'\ d\theta'&=
\dfrac{4}{3}\delta_{0l}-\dfrac{4}{15}\delta_{2l}\\
\end{align}$$
This restricts out summation to $l=0$ and $l=2$ only:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{1}{128\pi\epsilon_0}\dfrac{4}{3}P_0(\cos\theta)\left[\dfrac{1}{r}\int_0^rr'^{4}e^{-r'} dr'+\int_r^\infty r'^{3}e^{-r'}dr'\right]
\\&-\dfrac{4}{15}\dfrac{1}{128\pi\epsilon_0}P_2(\cos\theta)\left[\dfrac{1}{r^3}\int_0^rr'^{6}e^{-r'} dr'+r^2\int_r^\infty r'e^{-r'}dr'\right]
\end{align}$$
We are going to need the finite integral equation (from integration by parts):
$$\begin{align}
\int_0^a r^k e^{-r}\ dr&=k!-e^{-a}\sum_{n=0}^k\dfrac{k!}{n!}a^n & \int_a^\infty r^k e^{-r}\ dr&=e^{-a}\sum_{n=0}^k\dfrac{k!}{n!}a^n
\end{align}$$
We then reduce the potential integrals to:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{1}{128\pi\epsilon_0}\dfrac{4}{3}P_0(\cos\theta)\left[\dfrac{4!}{r}-e^{-r}\dfrac{1}{r}\sum_{n=0}^4\dfrac{4!}{n!}r^n+e^{-r}\sum_{n=0}^3\dfrac{3!}{n!}r^n\right]
\\&-\dfrac{4}{15}\dfrac{1}{128\pi\epsilon_0}P_2(\cos\theta)\left[\dfrac{6!}{r^3}-e^{-r}\dfrac{1}{r^3}\sum_{n=0}^6\dfrac{6!}{n!}r^n+e^{-r}r^2\sum_{n=0}^1\dfrac{1!}{n!}r^n\right]
\end{align}$$
Expanding the sums, we get:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{1}{128\pi\epsilon_0}\dfrac{4}{3}P_0(\cos\theta)\left[\dfrac{24}{r}-e^{-r}\dfrac{1}{r}\left(24+24r+12r^2+4r^3+r^4\right)+e^{-r}\left(6+6r+3r^2+r^3\right)\right]
\\&-\dfrac{4}{15}\dfrac{1}{128\pi\epsilon_0}P_2(\cos\theta)\left[\dfrac{720}{r^3}-e^{-r}\dfrac{1}{r^3}\left(720+720r+360r^2+120r^3+30r^4+6r^5+r^6\right)+e^{-r}r^2\left(r+1\right)\right]
\end{align}$$
Combining like terms, we get:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{1}{96\pi\epsilon_0}\left[\dfrac{24}{r}-e^{-r}\left(\dfrac{24}{r}+18+6r+r^2\right)\right]
\\&-\dfrac{1}{480\pi\epsilon_0}P_2(\cos\theta)\left[\dfrac{720}{r^3}-e^{-r}\left(\dfrac{720}{r^3}+\dfrac{720}{r^2}+\dfrac{360}{r}+120+30r+5r^2\right)\right]
\end{align}$$
<div style="page-break-before: always;"></div>

We can factor out a $4\pi\epsilon_0$ to put it in a form more like the above:
$$\begin{align}
\Phi(\vec{r})
&=\dfrac{1}{4\pi\epsilon_0}\dfrac{1}{24}\left[\dfrac{24}{r}-e^{-r}\left(\dfrac{24}{r}+18+6r+r^2\right)\right]
\\&-\dfrac{1}{4\pi\epsilon_0}\dfrac{1}{120}P_2(\cos\theta)\left[\dfrac{720}{r^3}-e^{-r}\left(\dfrac{720}{r^3}+\dfrac{720}{r^2}+\dfrac{360}{r}+120+30r+5r^2\right)\right]
\end{align}$$
The limit is painful to do, but we can find an approximation using a Taylor series:
$$\begin{align}
-e^{-r}\left(\dfrac{24}{r}+18+6r+r^2\right)&=-\dfrac{24}{r}+6+O(r)\\
-e^{-r}\left(\dfrac{720}{r^3}+\dfrac{720}{r^2}+\dfrac{360}{r}+120+30r+5r^2\right)&=-\dfrac{720}{r^3}-30r-5r^2+O(r^3)\\
\end{align}$$
In the limit as $r\to0$, the potential becomes:
$$\begin{align}
\Phi(\vec{r})&\simeq\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{1}{4}-\dfrac{r^2}{120}P_2(\cos\theta)\right]
\end{align}$$
Exactly as we expected.

---
### Question 4.7.C
If there exists, at the origin, a nucleus with a quadrupole moment $Q=10^{-28}\mathrm{m}^2$, determine the exact magnitude of the interaction energy, assuming that the unit of charge in $\rho(\vec{r})$ above is the electronic charge and the unit of length is the Bohr radius $a_0=4\pi\epsilon_0\hbar^2/me^2=0.529\times10^{-10}\mathrm{m}$. Express your answer as a frequency by dividing by Planck's constant $h$.

The charge density in this problem is that for the $m=\pm1$ states of the $2p$ level in hydrogen, while the quadrupole interactions is of the same order as found in molecules.''

The potential around the origin in our system here is:
$$\begin{align}
\Phi(\vec{r})&\simeq-\dfrac{e}{4\pi\epsilon_0a_0}\left[\dfrac{1}{4}-\dfrac{(r/a_0)^2}{120}P_2(\cos\theta)\right]
\end{align}$$
<div style="page-break-before: always;"></div>

We can calculate the work:
$$\begin{align}
W&=\int\rho\Phi\ d^3r\\
&=-\int\rho\dfrac{e}{4\pi\epsilon_0a_0}\left[\dfrac{1}{4}-\dfrac{(r/a_0)^2}{120}P_2(\cos\theta)\right]\ d^3r\\
&=-\dfrac{e}{4\pi\epsilon_0a_0}\left[\dfrac{1}{4}\int\rho\ d^3r-\dfrac{(r/a_0)^2}{120}\int \rho P_2(\cos\theta)\ d^3r\right]\\
&=-\dfrac{e}{4\pi\epsilon_0a_0}\left[\dfrac{1}{4}q-\dfrac{(r/a_0)^2}{240}\int \rho\left(3z^2-r^2\right)\ d^3r\right]\\
W&=-\dfrac{e}{4\pi\epsilon_0a_0}\left[\dfrac{1}{4}q-\dfrac{(r/a_0)^2}{240}Q_{zz}\right]
\end{align}$$
Dividing both sides by $\hbar$ and substituting out physical constants:
$$\begin{align}
\Aboxed{\dfrac{W}{\hbar}&=-\dfrac{e}{16\pi\epsilon_0a_0\hbar}q+\dfrac{e}{960\pi\epsilon_0\hbar a_0}\dfrac{r^2}{a_0^2}Q_{zz}}
\end{align}$$
Using the values they give us, this frequency becomes:
