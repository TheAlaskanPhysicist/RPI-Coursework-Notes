



Suppose we have a function of the form
$$\begin{align}
f_{n,m}(x)&=\frac{P_n(x)}{Q_m(x)}
&& P_n(x)\in\mathbb{R}_n[x]
&& Q_m(x)\in\mathbb{R}_m[x]
\end{align}$$
We want to approximate this function space with a basis. Suppose that $n>m$, then we can use polynomial long division to turn our function into
$$\begin{align}
f_{n,m}(x)&=S(x)_{n-m}+\frac{R_{m-1}(x)}{Q_m(x)}
\end{align}$$
We can find the solution to the remaining system if we are careful to use limits for poles. The numerator can be factored uniquely due to the Fundamental Theorem of Algebra, and then using partial fraction decomposition without repeated roots, we find that
$$\begin{align}
f_{n,m}(x)&=\sum_{i=0}^{m-n} a_ix^i+\sum_{j=1}^m\dfrac{b_j}{x+c_j}
\end{align}$$
For systems that have repeated roots, we add an offset $\epsilon e^{i\phi}$ about $c_j$ to be equally spaced around the center, where later we take the limit $\epsilon\to0$.








Suppose we have a function of the form
$$\begin{align}
f(x)&=\frac{P(x)}{Q(x)} & P(x),Q(x)\in\mathbb{R}[x]
\end{align}$$
We want to approximate this function space with a basis. I will start with defining finite degree polynomials for $P(x)$ and $Q(x)$ to look for a pattern.


| $n,m$ | General Function                               | Reduced Function                                  | New Basis Elements | Basis Elements |
| ----- | ---------------------------------------------- | ------------------------------------------------- | ------------------ | -------------- |
| $0,0$ | $f(x)=\frac{c_0}{d_0}$                         | $f(x)=a_{0,0}$                                    | $1$                | 1              |
| $1,0$ | $f(x)=\frac{c_0+c_1x}{d_0}$                    | $f(x)=a_{0,0}+a_{1,0}x$                           | $x$                | 2              |
| $0,1$ | $f(x)=\frac{c_0}{d_0+d_1x}$                    | $f(x)=a_{0,1}\frac{1}{1+r_1x}$                    | $\frac{1}{1+r_1x}$ | 2              |
| $1,1$ | $f(x)=\frac{c_0+c_1x}{d_0+d_1x}$               | $f(x)=a_{0,0}+a_{1,1}\frac{1}{r_1-x}$             | None!              | 3              |
| $2,0$ | $f(x)=\frac{c_0+c_1x+c_2x^2}{d_0}$             | $f(x)=a_{0,0}+a_{1,0}x+a_{2,0}x^2$                |                    |                |
| $2,1$ | $f(x)=\frac{c_0+c_1x+c_2x^2}{d_0+d_1x}$        | $f(x)=a_{0,0}+a_{1,0}x+a_{2,1}\frac{x^2}{1+r_1x}$ |                    |                |
| $2,2$ | $f(x)=\frac{c_0+c_1x+c_2x^2}{d_0+d_1x+d_2x^2}$ |                                                   |                    |                |
| $1,2$ | $f(x)=\frac{c_0+c_1x}{d_0+d_1x+d_2x^2}$        |                                                   |                    |                |
| $0,2$ | $f(x)=\frac{c_0}{d_0+d_1x+d_2x^2}$             |                                                   |                    |                |




From Partial Fraction Decomposition










Normal Polynomials:
$$\begin{align}
f(x)&=a_0+a_1(x-c_1)+a_2(x-c_2)^2+\dots
\end{align}$$
These get reduced to individual powers with coefficients, but what about reciprocal powers?

All rational functions can be generated with
$$\begin{align}
P(x)&=a_0+a_1(x-c_1)+a_2(x-c_2)^2+\dots\\
Q(x)&=b_0+b_1(x-d_1)+b_2(x-d_2)^2+\dots
\end{align}$$
The issue we run into is that the coefficients at the bottom don't split as nicely. Suppose we have 2nd order in both polynomials, then:
$$\begin{align}
f(x)&=\frac{a_0+a_1(x-c_1)+a_2(x-c_2)^2}{b_0+b_1(x-d_1)+b_2(x-d_2)^2}
\end{align}$$

