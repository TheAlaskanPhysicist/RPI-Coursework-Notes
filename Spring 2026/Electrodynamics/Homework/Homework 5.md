Author: Stanley Goodwin
Date: March 26th, 2026

---
## Question 9.1
> A common textbook example of a radiating system (see [[#Question 9.2|Problem 9.2]] is a configuration of charges fixed relative to each other but in rotation. The charge density is obviously a function of time, but it is not in the form of $(\text{9.1})$.
> $$\begin{align}
\rho(\vec{x},t)&\ne\rho(\vec{x})e^{-i\omega t} & 
\vec{J}(\vec{x},t)&\ne\vec{J}(\vec{x})e^{-i\omega t} &
\text{(The Negation of 9.1)}
\end{align}$$

Well like all rotation problems, we will define our axis of rotation to be the $z$-axis.

---
### Question 9.1.A
> Show that, for orbiting charges, one alternative is to calculate *real* time-dependent multipole moments using $\rho(\vec{x},t)$ directly, and then compute the multipole moments for a given harmonic frequency with the convention of $(\text{9.1})$ by inspection or Fourier decomposition of the time-dependent moments. Note that care must be taken when calculating $q_{lm}(t)$ to form linear combinations that are real before making this connection.

For a general charge distribution $\rho(\vec{x},t)$, we can represent this in Fourier space as
$$\begin{align}
&&\rho(\vec{x},\omega)&=\int_{-\infty}^\infty e^{i\omega t}\rho(\vec{x},t)\ dt\\
\implies&&\rho(\vec{x},t)&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}\rho(\vec{x},\omega)\ d\omega
\end{align}$$
where $\omega$ is the Fourier conjugate of time (angular frequency). So that our later sections are much more simple to compute, note that the sign of the exponentials are reversed from convention.

Our integral expression for the multipole moment $q_{lm}(t)$ is in terms of spherical harmonics:
$$\begin{align}
q_{lm}(t)&=\int Y_{lm}^*(\theta,\phi)r^{l}\rho(\vec{x},t)\ d^3x
\end{align}$$
<div style="page-break-before: always;"></div>


Using charge density represented in Fourier space, we can rearrange to the following form:
$$\begin{align}
&& q_{lm}(t)&=\int Y_{lm}^*(\theta,\phi)r^{l}\left[\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}\rho(\vec{x},\omega)\ d\omega\right]\ d^3x \\
\implies&&
q_{lm}(t)&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}\left[\int Y_{lm}^*(\theta,\phi)r^{l}\ \rho(\vec{x},\omega)\ d^3x\right]\ d\omega
\end{align}$$
The inner integral is the Fourier conjugate of the multipole moment $q_{lm}(\omega)$, and so:
$$\begin{align}
\Aboxed{q_{lm}(t)&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}q_{lm}(\omega)\ d\omega}
&&& q_{lm}(\omega)&=\int r^{l}Y_{lm}^*(\theta,\phi)\ \rho(\vec{x},\omega)\ d^3x
\end{align}$$
---
### Question 9.1.B
> Consider a charge density $\rho(\vec{x},t)$ that is periodic in time, with period $T=2\pi/\omega_0$. By making a Fourier *series* expansion, show that it can be written as:
> $$\begin{align}
\rho(\vec{x},t)&=\rho_0(\vec{x})
+\sum_{n=1}^\infty\Re\left[2\rho_n(\vec{x})e^{-in\omega_0t}\right] &&& \rho_n(\vec{x})&=\dfrac{1}{T}\int_0^T\rho(\vec{x},t)e^{in\omega_0t}\ dt
\end{align}$$
> This shows explicitly how to establish connection with $(\text{9.1})$.

For a charge density that is periodic, $\rho(\vec{x},t)=\rho(\vec{x},t+T)$, the Fourier transform can be split into the sum of the integrals over time spanning one period:
$$\begin{align}
\rho(\vec{x},\omega)&=\int_{-\infty}^\infty e^{i\omega t}\rho(\vec{x},t)\ dt=\sum_{n=-\infty}^\infty\int_{nT}^{(n+1)T} e^{i\omega t}\rho(\vec{x},t)\ dt
\end{align}$$
Suppose we reindex time as $\tau=t-nT\iff t=\tau+nT$, then we have:
$$\begin{align}
\rho(\vec{x},\omega)&=\sum_{n=-\infty}^\infty\int_{0}^{T} e^{i\omega (\tau+nT)}\rho(\vec{x},\tau+nT)\ d\tau
\end{align}$$
We can reduce the charge density using our periodicity condition, and simplify to:
$$\begin{align}
\rho(\vec{x},\omega)&=\int_{0}^{T} e^{i\omega\tau}\rho(\vec{x},\tau)\ d\tau\cdot \sum_{n=-\infty}^\infty e^{in\omega T}
\end{align}$$
The summation can be expanded in terms of Dirac delta functions as:
$$\begin{align}
\rho(\vec{x},\omega)&=\int_{0}^{T} e^{i\omega\tau}\rho(\vec{x},\tau)\ d\tau\cdot\dfrac{2\pi}{T}\sum_{n=-\infty}^\infty\delta(\omega-n\omega_0)
\end{align}$$
<div style="page-break-before: always;"></div>


This selects certain choice of $\omega$, so we can bring the integral inside and reduce:
$$\begin{align}
\rho(\vec{x},\omega)&=2\pi\sum_{n=-\infty}^\infty\delta(\omega-n\omega_0)\dfrac{1}{T}\int_{0}^{T} e^{in\omega_0\tau}\rho(\vec{x},\tau)\ d\tau
\end{align}$$
Using the standard definition for Fourier series coefficients, we get the final Fourier transform:
$$\begin{align}
\rho(\vec{x},\omega)&=2\pi\sum_{n=-\infty}^\infty\rho_n(\vec{x})\delta(\omega-n\omega_0) & 
\rho_n(\vec{x})&=\dfrac{1}{T}\int_{0}^{T} e^{in\omega_0\tau}\rho(\vec{x},\tau)\ d\tau
\end{align}$$
Now we can use the inverse Fourier transform on the delta functions to arrive at:
$$\begin{align}
\rho(\vec{x},t)&=\sum_{n=-\infty}^\infty\rho_n(\vec{x}) e^{-in\omega_0 t}
\end{align}$$
To get the expression we would like, we can split the summation into 3 parts:
$$\begin{align}
\rho(\vec{x},t)&=\rho_0(\vec{x})+\sum_{n=1}^\infty\left(\rho_n(\vec{x})e^{-in\omega_0 t}+\rho_{-n}(\vec{x}) e^{+in\omega_0 t}\right)
\end{align}$$
The exponentials can be expanded using Euler's formula so that in total:
$$\begin{align}
\rho(\vec{x},t)&=\rho_0(\vec{x})+\sum_{n=1}^\infty\left(\rho_n(\vec{x})+\rho_{-n}(\vec{x})\right)\cos\left(n\omega_0 t\right)-i\sum_{n=1}^\infty\left(\rho_n(\vec{x})-\rho_{-n}(\vec{x})\right)\sin\left(n\omega_0 t\right)
\end{align}$$
In order for the charge density to be real, $\rho_n(\vec{x})=\rho_{-n}^*(\vec{x})$ must be satisfied:
$$\begin{align}
\rho(\vec{x},t)&=\rho_0(\vec{x})+\sum_{n=1}^\infty 2\rho_n(\vec{x})\cos\left(n\omega_0 t\right)
\end{align}$$
Lastly, $\cos$ is the real part of the complex exponential, and so we can write finally:
$$\begin{align}
\Aboxed{\rho(\vec{x},t)&=\rho_0(\vec{x})
+\sum_{n=1}^\infty\Re\left[2\rho_n(\vec{x})e^{-in\omega_0t}\right]} &&& 
\Aboxed{\rho_n(\vec{x})&=\dfrac{1}{T}\int_0^Te^{in\omega_0t}\rho(\vec{x},t)\ dt}
\end{align}$$
<div style="page-break-before: always;"></div>


### Question 9.1.C
> For a single charge $q$ rotating about the origin in the $xy$-plane in a circle of radius $R$ and constant angular speed $\omega_0$, calculate the $l=0$ and $l=1$ multipole moments by the methods of parts [[#Question 9.1.A|A]] and [[#Question 9.1.B|B]] and compare. In method [[#Question 9.1.B|B]], express the charge density $\rho_n(\vec{x})$ in cylindrical coordinates. Are there higher multipoles, for example, quadrupole? At what frequencies.

For solving in the method used in [[#Question 9.1.A|Problem 9.1.A]], we can write the charge density as:
$$\begin{align}
\rho(\vec{x},t)&=\dfrac{q}{R^2}\delta(r-R)\delta(\theta-\pi/2)\delta(\phi-[\omega_0t+\phi_0])
\end{align}$$
The charge density in frequency space is then:
$$\begin{align}
\rho(\vec{x},\omega)
&=\dfrac{q}{R^2}\delta(r-R)\delta(\theta-\pi/2)\int_{-\infty}^\infty e^{i\omega t}\delta(\phi-[\omega_0t+\phi_0])\ dt\\
&=\dfrac{q}{\omega_0R^2}\delta(r-R)\delta(\theta-\pi/2)\int_{-\infty}^\infty e^{i\omega t}\delta\left(t-\dfrac{\phi-\phi_0}{\omega_0}\right)\ dt\\
\rho(\vec{x},\omega)&=\dfrac{q}{\omega_0R^2}e^{i\omega\tfrac{\phi-\phi_0}{\omega_0}}\delta(r-R)\delta(\theta-\pi/2)
\end{align}$$
The multipole moment in frequency space is then:
$$\begin{align}
q_{lm}(\omega)&=\int Y_{lm}^*(\theta,\phi)r^{l}\rho(\vec{x},\omega)\ d^3x\\
&=\dfrac{q}{\omega_0R^2}\int Y_{lm}^*(\theta,\phi)r^{l}e^{i\omega\tfrac{\phi-\phi_0}{\omega_0}}\delta(r-R)\delta(\theta-\pi/2)\ r^2\sin\theta\ dr\ d\theta\ d\phi\\
&=\dfrac{q}{\omega_0}R^{l}\int_0^{2\pi} Y_{lm}^*(\pi/2,\phi)e^{i\omega\tfrac{\phi-\phi_0}{\omega_0}}\ d\phi
\end{align}$$
The spherical harmonics can be written as $Y_{lm}^*(\pi/2,\phi)=K_{lm}e^{-im\phi}$, and so continuing:
$$\begin{align}
q_{lm}(\omega)
&=\dfrac{q}{\omega_0}K_{lm}R^{l}\int_0^{2\pi}e^{-im\phi}e^{i\omega\tfrac{\phi-\phi_0}{\omega_0}}\ d\phi\\
&=\dfrac{q}{\omega_0}K_{lm}R^{l}e^{-i\tfrac{\omega}{\omega_0}\phi_0}\int_0^{2\pi}e^{i\left(\tfrac{\omega}{\omega_0}-m\right)\phi}\ d\phi\\
&=q\dfrac{2\pi}{\omega_0}K_{lm}R^{l}e^{-i\tfrac{\omega}{\omega_0}\phi_0}e^{i\pi\left(\tfrac{\omega}{\omega_0}-m\right)}\dfrac{\sin\left[\pi\left(\tfrac{\omega}{\omega_0}-m\right)\right]}{\pi\left(\tfrac{\omega}{\omega_0}-m\right)}\\
\end{align}$$
Let $z=\pi\left(\tfrac{\omega}{\omega_0}-m\right)$, then our equation becomes:
$$\begin{align}
q_{lm}(\omega)
&=q\dfrac{2\pi}{\omega_0}K_{lm}R^{l}e^{-im\phi_0}e^{iz\left(1-\tfrac{\phi_0}{\pi}\right)}\dfrac{\sin z}{z}
\end{align}$$
<div style="page-break-before: always;"></div>


Now if we take the inverse Fourier transform, we get that:
$$\begin{align}
q_{lm}(t)&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\omega t}q_{lm}(\omega)\ d\omega\\
&=\dfrac{q}{\pi}K_{lm}R^{l}e^{-im\phi_0}\int_{-\infty}^\infty e^{-i\omega_0\left(z/\pi+m\right)t}e^{iz\left(1-\tfrac{\phi_0}{\pi}\right)}\dfrac{\sin z}{z}\ dz\\
&=\dfrac{q}{\pi}K_{lm}R^{l}e^{-im(\omega_0t+\phi_0)}\int_{-\infty}^\infty e^{i\left(1-\tfrac{\omega_0t+\phi_0}{\pi}\right)z}\dfrac{\sin z}{z}\ dz
\end{align}$$
We can use the following substitution and identity:
$$\begin{align}
\phi(t)&=\omega_0t+\phi_0 &&& \int_{-\infty}^\infty e^{i\alpha z}\dfrac{\sin z}{z}\ dz&=\pi\Theta(1-|\alpha|)
\end{align}$$
The multipole reduces to:
$$\begin{align}
q_{lm}(t)&=qK_{lm}R^{l}e^{-im(\omega_0t+\phi_0)}\Theta\left(0<\phi(t)<2\pi\right)
\end{align}$$
However, due to the condition for the angle being periodic in $2\pi$, this spans the entire interval with some interesting behavior exactly when the phase remodulates. Therefore our final equation is:
$$\begin{align}
\Aboxed{q_{lm}(t)&=qK_{lm}R^{l}e^{-im\phi(t)} & \phi(t)&=\omega_0t+\phi_0}
\end{align}$$
Lastly, our coefficient out the front is a pain, but it is computable. We have the following:
$$\begin{align}
Y_{lm}(\pi/2,\phi)&=\sqrt{\dfrac{2l+1}{4\pi}\dfrac{(l-m)!}{(l+m)!}}P^m_l(0)e^{-im\phi}\\
P^m_l(0)&=(-1)^{(l+m)/2}\dfrac{(l+m)!}{2^l\left(\tfrac{l+m}{2}\right)!\left(\tfrac{l-m}{2}\right)!}
\end{align}$$
All together, the coefficient is given by the following:
$$\begin{align}
K_{lm}&=(-1)^{(l+m)/2}\sqrt{\dfrac{2l+1}{4\pi}}\dfrac{\sqrt{(l-m)!(l+m)!}}{2^l\left(\tfrac{l+m}{2}\right)!\left(\tfrac{l-m}{2}\right)!} & (l+m\in\text{Even})
\end{align}$$
This coefficient is $0$ if $l+m$ is $\text{Odd}$. Otherwise the relation holds. Therefore our final solution is:
$$\begin{align}
\Aboxed{q_{lm}(t)&=q(-1)^{(l+m)/2}\sqrt{\dfrac{2l+1}{4\pi}}\dfrac{\sqrt{(l-m)!(l+m)!}}{\left(\tfrac{l-m}{2}\right)!\left(\tfrac{l+m}{2}\right)!}\left(\dfrac{R}{2}\right)^le^{-im\phi(t)}}
\end{align}$$
For $l=0$, this equation reduces to:
$$\begin{align}
\Aboxed{q_{00}(t)&=q\sqrt{\dfrac{1}{4\pi}}}
\end{align}$$
For $l=1$, only $m\pm1$ results in non-zero multipole coefficients, and so:
$$\begin{align}
\Aboxed{q_{1,0}(t)=0}&&&\Aboxed{q_{1,\pm1}(t)&=\mp qR\sqrt{\dfrac{3}{8\pi}}e^{\mp i\phi(t)}}
\end{align}$$
For $l\ge2$, we only non-zero coefficients when $l+m$ is an even number. 
$$\begin{align}
\Aboxed{q_{l,0}(t)&=q(-1)^{l/2}\sqrt{\dfrac{2l+1}{4\pi}}\binom{l}{l/2}\left(\dfrac{R}{2}\right)^l,\ \ \ \ \ l\in 2\mathbb{N}}\\
\Aboxed{q_{l,\pm m}(t)&=q(\pm1)^{m}(-1)^{(l+m)/2}\sqrt{\dfrac{2l+1}{4\pi}}\dfrac{\sqrt{(l-m)!(l+m)!}}{\left(\tfrac{l-m}{2}\right)!\left(\tfrac{l+m}{2}\right)!}\left(\dfrac{R}{2}\right)^le^{\mp im\phi(t)},\ \ \ \ \ (l+m)\in 2\mathbb{N}}
\end{align}$$
For some higher-order terms, we have:
$$\begin{align}
q_{2,0}(t)&=-qR^2\sqrt{\dfrac{5}{16\pi}} & 
q_{2,\pm 2}(t)&=+qR^2\sqrt{\dfrac{15}{32\pi}}e^{\mp i2\phi(t)} \\

q_{4,0}(t)&=+qR^4\sqrt{\dfrac{81}{256\pi}} &
q_{4,\pm 2}(t)&=-qR^4\sqrt{\dfrac{45}{128\pi}}e^{\mp 2i\phi(t)} \\ &&
q_{4,\pm 4}(t)&=+qR^4\sqrt{\dfrac{315}{512\pi}}e^{\mp 4i\phi(t)} \\

q_{6,0}(t)&=-qR^6\sqrt{\dfrac{325}{1024\pi}} &
q_{6,\pm2}(t)&=+qR^6\sqrt{\dfrac{1365}{4096\pi}}e^{\mp i2\phi(t)} \\
q_{6,\pm4}(t)&=-qR^6\sqrt{\dfrac{819}{2048\pi}}e^{\mp i4\phi(t)} &
q_{6,\pm6}(t)&=+qR^6\sqrt{\dfrac{3003}{4096\pi}}e^{\mp i6\phi(t)}
\end{align}$$
$$\begin{align}
q_{3,\pm 1}(t)&=\pm qR^3\sqrt{\dfrac{21}{64\pi}}e^{\mp i\phi(t)} &
q_{3,\pm 3}(t)&=\mp qR^3\sqrt{\dfrac{35}{64\pi}}e^{\mp i3\phi(t)} \\

q_{5,\pm 1}(t)&=\mp qR^5\sqrt{\dfrac{165}{512\pi}}e^{\mp i\phi(t)} &
q_{5,\pm 3}(t)&=\pm qR^5\sqrt{\dfrac{385}{1024\pi}}e^{\mp i3\phi(t)} \\ &&
q_{5,\pm 5}(t)&=\mp qR^5\sqrt{\dfrac{693}{1024\pi}}e^{\mp i5\phi(t)}
\end{align}$$
So yes, there are high-order multipoles, and they are of increasing harmonics of the original frequency $\omega_0$, since $\phi(t)=\phi_0+\omega_0t$. It is the exact same procedure with the other system, and I will not do all that again, so I apologize.
<div style="page-break-before: always;"></div>



## Question 9.2
> A radiating quadrupole consists of a square of side $a$ with charges $\pm q$ at alternate corners. The square rotates with angular velocity $\omega$ about an axis normal to the plane of the square and through its center. Calculate the quadrupole moments, the radiation fields, the angular distribution of radiation, and the total radiated power, all in the long-wavelength approximation. What is the frequency of this radiation?

Well I can use [[#Question 9.1.C]] to very quickly answer this. The multipole tensor for an individual particle at radius $R$ and in the $xy$-plane with angular velocity $\omega_0$ is:
$$\begin{align}
q_{lm}(t)&=qR^{l}K_{lm}e^{-im\phi(t)} & \phi(t)&=\omega_0t+\phi_0
\end{align}$$
We have 4 particles at radius $R=a/\sqrt{2}$, frequency $\omega$, with alternating charges and $\pi/2$ relative angles to each other. Therefore our system is can be written as:
$$\begin{align}
q_{lm}(t)&=q\dfrac{a^{l}}{2^{l/2}}K_{lm}\left(e^{-im0}-e^{-im\pi/2}+e^{-im\pi}-e^{-im3\pi/2}\right)e^{-im\omega_0t}\\
&=q\dfrac{a^{l}}{2^{l/2}}K_{lm}\left(1+(-1)^m-(-i)^m-(i)^m\right)e^{-im\omega_0t}\\
&=q\dfrac{a^{l}}{2^{l/2}}K_{lm}(1-i^m)\left(1+(-1)^m\right)e^{-im\omega_0t}
\end{align}$$
This simplifies immensely under the right conditions. It is only non-zero when $m\equiv2\mod4$, and from the coefficient we also have $l+m\equiv0\mod 2$, and then can be written as:
$$\begin{align}
q_{lm}(t)&=q\dfrac{4a^{l}}{2^{l/2}}K_{lm}e^{-im\omega_0t}, & m&\equiv2\mod4, & l&\equiv0\mod2
\end{align}$$
So for our system, the largest contribution will be the quadrupole components:
$$\begin{align}
\Aboxed{q_{2,\pm2}(t)&=2qa^{2}\sqrt{\dfrac{15}{32\pi}}e^{\mp i2\omega_0t} \ \ \ \ \ q_{2,0}(t)=q_{2,\pm1}(t)=0}
\end{align}$$
The quadrupole moment tensor, using our components, is:
$$\begin{align}
Q_{xx}(t)&=2qa^{2}\sqrt{\dfrac{15}{32\pi}}\sqrt{\dfrac{8\pi}{15}}\cos\left(2\omega_0t\right) &
Q_{xy}(t)&=-2qa^{2}\sqrt{\dfrac{15}{32\pi}}\sqrt{\dfrac{8\pi}{15}}\sin\left(2\omega_0t\right)
\\
Q_{yx}(t)&=-2qa^{2}\sqrt{\dfrac{15}{32\pi}}\sqrt{\dfrac{8\pi}{15}}\sin\left(2\omega_0t\right)&
Q_{yy}(t)&=-2qa^{2}\sqrt{\dfrac{15}{32\pi}}\sqrt{\dfrac{8\pi}{15}}\cos\left(2\omega_0t\right)
\end{align}$$
With all other components being zero. As a matrix, we can write this as:
$$\begin{align}
Q^{(2)}(t)&=qa^{2}\begin{bmatrix}
\cos\left(2\omega_0t\right)&-\sin\left(2\omega_0t\right)&0\\
-\sin\left(2\omega_0t\right)&-\cos\left(2\omega_0t\right)&0\\ 0&0&0
\end{bmatrix}
\end{align}$$
As a quadrupole vector, we can write:
$$\begin{align}
\vec{Q}(\hat{r},t)&=Q_{xx}\left[(\hat{x}\cdot\hat{r})\hat{x}-(\hat{y}\cdot\hat{r})\hat{y}\right]+Q_{xy}\left[(\hat{x}\cdot\hat{r})\hat{x}+(\hat{y}\cdot\hat{r})\hat{y}\right]
\end{align}$$
Or in spherical form:
$$\begin{align}
\vec{Q}(\hat{r},t)&=\left[Q_{xx}\cos2\phi+Q_{xy}\right]\sin^2\theta\ \hat{r}+\left[Q_{xx}\cos2\phi+Q_{xy}\right]\sin\theta\cos\theta\ \hat{\theta}-Q_{xy}\sin\theta\sin2\phi\ \hat{\phi}
\end{align}$$
The first cross product becomes the following:
$$\begin{align}
\hat{r}\times\vec{Q}&=\left[Q_{xx}\cos2\phi+Q_{xy}\right]\sin\theta\cos\theta\ \hat{\phi}+Q_{xy}\sin\theta\sin2\phi\ \hat{\theta}
\end{align}$$
The second cross product is:
$$\begin{align}
\left(\hat{r}\times\vec{Q}\right)\times\hat{r}&=\left[Q_{xx}\cos2\phi+Q_{xy}\right]\sin\theta\cos\theta\ \hat{\theta}-Q_{xy}\sin\theta\sin2\phi\ \hat{\phi}
\end{align}$$
The two electromagnetic fields are:
$$\begin{align}
c\vec{B}(\vec{r},t)&=\dfrac{k^3}{24\pi\epsilon_0}\dfrac{e^{ikr}}{r}\left(\left[Q_{xx}\cos2\phi+Q_{xy}\right]\sin\theta\cos\theta\ \hat{\phi}+Q_{xy}\sin\theta\sin2\phi\ \hat{\theta}\right)\\
\vec{E}(\vec{r},t)&=\dfrac{k^3}{24\pi\epsilon_0}\dfrac{e^{ikr}}{r}\left(\left[Q_{xx}\cos2\phi+Q_{xy}\right]\sin\theta\cos\theta\ \hat{\theta}-Q_{xy}\sin\theta\sin2\phi\ \hat{\phi}\right)\\
\end{align}$$
The cross product between them is:
$$\begin{align}
\vec{E}(\vec{r},t)\times c\vec{B}^*(\vec{r},t)&=\dfrac{k^6}{24^2\pi^2\epsilon_0^2r^2}\sin^2\theta\left(\left[Q_{xx}\cos2\phi+Q_{xy}\right]^2\cos^2\theta+Q_{xy}^2\sin^22\phi\right)\hat{r}
\end{align}$$
The power per unit solid angle $(9.21)$ is then:
$$\begin{align}
\dfrac{dP}{d\Omega}&=\dfrac{c\epsilon_0}{2}r^2\ \Re \left[\hat{r}\cdot\left(\vec{E}\times c\vec{B}^*\right)\right]\\
&=\dfrac{ck^6}{24^2\pi^2\epsilon_0}\sin^2\theta\left(\left[Q_{xx}\cos2\phi+Q_{xy}\right]^2\cos^2\theta+Q_{xy}^2\sin^22\phi\right)
\end{align}$$
Now we integrate over the whole surface and average over time:
$$\begin{align}
P(t)&=\dfrac{ck^6q^2a^{4}}{4320\pi\epsilon_0}\left(\cos^2\left(2\omega_0t\right)+7\sin^2\left(2\omega_0t\right)\right) &\implies && \Aboxed{\left\langle P\right\rangle&=\dfrac{ck^6q^2a^{4}}{1080\pi\epsilon_0}}
\end{align}$$
From the inside terms, we see that the frequency of the radiation is $\boxed{\omega=2\omega_0}$, and power is:
$$\begin{align}
\Aboxed{\left\langle P\right\rangle&=\dfrac{32}{135}\dfrac{\omega_0^6q^2a^{4}}{4\pi\epsilon_0c^5}}
\end{align}$$
My coefficient seems to disagree with what I can find online, but I can't be bothered to go find where my coefficients get changed. In the end, it's of the right order.



## Question 9.10
> The transitional charge and current densities for the radiative transition from the $m=0$, $2p$ state in hydrogen to the $1s$ ground state are, in the notation of $(9.1)$ and with the neglect of spin,
> $$\begin{align}
\rho(r,\theta,\phi,t)&=\dfrac{2}{\sqrt{6}}\dfrac{e}{a_0^4}re^{-3r/2a_0}Y_{00}Y_{10}e^{-i\omega_0t}\\
\vec{J}(r,\theta,\phi,t)&=-\dfrac{iv_0}{2}\left(\dfrac{\hat{r}}{2}+\dfrac{a_0}{z}\hat{z}\right)\rho(r,\theta,\phi,t)
\end{align}$$
> where $a_0=4\pi\epsilon_0\hbar^2/me^2=0.529\times10^{-10}\text{m}$ is the Bohr radius, $\omega_0=3e^2/32\pi\epsilon_0\hbar a_0$ is the frequency difference of the levels, and $v_0=e^2/4\pi\epsilon_0\hbar=\alpha c$ is the Bohr orbit speed.
<div style="page-break-before: always;"></div>



For reference, the spherical harmonics have the form ([Table Referenced](https://en.wikipedia.org/wiki/Table_of_spherical_harmonics)):
$$\begin{align}
Y_{00}&=\sqrt{\dfrac{1}{4\pi}} &&& 
Y_{10}&=\sqrt{\dfrac{3}{4\pi}}\cos\theta
\end{align}$$
Since we are interested in the vector potential, we can substitute the charge density and spherical harmonics into the current density:
$$\begin{align}
\vec{J}(r,\theta,\phi,t)
&=-\dfrac{iv_0}{2}\left(\dfrac{\hat{r}}{2}+\dfrac{a_0}{z}\hat{z}\right)\dfrac{2}{\sqrt{6}}\dfrac{e}{a_0^4}re^{-3r/2a_0}\sqrt{\dfrac{1}{4\pi}}\sqrt{\dfrac{3}{4\pi}}\dfrac{z}{r}e^{-i\omega_0t}\\
&=-\dfrac{i}{8\pi\sqrt{2}}\dfrac{ev_0}{a_0^4}\left(z\hat{r}+2a_0\hat{z}\right)e^{-3r/2a_0}e^{-i\omega_0t}\\
\end{align}$$
We'll also want to convert the $z,\hat{z}$ in spherical coordinates ([Table Referenced](https://en.wikipedia.org/wiki/Del_in_cylindrical_and_spherical_coordinates)):
$$\begin{align}
\vec{J}(r,\theta,\phi,t)
&=-\dfrac{i}{8\pi\sqrt{2}}\dfrac{ev_0}{a_0^4}\left[\left(z+2a_0\cos\theta\right)\hat{r}-2a_0\sin\theta\ \hat{\theta}\right]e^{-3r/2a_0}e^{-i\omega_0t}
\end{align}$$
---
### Question 9.10.A
> Show that the effective transitional (orbital) "magnetization" is
> $$\begin{align}
\vec{\mathcal{M}}(r,\theta,\phi,t)&=-i\dfrac{\alpha ca_0}{4}\left(\hat{x}\sin\theta-\hat{y}\cos\theta\right)\tan\theta\cdot\rho(r,\theta,\phi,t)
\end{align}$$
> Calculate $\vec\nabla\cdot\mathcal{M}$ and evaluate all the non-vanishing radiation multipoles in the long-wavelength limit.

We can use the equation for magnetization found in $(9.32)$ with our current density:
$$\begin{align}
\mathcal{M}(\vec{r},t)&=\dfrac{1}{2}\vec{r}\times\vec{J}(\vec{r},t) \\
&=-\dfrac{1}{2}r\hat{r}\times\dfrac{iv_0}{2}\left(\dfrac{\hat{r}}{2}+\dfrac{a_0}{z}\hat{z}\right)\rho(\vec{r},t) \\
&=-\dfrac{i\alpha c}{4}r\left(0-\dfrac{a_0}{z}\hat{r}\times\hat{\theta}\sin\theta\right)\rho(\vec{r},t)\\
&=\dfrac{i\alpha c}{4}a_0\left(\dfrac{r}{z}\sin\theta\ \hat{\phi}\right)\rho(\vec{r},t) \\
\Aboxed{\mathcal{M}(\vec{r},t)&=i\dfrac{\alpha ca_0}{4}\tan\theta\ \rho(\vec{r},t)\ \hat{\phi}}
\end{align}$$
This is equivalent to the answer above since $-\hat{\phi}=\hat{x}\sin\theta-\hat{y}\cos\theta$.
<div style="page-break-before: always;"></div>


Since our quantity $\mathcal{M}$ is only dependent on $r$ and $\theta$, and that it only has basis components in $\hat{\phi}$, the divergence is inherently $0$, and so:
$$\begin{align}
\Aboxed{\vec\nabla\cdot\mathcal{M}(\vec{r},t)&=0}
\end{align}$$
This makes calculating the electric multipole coefficients much simpler. It takes the form:
$$\begin{align}
q_{lm}(t)&=\int Y_{lm}^*(\theta,\phi)r^{l}\rho(\vec{r},t)\ d^3r\\
&=\dfrac{2}{\sqrt{6}}\dfrac{e}{a_0^4}e^{-i\omega_0t}\int_0^\infty r^{l+3}e^{-3r/2a_0}\ dr\int Y_{lm}^*Y_{00}Y_{10}\ d\Omega\\
&=\dfrac{2}{\sqrt{6}}\dfrac{e}{a_0^4}\left(\dfrac{2a_0}{3}\right)^{l+4}e^{-i\omega_0t}\int_0^\infty z^{l+3}e^{-z}\ dz\cdot\sqrt{\dfrac{1}{4\pi}}\delta_{l1}\delta_{m0}\\
&=\dfrac{1}{\sqrt{6\pi}}\dfrac{e}{a_0^4}\left(\dfrac{2a_0}{3}\right)^{1+4}e^{-i\omega_0t}(1+3)!\ \delta_{l1}\delta_{m0}\\
\Aboxed{q_{lm}(t)&=\dfrac{2^{15/2}}{3^{9/2}}\dfrac{ea_0}{\sqrt{\pi}}e^{-i\omega_0t} \delta_{l1}\delta_{m0}}
\end{align}$$
The magnetic dipole is also pretty simple, since our $\hat{\phi}$ doesn't accumulate over a period:
$$\begin{align}
\vec{m}&=\int\mathcal{M}(\vec{r},t)\ d^3r\propto\int\hat{\phi}\ d\phi=0 &\implies&& \Aboxed{\vec{m}=0}
\end{align}$$
For the magnetic quadrupole (not sure we need to go out this far), it will be helpful to use the solution given to us since it is in cartesian. There is no $z$-component, so we only need $4$ elements.
$$\begin{align}
M_{jj}&=2\int\left[r_i\mathcal{M}_{i}\right]\ d^3r=2\int\left[x_j\hat{x}_j\cdot i\dfrac{\alpha ca_0}{4}\tan\theta\ \rho(r,\theta,t)\ \hat{\phi}\right]\ d^3r\\
M_{jj}&\propto \int x_j(\phi)\ [\hat{x}_j\cdot\hat{\phi}]\ d\phi\propto \int \sin\left(2\phi\right)\ d\phi \implies \boxed{M_{xx}=M_{yy}=0} \\
M_{ij}=M_{ji}&=\int\left[r_i\mathcal{M}_{j}+r_j\mathcal{M}_{i}\right]\ d^3r\propto\int\left[x\left(\hat{y}\cdot \hat{\phi}\right)+y\left(\hat{x}\cdot \hat{\phi}\right)\right]\ d\phi\\
M_{ij}=M_{ji}&\propto\int\left[\cos^2\phi-\sin^2\phi\right]\ d\phi\propto\int\cos(2\phi)\ d\phi \implies \boxed{M_{xy}=M_{yx}=0}
\end{align}$$
So, like the magnetic dipole, the magnetic quadrupole also vanishes $\boxed{M_{ij}=0}$. A similar case can be made for higher order magnetic multipoles. Therefore, the only multipole that exists is the $z$-component of the electric dipole:
$$\begin{align}
\Aboxed{q_{10}(t)=p_z(t)&=\dfrac{2^{15/2}}{3^{9/2}}\dfrac{ea_0}{\sqrt{\pi}}e^{-i\omega_0t}}
\end{align}$$
<div style="page-break-before: always;"></div>



### Question 9.10.B
> In the electric dipole approximation, calculate the total time-averaged power radiated. Express your answer in units of $(\hbar\omega_0)\cdot(\alpha^4c/a_0)$, where $e^2/4\pi\epsilon_0\hbar c$ is the fine structure constant.

For electric dipole fields in the IR (far field), we can use the equations found in the textbook $(9.19)$:
$$\begin{align}
c\vec{B}&=\dfrac{k^2}{4\pi\epsilon_0}\dfrac{e^{ikr}}{r}\left(\hat{n}\times\vec{p}\right) &&& \vec{E}&=c\vec{B}\times\hat{n}=\dfrac{k^2}{4\pi\epsilon_0}\dfrac{e^{ikr}}{r}\left(\hat{n}\times\vec{p}\right)\times\hat{n}
\end{align}$$
The cross product for the normal and the electric dipole (only has a $z$) component:
$$\begin{align}
\hat{n}\times\vec{p}&=\dfrac{2^{15/2}}{3^{9/2}}\dfrac{ea_0}{\sqrt{\pi}}e^{-i\omega_0t}\left(\hat{r}\times\hat{z}\right)\\
&=\dfrac{2^{15/2}}{3^{9/2}}\dfrac{ea_0}{\sqrt{\pi}}e^{-i\omega_0t}\left(-\sin\theta\ \hat{r}\times\hat{\theta}\right)\\
\Aboxed{\hat{n}\times\vec{p}&=-\dfrac{2^{15/2}}{3^{9/2}}\dfrac{ea_0}{\sqrt{\pi}}e^{-i\omega_0t}\sin\theta\ \hat{\phi}}\\
\Aboxed{\left(\hat{n}\times\vec{p}\right)\times\hat{n}&=-\dfrac{2^{15/2}}{3^{9/2}}\dfrac{ea_0}{\sqrt{\pi}}e^{-i\omega_0t}\sin\theta\ \hat{\theta}}
\end{align}$$
Our electromagnetic fields then becomes:
$$\begin{align}
c\vec{B}&=-\dfrac{2^{15/2}}{3^{9/2}\sqrt{\pi}}\dfrac{ea_0k^2}{4\pi\epsilon_0}\dfrac{e^{ikr}}{r}e^{-i\omega_0t}\sin\theta\ \hat{\phi} &&& \vec{E}&=\left(c\vec{B}\cdot\hat{\phi}\right)\hat{\theta}
\end{align}$$
The cross product of these fields is also pretty simple:
$$\begin{align}
\vec{E}\times c\vec{B}^*&=\left(c\vec{B}\cdot\hat{\phi}\right)\hat{\theta}\times \left(c\vec{B}\cdot\hat{\phi}\right)^*\hat{\phi}=\left|c\vec{B}\cdot\hat{\phi}\right|^2\hat{r}
\end{align}$$
The power per unit solid angle $(9.21)$ is then:
$$\begin{align}
\dfrac{dP}{d\Omega}&=\dfrac{c\epsilon_0}{2}r^2\ \Re \left[\hat{r}\cdot\left(\vec{E}\times c\vec{B}^*\right)\right]=\dfrac{c\epsilon_0}{2}r^2\left|c\vec{B}\cdot\hat{\phi}\right|^2
\end{align}$$
If we substitute in the painful expression for the magnitude:
$$\begin{align}
\dfrac{dP}{d\Omega}&=\dfrac{2^{12}}{3^{9}\pi^2}\dfrac{ce^2a_0^2}{4\pi\epsilon_0}\cdot k^4\sin^2\theta
\end{align}$$
<div style="page-break-before: always;"></div>


In our system, the wavenumber $k$ is related to the frequency of the energy levels by $k=\omega_0/c$ :
$$\begin{align}
\dfrac{dP}{d\Omega}&=\dfrac{2^{10}}{3^{9}\pi}\dfrac{ce^2a_0^2}{4\pi\epsilon_0}\cdot\dfrac{\omega_0^4}{c^4}\cdot\dfrac{1}{4\pi}\sin^2\theta\\
&=\omega_0\dfrac{2^{10}}{3^{9}\pi}\dfrac{ce^2a_0^2}{4\pi\epsilon_0}\cdot\dfrac{\left(3e^2/32\pi\epsilon_0\hbar a_0\right)^3}{c^4}\cdot\dfrac{1}{4\pi}\sin^2\theta\\
&=\dfrac{\hbar\omega_0c}{a_0}\dfrac{1}{3^{6}\pi}\left(\dfrac{e^2}{\hbar c(4\pi\epsilon_0)}\right)^4\cdot\dfrac{1}{4\pi}\sin^2\theta\\
\dfrac{dP}{d\Omega}&=\dfrac{1}{3^{6}\pi}\dfrac{\hbar\omega_0c}{a_0}\alpha^4\cdot\dfrac{1}{4\pi}\sin^2\theta
\end{align}$$
When we integrate this over the whole surface of a sphere, we finally get:
$$\begin{align}
\Aboxed{P&=\dfrac{1}{2916}\dfrac{\hbar\omega_0c}{a_0}\alpha^4}
\end{align}$$
Not sure if the coefficient is correct, unfortunately. Way too much math.

---
### Question 9.10.C
> Interpreting the classically calculated power as the photon energy $(\hbar\omega_0)$ times the transition probability, evaluate numerically the transition amplitude in units of reciprocal seconds.

Doing as the question states, it's very simple to write an expression that represents it:
$$\begin{align}
P&=E_\gamma W_{2p^z\to1s} &\implies&& \Aboxed{W_{2p^z\to1s}&=\dfrac{1}{2916}\dfrac{c}{a_0}\alpha^4}
\end{align}$$
If we use the relationship between the Bohr radius and the fine structure constant, it becomes easier to calculate the probability numerically:
$$\begin{align}
W_{2p^z\to1s}&=\dfrac{\alpha^5}{2916}\dfrac{m_ec^2}{\hbar}
\end{align}$$
where $\alpha\sim1/137$, $m_ec^2\sim0.511\cdot10^6\text{ eV}$, and , $\hbar\sim6.582\cdot10^{-16}\text{ eV}\cdot\text{s}$, we get:
$$\begin{align}
W_{2p^z\to1s}&=5.5167\dfrac{1}{\mu\text{s}}=\dfrac{1}{0.1813\ \mu\text{s}}
\end{align}$$
What this would mean statistically is that the mean time for the transition from the $2p^z$ orbital to the $1s$ orbital is $\sim0.1813\mu\text{s}=\boxed{181.271\text{ ns}}$ if we use classical statistics. This is very different from reality, where the transition is on the order of nanoseconds.

This is assuming my coefficient is correct, which I am *not* confident about.




### Question 9.10.D
> If, instead of the semiclassical charge density used above, the electron in the $2p$ state was described by a circular Bohr orbit of radius $2a_0$, rotating with the transitional frequency $\omega_0$, what would the radiated power be? Express your answer in the same units are part [[#Question 9.10.B|B]] and evaluate the ratio of the two powers numerically.

For electric dipole fields in the IR (far field), we once again use $(9.19)$:
$$\begin{align}
c\vec{B}&=\dfrac{k^2}{4\pi\epsilon_0}\dfrac{e^{ikr}}{r}\left(\hat{r}\times\vec{p}\right) &&& \vec{E}&=c\vec{B}\times\hat{r}
\end{align}$$
The electric dipole moment, being a point particle, is trivially:
$$\begin{align}
\vec{p}&=-2ea_0\left(\hat{x}\cos(\omega_0t)+\hat{y}\sin(\omega_0t)\right)
\end{align}$$
The evaluation of the cross product is:
$$\begin{align}
\hat{r}\times\vec{p}=&-2ea_0\cos\theta\left(\cos\phi\cos(\omega_0t)+\sin\phi\sin(\omega_0t)\right)\ \hat{\phi}\\
&-2ea_0\left(\sin\phi\cos(\omega_0t)-\cos\phi\sin(\omega_0t)\right)\ \hat{\theta}\\
\end{align}$$
We can use angle sum formulae for trigonometry:
$$\begin{align}
\hat{r}\times\vec{p}&=-2ea_0\left[\cos\theta\cos\left(\phi-\omega_0t\right)\ \hat{\phi}+\sin\left(\phi-\omega_0t\right)\ \hat{\theta}\right]\\
(\hat{r}\times\vec{p})\times\hat{r}&=-2ea_0\left[\cos\theta\cos\left(\phi-\omega_0t\right)\ \hat{\theta}-\sin\left(\phi-\omega_0t\right)\ \hat{\phi}\right]
\end{align}$$
Substituting into the fields, we have:
$$\begin{align}
c\vec{B}&=-\dfrac{ea_0k^2}{2\pi\epsilon_0}\dfrac{e^{ikr}}{r}\left[\cos\theta\cos\left(\phi-\omega_0t\right)\ \hat{\phi}+\sin\left(\phi-\omega_0t\right)\ \hat{\theta}\right] \\
\vec{E}&=-\dfrac{ea_0k^2}{2\pi\epsilon_0}\dfrac{e^{ikr}}{r}\left[\cos\theta\cos\left(\phi-\omega_0t\right)\ \hat{\theta}-\sin\left(\phi-\omega_0t\right)\ \hat{\phi}\right]
\end{align}$$
The cross product between these two fields leaves the following:
$$\begin{align}
\vec{E}\times c\vec{B}^*&=\dfrac{e^2a_0^2k^4}{4\pi^2\epsilon_0^2r^2}\left[\cos^2\theta\cos^2\left(\phi-\omega_0t\right)+\sin^2\left(\phi-\omega_0t\right)\right]\hat{r}
\end{align}$$
Our power per unit area is:
$$\begin{align}
\dfrac{dP}{d\Omega}&=\dfrac{c\epsilon_0}{2}\dfrac{e^2a_0^2k^4}{4\pi^2\epsilon_0^2}\left[\cos^2\theta\cos^2\left(\phi-\omega_0t\right)+\sin^2\left(\phi-\omega_0t\right)\right]
\end{align}$$
The total power is then integrated over the surface:
$$\begin{align}
P&=\dfrac{4}{3}\dfrac{ce^2a_0^2k^4}{4\pi\epsilon_0}&\implies&&\Aboxed{P&=\dfrac{9}{128}\dfrac{\hbar c\omega_0}{a_0}\alpha^4}
\end{align}$$
If we divide this power by the one we found the true orbitals, we see:
$$\begin{align}
\Aboxed{\dfrac{P_\text{Bohr}}{P_\text{Orbital}}&=\dfrac{3^8}{2^5}\sim205\text{x}}
\end{align}$$
The naive Bohr model power is over $200$ times the amount of power compared to quantum mechanics calculations, assuming my coefficient was correct.

---
## Question 9.16
> A thin, linear, antenna of length $d$ is excited in such a way that the sinusoidal current makes a full wavelength of oscillation as shown in the figure.

To have a current that matches the diagram, I choose the $z$-axis to be our current direction, with the bounds of $z$ being symmetric, so $z\in[-d/2,d/2]$. It forms one full period, and so:
$$\begin{align}
I(z,t)&=I_0\sin\left(\dfrac{2\pi}{d}z\right)e^{-i\omega t} & I_0<0
\end{align}$$
We can then write the current density in terms of this current, also in the $z$-axis and same bounds:
$$\begin{align}
\vec{J}(\vec{x},t)&=I(z,t)\delta(x)\delta(y)\hat{z}
\end{align}$$
The vector potential, in terms of the current density, can be found in the textbook $(9.3)$, after we have simplified the expression removing the time-dependence with time retardation:
$$\begin{align}
\vec{A}(\vec{x})&=\dfrac{\mu_0}{4\pi}\int\vec{J}(x')\dfrac{e^{ik|\vec{x}-\vec{x}'|}}{|\vec{x}-\vec{x}'|}\ d^3x'
\end{align}$$
Substituting our current density into the potential, and exploiting the Dirac delta functions:
$$\begin{align}
\vec{A}(\vec{x})&=\dfrac{\mu_0}{4\pi}\int I_0\sin\left(\dfrac{2\pi}{d}z'\right)\delta(x')\delta(y')\hat{z}\dfrac{e^{ik|\vec{x}-\vec{x}'|}}{|\vec{x}-\vec{x}'|}\ d^3x'\\
&=\dfrac{\mu_0I_0}{4\pi}\hat{z}\int_{-d/2}^{d/2}\sin\left(\dfrac{2\pi}{d}z'\right)\dfrac{e^{ik\sqrt{x^2+y^2+(z-z')^2}}}{\sqrt{x^2+y^2+(z-z')^2}}\ dz'
\end{align}$$
Since we'll want to write the characteristics of this system in the far-field limit, it would be easier to calculate this in spherical coordinates. The current density in spherical coordinates is:
$$\begin{align}
\vec{A}(r,\theta)&=\dfrac{\mu_0I_0}{4\pi}\hat{z}\int_{-d/2}^{d/2}\sin\left(\dfrac{2\pi}{d}z'\right)\dfrac{e^{ik\sqrt{r^2+z'^2-2z'r\cos\theta}}}{\sqrt{r^2+z'^2-2rz'\cos\theta}}\ dz'\\
\end{align}$$
<div style="page-break-before: always;"></div>


For evaluating the field at large $r\gg d/2$, we want to linearize the distance by Taylor expansion:
$$\begin{align}
\sqrt{r^2+z'^2-2rz'\cos\theta}&=r\sqrt{1-2\dfrac{z'}{r}\cos\theta+\dfrac{z'^2}{r^2}}\approx r\left(1-\dfrac{2}{2}\dfrac{z'}{r}\cos\theta\right)=r-z'\cos\theta\\
\dfrac{1}{r-z'\cos\theta}&\approx\dfrac{1}{r}+\dfrac{z'\cos\theta}{r^2}+\dots\approx\dfrac{1}{r}
\end{align}$$
This immensely simplifies our integral in this regime, now written as:
$$\begin{align}
\lim_{r\gg d}\vec{A}(r,\theta)
&=\dfrac{\mu_0I_0}{4\pi}\dfrac{e^{ikr}}{r}\hat{z}\int_{-d/2}^{d/2}\sin\left(\dfrac{2\pi}{d}z'\right)e^{-ikz'\cos\theta}\ dz'\\
&=\dfrac{\mu_0I_0}{4\pi}\dfrac{e^{ikr}}{r}\hat{z}\dfrac{1}{2i}\int_{-d/2}^{d/2}\left[e^{-iz'\left(k\cos\theta-\tfrac{2\pi}{d}\right)}-e^{-iz'\left(k\cos\theta+\tfrac{2\pi}{d}\right)}\right]\ dz'\\
&=\dfrac{\mu_0I_0}{4\pi}\dfrac{e^{ikr}}{r}\hat{z}\dfrac{1}{2}\left[\dfrac{e^{-iz'\left(k\cos\theta-\tfrac{2\pi}{d}\right)}}{\left(k\cos\theta-\tfrac{2\pi}{d}\right)}-\dfrac{e^{-iz'\left(k\cos\theta+\tfrac{2\pi}{d}\right)}}{\left(k\cos\theta+\tfrac{2\pi}{d}\right)}\right|_{-d/2}^{d/2}\\
&=\dfrac{\mu_0I_0}{4\pi}\dfrac{e^{ikr}}{r}\hat{z}\dfrac{1}{2}\left[\dfrac{-e^{-i\left(\tfrac{kd}{2}\cos\theta\right)}+e^{+i\left(\tfrac{kd}{2}\cos\theta\right)}}{\left(k\cos\theta-\tfrac{2\pi}{d}\right)}-\dfrac{-e^{-i\left(\tfrac{kd}{2}\cos\theta\right)}+e^{+i\left(\tfrac{kd}{2}\cos\theta\right)}}{\left(k\cos\theta+\tfrac{2\pi}{d}\right)}\right]\\
&=\dfrac{\mu_0I_0}{4\pi}\dfrac{e^{ikr}}{r}\hat{z}\dfrac{2i}{2}\left[\dfrac{1}{\left(k\cos\theta-\tfrac{2\pi}{d}\right)}-\dfrac{1}{\left(k\cos\theta+\tfrac{2\pi}{d}\right)}\right]\sin\left(\tfrac{kd}{2}\cos\theta\right)\\
\lim_{r\gg d}\vec{A}(r,\theta)&=-i\dfrac{\mu_0(2I_0)}{4\pi}\dfrac{e^{ikr}}{kr}\hat{z}\left[\dfrac{\left(\tfrac{kd}{2\pi}\right)\sin\left(\tfrac{kd}{2}\cos\theta\right)}{1-\left(\tfrac{kd}{2\pi}\right)^2\cos^2\theta}\right]
\end{align}$$
---
### Question 9.16.A
> Calculate the power radiated per unit solid angle and plot the angular distribution of radiation.

In the far field, we have the following equations for the electromagnetic fields:
$$\begin{align}
\vec{B}&=ik\hat{r}\times\vec{A} & \vec{E}&=c\vec{B}\times\hat{r}
\end{align}$$
Using our vector potentials, we have the following expressions
$$\begin{align}
c\vec{B}(r,\theta)&=-\dfrac{I_0}{2\pi\epsilon_0 c}\dfrac{e^{ikr}}{r}\left[\dfrac{\left(\tfrac{kd}{2\pi}\right)\sin\left(\tfrac{kd}{2}\cos\theta\right)}{1-\left(\tfrac{kd}{2\pi}\right)^2\cos^2\theta}\right]\sin\theta\ \hat{\phi}\\
\vec{E}(r,\theta)&=-\dfrac{I_0}{2\pi\epsilon_0 c}\dfrac{e^{ikr}}{r}\left[\dfrac{\left(\tfrac{kd}{2\pi}\right)\sin\left(\tfrac{kd}{2}\cos\theta\right)}{1-\left(\tfrac{kd}{2\pi}\right)^2\cos^2\theta}\right]\sin\theta\ \hat{\theta}
\end{align}$$
<div style="page-break-before: always;"></div>


We can take their cross product:
$$\begin{align}
\vec{E}\times c\vec{B}^*&=\dfrac{4I_0^2}{(4\pi\epsilon_0)^2 c^2r^2}\left(\dfrac{kd}{2\pi}\right)^2\dfrac{\sin^2\left(\tfrac{kd}{2}\cos\theta\right)\sin^2\theta}{\left[1-\left(\tfrac{kd}{2\pi}\right)^2\cos^2\theta\right]^2}\ \hat{r}
\end{align}$$
For further simplification, since this is radiated from the antenna, we have the relationship:
$$\begin{align}
k=\dfrac{\omega}{c}=\dfrac{2\pi}{\lambda}=\dfrac{2\pi}{d}
\end{align}$$
The cross product then reduces even further:
$$\begin{align}
\vec{E}\times c\vec{B}^*&=\dfrac{4I_0^2}{(4\pi\epsilon_0)^2 c^2r^2}\dfrac{\sin^2\left(\pi\cos\theta\right)}{\sin^2\theta}\ \hat{r}
\end{align}$$
The power per unit surface area is:
$$\begin{align}
\dfrac{dP}{d\Omega}&=\dfrac{2I_0^2}{(4\pi\epsilon_0) c}\cdot\dfrac{1}{4\pi}\dfrac{\sin^2\left(\pi\cos\theta\right)}{\sin^2\theta}
\end{align}$$
If we plot this, where the radius is proportional to its contribution, it takes the following shape
![[9.16.A.png]]
where the angle $\theta$ is read from vertical up and goes clockwise to vertical down. This is azimuthally symmetric, and so this geometry is revolved around the vertical axis to make the final shape.
<div style="page-break-before: always;"></div>



### Question 9.16.B
> Determine the total power radiated and find a numerical value for the radiation resistance.

Integrating over over a whole sphere, we get the total power:
$$\begin{align}
P&=\dfrac{2I_0^2}{(4\pi\epsilon_0) c}\cdot\dfrac{1}{4\pi}\cdot2\pi\int_0^\pi\dfrac{\sin^2\left(\pi\cos\theta\right)}{\sin^2\theta}\ \sin\theta\ d\theta\\
&=\dfrac{I_0^2}{(4\pi\epsilon_0) c}\int_{-1}^{1}\dfrac{\sin^2\left(\pi z\right)}{1-z^2}\ dz\\
\Aboxed{P&=\dfrac{I_0^2}{4\pi\epsilon_0c}\cdot1.557}
\end{align}$$
Evaluating numerically, we get a power:
$$\begin{align}
\Aboxed{P&\sim46.684I_0^2\ \text{W}\cdot\text{A}^{-2}}
\end{align}$$
Radiation resistance, as I found it on [Wikipedia](https://en.wikipedia.org/wiki/Radiation_resistance), and substituted with our values:
$$\begin{align}
R_\text{rad}&=\dfrac{R_\text{rad}}{I_\text{rms}^2}=\dfrac{R_\text{rad}}{(I_0/\sqrt{2})^2} &\implies && \Aboxed{R_\text{rad}&\approx93.368\ \Omega}
\end{align}$$
