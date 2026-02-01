Show the following:
$$\begin{align}
\int_0^1P_{2k+1}(x)\ dx&=+\dfrac{(-1)^k(2k)!}{2^{2k}k!(k+1)!} & k\ge0\\
\int_{-1}^0P_{2k+1}(x)\ dx&=-\dfrac{(-1)^k(2k)!}{2^{2k}k!(k+1)!} & k\ge0\\
\int_0^1P_{2k}(x)\ dx&=0 & k\ge1\\
\int_{-1}^0P_{2k}(x)\ dx&=0 & k\ge1\\
\int_0^1P_{0}(x)\ dx&=1\\
\int_{-1}^0P_{0}(x)\ dx&=1\\
\end{align}$$






$$\begin{align}
c_l^{r=b}&=-c_l^{r=a} & 
c_{l=2k+1}^{r=a}&=V\dfrac{4k+3}{2}\dfrac{(-1)^k(2k)!}{2^{2k}k!(k+1)!}
\end{align}$$


$$\begin{align}
A_0&=\dfrac{V}{2} & B_0&=0\\
A_{2k}&=0 & B_{2k}&=0
\end{align}$$
$$\begin{align}
A_{2k+1}&=\dfrac{a^{2k+2}+b^{2k+2}}{a^{4k+3}-b^{4k+3}}V\dfrac{4k+3}{2}\dfrac{(-1)^k(2k)!}{2^{2k}k!(k+1)!}\\
B_{2k+1}&=-\dfrac{a^{2k+2}b^{4k+3}+a^{4k+3}b^{2k+2}}{a^{4k+3}-b^{4k+3}}V\dfrac{4k+3}{2}\dfrac{(-1)^k(2k)!}{2^{2k}k!(k+1)!}
\end{align}$$

$$\begin{align}
\Phi(r,\theta)&=\sum_{l=0}^\infty\left(A_lr^l+B_lr^{-l-1}\right)P_l(\cos\theta)\\
&=A_0r^0P_0+\sum_{k=1}^\infty\left(A_{2k}r^{2k}+B_{2k}r^{-{2k}-1}\right)P_{2k}(\cos\theta)+\sum_{k=0}^\infty\left(A_{2k+1}r^{2k+1}+B_lr^{-2k-2}\right)P_{2k+1}(\cos\theta)\\
&=\dfrac{V}{2}+\dfrac{V}{2}\sum_{k=0}^\infty\dfrac{(-1)^k(4k+3)(2k)!}{2^{2k}k!(k+1)!}\dfrac{1}{a^{4k+3}-b^{4k+3}}\left((a^{2k+2}+b^{2k+2})r^{2k+1}-(a^{2k+2}b^{4k+3}+a^{4k+3}b^{2k+2})r^{-2k-2}\right)P_{2k+1}(\cos\theta)\\
&=\dfrac{V}{2}+\dfrac{V}{2}\sum_{k=0}^\infty\dfrac{(-1)^k(4k+3)(2k)!}{2^{2k}k!(k+1)!}\dfrac{1}{a^{4k+3}-b^{4k+3}}\left(a^{2k+2}[r^{2k+1}-b^{4k+3}r^{-2k-2}]+b^{2k+2}[r^{2k+1}+a^{4k+3}r^{-2k-2}]\right)P_{2k+1}(\cos\theta)\\
\end{align}$$
