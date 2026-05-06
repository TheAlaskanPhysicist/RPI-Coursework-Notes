




Transition Amplitude between Eigenstates of $H_0$ :
$$\begin{align}
\bra{n}U_I(t,t_0)\ket{i}&=\delta_{ni}+\dfrac{1}{i\hbar}\sum_{m}\bra{n}V\ket{m}\int_{t_0}^t e^{i\omega_{nm}t'}\bra{m}U_I(t',t_0)\ket{i}\ dt'
\end{align}$$




## Scattering Theory
We will use big-box normalization inside a cube of length $L$ to discretize states. In coordinate representation, this gives us the inner products
$$\begin{align}
\left(\lim{L\to\infty}\right)&&
\left\langle\vec{x}\middle|\vec{k}\right\rangle&=\dfrac{1}{L^{3/2}}e^{i\vec{k}\cdot\vec{x}} 
&\text{where}&&
\left\langle\vec{k}'\middle|\vec{k}\right\rangle&=\delta_{\vec{k},\vec{k}'}
\end{align}$$
The first-order approximation for transition amplitude can then be written as
$$\begin{align}
\bra{\text{f}}U_I(t,t_0)\ket{\text{i}}&=\delta_{\text{f}\text{i}}+\dfrac{\bra{\text{f}}V\ket{\text{i}}}{i\hbar}\int_{t_0}^t e^{i\omega_{\text{f}\text{i}}t'}\ dt'
&\text{where}&&
E_\text{f}-E_\text{i}&=\hbar\omega_{\text{f}\text{i}}
\end{align}$$
We define the $T$ matrix in the limit process of $t\to\infty$ and $t_0\to-\infty$ to satisfy
$$\begin{align}
\bra{\text{f}}U_I(t,t_0)\ket{\text{i}}&=\delta_{\text{f}\text{i}}+\dfrac{1}{i\hbar}T_{\text{f}\text{i}}\int_{t_0}^t e^{(\varepsilon+i\omega_{\text{f}\text{i}})t'}\ dt'
&\text{where}&&
\varepsilon&\gt0
&\text{and}&&
\varepsilon t&\ll1
\end{align}$$
We then define the scattering matrix $S$ to be this limiting process
$$\begin{align}
S_{\text{f}\text{i}}&\equiv\lim_{t\to\infty}\lim_{\varepsilon\to0^+}\bra{\text{f}}U_I(t,-\infty)\ket{\text{i}}
\end{align}$$
or in terms of the $T$ matrix, it becomes
$$\begin{align}
S_{\text{f}\text{i}}&=\delta_{\text{f}\text{i}}-2\pi i\ \delta(E_\text{f}-E_\text{i})\ T_{\text{f}\text{i}}
\end{align}$$



### Transition Rates and Cross Sections
From Section 5.7, we define transition rate as
$$\begin{align}
\mathcal{W}_{\text{i}\to\text{f}}&\equiv\lim_{t_0\to-\infty}\dfrac{d}{dt}\left|\bra{\text{f}}U_I(t,t_0)\ket{\text{i}}\right|^2
&&\text{(Definition)}
\end{align}$$
or in terms of our $T$ matrix in the 1st-order approximation
$$\begin{align}
\mathcal{W}_{\text{i}\to\text{f}}&=\dfrac{2\pi}{\hbar}\left|T_{\text{f}\text{i}}\right|^2\delta(E_\text{f}-E_\text{i})
\end{align}$$
This is very similar to Fermi's golden rule, when $V_{\text{f}\text{i}}\to T_{\text{f}\text{i}}$, being more generalized. 

In the big-box limit, we can write this transition statistically as
$$\begin{align}
\mathcal{W}_{\text{i}\to\text{f}}&=\dfrac{mkL^3}{(2\pi)^2\hbar^3}\left|T_{\text{f}\text{i}}\right|^2d\Omega
\end{align}$$






## The Scattering Amplitude
For elastic scattering, $E_\text{f}=E_\text{i}=E$, and sufficiently small $\varepsilon$, we can write our recursive relationship for our wavefunction solution for $\ket{\psi^{(\pm)}}$ to be of the form
$$\begin{align}
\ket{\psi^{(\pm)}}&\equiv\ket{\text{i}}+\dfrac{1}{E-H_0\pm i\varepsilon}V\ket{\psi^{(\pm)}}
\end{align}$$
Multiplying on the left both sides by $\bra{\vec{x}'}$ and inserting completeness relations as needed,
$$\begin{align}
\braket{\vec{x}\lvert\psi^{(\pm)}}&=\braket{\vec{x}\lvert\text{i}}+\int\left\langle\vec{x}\middle|\dfrac{1}{E-H_0\pm i\varepsilon}\middle|\vec{x}'\right\rangle\bra{\vec{x}'}V\ket{\psi^{(\pm)}}\ d^3x'
\end{align}$$
This internal operator can be defined as a propagator function
$$\begin{align}
G_{\pm}(\vec{x},\vec{x}')&=\dfrac{\hbar^2}{2m}\left\langle\vec{x}\middle|\dfrac{1}{E-H_0\pm i\varepsilon}\middle|\vec{x}'\right\rangle
\implies
\braket{\vec{x}\lvert\psi^{(\pm)}}=\braket{\vec{x}\lvert\text{i}}+\dfrac{2m}{\hbar^2}\int G_{\pm}(\vec{x},\vec{x}')\bra{\vec{x}'}V\ket{\psi^{(\pm)}}\ d^3x'
\end{align}$$
The eigenstates of $H_0$ are more easily evaluated in momentum eigenstates, so we can insert two completeness relations to find that
$$\begin{align}
G_{\pm}(\vec{x},\vec{x}')&=\dfrac{\hbar^2}{2m}\sum_{\vec{k}',\vec{k}''}\left\langle\vec{x}\middle|\vec{k}'\right\rangle\left\langle\vec{k}'\middle|\dfrac{1}{E-H_0\pm i\varepsilon}\middle|\vec{k}''\right\rangle\left\langle\vec{k}''\middle|\vec{x}'\right\rangle\\
&=\dfrac{\hbar^2}{2m}\sum_{\vec{k}',\vec{k}''}\dfrac{1}{\tfrac{\hbar^2}{2m}\vec{k}^2-\tfrac{\hbar^2}{2m}\vec{k}'^2\pm i\varepsilon}\left\langle\vec{x}\middle|\vec{k}'\right\rangle\left\langle\vec{k}'\middle|\vec{k}''\right\rangle\left\langle\vec{k}''\middle|\vec{x}'\right\rangle\\
&=\dfrac{\hbar^2}{2m}\sum_{\vec{k}',\vec{k}''}\dfrac{2m}{\hbar^2}\dfrac{1}{\vec{k}^2-\vec{k}'^2\pm i\varepsilon}\cdot\dfrac{1}{L^{3/2}}e^{i\vec{k}'\cdot\vec{x}}\cdot\delta_{\vec{k}'\vec{k}''}\cdot\dfrac{1}{L^{3/2}}e^{-i\vec{k}''\cdot\vec{x}'}\\
G_{\pm}(\vec{x},\vec{x}')&=\dfrac{1}{L^3}\sum_{\vec{k}'}\dfrac{e^{i\vec{k}'\cdot(\vec{x}-\vec{x}')}}{\vec{k}^2-\vec{k}'^2\pm i\varepsilon}
\end{align}$$
In big-box normalization, we can substitute summations for integrals to arrive to
$$\begin{align}
G_{\pm}(\vec{x},\vec{x}')&=\dfrac{1}{(2\pi)^3}\int\dfrac{e^{i\vec{k}'\cdot(\vec{x}-\vec{x}')}}{\vec{k}^2-\vec{k}'^2\pm i\varepsilon}d^3k'
\end{align}$$
If we choose to integrate this in spherical coordinates, this reduces further to
$$\begin{align}
\Aboxed{G_{\pm}(\vec{x},\vec{x}')&=-\dfrac{1}{4\pi}\dfrac{e^{\pm ik\left|\vec{x}-\vec{x}'\right|}}{\left|\vec{x}-\vec{x}'\right|}}
\end{align}$$
Substituting back in, we see that this wavefunction in space has the relationship
$$\begin{align}
\braket{\vec{x}\lvert\psi^{(\pm)}}=\braket{\vec{x}\lvert\text{i}}-\dfrac{2m}{\hbar^2}\dfrac{1}{4\pi}\int\dfrac{e^{\pm ik\left|\vec{x}-\vec{x}'\right|}}{\left|\vec{x}-\vec{x}'\right|}\bra{\vec{x}'}V\ket{\psi^{(\pm)}}\ d^3x'
\end{align}$$
This is the sum of the incident wave and the scattered wave term.

### Local Potentials
Local potentials are diagonal in their space representation, as in only dependent on $\vec{x}$, or
$$\begin{align}
\left\langle\vec{x}'\middle|\vec{x}''\right\rangle&=V(\vec{x}')\delta\!\left(\vec{x}'-\vec{x}''\right)
\end{align}$$
After some simplification, the wavefunction in space now has the form
$$\begin{align}
\braket{\vec{x}\lvert\psi^{(\pm)}}=\braket{\vec{x}\lvert\text{i}}-\dfrac{2m}{\hbar^2}\dfrac{1}{4\pi}\int\dfrac{e^{\pm ik\left|\vec{x}-\vec{x}'\right|}}{\left|\vec{x}-\vec{x}'\right|}V(\vec{x}')\left\langle\vec{x}'\middle|\psi^{(\pm)}\right\rangle\ d^3x'
\end{align}$$
Since we would like to model the behavior of the wave effectively "at infinity," we can make a series of approximations that maintain the physics at distances far from the potential.
$$\begin{align}
\lim_{r\to\infty}\braket{\vec{x}\lvert\psi^{(\pm)}}&=\left\langle\vec{x}\middle|\vec{k}\right\rangle-\dfrac{1}{4\pi}\dfrac{2m}{\hbar^2}\dfrac{e^{\pm ikr}}{r}\int e^{\mp i\vec{k}'\cdot\vec{x}'}V(\vec{x}')\left\langle\vec{x}'\middle|\psi^{(\pm)}\right\rangle\ d^3x'
\end{align}$$
Alternatively, we can write this in terms of a new function $f\!\left(\vec{k}',\vec{k}\right)$, where
$$\begin{align}
\lim_{r\to\infty}\braket{\vec{x}\lvert\psi^{(\pm)}}&=\dfrac{1}{L^{3/2}}\left(e^{i\vec{k}\cdot\vec{x}}+\dfrac{e^{\pm ikr}}{r}f_{\pm}\!\left(\vec{k}',\vec{k}\right)\right)\\
f_{\pm}\left(\vec{k},\vec{k}'\right)&=-\dfrac{mL^3}{2\pi\hbar^2}\left\langle\pm\vec{k}'\middle|V\middle|\psi^{(\pm)}\right\rangle
\end{align}$$
This $f\!\left(\vec{k}',\vec{k}\right)$ is called the *scattering amplitude*. It relates to differential cross section by
$$\begin{align}
\dfrac{d\sigma}{d\Omega}&=\left|f\!\left(\vec{k}',\vec{k}\right)\right|^2
\end{align}$$
### Optical Theorem
The optical theorem relates the imaginary component of the forward scattering amplitude $f(\theta=0)\equiv f\!\left(\vec{k},\vec{k}\right)$ to the total cross section $\sigma$, written as
$$\begin{align}
\mathrm{Im}\ f(\theta=0)&=\dfrac{k\sigma_\text{tot}}{4\pi}
&\implies&&
\sigma_\text{tot}&=\dfrac{4\pi}{k}\mathrm{Im}\ f(\theta=0)
\end{align}$$

## The Born Approximation
We want to calculate $f\!\left(\vec{k}',\vec{k}\right)$ for some given potential energy function $V(\vec{x})$. I.e. the element
$$\begin{align}
\left\langle\vec{k}'\middle|V\middle|\psi^{(+)}\right\rangle&=\left\langle\vec{k}'\middle|T\middle|\vec{k}\right\rangle
\end{align}$$
Our recursive expansion for $T$ has the form
$$\begin{align}
T&=V+V\dfrac{1}{E-H_0\pm i\varepsilon}V+V\dfrac{1}{E-H_0\pm i\varepsilon}V\dfrac{1}{E-H_0\pm i\varepsilon}V+\dots
\end{align}$$
The first-order term of this expansion is $T^{(1)}=V$, called the first-order Born approximation. The scattering amplitude associated with this order term, $f^{(1)}$, is
$$\begin{align}
f^{(1)}\!\left(\vec{k}',\vec{k}\right)&=-\dfrac{m}{2\pi\hbar^2}\int e^{i\vec{q}\cdot\vec{x}'}V(\vec{x}')\ d^3x' & \vec{q}&\equiv\vec{k}-\vec{k}'
\end{align}$$
For a potential that is spherically symmetric, $f^{(1)}\!\left(\vec{k}',\vec{k}\right)$ is a function of $q\equiv\left|\vec{q}\right|$, which is related to the kinematic variables in experiment. By energy conservation, we can see that
$$\begin{align}
q&=\left|\vec{k}-\vec{k}'\right|=2k\sin\left(\theta/2\right)
&\implies&&
f^{(1)}\!\left(\vec{k}',\vec{k}\right)=f^{(1)}\!\left(\theta\right)
\end{align}$$
We can then perform the integration of this function to arrive to
$$\begin{align}
\Aboxed{f^{(1)}\!\left(\theta\right)&=-\dfrac{2m}{\hbar^2}\dfrac{1}{q}\int_0^\infty rV(r)\sin\left(qr\right)\ dr}
\end{align}$$
---
### Scattering by Sphere of Finite Potential
Suppose we have a potential $V$ given by
$$\begin{align}
V(r)&=\begin{cases}V_0,&r\le a\\0,&r\ge a\end{cases}
\end{align}$$
Our scattering amplitude evaluates to
$$\begin{align}
f^{(1)}\!\left(\theta\right)&=-\dfrac{2m}{\hbar^2}\dfrac{V_0a^3}{(qa)^2}\left[\dfrac{\sin qa}{qa}-\cos qa\right]
\end{align}$$
as well as the differential cross section becoming
$$\begin{align}
\dfrac{d\sigma}{d\Omega}(\theta)&=\dfrac{4m^2}{\hbar^4}\dfrac{V_0^2a^6}{(qa)^4}\left[\dfrac{\sin qa}{qa}-\cos qa\right]^2
\end{align}$$
If we expand these terms to be Taylor series, we find that
$$\begin{align}
f^{(1)}\!\left(\theta\right)&=\dfrac{4m}{\hbar^2}\dfrac{V_0a^3}{(qa)^2}\sum_{n=0}^\infty(-1)^n\dfrac{n}{(2n+1)!}(qa)^{2n} \\
\dfrac{d\sigma}{d\Omega}(\theta)&=\dfrac{16m^2}{\hbar^4}\dfrac{V_0^2a^6}{(qa)^4}\sum_{n=0}^\infty\sum_{m=0}^\infty(-1)^{n+m}\dfrac{nm}{(2n+1)!(2m+1)!}(qa)^{2(n+m)}
\end{align}$$
---
#### Limit Behavior $(qa\gg1)$
In the limit where $qa$ is very large, the $\operatorname{sinc}$ term will vanish, leaving only the cosine term
$$\begin{align}
\lim_{ka\gg1}\left|f^{(1)}\!\left(\theta\right)\right|&=\left(\dfrac{mV_0}{\hbar^2}\right)ak^{-2}\dfrac{1}{1-\cos\theta}
&&&
\lim_{ka\gg1}\dfrac{d\sigma}{d\Omega}(\theta)&=\left(\dfrac{mV_0}{\hbar^2}\right)^2a^2k^{-4}\dfrac{1}{(1-\cos\theta)^2}
\end{align}$$
---
#### Limit Behavior $(qa\ll1)$
In the limit where $qa$ is very small, we can use the full form of the Taylor expansion
$$\begin{align}
\lim_{ka\ll1}f^{(1)}\!\left(\theta\right)&=\dfrac{mV_0}{\hbar^2}a^3\sum_{n=0}^\infty(-1)^n\dfrac{4^{n}n}{(2n+1)!}(ka\sin\left(\theta/2\right))^{2(n-1)}
\end{align}$$
The square magnitude of this quantity is a little trickier
$$\begin{align}
\lim_{ka\ll1}\dfrac{d\sigma}{d\Omega}(\theta)
&=\left(\dfrac{mV_0}{\hbar^2}\right)^2a^6\dfrac{1}{(ka\sin\left(\theta/2\right))^{4}}\sum_{n=0}^\infty\sum_{m=0}^\infty(-1)^{n+m}\dfrac{4^{n+m}nm}{(2n+1)!(2m+1)!}(ka\sin\left(\theta/2\right))^{2(n+m)}\\
&=\left(\dfrac{mV_0}{\hbar^2}\right)^2a^6\sum_{\alpha=0}^\infty\sum_{\beta=0}^\alpha(-1)^{\alpha}\dfrac{4^{\alpha}\beta(\alpha-\beta)}{(2\beta+1)!(2(\alpha-\beta)+1)!}(ka\sin\left(\theta/2\right))^{2\alpha-4}\\
\end{align}$$
We have the following integral identities
$$\begin{align}
\int_0^\pi\dfrac{1}{\sin^p\!\left(\theta/2\right)}\sin\theta\ d\theta&=\dfrac{4}{2-p} & (p&<2)\\
\int_0^\pi\sin^p\!\left(\theta/2\right)\sin\theta\ d\theta&=\dfrac{4}{2+p} & (p&>-2)
\end{align}$$
When we integrate over a sphere to find the total cross section, our sine terms get integrated to
$$\begin{align}
\alpha&\ge2 & \int_0^\pi\sin^{2\alpha-4}\!\left(\theta/2\right)\sin\theta\ d\theta&=\dfrac{2}{\alpha-1}
\end{align}$$
In total, we then have:
$$\begin{align}
\lim_{ka\ll1}\sigma_\text{tot}
&=4\pi\left(\dfrac{mV_0}{\hbar^2}\right)^2a^6\sum_{\alpha=2}^\infty\sum_{\beta=0}^\alpha(-1)^{\alpha}\dfrac{4^{\alpha}\beta(\alpha-\beta)}{(2\beta+1)!(2(\alpha-\beta)+1)!}\dfrac{1}{\alpha-1}(ka)^{2\alpha-4}
\end{align}$$








we can truncate the expansion after the lowest non-vanishing order in the Taylor series expansion
$$\begin{align}
\lim_{ka\ll1}f^{(1)}\!\left(\theta\right)&=-\dfrac{2}{3}\left(\dfrac{mV_0}{\hbar^2}\right)a^3=-\dfrac{mV_0}{2\pi\hbar^2}v
&&&
\lim_{ka\ll1}\dfrac{d\sigma}{d\Omega}(\theta)&=\dfrac{4}{9}\left(\dfrac{mV_0}{\hbar^2}\right)^2a^6=\left(\dfrac{mV_0}{2\pi\hbar^2}\right)^2v^2
\end{align}$$
Where $v$ is the volume of the sphere $v=4\pi a^3/3$. The total cross section in this limit is
$$\begin{align}
\lim_{ka\ll1}\sigma_\text{tot}&=\dfrac{16\pi}{9}\left(\dfrac{mV_0}{\hbar^2}\right)^2a^6=\dfrac{1}{\pi}\left(\dfrac{mV_0}{\hbar^2}\right)^2v^2
\end{align}$$










In the $|ka|\sim qa\ll1$ limit (or $\theta\sim0$ limit), our amplitude and cross section become
$$\begin{align}
\lim_{qa\ll1}f^{(1)}\!\left(\theta\right)&=-\dfrac{2}{3}\dfrac{mV_0}{\hbar^2}a^3
&&&
\lim_{qa\ll1}\dfrac{d\sigma}{d\Omega}(\theta)&=\dfrac{4}{9}\dfrac{m^2V_0^2}{\hbar^4}a^6
\end{align}$$
For the $\sin\left(\theta/2\right)\approx1 \to \theta\approx\pi/2$ limit, our amplitude and cross section become
$$\begin{align}
\lim_{\theta\approx\pi/2}f^{(1)}\!\left(\theta\right)&=-\dfrac{1}{4}\dfrac{mV_0}{\hbar^2}k^{-3}
&&&
\lim_{\theta\approx\pi/2}\dfrac{d\sigma}{d\Omega}(\theta)&=\dfrac{1}{16}\dfrac{m^2V_0^2}{\hbar^4}k^{-6}
\end{align}$$










Evaluating the scattering amplitude $f^{(1)}\!\left(\theta\right)$, we have that
$$\begin{align}
\Aboxed{f^{(1)}\!\left(\theta\right)&=-\dfrac{2m}{\hbar^2}\dfrac{V_0a^3}{(qa)^2}\left[\dfrac{\sin qa}{qa}-\cos qa\right]}
\end{align}$$
It also has the differential cross scattering
$$\begin{align}
\dfrac{d\sigma}{d\Omega}&=\dfrac{(2mV_0)^2}{\hbar^4}\dfrac{a^2}{q^4}\left[\dfrac{\sin qa}{qa}-\cos qa\right]^2
\end{align}$$
In the $qa\gg 1$ limit, we have that
$$\begin{align}
\lim_{qa\gg1}f^{(1)}\!\left(\theta\right)&=\dfrac{2mV_0a^3}{\hbar^2}\dfrac{\cos qa}{(qa)^2} &
\lim_{qa\gg1}\dfrac{d\sigma}{d\Omega}&=
\end{align}$$


#### Scattering by Yukawa Potential
Suppose we have a potential given by
$$\begin{align}
V(r)&=V_0\dfrac{e^{-\mu r}}{\mu r}
\end{align}$$
Evaluating the scattering amplitude $f^{(1)}\!\left(\theta\right)$, we have that
$$\begin{align}
\Aboxed{f^{(1)}\!\left(\theta\right)&=-\dfrac{2m}{\hbar^2}\dfrac{V_0}{\mu}\dfrac{1}{\mu^2+q^2}}
&\text{or}&&
\Aboxed{f^{(1)}\!\left(\theta\right)&=-\dfrac{2m}{\hbar^2}\dfrac{V_0}{\mu}\dfrac{1}{\mu^2+4k^2\sin^2\left(\theta/2\right)}}
\end{align}$$

