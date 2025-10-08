Author: Stanley Goodwin
Date: October 13th, 2025

---
## Question 1
Calculate the matrix elements $\bra{\vec{x}_1\vec{x}_2\dots\vec{x}_N}e^{-\beta\hat{H}}\ket{\vec{x}_1\vec{x}_2\dots\vec{x}_N}$, where:
$$\begin{align}
\bra{\vec{x}_1\vec{x}_2\dots\vec{x}_N}e^{-\beta\hat{H}}\ket{\vec{x}_1\vec{x}_2\dots\vec{x}_N}&=\dfrac{1}{N!}\dfrac{1}{\lambda^{3N}}\sum_P\delta_Pf(P\vec{x}_1-\vec{x}_1)f(P\vec{x}_1-\vec{x}_1)\cdots f(P\vec{x}_N-\vec{x}_N)
\end{align}$$
$$\begin{align}
f(u)&=e^{-\tfrac{\pi u^2}{\lambda^2}}\\
\lambda&=\sqrt{\dfrac{h^2}{2\pi mkT}}
\end{align}$$
And $\delta_P=1$ for Bosons and $\delta_P=(-1)^{[P]}$ for Fermions.

In order to study lowest-order quantum corrections to classical non-interacting systems:
$$\begin{align}
\lambda^3\dfrac{N}{V}\ll1
\end{align}$$
it is sufficient to consider only the trivial permutation and 2-particle permutations in the above:
$$\begin{align}
\bra{\vec{x}_1\vec{x}_2\dots\vec{x}_N}e^{-\beta\hat{H}}\ket{\vec{x}_1\vec{x}_2\dots\vec{x}_N}&=\dfrac{1}{N!}\dfrac{1}{\lambda^{3N}}\left(1\pm \sum_{i<j}f^2(r_{ij})+\dots\right)
\end{align}$$
where $r_{ij}=\left|\vec{x}_i-\vec{x}_j\right|$, and the $\pm$ sign are for Bosons/Fermions.

---
### Question 1.A
Find the equation of state in this first order approximation.



---
### Question 1.B
Find $E$ as a function of $T,V$, and $N$ in the same approximation.



---
## Question 2
We defined in class the Fermi-Dirac ($+$) and Bose-Einstein ($-$) integrals:
$$\begin{align}
f^{\pm}_\nu(z)&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty\dfrac{x^{\nu-1}}{z^{-1}e^{x}\pm1}dx
\end{align}$$
Prove that for $z\ll1$, then:
$$\begin{align}
f^{\pm}_\nu(z)&=\sum_{k=1}^\infty (\mp1)^{k-1}\dfrac{z^k}{k^\nu}
\end{align}$$
Suspiciously looks like the Riemann Zeta function or Dirichlet Eta function ($z=1$).

For small $z$, we'll probably want to use some form of geometric series, and so:
$$\begin{align}
f^{\pm}_\nu(z)
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty\dfrac{x^{\nu-1}}{z^{-1}e^{x}\pm1}dx\\
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty\dfrac{x^{\nu-1}}{z^{-1}e^{x}\pm1}\dfrac{ze^{-x}}{ze^{-x}}dx\\
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty x^{\nu-1}ze^{-x}\cdot\dfrac{1}{1\pm ze^{-x}}dx\\
\end{align}$$
The denominator's $|z|<1$, and $e^{-x}\lt1$, and so we can do a geometric series:
$$\begin{align}
f^{\pm}_\nu(z)
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty x^{\nu-1}ze^{-x}\cdot\dfrac{1}{1\pm ze^{-x}}dx\\
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty x^{\nu-1}ze^{-x}\cdot\sum_{k=0}^\infty\left(\mp ze^{-x}\right)^k\ dx\\
&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty x^{\nu-1}ze^{-x}\cdot\sum_{k=0}^\infty(\mp1)^kz^ke^{-kx}\ dx\\
&=\dfrac{1}{\Gamma(\nu)}\sum_{k=0}^\infty\int_0^\infty x^{\nu-1}(\mp1)^kz^{k+1}e^{-(k+1)x}\ dx\\
&=\dfrac{1}{\Gamma(\nu)}\sum_{k=1}^\infty\int_0^\infty x^{\nu-1}(\mp1)^{k-1}z^{k}e^{-kx}\ dx\\
&=\dfrac{1}{\Gamma(\nu)}\sum_{k=1}^\infty(\mp1)^{k-1}z^{k}\int_0^\infty x^{\nu-1}e^{-kx}\ dx\\
&=\dfrac{1}{\Gamma(\nu)}\sum_{k=1}^\infty(\mp1)^{k-1}z^{k}\int_0^\infty\dfrac{1}{k^{\nu-1}}u^{\nu-1}e^{-u}\ \dfrac{du}{k}\\
&=\dfrac{1}{\Gamma(\nu)}\sum_{k=1}^\infty(\mp1)^{k-1}z^{k}\dfrac{1}{k^\nu}\int_0^\infty u^{\nu-1}e^{-u}du\\
&=\dfrac{1}{\Gamma(\nu)}\sum_{k=1}^\infty(\mp1)^{k-1}z^{k}\dfrac{1}{k^\nu}\Gamma(\nu)\\
\Aboxed{f^{\pm}_\nu(z)&=\sum_{k=1}^\infty(\mp1)^{k-1}\dfrac{z^{k}}{k^\nu}}
\end{align}$$
---
## Question 3
Working in the grand-canonical ensemble, we obtained in class for the ideal non relativistic 
Fermi $(+)$ and Bose $(-)$ systems with spin $s$:
$$\begin{align}
N&=\left(2s+1\right)\dfrac{V}{\lambda^3}f^{\pm}_{3/2}(z)\\
E&=\dfrac{3}{2}kT\left(2s+1\right)\dfrac{V}{\lambda^3}f^{\pm}_{5/2}(z)\\
\end{align}$$
where $z=e^{\mu/kT}$ and $\lambda=\sqrt{\dfrac{h^2}{2\pi mkT}}$.

---
### Question 3.A
Obtain the energy $E$ as a function of $T,V,N$, and the equation of state up to first order in $\lambda^3\dfrac{N}{V}$. Note that after using the small $z$ approximation for $f_\nu^\pm(z)$, $z$ must be eliminated from the equations in favor of $\lambda^3\dfrac{N}{V}$. To this end you should use the first equation above for $N$. How do your final results compare with those of Problem 1.(a) and (b)?



---
### Question 3.B
Using $E(T,V,N)$, obtain the specific heat of the quantum gas up to the same order in $\lambda^3\dfrac{N}{V}$.



---
## Question 4
Consider $\text{He}$ gas at room temperature and atmospheric pressure, and determine whether the classical approximation for the equation of state $(PV=NkT)$ is justified or not. Repeat the above considerations for the electron "gas" at room temperature.

