
### Grand Canonical Ensemble (Indistinguishable)
Since there is no interaction between the particles, we can calculate $Z_1$ and work from that:
$$\begin{align}
Z&=\sum_{N=0}^\infty\int\dfrac{1}{N!}\dfrac{d^{3N}p\ d^{3N}q}{h^{3N}}e^{-\beta (\hat{H}-\mu\hat{N})}\\
&=\sum_{N=0}^\infty\int\dfrac{1}{N!}\dfrac{d^{3N}p\ d^{3N}q}{h^{3N}}\exp\left(-\beta\sum_{i=1}^{3N}\left(\dfrac{p_i^2}{2m}\right)+\beta\mu N\right)\\
&=\sum_{N=0}^\infty\dfrac{1}{N!}Z_1^Ne^{\beta\mu N}\\
&=\sum_{N=0}^\infty\dfrac{(Z_1e^{\beta\mu})^N}{N!}\\
\Aboxed{Z&=e^{Z_1e^{\beta\mu}}}, Z_1=\dfrac{V}{h^3}\left(2\pi mkT\right)^{3/2}
\end{align}$$
The grand free energy is then:
$$\begin{align}
\phi&=-kT\ln Z\\
&=-kTZ_1e^{\beta\mu}\\
\Aboxed{\phi(T,V,\mu)&=-kT\dfrac{V}{h^3}\left(2\pi mkT\right)^{3/2}e^{\beta\mu}}
\end{align}$$
The differential form of this free energy is:
$$\begin{align}
d\phi&=\left(\dfrac{\partial\phi}{\partial T}\right)_{V,\mu}dT+\left(\dfrac{\partial\phi}{\partial V}\right)_{T,\mu}dV+\left(\dfrac{\partial\phi}{\partial\mu}\right)_{T,V}d\mu
\end{align}$$
This then leads to the following:
$$\begin{align}
-S=\left(\dfrac{\partial\phi}{\partial T}\right)_{V,\mu}&=\dfrac{5}{2}\dfrac{\phi}{T}-\dfrac{\mu\phi}{kT^2}\\
-P=\left(\dfrac{\partial\phi}{\partial V}\right)_{T,\mu}&=\dfrac{\phi}{V}\\
-N=\left(\dfrac{\partial\phi}{\partial\mu}\right)_{T,V}&=\dfrac{\phi}{kT}
\end{align}$$
And thus leading to:
$$\begin{align}
\phi(T,V,\mu)&=-\dfrac{kT^2}{\tfrac{5}{2}kT-\mu}S=-PV=-NkT\\
N&=\dfrac{V}{h^3}\left(2\pi mkT\right)^{3/2}e^{\mu/kT}\\
P&=kT\dfrac{1}{h^3}\left(2\pi mkT\right)^{3/2}e^{\mu/kT}\\
S&=\left(\dfrac{5}{2}k-\dfrac{\mu}{T}\right)\dfrac{V}{h^3}\left(2\pi mkT\right)^{3/2}e^{\mu/kT}
\end{align}$$
Substituting $N$ into $P$, we get:
$$\begin{align}
P(T,V,N)&=\dfrac{NkT}{V}\\
\end{align}$$


