


Suppose we have the integral
$$\begin{align}
I(n,m)&=\int\sin^n(kx)\cos^m\left(kx\right)dx
\end{align}$$
As a complex integral, we have
$$\begin{align}
I(n,m)&=\int\left(\frac{e^{ikx}-e^{-ikx}}{2i}\right)^n\left(\frac{e^{ikx}+e^{-ikx}}{2}\right)^mdx\\
&=\dfrac{1}{(2i)^n2^m}\sum_{a=0}^n\sum_{b=0}^m\binom{n}{a}\binom{m}{b}\int(-1)^{n-a}(e^{ikx})^{a}\left(e^{-ikx}\right)^{n-a}(e^{ikx})^{b}\left(e^{-ikx}\right)^{m-b}dx\\
&=\dfrac{1}{(2i)^n2^m}\sum_{a=0}^n\sum_{b=0}^m(-1)^{n-a}\binom{n}{a}\binom{m}{b}\int e^{ik(2a+2b-n-m)x}dx\\
&=\dfrac{i^n}{2^{n+m}}\sum_{a=0}^n\sum_{b=0}^m(-1)^{a}\binom{n}{a}\binom{m}{b} \int e^{ik(2a+2b-n-m)x}\ dx
\end{align}$$













For $n\in\text{Even}$ and $m\in\text{Odd}$, we have that
$$\begin{align}
I(2a,2b+1)&=\int\sin^{2a}(kx)\cos^{2b+1}\left(kx\right)dx\\
&=\dfrac{1}{k}\int\sin^{2a}(kx)\left(1-\sin^2\left(kx\right)\right)^bk\cos\left(kx\right)dx\\
&=\dfrac{1}{k}\int u^{2a}\left(1-u^2\right)^bdu\\
I(2a,2b+1)&=\dfrac{1}{k}\sum_{n=0}^{b}\frac{\left(-1\right)^{b+1-n}}{2a+1+2n}\binom{b}{n}\sin^{2a+1+2i}\left(kx\right)
\end{align}$$
Thus we have that
$$\begin{align}
\int\sin^{2a}(kx)\cos^{2b+1}\left(kx\right)dx&=\dfrac{1}{k}\sum_{n=0}^{b}\frac{\left(-1\right)^{b+1-n}}{2a+1+2n}\binom{b}{n}\sin^{2a+1+2n}\left(kx\right)
\end{align}$$




For $n\in\text{Even}$ and $m\in\text{Odd}$, we have that
$$\begin{align}
I(n,m)&=\int\sin^n(kx)\left(1-\sin^2\left(kx\right)\right)^\tfrac{m-1}{2}\cos\left(kx\right)dx\\
&=\dfrac{1}{k}\int u^n\left(1-u^2\right)^\tfrac{m-1}{2}du\\
&=\dfrac{1}{k}\sum_{i=0}^\tfrac{m-1}{2}\binom{\tfrac{m-1}{2}}{i}\frac{\left(-1\right)^{\tfrac{m-1}{2}-i+1}}{n+2i+1}\sin^{n+2i+1}\left(kx\right)\\
\end{align}$$


u=sin(kx)
du=k cos(kx) dx