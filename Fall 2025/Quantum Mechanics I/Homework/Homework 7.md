Author: Stanley Goodwin
Date: November 13th, 2025

---
## Question 3.5
The spin-dependent Hamiltonian of an electron-positron system in the presence of a uniform magnetic field in the $z$-direction can be written as:
$$\begin{align}
H&=A\vec{S}^{(e^-)}\vec{S}^{(e^+)}+\left(\dfrac{eB}{mc}\right)\left(S^{(e^-)}_z-S^{(e^+)}_z\right)
\end{align}$$
Suppose the spin function of the system is given by $\chi^{(e^-)}_+\chi^{(e^+)}_-$.

Component by component:
$$\begin{align}
A\vec{S}^{(e^-)}\cdot\vec{S}^{(e^+)}\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}
&=A\left(S^{(e^-)}_zS^{(e^+)}_z+\dfrac{1}{2}S^{(e^-)}_+S^{(e^+)}_-+\dfrac{1}{2}S^{(e^-)}_-S^{(e^+)}_+\right)\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}\\\\
&=AS^{(e^-)}_zS^{(e^+)}_z\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}+\dfrac{A}{2}S^{(e^-)}_+S^{(e^+)}_-\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}\\
&+\dfrac{A}{2}S^{(e^-)}_-S^{(e^+)}_+\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}\\\\
&=A\dfrac{\hbar}{2}\left(-\dfrac{\hbar}{2}\right)\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}+\dfrac{A}{2}0\cdot0\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}+\dfrac{A}{2}\hbar^2\ket{\chi^{(e^-)}_-}\ket{\chi^{(e^+)}_+}\\
\Aboxed{A\vec{S}^{(e^-)}\cdot\vec{S}^{(e^+)}\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}
&=-A\dfrac{\hbar^2}{4}\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}+A\dfrac{\hbar^2}{2}\ket{\chi^{(e^-)}_-}\ket{\chi^{(e^+)}_+}}
\end{align}$$
$$\begin{align}
H\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}&=\left(\dfrac{eB}{mc}\right)\left(S^{(e^-)}_z-S^{(e^+)}_z\right)\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}\\
&=\left(\dfrac{eB}{mc}\right)S^{(e^-)}_z\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}-\left(\dfrac{eB}{mc}\right)\ket{\chi^{(e^-)}_+}S^{(e^+)}_z\ket{\chi^{(e^+)}_-}\\\\
&=\left(\dfrac{eB}{mc}\right)\dfrac{\hbar}{2}\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}-\left(\dfrac{eB}{mc}\right)\ket{\chi^{(e^-)}_+}\left(-\dfrac{\hbar}{2}\right)\ket{\chi^{(e^+)}_-}\\\\
&=2\left(\dfrac{eB}{mc}\right)\dfrac{\hbar}{2}\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}\\
\Aboxed{H\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}&=\dfrac{eB\hbar}{mc}\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}}
\end{align}$$
And so we find:
$$\begin{align}
\Aboxed{H\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}&=\left(\dfrac{eB\hbar}{mc}-A\dfrac{\hbar^2}{4}\right)\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}+A\dfrac{\hbar^2}{2}\ket{\chi^{(e^-)}_-}\ket{\chi^{(e^+)}_+}}
\end{align}$$
### Question 3.5.A
Is this an eigenfunction of $H$ in the limit $A\rightarrow0$, $eB/mc\ne0$? If it is, what is the energy eigenvalue? If it is not, what is the expectation value of $H$?
$$\begin{align}
\Aboxed{\lim_{A\rightarrow0}H\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}&=\dfrac{eB\hbar}{mc}\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}}
\end{align}$$
The energy eigenvalue is then:
$$\begin{align}
\Aboxed{\lim_{A\rightarrow0}E&=\dfrac{eB\hbar}{mc}}
\end{align}$$
### Question 3.5.B
Same problem when $eB/mc\rightarrow0$, $A\ne0$.
$$\begin{align}
\Aboxed{\lim_{eB/mc\rightarrow0}H\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}&=-A\dfrac{\hbar^2}{4}\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}+A\dfrac{\hbar^2}{2}\ket{\chi^{(e^-)}_-}\ket{\chi^{(e^+)}_+}}
\end{align}$$
This is not an energy eigenstate, but we can calculate the expected value of energy:
$$\begin{align}
\lim_{eB/mc\rightarrow0}E\braket{E}&=\bra{\chi^{(e^+)}_-}\bra{\chi^{(e^-)}_+}\hat{H}\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}\\
&=\bra{\chi^{(e^+)}_-}\bra{\chi^{(e^-)}_+}\left(-A\dfrac{\hbar^2}{4}\right)\ket{\chi^{(e^-)}_+}\ket{\chi^{(e^+)}_-}+\bra{\chi^{(e^+)}_-}\bra{\chi^{(e^-)}_+}\left(A\dfrac{\hbar^2}{2}\right)\ket{\chi^{(e^-)}_-}\ket{\chi^{(e^+)}_+}\\
&=-A\dfrac{\hbar^2}{4}+0\\
\Aboxed{\lim_{eB/mc\rightarrow0}E\braket{E}&=-A\dfrac{\hbar^2}{4}}
\end{align}$$
---
## Question 3.10
Consider a sequence of Euler rotations represented by:
$$\begin{align}
\mathcal{D}^{(1/2)}(\alpha,\beta,\gamma)&=e^{-i\sigma_3\alpha/2}e^{-i\sigma_2\beta/2}e^{-i\sigma_3\gamma/2}
\end{align}$$
Because of the group properties of rotations, we expect that this sequence of operations is equivalent to a single rotation about some axis by an angle $\theta$. Find $\theta$.

Something of note, we can use:
$$\begin{align}
e^{-i\sigma_a\alpha/2}&=\mathbb{I}\cos\left(\dfrac{\alpha}{2}\right)-i\sigma_a\sin\left(\dfrac{\alpha}{2}\right)
\end{align}$$
So we get the following matrices:
$$\begin{align}
e^{-i\sigma_3\alpha/2}&=\begin{bmatrix}
\cos\left(\tfrac{\alpha}{2}\right)-i\sin\left(\tfrac{\alpha}{2}\right) & 0\\
0&\cos\left(\tfrac{\alpha}{2}\right)+i\sin\left(\tfrac{\alpha}{2}\right)
\end{bmatrix}=
\begin{bmatrix}
e^{-i\alpha/2} & 0\\
0&e^{+i\alpha/2}
\end{bmatrix}\\

e^{-i\sigma_2\beta/2}&=\begin{bmatrix}
\cos\left(\tfrac{\beta}{2}\right)&-i(-i)\sin\left(\tfrac{\beta}{2}\right)\\
i(-i)\sin\left(\tfrac{\beta}{2}\right)&\cos\left(\tfrac{\beta}{2}\right)
\end{bmatrix}=\begin{bmatrix}
\cos\left(\tfrac{\beta}{2}\right)&-\sin\left(\tfrac{\beta}{2}\right)\\
\sin\left(\tfrac{\beta}{2}\right)&\cos\left(\tfrac{\beta}{2}\right)
\end{bmatrix}\\

e^{-i\sigma_3\gamma/2}&=\begin{bmatrix}
\cos\left(\tfrac{\gamma}{2}\right)-i\sin\left(\tfrac{\gamma}{2}\right) & 0\\
0&\cos\left(\tfrac{\gamma}{2}\right)+i\sin\left(\tfrac{\gamma}{2}\right)
\end{bmatrix}=
\begin{bmatrix}
e^{-i\gamma/2} & 0\\
0&e^{+i\gamma/2}
\end{bmatrix}\\
\end{align}$$
The product of these 3 are:
$$\begin{align}
\mathcal{D}^{(1/2)}(\alpha,\beta,\gamma)&=e^{-i\sigma_3\alpha/2}e^{-i\sigma_2\beta/2}e^{-i\sigma_3\gamma/2}\\
&=\begin{bmatrix}e^{-i\alpha/2} & 0\\0&e^{+i\alpha/2}\end{bmatrix}
\begin{bmatrix}
\cos\left(\tfrac{\beta}{2}\right)&-\sin\left(\tfrac{\beta}{2}\right)\\
\sin\left(\tfrac{\beta}{2}\right)&\cos\left(\tfrac{\beta}{2}\right)
\end{bmatrix}
\begin{bmatrix}e^{-i\gamma/2}&0\\0&e^{+i\gamma/2}\end{bmatrix}\\
&=\begin{bmatrix}e^{-i\alpha/2} & 0\\0&e^{+i\alpha/2}\end{bmatrix}
\begin{bmatrix}
e^{-i\gamma/2}\cos\left(\tfrac{\beta}{2}\right)&-e^{+i\gamma/2}\sin\left(\tfrac{\beta}{2}\right)\\
e^{-i\gamma/2}\sin\left(\tfrac{\beta}{2}\right)&e^{+i\gamma/2}\cos\left(\tfrac{\beta}{2}\right)
\end{bmatrix}\\
&=\begin{bmatrix}
e^{-i\alpha/2}e^{-i\gamma/2}\cos\left(\tfrac{\beta}{2}\right)&-e^{-i\alpha/2}e^{+i\gamma/2}\sin\left(\tfrac{\beta}{2}\right)\\
e^{+i\alpha/2}e^{-i\gamma/2}\sin\left(\tfrac{\beta}{2}\right)&e^{+i\gamma/2}e^{+i\alpha/2}\cos\left(\tfrac{\beta}{2}\right)
\end{bmatrix}\\
\end{align}$$
Alternatively we express the transform matrix in terms of the axial form:
$$\begin{align}
\mathcal{D}^{(1/2)}(\theta)&=e^{-i(\vec\sigma\cdot\hat{n})\theta/2}\\
&=\mathbb{I}\cos\left(\dfrac{\theta}{2}\right)-i\vec{\sigma}\cdot\hat{n}\sin\left(\dfrac{\theta}{2}\right)\\
&=\mathbb{I}\cos\left(\dfrac{\theta}{2}\right)-i\sigma_xn_x\sin\left(\dfrac{\theta}{2}\right)-i\sigma_yn_y\sin\left(\dfrac{\theta}{2}\right)-i\sigma_zn_z\sin\left(\dfrac{\theta}{2}\right)\\\\
&=\begin{bmatrix}\cos\left(\tfrac{\theta}{2}\right)&0\\0&\cos\left(\tfrac{\theta}{2}\right)\end{bmatrix}-i\begin{bmatrix}0&n_x\sin\left(\tfrac{\theta}{2}\right)\\n_x\sin\left(\tfrac{\theta}{2}\right)&0\end{bmatrix}\\&-i\begin{bmatrix}0&-in_y\sin\left(\tfrac{\theta}{2}\right)\\in_y\sin\left(\tfrac{\theta}{2}\right)&0\end{bmatrix}-i\begin{bmatrix}n_z\sin\left(\tfrac{\theta}{2}\right)&0\\0&-n_z\sin\left(\tfrac{\theta}{2}\right)\end{bmatrix}\\\\

\mathcal{D}^{(1/2)}(\theta)&=\begin{bmatrix}\cos\left(\tfrac{\theta}{2}\right)-in_z\sin\left(\tfrac{\theta}{2}\right)&-in_x\sin\left(\tfrac{\theta}{2}-n_y\sin\left(\tfrac{\theta}{2}\right)\right)\\-in_x\sin\left(\tfrac{\theta}{2}\right)+n_y\sin\left(\tfrac{\theta}{2}\right)&\cos\left(\tfrac{\theta}{2}\right)+in_z\sin\left(\tfrac{\theta}{2}\right)\end{bmatrix}
\end{align}$$
The diagonals look nice to substitute, so:
$$\begin{align}
e^{-i\alpha/2}e^{-i\gamma/2}\cos\left(\tfrac{\beta}{2}\right)&=\cos\left(\tfrac{\theta}{2}\right)-in_z\sin\left(\tfrac{\theta}{2}\right)\\
e^{+i\gamma/2}e^{+i\alpha/2}\cos\left(\tfrac{\beta}{2}\right)&=\cos\left(\tfrac{\theta}{2}\right)+in_z\sin\left(\tfrac{\theta}{2}\right)\\
\end{align}$$
Adding the two equations together, we get:
$$\begin{align}
\cos\left(\tfrac{\theta}{2}\right)-in_z\sin\left(\tfrac{\theta}{2}\right)+\cos\left(\tfrac{\theta}{2}\right)+in_z\sin\left(\tfrac{\theta}{2}\right)&=e^{-i\alpha/2}e^{-i\gamma/2}\cos\left(\tfrac{\beta}{2}\right)+e^{+i\gamma/2}e^{+i\alpha/2}\cos\left(\tfrac{\beta}{2}\right)\\
2\cos\left(\tfrac{\theta}{2}\right)&=2\dfrac{e^{+i(\alpha+\gamma)/2}+e^{-i(\alpha+\gamma)/2}}{2}\cos\left(\tfrac{\beta}{2}\right)\\
2\cos\left(\tfrac{\theta}{2}\right)&=2\cos\left(\tfrac{\alpha+\gamma}{2}\right)\cos\left(\tfrac{\beta}{2}\right)\\
\cos\left(\tfrac{\theta}{2}\right)&=\cos\left(\tfrac{\alpha+\gamma}{2}\right)\cos\left(\tfrac{\beta}{2}\right)\\
\Aboxed{\theta&=2\cos^{-1}\left[\cos\left(\tfrac{\alpha+\gamma}{2}\right)\cos\left(\tfrac{\beta}{2}\right)\right]}
\end{align}$$
---
## Question 3.12
A large collection of spin $1/2$ particles is in a mixture of the two states $\ket{S_z;+}$ and $\ket{S_y;-}$. The fraction of particles in the state $\ket{S_z;+}$ is $a$. Find the ensemble averages $[S_x]$, $[S_y]$, and $[S_z]$ in terms of $a$. Confirm that your expression gives the answers you expect for $a = 0$ and $a = 1$.

Lets write the state in the following form:
$$\begin{align}
\braket{S_x}&=a\bra{S_z;+}S_x\ket{S_z;+}+(1-a)\bra{S_y;-}S_x\ket{S_y;-}\\
&=a\cdot0+(1-a)\cdot0\\
\Aboxed{\braket{S_x}&=0}
\end{align}$$
$$\begin{align}
\braket{S_y}&=a\bra{S_z;+}S_y\ket{S_z;+}+(1-a)\bra{S_y;-}S_y\ket{S_y;-}\\
&=a\cdot0-(1-a)\cdot\dfrac{\hbar}{2}\\
\Aboxed{\braket{S_y}&=(a-1)\cdot\dfrac{\hbar}{2}}
\end{align}$$
$$\begin{align}
\braket{S_z}&=a\bra{S_z;+}S_z\ket{S_z;+}+(1-a)\bra{S_y;-}S_z\ket{S_y;-}\\
&=a\cdot\dfrac{\hbar}{2}+(1-a)\cdot0\\
\Aboxed{\braket{S_z}&=a\cdot\dfrac{\hbar}{2}}
\end{align}$$
We can show this over the two different systems given:

| a   | $\braket{S_x}$ | $\braket{S_y}$      | $\braket{S_z}$      |
| --- | -------------- | ------------------- | ------------------- |
| $0$ | $0$            | $-\dfrac{\hbar}{2}$ | $0$                 |
| $1$ | $0$            | $0$                 | $+\dfrac{\hbar}{2}$ |

---
## Question 3.14
Consider a one-dimensional simple harmonic oscillator with frequency $\omega$ and eigenstates $\ket0$, $\ket1$, $\ket2$, $\dots$ A mixed ensemble is formed with equal parts of each of the three states:
$$\begin{align}
\ket\alpha&\equiv\dfrac{1}{\sqrt2}\left(\ket0+\ket1\right) & \ket\beta&\equiv\dfrac{1}{\sqrt2}\left(\ket1+\ket2\right) & \ket\gamma&\equiv\ket2
\end{align}$$
Find the density operator $\rho$ and calculate the ensemble average of energy.

Start with the definition of the density operator of equal parts:
$$\begin{align}
\rho&=\dfrac{1}{3}\ket{\alpha}\bra{\alpha}+\dfrac{1}{3}\ket{\beta}\bra{\beta}+\dfrac{1}{3}\ket{\gamma}\bra{\gamma}\\
\end{align}$$
The inner products are as follows:
$$\begin{align}
\ket\alpha\bra\alpha&=\dfrac{1}{\sqrt2}\left(\ket0+\ket1\right)\cdot\dfrac{1}{\sqrt2}\left(\bra0+\bra1\right)\\
&=\dfrac{1}{2}\left(\ket0\bra0+\ket0\bra1+\ket1\bra0+\ket1\bra1\right)\\
\Aboxed{\ket\alpha\bra\alpha&=\dfrac{1}{2}\ket0\bra0+\dfrac{1}{2}\ket0\bra1+\dfrac{1}{2}\ket1\bra0+\dfrac{1}{2}\ket1\bra1}\\
\ket\beta\bra\beta&=\dfrac{1}{\sqrt2}\left(\ket1+\ket2\right)\cdot\dfrac{1}{\sqrt2}\left(\bra1+\bra2\right)\\
&=\dfrac{1}{2}\left(\ket1\bra1+\ket1\bra2+\ket2\bra1+\ket2\bra2\right)\\
\Aboxed{\ket\alpha\bra\alpha&=\dfrac{1}{2}\ket1\bra1+\dfrac{1}{2}\ket1\bra2+\dfrac{1}{2}\ket2\bra1+\dfrac{1}{2}\ket2\bra2}\\\\
\Aboxed{\ket\gamma\bra\gamma&=\ket2\bra2}
\end{align}$$
The total density operator is then:
$$\begin{align}
\rho&=\dfrac{1}{3}\ket{\alpha}\bra{\alpha}+\dfrac{1}{3}\ket{\beta}\bra{\beta}+\dfrac{1}{3}\ket{\gamma}\bra{\gamma}\\
&=\dfrac{1}{3}\dfrac{1}{2}\left(\ket0\bra0+\ket0\bra1+\ket1\bra0+\ket1\bra1+\ket1\bra1+\ket1\bra2+\ket2\bra1+\ket2\bra2+2\ket2\bra2\right)\\
&=\dfrac{1}{6}\left(\ket0\bra0+\ket0\bra1+\ket1\bra0+2\ket1\bra1+\ket1\bra2+\ket2\bra1+3\ket2\bra2\right)\\
\Aboxed{\rho&=\dfrac{1}{6}\ket0\bra0+\dfrac{1}{6}\ket0\bra1+\dfrac{1}{6}\ket1\bra0+\dfrac{1}{3}\ket1\bra1+\dfrac{1}{6}\ket1\bra2+\dfrac{1}{6}\ket2\bra1+\dfrac{1}{2}\ket2\bra2}
\end{align}$$
Alternatively, we can write it as a matrix as:
$$\begin{align}
\rho&=\begin{bmatrix}
\tfrac{1}{6}&\tfrac{1}{6}&0\\
\tfrac{1}{6}&\tfrac{1}{3}&\tfrac{1}{6}\\
0&\tfrac{1}{6}&\tfrac{1}{2}
\end{bmatrix}
\end{align}$$
To find the energy, we use the following matrix:
$$\begin{align}
\hat{H}&=\begin{bmatrix}
\tfrac{\hbar\omega}{2}&0&0\\
0&\tfrac{3\hbar\omega}{2}&0\\
0&0&\tfrac{5\hbar\omega}{2}
\end{bmatrix}
\end{align}$$
Then to find average energy, we evaluate:
$$\begin{align}
\braket{E}&=\text{Tr}\left(
\begin{bmatrix}
\tfrac{1}{6}&\tfrac{1}{6}&0\\
\tfrac{1}{6}&\tfrac{1}{3}&\tfrac{1}{6}\\
0&\tfrac{1}{6}&\tfrac{1}{2}
\end{bmatrix}
\begin{bmatrix}
\tfrac{\hbar\omega}{2}&0&0\\
0&\tfrac{3\hbar\omega}{2}&0\\
0&0&\tfrac{5\hbar\omega}{2}
\end{bmatrix}\right)\\
&=\hbar\omega\cdot\text{Tr}\left(
\begin{bmatrix}
\tfrac{1}{6}\cdot\tfrac{1}{2}&\tfrac{1}{6}\cdot\tfrac{1}{2}&0\cdot\tfrac{1}{2}\\
\tfrac{1}{6}\cdot\tfrac{3}{2}&\tfrac{1}{3}\cdot\tfrac{3}{2}&\tfrac{1}{6}\cdot\tfrac{3}{2}\\
0\cdot\tfrac{5}{2}&\tfrac{1}{6}\cdot\tfrac{5}{2}&\tfrac{1}{2}\cdot\tfrac{5}{2}
\end{bmatrix}
\right)\\
&=\hbar\omega\cdot\text{Tr}\left(
\begin{bmatrix}
\tfrac{1}{12}&\tfrac{1}{12}&0\\
\tfrac{1}{4}&\tfrac{1}{2}&\tfrac{3}{4}\\
0&\tfrac{5}{12}&\tfrac{5}{4}
\end{bmatrix}
\right)\\
&=\dfrac{1}{12}\hbar\omega+\dfrac{1}{2}\hbar\omega+\dfrac{5}{4}\hbar\omega\\
&=\dfrac{1+6+15}{12}\hbar\omega\\
&=\dfrac{22}{12}\hbar\omega\\
\Aboxed{\braket{E}&=\dfrac{11}{6}\hbar\omega}
\end{align}$$
