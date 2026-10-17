## 2.4
Show the following:
$$\begin{align}
X^\dagger(m,n)&=\left(\ket{\phi_m}\bra{\phi_n}\right)^\dagger=\bra{\phi_n}^\dagger\ket{\phi_m}^\dagger=\ket{\phi_n}\bra{\phi_m}\\
[H,X]&=(E_m-E_n)X(m,n)\\
X(m,n)X^\dagger(p,q)&=\delta_{nq}X(m,p)\\
\operatorname{Tr}(X(m,n))&=\delta_{mn}\\
A&=\sum_{m,n}A_{mn}X(m,n)\\
A_{pq}&=\operatorname{Tr}(AX^\dagger(p,q))
\end{align}$$
## 3.15.A
Show the following:
$$\begin{align}
i\hbar\dfrac{d}{dt}\ket{\psi_I(t)}&=W_I(t)\ket{\psi_I(t)} & W_I(t)&=U_0^\dagger(t,t_0)W(t)U_0(t,t_0)
\end{align}$$
Explain why when $W(t)$ is smaller than $H_0(t)$, the motion of $\ket{\psi_I(t)}$ is smaller than $\ket{\psi_S(t)}$.
## 3.15.B
Show that the differential equation is equivalent to the integral equation
$$\begin{align}
\ket{\psi_I(t)}&=\ket{\psi_I(t_0)}+\dfrac{1}{i\hbar}\int_{t_0}^t\ dt'\ W_I(t')\ket{\psi_I(t')}
\end{align}$$
## 3.15.C
Show that by iteration the statevector equation becomes
$$\begin{align}
\ket{\psi_I(t)}&=\left[\mathbb{I}+\dfrac{1}{i\hbar}\int_{t_0}^t\ dt'\ W_I(t')+\dfrac{1}{(i\hbar)^2}\int_{t_0}^t\ dt'\ W_I(t')\int_{t_0}^{t'}\ dt''\ W_I(t'')+\dots\right]\ket{\psi_I(t_0)}
\end{align}$$








