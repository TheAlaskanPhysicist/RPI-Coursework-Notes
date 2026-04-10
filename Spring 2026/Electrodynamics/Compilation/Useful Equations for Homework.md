

Electrostatic Boundary Conditions:
$$\begin{align}
\vec\nabla^2G(\vec{x},\vec{x}')&=-4\pi\delta(\vec{x}-\vec{x}') &\implies&& G(\vec{x},\vec{x}')&=\dfrac{1}{|\vec{x}-\vec{x}'|}+\operatorname{Ker}[\vec\nabla^2](\vec{x},\vec{x}')
\end{align}$$
Construct a Green's function that becomes $0$ where the field shall not propagate.



The Green's function of the Laplacian in spherical coordinates is:
$$\begin{align}
\dfrac{1}{|\vec{x}-\vec{x}'|}&=\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}\dfrac{r_<^l}{r_>^{l+1}}Y_l^{m*}(\theta',\phi')Y_l^m(\theta,\phi)
\end{align}$$

We can write the charge distribution in spherical coordinates as well:
$$\begin{align}
\rho(\vec{x}')&=\sum_{l=0}^\infty\sum_{m=-l}^{+l}\rho_{lm}(r')Y_l^m(\theta',\phi')
\end{align}$$
The potential in spherical coordinates is then:
$$\begin{align}
\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}\left[\dfrac{1}{r^{l+1}}\int_0^r r'^{l+2}\rho_{lm}(r')\ dr'+r^l\int_r^\infty\dfrac{1}{r'^{l-1}}\rho_{lm}(r')\ dr'\right]Y_l^m(\theta,\phi)
\end{align}$$




## Generalizing Fields
From the Lorenz gauge, we start with the *retarded Green's function*:
$$\begin{align}
G(\vec{x},t;\vec{x}',t')&=\dfrac{1}{|\vec{x}-\vec{x}'|}\delta\left(t-\left[t'+\dfrac{|\vec{x}-\vec{x}'|}{c}\right]\right)
\end{align}$$
The scalar and vector potential in this gauge decouple to:
$$\begin{align}
\Phi(\vec{x},t)&=\dfrac{1}{4\pi\epsilon_0}\iint G(\vec{x},t;\vec{x}',t')\ \rho(\vec{x}',t')\ d^3x'\ dt'\\
\vec{A}(\vec{x},t)&=\dfrac{\mu_0}{4\pi}\iint G(\vec{x},t;\vec{x}',t')\ \vec{J}(\vec{x}',t')\ d^3x'\ dt'
\end{align}$$
The Green's function can be written in spherical coordinates as:
$$\begin{align}
\dfrac{1}{|\vec{x}-\vec{x}'|}&=\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}\dfrac{r_<^l}{r_>^{l+1}}Y_l^{m*}(\theta',\phi')Y_l^m(\theta,\phi)
\end{align}$$
Substituting, we get:
$$\begin{align}
\Phi(\vec{x},t)&=\dfrac{1}{4\pi\epsilon_0}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}\left[\int\dfrac{r_<^l}{r_>^{l+1}}Y_l^{m*}(\theta',\phi')\ \rho(\vec{x}',t_r)\ d^3x'\right]Y_l^m(\theta,\phi)\\
\vec{A}(\vec{x},t)&=\dfrac{\mu_0}{4\pi}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}\left[\int\dfrac{r_<^l}{r_>^{l+1}}Y_l^{m*}(\theta',\phi')\ \vec{J}(\vec{x}',t_r)\ d^3x'\right]Y_l^m(\theta,\phi)
\end{align}$$

### Far-Field Limit
In the far-field limit, $r\gg r'$, so we expect that $r'<r$ always:
$$\begin{align}
\Phi(\vec{x},t)&=\dfrac{1}{4\pi\epsilon_0}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}\dfrac{Q_l^m(t)}{r^{l+1}}Y_l^m(\theta,\phi)\\
\vec{A}(\vec{x},t)&=\dfrac{\mu_0}{4\pi}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}\dfrac{M_l^m(t)}{r^{l+1}}Y_l^m(\theta,\phi)
\end{align}$$
Where we have these new multipole coefficients:
$$\begin{align}
Q_l^m(t)&=\int r'^lY_l^{m*}(\theta',\phi')\ \rho(\vec{x}',t)\ d^3x'\\
M_l^m(t)&=\int r'^lY_l^{m*}(\theta',\phi')\ \vec{J}(\vec{x}',t)\ d^3x'
\end{align}$$
The electric and magnetic fields are then:
$$\begin{align}
\vec{E}(\vec{x},t)&=-\dfrac{1}{4\pi\epsilon_0}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}Q_l^m(t)\left[\dfrac{1}{r^{l+1}}\vec\nabla Y_l^m(\theta,\phi)-\dfrac{l+1}{r^{l+2}}Y_l^m(\theta,\phi)\right]\\
&-\dfrac{\mu_0}{4\pi}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}\dfrac{\dot{M}_l^m(t)}{r^{l+1}}Y_l^m(\theta,\phi)\\
\vec{B}(\vec{x},t)&=\dfrac{\mu_0}{4\pi}\sum_{l=0}^\infty\sum_{m=-l}^{+l}\dfrac{4\pi}{2l+1}M_l^m(t)\left[\vec\nabla\times\dfrac{1}{r^{l+1}}Y_l^m(\theta,\phi)+\dfrac{1}{r^{l+1}}\vec\nabla\times Y_l^m(\theta,\phi)\right]
\end{align}$$







