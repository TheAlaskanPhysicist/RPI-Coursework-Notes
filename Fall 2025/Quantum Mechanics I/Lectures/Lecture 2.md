Author: Stanley Goodwin
Date: XX, 2025

---
### Tensor Objects in Quantum Mechanics
A state vector $\ket\psi$ is an element of a complex Hilbert space $\mathcal{H}$.
 - A Hilbert space is a complex inner product space.
#### Vectors and Covectors
Let $\{e_i=\ket{e_i}\}$ be an orthonormal basis of $\mathcal{H}$, with corresponding dual space $\{e^i=\ket{e^i}\}$ in $\mathcal{H}^*$.
We can represent a state 1-vector as:
$$\begin{align}
\ket\psi&=\lambda^ie_i=\lambda^i\ket{e_i}
\end{align}$$
Components $\lambda^i\in\mathbb{C}$. 
These transform as contravariant vectors.

We can represent a state 1-form as:
$$\begin{align}
\bra\psi&=\lambda_ie^i=\lambda_i\bra{e^i}
\end{align}$$
Components $\lambda_i=g_{ji}\lambda^j\in\mathbb{C}$, using the Hermitian metric $g_{ij}=\braket{e_i|e_j}$.
These transform as contravariant vectors.

In the case where the basis is orthonormal, the relationships simplify to:
$$\begin{align}
g_{ij}&\rightarrow\delta_{ij} & \lambda_i&=(\lambda^i)^*\\
\end{align}$$
Where $*$ is the complex conjugate. The inner product defines an isomorphism between $\mathcal{H}$ and $\mathcal{H}^*$.

#### Operators
Operators in quantum mechanics are linear transform tensors $A\in\mathcal{H}\otimes\mathcal{H}^*$.
We can represent a general operator as:
$$\begin{align}
A&=A_{j}^ie_ie^j=A_{j}^i\ket{e_i}\bra{e^j}
\end{align}$$
These operators act on the left of vectors:
$$\begin{align}
A\ket\psi&=\left(A_{j}^i\ket{e_i}\bra{e^j}\right)\left(\psi^k\ket{\tilde{e}_k}\right)\\
&=A_{j}^i\psi^k\ket{e_i}\braket{e^j|\tilde{e}_k}\\
\end{align}$$
When the basis for the linear transform and vector are the same, then:
$$\begin{align}
A\ket\psi&=\left(A_{j}^i\ket{e_i}\bra{e^j}\right)\left(\psi^k\ket{\tilde{e}_k}\right)\\
&=A_{j}^i\psi^k\ket{e_i}\delta^j_k\\
\Aboxed{A\ket\psi&=\left(A_{k}^i\psi^k\right)\ket{e_i}}
\end{align}$$
These operators also act on the right of covectors:
$$\begin{align}
\bra\psi A&=\left(\psi_k\bra{\tilde{e}^k}\right)\left(A_{j}^i\ket{e_i}\bra{e^j}\right)\\
&=\psi_kA_{j}^i\braket{\tilde{e}^k|e_i}\bra{e^j}\\
\end{align}$$
When the basis for the linear transform and vector are the same, then:
$$\begin{align}
\bra\psi A&=A_{j}^i\psi_k\braket{e^k|e_i}\bra{e^j}\\
&=A_{j}^i\psi_k\bra{e^j}\delta^k_i\\
\Aboxed{\bra\psi A&=\left(A_{j}^k\psi_k\right)\bra{e^j}}
\end{align}$$











