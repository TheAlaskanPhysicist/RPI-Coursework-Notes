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

I'm not sure how to approach this problem, but I'll start with calculating the partition function $Z$:
$$\begin{align}
Z&=\int\bra{\vec{x}_1\vec{x}_2\dots\vec{x}_N}e^{-\beta\hat{H}}\ket{\vec{x}_1\vec{x}_2\dots\vec{x}_N}\ dx^3_1dx^3_2\dots dx^3_N\\
&=\dfrac{1}{N!}\dfrac{1}{\lambda^{3N}}\int\left(1\pm \sum_{i<j}f^2(r_{ij})+\dots\right)\ dx^3_1dx^3_2\dots dx^3_N\\
&\approx\dfrac{1}{N!}\dfrac{1}{\lambda^{3N}}\int\left(1\pm \sum_{i<j}e^{-2\tfrac{\pi r_{ij}^2}{\lambda^2}}\right)\ dx^3_1dx^3_2\dots dx^3_N\\
&=\dfrac{1}{N!}\dfrac{1}{\lambda^{3N}}\int1\ dx^3_1dx^3_2\dots dx^3_N\pm \sum_{i<j}\dfrac{1}{N!}\dfrac{1}{\lambda^{3N}}\int e^{-2\tfrac{\pi r_{ij}^2}{\lambda^2}}\ dx^3_1dx^3_2\dots dx^3_N\\
&=\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\pm \sum_{i<j}\dfrac{1}{N!}\dfrac{1}{\lambda^{3N}}\int e^{-2\tfrac{\pi(\vec{x}_i-\vec{x}_j)^2}{\lambda^2}}\ dx^3_1dx^3_2\dots dx^3_N\\
&=\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\pm \sum_{i<j}\dfrac{1}{N!}\dfrac{V^{N-2}}{\lambda^{3N}}\int e^{-2\tfrac{\pi(\vec{x}_i-\vec{x}_j)^2}{\lambda^2}}\ dx^3_idx^3_j
\end{align}$$
Since we have 2 vector inputs, we'll want to transform it into something more manageable.

Let $\vec{r}$ be the difference vector from the mean vector $\vec{R}$. We can then see that:
$$\begin{align}
\vec{x}_i&=\vec{R}+\dfrac{1}{2}\vec{r} & \vec{x}_j&=\vec{R}-\dfrac{1}{2}\vec{r}
\end{align}$$
We can then change between the bases as:
$$\begin{align}
\vec{R}&=\dfrac{\vec{x}_i+\vec{x}_j}{2} & \vec{r}&=\vec{x}_i-\vec{x}_j
\end{align}$$
I'm not 100% sure how it was proved for me in Quantum Mechanics (COM coordinates), but we know the Jacobian of this transform is just 1, and so we can then write the partition function as:
$$\begin{align}
Z&=\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\pm \sum_{i<j}\dfrac{1}{N!}\dfrac{V^{N-2}}{\lambda^{3N}}\int e^{-2\tfrac{\pi(\vec{x}_i-\vec{x}_j)^2}{\lambda^2}}\ dx^3_idx^3_j\\
&=\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\pm \sum_{i<j}\dfrac{1}{N!}\dfrac{V^{N-2}}{\lambda^{3N}}\int e^{-2\tfrac{\pi\vec{r}^2}{\lambda^2}}\ d\vec{r}\cdot \int d\vec{R}\\
&=\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\pm \sum_{i<j}\dfrac{1}{N!}\dfrac{V^{N-1}}{\lambda^{3N}}\int e^{-\left(\tfrac{2\pi}{\lambda^2}\right)\vec{r}^2}\ d\vec{r}\\
\end{align}$$
This is just the typical Gaussian integral in 3 dimensions. This system is also now independent of the choice of $i,j$ (since Gaussian integrals are identical under translation), and so:
$$\begin{align}
Z&=\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\pm \sum_{i<j}\dfrac{1}{N!}\dfrac{V^{N-1}}{\lambda^{3N}}\int e^{-\left(\tfrac{2\pi}{\lambda^2}\right)\vec{r}^2}\ d\vec{r}\\
&=\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\pm \dfrac{N(N-1)}{2}\dfrac{1}{N!}\dfrac{V^{N-1}}{\lambda^{3N}}\cdot\left(\dfrac{\pi}{\tfrac{2\pi}{\lambda^2}}\right)^{3/2}\\
&=\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\pm \dfrac{N(N-1)}{2}\dfrac{1}{N!}\dfrac{V^{N-1}}{\lambda^{3N}}\cdot\left(\dfrac{\lambda^2}{2}\right)^{3/2}\\
\Aboxed{Z&=\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\left(1\pm \dfrac{1}{2^{3/2}}\dfrac{N(N-1)}{2}\dfrac{\lambda^3}{V}\right)}
\end{align}$$
I'm not entirely sure if this is Canonical (but I think it is, since $N$ seems to be fixed), but we can then find the relationship between the free energy and partition function as:
$$\begin{align}
F&=-kT\ln Z\\
-F/kT&=\ln\left[\dfrac{1}{N!}\dfrac{V^N}{\lambda^{3N}}\left(1\pm \dfrac{1}{2^{3/2}}\dfrac{N(N-1)}{2}\dfrac{\lambda^3}{V}\right)\right]\\
&=-\ln(N!)+N\ln V-3N\ln\lambda+\ln\left(1\pm \dfrac{1}{2^{3/2}}\dfrac{N(N-1)}{2}\dfrac{\lambda^3}{V}\right)
\end{align}$$
For a first order expansion of $\ln(1+ax)\approx ax$, we then can linearize to:
$$\begin{align}
-F/kT&=-\ln(N!)+N\ln V-3N\ln\lambda+\ln\left(1\pm \dfrac{1}{2^{3/2}}\dfrac{N(N-1)}{2}\dfrac{\lambda^3}{V}\right)\\
&=-N\ln N+N+N\ln V-3N\ln\lambda\pm \dfrac{1}{2^{3/2}}\dfrac{N(N-1)}{2}\dfrac{\lambda^3}{V}\\
&=N\left(-\ln N+1+\ln V-3\ln\lambda\pm \dfrac{1}{2^{3/2}}\dfrac{N-1}{2}\dfrac{\lambda^3}{V}\right)\\
-F/kT&\approx N\left(\ln \dfrac{V}{\lambda^3}\pm \dfrac{1}{2^{5/2}}\dfrac{N\lambda^3}{V}\right)\\
\Aboxed{F&\approx -NkT\left(\ln \dfrac{V}{\lambda^3}\pm \dfrac{1}{2^{5/2}}\dfrac{N\lambda^3}{V}\right)}
\end{align}$$
To find the equation of state (typically pressure), we want to do the following:
$$\begin{align}
P&=-\left(\dfrac{\partial F}{\partial V}\right)_{N}\\
&=NkT\dfrac{\partial}{\partial V}\left(\ln \dfrac{V}{\lambda^3}\pm \dfrac{1}{2^{5/2}}\dfrac{N\lambda^3}{V}\right)\\
&=NkT\left(\dfrac{1}{V}\mp \dfrac{1}{2^{5/2}}\dfrac{N\lambda^3}{V^2}\right)\\
\Aboxed{P(T,N/V)&=kT\left(\dfrac{N}{V}\mp \dfrac{\lambda^3}{2^{5/2}}\left(\dfrac{N}{V}\right)^2\right)}
\end{align}$$
Or, using that $N/V$ is the number density $n$, we conclude that:
$$\begin{align}
\Aboxed{P(T,n)&=kT\left(n\mp \dfrac{\lambda^3}{2^{5/2}}n^2\right)}
\end{align}$$
---
### Question 1.B
Find $E$ as a function of $T,V$, and $N$ in the same approximation.

The free energy relationship rewritten to solve for internal energy $E$, and so:
$$\begin{align}
F&\equiv E-TS & \implies && E&=F+TS
\end{align}$$
We can then substitute the relationship for entropy to arrive to:
$$\begin{align}
E&=F-T\left(\dfrac{\partial F}{\partial T}\right)_{V,N}
\end{align}$$
Using our free energy from before, we can see that the derivative term is:
$$\begin{align}
\left(\dfrac{\partial F}{\partial T}\right)_{V,N}&=-\dfrac{\partial}{\partial T}NkT\left(\ln V-3\ln\lambda\pm \dfrac{1}{2^{5/2}}\dfrac{N\lambda^3}{V}\right)\\
&=\dfrac{F}{T}-NkT\dfrac{\partial}{\partial T}\left(\ln V-3\ln\lambda\pm \dfrac{1}{2^{5/2}}\dfrac{N\lambda^3}{V}\right)\\
&=\dfrac{F}{T}-NkT\left(-3\dfrac{\partial}{\partial T}(\ln\lambda)\pm \dfrac{1}{2^{5/2}}\dfrac{N}{V}\dfrac{\partial}{\partial T}(\lambda^3)\right)\\
\end{align}$$
These derivatives of thermal wavelength are then as follows:
$$\begin{align}
\dfrac{\partial}{\partial T}(\ln\lambda)&=\dfrac{\partial}{\partial T}\ln\left(\sqrt{\dfrac{h^2}{2\pi mkT}}\right)\\
&=\dfrac{1}{2}\dfrac{\partial}{\partial T}\left(\ln\dfrac{h^2}{2\pi mk}-\ln T\right)\\
&=-\dfrac{1}{2}\dfrac{\partial}{\partial T}\left(\ln T\right)\\
\Aboxed{\dfrac{\partial}{\partial T}(\ln\lambda)&=-\dfrac{1}{2}\dfrac{1}{T}}
\end{align}$$
$$\begin{align}
\dfrac{\partial}{\partial T}(\lambda^3)&=\dfrac{\partial}{\partial T}\left(\dfrac{h^2}{2\pi mkT}\right)^{3/2}\\
&=\left(\dfrac{h^2}{2\pi mk}\right)^{3/2}\dfrac{\partial}{\partial T}T^{-3/2}\\
&=-\dfrac{3}{2}\left(\dfrac{h^2}{2\pi mk}\right)^{3/2}T^{-3/2}\dfrac{1}{T}\\
\Aboxed{\dfrac{\partial}{\partial T}(\lambda^3)&=-\dfrac{3}{2}\dfrac{1}{T}\lambda^3}
\end{align}$$
Continuing, we find that the derivative term is:
$$\begin{align}
\left(\dfrac{\partial F}{\partial T}\right)_{V,N}
&=\dfrac{F}{T}-NkT\left(-3\dfrac{\partial}{\partial T}(\ln\lambda)\pm \dfrac{1}{2^{5/2}}\dfrac{N}{V}\dfrac{\partial}{\partial T}(\lambda^3)\right)\\
&=\dfrac{F}{T}-NkT\left(\dfrac{3}{2}\dfrac{1}{T}\mp \dfrac{1}{2^{5/2}}\dfrac{N}{V}\dfrac{3}{2}\dfrac{1}{T}\lambda^3\right)\\
\Aboxed{\left(\dfrac{\partial F}{\partial T}\right)_{V,N}&=\dfrac{F}{T}-\dfrac{3}{2}Nk\left(1\mp \dfrac{1}{2^{5/2}}\dfrac{N}{V}\lambda^3\right)}
\end{align}$$
Substituting this derivative into the internal energy, we can then see that:
$$\begin{align}
E&=F-T\left(\dfrac{\partial F}{\partial T}\right)_{V,N}\\
&=F-T\left(\dfrac{F}{T}-\dfrac{3}{2}Nk\left(1\mp \dfrac{1}{2^{5/2}}\dfrac{N}{V}\lambda^3\right)\right)\\
&=F-T\dfrac{F}{T}+T\dfrac{3}{2}Nk\left(1\mp \dfrac{1}{2^{5/2}}\dfrac{N}{V}\lambda^3\right)\\
\Aboxed{E(T,V,N)&=\dfrac{3}{2}NkT\left(1\mp \dfrac{1}{2^{5/2}}\dfrac{N}{V}\lambda^3\right)}
\end{align}$$
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

From Question 2, as well as the equations above, we can write the the following relationship:
$$\begin{align}
&&N&=\left(2s+1\right)\dfrac{V}{\lambda^3}f^{\pm}_{3/2}(z)\\
\implies&& \lambda^3\dfrac{N}{V}&=\left(2s+1\right)\left(z\pm\dfrac{z^2}{2^{3/2}}+O(z^3)\right)\\
\implies&& \lambda^3\dfrac{N}{V}&\approx\left(2s+1\right)\left(z\pm\dfrac{z^2}{2^{3/2}}\right)
\end{align}$$
We can then invert then invert this relationship (with approximation) to find that:
$$\begin{align}
\dfrac{1}{\left(2s+1\right)}\lambda^3\dfrac{N}{V}&=z\pm\dfrac{z^2}{2^{3/2}}\\
z\pm\dfrac{z^2}{2^{3/2}}&=\dfrac{1}{\left(2s+1\right)}\lambda^3\dfrac{N}{V}\\
z&=\dfrac{1}{\left(2s+1\right)}\lambda^3\dfrac{N}{V}\mp\dfrac{z^2}{2^{3/2}}
\end{align}$$
Under the ideal that $z\approx\tfrac{1}{\left(2s+1\right)}\lambda^3\tfrac{N}{V}$, we see that:
$$\begin{align}
\Aboxed{z&\approx\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\mp\dfrac{1}{2^{3/2}}\left(\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\right)^2}
\end{align}$$
Similar to the approximation we had for $N$, we can approximate $E$ as:
$$\begin{align}
E&=\dfrac{3}{2}kT\left(2s+1\right)\dfrac{V}{\lambda^3}\left(z\pm\dfrac{z^2}{2^{5/2}}+O(z^3)\right)\\
E&\approx\dfrac{3}{2}kT\left(2s+1\right)\dfrac{V}{\lambda^3}\left(z\pm\dfrac{z^2}{2^{5/2}}\right)
\end{align}$$
Using our value of $z$ we got earlier, and neglecting all higher powers of $\lambda^3 N/V$, we get:
$$\begin{align}
E&\approx\dfrac{3}{2}kT\left(2s+1\right)\dfrac{V}{\lambda^3}\left(z\pm\dfrac{z^2}{2^{5/2}}\right)\\
&\approx\dfrac{3}{2}kT\left(2s+1\right)\dfrac{V}{\lambda^3}\left(\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\mp\dfrac{1}{2^{3/2}}\left(\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\right)^2\pm\dfrac{1}{2^{5/2}}\left(\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\right)^2\right)\\
&=\dfrac{3}{2}kT\left(2s+1\right)\dfrac{V}{\lambda^3}\left(\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\mp\left(\dfrac{1}{2^{3/2}}-\dfrac{1}{2^{5/2}}\right)\left(\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\right)^2\right)\\
&=\dfrac{3}{2}kT\left(2s+1\right)\dfrac{V}{\lambda^3}\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\left(1\mp\left(\dfrac{1}{2^{3/2}}-\dfrac{1}{2^{5/2}}\right)\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\right)\\
&=\dfrac{3}{2}NkT\left(1\mp\left(\dfrac{1}{2^{3/2}}-\dfrac{1}{2^{5/2}}\right)\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\right)\\
&=\dfrac{3}{2}NkT\left(1\mp\left(\dfrac{2}{2^{5/2}}-\dfrac{1}{2^{5/2}}\right)\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\right)\\
\Aboxed{E(T,V,N)&\approx\dfrac{3}{2}NkT\left(1\mp\dfrac{1}{2^{5/2}}\dfrac{\lambda^3}{\left(2s+1\right)}\dfrac{N}{V}\right)}
\end{align}$$
The solution we had from Question 1 was:
$$\begin{align}
E(T,V,N)&=\dfrac{3}{2}NkT\left(1\mp \dfrac{1}{2^{5/2}}\dfrac{N}{V}\lambda^3\right)
\end{align}$$
Our new equation is the more general form that also accounts particles with non-zero spin.

---
### Question 3.B
Using $E(T,V,N)$, obtain the specific heat of the quantum gas up to the same order in $\lambda^3\dfrac{N}{V}$.
$$\begin{align}
C_V(T)&=\dfrac{\partial}{\partial T}E(T,V,N)\\
&=\dfrac{\partial}{\partial T}\left(\dfrac{3}{2}NkT\left(1\mp \dfrac{1}{2^{5/2}}\dfrac{N}{V}\lambda^3\right)\right)\\
&=\dfrac{3}{2}Nk\dfrac{\partial}{\partial T}\left(T\right)\mp\dfrac{3}{2^{7/2}}\dfrac{N^2k}{V}\dfrac{\partial}{\partial T}\left(T\lambda^3\right)\\
&=\dfrac{3}{2}Nk\mp\dfrac{3}{2^{7/2}}\dfrac{N^2k}{V}\left(\lambda^3-T\dfrac{3}{2}\dfrac{1}{T}\lambda^3\right)\\
&=\dfrac{3}{2}Nk\mp\dfrac{3}{2^{7/2}}\dfrac{N^2k}{V}\left(1-\dfrac{3}{2}\right)\lambda^3\\
&=\dfrac{3}{2}Nk\pm\dfrac{1}{2}\dfrac{3}{2^{7/2}}\dfrac{N^2k}{V}\lambda^3\\
\Aboxed{C_V(T)&=\dfrac{3}{2}Nk\left(1\pm\dfrac{1}{2^{7/2}}\dfrac{N}{V}\lambda^3\right)}
\end{align}$$
---
## Question 4
Consider $\text{He}$ gas at room temperature and atmospheric pressure, and determine whether the classical approximation for the equation of state $(PV=NkT)$ is justified or not. Repeat the above considerations for the electron "gas" at room temperature.

We want to determine if the thermal wavelength is "small enough" for our system.
### Helium Gas
We can calculate the thermal wavelength $\lambda$ at $T\approx 300 K$ (I don't know where I learned this number from, but I've heard it so often it's as close to a definition for room temperature I have):
$$\begin{align}
\lambda&=\sqrt{\dfrac{h^2}{2\pi mkT}}\\
&\approx\dfrac{6.626\cdot10^{-34}\text{ J}\cdot\text{s}}{\sqrt{2\pi\left(4.003\cdot10^{-3}\dfrac{\text{kg}}{\text{mol}}\cdot\dfrac{1}{6.022}\cdot10^{-23}\text{mol}\right)\left(1.38\cdot10^{-23}\dfrac{\text{J}}{\text{K}}\right)\left(300\text{ K}\right)}}\\
&\approx\dfrac{6.626\cdot10^{-34}\text{ J}\cdot\text{s}}{\sqrt{2\pi\left(6.647\cdot10^{-27}\text{kg}\right)\left(1.38\cdot10^{-23}\dfrac{\text{J}}{\text{K}}\right)\left(300\text{ K}\right)}}\\
&\approx\dfrac{6.626\cdot10^{-34}\text{ J}\cdot\text{s}}{\sqrt{1.729\cdot10^{-46}\text{ J}\cdot\text{kg}}}\\
&\approx5.039\cdot10^{-11}\sqrt{\dfrac{\text{J}^2\cdot\text{s}^2}{\text{J}\cdot\text{kg}}}\\
&\approx5.039\cdot10^{-11}\sqrt{\dfrac{\text{kg}\cdot\text{m}^2\cdot\text{s}^2}{\text{kg}\cdot\text{s}^2}}\\
\Aboxed{\lambda&\approx5.039\cdot10^{-11}\text{ m}}
\end{align}$$
The thermal wavelength is about half an angstromm.

If we assume the case of the ideal gas, then:
$$\begin{align}
PV&=NkT & \implies && \dfrac{N}{V}=\dfrac{P}{kT}
\end{align}$$
Using $1\text{ atm}$ as our pressure and $T\approx 300 K$, we see the ratio comes out to be:
$$\begin{align}
\dfrac{N}{V}&=\dfrac{P}{kT}\\
&=\dfrac{101325\text{ Pa}}{\left(1.38\cdot10^{-23}\dfrac{\text{J}}{\text{K}}\right)\left(300\text{ K}\right)}\\
&=\dfrac{101325\text{ Pa}}{\left(1.38\cdot10^{-23}\dfrac{\text{J}}{\text{K}}\right)\left(300\text{ K}\right)}\\
&=2.447\cdot10^{25}\dfrac{\text{J}/\text{m}^3}{\text{J}}\\
\Aboxed{\dfrac{N}{V}&=2.447\cdot10^{25}\dfrac{1}{\text{m}^3}}
\end{align}$$
The classical condition is allowed when $\dfrac{N}{V}\lambda^3\ll1$, and we can calculate that as:
$$\begin{align}
\dfrac{N}{V}\lambda^3&=\left(2.447\cdot10^{25}\dfrac{1}{\text{m}^3}\right)\left(5.039\cdot10^{-11}\text{ m}\right)^3\\
\Aboxed{\dfrac{N}{V}\lambda^3&=3.13\cdot10^{-6}}
\end{align}$$
This is considerably smaller than $1$, so we can conclude the Ideal Gas is fine in this approximation.

### Electron Gas
We can calculate the thermal wavelength $\lambda$ at $T\approx 300 K$.
$$\begin{align}
\lambda&=\sqrt{\dfrac{h^2}{2\pi mkT}}\\
&=\sqrt{\dfrac{h^2c^2}{2\pi (mc^2)kT}}\\
&=\dfrac{hc}{\sqrt{2\pi (mc^2)kT}}\\
&=\dfrac{1240\text{ eV}\text{ nm}}{\sqrt{2\pi (0.5\cdot10^{6}\text{ eV})(8.617\cdot10^{-5}\text{ eV}/\text{K})(300\text{ K})}}\\
&=\dfrac{1240\text{ eV}\text{ nm}}{\sqrt{8.121\cdot10^{4}\text{ eV}^2}}\\
\Aboxed{\lambda&=4.35\text{ nm}}
\end{align}$$
The ideal gas condition is the same as the above, and so:
$$\begin{align}
\Aboxed{\dfrac{N}{V}&=2.447\cdot10^{25}\dfrac{1}{\text{m}^3}}
\end{align}$$
The classical condition is allowed when $\dfrac{N}{V}\lambda^3\ll1$, and we can calculate that as:
$$\begin{align}
\dfrac{N}{V}\lambda^3&=\left(2.447\cdot10^{25}\dfrac{1}{\text{m}^3}\right)\left(4.35\cdot10^{-9}\text{ m}\right)^3\\
\Aboxed{\dfrac{N}{V}\lambda^3&=2.01}
\end{align}$$
This would be a bad time to use the Ideal Gas since this number is definitely larger than 1.
