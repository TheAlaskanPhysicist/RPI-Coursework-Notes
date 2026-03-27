Stanley Goodwin, 2/24/2026

---
### Question 1
Calculate the density of states $\rho(E)$ for a free particle in a three-dimensional box of size $L$.

For the typical case of a one-dimensional box with periodic boundary conditions:
$$\begin{align}
\psi_n(x)&\propto\sin\left(\dfrac{2n\pi}{L}x\right) & k&=\dfrac{2n\pi}{L} & E_{n}&=\dfrac{\hbar^2k^2}{2m}=\dfrac{(2\pi\hbar)^2}{2mL^2}n^2=\dfrac{h^2}{2mL^2}n^2
\end{align}$$
We effectively have this solution in each coordinate (independently), and so:
$$\begin{align}
\vec{k}&=\dfrac{2\pi}{L}\vec{n} & E(\vec{n})&=\dfrac{h^2}{2mL^2}\left|\vec{n}\right|^2
\end{align}$$
Define an cumulative density of state function $N(\varepsilon\le E)$:
$$\begin{align}
N(\varepsilon\le E)&=\sum_{\left|\vec{n}\right|^2=\tfrac{L^2}{h^2}\cdot2mE} 1
\end{align}$$
In the continuum limit of states (arbitrarily high momentum eigenstates):
$$\begin{align}
N(\varepsilon\le E)&\simeq\int_0^E\ dV=\dfrac{4}{3}\pi|\vec{n}|^3
\end{align}$$
This is the full volume since the solution can have both positive and negative momenta.

If we solve for $|\vec{n}|$ in terms of energy, we can find an expression for the CDF:
$$\begin{align}
\left|\vec{n}\right|&=\dfrac{L}{h}\sqrt{2mE} &\implies&& N(\varepsilon\le E)&\simeq\dfrac{4}{3}\pi\cdot\dfrac{L^3}{h^3}(2m)^{3/2}E^{3/2}
\end{align}$$
The differential of the CDF gives the PDF (in our case, the density of states):
$$\begin{align}
N(\varepsilon\le E)&\simeq\dfrac{2^{7/2}\pi}{3}\dfrac{L^3m^{3/2}}{h^3}E^{3/2} &\implies&&\left.\dfrac{dN}{dE}\right|_{E}=\rho(E)&=2^{5/2}\pi\dfrac{L^3m^{3/2}}{h^3}E^{1/2}
\end{align}$$
Since our density of states is independent of $\theta,\phi$, we can write the radial density of state:
$$\begin{align}
\dfrac{d\rho(E)}{d\Omega}&=\dfrac{2^{5/2}\pi}{4\pi}\dfrac{L^3m^{3/2}}{h^3}E^{1/2}
\end{align}$$
Therefore, we have the following density of states:
$$\begin{align}
\Aboxed{\rho(E)&=2^{5/2}\pi\dfrac{L^3m^{3/2}}{h^3}E^{1/2}}
&& \substack{\text{Constant} \\ \text{Separated}} &
\Aboxed{\rho(E)&=2\pi\dfrac{(2mL^2)^{3/2}}{h^3}E^{1/2}}
&& \substack{\text{Written Like} \\ \text{Energy Term}} \\
\Aboxed{\rho(E)&=\dfrac{1}{\pi^2\sqrt{2}}\dfrac{L^3m^{3/2}}{\hbar^3}E^{1/2}}
&& \substack{\text{In Terms} \\ \text{Of }\hbar\text{ Instead}} &
\Aboxed{\rho(E)&=\dfrac{1}{4\pi^2}\dfrac{(2mL^2)^{3/2}}{\hbar^3}E^{1/2}}
&& \substack{\text{Written Like} \\ \text{Energy Term} \\ \text{With }\hbar\text{ Instead}}
\end{align}$$
Our radial density of states are similarly written:
$$\begin{align}
\Aboxed{\dfrac{d\rho}{d\Omega}&=\sqrt{2}\dfrac{L^3m^{3/2}}{h^3}E^{1/2}}
&& \substack{\text{Constant} \\ \text{Separated}} &
\Aboxed{\dfrac{d\rho}{d\Omega}&=\dfrac{1}{2}\dfrac{(2mL^2)^{3/2}}{h^3}E^{1/2}}
&& \substack{\text{Written Like} \\ \text{Energy Term}} \\
\Aboxed{\dfrac{d\rho}{d\Omega}&=\dfrac{1}{2^{5/2}\pi^3}\dfrac{L^3m^{3/2}}{\hbar^3}E^{1/2}}
&& \substack{\text{In Terms} \\ \text{Of }\hbar\text{ Instead}} &
\Aboxed{\dfrac{d\rho}{d\Omega}&=\dfrac{1}{16\pi^3}\dfrac{(2mL^2)^{3/2}}{\hbar^3}E^{1/2}}
&& \substack{\text{Written Like} \\ \text{Energy Term} \\ \text{With }\hbar\text{ Instead}}
\end{align}$$
---
### Question 2
Show that, in the limit that $\lim_{r\to\infty}f(\vec{x})g(\vec{x})=0$, the following is true:
$$\begin{align}
\int f(\vec{x})\vec\nabla g(\vec{x})\ d^3x&=-\int g(\vec{x})\vec\nabla f(\vec{x})\ d^3x
\end{align}$$
To be more precise, the product vanishes faster than $\sim 1/r^2$ as $r\to\infty$.

We can take the gradient of the function product using the chain rule:
$$\begin{align}
\vec\nabla\left(f(\vec{x})g(\vec{x})\right)&=g(\vec{x})\vec\nabla f(\vec{x})+f(\vec{x})\vec\nabla g(\vec{x})\\
\end{align}$$
Now we can integrate both sides over a volume:
$$\begin{align}
\int\vec\nabla\left(f(\vec{x})g(\vec{x})\right)\ d^3x&=\int g(\vec{x})\vec\nabla f(\vec{x})\ d^3x+\int f(\vec{x})\vec\nabla g(\vec{x})\ d^3x
\end{align}$$
On the left side, we can use the Divergence Theorem:
$$\begin{align}
\int_\Omega\vec\nabla F\ dV &=\oint_{\partial\Omega}F\ d\vec{S} &\implies&&
\int_{V}\vec\nabla\left(f(\vec{x})g(\vec{x})\right)\ dV &=\oint_{\partial V}f(\vec{x})g(\vec{x})\ d\vec{S}
\end{align}$$
When we take the limit as $r\to\infty$, we find that:
$$\begin{align}
\lim_{r\to\infty}\oint_{\partial V}f(\vec{x})g(\vec{x})\ d\vec{S}=\oint_{\partial V}\lim_{r\to\infty} f(\vec{x})g(\vec{x})\ d\vec{S}&=0 &\implies&&
\int_{V}\vec\nabla\left(f(\vec{x})g(\vec{x})\right)\ dV&=0
\end{align}$$
The left side is just zero in our original expression, and so:
$$\begin{align}
\int g(\vec{x})\vec\nabla f(\vec{x})\ d^3x+\int f(\vec{x})\vec\nabla g(\vec{x})\ d^3x&=0
\end{align}$$
We can then rearrange to get the result we would like:
$$\begin{align}
\lim_{r\to\infty} && \Aboxed{\int f(\vec{x})\vec\nabla g(\vec{x})\ d^3x&=-\int g(\vec{x})\vec\nabla f(\vec{x})\ d^3x}
\end{align}$$
---
### Question 3
Calculate the integral:
$$\begin{align}
\int_{\mathbb{R}^3}e^{-i\vec{q}\cdot\vec{x}}e^{-Zr/a_0}\ d^3x
\end{align}$$
We can represent both $\vec{q}$ and $\vec{x}$ in spherical coordinates. Let $\vec{q}$ be on the $z$-axis without loss of generality, since the angular parts are relative to the position, so we can always realign $\vec{q}$:
$$\begin{align}
\vec{x}&=r\sin\theta\cos\phi\ \hat{x}+r\sin\theta\sin\phi\ \hat{y}+r\cos\theta\ \hat{z} & \vec{q}&=q\hat{z}\\
\vec{q}\cdot\vec{x}&=qr\cos\theta
\end{align}$$
Writing our integral in spherical coordinates, and substituting the inner product:
$$\begin{align}
I&=\int_0^{2\pi}\int_0^\pi\int_0^\infty e^{-i(qr\cos\theta)}e^{-Zr/a_0}\ \left(r^2\sin\theta\ dr\ d\theta\ d\phi\right)
\end{align}$$
The azimuthal integration is trivial, and the polar integral is an integral found on a table:
$$\begin{align}
I&=\int_0^\infty dr\ r^2e^{-Zr/a_0}\int_0^\pi\  e^{-iqr\cos\theta}\sin\theta\ d\theta\int_0^{2\pi}d\phi\\
&=\int_0^\infty dr\ r^2e^{-Zr/a_0}\cdot\dfrac{2\sin\left(qr\right)}{qr}\cdot2\pi\\
I&=\dfrac{4\pi}{q}\int_0^\infty re^{-Zr/a_0}\sin\left(qr\right)\ dr
\end{align}$$
This is also a well-known integral because of complex analysis:
$$\begin{align}
\int_0^\infty re^{-\alpha r}\sin\left(\beta r\right)\ dr&=\dfrac{2\alpha\beta}{|\alpha+i\beta|^4} & \alpha&=Z/a_0 & \beta&=q
\end{align}$$
Our integral can be simplified more:
$$\begin{align}
I&=\dfrac{4\pi}{q}\dfrac{2(Z/a_0)(q)}{|(Z/a_0)+i(q)|^4}\\
&=8\pi\dfrac{a_0^4}{a_0^4}\dfrac{Z/a_0}{|Z/a_0+iq|^4}\\
\Aboxed{I&=8\pi\dfrac{Za_0^3}{|Z+iqa_0|^4}}
\end{align}$$
One last thing we can do is emphasize that there is a pole at a certain value of $q$:
$$\begin{align}
\Aboxed{I&=\dfrac{8\pi Z/a_0}{|q-iZ/a_0|^4}}
\end{align}$$
Or if we want to make it explicit that this integral is real-valued:
$$\begin{align}
\Aboxed{I&=8\pi\dfrac{Za_0^3}{|Z^2+q^2a_0^2|^2}}
\end{align}$$
