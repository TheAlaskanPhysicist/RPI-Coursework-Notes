

Suppose we have $N$ particles with $N$ states (microstates).

For the simpler case of an ensemble of spin particles, we get:
$$\begin{align}
\ket\psi&=\bigotimes_{j=1}^N\ket{s_j,m_j}
\\
\ket{S,M}&=\braket{\psi|S,M}\ket{\psi}
\end{align}$$
where $|m_j|\le s_j$ and $\sum_{j=1}^Nm_j=M$.

We can define the ladder operators as:
$$\begin{align}
S_\pm&=\sum_{i=1}^N s_{i,\pm}
\end{align}$$
When applied to a state, we see:
$$\begin{align}
\ket{\psi}^\pm_i&=\bigotimes_{j=1}^{i-1}\ket{s_j,m_j}\otimes\ket{s_i,m_i\pm1}\otimes\bigotimes_{j=i+1}^{N}\ket{s_j,m_j}\\
S_\pm\ket{S,M}&=\sum_{i=1}^N s_{i,\pm}\ket{\psi}\\
\sqrt{S(S+1)-M(M\pm1)}\ket{S,M\pm1}&=\sum_{i=1}^N\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}\ket{\psi}^\pm_i\\
\ket{S,M\pm1}&=\sum_{i=1}^N\dfrac{\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}}{\sqrt{S(S+1)-M(M\pm1)}}\ket{\psi}^\pm_i\\
\Aboxed{\bra{\psi}^\pm_i\ket{S,M\pm1}&=\dfrac{\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}}{\sqrt{S(S+1)-M(M\pm1)}}=C^{\pm}_{SM}}
\end{align}$$
These are Clebsch-Gordon Coefficients, extended to more particles.

Applying the operator twice (same operator), we see:
$$\begin{align}
\ket{S,M}&=\ket{\psi}\\
S_\pm\ket{S,M\pm1}&=\sum_{i=1}^N\sum_{j=1}^N\dfrac{\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}}{\sqrt{S(S+1)-M(M\pm1)}}s_{j,\pm}\ket{\psi}^\pm_i\\\\
&=\sum_{i=1}^N\dfrac{\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}}{\sqrt{S(S+1)-M(M\pm1)}}\sqrt{s_i(s_i+1)-(m_i\pm1)(m_i\pm2)}\ket{\psi}^\pm_{ii}\\
&+\sum_{i=1}^N\sum_{j\neq i}^N\dfrac{\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}}{\sqrt{S(S+1)-M(M\pm1)}}\sqrt{s_j(s_j+1)-m_j(m_j\pm1)}\ket{\psi}^\pm_{ij}\\\\
\ket{S,M\pm2}&=\sum_{i=1}^N\dfrac{\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}}{\sqrt{S(S+1)-M(M\pm1)}}\dfrac{\sqrt{s_i(s_i+1)-(m_i\pm1)(m_i\pm2)}}{\sqrt{S(S+1)-(M\pm1)(M\pm2)}}\ket{\psi}^\pm_{ii}\\
&+\sum_{i=1}^N\sum_{j\neq i}^N\dfrac{\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}}{\sqrt{S(S+1)-M(M\pm1)}}\dfrac{\sqrt{s_j(s_j+1)-m_j(m_j\pm1)}}{\sqrt{S(S+1)-(M\pm1)(M\pm2)}}\ket{\psi}^\pm_{ij}
\end{align}$$
For spin-$1/2$ particles, however, it is not possible to operate on a state twice, thus:
$$\begin{align}
\ket{S,M\pm2}&=\sum_{i=1}^N\sum_{j\neq i}^N\dfrac{\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}}{\sqrt{S(S+1)-M(M\pm1)}}\dfrac{\sqrt{s_j(s_j+1)-m_j(m_j\pm1)}}{\sqrt{S(S+1)-(M\pm1)(M\pm2)}}\ket{\psi}^\pm_{ij}\\
\Aboxed{\bra{\psi}^\pm_{ij}\ket{S,M\pm2}&=\dfrac{\sqrt{s_i(s_i+1)-m_i(m_i\pm1)}}{\sqrt{S(S+1)-M(M\pm1)}}\dfrac{\sqrt{s_j(s_j+1)-m_j(m_j\pm1)}}{\sqrt{S(S+1)-(M\pm1)(M\pm2)}}(1-\delta_{ij})}\\
\ket{\psi}^\pm_{ij}&=\ket{s_1,m_1}\dots\ket{s_i,m_i}\dots\ket{s_j,m_j}\dots\dots\ket{s_N,m_N}
\end{align}$$
Suppose our original state $\ket\psi=\ket{\tfrac{N}{2},+\tfrac{N}{2}}$, then:
$$\begin{align}
\ket{\tfrac{N}{2},\tfrac{N}{2}-1}&=\dfrac{1}{\sqrt{N}}\sum_{i=1}^N\ket{\psi}^-_i\\
\end{align}$$
$$\begin{align}
\ket{S,M-2}&=\sum_{i=1}^N\sum_{j\neq i}^N\dfrac{1}{\sqrt{2}}\dfrac{1}{\sqrt{N(N-1)}}\ket{\psi}^-_{ij}
\end{align}$$




## Generalizing to any $SU(2)$
For an ensemble of $N$ particles that have any kind of angular moment, we can write the state:
$$\begin{align}
\ket\psi&=\bigotimes_{i=1}^N\ket{j_i,m_i}
\\
\ket{J,M}&=\braket{\psi|J,M}\ket{\psi}
\end{align}$$
Each tensor element may have differing representations, but should work out nonetheless.

We can define the following operators:
$$\begin{align}
J_\pm&=\sum_{i=1}^N j_{i,\pm} & J_z&=\sum_{i=1}^N j_{i,z}\\
\end{align}$$
$$\begin{align}
j_{i,\pm}\ket{j_i,m_i}&=\sqrt{j_i(j_i+1)-m_i(m_i\pm1)}\ket{j_i,m_i\pm1}\\
j_{i,z}\ket{j_i,m_i}&=m_i\ket{j_i,m_i}\\
\end{align}$$
On any arbitrary state $\psi$, we can then find that:
$$\begin{align}
J_\pm\ket{J,M}&=\sum_{i=1}^N j_{i,\pm}\ket{\psi}\\
\sqrt{J(J+1)-M(M\pm1)}\ket{J,M\pm1}&=\sum_{i=1}^N\sqrt{j_i(j_i+1)-m_i(m_i\pm1)}\ket{\psi}^\pm_i\\
\ket{J,M\pm1}&=\sum_{i=1}^N\dfrac{\sqrt{j_i(j_i+1)-m_i(m_i\pm1)}}{\sqrt{J(J+1)-M(M\pm1)}}\ket{\psi}^\pm_i\\
\Aboxed{\bra{\psi}^\pm_i\ket{J,M\pm1}&=\dfrac{\sqrt{j_i(j_i+1)-m_i(m_i\pm1)}}{\sqrt{J(J+1)-M(M\pm1)}}=C^{\pm}_{JM}}\\
\ket{\psi}^\pm_i&=\ket{j_1,m_1}\oplus\dots\oplus\ket{j_i,m_i\pm1}\oplus\dots\ket{j_N,m_N}
\end{align}$$

