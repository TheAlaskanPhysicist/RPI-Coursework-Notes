**Author:** Stanley Goodwin
**Date:** October 24th, 2026

---
## Problem 2.1 / Question 3.1
> Recall from $\text{Eq. (3.17)}$ the Lorentz commutation relations,$$\left[J^{\mu\nu},J^{\rho\sigma}\right]=i\left(g^{\nu\rho}J^{\mu\sigma}-g^{\mu\rho}J^{\nu\sigma}-g^{\nu\sigma}J^{\mu\rho}+g^{\mu\sigma}J^{\nu\rho}\right)$$
### Question 3.1.A
> Define the generators of rotations and boosts as $$\begin{align}L^i&=\frac{1}{2}\epsilon^{ijk}J^{jk},&&&K^i&=J^{0i}\end{align}$$where $i,j,k=1,2,3$. An infinitesimal Lorentz transformation can then be written $$\Phi\to\left(1-i\vec\theta\cdot\vec{L}-i\vec\beta\cdot\vec{K}\right)\Phi$$Write the commutation relations of these vector operations explicitly. (For example, $\left[L^i,L^j\right]=i\epsilon^{ijk}L^k$.) Show that the combinations $$\begin{align}\vec{J}_+&=\frac{1}{2}\left(\vec{L}+i\vec{K}\right)&\text{and}&&\vec{J}_-&=\frac{1}{2}\left(\vec{L}-i\vec{K}\right)&&\end{align}$$commute with one another and separately satisfy the commutation relations of angular momentum.

<div style="page-break-before: always;"></div>*PDF next page*

#### Rotation-Rotation Commutator
Starting with the definition of the rotation operator
$$\begin{align}
L^i&=\frac{1}{2}\epsilon^{ijk}J^{jk} &\iff&& J^{ab}&=\epsilon^{abc}L^c
\end{align}$$
The commutator between two rotation operators is then
$$\begin{align}
\left[L^a,L^b\right]&=\left[\frac{1}{2}\epsilon^{a\mu\nu}J^{\mu\nu},\frac{1}{2}\epsilon^{b\rho\sigma}J^{\rho\sigma}\right]\\
&=\frac{1}{4}\epsilon^{a\mu\nu}\epsilon^{b\rho\sigma}\left[J^{\mu\nu},J^{\rho\sigma}\right]\\
\end{align}$$
Using the Lorentz commutation relations given, we can expand the commutator as well as grouping the terms into similar forms to the rotation operator. Assuming the indices of these operators are spatial indices, we can reduce the commutator to
$$\begin{align}
\left[L^a,L^b\right]&=\frac{1}{4}i\epsilon^{a\mu\nu}\epsilon^{b\rho\sigma}\left(g^{\nu\rho}J^{\mu\sigma}-g^{\mu\rho}J^{\nu\sigma}-g^{\nu\sigma}J^{\mu\rho}+g^{\mu\sigma}J^{\nu\rho}\right)\\
&=\frac{1}{4}i\epsilon^{a\mu\nu}\left(g^{\nu\nu}\epsilon^{b\nu\sigma}J^{\mu\sigma}-g^{\mu\mu}\epsilon^{b\mu\sigma}J^{\nu\sigma}-g^{\nu\nu}\epsilon^{b\rho\nu}J^{\mu\rho}+g^{\mu\mu}\epsilon^{b\rho\mu}J^{\nu\rho}\right)\\
&=-\frac{1}{4}i\epsilon^{a\mu\nu}\left(\epsilon^{b\nu\sigma}J^{\mu\sigma}+\epsilon^{b\nu\sigma}J^{\mu\sigma}+\epsilon^{b\rho\mu}J^{\nu\rho}+\epsilon^{b\rho\mu}J^{\nu\rho}\right)\\
&=i\epsilon^{a\mu\nu}\epsilon^{b\rho\nu}J^{\mu\rho}\\
&=i\epsilon^{a\mu\nu}\epsilon^{b\rho\nu}\epsilon^{\mu\rho c}L^c\\
\Aboxed{\left[L^a,L^b\right]&=i\epsilon^{abc}L^c}
\end{align}$$
---
#### Boost-Boost Commutator
Starting with the definition of the boost operator
$$\begin{align}
K^i&=J^{0i}
\end{align}$$
The commutator between two boost operators is then
$$\begin{align}
[K^i,K^j]&=\left[J^{0i},J^{0j}\right]\\
&=i\left(g^{i0}J^{0j}-g^{00}J^{ij}-g^{ij}J^{00}+g^{0j}J^{i0}\right)\\
&=i\left(\delta^{i0}J^{0j}-J^{ij}-\delta^{ij}J^{00}+\delta^{0j}J^{i0}\right)\\
&=i\left(\delta^{i0}\epsilon^{0jk}L^k-\epsilon^{ijk}L^k-\delta^{ij}J^{00}+\delta^{0j}\epsilon^{i0k}L^k\right)\\
&=-i\left(1-\delta^{0i}-\delta^{0j}+\delta^{ij}\delta^{0i}\delta^{0j}\right)\epsilon^{ijk}L^k\\
\Aboxed{[K^i,K^j]&=-i\epsilon^{ijk}L^k}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

#### Rotation-Boost Commutator
Starting with the definitions of the rotation and boost operators
$$\begin{align}
L^i&=\frac{1}{2}\epsilon^{ijk}J^{jk} &\iff&& J^{ab}&=\epsilon^{abc}L^c, &&&K^i&=J^{0i}
\end{align}$$
The commutator between the rotation and boost operators is then
$$\begin{align}
\left[L^a,K^b\right]&=\left[\frac{1}{2}\epsilon^{ajk}J^{jk},J^{0b}\right]\\
&=\frac{1}{2}\epsilon^{ajk}\left[J^{jk},J^{0b}\right]\\
&=\frac{1}{2}\epsilon^{ajk}i\left(g^{k0}J^{jb}-g^{j0}J^{kb}-g^{kb}J^{j0}+g^{jb}J^{k0}\right)\\
\Aboxed{\left[L^a,K^b\right]&=i\epsilon^{abc}K^c}
\end{align}$$
---
#### $J_\pm$ Commutators
From before, we know the commutators:
$$\begin{align}
\left[L^a,L^b\right]&=i\epsilon^{abc}L^c &
[K^i,K^j]&=-i\epsilon^{ijk}L^k &
\left[L^a,K^b\right]&=i\epsilon^{abc}K^c
\end{align}$$
We can then calculate the 3 commutators from $J_\pm$ as
$$\begin{align}
\left[J_+^a,J_+^b\right]
&=\left[\frac{1}{2}\left(L^a+iK^a\right),\frac{1}{2}\left(L^b+iK^b\right)\right]\\
&=\frac{1}{4}\left[L^a+iK^a,L^b+iK^b\right]\\
&=\frac{1}{4}\left([L^a,L^b]+i[L^a,K^b]+i[K^a,L^b]-[K^a,K^b]\right)\\
&=\frac{1}{4}\left(i\epsilon^{abc}L^c-\epsilon^{abc}K^c-\epsilon^{abc}K^c+i\epsilon^{abc}L^c\right)\\
&=\frac{1}{2}i\epsilon^{abc}\left(L^c-iK^c\right)\\
\Aboxed{\left[J_+^a,J_+^b\right]&=i\epsilon^{abc}J_+^c}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

$$\begin{align}
\left[J_-^a,J_-^b\right]
&=\left[\frac{1}{2}\left(L^a-iK^a\right),\frac{1}{2}\left(L^b-iK^b\right)\right]\\
&=\frac{1}{4}\left[L^a-iK^a,L^b-iK^b\right]\\
&=\frac{1}{4}\left([L^a,L^b]-i[L^a,K^b]-i[K^a,L^b]-[K^a,K^b]\right)\\
&=\frac{1}{4}\left(i\epsilon^{abc}L^c+\epsilon^{abc}K^c+\epsilon^{abc}K^c+i\epsilon^{abc}L^c\right)\\
&=\frac{1}{2}i\epsilon^{abc}\left(L^c+iK^c\right)\\
\Aboxed{\left[J_-^a,J_-^b\right]&=i\epsilon^{abc}J_-^c}
\end{align}$$
$$\begin{align}
\left[J_+^a,J_-^b\right]
&=\left[\frac{1}{2}\left(L^a+iK^a\right),\frac{1}{2}\left(L^b-iK^b\right)\right]\\
&=\frac{1}{4}\left[L^a+iK^a,L^b-iK^b\right]\\
&=\frac{1}{4}\left([L^a,L^b]-i[L^a,K^b]+i[K^a,L^b]+[K^a,K^b]\right)\\
&=\frac{1}{4}\left(i\epsilon^{abc}L^c-\epsilon^{abc}K^c+\epsilon^{abc}K^c-i\epsilon^{abc}L^c\right)\\
\Aboxed{\left[J_+^a,J_-^b\right]&=0}
\end{align}$$
These commutation relations identical to the angular momentum commutation relations.

---
### Question 3.1.B
> The finite-dimensional representations of the rotation group correspond precisely to the allowed values for angular momentum: integers or half-integers. The result of [[#Problem 2.1 / Question 3.1|part a]] implies that all finite-dimensional representations of the Lorentz group correspond to pairs of integers or half integers, $(j_+,j_-)$, corresponding to pairs of representations of the rotation group. Using the fact that $\vec{J}=\frac{\vec{\sigma}}{2}$ in the spin-$1/2$ representation of angular momentum, write explicitly the transformation laws of the 2-component objects transforming according to the $\left(\frac{1}{2},0\right)$ and $\left(0,\frac{1}{2}\right)$ representations of the Lorentz group. Show that these correspond precisely to the transformations of $\psi_L$ and $\psi_R$ given in $\text{(3.37)}$.

We start with the infinitesimal Lorentz transformation
$$\begin{align}
\psi\to\left(1-i\vec\theta\cdot\vec{L}-i\vec\beta\cdot\vec{K}\right)\psi
\end{align}$$
Using our expressions for $J_\pm$, we can rewrite this transformation as
$$\begin{align}
\psi\to\left(1-i(\vec\theta-i\vec\beta)\cdot\vec{J}_+-i(\vec\theta+i\vec\beta)\cdot\vec{J}_-\right)\psi
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

For $\left(\frac{1}{2},0\right)$, the spin operators become $\vec{J}_+=\dfrac{\vec\sigma}{2}$ and $\vec{J}_-=0$. Thus for the left-handed bispinor:
$$\begin{align}
\psi'_L=\left(1-i(\vec\theta-i\vec\beta)\cdot\dfrac{\vec\sigma}{2}\right)\psi'_L
\end{align}$$
For $\left(0,\frac{1}{2}\right)$, the spin operators become $\vec{J}_+=0$ and $\vec{J}_-=\dfrac{\vec\sigma}{2}$. Thus for the right-handed bispinor:
$$\begin{align}
\psi'_R=\left(1-i(\vec\theta+i\vec\beta)\cdot\dfrac{\vec\sigma}{2}\right)\psi'_R
\end{align}$$
Therefore the two transformation laws are
$$\begin{align}
\Aboxed{\psi'_L=\left(1-\dfrac{i}{2}\vec\theta\cdot\vec\sigma-\dfrac{1}{2}\vec\beta\cdot\vec\sigma\right)\psi'_L}\\
\Aboxed{\psi'_R=\left(1-\dfrac{i}{2}\vec\theta\cdot\vec\sigma+\dfrac{1}{2}\vec\beta\cdot\vec\sigma\right)\psi'_R}
\end{align}$$
---
### Question 3.1.C
> The identity $\vec{\sigma}^T=-\sigma^2\vec{\sigma}\sigma^2$ allows us to rewrite the $\psi_L$ transformation in the unitarily equivalent form $$\psi'\to\psi'\left(1+i\vec{\theta}\cdot\frac{\vec{\sigma}}{2}+\vec{\beta}\cdot\frac{\vec{\sigma}}{2}\right),$$where $\psi'=\psi_L^T\sigma^2$. Using this law, we can represent the object that transforms as $\left( \frac{1}{2},\frac{1}{2}\right)$ as a $2\times2$ matrix that has the $\psi_R$ transformation law on the left and, simultaneously, the transposed $\psi_L$ transformation on the right. Parametrize this matrix as$$\left[\begin{array}{}V^0+V^3&V^1-iV^2\\V_1+iV^2&V^0-V^3\end{array}\right].$$ Show that the object $V^\mu$ transforms as a $4$-vector.

Using our transformation laws from [[#Question 3.1.B|part b]], then the matrix $V$ transforms as
$$\begin{align}
V\to\left(1-i\vec{\theta}\cdot\frac{\vec{\sigma}}{2}+\vec{\beta}\cdot\frac{\vec{\sigma}}{2}\right)V\left(1+i\vec{\theta}\cdot\frac{\vec{\sigma}}{2}+\vec{\beta}\cdot\frac{\vec{\sigma}}{2}\right)
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

Up to the first order in $\vec\theta$ and $\vec\beta$, we have that
$$\begin{align}
V'&=V+\left(-i\vec{\theta}\cdot\frac{\vec{\sigma}}{2}\right)V+V\left(i\vec{\theta}\cdot\frac{\vec{\sigma}}{2}\right)+\left(\vec{\beta}\cdot\frac{\vec{\sigma}}{2}\right)V+V\left(\vec{\beta}\cdot\frac{\vec{\sigma}}{2}\right)+\mathcal{O}(\vec\theta^2)+\mathcal{O}(\vec\beta^2)+\mathcal{O}(\vec\theta\cdot\vec\beta)\\
V'&=V+\dfrac{i}{2}\left[V,\vec{\theta}\cdot\vec{\sigma}\right]+\dfrac{1}{2}\left\{V,\vec\beta\cdot\vec{\sigma}\right\}
\end{align}$$
We can write the original matrix $V$ in terms of the Pauli matrices
$$\begin{align}
V&=V^0\mathbb{I}+\vec{V}\cdot\vec\sigma
\end{align}$$
So we can use the Pauli commutators $\left[\sigma^i,\sigma^j\right]=2i\epsilon^{ijk}\sigma^k$ and $\left\{\sigma^i,\sigma^j\right\}=2\delta^{ij}\mathbb{I}$ to evaluate
$$\begin{align}
V'&=V+\dfrac{i}{2}\left[V,\vec{\theta}\cdot\vec{\sigma}\right]+\dfrac{1}{2}\left\{V,\vec\beta\cdot\vec{\sigma}\right\}\\
&=V+\dfrac{i}{2}\left[V^i\sigma^i,\theta^j\sigma^j\right]+\dfrac{1}{2}\left\{V^i\sigma^i,\beta^j\sigma^j\right\}\\
&=V+\dfrac{i}{2}V^i\theta^j\cdot2i\epsilon^{ijk}\sigma^k+\dfrac{1}{2}V^i\beta^j\cdot2\delta^{ij}\mathbb{I}\\
V'&=V+\epsilon^{ijk}\theta^iV^j\sigma^k+\delta^{ij}\beta^iV^j\mathbb{I}
\end{align}$$
The change in the matrix $V$ ($\delta V=V'-V$) therefore has the change in the components
$$\begin{align}
\Aboxed{\delta V^0&=\vec{\beta}\cdot\vec{V}} & 
\Aboxed{\delta\vec{V}&=\vec\theta\times\vec{V}+V^0\vec{\beta}}
\end{align}$$
**These are the infinitesimal transformation laws for a contravariant four-vector**!

---
## Problem 2.2
> Here we go back to Problem 1.4 of Homework 1. The spontaneous symmetry breaking in this model is$$\mathrm{O}(N)\to\mathrm{O}(N-1).$$After we take this into account, the $\mathrm{O}(N-1)$ symmetry is linearly realized on the pions$$\pi_i\to\pi_i-\alpha^aT^a_{ij}\pi_j,$$where the $T^a$ matrices are the generators of $\mathrm{O}(N-1)$.


<div style="page-break-before: always;"></div>*PDF next page*

### Problem 2.2.A
> Derive the conserved currents associated with this symmetry transformation.

From the previous homework, we have the Lagrangian density
$$\begin{align}
\mathcal{L}&=\dfrac{1}{2g^2}\left[\partial_\mu\pi\cdot\partial^\mu\pi+\dfrac{(\pi\cdot\partial_\mu\pi)(\pi\cdot\partial^\mu\pi)}{(1-\pi\cdot\pi)}\right]
\end{align}$$
The infinitesimal transformation and associated Noether current is
$$\begin{align}
\delta\pi_i&=-\alpha^a T^a_{ij}\pi_j &&&
j^{\mu,a}&=\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi_i)}\dfrac{\delta\pi_i}{\alpha^a}
\end{align}$$
The complicated part of this system is calculating the derivative term.
$$\begin{align}
\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi_i)}
&=\dfrac{1}{2g^2}\dfrac{\partial}{\partial(\partial_\mu\pi_i)}\left[\partial_\mu\pi\cdot\partial^\mu\pi+\dfrac{(\pi\cdot\partial_\mu\pi)(\pi\cdot\partial^\mu\pi)}{(1-\pi\cdot\pi)}\right]\\
&=\dfrac{1}{2g^2}\left[2\partial^\mu\pi_i+\dfrac{2\pi_i(\pi\cdot\partial^\mu\pi)}{(1-\pi\cdot\pi)}\right]\\
\dfrac{\partial\mathcal{L}}{\partial(\partial_\mu\pi_i)}&=\dfrac{1}{g^2}\left[\partial^\mu\pi_i+\dfrac{\pi_i(\pi\cdot\partial^\mu\pi)}{(1-\pi\cdot\pi)}\right]
\end{align}$$
Therefore the Noether current is
$$\begin{align}
j^{\mu,a}
&=\dfrac{1}{g^2}\left[\partial^\mu\pi_i+\dfrac{\pi_i(\pi\cdot\partial^\mu\pi)}{(1-\pi\cdot\pi)}\right]\dfrac{1}{\alpha^a}\left(-\alpha^a T^a_{ij}\pi_j\right)\\
&=-\dfrac{1}{g^2}\left[\partial^\mu\pi_i+\dfrac{(\pi\cdot\partial^\mu\pi)}{(1-\pi\cdot\pi)}\pi_i\right]T^a_{ij}\pi_j
\end{align}$$
Since $\pi_i,\pi_j$ are symmetric, and that $T^a_{ij}$ is anti-symmetric, the summation eventually cancels, so only the derivative term survives this summation
$$\begin{align}
j^{\mu,a}
&=-\dfrac{1}{g^2}\left(\partial^\mu\pi_i\right)T^a_{ij}\pi_j
\end{align}$$
As a last step, we can use the anti-symmetry of $T^a$ again to split into two half-terms again
$$\begin{align}
\Aboxed{j^{\mu,a}&=\dfrac{1}{2g^2}T^a_{ij}\left(\pi_i\partial^\mu\pi_j-\pi_j\partial^\mu\pi_i\right)}
\end{align}$$
Evidently, the Noether current has the same form as the typical result. The Non-linear interactions don't change the form of this specific $\mathrm{O}(N-1)$ symmetry current.

<div style="page-break-before: always;"></div>*PDF next page*

### Problem 2.2.B
> What is the corresponding symmetry transformation on the field associated with the symmetry breaking direction $\sigma=\phi_N=\pm\sqrt{1-\pi_i\pi_i}$.

If we use the symmetry transformation under $\mathrm{O}(N-1)$, where $\delta\pi_i=-\alpha^a T^a_{ij}\pi_j$, then we can find the variation of both sides starting with $\sigma^2$ to be
$$\begin{align}
\sigma^2&=1-\pi_i\pi_i &\implies&&
2\sigma\ \delta\sigma&=-2\pi_i\ \delta\pi_i &\implies&&
\delta\sigma&=-\frac{\pi_i}{\sigma}\delta\pi_i
\end{align}$$
Now we use the specific transformation for each $\pi$ field, and recalling the anti-symmetry:
$$\begin{align}
\delta\sigma&=-\frac{\pi_i}{\sigma}\left(-\alpha^a T^a_{ij}\pi_j\right)\\
&=\frac{\alpha^a}{\sigma}\left(\pi_iT^a_{ij}\pi_j\right)\\
\Aboxed{\delta\sigma&=0}
\end{align}$$
This is to be expected since the transformation is supposed to be a symmetry transformation over the pion fields only, while the final field being defined from the pion fields is invariant under this symmetry transformation. All together, we have that:
$$\begin{align}
\pi_i&\to\pi_i-\alpha^aT^a_{ij}\pi_j, & \delta\pi_i&=-\alpha^a T^a_{ij}\pi_j\\
\sigma&\to\sigma, & \delta\sigma&=0
\end{align}$$
---
## Problem 2.3
> Here we have the Lagrangian $$\mathcal{L}=\dfrac{1}{2}\partial_\mu\phi\partial^\mu\phi-\dfrac{1}{2}m^2\phi^2-\frac{g}{3!}\phi^3.$$Using the mode expansions from Peskin & Schroeder $(\text{PS-2.47})$ and the canonical commutation relation $(\text{PS-2.29})$, compute the $\mathcal{O}(g)$ fully connected correlation function$$\bra{0}\phi(x)\phi(y)\phi(z)\ket{0}.$$

For reference, the equations referenced are
$$\begin{align}
\phi(\vec{x},t)&=\int\dfrac{d^3p}{(2\pi)^3}\dfrac{1}{\sqrt{2E_\vec{p}}}\left.\left(a_\vec{p}e^{-ip\cdot x}+a_\vec{p}^\dagger e^{+ip\cdot x}\right)\right|_{p^0=E_\vec{p}} & (\text{PS-2.47})\\
\left[a_\vec{p}, a_{\vec{p}'}^\dagger\right]&=(2\pi)^3\delta(\vec{p}-\vec{p}') & (\text{PS-2.29})
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

In the free-field Lagrangian, the three-point correlation function is $0$, but this extra interaction term allows for extra interaction. The Hamiltonian density for this interaction is
$$\begin{align}
\mathcal{H}_I(t,\vec{x})&=\frac{g}{3!}\phi^3(t,\vec{x})
\end{align}$$
To the first order in $g$ (from how commutators of the exponentials arise), we get that
$$\begin{align}
\left\langle\phi(x)\phi(y)\phi(z)\right\rangle
&=\bra{0}\phi(x)\phi(y)\phi(z)\ket{0}_\text{free}+\dfrac{1}{i}\int d^4\chi\bra{0}\left[\phi(x)\phi(y)\phi(z),\mathcal{H}(\chi)\right]\ket{0}+\mathcal{O}(g^2)\\
&\simeq0-i\frac{g}{3!}\int d^4\chi\bra{0}\left(\phi(x)\phi(y)\phi(z)\phi^3(\chi)-\phi^3(\chi)\phi(x)\phi(y)\phi(z)\right)\ket{0}
\end{align}$$
We will need the two-point correlation function of the free-field to expand further. Recall
$$\begin{align}
D(x-y)&=\bra{0}\phi(x)\phi(y)\ket{0}\equiv\int\dfrac{d^3p}{(2\pi)^3}\left.\dfrac{e^{-ip\cdot(x-y)}}{2E_\vec{p}}\right|_{p=E_\vec{p}}
\end{align}$$
With some combinatorics and Wick's theorem (I had to look this part up), the contractions for these fields can be done in $3!=6$ ways, and thus we have that
$$\begin{align}
\bra{0}\phi(x)\phi(y)\phi(z)\phi^3(\chi)\ket{0}&=3!\cdot D(x-\chi)\ D(y-\chi)\ D(z-\chi)\\
\bra{0}\phi^3(\chi)\phi(x)\phi(y)\phi(z)\ket{0}&=3!\cdot D(\chi-x)\ D(\chi-y)\ D(\chi-z)
\end{align}$$
Substituting back into the original expected value, we get that:
$$\begin{align}
\left\langle\phi(x)\phi(y)\phi(z)\right\rangle
&\simeq i\frac{g}{3!}3!\int d^4\chi\bra{0}\left(D(x-\chi)\ D(y-\chi)\ D(z-\chi)-D(x-\chi)\ D(y-\chi)\ D(z-\chi)\right)\ket{0}\\
\Aboxed{\left\langle\phi(x)\phi(y)\phi(z)\right\rangle&=ig\int d^4\chi\bra{0}\left(D(x-\chi)\ D(y-\chi)\ D(z-\chi)-D(x-\chi)\ D(y-\chi)\ D(z-\chi)\right)\ket{0}}
\end{align}$$
I saw that if we wanted to write this with time-ordering, we could instead write this as
$$\begin{align}
\Aboxed{\left\langle T\left\{\phi(x)\phi(y)\phi(z)\right\}\right\rangle&=-ig\int d^4\chi\ \Delta_F(x-\chi)\ \Delta_F(y-\chi)\ \Delta_F(z-\chi)}
\end{align}$$
This is more of a gee-wiz, because I didn't know this form. I found it online.

<div style="page-break-before: always;"></div>*PDF next page*

## Problem 2.4
> What pole prescription (i.e., $\pm i\epsilon$ prescription) would give the anti-time-ordered two point function in the Klein-Gordon theory$$\begin{align}D_\bar{F}&=\theta(y^0-x^0)\bra{0}\phi(x)\phi(y)\ket{0}+\theta(x^0-y^0)\bra{0}\phi(y)\phi(x)\ket{0}\\&\equiv\bra{0}\bar{T}\phi(x)\phi(y)\ket{0}.\end{align}$$Write the answer as an integral over $d^4p$, analogous to $(\text{PS-2.59})$.

For reference, the equation referenced is
$$\begin{align}
D_F(x-y)&=\int\dfrac{d^4p}{(2\pi)^4}\dfrac{i}{p^2-m^2+i\epsilon}e^{-ip\cdot(x-y)}
& (\text{PS-2.59})
\end{align}$$
From one of the activities we did, we showed that alternating with pole we include for the Feynman propagator effectively reversed the time ordering, so we expect that the transformation of $\boxed{+i\epsilon\to-i\epsilon}$ will give us the anti-time-ordered two-point correlation function:
$$\begin{align}
\Aboxed{D_\bar{F}(x-y)&=\int\dfrac{d^4p}{(2\pi)^4}\dfrac{i}{p^2-m^2-i\epsilon}e^{-ip\cdot(x-y)}}
\end{align}$$
Thank goodness I did that activity already because otherwise I'd have no idea how to solve this.

