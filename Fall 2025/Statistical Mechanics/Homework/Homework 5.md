Author: Stanley Goodwin
Date: December 1st, 2025

---
## Question 1
Starting from the van der Waals equation:
$$\begin{align}
\left(P+a\dfrac{N^2}{V^2}\right)\left(V-bN\right)&=NkT & \implies&& P&=\dfrac{NkT}{V-bN}-a\dfrac{N^2}{V^2}
\end{align}$$
### Question 1.A
Show that the critical values of the volume, temperature, and pressure are given by:
$$\begin{align}
V_c&=3Nb & kT_c&=\dfrac{8}{27}\dfrac{a}{b} & P_c&=\dfrac{1}{27}\dfrac{a}{b^2}
\end{align}$$
The critical point is when the first and second derivative of pressure with respect to volume is 0:
$$\begin{align}
\left(\dfrac{\partial P}{\partial V}\right)_T&=\dfrac{\partial}{\partial V}\left(\dfrac{NkT}{V-bN}-a\dfrac{N^2}{V^2}\right)_T\\
0&=-\dfrac{NkT}{(V-bN)^2}+2a\dfrac{N^2}{V^{3}}\\
2a\dfrac{N^2}{V^{3}}&=\dfrac{NkT}{(V-bN)^2}\\
2a(V-bN)^2N^2&=NkTV^{3}\\
\Aboxed{2Na(V-bN)^2&=kTV^{3}}
\end{align}$$
$$\begin{align}
\left(\dfrac{\partial^2 P}{\partial V^2}\right)_T&=\dfrac{\partial^2}{\partial V^2}\left(\dfrac{NkT}{V-bN}-a\dfrac{N^2}{V^2}\right)_T\\
&=\dfrac{\partial}{\partial V}\left(-\dfrac{NkT}{(V-bN)^2}+2a\dfrac{N^2}{V^{3}}\right)_T\\
0&=2\dfrac{NkT}{(V-bN)^3}-6a\dfrac{N^2}{V^{4}}\\
6a\dfrac{N^2}{V^{4}}&=2\dfrac{NkT}{(V-bN)^3}\\
\Aboxed{3aN^2(V-bN)^3&=NkTV^{4}}
\end{align}$$
We then have a system of equations at these special critical values:
$$\begin{align}
2Na(V-bN)^2&=kTV^{3}\\
3aN^2(V-bN)^3&=NkTV^{4}
\end{align}$$
Dividing the second by the first, we see:
$$\begin{align}
\dfrac{3}{2}N(V-bN)&=NV & \implies && \Aboxed{V_c&=3bN}
\end{align}$$
Using this relation, we can substitute it back into either equation to find:
$$\begin{align}
2Na(V-bN)^2&=kTV^{3}\\
2Na(3bN-bN)^2&=kT(3bN)^{3}\\
2N^3ab^2(3-1)^2&=27kTN^3b^3\\
8a=27kTb\\
\Aboxed{T_c&=\dfrac{8a}{27kb}}
\end{align}$$
Using both of these back in the Equation of State, we find the pressure:
$$\begin{align}
P&=\dfrac{NkT}{V-bN}-a\dfrac{N^2}{V^2}\\
&=\dfrac{Nk}{3bN-bN}\dfrac{8a}{27kb}-a\dfrac{N^2}{(3bN)^2}\\
&=\dfrac{4a}{27b^2}-\dfrac{3a}{27b^2}\\
\Aboxed{P_c&=\dfrac{a}{27b^2}}
\end{align}$$
---
### Question 1.B
Show that in the vicinity of the critical point, the van der Waals equation can be written as:
$$\begin{align}
\pi\approx4t-6t\phi-\dfrac{3}{2}\phi^3
\end{align}$$
where $t=\dfrac{T-T_c}{T_c}$, $\pi=\dfrac{P-P_c}{P_c}$, and $\phi=\dfrac{V-V_c}{V_c}$.

For the purposes of substitution, we can rearrange these parameters as:
$$\begin{align}
T&=(t+1)T_c & P&=(\pi+1)P_c & V&=(\phi+1)V_c
\end{align}$$
Or in terms of the critical values:
$$\begin{align}
kT&=\dfrac{8}{27}\dfrac{a}{b}(t+1) & P&=\dfrac{1}{27}\dfrac{a}{b^2}(\pi+1) & V&=3Nb(\phi+1)
\end{align}$$
Substituting into the van der Waals equation of state, we get:
$$\begin{align}
PV^2+aN^2&=\dfrac{NkTV^2}{\left(V-bN\right)}\\
\dfrac{1}{27}\dfrac{a}{b^2}(\pi+1)[3Nb(\phi+1)]^2+aN^2&=\dfrac{N[3Nb(\phi+1)]^2}{3Nb(\phi+1)-bN}\cdot\dfrac{8}{27}\dfrac{a}{b}(t+1)\\
\left[(\pi+1)(\phi+1)^2+3\right]\dfrac{aN^2}{3}&=8(t+1)\dfrac{aN^2}{3}\dfrac{(\phi+1)^2}{3\phi+2}\\
(\pi+1)(\phi+1)^2&=8(t+1)\dfrac{(\phi+1)^2}{3\phi+2}-3\\
\Aboxed{\pi&=8(t+1)\dfrac{1}{3\phi+2}-3\dfrac{1}{(\phi+1)^2}-1}
\end{align}$$
Since $\phi$ becomes vanishingly small in this limit, we can approximate these powers:
$$\begin{align}
\pi(t,\phi)&=8(t+1)\dfrac{1}{3\phi+2}-3\dfrac{1}{(\phi+1)^2}-1\\
&=8(t+1)\dfrac{1}{2}\dfrac{1}{1+\tfrac{3}{2}\phi}-3\dfrac{1}{(1+\phi)^2}-1\\
&=-1+8(t+1)\dfrac{1}{2}\sum_{n=0}^\infty(-\tfrac{3}{2})^n\phi^n-3\sum_{n=0}^\infty (n+1)(-1)^n\phi^{n}\\
&=-1+\sum_{n=0}^\infty\left[4(\tfrac{3}{2})^nt+4(\tfrac{3}{2})^n-3(n+1)\right](-1)^n\phi^{n}\\
&\approx4t+\left[4-3-1\right]-\left[4(\tfrac{3}{2})t+4(\tfrac{3}{2})-6\right]\phi\\
&+\left[4(\tfrac{3}{2})^2t+4(\tfrac{3}{2})^2-9\right]\phi^{2}-\left[4(\tfrac{3}{2})^3t+4(\tfrac{3}{2})^3-12\right]\phi^3\\\\
&=4t-6t\phi+9t\phi^{2}-\left[\tfrac{27}{2}t+\tfrac{3}{2}\right]\phi^3\\
\Aboxed{\pi(t,\phi)&\approx4t-6t\phi+9t\phi^{2}-\tfrac{27}{2}t\phi^3-\tfrac{3}{2}\phi^3}
\end{align}$$
There probably is some particular justification as to why the $t\phi^2$ and $t\phi^3$ are neglected even when we have the $t\phi$ and $\phi^3$ term, but for the sake of this small region around the critical point, this is well approximated by a smaller subset of these terms, namely:
$$\begin{align}
\Aboxed{\pi(t,\phi)&\approx4t-6t\phi-\tfrac{3}{2}\phi^3}
\end{align}$$
There likely is a set of specific approximations that gives exactly the above without those extra terms, but I couldn't be bothered to do many permutations to find the *exact* version.

---


