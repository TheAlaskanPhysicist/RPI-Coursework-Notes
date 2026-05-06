**Author:** Stanley Goodwin
**Date:** March 26th, 2026

---
### Question 1
> Using the residue theorem, calculate the following integral:
> $$\begin{align}
\int_{-\infty}^{+\infty}\dfrac{dk}{2\pi}e^{ikx}\dfrac{1}{k^2+m^2}
\end{align}$$
> where $m>0$. Make sure you discuss the $x>0$ and $x<0$ cases separately.

Since there are poles at $k=\pm im$, we can complete the contour looping in the upper half plane:
$$\begin{align}
\oint_\Gamma f(z)\ dz&=\lim_{R\to\infty}\int_{-R}^{+R}f(x)\ dx+\lim_{R\to\infty}\int_0^\pi f\left(Re^{i\phi}\right)\cdot iRe^{i\phi}d\phi
\end{align}$$
To see the evaluation for this added extra contour, look at the limit of the magnitude:
$$\begin{align}
\lim_{R\to\infty}\int_0^\pi\dfrac{\left|e^{iRe^{i\phi}x}\right|}{\left|(Re^{i\phi})^2+m^2\right|}|i|\left|Re^{i\phi}\right|d\phi&\le\lim_{R\to\infty}\int_0^\pi\dfrac{Re^{-R\sin\phi x}}{R^2+m^2}d\phi
\end{align}$$
This upper-half plane only converges to $0$ if $x>0$. Similarly, a contour in the lower-half plane only converges for $x<0$. The full contour is equal to $2\pi i$ times the sum of the residues.
$$\begin{align}
\operatorname{Res}(f,\pm mi)&=\pm\dfrac{1}{2\pi}\lim_{k\to\pm im}(k\mp im)\dfrac{e^{ikx}}{k^2+m^2}\\
&=\pm\dfrac{1}{2\pi}\lim_{k\to\pm im}\dfrac{e^{ikx}}{(k\pm im)}\\
\operatorname{Res}(f,\pm mi)&=\dfrac{1}{2\pi i}\cdot\dfrac{e^{\mp mx}}{2m}
\end{align}$$
So, for the two conditions for $x$, we have:
$$\begin{align}
\int_{-\infty}^{+\infty}\dfrac{dk}{2\pi}e^{ikx}\dfrac{1}{k^2+m^2}&=\dfrac{e^{-mx}}{2m} & x>0\\
\int_{-\infty}^{+\infty}\dfrac{dk}{2\pi}e^{ikx}\dfrac{1}{k^2+m^2}&=\dfrac{e^{+mx}}{2m} & x<0
\end{align}$$
Or, more compactly, we can write the final integral as:
$$\begin{align}
\Aboxed{\int_{-\infty}^{+\infty}\dfrac{dk}{2\pi}e^{ikx}\dfrac{1}{k^2+m^2}&=\dfrac{e^{-m|x|}}{2m}} & x\ne0
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 2
> Calculate the following Cauchy Principle Value integral:
> $$\begin{align}
\mathcal{P}\int_{-1}^{+2}\dfrac{1}{x}dx
\end{align}$$

We can split the integral into two limits:
$$\begin{align}
\mathcal{P}\int_{-1}^{+2}\dfrac{1}{x}dx
&=\lim_{\delta\to0^-}\int_{-1}^{\delta}\dfrac{dx}{x}+\lim_{\delta\to0^+}\int_{\delta}^{+2}\dfrac{dx}{x}\\
&=\lim_{\delta\to0^-}\left.\ln\left|x\right|\right|_{-1}^{\delta}+\lim_{\delta\to0^+}\left.\ln\left|x\right|\right|_{\delta}^{2}\\
&=\lim_{\delta\to0}\left[\ln\left|-\delta\right|-\ln\left|-1\right|+\ln\left|2\right|-\ln\left|+\delta\right|\right]\\
&=\ln\left|2\right|-\ln\left|-1\right|+\lim_{\delta\to0}\left[\ln\delta-\ln\delta\right]\\
\Aboxed{\mathcal{P}\int_{-1}^{+2}\dfrac{1}{x}dx&=\ln2}
\end{align}$$
---
### Question 3
> Show that when $f(z)$ is analytic in the domain $\mathrm{Im}(z)\ge0$, and that $\lim_{|z|\to\infty}|f(z)|=0$, then:
> $$\begin{align}
\mathcal{P}\int_{-\infty}^{+\infty}\dfrac{f(x)}{x-x_0}dx&=i\pi f(x_0)
\end{align}$$

Well the first thing we can do is rewrite this integral by shifting the $x$ axis:
$$\begin{align}
\mathcal{P}\int_{-\infty}^{+\infty}\dfrac{f(x)}{x-x_0}dx&=\mathcal{P}\int_{-\infty}^{+\infty}\dfrac{f(x+x_0)}{x}dx
\end{align}$$
We can create a complete contour with the following integrals:
$$\begin{align}
I_1&=\lim_{R\to-\infty}\lim_{\delta\to0^-}\int_R^\delta\dfrac{f(x+x_0)}{x}dx &
I_2&=\lim_{\delta\to0^+}\int_{\pi}^{2\pi}\dfrac{f(\delta e^{i\phi}+x_0)}{\delta e^{i\phi}}\cdot i\delta e^{i\phi}d\phi\\
I_3&=\lim_{R\to+\infty}\lim_{\delta\to0^+}\int_{\delta}^R\dfrac{f(x+x_0)}{x}dx &
I_4&=\lim_{R\to\infty}\int_{0}^{\pi}\dfrac{f(Re^{i\phi}+x_0)}{Re^{i\phi}}\cdot iRe^{i\phi}d\phi
\end{align}$$
The addition of $I_1$ and $I_3$ is just the original principle integral, while $I_2$ and $I_4$ are semicircle contours that connect the two disjoint real integrations. Integral $2$ is:
$$\begin{align}
I_2&=\lim_{\delta\to0^+}i\int_{\pi}^{2\pi}f(\delta e^{i\phi}+x_0)\ d\phi=i\int_{\pi}^{2\pi}f(x_0)\ d\phi\\
\Aboxed{I_2&=i\pi f(x_0)}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


Integral $4$ is similar, but needs constraints:
$$\begin{align}
I_4&=i\lim_{R\to\infty}\int_{0}^{\pi}f(Re^{i\phi}+x_0)\ d\phi\\
|I_4|&\le |i|\int_{0}^{\pi}\lim_{R\to\infty}\left|f(Re^{i\phi}+x_0)\right|\ d\phi\\
&=\int_{0}^{\pi}\lim_{|z|\to\infty}\left|f(z)\right|\ d\phi\\
|I_4|&\le0
\end{align}$$
Since the absolute value of the integral is less than or equal to zero, and that the absolute value evaluates to elements zero or strictly positive, we know that $\boxed{I_4=0}$. We then have that the total contour integral is equal to:
$$\begin{align}
I=\mathcal{P}\int_{-\infty}^{+\infty}\dfrac{f(x)}{x-x_0}dx+i\pi f(x_0)=2\pi i\operatorname{Res}\left(f,z=x_0\right)
\end{align}$$
The residue is trivial to calculate:
$$\begin{align}
&&2\pi i\lim_{z\to x_0}(z-x_0)\dfrac{f(z)}{z-x_0}=2\pi if(x_0) \\
\implies&&\mathcal{P}\int_{-\infty}^{+\infty}\dfrac{f(x)}{x-x_0}dx+i\pi f(x_0)=2\pi if(x_0)
\end{align}$$
Rearranging for the principle value integral, we get the final solution:
$$\begin{align}
\Aboxed{\mathcal{P}\int_{-\infty}^{+\infty}\dfrac{f(x)}{x-x_0}dx&=i\pi f(x_0)}
\end{align}$$
