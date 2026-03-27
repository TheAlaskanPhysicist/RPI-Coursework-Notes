

## Relativistic Kinetic Energy
The Taylor series approximation for relativistic kinetic energy is:
$$\begin{align}
T&=mc^2\sum_{n=1}^\infty\binom{2n}{n}\dfrac{1}{4^n}\left(\dfrac{v^2}{c^2}\right)^n
\end{align}$$
For the relativistic (kinetic energy) hydrogen atom, the Hamiltonian is:
$$\begin{align}
H&=-\dfrac{Ze^2}{4\pi\epsilon_0}\dfrac{1}{r}+mc^2\sum_{n=1}^\infty\binom{2n}{n}\dfrac{1}{4^nm^{2n}}\left(\dfrac{p^2}{c^2}\right)^n
\end{align}$$
This is painful to calculate, so we're going to use perturbation theory for calculating this system. We define the two following operators:
$$\begin{align}
H_0&=\dfrac{p^2}{2m}-\dfrac{Ze^2}{4\pi\epsilon_0}\dfrac{1}{r} & V&=mc^2\sum_{k=2}^\infty\binom{2k}{k}\left(\dfrac{p}{2mc}\right)^{2k}
\end{align}$$
The first-order energy corrections are as follows:
$$\begin{align}
E_n^{(1)}&=\bra{n^{(0)}}V\ket{n^{(0)}}\\
&=mc^2\sum_{k=2}^\infty\dfrac{1}{(2mc)^{2k}}\binom{2k}{k}\left\langle p^{2k}\right\rangle\\
&=mc^2\sum_{k=2}^\infty\dfrac{1}{(2mc)^{2k}}\binom{2k}{k}\left(i\hbar\dfrac{Z}{a_0}\right)^{2k}\dfrac{(n-l-1)!}{(n+l)!}\dfrac{1}{n^{2k}}\sum_{j=0}^{k}\binom{k}{j}(-2n)^{j}\prod_{s=1}^j\left(n^2-l(l+1)+s-1\right)\\
E_n^{(1)}&=mc^2\sum_{k=2}^\infty\sum_{j=0}^{k}\left(\dfrac{i\hbar Z}{2mca_0}\right)^{2k}\binom{2k}{k}\dfrac{(n-l-1)!}{(n+l)!}\dfrac{(-2)^{j}}{n^{2k-j}}\binom{k}{j}\prod_{s=1}^j\left(n^2-l(l+1)+s-1\right)
\end{align}$$
Since these energy terms are an alternating series and each term is monotonically decreasing, we know an upper bound of error in the first-order energy correction as:
$$\begin{align}
\left|E_n^{(1)}-E_n^{(1,K-1)}\right|&\le mc^2\left(\dfrac{\hbar Z}{2mca_0}\right)^{2K}\binom{2K}{K}\dfrac{(n-l-1)!}{n^{2K}(n+l)!}\sum_{j=0}^{K}\binom{K}{j}(2n)^{j}\prod_{s=1}^j\left(n^2-l(l+1)+s-1\right)
\end{align}$$
So the energy to the first order of a physical hydrogen atom is:
$$\begin{align}
E_n^{(1)}&=mc^2\sum_{k=2}^\infty\sum_{j=0}^{k}(-1)^{k-j}\dfrac{\alpha^{2k}}{4^{2k-j}}\binom{2k}{k}\binom{k}{j}\dfrac{(n-l-1)!}{n^{2k-j}(n+l)!}\prod_{s=1}^j\left(n^2-l(l+1)+s-1\right)
\end{align}$$
This doesn't account for the Darwin term or spin-orbit coupling, and the effectiveness of perturbation theory has pretty much run out for this system. To solve the real system, we would solve the Dirac equation exactly, which gives the result:
$$\begin{align}
E_{n,j}&=mc^2\left(1+\dfrac{(Z\alpha)^2}{(n-\delta_j)^2}\right)^{-1/2} & \delta_j&=j+\tfrac{1}{2}-\sqrt{\left(j+\tfrac{1}{2}\right)^2-(Z\alpha)^2}
\end{align}$$
The energy of the hydrogen atom is independent of the orbital angular momentum and spin state, only their combined angular momentum and principle quantum number.

If we do perturbation theory on all 3 terms, we'd get the lowest order term from the Dirac solution.












## Appendix I
The expected value of power of momentum of the classical hydrogen atom starts as:
$$\begin{align}
p^2&=2mE_n^{(0)}+\dfrac{Zme^2}{2\pi\epsilon_0}\dfrac{1}{r} &\implies&& p^{2k}&=\sum_{j=0}^{k}\binom{k}{j}\left(2mE_n^{(0)}\right)^{k-j}\left(\dfrac{Zme^2}{2\pi\epsilon_0}\dfrac{1}{r}\right)^j
\end{align}$$
Taking the expected value of this system, we have:
$$\begin{align}
\left\langle p^{2k}\right\rangle&=\sum_{j=0}^{k}\binom{k}{j}\left(2mE_n^{(0)}\right)^{k-j}\left(\dfrac{2\hbar^2Z}{a_0}\right)^j\left\langle\dfrac{1}{r^j}\right\rangle
\end{align}$$
The expected value of inverse powers are of the form:
$$\begin{align}
\left\langle\dfrac{1}{r^j}\right\rangle&=\dfrac{Z^j}{(na_0)^j}\dfrac{(n-l-1)!}{(n+l)!}\prod_{s=1}^j\left(n^2-l(l+1)+s-1\right)
\end{align}$$
Therefore the expected value of even powers of momentum, we have:
$$\begin{align}
\left\langle p^{2k}\right\rangle&=\left(i\hbar\dfrac{Z}{a_0}\right)^{2k}\dfrac{(n-l-1)!}{(n+l)!}\dfrac{1}{n^{2k}}\sum_{j=0}^{k}\binom{k}{j}(-2n)^{j}\prod_{s=1}^j\left(n^2-l(l+1)+s-1\right)
\end{align}$$











