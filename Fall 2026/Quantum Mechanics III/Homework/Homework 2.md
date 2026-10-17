**Author:** Stanley Goodwin
**Date:** October 24th, 2026

---
## Problem 2.1 / Question 3.1
> Recall from $\text{Eq. (3.17)}$ the Lorentz commutation relations,$$\left[J^{\mu\nu},J^{\rho\sigma}\right]=i\left(g^{\nu\rho}J^{\mu\sigma}-g^{\mu\rho}J^{\nu\sigma}-g^{\nu\sigma}J^{\mu\rho}+g^{\mu\sigma}J^{\nu\rho}\right)$$
### Question 3.1.A
> Define the generators of rotations and boosts as $$\begin{align}L^i&=\frac{1}{2}\epsilon^{ijk}J^{jk},&&&K^i&=J^{0i}\end{align}$$where $i,j,k=1,2,3$. An infinitesimal Lorentz transformation can then be written $$\Phi\left(1-i\vec\theta\cdot\vec{L}-i\vec\beta\cdot\vec{K}\right)\Phi$$Write the commutation relations of these vector operations explicitly. (For example, $\left[L^i,L^j\right]=i\epsilon^{ijk}L^k$.) Show that the combinations $$\begin{align}\vec{J}_+&=\frac{1}{2}\left(\vec{L}+i\vec{K}\right)&\text{and}&&\vec{J}_-&=\frac{1}{2}\left(\vec{L}-i\vec{K}\right)&&\end{align}$$commute with one another and separately satisfy the commutation relations of angular momentum.

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
&=0-i\epsilon^{b a c}L^c\\
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
---
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




---
### Question 3.1.C
> The identity $\vec{\sigma}^T=-\sigma^2\vec{\sigma}\sigma^2$ allows us to rewrite the $\psi_L$ transformation in the unitarily equivalent form $$\psi\to\psi'\left(1+i\vec{\theta}\cdot\frac{\vec{\sigma}}{2}+\vec{\beta}\cdot\frac{\vec{\sigma}}{2}\right),$$where $\psi'=\psi_L^T\sigma^2$. Using this law, we can represent the object that transforms as $\left( \frac{1}{2},\frac{1}{2}\right)$ as a $2\times2$ matrix that has the $\psi_R$ transformation law on the left and, simultaneously, the transposed $\psi_L$ transformation on the right. Parametrize this matrix as$$\left[\begin{array}{}V^0+V^3&V^1-iV^2\\V_1+iV^2&V^0-V^3\end{array}\right].$$ Show that the object $V^\mu$ transforms as a $4$-vector.




---
## Problem 2.2
> Here we go back to Problem 1.4 of Homework 1. The spontaneous symmetry breaking in this model is$$\mathrm{O}(N)\to\mathrm{O}(N-1).$$After we take this into account, the $\mathrm{O}(N-1)$ symmetry is linearly realized on the pions$$\pi_i\to\pi_i-\alpha^aT^a_{ij}\pi_j,$$where the $T^a$ matrices are the generators of $\mathrm{O}(N-1)$.

---
### Problem 2.2.A
> Derive the conserved currents associated with this symmetry transformation.

---
### Problem 2.2.B
> What is the corresponding symmetry transformation on the field associated with the symmetry breaking direction $\sigma=\phi_N=\pm\sqrt{1-\pi_i\pi_i}$.

---
## Problem 2.3
> Here we have the Lagrangian $$\mathcal{L}=\dfrac{1}{2}\partial_\mu\phi\partial^\mu\phi-\dfrac{1}{2}m^2\phi^2-\frac{g}{3!}\phi^3.$$Using the mode expansions from Peskin & Schroeder $(\text{PS-2.47})$ and the canonical commutation relation $(\text{PS-2.29})$, compute the $\mathcal{O}(g)$ fully connected correlation function$$\bra{0}\phi(x)\phi(y)\phi(z)\ket{0}.$$

---
## Problem 2.4
> What pole prescription (i.e., $\pm i\epsilon$ prescription) would give the anti-time-ordered two point function in the Klein-Gordon theory$$\begin{align}D_\bar{F}&=\theta(y^0-x^0)\bra{0}\phi(x)\phi(y)\ket{0}+\theta(x^0-y^0)\bra{0}\phi(y)\phi(x)\ket{0}\\&\equiv\bra{0}\bar{T}\phi(x)\phi(y)\ket{0}.\end{align}$$Write the answer as an integral over $d^4p$, analogous to $(\text{PS-2.59})$.

