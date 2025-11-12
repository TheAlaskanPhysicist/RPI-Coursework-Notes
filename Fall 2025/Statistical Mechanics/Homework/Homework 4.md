Author: Stanley Goodwin
Date: October 27th, 2025

---
## Question 1
Consider a hypothetical Fermi system with $N$ particles in volume $V$ and with the density of states $g(\varepsilon)$ given by:
$$\begin{align}
g(\varepsilon)&=\begin{cases}
0, & \varepsilon<0\\
\alpha V, & \varepsilon>0\\
\end{cases}
\end{align}$$
where $\alpha$ is a constant.

---
### Question 1.A
Find the Fermi energy $\varepsilon_F$ and the internal energy of the system at zero temperature.
$$\begin{align}
N&=\lim_{\beta\rightarrow\infty}\int_{-\infty}^\infty\dfrac{1}{e^{\beta(\varepsilon-\mu)}+1}g(\varepsilon)\ d\varepsilon\\
&=\int_{-\infty}^{0}\dfrac{1}{0+1}\cdot0\ d\varepsilon+\int_{0}^{\varepsilon_F}\dfrac{1}{0+1}\alpha V\ d\varepsilon+\int_{0}^\infty\dfrac{1}{\infty+1}\alpha V\ d\varepsilon\\
&=0+\alpha V\int_{0}^{\varepsilon_F}1\ d\varepsilon+0\\
N&=\alpha V\varepsilon_F\\
\Aboxed{\varepsilon_F&=\dfrac{N}{\alpha V}}
\end{align}$$
The internal energy is similarly found:
$$\begin{align}
E&=\lim_{\beta\rightarrow\infty}\int_{-\infty}^\infty\dfrac{\varepsilon}{e^{\beta(\varepsilon-\mu)}+1}g(\varepsilon)\ d\varepsilon\\
&=\int_{-\infty}^{0}\dfrac{\varepsilon}{0+1}\cdot0\ d\varepsilon+\int_{0}^{\varepsilon_F}\dfrac{\varepsilon}{0+1}\alpha V\ d\varepsilon+\int_{0}^\infty\dfrac{\varepsilon}{\infty+1}\alpha V\ d\varepsilon\\
&=0+\alpha V\int_{0}^{\varepsilon_F}\varepsilon\ d\varepsilon+0\\
&=\dfrac{\alpha V}{2}\varepsilon_F^2\\
&=\dfrac{\alpha V}{2}\left(\dfrac{N}{\alpha V}\right)^2\\
\Aboxed{E&=\dfrac{N^2}{2\alpha V}}
\end{align}$$
---
### Question 1.B
Using the Sommerfeld expansion, find the chemical potential, the internal energy, and the specific heat at low temperatures.

The Sommerfeld Expansion is written (at least in my notes):
$$\begin{align}
\int_0^\infty f(\varepsilon)\braket{n(\varepsilon)}\ d\varepsilon&=\int_0^\mu f(\varepsilon)\ d\varepsilon + (kT)^2\dfrac{\pi^2}{6}\left.\dfrac{df}{d\varepsilon}\right|_{\varepsilon=\mu} + O(T^4)
\end{align}$$
For the case of $f(\varepsilon)=g(\varepsilon)$, then:
$$\begin{align}
N&=\int_0^\infty g(\varepsilon)\braket{n(\varepsilon)}\ d\varepsilon\\
&=\int_0^\mu g(\varepsilon)\ d\varepsilon + (kT)^2\dfrac{\pi^2}{6}\left.\dfrac{dg}{d\varepsilon}\right|_{\varepsilon=\mu} + O(T^4)\\
&=\alpha V\mu + (kT)^2\dfrac{\pi^2}{6}\cdot0 + O(T^4)\\
N&=\alpha V\mu\\
\mu&=\dfrac{N}{\alpha V}\\
\Aboxed{\mu&=\varepsilon_F}
\end{align}$$
The internal energy is:
$$\begin{align}
E&=\int_0^\infty \varepsilon g(\varepsilon)\braket{n(\varepsilon)}\ d\varepsilon\\
&=\int_0^\mu \varepsilon g(\varepsilon)\ d\varepsilon + (kT)^2\dfrac{\pi^2}{6}\left.\dfrac{d(\varepsilon g)}{d\varepsilon}\right|_{\varepsilon=\mu} + O(T^4)\\
&=\dfrac{\alpha V}{2}\mu^2 + (kT)^2\dfrac{\pi^2}{6}\alpha V + O(T^4)\\
&=\dfrac{N}{2}\dfrac{\alpha V}{N}\varepsilon_F^2 + (kT)^2\dfrac{\pi^2}{6}\dfrac{\alpha V}{N}N\\
&=\dfrac{N}{2}\dfrac{1}{\varepsilon_F}\varepsilon_F^2 + (kT)^2\dfrac{\pi^2}{6}\dfrac{1}{\varepsilon_F}N\\
\Aboxed{E&=\dfrac{N\varepsilon_F}{2} + (kT)^2\dfrac{\pi^2}{6}\dfrac{N}{\varepsilon_F}}
\end{align}$$
And the specific heat:
$$\begin{align}
C_V&=\left(\dfrac{\partial E}{\partial T}\right)_{V,N}\\
&=\dfrac{\partial}{\partial T}\left(\dfrac{N\varepsilon_F}{2} + (kT)^2\dfrac{\pi^2}{6}\dfrac{N}{\varepsilon_F}\right)\\
&=0+2k^2T\dfrac{\pi^2}{6}\dfrac{N}{\varepsilon_F}\\
\Aboxed{C_V&=\dfrac{\pi^2k^2}{3\varepsilon_F}NT}
\end{align}$$
---
## Question 2
The dimensionality plays a fundamental role in phase transitions and critical phenomena. Its importance also shows in the peculiar phenomenon of Bose-Einstein condensation. Show that there is *no* Bose-Einstein condensation in the one or two dimensional ideal Bose gas with the dispersion relation $\varepsilon(p)=p^2/2m$ at any nonzero temperature. (At $T=0$ , of course, all particles are in the ground state.)

We want to find the expected value of the number of particles:
$$\begin{align}
\braket{N}&=\sum_r\braket{n_r}\\
&\approx\dfrac{L^d}{h^d}\int_0^\infty\dfrac{1}{e^{(\varepsilon(\vec{p})-\mu)/kT}-1}\ d^dp\\
&=\dfrac{L^d}{h^d}\int_0^\infty\dfrac{J(d)\ p^{d-1}}{e^{(\varepsilon(p)-\mu)/kT}-1}\ dp\\
\int_0^\infty g_d(\varepsilon)\dfrac{1}{e^{(\varepsilon-\mu)/kT}-1}\ d\varepsilon&=\dfrac{L^d}{h^d}\int_0^\infty\dfrac{J(d)\ p^{d-1}}{e^{(\varepsilon(p)-\mu)/kT}-1}\ dp\\
g_d(\varepsilon)\ d\varepsilon&=\dfrac{L^d}{h^d}J(d)\ p^{d-1} dp\\
g_d(\varepsilon)&=\dfrac{L^d}{h^d}J(d)\ p^{d-1}\dfrac{dp}{d\varepsilon}
\end{align}$$
We can substitute $\varepsilon=p^2/2m$ to then find:
$$\begin{align}
g_d(\varepsilon)&=\dfrac{L^d}{h^d}J(d)\ p^{d-1}\dfrac{dp}{d\varepsilon}\\
&=\dfrac{L^d}{h^d}J(d)\ p^{d-1}\left(\dfrac{p}{m}\right)^{-1}\\
&=\dfrac{mL^d}{h^d}J(d)\ p^{d-2}\\
&=\dfrac{mL^d}{h^d}J(d)\left(\sqrt{2m\varepsilon}\right)^{d-2}\\
&=\dfrac{1}{2m}\dfrac{mL^d}{h^d}J(d)\left(\sqrt{2m}\right)^{d}\varepsilon^{d/2-1}\\
g_d(\varepsilon)&=\dfrac{J(d)}{2}\left(\sqrt{\dfrac{2mL^2}{h^2}}\right)^{d}\varepsilon^{d/2-1}\\
\Aboxed{g_d(\varepsilon)&\propto\varepsilon^{d/2-1}}
\end{align}$$
Bose-Einstein Condensation can only happen when the state density converges:
$$\begin{align}
\braket{N}_d
&=\int_0^\infty\dfrac{1}{e^{(\varepsilon-\mu)/kT}-1}g_d(\varepsilon)\ d\varepsilon\\
&\propto\int_0^\infty\dfrac{1}{e^{(\varepsilon-\mu)/kT}-1}\varepsilon^{d/2-1}\ d\varepsilon
\end{align}$$
Substituting $z=(\varepsilon-\mu)/kT$, then $\varepsilon=kTz+\mu$ and $d\varepsilon=kT\ dz$:
$$\begin{align}
&\propto\int_{-\mu/kT}^\infty\dfrac{1}{e^{z}-1}(kTz+\mu)^{d/2-1}\ kTdz
\end{align}$$
Our chemical potential being $\mu=0$ must be a condition:
$$\begin{align}
&\approx\int_0^\infty\dfrac{1}{e^{z}-1}(kTz)^{d/2-1}\ kTdz\\
&\propto \int_0^\infty\dfrac{z^{d/2-1}}{e^{z}-1}\ dz\\
&=\Gamma\left(\dfrac{d}{2}\right)\zeta\left(\dfrac{d}{2}\right)\\
\braket{N}_d&\propto\zeta\left(\dfrac{d}{2}\right)
\end{align}$$
The Riemann Zeta function takes the form of:
$$\begin{align}
\zeta(z)&=\sum_{n=0}^\infty\dfrac{1}{z^n}
\end{align}$$
This function converges for $\Re(z)>1$, and with the condition we found:
$$\begin{align}
\braket{N}_d&\propto\zeta\left(\dfrac{d}{2}\right)
\end{align}$$
$$\begin{align}
d=1,\ &\braket{N}_1&&\text{ Diverges}\\
d=2,\ &\braket{N}_2&&\text{ Diverges}\\
d\ge3,\ &\braket{N}_{3+}&&\text{ Converges}\\
\end{align}$$
It must be that $d=1$ and $d=2$ both diverge, and therefore **cannot** form Bose-Einstein Condensate. For condensation to occur, $d\ge3$; that the number of dimensions is more than 3.

---
## Question 3
Find the behavior of the isotherm compressibility, $\kappa_T$ , in as the critical temperature is approached from *above*, i.e., in the $T\rightarrow T_c+0$ limit. This means that you should obtain an expression for $\kappa_T$ as a function of $(T-T_c)$ in the vicinity of the transition temperature. You should review the notes posted on LMS regarding the behavior of the Bose gas just above $T_c$. In particular, use:
$$\begin{align}
\mu(T)\approx-kT\left(\dfrac{3}{4\sqrt\pi}\zeta\left(\tfrac{3}{2}\right)\right)^2\left(\dfrac{T-T_c}{T_c}\right)^2\approx-kT_c\left(\dfrac{3}{4\sqrt\pi}\zeta\left(\tfrac{3}{2}\right)\right)^2\left(\dfrac{T-T_c}{T_c}\right)^2
\end{align}$$
and:
$$\begin{align}
f_{3/2}^-\left(e^{-\alpha}\right)&\approx\zeta\left(\tfrac{3}{2}\right)-2\sqrt\pi\alpha^{1/2} & \alpha&=-\dfrac{\mu}{kT}
\end{align}$$
Also, you will need to employ the basic thermodynamic relation:
$$\begin{align}
-\left(\dfrac{\partial V}{\partial P}\right)_{T,N}&=\dfrac{V^2}{N^2}\left(\dfrac{\partial N}{\partial\mu}\right)_{T,V}
\end{align}$$
The expression for Isotherm Compressibility is:
$$\begin{align}
\kappa_T&=-\dfrac{1}{V}\left(\dfrac{\partial V}{\partial P}\right)_T\\
&=\dfrac{1}{V}\dfrac{V^2}{N^2}\left(\dfrac{\partial N}{\partial\mu}\right)_{T,V}\\
&=\dfrac{V}{N^2}\dfrac{\partial}{\partial\mu}\left(\int_0^\infty g(\varepsilon)\dfrac{1}{e^{(\varepsilon-\mu)/kT}-1}\ d\varepsilon\right)\\
&=\dfrac{V}{N^2}\int_0^\infty g(\varepsilon)\dfrac{\partial}{\partial\mu}\left(\dfrac{1}{e^{(\varepsilon-\mu)/kT}-1}\right)\ d\varepsilon\\
&=\dfrac{V}{N^2}\int_0^\infty g(\varepsilon)\left(\dfrac{-(-\tfrac{1}{kT}e^{(\varepsilon-\mu)/kT})}{(e^{(\varepsilon-\mu)/kT}-1)^2}\right)\ d\varepsilon\\
&=\dfrac{V}{N^2}\dfrac{1}{kT}\int_0^\infty A_3\varepsilon^{1/2}\left(\dfrac{e^{(\varepsilon-\mu)/kT}}{(e^{(\varepsilon-\mu)/kT}-1)^2}\right)\ d\varepsilon\\
\end{align}$$
From the definition of the Bose functions:
$$\begin{align}
f^-_\nu(z)&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty\dfrac{x^{\nu-1}}{z^{-1}e^x-1}\ dx\\
\dfrac{d}{dz}f^-_\nu(z)&=\dfrac{1}{\Gamma(\nu)}\dfrac{d}{dz}\int_0^\infty\dfrac{x^{\nu-1}}{z^{-1}e^x-1}\ dx\\
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty\dfrac{\partial}{\partial z}\dfrac{x^{\nu-1}}{z^{-1}e^x-1}\ dx\\
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty x^{\nu-1}\dfrac{\partial}{\partial z}\left(z^{-1}e^x-1\right)^{-1}\ dx\\
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty -x^{\nu-1}\left(z^{-1}e^x-1\right)^{-2}\dfrac{\partial}{\partial z}(z^{-1}e^x)\ dx\\
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty x^{\nu-1}\left(z^{-1}e^x-1\right)^{-2}(z^{-2}e^x)\ dx\\
\Aboxed{\dfrac{d}{dz}f^-_\nu(z)&=\dfrac{z^{-1}}{\Gamma(\nu)}\int_0^\infty x^{\nu-1}\dfrac{z^{-1}e^x}{(z^{-1}e^x-1)^2}\ dx}
\end{align}$$
For our system:
$$\begin{align}
\dfrac{d}{dz}f^-_\nu(z)&=\dfrac{z^{-1}}{\Gamma(\nu)}\int_0^\infty x^{\nu-1}\dfrac{z^{-1}e^x}{(z^{-1}e^x-1)^2}\ dx\\
&=\dfrac{z^{-1}}{\Gamma(\nu)}\int_0^\infty ({\varepsilon/kT})^{\nu-1}\dfrac{z^{-1}e^{\varepsilon/kT}}{(z^{-1}e^{\varepsilon/kT}-1)^2}\ d\varepsilon/kT\\
&=\dfrac{z^{-1}}{\Gamma(\nu)}\dfrac{1}{(kT)^\nu}\int_0^\infty \varepsilon^{\nu-1}\dfrac{z^{-1}e^{\varepsilon/kT}}{(z^{-1}e^{\varepsilon/kT}-1)^2}\ d\varepsilon\\
\Aboxed{\dfrac{d}{dz}f^-_\nu(e^{\mu/kT})&=\dfrac{e^{-\mu/kT}}{\Gamma(\nu)}\dfrac{1}{(kT)^\nu}\int_0^\infty \varepsilon^{\nu-1}\dfrac{e^{(\varepsilon-\mu)/kT}}{(e^{(\varepsilon-\mu)/kT}-1)^2}\ d\varepsilon}
\end{align}$$
Or for easier use:
$$\begin{align}
e^{\mu/kT}\Gamma(\nu)(kT)^\nu\dfrac{d}{dz}f^-_\nu(e^{\mu/kT})&=\int_0^\infty \varepsilon^{\nu-1}\dfrac{e^{(\varepsilon-\mu)/kT}}{(e^{(\varepsilon-\mu)/kT}-1)^2}\ d\varepsilon\\
\Aboxed{e^{\mu/kT}\Gamma(\tfrac{3}{2})(kT)^{3/2}\dfrac{d}{dz}f^-_{3/2}(e^{\mu/kT})&=\int_0^\infty \varepsilon^{1/2}\dfrac{e^{(\varepsilon-\mu)/kT}}{(e^{(\varepsilon-\mu)/kT}-1)^2}\ d\varepsilon}
\end{align}$$
Our constant out the front is also the following:
$$\begin{align}
A_3&=\dfrac{4\pi V}{2h^3}\left(2m\right)^{3/2}
\end{align}$$
We can then find these kinds of expressions in the original equation:
$$\begin{align}
\kappa_T&=\dfrac{V}{N^2}\dfrac{A_3}{kT}\int_0^\infty \varepsilon^{1/2}\dfrac{e^{(\varepsilon-\mu)/kT}}{(e^{(\varepsilon-\mu)/kT}-1)^2}\ d\varepsilon\\
&=\dfrac{V}{N^2}\dfrac{1}{kT}\dfrac{4\pi V}{2h^3}\left(2m\right)^{3/2}\cdot e^{\mu/kT}\Gamma(\tfrac{3}{2})(kT)^{3/2}\dfrac{d}{dz}f^-_{3/2}(e^{\mu/kT})\\
&=\dfrac{V^2}{N^2}\dfrac{(2\pi m)^{3/2}}{h^3}(kT)^{1/2}\cdot e^{\mu/kT}\dfrac{d}{dz}f^-_{3/2}(e^{\mu/kT})\\
\end{align}$$
With our approximation, we can find this derivative:
$$\begin{align}
e^{\mu/kT}\dfrac{d}{dz}f^-_{3/2}(e^{\mu/kT})&=e^{-\alpha}\dfrac{d}{dz}f^-_{3/2}(e^{-\alpha})\\
&=e^{-\alpha}\dfrac{d}{d\alpha}f^-_{3/2}(e^{-\alpha})\cdot\dfrac{d\alpha}{dz}\\
&=e^{-\alpha}\dfrac{d}{d\alpha}\left(\zeta\left(\tfrac{3}{2}\right)-2\sqrt\pi\alpha^{1/2}\right)\cdot\dfrac{d\alpha}{dz}\left(-\ln z\right)\\
&=e^{-\alpha}\left(-\sqrt\pi\alpha^{-1/2}\right)\cdot\left(-\dfrac{1}{z}\right)\\
&=e^{-\alpha}\left(\sqrt\pi\alpha^{-1/2}\right)\cdot\left(\dfrac{1}{e^{-\alpha}}\right)\\
&=\sqrt\pi\alpha^{-1/2}\\
&=\sqrt\pi\left(-\dfrac{\mu}{kT}\right)^{-1/2}\\
\Aboxed{e^{\mu/kT}\dfrac{d}{dz}f^-_{3/2}(e^{\mu/kT})&=\sqrt\pi\left(-\dfrac{kT}{\mu}\right)^{1/2}}
\end{align}$$
Substituting back in, we get:
$$\begin{align}
\kappa_T&=\dfrac{V^2}{N^2}\dfrac{(2\pi m)^{3/2}}{h^3}(kT)^{1/2}\cdot e^{\mu/kT}\dfrac{d}{dz}f^-_{3/2}(e^{\mu/kT})\\
&=\dfrac{V^2}{N^2}\dfrac{(2\pi m)^{3/2}}{h^3}(kT)^{1/2}\cdot\sqrt\pi\left(-\dfrac{kT}{\mu}\right)^{1/2}\\
\Aboxed{\kappa_T&=\sqrt\pi\dfrac{(2\pi m)^{3/2}}{h^3}\dfrac{V^2}{N^2}\dfrac{kT}{\sqrt{|\mu|}}}
\end{align}$$
We then need to write $\mu$ using our approximation:
$$\begin{align}
\mu(T)\approx-kT\left(\dfrac{3}{4\sqrt\pi}\zeta\left(\tfrac{3}{2}\right)\right)^2\left(\dfrac{T-T_c}{T_c}\right)^2\approx-kT_c\left(\dfrac{3}{4\sqrt\pi}\zeta\left(\tfrac{3}{2}\right)\right)^2\left(\dfrac{T-T_c}{T_c}\right)^2
\end{align}$$
And so:
$$\begin{align}
\kappa_T&=\sqrt\pi\dfrac{(2\pi m)^{3/2}}{h^3}\dfrac{V^2}{N^2}kT\left(kT_c\left(\dfrac{3}{4\sqrt\pi}\zeta\left(\tfrac{3}{2}\right)\right)^2\left(\dfrac{T-T_c}{T_c}\right)^2\right)^{-1/2}\\
&=\sqrt\pi\dfrac{(2\pi m)^{3/2}}{h^3}\dfrac{V^2}{N^2}kT(kT_c)^{-1/2}\left(\dfrac{4\sqrt\pi}{3}\dfrac{1}{\zeta\left(\tfrac{3}{2}\right)}\right)\left(\dfrac{T_c}{T-T_c}\right)\\
\kappa_T&=\dfrac{4\pi}{3\zeta\left(\tfrac{3}{2}\right)}\dfrac{(2\pi m)^{3/2}}{h^3}\dfrac{V^2}{N^2}\sqrt{kT_c}\cdot\dfrac{T}{T-T_c}\\
\Aboxed{\kappa_T&\approx\dfrac{4\pi}{3\zeta\left(\tfrac{3}{2}\right)}\dfrac{(2\pi m)^{3/2}}{h^3}\dfrac{V^2}{N^2}\dfrac{\sqrt{kT_c}}{T}\cdot\left(T-T_c\right)^{-1}}
\end{align}$$
The compressibility is inversely proportional to the difference of our temperature and the gas's critical temperature.

---
## Question 4
Consider the simple model for a one-dimensional solid consisting of $N$ atoms of identical mass $m$ along a chain. Atoms are connected only with nearest-neighbor atoms by "springs" with spring constant $\kappa$. The equilibrium separation between atoms (i.e., the lattice constant) is $a$. The springs are relaxed in equilibrium and we allow only for longitudinal oscillations. For simplicity, use periodic boundary conditions, $u_{j+N}=u_j$, where $u_j$ is the displacement of the $j$th atom, measured from its equilibrium position.

---
### Question 4.A
Show that the equation of motion for the displacements is
$$\begin{align}
m\ddot{u}_j&=\kappa\left(u_{j+1}+u_{j-1}-2u_{j}\right) & j&=1,2,\dots,N
\end{align}$$
Well I assume we'd need to construct the Hamiltonian/Lagrangian, and so:
$$\begin{align}
T&=\sum_{j=1}^N\dfrac{1}{2}m\dot{u}_j^2\\
V&=\sum_{j=1}^N\dfrac{1}{2}\kappa\left(u_{j+1}-u_{j}\right)^2\\
\end{align}$$
We could use the Hamiltonian here, but I'd actually prefer the Lagrangian:
$$\begin{align}
L&=\sum_{j=1}^N\dfrac{1}{2}m\dot{u}_j^2-\sum_{j=1}^N\dfrac{1}{2}\kappa\left(u_{j+1}-u_{j}\right)^2
\end{align}$$
Then with the Euler-Lagrange Equations, we get:
$$\begin{align}
\dfrac{d}{dt}\dfrac{\partial L}{\partial \dot{u}_j}&=m\ddot{u}_j\\
\dfrac{\partial L}{\partial u_j}&=-\dfrac{1}{2}\kappa\dfrac{\partial}{\partial u_j}\left(\left(u_{j+1}-u_{j}\right)^2+\left(u_{j}-u_{j-1}\right)^2\right)\\
&=-\kappa\left(-[u_{j+1}-u_{j}]+u_{j}-u_{j-1}\right)\\
&=-\kappa\left(-u_{j+1}-u_{j-1}+2u_{j}\right)\\
\Aboxed{m\ddot{u}_j&=\kappa\left(u_{j+1}u_{j-1}-2u_{j}\right)}
\end{align}$$
---
### Question 4.B
Solve the above set of equation by means of complex Fourier series, yielding the normal modes and the spectrum. In particular, show that the frequency – wave-number dispersion relation is given by:
$$\begin{align}
\omega(k)&=2\sqrt{\dfrac{\kappa}{m}}\left|\sin\left(\dfrac{ka}{2}\right)\right|
\end{align}$$
where $k=\dfrac{2\pi}{Na}n$, where $n=-\dfrac{N}{2},\dots,\dfrac{N}{2}$ (assumed even $N$ for simplicity).

Let the solution be a plane wave (we just had this question on the Quantum Mechanics exam):
$$\begin{align}
u_j(t)=Ae^{i(\omega t-k(aj))}
\end{align}$$
Substituting, we get:
$$\begin{align}
m\dfrac{\partial^2}{\partial t^2}u_j&=\kappa\left(u_{j+1}u_{j-1}-2u_{j}\right)\\
\dfrac{m}{\kappa}\dfrac{\partial^2}{\partial t^2}\left(Ae^{i\omega t}e^{-ikaj}\right)&=Ae^{i\omega t}e^{-ika(j+1)}+Ae^{i\omega t}e^{-ika(j-1)}-2Ae^{i\omega t}e^{-ikaj}\\
\dfrac{m}{\kappa}(i\omega)^2e^{-ikaj}&=e^{-ika(j+1)}+e^{-ika(j-1)}-2e^{-ikaj}\\
\dfrac{m}{\kappa}\omega^2&=2-2\dfrac{e^{+ika}+e^{-ika}}{2}\\
\dfrac{m}{\kappa}\omega^2&=2-2\cos(ka)\\
\dfrac{m}{\kappa}\omega^2&=4\dfrac{1-\cos(ka)}{2}\\
\omega^2&=4\dfrac{\kappa}{m}\sin^2\left(\dfrac{ka}{2}\right)\\
\Aboxed{\omega(k)&=2\sqrt{\dfrac{\kappa}{m}}\left|\sin\left(\dfrac{ka}{2}\right)\right|}
\end{align}$$
---
### Question 4.C
From the above dispersion relation it follows that for small $k$ values we can use $\omega(k)=ck$, where $c$ is the speed of longitudinal vibrations in this solid. Obtain the **low-temperature** behavior of the specific heat of this one-dimensional solid of size $L=Na$ in the Debye approximation.

Quickly, the speed of propagation is an equivalence:
$$\begin{align}
ck&=2\sqrt{\dfrac{\kappa}{m}}\dfrac{ka}{2} &\implies&& c&=\sqrt{\dfrac{\kappa}{m}}a
\end{align}$$
The wavenumber and angular frequency is found as:
$$\begin{align}
k&=\dfrac{2\pi}{Na}n  & \implies&& \omega&=c\dfrac{2\pi}{Na}n 
\end{align}$$
The Debye approximation maximum values are then:
$$\begin{align}
k_D&=\dfrac{\pi}{a}  & \implies&& \omega_D&=c\dfrac{\pi}{a} 
\end{align}$$
We find the density of states as:
$$\begin{align}
g(\omega)&=\dfrac{Na}{\pi}\dfrac{dk}{d\omega}\\
&=N\dfrac{a}{\pi}\left(\dfrac{1}{c}\right)\\
&=N\dfrac{1}{k_Dc}\\
\Aboxed{g(\omega)&=\dfrac{N}{\omega_D}}
\end{align}$$
The internal energy has the form:
$$\begin{align}
U&=\int_0^{\omega_D} \dfrac{\hbar\omega}{e^{\beta\hbar\omega}-1}g(\omega)\ d\omega\\
&=\dfrac{(kT)^2}{\hbar}\int_0^{\omega_D} \dfrac{\beta\hbar\omega}{e^{\beta\hbar\omega}-1}\dfrac{N}{\omega_D}\ \beta\hbar d\omega\\
&=\dfrac{(kT)^2}{\hbar}\dfrac{N}{\omega_D}\int_0^{\omega_D} \dfrac{\beta\hbar\omega}{e^{\beta\hbar\omega}-1}\ \beta\hbar d\omega
\end{align}$$
Let $z=\beta\hbar\omega$, then $dz=\beta\hbar d\omega$:
$$\begin{align}
U&=\dfrac{(kT)^2}{\hbar}\dfrac{N}{\omega_D}\int_0^{\omega_D} \dfrac{\beta\hbar\omega}{e^{\beta\hbar\omega}-1}\ \beta\hbar d\omega\\
&=\dfrac{(kT)^2}{\hbar}\dfrac{N}{\omega_D}\int_0^{\beta\hbar\omega_D} \dfrac{z}{e^{z}-1}\ dz
\end{align}$$
For low temperature $T\ll1$, then $\beta\gg1$, so we can approximate the top bound as $\infty$:
$$\begin{align}
E&\approx\dfrac{(kT)^2}{\hbar}\dfrac{N}{\omega_D}\int_0^{\infty} \dfrac{z}{e^{z}-1}\ dz\\
&=\dfrac{(kT)^2}{\hbar}\dfrac{N}{\omega_D}\Gamma(2)\zeta(2)\\
&=\dfrac{(kT)^2}{\hbar}\dfrac{N}{\omega_D}\cdot1\cdot\dfrac{\pi^2}{6}\\
&=\dfrac{\pi^2}{6}\dfrac{(kT)^2}{\hbar}\dfrac{N}{\omega_D}\\
&=\dfrac{\pi^2}{6}\dfrac{(kT)^2}{\hbar}\dfrac{Na}{c\pi}\\
\Aboxed{E&=\dfrac{\pi}{6}\dfrac{(kT)^2}{\hbar c}Na}
\end{align}$$
Then we differentiate this with respect to temperature:
$$\begin{align}
C_V&=\left(\dfrac{\partial E}{\partial T}\right)_V\\
&\approx\dfrac{\partial}{\partial T}\left(\dfrac{\pi}{6}\dfrac{(kT)^2}{\hbar c}Na\right)\\
\Aboxed{C_V&=\dfrac{\pi}{3}\dfrac{Nak^2}{\hbar c}T}
\end{align}$$
So long as $\dfrac{\hbar\omega}{kT}\gg 1$, which is satisfied in the low-temperature limit.

---
## Question 5
Obtain an estimate for the:
### Question 5.A
Fermi energy and Fermi temperature in copper (assume one conduction or "free" electron per atom). For the mass density of copper use $\rho=9\dfrac{\text{g}}{\text{cm}^3}$, and the atomic mass is $63.5$g/mol.

The Fermi Energy is the following (from lecture):
$$\begin{align}
\varepsilon_F&=\dfrac{h^2}{2m}\left(\dfrac{3n_0}{8\pi}\right)^{2/3}
\end{align}$$
We need to calculate number density, so:
$$\begin{align}
n_0&=\dfrac{N}{V}=\dfrac{N}{m}\cdot\dfrac{m}{V}=\left(\dfrac{m}{N}\right)^{-1}\cdot\dfrac{m}{V}
\end{align}$$
From our variables on top, we can see:
$$\begin{align}
\dfrac{m}{V}&=9\dfrac{\text{g}}{\text{cm}^3}\\
&=9\cdot10^6\cdot10^{-3}\dfrac{10^3\text{g}}{10^6\text{cm}^3}\\
\Aboxed{\dfrac{m}{V}&=9\cdot10^3\dfrac{\text{kg}}{\text{m}^3}}
\end{align}$$
$$\begin{align}
\left(\dfrac{m}{N}\right)^{-1}&=\dfrac{1}{63.5}\dfrac{\text{mol}}{g}\\
&=1.575\cdot10^{-2}\cdot10^3\dfrac{\text{mol}}{10^3g}\\
\Aboxed{\left(\dfrac{m}{N}\right)^{-1}&=1.575\cdot10^1\dfrac{\text{mol}}{\text{kg}}}
\end{align}$$
We need to convert $\text{mol}$ of copper to electrons, but we assume 1:1, and so:
$$\begin{align}
\Aboxed{\left(\dfrac{m}{N}\right)^{-1}&=9.483\cdot10^{24}\dfrac{\text{1}}{\text{kg}}}
\end{align}$$
The product of these 2 give the number density:
$$\begin{align}
n_0&=\left(\dfrac{m}{N}\right)^{-1}\cdot\dfrac{m}{V}\\
&=9.483\cdot10^{24}\dfrac{1}{\text{kg}}\cdot9\cdot10^3\dfrac{\text{kg}}{\text{m}^3}\\
\Aboxed{n_0&=8.535\cdot10^{28}\dfrac{1}{\text{m}^3}}
\end{align}$$
We can then find the Fermi Energy as:
$$\begin{align}
\varepsilon_F&=\dfrac{h^2}{2m}\left(\dfrac{3n_0}{8\pi}\right)^{2/3}\\
&=\dfrac{1}{2}\left(\dfrac{3}{8\pi}\right)^{2/3}\dfrac{(hc)^2}{mc^2}n_0^{2/3}\\
&=\dfrac{1}{2}\left(\dfrac{3}{8\pi}\right)^{2/3}\dfrac{(1240\text{ eV}\text{ nm})^2}{0.511
\cdot10^6\text{ eV}}(8.535\cdot10^{28})^{2/3}\dfrac{1}{\text{m}^2}\\
&=7.07\cdot10^{18}\dfrac{\text{ eV}^2\text{ nm}^2}{\text{ eV}}\dfrac{1}{10^{18}\text{nm}^2}\\
\Aboxed{\varepsilon_F&=7.070\text{ eV}}
\end{align}$$
The Fermi Temperature is super simple from here, and so:
$$\begin{align}
T_F&=\dfrac{\varepsilon_F}{k}\\
&=\dfrac{7.070\text{ eV}}{8.617\cdot10^{-5}\text{ eV}/\text{K}}\\
\Aboxed{T_F&=8.205\cdot10^4\text{ K}}
\end{align}$$
---
### Question 5.B
Critical temperature for the Bose-Einstein condensation in an ideal $\text{He}^4$ "gas" with density $\rho=0.145\dfrac{\text{g}}{\text{cm}^3}$. The atomic mass is $4$g/mol.

We need to calculate number density, so:
$$\begin{align}
n&=\left(\dfrac{m}{N}\right)^{-1}\cdot\dfrac{m}{V}
\end{align}$$
These come out to:
$$\begin{align}
\Aboxed{\dfrac{m}{V}&=1.45\cdot10^2\dfrac{\text{kg}}{\text{m}^3}}
\end{align}$$
$$\begin{align}
\Aboxed{\left(\dfrac{m}{N}\right)^{-1}&=2.5\cdot10^2\dfrac{\text{mol}}{\text{kg}}=1.506\cdot10^{26}\dfrac{1}{\text{kg}}}
\end{align}$$
We then find the number density as:
$$\begin{align}
\Aboxed{n&=2.183\cdot10^{28}\dfrac{1}{\text{m}^3}}
\end{align}$$
The critical temperature is found to be:
$$\begin{align}
T_c&=\left(\dfrac{n}{\zeta(3/2)}\right)^{2/3}\dfrac{h^2}{2\pi m k}\\
&=\left(\dfrac{n}{\zeta(3/2)}\right)^{2/3}\dfrac{(hc)^2}{2\pi (mc^2) k}\\
&=\left(\dfrac{2.183\cdot10^{28}}{\zeta(3/2)}\right)^{2/3}\dfrac{1}{\text{m}^2}\dfrac{(1240\text{ eV}\text{ nm})^2}{2\pi (3.727\cdot10^{9}\text{ eV})(8.617\cdot10^{-5}\text{ eV}/\text{K})}\\
&=\dfrac{5.952}{\zeta(3/2)^{2/3}}\dfrac{1}{\text{nm}^2}\dfrac{\text{ eV}^2\text{ nm}^2}{\text{ eV}\text{ eV}/\text{K}}\\
\Aboxed{T_c&=3.138\text{ K}}
\end{align}$$
---
### Question 5.C
Debye temperature in copper (use the parameters given in (a) and the effective sound velocity $c\approx4000\dfrac{\text{m}}{\text{s}}$.

The Debye Temperature is pretty simple:
$$\begin{align}
k\Theta_D&=\hbar\omega_D
\end{align}$$
From my lecture notes, the Debye frequency is:
$$\begin{align}
\omega_D&\approx\left(6\pi^2n_0\right)^{1/3}c\\
&=\left(6\pi^2\cdot8.535\cdot10^{28}\right)^{1/3}\dfrac{1}{\text{m}}\left(4000\dfrac{\text{m}}{\text{s}}\right)\\
\Aboxed{\omega_D&=6.865\cdot10^{13}\dfrac{\text{rad}}{\text{s}}}
\end{align}$$
We can then substitute this in for the Debye Temperature:
$$\begin{align}
\Theta_D&=\dfrac{\hbar}{k}\omega_D\\
&=\dfrac{4.136\cdot10^{-15}\text{ eV}\text{ s}}{8.617\cdot10^{-5}\text{ eV}/\text{K}}6.865\cdot10^{13}\dfrac{\text{rad}}{\text{s}}\\
&=3.294\cdot10^3\dfrac{\text{ eV}\text{ s}}{\text{ eV}/\text{K}}\dfrac{\text{rad}}{\text{s}}\\
\Aboxed{\Theta_D&=3.294\cdot10^3\text{ K}}
\end{align}$$
