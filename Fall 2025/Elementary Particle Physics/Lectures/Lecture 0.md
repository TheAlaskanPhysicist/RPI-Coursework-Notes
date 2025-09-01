---

---
Author: Stanley Goodwin
Date: August 28th, 2025

---
### Elementary Particle Physics
Almost all experimental information comes from:
 - Scattering
 - Decays
 - Bound states























### The Dirac Equation
We can find that the Dirac equation, written in SI units, can be expressed as:
$$\begin{align}
\left(i\hbar\gamma^\mu\partial_\mu-mc\right)\psi&=0
\end{align}$$
where $\psi$ is the Dirac Bi-spinor who's natural representational basis is:
$$\begin{align}
\psi\in\text{Span}\left\{\ket{e^-,\uparrow},\ket{e^-,\downarrow},\ket{e^+,\uparrow},\ket{e^+,\downarrow}\right\}
\end{align}$$
These are the product space of spin and electric charge of an electron.


 
### Field Gauge Transformation
When we make a choice on the basis of our Dirac particle, we maintain a level of degrees of freedom when there exists a transformation $U$ who maintains the same observable physics.

Suppose we have a general unitary transformation $U$, such that:
$$\begin{align}
\psi'&=U\psi
\end{align}$$
Since this kind of transformation is also a wavefunction, it should also satisfy the Dirac equation:
$$\begin{align}
\left(i\hbar\gamma^\mu\partial_\mu-mc\right)\psi'
&=\left(i\hbar\gamma^\mu\partial_\mu-mc\right)(U\psi)\\
&=\left(i\hbar\gamma^\mu\partial_\mu-mc\right)U\cdot\psi+U\left(i\hbar\gamma^\mu\partial_\mu-mc\right)\psi\\
&=\left(i\hbar\gamma^\mu\partial_\mu U-mcU\right)\psi+U\cdot0\\
&=\left(i\hbar\gamma^\mu\partial_\mu U-mcU\right)\psi
\end{align}$$





We would like to enforce that a unitary transformation $U$ makes the resultant wavefunction $\psi'$ also satisfy the Dirac equation, since we're effectively changing reference basis:
$$\begin{align}
\left(i\hbar\gamma^\mu\partial_\mu U-mcU\right)\psi&=0\\
\end{align}$$
We assume that the wavefunction is not trivial, and so:
$$\begin{align}
i\hbar\gamma^\mu\partial_\mu U-mcU&=0\\
\end{align}$$
### $U(1)$ Symmetry Transformation
If we assume that $U\in U(1)$, we can represent it as the following general form:
$$\begin{align}
U&=e^{i\phi}\\
\end{align}$$
From our equation to satisfy earlier, we can see that:
$$\begin{align}
i\hbar\gamma^\mu\partial_\mu U-mc\cdot U&=0\\
i\hbar\gamma^\mu\partial_\mu (e^{i\phi})-mc\cdot e^{i\phi}&=\\
i\hbar e^{i\phi}\gamma^\mu\partial_\mu (i\phi)-mc\cdot e^{i\phi}&=\\
-\hbar e^{i\phi}\gamma^\mu\partial_\mu\phi-mc\cdot e^{i\phi}&=\\
\hbar \gamma^\mu\partial_\mu\phi+mc&=\\
\gamma^\mu\partial_\mu\phi+\dfrac{mc}{\hbar}&=0\\
\end{align}$$
So as long as our equation satisfies the equation listed above, then expanded it satisfies:
$$\begin{align}
\gamma^0\dfrac{1}{c}\dfrac{\partial\phi}{\partial t}-\gamma^1\dfrac{\partial}{\partial x}\phi-\gamma^2\dfrac{\partial\phi}{\partial t}-\gamma^3\dfrac{\partial\phi}{\partial t}+\dfrac{mc}{\hbar}&=0\\
\end{align}$$
For reasons that will be more apparent later, we can represent $\phi=-qA$, where $A$ is a 4-vector:
$$\begin{align}
-q\gamma^\mu\partial_\mu A+\dfrac{mc}{\hbar}&=0\\
\end{align}$$
We can then write the final form of this equation as:
$$\begin{align}
\Aboxed{q\gamma^\mu\partial_\mu A&=\dfrac{mc}{\hbar}}\\
\end{align}$$

### Lagrangian Density of $U(1)$
The following definition of the Lagrangian Density is as follows:
$$\begin{align}
\mathcal{L}_\text{Dirac}&=\bar\psi\left(i\hbar c\gamma^\mu\partial_\mu-mc^2\right)\psi
\end{align}$$
where $\bar\psi$ is the Dirac dual of the bispinor field, represented as:
$$\begin{align}
\psi&=\begin{bmatrix}\psi_-^\uparrow&\psi_-^\downarrow&\psi_+^\uparrow&\psi_+^\downarrow\end{bmatrix}^T\\
\bar\psi&=\begin{bmatrix}\psi_-^\uparrow&\psi_-^\downarrow&-\psi_+^\uparrow&-\psi_+^\downarrow\end{bmatrix}
\end{align}$$
Under a local $U\in U(1)$ on $\psi$, we can find that:
$$\begin{align}
\mathcal{L}_\text{Dirac}&=\bar\psi'\left(i\hbar c\gamma^\mu\partial_\mu-mc^2\right)\psi'\\
&=\bar\psi U^\dagger\left(i\hbar c\gamma^\mu\partial_\mu-mc^2\right)U\psi\\
&=\bar\psi U^\dagger\left(i\hbar c\gamma^\mu\partial_\mu-mc^2\right)U\cdot\psi+\bar\psi U^\dagger U\left(i\hbar c\gamma^\mu\partial_\mu-mc^2\right)\psi
\end{align}$$
By the definition of unitarity, we know that $U^\dagger U=I$, and so:
$$\begin{align}
&=\bar\psi U^\dagger\left(i\hbar c\gamma^\mu\partial_\mu U-mc^2\cdot U\right)\cdot\psi+\bar\psi\left(i\hbar c\gamma^\mu\partial_\mu-mc^2\right)\psi\\
&=\bar\psi U^\dagger\left(i\hbar c\gamma^\mu\partial_\mu U-mc^2\cdot U\right)\cdot\psi+\bar\psi\left(i\hbar c\gamma^\mu\partial_\mu-mc^2\right)\psi\\
\end{align}$$

