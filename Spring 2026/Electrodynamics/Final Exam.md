**Author:** Stanley Goodwin
**Date:** April 28th, 2026

---
## Question 1
> **Electric Dipole Radiation:** The simplest "realistic" source of electromagnetic fields is an oscillating dipole which consists of a pair of harmonically varying point charges $\pm q_0e^{-i\omega t}$ connected by a wire of length $\ell$ and indicated in $\text{Figure 1}$.
> 
> We can readily generalize the expression for the potential $\Phi$ to an arbitrary time-varying charge distribution $\rho(\vec{r},t)$. As shown in class, each source element contributes its own retarded potential as any point, giving$$\begin{align}\Phi_\text{ret}\left(\vec{r},t\right)&=\dfrac{1}{4\pi\epsilon_0}\int\dfrac{\rho(\vec{r}',t_\text{ret})}{|\vec{r}-\vec{r}'|}\ d^3r'&t_\text{ret}&=t-\dfrac{|\vec{r}-\vec{r}'|}{c}\end{align}$$

---
### Question 1.A
> Show that the retarded potential $\Phi_\text{ret}$ (for $\text{Figure 1}$) at large distances is given by$$\begin{align}\Phi_\text{ret}\left(\vec{r},t\right)&=\dfrac{q_0\ell e^{-i\omega(t-r/c)}}{4\pi\epsilon_0 r}\left(\dfrac{1}{r}-\dfrac{2\pi i}{\lambda}\right)\cos\theta\end{align}$$

I am most comfortable with spherical coordinates, so I will write charge density as
$$\begin{align}
\rho(\vec{r},t)&=\dfrac{q_0e^{-i\omega t}}{2\pi\rho^2\sin\theta}\delta(r-\ell/2)\left[\delta(\theta)-\delta(\theta-\pi)\right]
\end{align}$$
This ensures that the integration over all space correctly creates two charges of the right value.

We make the substitutions $\vec{r}\to\vec{r}'$ and $t\to t_\text{ret}$ and simplify to write it like the integration
$$\begin{align}
\rho(\vec{r}',t)&=\dfrac{q_0e^{-i\omega t}}{2\pi\rho'^2\sin\theta'}e^{i\tfrac{\omega}{c}|\vec{r}-\vec{r}'|}\delta(r'-\ell/2)\left[\delta(\theta')-\delta(\theta'-\pi)\right]
\end{align}$$
Substituting into our potential and integrating, we get the following
$$\begin{align}
\Phi_\text{ret}\left(\vec{r},t\right)&=\dfrac{q_0}{4\pi\epsilon_0}e^{-i\omega t}\left[\dfrac{e^{i\tfrac{\omega}{c}|\vec{r}-\vec{r}_t'|}}{|\vec{r}-\vec{r}_t'|}-\dfrac{e^{i\tfrac{\omega}{c}|\vec{r}-\vec{r}_b'|}}{|\vec{r}-\vec{r}_b'|}\right]
\end{align}$$
where $\vec{r}_t'=\tfrac{\ell}{2}\hat{z}$ and $\vec{r}_b'=-\tfrac{\ell}{2}\hat{z}$. 


<div style="page-break-before: always;"></div>*PDF next page*


In the far-field limit, we have the following approximations
$$\begin{align}
|\vec{r}-\vec{r}'|&\approx r-\hat{r}\cdot\vec{r}' & \dfrac{1}{|\vec{r}-\vec{r}'|}&\approx \dfrac{1}{r}+\dfrac{\hat{r}\cdot\vec{r}'}{r^2}
\end{align}$$
Both $\vec{r}_t'$ and $\vec{r}_b'$ are in $z$, so we get the inner products
$$\begin{align}
\hat{r}\cdot\vec{r}_t'&=\dfrac{\ell}{2}\cos\theta &
\hat{r}\cdot\vec{r}_b'&=-\dfrac{\ell}{2}\cos\theta 
\end{align}$$
Using all of these approximations, we get the that the potential in the far field is
$$\begin{align}
\Phi_\text{ret}\left(\vec{r},t\right)
&=\dfrac{q_0}{4\pi\epsilon_0}e^{-i\omega t}\left[-\dfrac{e^{i\tfrac{\omega}{c}\left(r+\tfrac{\ell}{2}\cos\theta\right)}-e^{i\tfrac{\omega}{c}\left(r-\tfrac{\ell}{2}\cos\theta\right)}}{r}+\dfrac{e^{i\tfrac{\omega}{c}\left(r+\tfrac{\ell}{2}\cos\theta\right)}+e^{i\tfrac{\omega}{c}\left(r-\tfrac{\ell}{2}\cos\theta\right)}}{r^2}\dfrac{\ell}{2}\cos\theta\right]\\
&=\dfrac{q_0}{4\pi\epsilon_0}e^{-i\omega t}\left[-2i\dfrac{e^{i\tfrac{\omega}{c}r}}{r}\sin\left(\tfrac{\omega}{c}\tfrac{\ell}{2}\cos\theta\right)+\ell\dfrac{e^{i\tfrac{\omega}{c}r}}{r^2}\cos\left(\tfrac{\omega}{c}\tfrac{\ell}{2}\cos\theta\right)\cos\theta\right]\\
&\approx\dfrac{q_0}{4\pi\epsilon_0}e^{-i\omega(t-r/c)}\left[-i\dfrac{\ell\omega}{rc}+\dfrac{\ell}{r^2}\right]\cos\theta\\
&=\dfrac{q_0\ell}{4\pi\epsilon_0r}e^{-i\omega(t-r/c)}\left[\dfrac{1}{r}-i\dfrac{\omega}{c}\right]\cos\theta
\end{align}$$
Lastly using $c=\omega/k$ and $k=2\pi/\lambda$, we get the final approximation to be
$$\begin{align}
\Aboxed{\Phi_\text{ret}\left(\vec{r},t\right)&=\dfrac{q_0\ell e^{-i\omega(t-r/c)}}{4\pi\epsilon_0 r}\left(\dfrac{1}{r}-\dfrac{2\pi i}{\lambda}\right)\cos\theta}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 1.B
> To verify your answer, check that when $\omega=0$, the retarded solution reduces to the first two terms of the electrostatic potential derived in class $(4.10)$.

With the solution from [[#Question 1.A]] (before substituting in $\lambda$),
$$\begin{align}
\Phi_\text{ret}\left(\vec{r},t\right)&=\dfrac{q_0\ell}{4\pi\epsilon_0r}e^{-i\omega(t-r/c)}\left[\dfrac{1}{r}-i\dfrac{\omega}{c}\right]\cos\theta
\end{align}$$
In the $\omega\to0$ limit, this becomes
$$\begin{align}
\Aboxed{\lim_{\omega\to0}\Phi_\text{ret}\left(\vec{r},t\right)&=\dfrac{q_0\ell}{4\pi\epsilon_0}\dfrac{\cos\theta}{r^2}}
\end{align}$$
In Jackson's Electrodynamics (3rd Edition), equation $(4.10)$ gives us the potential expansion
$$\begin{align}
\Phi(\vec{x})&=\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{q}{r}+\dfrac{\vec{p}\cdot\vec{x}}{r^3}+\dots\right]
\end{align}$$
The charge and dipole moment, after integration, reduce to
$$\begin{align}
q&=0 & \vec{p}&=q_0\ell z=q_0\ell r\cos\theta
\end{align}$$
Substituting into the classic equation, our potential becomes
$$\begin{align}
\Phi(\vec{x})&\approx\dfrac{1}{4\pi\epsilon_0}\left[\dfrac{0}{r}+\dfrac{q_0\ell r\cos\theta}{r^3}\right]=\boxed{\dfrac{q_0\ell}{4\pi\epsilon_0}\dfrac{\cos\theta}{r^2}}
\end{align}$$
These both match!


<div style="page-break-before: always;"></div>*PDF next page*

### Question 1.C
> We next proceed to generate the electric and magnetic fields, but first we must obtain the retarded vector potential $\vec{A}_\text{ret}$. Note that in a short wire connecting two charges, there is a current $I$.

---
#### Question 1.C.i
> Find $I$.

The rate change in charge at either point is the current, and so it is simply
$$\begin{align}
I&=\dfrac{d}{dt}\left(q_0e^{-i\omega t}\right)=-i\omega q_0e^{-i\omega t}
\end{align}$$
The current density just restricts the current in this domain of space, and so
$$\begin{align}
\Aboxed{I&=-i\omega q_0e^{-i\omega t}} & \Aboxed{\vec{J}(\vec{r},t)=-i\omega q_0e^{-i\omega t}\hat{z}\ \delta(x)\delta(y)}
\end{align}$$
Where I am writing this in cartesian coordinates for sake of brevity.


<div style="page-break-before: always;"></div>*PDF next page*

#### Question 1.C.ii
> Using your expression for the current, derive the retarded vector potential $\vec{A}_\text{ret}$.

The retarded vector potential takes a very similar form to the scalar potential
$$\begin{align}
\vec{A}_\text{ret}\left(\vec{r},t\right)&=\dfrac{\mu_0}{4\pi}\int\dfrac{\vec{J}(\vec{r}',t_\text{ret})}{|\vec{r}-\vec{r}'|}\ d^3r'&t_\text{ret}&=t-\dfrac{|\vec{r}-\vec{r}'|}{c}
\end{align}$$
Substituting the current density from [[#Question 1.C.i|above]], we have that (after simplification from the delta functions), our vector potential is
$$\begin{align}
\vec{A}_\text{ret}\left(\vec{r},t\right)&=\dfrac{-i\omega q_0\mu_0}{4\pi}e^{-i\omega t}\hat{z}\int\dfrac{e^{i\tfrac{\omega}{c}|\vec{r}-\vec{r}'|}}{|\vec{r}-\vec{r}'|}\ dz'
\end{align}$$
Same approximations as previous
$$\begin{align}
|\vec{r}-\vec{r}'|&\approx r-\hat{r}\cdot\vec{r}' & \dfrac{1}{|\vec{r}-\vec{r}'|}&\approx \dfrac{1}{r}+\dfrac{\hat{r}\cdot\vec{r}'}{r^2}
\end{align}$$
Our vector potential becomes
$$\begin{align}
\vec{A}_\text{ret}\left(\vec{r},t\right)
&=\dfrac{-i\omega q_0\mu_0}{4\pi}e^{-i\omega t}\hat{z}\int_{-\ell/2}^{\ell/2}\left(\dfrac{1}{r}+\dfrac{z'\cos\theta}{r^2}\right)e^{i\tfrac{\omega}{c}r}e^{-i\tfrac{\omega}{c}z'\cos\theta}\ dz'\\
&=\dfrac{-i\omega q_0\mu_0}{4\pi}e^{-i\omega(t-r/c)}\hat{z}\left[\dfrac{1}{r}\int e^{-i\tfrac{\omega}{c}z'\cos\theta}\ dz'+\dfrac{\cos\theta}{r^2}\int z'e^{-i\tfrac{\omega}{c}z'\cos\theta}\ dz'\right]\\
&=\dfrac{-i\omega q_0\mu_0}{4\pi}e^{-i\omega(t-r/c)}\hat{z}\left[\dfrac{2}{r} \dfrac{\sin\left(\tfrac{\omega}{c}\tfrac{\ell}{2}\cos\theta\right)}{2i\tfrac{\omega}{c}\cos\theta}+2i\dfrac{\cos\theta}{r^2}\dfrac{\sin\left(\tfrac{\omega}{c}\tfrac{\ell}{2}\cos\theta\right)}{\left(\tfrac{\omega}{c}\cos\theta\right)^2}-i\dfrac{\ell\cos\theta}{r^2}\dfrac{\cos\left(\tfrac{\omega}{c}\cos\theta\right)}{\left(\tfrac{\omega}{c}\cos\theta\right)}\right]\\
&\approx\dfrac{-i\omega q_0\mu_0}{4\pi}e^{-i\omega(t-r/c)}\hat{z}\left[\dfrac{2}{r} \dfrac{\tfrac{\omega}{c}\tfrac{\ell}{2}\cos\theta}{2i\tfrac{\omega}{c}\cos\theta}+2i\dfrac{\cos\theta}{r^2}\dfrac{\tfrac{\omega}{c}\tfrac{\ell}{2}\cos\theta}{\left(\tfrac{\omega}{c}\cos\theta\right)^2}-i\dfrac{\ell\cos\theta}{r^2}\dfrac{1}{\left(\tfrac{\omega}{c}\cos\theta\right)}\right]\\
&=\dfrac{-i\omega q_0\mu_0}{4\pi}e^{-i\omega(t-r/c)}\hat{z}\left[-i\dfrac{\ell}{2r} +i\dfrac{c\ell}{\omega r^2}-i\dfrac{c\ell}{\omega r^2}\right]\\
\Aboxed{\vec{A}_\text{ret}\left(\vec{r},t\right)&=-\dfrac{\omega q_0\ell\mu_0}{8\pi r}e^{-i\omega(t-r/c)}\hat{z}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

#### Question 1.C.iii
> Then derive $\vec{B}$ and $\vec{E}$.

Using the table for coordinates [Wikipedia](https://en.wikipedia.org/wiki/Del_in_cylindrical_and_spherical_coordinates), the curl in cylindrical coordinates using our previous result in $\hat{z}$ and having no $\phi$ dependence, is
$$\begin{align}
\vec{B}&=\vec\nabla\times\vec{A}=-\dfrac{\partial A_z}{\partial\rho}\hat{\phi} & r=\sqrt{\rho^2+z^2}
\end{align}$$
This corresponds to the derivative
$$\begin{align}
-\dfrac{\partial}{\partial\rho}\dfrac{\omega q_0\ell\mu_0}{8\pi\sqrt{\rho^2+z^2}}e^{-i\omega(t-\sqrt{\rho^2+z^2}/c)}
\end{align}$$
Using the product and chain rule, we get that
$$\begin{align}
B_\phi
&=-\dfrac{\omega q_0\ell\mu_0}{8\pi}e^{-i\omega t}\dfrac{\partial}{\partial\rho}\dfrac{e^{i\tfrac{\omega}{c}(\sqrt{\rho^2+z^2})}}{\sqrt{\rho^2+z^2}}\\
&=-\dfrac{\omega q_0\ell\mu_0}{8\pi}e^{-i\omega t}\dfrac{i\tfrac{\omega}{c}e^{i\tfrac{\omega}{c}(\sqrt{\rho^2+z^2})}\sqrt{\rho^2+z^2}-e^{i\tfrac{\omega}{c}(\sqrt{\rho^2+z^2})}}{\rho^2+z^2}\dfrac{\partial}{\partial\rho}\left(\sqrt{\rho^2+z^2}\right)\\
&=-\dfrac{\omega q_0\ell\mu_0}{8\pi}e^{-i\omega(t-r/c)}\dfrac{i\tfrac{\omega}{c}r-1}{r^2}\dfrac{\rho}{r}\\
\Aboxed{B_\phi&=-\dfrac{\omega q_0\ell\mu_0}{8\pi}e^{-i\omega(t-r/c)}\left(\dfrac{i\omega/c}{r}-\dfrac{1}{r^2}\right)\sin\theta}
\end{align}$$
In the far-field limit, the $1/r^2$ drops off fast, so we can neglect it. Our two fields are then
$$\begin{align}
\Aboxed{\vec{B}&=-i\dfrac{\omega^2 q_0\ell\mu_0}{8\pi r c}e^{-i\omega(t-r/c)}\sin\theta\ \hat{\phi}} & \Aboxed{\vec{E}&=-i\dfrac{\omega^2 q_0\ell}{8\pi\epsilon_0 r c}e^{-i\omega(t-r/c)}\sin\theta\ \hat{\theta}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

## Question 2
> A large flat plate of glass of thickness $d$ and dielectric constant $\epsilon$ is placed in a uniform field $\vec{E}_0$. The plate is inclined at an angle $\theta$ with respect to the electric field.

I will assume that the plate has fully polarized and is at equilibrium.

---
### Question 2.A
> Show that if $\theta\ll1$ then the electric field inside the plate makes an angle $\theta'=\theta/\epsilon$ with the surface of the plate and has a magnitude of$$E=E_0\left[1-\left(1-\dfrac{1}{\epsilon^2}\right)\dfrac{\theta^2}{2}\right]$$

What I did immediately is reorient the electric field to be in the $\hat{z}$ direction and have the plane then respect to this direction. Since the material is isotropic, this makes no difference.

The two boundary equations we will need are
$$\begin{align}
\vec{D}^\perp_0-\vec{D}^\perp&=\sigma & \vec{E}_0^\parallel-\vec{E}^\parallel&=0
\end{align}$$
There are no free surface charges, so $\sigma=0$, and splitting each vector into components based off of the angles, we have that
$$\begin{align}
\epsilon_0E_0\sin\theta&=\epsilon_g E\sin\theta' & E_0\cos\theta&=E\cos\theta'
\end{align}$$
Dividing each equation by each other (and letting $\epsilon=\epsilon_g/\epsilon_0$), we get the relationship that
$$\begin{align}
\dfrac{\epsilon_0E_0\sin\theta}{E_0\cos\theta}&=\dfrac{\epsilon E\sin\theta'}{E\cos\theta'}
&\implies &&
\epsilon_0\tan\theta&=\epsilon\tan\theta'
&\implies &&
\tan\theta&=\epsilon\tan\theta'
\end{align}$$
For small angles $\theta$, the relationship between the angles become
$$\begin{align}
\Aboxed{\theta'&=\dfrac{1}{\epsilon}\theta}
\end{align}$$
We can Taylor expand the parallel equation to find that
$$\begin{align}
E&=E_0\left(1-\dfrac{1}{2}\theta^2\right)\left(1+\dfrac{1}{2}\dfrac{1}{\epsilon^2}\theta^2\right)\\
&=E_0\left(1-\dfrac{1}{2}\theta^2+\dfrac{1}{2}\dfrac{1}{\epsilon^2}\theta^2\right)+\mathcal{O}\left(\theta^4\right)\\
\Aboxed{E&\approx E_0\left(1-\left[1-\dfrac{1}{\epsilon^2}\right]\dfrac{\theta^2}{2}\right)}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

%% ### Question 2.B
> Sketch the lines of the electric field displacement $\vec{D}$ inside and outside the plate. 
> Sketch the lines of the electric field $\vec{E}$ inside and outside the plate. Assume $\epsilon>1$.

On exam paper. %%

## Question 3
> A particle of charge $q$ and mass $m$, initially at rest, is acted upon by a uniform electric field $\vec{E}$ directed along the $x$-axis. Show that the relativistic equation of motion has the solution$$\begin{align}x=\dfrac{c}{qE}\sqrt{m^2c^2+(qEt)^2}-\dfrac{mc^2}{qE}\end{align}$$Check that $\tfrac{dx}{dt}\to c$ as $t\to\infty$. Check that in the non-relativistic limit, this solution has the expected form.

Starting from $\vec{F}=\dfrac{d\vec{p}}{dt}$, and that this moves in one direction, and force is constant in time,
$$\begin{align}
qE&=\dfrac{d}{dt}\left(\gamma mv\right) &\implies&& \gamma mv&=qEt
\end{align}$$
with the implicit assumption that $v(0)=0$ for the sake of convenience. We now need to solve this for velocity, and so
$$\begin{align}
\gamma mv&=qEt
&\implies&&
\dfrac{v}{\sqrt{1-v^2}}&=\dfrac{qE}{m}t
&\implies&&
v^2&=\left(\dfrac{qE}{m}t\right)^2\left(1-v^2\right)
\end{align}$$
Rearranging, we get that
$$\begin{align}
v^2&=\dfrac{\left(\tfrac{qE}{m}t\right)^2}{\left(1+\left(\tfrac{qE}{m}t\right)^2\right)}
&\implies&&
v(t)&=t\left(\left(\tfrac{m}{qE}\right)^2+t^2\right)^{-1/2}\\
\end{align}$$
We now integrate this velocity over time, taking $v(0)=0$, to get that
$$\begin{align}
x(t)&=\int_0^t t'\left(\left(\tfrac{m}{qE}\right)^2+t'^2\right)^{-1/2}\ dt'\\
&=\left(\left(\tfrac{m}{qE}\right)^2+t^2\right)^{1/2}-\dfrac{m}{qE}\\
&=\dfrac{1}{qE}\sqrt{m^2+(qEt)^2}-\dfrac{m}{qE}\\
\Aboxed{x(t)&=\dfrac{c}{qE}\sqrt{(mc)^2+(qEt)^2}-\dfrac{mc^2}{qE}}
\end{align}$$
The last step was just reinserting $c$ in since I had used $c=1$ for simplicity.


<div style="page-break-before: always;"></div>*PDF next page*


In the time-to-infinity limit, we do correctly find
$$\begin{align}
\Aboxed{\lim_{t\to\infty}v(t)=\lim_{t\to\infty}\dfrac{t}{\sqrt{\left(\tfrac{m}{qE}\right)^2+t^2}}=\lim_{t\to\infty}\dfrac{t}{\sqrt{t^2}}=1\  (c)}
\end{align}$$
In the non-relativistic limit, we can approximate the square root as $\sqrt{1+x}=1+\tfrac{1}{2}x$, we get that
$$\begin{align}
x(t)&=\dfrac{c}{qE}mc\left(1+\dfrac{1}{2}\dfrac{(qEt)^2}{(mc)^2}\right)-\dfrac{mc^2}{qE}\\
&=\dfrac{c}{qE}mc\cdot\dfrac{1}{2}\dfrac{(qEt)^2}{(mc)^2}\\
\Aboxed{x(t)&=\dfrac{qE}{2m}t^2}
\end{align}$$
Starting from a constant acceleration $\dfrac{F}{m}=\dfrac{qE}{m}$, and integrating twice for time, this is what you would expect the solution to be.


<div style="page-break-before: always;"></div>*PDF next page*

%% ## Question 4
> As a charge's speed approaches $c$, its electromagnetic field increasingly resembles that of a plane wave. To quantify this correspondence, we analyze the frequency spectrum of the field. The field from a passing charge is a time pulse, and its frequency-domain integral gives the total field energy, which diverges without a short-distance cutoff. We begin by Fourier-analyzing the electric field component transverse to the velocity $u$. %%


### Question 4.A
> Use the transverse field that was derived in class to show that its Fourier component is$$\begin{align}E_{\perp}(\omega)&=\dfrac{e}{4\pi^2\epsilon_0bu}\left[\dfrac{\omega b}{\gamma u}K_1\left(\dfrac{\omega b}{\gamma u}\right)\right]\end{align}$$where $K_1$ is the Bessel function of the second kind with imaginary argument, $\gamma=(1-u^2/c^2)^{-1/2}$and $b$ is the perpendicular particle trajectory and the observer.

Start with the electric field perpendicular
$$\begin{align}
E_\perp(t)&=\dfrac{e}{4\pi\epsilon_0}\dfrac{\gamma b}{(b^2+\gamma^2u^2t^2)^{3/2}}
\end{align}$$
We then take its Fourier transform
$$\begin{align}
E_\perp(\omega)&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{i\omega t}\cdot\dfrac{e}{4\pi\epsilon_0}\dfrac{\gamma b}{(b^2+\gamma^2u^2t^2)^{3/2}}\ dt
\end{align}$$
Since we want to get an expression that can be found on a table, make the substitution
$$\begin{align}
x&=\dfrac{\gamma u}{b}t & t&=\dfrac{b}{\gamma u}x & dt&=\dfrac{b}{\gamma u}dx
\end{align}$$
Substituting, we get that
$$\begin{align}
E_\perp(\omega)&=\dfrac{e}{8\pi^2\epsilon_0}\dfrac{1}{bu}\int_{-\infty}^\infty e^{i\omega\tfrac{b}{\gamma u}x}\dfrac{1}{(1+x^2)^{3/2}}dx
\end{align}$$
Now we need another substitution $\Omega=\dfrac{\omega b}{\gamma u}\iff\omega=\dfrac{\gamma u}{b}\Omega$, and so we then have
$$\begin{align}
E_\perp(\omega)&=\dfrac{e}{8\pi^2\epsilon_0}\dfrac{1}{bu}\int_{-\infty}^\infty e^{i\Omega x}\dfrac{1}{(1+x^2)^{3/2}}dx
\end{align}$$
From an integral table, this Fourier transform turns into
$$\begin{align}
E_\perp(\omega)&=\dfrac{e}{8\pi^2\epsilon_0}\dfrac{1}{bu}\cdot2\Omega K_1\left(\Omega\right)
\end{align}$$
Reversing our substitution for $\Omega$, we get that
$$\begin{align}
\Aboxed{E_\perp(\omega)&=\dfrac{e}{4\pi^2\epsilon_0}\dfrac{1}{bu}\left[\dfrac{\omega b}{\gamma u}K_1\left(\dfrac{\omega b}{\gamma u}\right)\right]}
\end{align}$$


<div style="page-break-before: always;"></div>*PDF next page*

%% ### Question 4.B
--- %%
#### Question 4.B.i
> Write down the expression for the total energy $U$ carried by the electric field.

We just need to integrate the energy density in time
$$\begin{align}
U(t)&=\dfrac{1}{2}\epsilon_0\int\left|\vec{E}(\vec{r},t)\right|^2\ d^3r\approx\dfrac{1}{2}\epsilon_0\int\left|\vec{E}_\perp(\vec{r},t)\right|^2\ d^3r
\end{align}$$
or in terms of the Fourier transformed quantity $\omega$
$$\begin{align}
U(\omega)&=\dfrac{1}{2}\epsilon_0\int\left|\vec{E}(\vec{r},\omega)\right|^2\ d^3r\approx\dfrac{1}{2}\epsilon_0\int\left|\vec{E}_\perp(\vec{r},\omega)\right|^2\ d^3r
\end{align}$$
Since this is very fast moving, the perpendicular component is much larger than $E_\parallel$.


<div style="page-break-before: always;"></div>*PDF next page*

#### Question 4.B.i
> Show that the Fourier component of the energy is given by$$\begin{align}U(\omega)&=\dfrac{2}{\omega}\dfrac{e^2}{4\pi\epsilon_0}\ln\!\left(\dfrac{\gamma u}{\omega b_\text{min}}\right)\end{align}$$where $b_\text{min}$ is an arbitrary lower cutoff for the Coulomb field, choosing $\gamma u/\omega$ as your upper limit along $b$.

Starting with the perpendicular component in frequency form
$$\begin{align}
E_{\perp}(\omega)&=\dfrac{e}{4\pi^2\epsilon_0}\dfrac{\omega}{\gamma u^2}K_1\!\left(\dfrac{\omega b}{\gamma u}\right)
\end{align}$$
the square magnitude is
$$\begin{align}
|E_{\perp}(\omega)|^2&=\dfrac{e^2}{16\pi^4\epsilon_0^2}\dfrac{\omega^2}{\gamma^2 u^4}K_1\!\left(\dfrac{\omega b}{\gamma u}\right)^2
\end{align}$$
Our value for $b$ is the radius of a cylinder about the axis that is the particle's motion at a singular point $z$. We can then write the space integral in cylindrical coordinates as
$$\begin{align}
U(\omega)
&\approx\dfrac{1}{2}\epsilon_0\int\left|\vec{E}_\perp(\vec{r},\omega)\right|^2\ b\ db\ d\phi\\
&=\dfrac{e^2}{32\pi^4\epsilon_0}\dfrac{\omega^2}{\gamma^2 u^4}\int_{b_\text{min}}^{\gamma u/\omega}bK_1\!\left(\dfrac{\omega b}{\gamma u}\right)^2\ db\ d\phi\\
&=\dfrac{e^2}{16\pi^3\epsilon_0}\dfrac{\omega^2}{\gamma^2 u^4}\left(\dfrac{\gamma u}{\omega}\right)^2\int_{b_\text{min}}^{\gamma u/\omega}\left(\dfrac{\omega b}{\gamma u}\right)K_1\!\left(\dfrac{\omega b}{\gamma u}\right)^2\ d\left(\dfrac{\omega b}{\gamma u}\right)\\
&=\dfrac{e^2}{16\pi^3\epsilon_0}\dfrac{1}{u^2}\int_{\tfrac{\omega}{\gamma u}b_\text{min}}^{1}xK_1\!\left(x\right)^2\ dx\\
&\approx\dfrac{e^2}{16\pi^3\epsilon_0}\dfrac{1}{u^2}\int_{\tfrac{\omega}{\gamma u}b_\text{min}}^{1}x\left(\dfrac{1}{x}\right)^2\ dx\\
&=\dfrac{e^2}{16\pi^3\epsilon_0}\dfrac{1}{u^2}\int_{\tfrac{\omega}{\gamma u}b_\text{min}}^{1}\dfrac{1}{x}\ dx\\
&=\dfrac{e^2}{16\pi^3\epsilon_0}\dfrac{1}{u^2}\ln\left(\dfrac{\gamma u}{\omega b_\text{min}}\right)
\end{align}$$
I'm not sure why my answer is different here. Maybe the extra factor out the front is proportional? If the following is true, I have the same answer
$$\begin{align}
\omega&=8\pi^2u^2 &&\text{But I don't think this is correct...}
\end{align}$$
