**Author:** Stanley Goodwin
**Date:** April 2nd, 2026

---
## Question 10.1
---
### Question 10.1.A
> Show that, for arbitrary initial polarization, the scattering cross section of a perfectly conducting sphere of radius $a$ (summed over outgoing polarizations) is given in the IR limit by
> $$\begin{align}
\dfrac{d\sigma}{d\Omega}\left(\hat{\epsilon}_0,\hat{n}_0,\hat{n}\right)&=k^4a^6\left[\dfrac{5}{4}-|\hat{\epsilon}_0\cdot\hat{n}|^2-\dfrac{1}{4}\left|\hat{n}\cdot(\hat{n}_0\times\hat{\epsilon}_0)\right|^2-\hat{n}_0\cdot\hat{n}\right]
\end{align}$$
> where $\hat{n}_0$ and $\hat{n}$ are the directions of the incident and scattered radiations, respectively, while $\hat{\epsilon}_0$ is the (perhaps complex) unit polarization vector of the incident radiation.

I'm so done doing lots of math and being explicit about all these extra cofactors. Instead, I will describe literally exactly what I am required to do and just take large jumps like Jackson does.

Assume that Jackson means "long wavelength" to mean that $\lambda\gg a$. Therefore, $ka\ll1$. Relative to the sphere, the fields are effectively uniform. Since it is a perfectly conducting sphere, the charges rearrange much faster to form a dipole than the period of the incoming wave. Thus, we have:
$$\begin{align}
\vec{p}&=4\pi\epsilon_0a^3E_0\hat{\epsilon}_0 &&& \vec{m}&=-2\pi \epsilon_0a^3cE_0\left(\hat{n}_0\times\hat{\epsilon}_0\right)
\end{align}$$
The electric field of this sphere is then calculated as our IR limit dipole field:
$$\begin{align}
\vec{E}_\text{sc}(\vec{r})&=\dfrac{1}{4\pi\epsilon_0}\left[k^2\dfrac{e^{ikr}}{r}(\hat{n}\times\vec{p})\times\hat{n}\right]
\end{align}$$
Substituting in our value for our dipole moment, we get:
$$\begin{align}
\vec{E}_\text{sc}(\vec{r})&=k^2a^3E_0\dfrac{e^{ikr}}{r}(\hat{n}\times\hat{\epsilon}_0)\times\hat{n}=k^2a^3E_0\dfrac{e^{ikr}}{r}\left[\hat{\epsilon}_0-(\hat{n}\cdot\hat{\epsilon}_0)\hat{n}\right]
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


This vector term in the back can be averaged over all polarizations, which is the plane perpendicular to $\hat{n}$. Power is related to the intensity, which is in terms of the field squared:
$$\begin{align}
\dfrac{|\vec{E}_\text{sc}|^2}{E_0^2}&=\dfrac{k^4a^6}{r^2}\left[1-|\hat{n}\cdot\hat{\epsilon}_0|^2\right]
\end{align}$$
The rest is just projective algebra to get it in terms of all three unit direction vectors, as well as multiplying by $r^2/|E_0|^2$ for the correct units of power, and so:
$$\begin{align}
\Aboxed{\dfrac{d\sigma}{d\Omega}&=k^4a^6\left[\dfrac{5}{4}-|\hat{\epsilon}_0\cdot\hat{n}|^2-\dfrac{1}{4}\left|\hat{n}\cdot(\hat{n}_0\times\hat{\epsilon}_0)\right|^2-\hat{n}_0\cdot\hat{n}\right]}
\end{align}$$
---
### Question 10.1.B
> If the incident radiation is linearly polarized, show that the cross section is
> $$\begin{align}
\dfrac{d\sigma}{d\Omega}\left(\hat{\epsilon}_0,\hat{n}_0,\hat{n}\right)&=k^4a^6\left[\dfrac{5}{8}\left(1+\cos^2\theta\right)-\cos\theta-\dfrac{3}{8}\sin^2\theta\cos2\phi\right]
\end{align}$$
> where $\hat{n}\cdot\hat{n}_0=\cos\theta$, and the azimuthal angle $\phi$ is measured from the linear polarization.

With the given definitions, we have the three unit direction vectors (without loss of generality):
$$\begin{align}
\hat{n}_0&=\hat{z} & \hat{n}&=\hat{x}\sin\theta+\hat{z}\cos\theta & \hat{\epsilon}_0&=\hat{x}\cos\phi+\hat{y}\sin\phi
\end{align}$$
We can find the three products useful later as:
$$\begin{align}
|\hat{\epsilon}_0\cdot\hat{n}|&=\sin\theta\cos\phi & 
|\hat{n}\cdot(\hat{n}_0\times\hat{\epsilon}_0)|&=\sin\theta\sin\phi &
|\hat{n}_0\cdot\hat{n}|=\cos\theta
\end{align}$$
Using the relation from [[#Question 10.1.A|part A]], we find the differential cross section is:
$$\begin{align}
\dfrac{d\sigma}{d\Omega}\left(\hat{\epsilon}_0,\hat{n}_0,\hat{n}\right)
&=k^4a^6\left[\dfrac{5}{4}-\sin^2\theta\cos^2\phi-\dfrac{1}{4}\sin^2\theta\sin^2\phi-\cos\theta\right]
\end{align}$$
After some trigonometric identities, we find the expected relation:
$$\begin{align}
\Aboxed{\dfrac{d\sigma}{d\Omega}&=k^4a^6\left[\dfrac{5}{8}\left(1+\cos^2\theta\right)-\cos\theta-\dfrac{3}{8}\sin^2\theta\cos2\phi\right]}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 10.1.C
> What is the ratio of the scattered intensities at $\theta=\pi/2,\phi=0$ and $\theta=\pi/2,\phi=\pi/2$. Explain, physically, in terms of the induced multipoles and their radiation patterns.

Our two cross sections are:
$$\begin{align}
\dfrac{d\sigma}{d\Omega}\left(\tfrac{\pi}{2},0\right)&=k^4a^6\left[\dfrac{5}{8}-\dfrac{3}{8}\right]=\dfrac{1}{4}k^4a^6 &&& \dfrac{d\sigma}{d\Omega}\left(\tfrac{\pi}{2},\tfrac{\pi}{2}\right)&=k^4a^6\left[\dfrac{5}{8}+\dfrac{3}{8}\right]=1k^4a^6
\end{align}$$
Thus, the ratio between these two intensities is:
$$\begin{align}
\Aboxed{\dfrac{I\left(\theta=\tfrac{\pi}{2},\phi=0\right)}{I\left(\theta=\tfrac{\pi}{2},\phi=\tfrac{\pi}{2}\right)}&=\dfrac{1}{4}}
\end{align}$$
The angle $\phi=0$ is in the plane of the dipole axis, thus has weaker radiation. The angle $\phi=\pi/2$ is perpendicular to the dipole axis, and therefore has stronger radiation. 

---
## Question 10.3
> A solid, uniform, sphere of radius $R$ and conductivity $\sigma$ acts as a scatterer of a plane-wave beam of unpolarized radiation of frequency $\omega$, with $\omega R/c\ll1$. The conductivity is large enough that the skin depth $\delta$ is small compared to $R$.

---
### Question 10.3.A
> Justify and use the magnetostatic scalar potential to determine the magnetic field around the sphere, assuming the conductivity is infinite (remembering that $\omega\ne0$).

Similar to the previous problem, the wavelength much larger than the radius of the sphere, so the field is effectively uniform over time (very slow change in field, quasistatic). Therefore, there is very little contribution from displacement currents, so our equations become:
$$\begin{align}
\vec\nabla\times\vec{B}&\approx0 & \vec\nabla\cdot\vec{B}&=0
\end{align}$$
This curl being zero means we can write $\vec{B}$ as a gradient of another field, with the equation:
$$\begin{align}
\vec{B}&=-\vec\nabla\psi &\implies&& \vec\nabla^2\psi&=0
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


This is effectively identical to electrostatics solutions, just with this new field $\psi$. Its solution for our system is the azimuthally symmetric solution of the Laplace equation,
$$\begin{align}
\psi(r,\theta)&=-B_0r\cos\theta+\dfrac{m\cos\theta}{r^2} & (r>R)
\end{align}$$
where $m$ is a constant proportional to the magnetic dipole moment magnitude. We enforce that this magnetic field is zero on the surface of the sphere, and so we have the condition:
$$\begin{align}
B(R)&=0 &\implies&& \dfrac{\partial\psi}{\partial r}(R)&=0
\end{align}$$
This imposes that the value for $m$ must be:
$$\begin{align}
0&=B_0\cos\theta+2\dfrac{m\cos\theta}{R^3} &\implies&& m&=-\dfrac{1}{2}R^3B_0
\end{align}$$
Therefore, the magnetic field outside takes the form:
$$\begin{align}
\vec{B}&=B_0\cos\theta\left[1-\dfrac{R^3}{r^3}\right]\hat{r}-B_0\sin\theta\left[1+\dfrac{R^3}{2r^3}\right]\hat{\theta} & (r>R)
\end{align}$$
We can rearrange this to a more standard form:
$$\begin{align}
\vec{B}&=B_0\left[\hat{r}\cos\theta-\hat{\theta}\sin\theta\right]-\dfrac{\tfrac{1}{2}R^3B_0}{r^3}\left[3\hat{r}\cos\theta-(\hat{r}\cos\theta-\hat{\theta}\sin\theta)\right]\\
\Aboxed{\vec{B}&=B_0\hat{z}-\dfrac{\tfrac{1}{2}R^3B_0}{r^3}\left[3\hat{r}\cos\theta-\hat{z}\right]} & (r>R)
\end{align}$$
---
### Question 10.3.B
> Use the technique of Section $8.1$ to determine the absorption cross section of the sphere. Show that it varies as $\omega^{1/2}$ provided that $\sigma$ is independent from frequency.

Our magnetostatic solution previously has a tangential component of the form:
$$\begin{align}
\vec{B}_\parallel&=-B_0\sin\theta\left[1+\dfrac{R^3}{2r^3}\right]\hat{\theta}
\end{align}$$
Thus the power absorbed per unit area $(8.12)$ is:
$$\begin{align}
\Aboxed{\dfrac{dP}{dA}&=-\dfrac{9}{16}\sqrt{\dfrac{2\mu_c\omega}{\sigma}} B_0^2\sin^2\theta}
\end{align}$$
Exactly as the question states should happen.


<div style="page-break-before: always;"></div>*PDF next page*

## Question 10.4
> An unpolarized wave of frequency $\omega=ck$ is scattered by a *slightly* lossy uniform isotropic dielectric sphere of radius $R$ much smaller than a wavelength. The sphere is characterized by an ordinary real dielectric constant $\epsilon_r$ and a real conductivity $\sigma$. The parameters are such that the skin depth $\delta$ is very *large* compared to the radius $R$.

For a linearly responding dielectric, the permittivity is:
$$\begin{align}
\epsilon&=\epsilon_r\epsilon_0+i\dfrac{\sigma}{\omega}
\end{align}$$
Since our sphere is tiny in relation to the wavelength, our polarization vector is:
$$\begin{align}
\vec{p}&=4\pi\epsilon_0R^3\dfrac{\epsilon_r-1+i\tfrac{\sigma}{\epsilon_0\omega}}{\epsilon_r+2+i\tfrac{\sigma}{\epsilon_0\omega}}\vec{E}_0
\end{align}$$
Or as a sum of real and imaginary numbers, we have:
$$\begin{align}
\Aboxed{\vec{p}&=4\pi\epsilon_0R^3\dfrac{(\epsilon_r-1)(\epsilon_r+2)+(\tfrac{\sigma}{\epsilon_0\omega})^2}{(\epsilon_r+2)^2+(\tfrac{\sigma}{\epsilon_0\omega})^2}\vec{E}_0+i4\pi\epsilon_0R^3\dfrac{3\tfrac{\sigma}{\epsilon_0\omega}}{(\epsilon_r+2)^2+(\tfrac{\sigma}{\epsilon_0\omega})^2}\vec{E}_0}
\end{align}$$
---
### Question 10.4.A
> Calculate the differential and total scattering cross sections.

The differential cross section for a dipole is:
$$\begin{align}
\dfrac{d\sigma}{d\Omega}&=\dfrac{k^4}{16\pi^2\epsilon_0^2}\left|\hat{n}\times(\hat{n}\times\vec{p})\right|^2
\end{align}$$
The polarization squared is as follows:
$$\begin{align}
\left|\vec{p}\right|^2&=(4\pi\epsilon_0R^3)^2\dfrac{(\epsilon_r-1)^2+(\tfrac{\sigma}{\epsilon_0\omega})^2}{(\epsilon_r+2)+(\tfrac{\sigma}{\epsilon_0\omega})^2}E_0^2
\end{align}$$
Substituting, we get that:
$$\begin{align}
\dfrac{d\sigma}{d\Omega}&=k^4R^6\dfrac{(\epsilon_r-1)^2+(\tfrac{\sigma}{\epsilon_0\omega})^2}{(\epsilon_r+2)+(\tfrac{\sigma}{\epsilon_0\omega})^2}\left[1-\left|\hat{n}\cdot\hat{\epsilon}_0\right|^2\right]
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


If the incidence is along $\hat{z}$, and that our light is unpolarized, we get:
$$\begin{align}
\dfrac{d\sigma}{d\Omega}&=\dfrac{k^4R^6}{2}\dfrac{(\epsilon_r-1)^2+(\tfrac{\sigma}{\epsilon_0\omega})^2}{(\epsilon_r+2)+(\tfrac{\sigma}{\epsilon_0\omega})^2}\left[1+\cos^2\theta\right]
\end{align}$$
If we integrate this over the surface of a sphere, we get a factor of $16\pi/3$, and so:
$$\begin{align}
\Aboxed{\sigma_\text{sc}&=\dfrac{8\pi}{3}\dfrac{(\epsilon_r-1)^2+(\tfrac{\sigma}{\epsilon_0\omega})^2}{(\epsilon_r+2)+(\tfrac{\sigma}{\epsilon_0\omega})^2}k^4R^6=\dfrac{8\pi}{3}\dfrac{(\epsilon_r-1)^2+(Z_0\sigma/k)^2}{(\epsilon_r+2)+(Z_0\sigma/k)^2}k^4R^6}
\end{align}$$
---
### Question 10.4.B
> Show that the absorption cross section is
> $$\begin{align}
\sigma_\text{abs}&=12\pi R^2\dfrac{RZ_0\sigma}{(\epsilon_r+2)^2+(Z_0\sigma/k)^2}
\end{align}$$

The absorption cross section is of the form:
$$\begin{align}
\sigma_\text{abs}&=\dfrac{\omega}{\epsilon_0c}\mathrm{Im}(\vec{p}\cdot\vec{E}_0^*)
\end{align}$$
Using the split value for the imaginary part of $\vec{p}$, we get:
$$\begin{align}
\sigma_\text{abs}&=\dfrac{\omega}{\epsilon_0c}4\pi\epsilon_0R^3\dfrac{3\tfrac{\sigma}{\epsilon_0\omega}}{(\epsilon_r+2)^2+(\tfrac{\sigma}{\epsilon_0\omega})^2}\\
&=12\pi R^2\dfrac{R\tfrac{\sigma}{\epsilon_0\omega}\tfrac{\omega}{c}}{(\epsilon_r+2)^2+(\tfrac{\sigma}{\epsilon_0\omega})^2}\\
\Aboxed{\sigma_\text{abs}&=12\pi R^2\dfrac{RZ_0\sigma}{(\epsilon_r+2)^2+(Z_0\sigma/k)^2}}
\end{align}$$
Exactly as expected.


<div style="page-break-before: always;"></div>*PDF next page*

### Question 10.4.C
From [[#Question 10.4.A|part a]], write down the forward scattering amplitude and use the optical theorem to evaluate the total cross section. Compare your answer with the sum of the scattering and absorption cross sections from [[#Question 10.4.A|part a]] and [[#Question 10.4.B|part b]]. Comment.

The forward scattering amplitude is:
$$\begin{align}
f(0)&=\dfrac{k^2}{4\pi\epsilon_0}\left(\hat{\epsilon}_0\cdot\vec{p}\right)&\implies&&
f(0)&=k^2R^3\dfrac{\epsilon_r-1+i\tfrac{\sigma}{\epsilon_0\omega}}{\epsilon_r+2+i\tfrac{\sigma}{\epsilon_0\omega}}
\end{align}$$
The optical theorem has the form:
$$\begin{align}
\sigma_\text{ext}&=\dfrac{4\pi}{k}\mathrm{Im} f(0) &\implies&& \sigma_\text{ext}&=4\pi kR^3\dfrac{3\tfrac{\sigma}{\epsilon_0\omega}}{(\epsilon_r+2)^2+(\tfrac{\sigma}{\epsilon_0\omega})^2}
\end{align}$$
After substituting in $Z_0$ and $k=\omega/c$, this reduces exactly to our absorption scattering:
$$\begin{align}
\Aboxed{\sigma_\text{ext}&\simeq\sigma_\text{abs}}
\end{align}$$


As for adding both cross sections together, we get:
$$\begin{align}
\sigma_\text{sc}+\sigma_\text{abs}&=\dfrac{8\pi}{3}\dfrac{(\epsilon_r-1)^2+(Z_0\sigma/k)^2}{(\epsilon_r+2)+(Z_0\sigma/k)^2}k^4R^6+12\pi R^2\dfrac{RZ_0\sigma}{(\epsilon_r+2)^2+(Z_0\sigma/k)^2}\\
&=\dfrac{\pi}{3}R^3\dfrac{8(\epsilon_r-1)^2k^4R^3+(36 Z_0)\sigma+(8Z_0^2k^2R^3)\sigma^2}{(\epsilon_r+2)+(Z_0\sigma/k)^2}\\
\end{align}$$
For small losses, the extinction is pretty much identical to the absorption. Since this is a little sphere of almost no losses, the total extinction is pretty much only in absorption, and very little contribution of scattering exists. The equation is painful, but in the end it mostly has the contribution from the absorption.
