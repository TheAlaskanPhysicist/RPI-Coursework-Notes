Author: Stanley Goodwin
Date: February 10th, 2026

---
## Question 4.7
**Note for the grader:** This is the same as my Homework #1 solution, copy-pasted.
### Question 4.7.A
Let $\psi(\vec{x},t)$ be the wave function of a spinless particle corresponding to a plane-wave in three dimensions. Show that $\psi^*(\vec{x},-t)$ is a wavefunction for the plane wave with the momentum direction reversed.

A three-dimensional plane-wave wavefunction as:
$$\begin{align}
\psi(\vec{x},t)&=A\exp\left(i\vec{k}\cdot\vec{x}-i\omega t\right)
\end{align}$$
Applying time-reversal and complex conjugation, we get:
$$\begin{align}
\psi^*(\vec{x},-t)
&=\left[A\exp\left(i\vec{k}\cdot\vec{x}-i\omega (-t)\right)\right]^*\\
&=\left[A\exp\left(i\vec{k}\cdot\vec{x}+i\omega t\right)\right]^*\\
&=A\exp\left(-i\vec{k}\cdot\vec{x}-i\omega t\right)\\
\Aboxed{\psi^*(\vec{x},-t)&=A\exp\left(i(-\vec{k})\cdot\vec{x}-i\omega t\right)}
\end{align}$$
This operation looks identical to the prior wavefunction with the momentum direction reversed.

---
### Question 4.7.B
Let $\chi(\hat{n})$ be the two-component eigenspinor $\sigma\cdot\hat{n}$ with eigenvalue $+1$. *Using the explicit form of* $\chi(\hat{n})$, in terms of polar and azimuthal angles $\beta$ and $\gamma$ that characterize $\hat{n}$, verify that $-i\sigma_2\chi^*(\hat{n})$ is the two-component eigenspinor with the spin direction reversed.

We can start by writing the eigenspinor in as Euler angles (in the Z-basis):
$$\begin{align}
\chi(\hat{n})&=\begin{bmatrix}\cos(\beta/2)\\e^{i\gamma}\sin(\beta/2)\end{bmatrix}
& \implies &&
\chi^*(\hat{n})&=\begin{bmatrix}\cos(\beta/2)\\e^{-i\gamma}\sin(\beta/2)\end{bmatrix}
\end{align}$$
If I remember correctly, $\sigma_2=\sigma_y$, and so:
$$\begin{align}
-i\sigma_2\chi^*(\hat{n})&=-i\begin{bmatrix}0&-i\\i&0\end{bmatrix}
\begin{bmatrix}\cos(\beta/2)\\e^{-i\gamma}\sin(\beta/2)\end{bmatrix}\\
&=\begin{bmatrix}0&-1\\1&0\end{bmatrix}
\begin{bmatrix}\cos(\beta/2)\\e^{-i\gamma}\sin(\beta/2)\end{bmatrix}\\
\chi(-\hat{n})&=\begin{bmatrix}-e^{-i\gamma}\sin(\beta/2)\\\cos(\beta/2)\end{bmatrix}
\end{align}$$
To verify, we can evaluate the inner product of these two vectors:
$$\begin{align}
\chi(-\hat{n})^\dagger\chi(\hat{n})
&=\begin{bmatrix}-e^{-i\gamma}\sin(\beta/2)\\\cos(\beta/2)\end{bmatrix}^\dagger
\begin{bmatrix}\cos(\beta/2)\\e^{i\gamma}\sin(\beta/2)\end{bmatrix}\\
&=\begin{bmatrix}-e^{i\gamma}\sin(\beta/2)&\cos(\beta/2)\end{bmatrix}
\begin{bmatrix}\cos(\beta/2)\\e^{i\gamma}\sin(\beta/2)\end{bmatrix}\\
&=-e^{i\gamma}\sin(\beta/2)\cos(\beta/2)+\cos(\beta/2)e^{i\gamma}\sin(\beta/2)\\
&=-e^{i\gamma}\sin(\beta/2)\cos(\beta/2)+e^{i\gamma}\sin(\beta/2)\cos(\beta/2)\\
\Aboxed{\chi(-\hat{n})^\dagger\chi(\hat{n})&=0}
\end{align}$$
This is, indeed, the opposite spin state, and thus concludes the proof.

---
## Question 5.7
Consider an isotropic harmonic oscillator in two dimensions. The Hamiltonian is:
$$
H_{0}=\dfrac{p_{x}^{2}}{2m}+\dfrac{p_{y}^{2}}{2m}+\dfrac{m\omega^{2}}{2}\left(x^{2}+y^{2}\right)
$$
### Question 5.7.A
What are the energies of the three lowest-lying states? Is there any degeneracy?

The first thing I thought of was the Schwinger picture for angular momenta, so I believe it's probably best to start with representing our Hamiltonian in terms of creation/annihilation.
$$
\begin{align}
x&=\sqrt{\dfrac{\hbar}{2m\omega}}\left(a^{\dagger}+a\right) & p_{x}&=i\sqrt{\dfrac{\hbar m\omega}{2}}\left(a^{\dagger}-a\right) \\
y&=\sqrt{\dfrac{\hbar}{2m\omega}}\left(b^{\dagger}+b\right) & p_{y}&=i\sqrt{\dfrac{\hbar m\omega}{2}}\left(b^{\dagger}-b\right) \\
\end{align}
$$
Substituting back into our Hamiltonian, we get:
$$
\begin{align}
H_{0}
&=-\dfrac{1}{2m}\dfrac{\hbar m\omega}{2}\left(\left(a^{\dagger}-a\right)^2+\left(b^{\dagger}-b\right)^2\right)+\dfrac{m\omega^{2}}{2}\dfrac{\hbar}{2m\omega}\left(\left(a^{\dagger}+a\right)^2+\left(b^{\dagger}+b\right)^2\right)\\
&=\dfrac{\hbar\omega}{2}\left(a^{\dagger}a+aa^{\dagger}+b^{\dagger}b+bb^{\dagger}\right)\\
H_{0}&=\hbar\omega\left(a^{\dagger}a+b^{\dagger}b+1\right)\\
\end{align}
$$
The natural eigenbasis for this system is a number basis:
$$
\begin{align}
H_{0}\ket{n_x,n_y}&=\hbar\omega\left(n_x+n_y+1\right)\ket{n_x,n_y}=E_{n_x,n_y}\ket{n_x,n_y}
\end{align}
$$
The three lowest-lying states are then just the following:
$$
\begin{align}
\ket{0,0} && H_{0}\ket{0,0}&=\hbar\omega\ket{0,0}\\
\ket{1,0} && H_{0}\ket{1,0}&=2\hbar\omega\ket{1,0}\\
\ket{0,1} && H_{0}\ket{0,1}&=2\hbar\omega\ket{0,1}\\
\end{align}
$$
These are just the ground state and the first excited states in each direction. There is a degeneracy on the first-excited states.

---
### Question 5.7.B
We now apply a perturbation:
$$
V=\delta m\omega^2xy
$$
where $\delta$ is a dimensionless real number much smaller than unity. Find the zeroth-order energy eigenket and the corresponding energy to first order (that is, the unperturbed energy obtained in [[#Question 5.7.A]] plus the first-order energy shift) for each of the three lowest-lying states.

We can represent this perturbative potential as creation/annihilation as well:
$$
V=\delta\dfrac{\hbar\omega}{2}\left(a^{\dagger}+a\right)\left(b^{\dagger}+b\right)=\delta\dfrac{\hbar\omega}{2}\left(a^{\dagger}b^{\dagger}+a^{\dagger}b+ab^{\dagger}+ab\right)
$$
For the ground state, we can apply $V$ to see any change in the energy from $\hbar\omega$:
$$
\begin{align}
V\ket{0,0}
&=\delta\dfrac{\hbar\omega}{2}\left(a^{\dagger}b^{\dagger}+a^{\dagger}b+ab^{\dagger}+ab\right)\ket{0,0}\\
V\ket{0,0}&=\delta\dfrac{\hbar\omega}{2}\ket{1,1}\\
\bra{0,0}V\ket{0,0}&=\delta\dfrac{\hbar\omega}{2}\braket{0,0\lvert 1,1}=0\\
(H_0+V)\ket{0,0}&=\hbar\omega
\end{align}
$$
There is no change in the energy of the ground state. The state thus remains the same:
$$
\begin{align}
\ket{0,0} && H\ket{0,0}&=\hbar\omega\ket{0,0}
\end{align}
$$
The issue arises with the first-excited state being initially degenerate. Applying $V$:
$$
\begin{align}
V\ket{1,0}
&=\delta\dfrac{\hbar\omega}{2}\left(a^{\dagger}b^{\dagger}+a^{\dagger}b+ab^{\dagger}+ab\right)\ket{1,0}\\
&=\delta\dfrac{\hbar\omega}{2}\left(\sqrt{2}\ket{2,1}+\ket{0,1}\right)\\
V\ket{0,1}
&=\delta\dfrac{\hbar\omega}{2}\left(a^{\dagger}b^{\dagger}+a^{\dagger}b+ab^{\dagger}+ab\right)\ket{0,1}\\
&=\delta\dfrac{\hbar\omega}{2}\left(\sqrt{2}\ket{1,2}+\ket{1,0}\right)\\
\end{align}
$$
What is clear to see from these is that, ignoring the higher energy states, $V$ has the form:
$$
\begin{align}
V\ket{1,0}&=\delta\dfrac{\hbar\omega}{2}\ket{0,1} & V\ket{0,1}&=\delta\dfrac{\hbar\omega}{2}\ket{1,0}
\end{align}
$$
If we express the potential in the $\ket{1,0},\ket{0,1}$ basis, it takes the form:
$$
V=\delta\dfrac{\hbar\omega}{2}\begin{bmatrix}0&1\\1&0\end{bmatrix}
$$
This is very easy to diagonalize since the matrix is the 2x2 representation of the $x$ Pauli matrix:
$$
\begin{align}
\ket{\pm}&=\dfrac{\ket{1,0}\pm\ket{0,1}}{\sqrt{2}} & E_\pm&=\pm\delta\dfrac{\hbar\omega}{2}
\end{align}
$$
One last thing, since $\ket{1,0},\ket{0,1}$ are degenerate, any linear combination will have same energy:
$$
\begin{align}
\dfrac{\ket{1,0}+\ket{0,1}}{\sqrt{2}} && E_+&=2\hbar\omega+\delta\dfrac{\hbar\omega}{2}\\
\dfrac{\ket{1,0}-\ket{0,1}}{\sqrt{2}} && E_-&=2\hbar\omega-\delta\dfrac{\hbar\omega}{2}\\
\end{align}
$$
This is also a valid basis in the $\delta\to0$ limit due to degeneracy.

---
### Question 5.7.C
Solve the $H_{0}+V$ problem *exactly*. Compare with the perturbation results obtained in [[#Question 5.7.B]].

Start with the total Hamiltonian:
$$
\begin{align}
&&H&=\dfrac{p_{x}^{2}}{2m}+\dfrac{p_{y}^{2}}{2m}+\dfrac{m\omega^{2}}{2}\left(x^{2}+y^{2}\right)+\delta m\omega^2xy\\
\implies&& V&=\dfrac{m\omega^{2}}{2}\left(x^{2}+y^{2}+2\delta xy\right)
\end{align}
$$
This almost looks $(x+y)^2$, so we can use a matrix representation:
$$
\begin{align}
V&=\dfrac{m\omega^{2}}{2}\begin{bmatrix}x&y\end{bmatrix}\begin{bmatrix}x+\delta y\\\delta x+y\end{bmatrix}=\dfrac{m\omega^{2}}{2}\begin{bmatrix}x&y\end{bmatrix}\begin{bmatrix}1&\delta\\\delta&1\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}
\end{align}
$$
We can diagonalize this new matrix, skipping steps but having the form:
$$
\begin{align}
\lambda_\pm&=1\pm\delta & \vec{\lambda}_\pm&=\dfrac{x\pm y}{\sqrt{2}}=x',y'
\end{align}
$$
For the sake of simplicity, we will define the following new position coordinates:
$$
\begin{align}
x'&=\dfrac{x+y}{\sqrt{2}} & y'&=\dfrac{x-y}{\sqrt{2}} &\implies&& x&=\dfrac{x'+y'}{\sqrt{2}} & y&=\dfrac{x'-y'}{\sqrt{2}}
\end{align}
$$
Since this a rotation of the coordinates, $p_x^2+p_y^2$ is preserved into the new coordinates, and so:
$$
\begin{align}
H
&=\dfrac{p_{x'}^{2}}{2m}+\dfrac{p_{y'}^{2}}{2m}+\dfrac{m\omega^{2}}{2}\left(\left(\dfrac{x'+y'}{\sqrt{2}}\right)^{2}+\left(\dfrac{x'-y'}{\sqrt{2}}\right)^{2}\right)+\delta m\omega^2\left(\dfrac{x'+y'}{\sqrt{2}}\right)\left(\dfrac{x'-y'}{\sqrt{2}}\right)\\
&=\dfrac{p_{x'}^{2}}{2m}+\dfrac{p_{y'}^{2}}{2m}+\dfrac{m\omega^{2}}{2}\left(x'^2+y'^2\right)+\dfrac{\delta m\omega^2}{2}\left(x'^2-y'^2\right)\\
&=\dfrac{p_{x'}^{2}}{2m}+\dfrac{p_{y'}^{2}}{2m}+\dfrac{m\omega^{2}}{2}\left(1+\delta\right)x'^2+\dfrac{m\omega^{2}}{2}\left(1-\delta\right)y'^2\\
H&=\dfrac{p_{x'}^{2}}{2m}+\dfrac{p_{y'}^{2}}{2m}+\dfrac{m(\omega\sqrt{1+\delta})^{2}}{2}x'^2+\dfrac{m(\omega\sqrt{1-\delta})^{2}}{2}y'^2\\
\end{align}
$$
Our system is then akin to a 2D uncoupled oscillator with modified frequency:
$$
\begin{align}
H\ket{n_+,n_-}&=\hbar\left[\omega\sqrt{1+\delta}(n_++\tfrac{1}{2})+\omega\sqrt{1-\delta}(n_-+\tfrac{1}{2})\right]
\end{align}
$$
Where $\ket{n_+,n_-}$ is our new parametrization from the aforementioned eigenbasis.

If we do a first-order Taylor expansion of the $\delta$ terms, assuming that $\delta\ll1$, then:
$$
\begin{align}
&&\sqrt{1\pm\delta}&\approx1\pm\dfrac{1}{2}\delta+\mathcal{O}(\delta^2)\\
\implies&&
E_{n_+,n_-}&\approx\hbar\left[\omega\left(1+\dfrac{1}{2}\delta\right)(n_++\tfrac{1}{2})+\omega\left(1-\dfrac{1}{2}\delta\right)(n_-+\tfrac{1}{2})\right]\\
&&&=\hbar\omega\left[(n_++\tfrac{1}{2})+(n_-+\tfrac{1}{2})\right]+\delta\dfrac{\hbar\omega}{2}\left[(n_++\tfrac{1}{2})-(n_-+\tfrac{1}{2})\right]\\
&&&=\hbar\omega\left[n_++n_- +1)\right]+\delta\dfrac{\hbar\omega}{2}\left[n_+-n_-\right]
\end{align}
$$
Compared to [[#Question 5.7.B]], if we evaluate at for 
$$
\begin{align}
\ket{\pm}&=\dfrac{\ket{1,0}\pm\ket{0,1}}{\sqrt{2}} & E_\pm&=\pm\delta\dfrac{\hbar\omega}{2}
\end{align}
$$
This is exactly the same answer, which can be shown as:
$$
\begin{align}
\ket{+}&=\ket{1,0}_\pm & E_{1,0}&=2\hbar\omega+(+1)\delta\dfrac{\hbar\omega}{2}\\
\ket{-}&=\ket{0,1}_\pm & E_{0,1}&=2\hbar\omega+(-1)\delta\dfrac{\hbar\omega}{2}\\
\end{align}
$$
Thus the exact solution and first-order perturbative solutions match in the first order for small $\delta$.

---
## Question 5.12
A p-orbital electron characterized by $\ket{n,l=1,m=\{0,\pm1\}}$ is subjected to a potential:
$$
V=\lambda(x^2-y^2)
$$
Heeding the hint, the Wigner-Eckart theorem is:
$$
\bra{jm}T_q^{(k)}\ket{j'm'}=\braket{j'm'kq\lvert jm}\dfrac{\bra{j}\left\lVert T^{k}\right\rVert\ket{j'}}{\sqrt{2j+1}}
$$
The associated spherical tensors we might need are as follows:
$$
\begin{align}
T^{(2)}_{0}&=\dfrac{1}{\sqrt{6}}(2z^2-x^2-y^2) & T^{(2)}_{\pm1}&=\mp\dfrac{1}{2}\left[(x\pm iy)z+z(x\pm iy)\right] & T^{(2)}_{\pm2}&=\dfrac{1}{2}(x\pm iy)^2
\end{align}
$$
---
### Question 5.12.A
Obtain the "correct" zeroth-order energy eigenstates that diagonalize the perturbation. You need not evaluate the energy shifts in detail, but show that the original threefold degeneracy is now completely removed.

We can express the potential in terms of spherical tensors:
$$
\begin{align}
V&=AT^{(2)}_{+2}+BT^{(2)}_{-2}\\
&=A\dfrac{1}{2}(x+iy)^2+B\dfrac{1}{2}(x-iy)^2\\
\lambda(x^2-y^2)&=\dfrac{A+B}{2}x^2+i(A-B)xy-\dfrac{A+B}{2}y^2\\
\end{align}
$$
For it to take the right form, $A=\lambda$ and $B=\lambda$, and so:
$$
\begin{align}
\lambda(x^2-y^2)&=\lambda x^2+0-\lambda y^2\\
\Aboxed{V&=\lambda T^{(2)}_{+2}+\lambda T^{(2)}_{-2}}
\end{align}
$$
For the $l=1$ electron, $j=1$ and $m\in\left\{0,\pm1\right\}$, the Wigner-Eckart theorem turns into:
$$
\bra{1m}T_q^{(2)}\ket{1m'}=\braket{1m'2q\lvert 1m}\dfrac{\bra{1}\left\lVert T^{2}\right\rVert\ket{1}}{\sqrt{3}}
$$
The selection rule that comes out of this is $m-m'=q\implies\boxed{m=m'+q}$:
$$
\begin{align}
(m&=m'+2) & \bra{1,+1}T_{+2}^{(2)}\ket{1,-1}&=\braket{1,-1,2,+2\lvert 1,+1}\dfrac{\bra{1}\left\lVert T^{2}\right\rVert\ket{1}}{\sqrt{3}}\\
(m&=m'-2) & \bra{1,-1}T_{-2}^{(2)}\ket{1,+1}&=\braket{1,+1,2,-2\lvert 1,-1}\dfrac{\bra{1}\left\lVert T^{2}\right\rVert\ket{1}}{\sqrt{3}}\\
\end{align}
$$
Looking at a Clebsch-Gordon table, we find that the non-zero elements are:
$$
\begin{align}
\bra{1,+1}T_{+2}^{(2)}\ket{1,-1}&=\dfrac{\bra{1}\left\lVert T^{2}\right\rVert\ket{1}}{\sqrt{30}} & \bra{1,-1}T_{-2}^{(2)}\ket{1,+1}&=\dfrac{\bra{1}\left\lVert T^{2}\right\rVert\ket{1}}{\sqrt{30}}\\
\end{align}
$$
Therefore, the potential written in the $l=1$ state basis is then:
$$
\begin{align}
V&=\lambda\dfrac{\bra{1}\left\lVert T^{2}\right\rVert\ket{1}}{\sqrt{30}}\left[\ket{1,+1}\bra{1,-1}+\ket{1,-1}\bra{1,+1}\right]
\end{align}
$$
The potential swaps the $m\pm1$ states, and leaves $m=0$ untouched. In this degenerate subspace of state vectors $\ket{1,\pm1}$, the potential is identical to $\sigma_x$, and thus has the eigenvector decomposition:
$$
\begin{align}
\ket{1,\text{sym}}&=\dfrac{\ket{1,+1}+\ket{1,-1}}{\sqrt{2}} & \ket{1,\text{asym}}&=\dfrac{\ket{1,+1}-\ket{1,-1}}{\sqrt{2}}
\end{align}
$$
These states have new eigenvalues for energy to be the following:
$$
\begin{align}
E^\text{sym}&=E_0+\lambda\dfrac{\bra{1}\left\lVert T^{2}\right\rVert\ket{1}}{\sqrt{30}} & 
E^\text{asym}&=E_0-\lambda\dfrac{\bra{1}\left\lVert T^{2}\right\rVert\ket{1}}{\sqrt{30}}\\
\end{align}
$$
The $m=0$ state remains $E_0$, and thus all 3 states are now non-degenerate under this potential.

---
### Question 5.12.B
Because $V$ is invariant under time reversal and because there is no longer any degeneracy, we expect each of the energy eigenstates obtained in [[#Question 5.12.A]] to go into itself (up to a phase factor or sign) under time reversal. Check this point explicitly.

Recall that time-reversal applied to an angular state vector has the following operation effect:
$$
\begin{align}
\Theta\ket{l,m}&=(-1)^{l-m}\ket{l,-m} &\implies&& \Theta\ket{1,\pm1}&=\ket{1,\mp1} &\land&& \Theta\ket{1,0}&=-\ket{1,0}
\end{align}
$$
Applying time-reversal to our 3 states, we get:
$$
\begin{align}
\Theta\ket{1,\text{sym}}&=\dfrac{\ket{1,-1}+\ket{1,+1}}{\sqrt{2}}=\ket{1,\text{sym}}\\
\Theta\ket{1,\text{asym}}&=\dfrac{\ket{1,-1}-\ket{1,+1}}{\sqrt{2}}=-\ket{1,\text{asym}}\\
\Theta\ket{1,0}&=-\ket{1,0}
\end{align}
$$
All 3 states are identical to themselves up to a phase, Q.E.D.

---
## Question 5.13
Consider a spinless particle in a two-dimensional infinite square well:
$$
V=\begin{cases}
0,&0\le x\le a,\ 0\le y\le a \\
\infty,&\text{otherwise}
\end{cases}
$$
### Question 5.13.A
What are the energy eigenvalues for the three lowest states? Is there any degeneracy?

Our unperturbed Hamiltonian within the box can be written as:
$$\begin{align}
H_0&=-\dfrac{\hbar^2}{2m}\vec{\nabla}^2=-\dfrac{\hbar^2}{2m}\left(\dfrac{\partial^2}{\partial x^2}+\dfrac{\partial^2}{\partial y^2}\right)
\end{align}$$
Supposing our wavefunction is an eigenstate of $H_0$, let $\ket{\psi_{nm}}$ satisfy:
$$\begin{align}
-\dfrac{\hbar^2}{2m}\left(\dfrac{\partial^2}{\partial x^2}+\dfrac{\partial^2}{\partial y^2}\right)\ket{\psi_{nm}}&=E_{nm}\ket{\psi_{nm}}
&\implies&&
\left(\dfrac{\partial^2}{\partial x^2}+\dfrac{\partial^2}{\partial y^2}\right)\ket{\psi_{nm}}&=-\dfrac{2mE_{nm}}{\hbar^2}\ket{\psi_{nm}}
\end{align}$$
To allow the wavefunction to be $0$ at the boundary, let:
$$\begin{align}
\ket{\psi_{nm}}&=\sqrt{\dfrac{2}{a}}\sin\left(\dfrac{n\pi x}{a}\right)\cdot\sqrt{\dfrac{2}{a}}\sin\left(\dfrac{m\pi y}{a}\right)
\end{align}$$
Substituting back into our energy equation, we get:
$$\begin{align}
-\left(\dfrac{n\pi}{a}\right)^2-\left(\dfrac{m\pi}{a}\right)^2&=-\dfrac{2mE_{nm}}{\hbar^2} &\implies&& \Aboxed{E_{nm}&=\dfrac{h^2}{8ma^2}\left(n^2+m^2\right)}
\end{align}$$
The first 3 lowest energy eigenvalue are as follows:
$$\begin{align}
\Aboxed{E_{11}&=\dfrac{2h^2}{8ma^2}}&\Aboxed{E_{12}=E_{21}&=\dfrac{5h^2}{8ma^2}}
\end{align}$$
The ground state is unique, but there are 2 first-excited states (degenerate).

---
### Question 5.13.B
We now add a potential:
$$
V_{1}=\lambda xy,\ 0\le x\le a,\ 0\le y\le a
$$
Taking this as a weak perturbation, answer the following.
#### Question 5.13.B.I
Is the energy shift due to the perturbation linear or quadratic in $\lambda$ for each of the three states?

We can use the equation for the first order energy shift as:
$$
\Delta_{nm}^{(1)}=\bra{\psi_{nm}^{(0)}}V_1\ket{\psi_{nm}^{(0)}}
$$
The energy shift is linear with $\lambda$, as more explicitly shown in [[#Question 5.13.B.II]].

---
#### Question 5.13.B.II
Obtain expressions for the energy shifts of the three lowest states accurate to order $\lambda$.

Substituting our expression for $V_1$ and our unperturbed wavefunctions into the correction, we get:
$$
\begin{align}
\Delta_{nm}^{(1)}
&=\int_{0}^a\int_{0}^a\dfrac{2}{a}\sin\left(\dfrac{n\pi x}{a}\right)\sin\left(\dfrac{m\pi y}{a}\right)\cdot\lambda xy\cdot\dfrac{2}{a}\sin\left(\dfrac{n\pi x}{a}\right)\sin\left(\dfrac{m\pi y}{a}\right)\ dx\ dy\\
&=\dfrac{4\lambda}{a^2}\int_{0}^ax\sin^2\left(\dfrac{n\pi x}{a}\right)\ dx\int_{0}^ay\sin^2\left(\dfrac{m\pi y}{a}\right)\ dy\\
&=\dfrac{4\lambda}{a^2}\left(\dfrac{a^2}{4}\right)\left(\dfrac{a^2}{4}\right)\\
\Aboxed{\Delta_{nm}^{(1)}&=\dfrac{\lambda a^2}{4}}
\end{align}
$$
It is agnostic to our quantum state parameter, interestingly. 

---
#### Question 5.13.B.III
Draw an energy diagram with and without the perturbation for the three energy states. Make sure to specify which unperturbed state is connected to which perturbed state.

The structure of the perturbed state diagram is identical to the unperturbed state diagram, except that it is shifted up by energy addition energy $+\tfrac{\lambda a^2}{4}$:
![[5.13.B.III.png]]
The degeneracy of the first excited states is preserved in the 1st order correction.

---
## Question 5.15
A system that has three unperturbed states can be represented by the perturbed Hamiltonian matrix:
$$
\begin{bmatrix}
E_{1}&0&a \\
0&E_{1}&b \\
a^*&b^*&E_{2}
\end{bmatrix}
$$
where $E_{2}>E_{1}$. The quantities $a$ and $b$ are to be regarded as perturbations that are of the same order and are small compared with $E_{2}-E_{1}$.

For my usage, we can split this matrix into 2 components:
$$
\begin{align}
H_0&=\begin{bmatrix}
E_{1}&0&0 \\
0&E_{1}&0 \\
0&0&E_{2}
\end{bmatrix} &
V&=\begin{bmatrix}
0&0&a \\
0&0&b \\
a^*&b^*&0
\end{bmatrix}
\end{align}
$$
---
### Question 5.15.A
Use the second-order nondegenerate perturbation theory to calculate the perturbed eigenvalues. (Is this procedure correct?)

The second-order nondegenerate energy is the following:
$$
\begin{align}
E_n^{(2)}&=\sum_{m\ne n}\dfrac{|V_{mn}|^2}{E_n-E_m}
\end{align}
$$
From the potential matrix, we can find each energy component as:
$$
\begin{align}
E_1^{(2)}&=\dfrac{|a^*|^2}{E_1-E_2} & E_2^{(2)}&=\dfrac{|b^*|^2}{E_1-E_2} & E_3^{(2)}&=\dfrac{|a|^2}{E_2-E_1}+\dfrac{|b|^2}{E_2-E_1}\\
\end{align}
$$
Our corrected energies are then the following:
$$
\begin{align}
\Aboxed{E_{n=1}&=E_1-\dfrac{|a|^2}{E_2-E_1}} & \Aboxed{E_{n=2}&=E_1-\dfrac{|b|^2}{E_2-E_1}} & \Aboxed{E_{n=3}&=E_2+\dfrac{|a|^2+|b|^2}{E_2-E_1}}
\end{align}
$$
---
### Question 5.15.B
Diagonalize the matrix to find the exact eigenvalues. 

I had originally done this by hand, but was able to simplify it since one eigenvalue is $\lambda=E_1$.

For the matrix:
$$
\begin{bmatrix}
E_{1}&0&a \\
0&E_{1}&b \\
a^*&b^*&E_{2}
\end{bmatrix}
$$
The eigenvalues are:
$$
\begin{align}
\Aboxed{\lambda_{0}&=E_1} & \Aboxed{\lambda_{\pm}&=\dfrac{E_2+E_1}{2}\pm\sqrt{\dfrac{(E_2-E_1)^2}{4}+|a|^2+|b|^2}}
\end{align}
$$
While I could show all the work, I deleted the LaTeX because it was like 3 pages.

If we want to Taylor expand around a small quantity, we can notice that:
$$
\begin{align}
\lambda_{\pm}&\sim y\pm x\sqrt{1+\dfrac{\epsilon}{x^2}}\approx y\pm x\left(1+\dfrac{1}{2}\dfrac{\epsilon}{x^2}\right)
\end{align}
$$
We then have two approximate solutions:
$$
\begin{align}
\lambda_{+}&\approx y+x+\dfrac{1}{2}\dfrac{\epsilon}{x} & \lambda_{-}&\approx y-x-\dfrac{1}{2}\dfrac{\epsilon}{x}\\
\end{align}
$$
Substituting our values back in, we see that:
$$\begin{align}
\Aboxed{E_{n=1}&=E_1} & \Aboxed{E_{n=2}&\approx E_1-\dfrac{|a|^2+|b|^2}{E_2-E_1}} & \Aboxed{\lambda_{3}&\approx E_{n=3}+\dfrac{|a|^2+|b|^2}{E_2-E_1}} 
\end{align}$$
---
### Question 5.15.C
Finally, use the second-order degenerate perturbation theory. 
$$\begin{align}
\bra{i}H_\text{D}^{(2)}\ket{j}&=\sum_{k\not\in D}\dfrac{\bra{i}V\ket{k}\bra{k}V\ket{j}}{E_1-E_k}
\end{align}$$
States $\ket{1}$ and $\ket{2}$ are part of the degenerate subspace, so the only $\ket{k}$ is $\ket{3}$:
$$\begin{align}
\bra{i}H_\text{D}^{(2)}\ket{j}&=-\dfrac{\bra{i}V\ket{3}\bra{3}V\ket{j}}{E_2-E_1}
\end{align}$$
For the 4 elements of this Hamiltonian in this degenerate subspace, we get:
$$\begin{align}
\bra{1}H_\text{D}^{(2)}\ket{1}&=-\dfrac{|a|^2}{E_2-E_1} & \bra{1}H_\text{D}^{(2)}\ket{2}&=-\dfrac{ab^*}{E_2-E_1} \\
\bra{2}H_\text{D}^{(2)}\ket{1}&=-\dfrac{a^*b}{E_2-E_1} & \bra{i}H_\text{D}^{(2)}\ket{j}&=-\dfrac{|b|^2}{E_2-E_1}
\end{align}$$
Therefore the Hamiltonian in matrix form is:
$$\begin{align}
H_\text{D}^{(2)}&=-\dfrac{1}{E_2-E_1}\begin{bmatrix}|a|^2&ab^*\\ba^*&|b|^2\end{bmatrix}
\end{align}$$
We can diagonalize the matrix pretty simply:
$$\begin{align}
0&=-\dfrac{1}{E_2-E_1}\left[(\lambda-|a|^2)(\lambda-|b|^2)-ab^*ba^*\right]\\
&=\lambda^2-(|a|^2+|b|^2)\lambda+|a|^2|b|^2-|a|^2|b|^2\\
0&=\lambda\left(\lambda-(|a|^2+|b|^2)\right)\\
\end{align}$$
The two eigenvalues we get are:
$$\begin{align}\lambda&=0 & \lambda&=-\dfrac{|a|^2+|b|^2}{E_2-E_1}\end{align}$$
Thus the two energies in the degenerate subspace are:
$$\begin{align}E_{n=1}&=E_1 & E_{n=3}&=E_1-\dfrac{|a|^2+|b|^2}{E_2-E_1}\end{align}$$
The third energy is the same as that found in nondegenerate perturbations theory:
$$\begin{align}E_{n=3}&=E_2+\dfrac{|a|^2+|b|^2}{E_2-E_1}\end{align}$$
---
### Question 5.15.D
Compare the three results obtained.

From [[#Question 5.15.A]]:
$$\begin{align}
\Aboxed{E_{n=1}&=E_1-\dfrac{|a|^2}{E_2-E_1}} & \Aboxed{E_{n=2}&=E_1-\dfrac{|b|^2}{E_2-E_1}} & \Aboxed{E_{n=3}&=E_2+\dfrac{|a|^2+|b|^2}{E_2-E_1}}
\end{align}$$
From [[#Question 5.15.B]]:
$$\begin{align}
\Aboxed{E_{n=1}&=E_1} & \Aboxed{E_{n=2}&\approx E_1-\dfrac{|a|^2+|b|^2}{E_2-E_1}} & \Aboxed{E_{n=3}&\approx E_2+\dfrac{|a|^2+|b|^2}{E_2-E_1}} 
\end{align}$$
From [[#Question 5.15.C]]:
$$\begin{align}
\Aboxed{E_{n=1}&=E_1} & \Aboxed{E_{n=2}&=E_1-\dfrac{|a|^2+|b|^2}{E_2-E_1}} & \Aboxed{E_{n=3}&=E_2+\dfrac{|a|^2+|b|^2}{E_2-E_1}} 
\end{align}$$
From what I can see, part A is different from part B, even though there is no potential correlation between the degenerate ground states. Thus, any degenerate subspace has to use degenerate perturbation, even if the coupling potential is not directly correlative on first order.

While $\ket{1}$ and $\ket{2}$ don't coupling in first-order, they do couple with $\ket{3}$, so with 2nd order they do coupling since they relate through $\ket{3}$.