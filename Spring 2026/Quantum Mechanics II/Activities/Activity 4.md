Stanley Goodwin, 2/10/2026

---
Consider an infinite square potential in the $(-a,a)$ interval $(a>0)$. Consider the trial function:
$$\begin{align}
\braket{x\lvert\psi}&=A\left(a^\lambda-|x|^\lambda\right)
\end{align}$$
### Part A
Find $\lambda_\text{min}$ for which $\bar{H}(\lambda)$ is minimum.

We can find the normalization of this state:
$$\begin{align}
1&=\int_{-a}^{+a}A^2\left(a^\lambda-|x|^\lambda\right)^2\ dx\\
&=2A^2\int_{0}^{a}\left(a^{2\lambda}-2a^\lambda|x|^\lambda+|x|^{2\lambda}\right)\ dx\\
&=2A^2\left[a^{2\lambda}x-2a^\lambda\dfrac{|x|^{\lambda+1}}{\lambda+1}+\dfrac{|x|^{2\lambda+1}}{2\lambda+1}\right|_{0}^{a}\\
1&=2A^2a^{2\lambda+1}\left[1-\dfrac{2}{\lambda+1}+\dfrac{1}{2\lambda+1}\right]\\
\end{align}$$
The energy is calculated similarly:
$$\begin{align}
\left\langle H\right\rangle
&=\int_{-a}^{+a}A\left(a^\lambda-|x|^\lambda\right)\cdot-\dfrac{\hbar^2}{2m}\dfrac{d^2}{dx^2}\cdot A\left(a^\lambda-|x|^\lambda\right)\ dx\\
&=\dfrac{\hbar^2}{2m}2A^2\int_{0}^{a}\left(a^\lambda-|x|^\lambda\right)\cdot\left(\lambda(\lambda-1)\right)|x|^{\lambda-2}\ dx\\
&=\dfrac{\hbar^2}{2m}2A^2\lambda(\lambda-1)\left[a^\lambda\dfrac{|x|^{\lambda-1}}{\lambda-1}-\dfrac{|x|^{2\lambda-1}}{2\lambda-1}\right|_{0}^{a}\\
&=\dfrac{\hbar^2}{2m}2A^2a^{2\lambda-1}\lambda(\lambda-1)\left[\dfrac{1}{\lambda-1}-\dfrac{1}{2\lambda-1}\right]\\
&=\dfrac{\hbar^2}{2ma^2}\lambda(\lambda-1)\dfrac{\left[\dfrac{1}{\lambda-1}-\dfrac{1}{2\lambda-1}\right]}{\left[1-\dfrac{2}{\lambda+1}+\dfrac{1}{2\lambda+1}\right]}\\
\end{align}$$
We need to simply this rational expression. Start with all the lambda terms:
$$\begin{align}
R&=\lambda(\lambda-1)\dfrac{\left[\dfrac{1}{\lambda-1}-\dfrac{1}{2\lambda-1}\right]}{\left[1-\dfrac{2}{\lambda+1}+\dfrac{1}{2\lambda+1}\right]}\\
&=\lambda(\lambda-1)\dfrac{(\lambda+1)(2\lambda+1)}{(\lambda-1)(2\lambda-1)}\dfrac{\lambda}{2\lambda^2}\\
R&=\dfrac{1}{2}\dfrac{(\lambda+1)(2\lambda+1)}{(2\lambda-1)}
\end{align}$$
We can take the derivative of $R$ w.r.t. $\lambda$:
$$\begin{align}
\dfrac{dR}{d\lambda}
&=\dfrac{d}{d\lambda}\left(\dfrac{1}{2}(\lambda+1)(2\lambda+1)(2\lambda-1)^{-1}\right)\\
0&=(2\lambda+1)(2\lambda-1)^{-1}+2(\lambda+1)(2\lambda-1)^{-1}-2(\lambda+1)(2\lambda+1)(2\lambda-1)^{-2}\\
&=(2\lambda+1)(2\lambda-1)+2(\lambda+1)(2\lambda-1)-2(\lambda+1)(2\lambda+1)\\
&=4\lambda^2-1+4\lambda^2+2\lambda-2-4\lambda^2-6\lambda-2\\
0&=4\lambda^2-4\lambda-5
\end{align}$$
The solutions where these extrema occur are the following:
$$\begin{align}
\lambda&=\dfrac{1\pm\sqrt{6}}{2} &\implies&& \Aboxed{\lambda_\text{min}&=\dfrac{1+\sqrt{6}}{2}, \ R''(\lambda_\text{min})>0}
\end{align}$$
---
### Part B
Find the energy $\bar{H}_\text{min}=\bar{H}(\lambda_\text{min})$ as the approximate energy of the ground state.

Our Hamiltonian Parametrized by $\lambda$ is the following:
$$\begin{align}
\left\langle H\right\rangle_\lambda
&=\dfrac{\hbar^2}{4ma^2}\dfrac{(\lambda+1)(2\lambda+1)}{(2\lambda-1)}
\end{align}$$
At our assignment of our extremal value of $\lambda$, we have:
$$\begin{align}
\bar{H}_\text{min}
&=\dfrac{\hbar^2}{8ma^2}\dfrac{(1+\sqrt{6}+2)(1+\sqrt{6}+1)}{(1+\sqrt{6}-1)}\\
&=\dfrac{\hbar^2}{8ma^2}\dfrac{(3+\sqrt{6})(2+\sqrt{6})}{\sqrt{6}}\\
&=\dfrac{\hbar^2}{8ma^2}\left(\dfrac{5\sqrt{6}}{\sqrt{6}}+\dfrac{12}{\sqrt{6}}\right)\\
\Aboxed{\bar{H}_\text{min}&=\dfrac{\hbar^2}{2ma^2}\cdot\dfrac{5+2\sqrt{6}}{4}}
\end{align}$$
It is true that our numerator is actually a good approximation for $\pi^2$:
$$\begin{align}
5+2\sqrt{6}&\approx9.89897948557 & \pi^2\approx 9.86960440109\\
\sqrt{5+2\sqrt{6}}&\approx3.14626436994 & \pi\approx 3.14159265359\\
\end{align}$$

