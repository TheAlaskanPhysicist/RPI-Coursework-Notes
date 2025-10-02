Author: Stanley Goodwin
Date: XX, 2025

---
### Spin $1/2$ Systems
Let us define a Hilbert space $\mathcal{H}$ whose basis is orthonormal and complete:
$$\begin{align}
\mathcal{H}&=\text{span}\left\{\ket{\chi^{(r)}_+},\ket{\chi^{(r)}_-}\right\}
\end{align}$$
These can be any radial direction of measurement, but lets use $r=z$ for our systems.
We can form the identity operator in this space as:
$$\begin{align}
\mathbb{I}&=\ket{\chi^{z}_+}\bra{\chi^{z}_+}+\ket{\chi^{z}_-}\bra{\chi^{z}_-}
\end{align}$$
Some useful operators are as follows:
$$\begin{align}
\sigma_x&=\ \ket{\chi^{z}_-}\bra{\chi^{z}_+}\ +\ \ket{\chi^{z}_+}\bra{\chi^{z}_-}\\
\sigma_y&=i\ket{\chi^{z}_-}\bra{\chi^{z}_+}-i\ket{\chi^{z}_+}\bra{\chi^{z}_-}\\
\sigma_z&=\ \ket{\chi^{z}_+}\bra{\chi^{z}_+}\ -\ \ket{\chi^{z}_-}\bra{\chi^{z}_-}\\
\end{align}$$
These traceless $\text{Tr}(\sigma_i)=0$ matrices are the generators of rotation for our spins.
When acting on our state vectors, we can see that:
$$\begin{align}
\sigma_x:&&\psi_+\ket{\chi^{z}_+}+\psi_-\ket{\chi^{z}_-}&&\rightarrow&&\psi_-\ket{\chi^{z}_+}&+\psi_+\ket{\chi^{z}_-}\\
\sigma_y:&&\psi_+\ket{\chi^{z}_+}+\psi_-\ket{\chi^{z}_-}&&\rightarrow&&-i\psi_-\ket{\chi^{z}_+}&+i\psi_+\ket{\chi^{z}_-}\\
\sigma_z:&&\psi_+\ket{\chi^{z}_+}+\psi_-\ket{\chi^{z}_-}&&\rightarrow&&\psi_+\ket{\chi^{z}_+}&-\psi_-\ket{\chi^{z}_-}\\
\end{align}$$
These operators are Hermitian and Unitary. The also satisfy:
$$\begin{align}
\sigma_i\sigma_j&=\delta_{ij}+i\epsilon_{ijk}\sigma_k\\
[\sigma_i,\sigma_j]&=2i\epsilon_{ijk}\sigma_k\\
\{\sigma_i,\sigma_j\}&=2\delta_{ij}\\
\end{align}$$
The true spin operators are written as a scale factor of the Pauli matrices:
$$\begin{align}
S_i&=\dfrac{\hbar}{2}\sigma_i & [S_i,S_j]&=i\hbar^2 \epsilon_{ijk}S_k & \{\sigma_i,\sigma_j\}&=\dfrac{\hbar^2}{2}\delta_{ij}\\
\end{align}$$







