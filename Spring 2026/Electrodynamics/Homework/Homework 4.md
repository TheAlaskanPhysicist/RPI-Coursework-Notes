**Author:** Stanley Goodwin
**Date:** March 15th, 2026

---
## Question 7.3
> An infinite volume of uniform, isotropic, apermeable, lossless dielectric with index of refraction $n$ is bisected by a plane $P$, and physically separated in the direction of $P$'s normal by displacement $d$. The new separated volume is filled with air $(n=1)$. A electromagnetic plane wave of frequency $\omega$ originates within the dielectric volume from infinity and is incident on the interface of the gap with angle of incidence $i$.
#### Clarification of Standards
I will separate the problem into 3 regions:
$$\begin{align}
\text{Region I: Incidence} && \text{Region II: Air Gap} && \text{Region III: Transmittence}
\end{align}$$
All three regions have incoming wavevectors, then regions $\text{I, II}$ have reflected wavevectors. Reflected wavevectors will be denoted with a $'$ with the same symbol as incoming.


<div style="page-break-before: always;"></div>*PDF next page*

#### Electric Field & Boundary Conditions
For the sake of writing more LaTeX than is needed, it's relatively simple to show all the angular frequencies are identical, since our boundary conditions hold for all time $t$. Thus, we can write the following general forms of the electric fields in each region as:
$$\begin{align}
\vec{E}_\text{I}(\vec{x},t)&=
\hat{\epsilon}_\text{I}E_\text{I}e^{-i\left(\omega t-\vec{k}_\text{I}\cdot\vec{x}\right)}+
\hat{\epsilon}_\text{I}'E_\text{I}'e^{-i\left(\omega t-\vec{k}_\text{I}'\cdot\vec{x}\right)} & 
\vec{k}_\text{I}&=\dfrac{\omega}{c/n}\hat{k}_\text{I} \\

\vec{E}_\text{II}(\vec{x},t)&=
\hat{\epsilon}_\text{II}E_\text{II}e^{-i\left(\omega t-\vec{k}_\text{II}\cdot\vec{x}\right)}+
\hat{\epsilon}_\text{II}'E_\text{II}'e^{-i\left(\omega t-\vec{k}_\text{II}'\cdot\vec{x}\right)} & 
\vec{k}_\text{II}&=\dfrac{\omega}{c/1}\hat{k}_\text{II} \\

\vec{E}_\text{III}(\vec{x},t)&=
\hat{\epsilon}_\text{III}E_\text{III}e^{-i\left(\omega t-\vec{k}_\text{III}\cdot(\vec{x}-d\hat{z})\right)} & 
\vec{k}_\text{III}&=\dfrac{\omega}{c/n}\hat{k}_\text{III}
\end{align}$$
We must have continuity for all $t$ and any point on the $xy$-plane at each interface. After cancelling like terms, we get the following conditions that must be satisfied:
$$\begin{align}
\vec{k}_\text{I}\cdot\vec{x}=\vec{k}_\text{I}'\cdot\vec{x}
&=\vec{k}_\text{II}\cdot\vec{x}=\vec{k}_\text{II}'\cdot\vec{x}
&\implies&&
n\hat{k}_\text{I}\cdot\vec{x}=n\hat{k}_\text{I}'\cdot\vec{x}
&=\hat{k}_\text{II}\cdot\vec{x}=\hat{k}_\text{II}'\cdot\vec{x}
& (z&=0)
\\
\vec{k}_\text{II}\cdot\vec{x}=\vec{k}_\text{II}'\cdot\vec{x}
&=\vec{k}_\text{III}\cdot(\vec{x}-d\hat{z})
&\implies&&
\hat{k}_\text{II}\cdot\vec{x}=\hat{k}_\text{II}'\cdot\vec{x}
&=n\hat{k}_\text{III}\cdot(\vec{x}-d\hat{z})
& (z&=d)
\end{align}$$
Since our medium is agnostic to translation or rotations in the $xy$-plane, we can impose the plane of incidence is the $xz$-plane without loss of generality. Therefore, we can represent our wavevector components in polar form relative to the surface normal $(\pm\hat{z})$:
$$\begin{align}
\hat{k}&=\hat{x}\sin\theta+\hat{z}\cos\theta
\end{align}$$
For our conditions, that gives us the following:
$$\begin{align}
n\sin\theta_\text{I}=n\sin\theta_\text{I}'
&=\sin\theta_\text{II}=\sin\theta_\text{II}'
\\
x\sin\theta_\text{II}=x\sin\theta_\text{II}'
&=nx\sin\theta_\text{III}
\end{align}$$
These can be written in terms of Snell's Laws and Law of Reflections:
$$\begin{align}
\theta_\text{I}&=\theta_\text{I}'=\theta_\text{III} & n\sin\theta_\text{I}&=\sin\theta_\text{II}\\
\theta_\text{II}&=\theta_\text{II}' & \sin\theta_\text{II}&=n\sin\theta_\text{III}
\end{align}$$
We also know that $\cos\theta_\text{II}=\sqrt{1-n^2\sin^2\theta_\text{I}}$ . To substitute back into the electric fields, for any arbitrary choice of $t,x,y$, it will only introduce a phase factor into the electric field coefficients. Since we are yet to calculate them, we will let $t=x=y=0$ without loss of generality:
$$\begin{align}
\vec{E}_\text{I}(\vec{x},t)&=
\hat{\epsilon}_\text{I}E_\text{I}e^{i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} +
\hat{\epsilon}_\text{I}'E_\text{I}'e^{-i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} \\

\vec{E}_\text{II}(\vec{x},t)&=
\hat{\epsilon}_\text{II}E_\text{II}e^{i\tfrac{\omega}{c}z\cos\theta_\text{II}} +
\hat{\epsilon}_\text{II}'E_\text{II}'e^{-i\tfrac{\omega}{c}z\cos\theta_\text{II}} \\

\vec{E}_\text{III}(\vec{x},t)&=
\hat{\epsilon}_\text{III}E_\text{III}e^{i\tfrac{\omega}{c/n}(z-d)\cos\theta_\text{I}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

#### Field Coefficients: Perpendicular Polarization
The electric field is perpendicular to the plane of incidence ($xz$-plane), so $+\hat{y}$. Magnetic field is written in the form $\vec{B}=\tfrac{1}{c/n}\hat{k}\times\vec{E}$. All together, we get the 6 fields:
$$\begin{align}
\vec{E}_\text{I}(\vec{x},t)&=
\hat{y}E_\text{I}e^{i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} +
\hat{y}E_\text{I}'e^{-i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} \\

\vec{E}_\text{II}(\vec{x},t)&=
\hat{y}E_\text{II}e^{i\tfrac{\omega}{c}z\cos\theta_\text{II}} +
\hat{y}E_\text{II}'e^{-i\tfrac{\omega}{c}z\cos\theta_\text{II}} \\

\vec{E}_\text{III}(\vec{x},t)&=
\hat{y}E_\text{III}e^{i\tfrac{\omega}{c/n}(z-d)\cos\theta_\text{I}}
\end{align}$$
$$\begin{align}
\vec{B}_\text{I}(\vec{x},t)&=
\left(\hat{z}\sin\theta_\text{I}-\hat{x}\cos\theta_\text{I}\right)\dfrac{E_\text{I}}{c/n}e^{i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} +
\left(\hat{z}\sin\theta_\text{I}+\hat{x}\cos\theta_\text{I}\right)\dfrac{E_\text{I}'}{c/n}e^{-i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} \\

\vec{B}_\text{II}(\vec{x},t)&=
\left(\hat{z}\sin\theta_\text{II}-\hat{x}\cos\theta_\text{II}\right)\dfrac{E_\text{II}}{c}e^{i\tfrac{\omega}{c}z\cos\theta_\text{II}} +
\left(\hat{z}\sin\theta_\text{II}+\hat{x}\cos\theta_\text{II}\right)\dfrac{E_\text{II}'}{c}e^{-i\tfrac{\omega}{c}z\cos\theta_\text{II}} \\

\vec{B}_\text{III}(\vec{x},t)&=
\left(\hat{z}\sin\theta_\text{I}-\hat{x}\cos\theta_\text{I}\right)\dfrac{E_\text{III}}{c/n}e^{i\tfrac{\omega}{c/n}(z-d)\cos\theta_\text{I}}
\end{align}$$
Since there are no free charges or currents at either interface, we have continuity in the perpendicular components of $\vec{D},\vec{B}$, and parallel components of $\vec{E},\vec{H}$. We have two interfaces to consider, so we have 8 total conditions:
$$\begin{align}
\left[\epsilon_\text{I}\vec{E}_\text{I}(\vec{x},t)\cdot\hat{z}\right.&=\left.\epsilon_\text{II}\vec{E}_\text{II}(\vec{x},t)\cdot\hat{z}\right]_{z=0}&\implies&& 
0&=0\\

\left[\vec{E}_\text{I}(\vec{x},t)\times\hat{z}\right.&=\left.\vec{E}_\text{II}(\vec{x},t)\times\hat{z}\right]_{z=0}&\implies&& 
E_\text{I}+E_\text{I}'&=E_\text{II}+E_\text{II}' \\

\left[\vec{B}_\text{I}(\vec{x},t)\cdot\hat{z}\right.&=\left.\vec{B}_\text{II}(\vec{x},t)\cdot\hat{z}\right]_{z=0}&\implies&&
E_\text{I}+E_\text{I}'&=E_\text{II}+E_\text{II}'\\

\left[\dfrac{1}{\mu_\text{I}}\vec{B}_\text{I}(\vec{x},t)\times\hat{z}\right.&=\left.\dfrac{1}{\mu_\text{I}}\vec{B}_\text{II}(\vec{x},t)\times\hat{z}\right]_{z=0}&\implies&& 
\dfrac{\mu_\text{II}}{\mu_\text{I}}\dfrac{n\cos\theta_\text{I}}{\cos\theta_\text{II}}\left(E_\text{I}-E_\text{I}'\right)
&=E_\text{II}-E_\text{II}' \\

\left[\epsilon_\text{II}\vec{E}_\text{II}(\vec{x},t)\cdot\hat{z}\right.&=\left.\epsilon_\text{III}\vec{E}_\text{III}(\vec{x},t)\cdot\hat{z}\right]_{z=d}&\implies&& 
0&=0\\

\left[\vec{E}_\text{II}(\vec{x},t)\times\hat{z}\right.&=\left.\vec{E}_\text{III}(\vec{x},t)\times\hat{z}\right]_{z=d}&\implies&& 
E_\text{II}e^{i\tfrac{\omega}{c}d\cos\theta_\text{II}} +
E_\text{II}'e^{-i\tfrac{\omega}{c}d\cos\theta_\text{II}}&=E_\text{III}\\

\left[\vec{B}_\text{II}(\vec{x},t)\cdot\hat{z}\right.&=\left.\vec{B}_\text{III}(\vec{x},t)\cdot\hat{z}\right]_{z=d}&\implies&&
E_\text{II}e^{i\tfrac{\omega}{c}d\cos\theta_\text{II}}+E_\text{II}'e^{-i\tfrac{\omega}{c}d\cos\theta_\text{II}}
&=\dfrac{n\sin\theta_\text{I}}{\sin\theta_\text{II}}\ E_\text{III}\\

\left[\dfrac{1}{\mu_\text{II}}\vec{B}_\text{II}(\vec{x},t)\times\hat{z}\right.&=\left.\dfrac{1}{\mu_\text{III}}\vec{B}_\text{III}(\vec{x},t)\times\hat{z}\right]_{z=d}&\implies&& 
E_\text{II}e^{i\tfrac{\omega}{c}d\cos\theta_\text{II}}-E_\text{II}'e^{-i\tfrac{\omega}{c}d\cos\theta_\text{II}}
&=\dfrac{\mu_\text{II}}{\mu_\text{III}}\dfrac{n\cos\theta_\text{I}}{\cos\theta_\text{II}}\ E_\text{III}
\end{align}$$
For some further simplification, we can assume the following values:
$$\begin{align}
\epsilon_\text{I}&=\epsilon_\text{III}=\epsilon & \epsilon_\text{II}=\epsilon_0\\
\mu_\text{I}&=\mu_\text{III}=\mu & \mu_\text{II}=\mu_0\\
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


Using those and earlier relations for the angles, we have the conditions:
$$\begin{align}
E_\text{I}+E_\text{I}'&=E_\text{II}+E_\text{II}' &
E_\text{II}e^{i\alpha} +
E_\text{II}'e^{-i\alpha}
&=E_\text{III}\\
\beta\left(E_\text{I}-E_\text{I}'\right)&=E_\text{II}-E_\text{II}' &
E_\text{II}e^{i\alpha} -
E_\text{II}'e^{-i\alpha}
&=\beta E_\text{III}
\end{align}$$
where we have these coefficients:
$$\begin{align}
\alpha&=\dfrac{\omega}{c}d\sqrt{1-n^2\sin^2\theta_\text{I}} &&&
\beta&=\dfrac{\mu_0}{\mu}\dfrac{n\cos\theta_\text{I}}{\sqrt{1-n^2\sin^2\theta_\text{I}}}
\end{align}$$
With 4 equations and 5 unknowns, we can rearrange all systems in terms of $E_\text{I}$:
$$\begin{align}
\dfrac{E_\text{I}'}{E_\text{I}}&=-\dfrac{(1+\beta)}{(1-\beta)}\dfrac{e^{i\alpha}-e^{-i\alpha}}{e^{i\alpha}-\left(\tfrac{1+\beta}{1-\beta}\right)^2e^{-i\alpha}}\\
\dfrac{E_\text{II}}{E_\text{I}}&=\dfrac{1}{2}(1+\beta)\left[1-(1-\beta)^2\dfrac{e^{i\alpha}-e^{-i\alpha}}{(1-\beta)^2e^{i\alpha}-(1+\beta)^2e^{-i\alpha}}\right]\\
\dfrac{E_\text{II}'}{E_\text{I}}&=\dfrac{1}{2}(1-\beta)\left[1-(1+\beta)^2\dfrac{e^{i\alpha}-e^{-i\alpha}}{(1-\beta)^2e^{i\alpha}-(1+\beta)^2e^{-i\alpha}}\right]\\
\dfrac{E_\text{III}}{E_\text{I}}&=\left[1-\dfrac{e^{i\alpha}-e^{-i\alpha}}{e^{i\alpha}-\left(\tfrac{1+\beta}{1-\beta}\right)^2e^{-i\alpha}}\right]e^{i\alpha}
\end{align}$$
---
#### Field Coefficients: Parallel Polarization
The magnetic field is perpendicular to the plane of incidence ($xz$-plane), so $-\hat{y}$. Magnetic field relates to the electric field by $\vec{B}=\tfrac{1}{c/n}\hat{k}\times\vec{E}$. All together, we get the 6 fields:
$$\begin{align}
\vec{B}_\text{I}(\vec{x},t)&=
-\hat{y}\dfrac{E_\text{I}}{c/n}e^{i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} -
\hat{y}\dfrac{E_\text{I}'}{c/n}e^{-i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} \\

\vec{B}_\text{II}(\vec{x},t)&=
-\hat{y}\dfrac{E_\text{II}}{c}e^{i\tfrac{\omega}{c}z\cos\theta_\text{II}} -
\hat{y}\dfrac{E_\text{II}'}{c}e^{-i\tfrac{\omega}{c}z\cos\theta_\text{II}} \\

\vec{B}_\text{III}(\vec{x},t)&=
-\hat{y}\dfrac{E_\text{III}}{c/n}e^{i\tfrac{\omega}{c/n}(z-d)\cos\theta_\text{I}}
\end{align}$$
$$\begin{align}
\vec{E}_\text{I}(\vec{x},t)&=
\left(\hat{z}\sin\theta_\text{I}-\hat{x}\cos\theta_\text{I}\right)E_\text{I}e^{i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} +
\left(\hat{z}\sin\theta_\text{I}+\hat{x}\cos\theta_\text{I}\right)E_\text{I}'e^{-i\tfrac{\omega}{c/n}z\cos\theta_\text{I}} \\

\vec{E}_\text{II}(\vec{x},t)&=
\left(\hat{z}\sin\theta_\text{II}-\hat{x}\cos\theta_\text{II}\right)E_\text{II}e^{i\tfrac{\omega}{c}z\cos\theta_\text{II}} +
\left(\hat{z}\sin\theta_\text{II}+\hat{x}\cos\theta_\text{II}\right)E_\text{II}'e^{-i\tfrac{\omega}{c}z\cos\theta_\text{II}} \\

\vec{E}_\text{III}(\vec{x},t)&=
\left(\hat{z}\sin\theta_\text{I}-\hat{x}\cos\theta_\text{I}\right)E_\text{III}e^{i\tfrac{\omega}{c/n}(z-d)\cos\theta_\text{I}}
\end{align}$$
Since there are no free charges or currents at either interface, we have continuity in the perpendicular components of $\vec{D},\vec{B}$, and parallel components of $\vec{E},\vec{H}$. 


<div style="page-break-before: always;"></div>*PDF next page*


We have two interfaces to consider, so we have 8 total conditions:
$$\begin{align}
\left[\epsilon_\text{I}\vec{E}_\text{I}(\vec{x},t)\cdot\hat{z}\right.&=\left.\epsilon_\text{II}\vec{E}_\text{II}(\vec{x},t)\cdot\hat{z}\right]_{z=0}&\implies&& 
E_\text{I}+E_\text{I}'&=n\dfrac{\epsilon_\text{II}}{\epsilon_\text{I}}\left(E_\text{II}+E_\text{II}'\right)\\

\left[\vec{E}_\text{I}(\vec{x},t)\times\hat{z}\right.&=\left.\vec{E}_\text{II}(\vec{x},t)\times\hat{z}\right]_{z=0}&\implies&& 
\dfrac{\cos\theta_\text{I}}{\cos\theta_\text{II}}\left(E_\text{I}-E_\text{I}'\right)&=E_\text{II}-E_\text{II}'\\

\left[\vec{B}_\text{I}(\vec{x},t)\cdot\hat{z}\right.&=\left.\vec{B}_\text{II}(\vec{x},t)\cdot\hat{z}\right]_{z=0}&\implies&&
0&=0\\

\left[\dfrac{1}{\mu_\text{I}}\vec{B}_\text{I}(\vec{x},t)\times\hat{z}\right.&=\left.\dfrac{1}{\mu_\text{I}}\vec{B}_\text{II}(\vec{x},t)\times\hat{z}\right]_{z=0}&\implies&& 
\dfrac{\mu_\text{II}}{\mu_\text{I}}n\left(E_\text{I}+E_\text{I}'\right)&=E_\text{II}+E_\text{II}'\\

\left[\epsilon_\text{II}\vec{E}_\text{II}(\vec{x},t)\cdot\hat{z}\right.&=\left.\epsilon_\text{III}\vec{E}_\text{III}(\vec{x},t)\cdot\hat{z}\right]_{z=d}&\implies&& 
E_\text{II}e^{i\alpha} +
E_\text{II}'e^{-i\alpha}&=\dfrac{\epsilon_\text{III}
\sin\theta_\text{I}}{\epsilon_\text{II}\sin\theta_\text{II}}E_\text{III}\\

\left[\vec{E}_\text{II}(\vec{x},t)\times\hat{z}\right.&=\left.\vec{E}_\text{III}(\vec{x},t)\times\hat{z}\right]_{z=d}&\implies&& 
E_\text{II}e^{i\alpha}-E_\text{II}'e^{-i\alpha}&=
\dfrac{\mu_\text{II}}{\mu_\text{III}}\dfrac{\cos\theta_\text{I}}{\cos\theta_\text{II}}E_\text{III}\\

\left[\vec{B}_\text{II}(\vec{x},t)\cdot\hat{z}\right.&=\left.\vec{B}_\text{III}(\vec{x},t)\cdot\hat{z}\right]_{z=d}&\implies&&
0&=0\\

\left[\dfrac{1}{\mu_\text{II}}\vec{B}_\text{II}(\vec{x},t)\times\hat{z}\right.&=\left.\dfrac{1}{\mu_\text{III}}\vec{B}_\text{III}(\vec{x},t)\times\hat{z}\right]_{z=d}&\implies&&
E_\text{II}e^{i\alpha} + E_\text{II}'e^{-i\alpha}&=\dfrac{\mu_\text{II}}{\mu_\text{III}}nE_\text{III}
\end{align}$$
For some further simplification, we can assume the following values:
$$\begin{align}
\epsilon_\text{I}&=\epsilon_\text{III}=\epsilon & \epsilon_\text{II}=\epsilon_0\\
\mu_\text{I}&=\mu_\text{III}=\mu & \mu_\text{II}=\mu_0\\
\end{align}$$
Using those and earlier relations for the angles, we have the conditions:
$$\begin{align}
\dfrac{\mu_0}{\mu}n\left(E_\text{I}+E_\text{I}'\right)&=E_\text{II}+E_\text{II}' &
E_\text{II}e^{i\alpha} + E_\text{II}'e^{-i\alpha}&=\dfrac{\mu_0}{\mu}nE_\text{III} \\

\dfrac{\mu}{\mu_0}\dfrac{\beta}{n}\left(E_\text{I}-E_\text{I}'\right)&=E_\text{II}-E_\text{II}' & E_\text{II}e^{i\alpha}-E_\text{II}'e^{-i\alpha}&=\dfrac{1}{n}\beta E_\text{III}
\end{align}$$
where we have these coefficients:
$$\begin{align}
\alpha&=\dfrac{\omega}{c}d\sqrt{1-n^2\sin^2\theta_\text{I}} &&&
\beta&=\dfrac{\mu_0}{\mu}\dfrac{n\cos\theta_\text{I}}{\sqrt{1-n^2\sin^2\theta_\text{I}}}
\end{align}$$
With 4 equations and 5 unknowns, we can rearrange all systems in terms of $E_\text{I}$:
$$\begin{align}
\dfrac{E_\text{I}'}{E_\text{I}}&=\dfrac{\left(1-\dfrac{\mu_0}{\mu}\right)n^2\beta\cos\alpha-i\left(\left(\dfrac{\mu_0}{\mu}\right)^2n^4-\dfrac{\mu}{\mu_0}\beta^2\right)\sin\alpha}{\left(1+\dfrac{\mu_0}{\mu}\right)n^2\beta\cos\alpha-i\left(\left(\dfrac{\mu_0}{\mu}\right)^2n^4+\dfrac{\mu}{\mu_0}\beta^2\right)\sin\alpha}\\
\dfrac{E_\text{III}}{E_\text{I}}&=\dfrac{2n^2\beta}{\left(1+\dfrac{\mu_0}{\mu}\right)n^2\beta\cos\alpha-i\left(\left(\dfrac{\mu_0}{\mu}\right)^2n^4+\dfrac{\mu}{\mu_0}\beta^2\right)\sin\alpha}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 7.3.A
> For linear polarization (both parallel to **and** perpendicular to the plane of incidence), calculate:
 > - The ratio of power transmitted into the second volume to the incident power.
 > - The ratio of power reflected back into the first volume to incident power.

The magnitude squared of the perpendicular polarizations are as follows:
$$\begin{align}
\Aboxed{\left|\dfrac{E_\text{I}'}{E_\text{I}}\right|^2&=\dfrac{4\kappa^2\sin^2\left(\alpha\right)}{1-2\kappa^2\cos\left(2\alpha\right)+\kappa^4}} &&&
\Aboxed{\left|\dfrac{E_\text{III}}{E_\text{I}}\right|^2&=\dfrac{(1-\kappa^2)^2}{1-2\kappa\cos\left(2\alpha\right)+\kappa^4}}
\end{align}$$
For the parallel polarizations, we have the ratios:
$$\begin{align}
\Aboxed{\left|\dfrac{E_\text{III}}{E_\text{I}}\right|^2&=\dfrac{4n^4\beta^2}{\left(\tfrac{\mu_0}{\mu}+1\right)^2n^4\beta^2\cos^2\alpha+\left(\left(\tfrac{\mu_0}{\mu}\right)^2n^4+\tfrac{\mu}{\mu_0}\beta^2\right)^2\sin^2\alpha}}\\
\Aboxed{\left|\dfrac{E_\text{I}'}{E_\text{I}}\right|^2&=\dfrac{m^2\left(1-m\right)^2n^4\beta^2\cos^2\alpha+\left(m^3n^4-\beta^2\right)^2\sin^2\alpha}{m^2\left(1+m\right)^2n^4\beta\cos^2\alpha+\left(m^3n^4+\beta^2\right)^2\sin^2\alpha}}
\end{align}$$
With the constants to simplify things:
$$\begin{align}
\alpha&=\dfrac{\omega}{c}d\sqrt{1-n^2\sin^2\theta_\text{I}} &&&
\beta&=\dfrac{\mu_0}{\mu}\dfrac{n\cos\theta_\text{I}}{\sqrt{1-n^2\sin^2\theta_\text{I}}} \\
\kappa&=\dfrac{1+\beta}{1-\beta} &&& m&=\dfrac{\mu_0}{\mu}
\end{align}$$
---
### Question 7.3.B
> For $i$ greater than the critical angle for total internal reflection, sketch the ratio of transmitted power to incident power as a function of $d$ measured in units of wavelength in the gap.

I can't be bothered. This homework is way too much work for literally nothing.


<div style="page-break-before: always;"></div>*PDF next page*

## Question 7.4
> A plane-polarized electromagnetic wave of frequency $\omega$ in free space is normally incident on the flat surface of a nonpermeable medium of conductivity $\sigma$ and dielectric constant $\epsilon$.


<div style="page-break-before: always;"></div>*PDF next page*

### Question 7.4.A
> Calculate the amplitude and phase of the reflected wave relative to the incident wave for arbitrary $\sigma$ and $\epsilon$.


<div style="page-break-before: always;"></div>*PDF next page*

### Question 7.4.B
> Discuss the limiting cases of a very poor and a very good conductor, and show that for a good conductor the reflection coefficient (ratio of reflected to incident intensity) is approximately:
> $$\begin{align}
R&\simeq1-2\dfrac{\omega}{c}\delta
\end{align}$$
> where $\delta$ is the skin depth.


<div style="page-break-before: always;"></div>*PDF next page*

## Question 7.6
> A plane wave of frequency $\omega$ is normally incident from vacuum on a semi-infinite slab of material with a *complex* index of refraction $n(\omega)$, where $n^2(\omega)=\epsilon(\omega)/\epsilon_0$.

---
### Question 7.6.A
> Show that the ratio of reflected power to incident power is
> $$\begin{align}
R&=\left|\dfrac{1-n(\omega)}{1+n(\omega)}\right|^2
\end{align}$$
> while the ratio of power transmitted into the medium to the incident power is
> $$\begin{align}
T&=\dfrac{4\Re\left(n(\omega)\right)}{|1+n(\omega)|^2}
\end{align}$$


<div style="page-break-before: always;"></div>*PDF next page*

### Question 7.6.B
> Evaluate $\Re\left[\tfrac{i\omega}{2}(\vec{E}\cdot\vec{D}^*-\vec{B}\cdot\vec{H}^*)\right]$ as a function of $(x,y,z)$. Show that this rate of change of energy per unit volume accounts for the relative transmitted power $T$.


<div style="page-break-before: always;"></div>*PDF next page*

### Question 7.6.C
> For a conductor, with $n^2=1+i(\sigma/\omega\epsilon_0)$, $\sigma\in\mathbb{R}$, write out the results of [[#Question 7.6.A|part a]] and [[#Question 7.6.B|part b]] in the limit $\epsilon_0\omega\ll\sigma$. Express your answer in terms of $\delta$ as much as possible. Calculate $\tfrac{1}{2}\Re\left(\vec{J}^*\cdot\vec{E}\right)$ and compare with the result of [[#Question 7.6.B|part b]]. Do both enter the complex form of Poynting's theorem?


<div style="page-break-before: always;"></div>*PDF next page*

## Question 7.12
> The time dependence of the electrical disturbances in good conductors is governed by the frequency-dependent conductivity (7.58). Consider longitudinal electric fields in a conductor, using Ohm's law, the continuity equation, and the differential form of Coulomb's law.

---
### Question 7.12.A
> Show that the time-Fourier-transformed charge density satisfies the equation
> $$\begin{align}
\left[\sigma(\omega)-i\omega\epsilon_0\right]\rho(\vec{x},\omega)&=0
\end{align}$$


<div style="page-break-before: always;"></div>*PDF next page*

### Question 7.12.B
> Using the representation $\sigma(\omega)=\sigma_0/(1-i\omega\tau)$, where $\sigma_0=\epsilon_0\omega_p^2\tau$ and $\tau$ is a damping time, show that in the approximation $\omega_p\tau\gg1$ any disturbance will oscillate with the plasma frequency and decay in amplitude with decay constant $\lambda=1/2\tau$. Note that if you use $\sigma(\omega)\simeq\sigma(0)=\sigma_0$ in [[#Question 7.12.A|part a]], you will find no oscillations and extremely rapid damping with the (wrong) decay constant $\lambda_w=\sigma_0/\epsilon_0$.
