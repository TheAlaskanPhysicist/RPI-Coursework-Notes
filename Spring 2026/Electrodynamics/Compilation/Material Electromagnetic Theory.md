
## Field Dynamics

### Maxwell's Equations of Motion
We start with Maxwell's equations in macroscopic media:
$$\begin{align}
\vec\nabla\cdot\vec{D}&=\rho_\text{free} &
\vec\nabla\times\vec{E}+\dfrac{\partial\vec{B}}{\partial t}&=0\\
\vec\nabla\cdot\vec{B}&=0 &
\vec\nabla\times\vec{H}-\dfrac{\partial\vec{D}}{\partial t}&=J_\text{free}
\end{align}$$
where we have the auxiliary fields $\vec{D}$ and $\vec{H}$, of the form:
$$\begin{align}
\vec{D}&=\vec{D}\left[\vec{E},\vec{B}\right] & \vec{H}&=\vec{H}\left[\vec{E},\vec{B}\right]
\end{align}$$
The square brackets indicate the fields may depend on the present and past field configurations.

---
### Electromagnetic Media
Materials are complicated. They often add a lot of complexity that doesn't appear when dealing with (classical) electromagnetism in vacuum. 

We can always write the fields in the following form:
$$\begin{align}
\vec{D}&=\epsilon_0\vec{E}+\vec{P}\left[\vec{E},\vec{B}\right] & \vec{H}&=\dfrac{1}{\mu_0}\vec{B}-\vec{M}\left[\vec{E},\vec{B}\right]
\end{align}$$
We can express these material field $\vec{P}$ and $\vec{M}$ as a tensor summation:
$$\begin{align}
\vec{P}\left[\vec{E},\vec{B}\right]&=
\sum_{n,m=0}^\infty\chi^{(n,m)}:\left(\vec{E}^{\otimes n}\otimes\vec{B}^{\otimes n}\right) & \vec{M}\left[\vec{E},\vec{B}\right]&=
\sum_{n,m=0}^\infty\eta^{(n,m)}:\left(\vec{E}^{\otimes n}\otimes\vec{B}^{\otimes n}\right)\\
\end{align}$$
where $\chi^{(n,m)},\eta^{(n,m)}$ are the susceptibility tensors, and $:$ means tensor contraction.

---
#### Instantaneous Linear Media
If we assume that the response is instant, and linear in $\vec{E},\vec{B}$, our expressions can simplify to:
$$\begin{align}
D_i&=\epsilon_{ij}E_j+\xi_{ij}B_j & H_i&=\zeta_{ij}E_j+(\mu^{-1})_{ij}B_j
\end{align}$$
This allows different permittivity and permeability in different axes to mix with the field, as well as a coupling between the Electric and Magnetic fields.

---
#### Non-Linear Optics
We often want to consider higher order electric field interactions with electric polarizability, with no coupling in the fields otherwise, and that magnetic field interactions are negligible:
$$\begin{align}
\vec{D}&=\epsilon_0\vec{E}+\epsilon_0\left(\chi^{(1)}\vec{E}+\chi^{(2)}:\vec{E}^{\otimes2}+\chi^{(3)}:\vec{E}^{\otimes3}+\dots\right)
\end{align}$$
---










### Linear, Isotropic, Instantaneous Medium
The case we usually use in Electrodynamics is a medium that is linear in the fundamental fields with a permittivity and permeability static in space and time, as well responses being instant:
$$\begin{align}
\vec{D}&=\epsilon\vec{E} & \vec{B}&=\mu\vec{H}
\end{align}$$




