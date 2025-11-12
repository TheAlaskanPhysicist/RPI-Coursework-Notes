#### Known Zeros
If you can write your expression as the following, then it reduces to 0.
$$\begin{align}
k&\in\text{Odd} & n&\in\text{Odd} &  p&\in\text{Odd} & \implies && P=0\\
k&\in\text{Even} & n&\in\text{Even} &  p&\in\text{Odd} & \implies && P=0\\
k&\in\text{Even} & n&\in\text{Odd} &  p&\in\text{Even} & \implies && P=0\\
k&\in\text{Odd} & n&\in\text{Even} &  p&\in\text{Even} & \implies && P=0\\
\end{align}$$
$$\begin{align}
\bra{2k+1}(a^\dagger-a)^{2p+1}\ket{2n+1}&=0\\
\bra{2k+0}(a^\dagger-a)^{2p+1}\ket{2n+0}&=0\\
\bra{2k+0}(a^\dagger-a)^{2p+0}\ket{2n+1}&=0\\
\bra{2k+1}(a^\dagger-a)^{2p+0}\ket{2n+0}&=0\\
\end{align}$$
---
### General Solutions
For same-state correlation:
$$\begin{align}
\bra{k}(a^\dagger-a)^{n}\ket{k}&=\begin{cases}(-1)^{n/2}\dfrac{n!}{(n/2)!}\sum_{j=0}^{\min(k,n/2)}\dfrac{1}{2^{(n/2)-j}}\dfrac{k!}{j!(k-j)!}\dfrac{(n/2)!}{j!(n/2-j)!}, &n\in2\mathbb{Z}_0^+\\
0, &n\text{ otherwise}\\
\end{cases}
\end{align}$$
For some specific values of $n$:
$$\begin{align}
\bra{k}(a^\dagger-a)^{0}\ket{k}&=1\\
-\bra{k}(a^\dagger-a)^{2}\ket{k}&=2k+1\\
\bra{k}(a^\dagger-a)^{4}\ket{k}&=6k^2+6k+3

\end{align}$$
For some specific values of $k$:
$$\begin{align}
\bra{0}(a^\dagger-a)^{2n}\ket{0}&=(-1)^n\dfrac{(2n)!}{n!}\left(\dfrac{1}{2^{n}}\right),&n\ge0\\
\bra{1}(a^\dagger-a)^{2n}\ket{1}&=(-1)^n\dfrac{(2n)!}{n!}\left(\dfrac{1}{2^{n}}+\dfrac{n}{2^{n-1}}\right),&n\ge0\\
\bra{2}(a^\dagger-a)^{2n}\ket{2}&=(-1)^n\dfrac{(2n)!}{n!}\left(\dfrac{1}{2^{n}}+\dfrac{2n}{2^{n-1}}+\dfrac{1}{2^{n-2}}\dfrac{n(n-1)}{2}\right),&n\ge0\\
\bra{3}(a^\dagger-a)^{2n}\ket{3}&=(-1)^n\dfrac{(2n)!}{n!}\left(\dfrac{1}{2^{n}}+\dfrac{3n}{2^{n-1}}+\dfrac{3}{2^{n-2}}\dfrac{n(n-1)}{2}+\dfrac{1}{2^{n-3}}\dfrac{n(n-1)(n-2)}{6}\right),&n\ge0\\
\end{align}$$
