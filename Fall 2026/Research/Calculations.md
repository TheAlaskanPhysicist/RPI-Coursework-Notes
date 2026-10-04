

Suppose we have an initial statevector $\ket{\psi(0)}$ and a time-independent Hamiltonian:
$$\begin{align}
\ket{\psi(t)}&=e^{-i\hat{H}t/\hbar}\ket{\psi(0)}
\end{align}$$
We can write this statevector as a linear combination of the energy eigenvectors:
$$\begin{align}
\ket{\psi(t)}&=\sum_{n}c_ne^{-iE_nt/\hbar}\ket{\phi_n}
\end{align}$$
Suppose we now want to calculate the average magnetization of this state
$$\begin{align}
\left\langle M^i\right\rangle&=\sum_{n,m}c_m^*c_ne^{-i(E_n-E_m)t/\hbar}\bra{\phi_m}M^i\ket{\phi_n}
\end{align}$$
Let $E_n-E_m=\hbar\omega_{nm}$, then we have that
$$\begin{align}
\left\langle M^i\right\rangle&=\sum_{n,m}c_m^*c_ne^{-i\omega_{nm}t}\bra{\phi_m}M^i\ket{\phi_n}
\end{align}$$
Now lets integrate this over time. Let $T$ be the period of time that we're integrating, then
$$\begin{align}
\left\langle \left\langle M^i\right\rangle\right\rangle&=\dfrac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}}\sum_{n,m}c_m^*c_ne^{-i\omega_{nm}t}\bra{\phi_m}M^i\ket{\phi_n}\ dt
\end{align}$$
The only time dependence is the exponential term, and thus
$$\begin{align}
\left\langle \left\langle M^i\right\rangle\right\rangle
&=\dfrac{1}{T}\sum_{n,m}c_m^*c_n\bra{\phi_m}M^i\ket{\phi_n}\int_{-\frac{T}{2}}^{\frac{T}{2}}e^{-i\omega_{nm}t}\ dt\\
&=\dfrac{2}{T}\sum_{n,m}c_m^*c_n\dfrac{1}{\omega_{nm}}\bra{\phi_m}M^i\ket{\phi_n}\sin\left(\frac{\omega_{nm}T}{2}\right)\\
\left\langle \left\langle M^i\right\rangle\right\rangle&=\sum_{n,m}c_m^*c_n\bra{\phi_m}M^i\ket{\phi_n}\frac{\sin\left(\frac{\omega_{nm}T}{2}\right)}{\frac{\omega_{nm}T}{2}}
\end{align}$$
In the limit of $T\to\infty$, this vanishes unless $\omega_{nm}=0$, and so becomes
$$\begin{align}
\lim_{T\to\infty}\left\langle \left\langle M^i\right\rangle\right\rangle&=\sum_{n,m}c_m^*c_n\bra{\phi_m}M^i\ket{\phi_n}\delta_{\omega_{nm},0}
\end{align}$$
This only occurs when the energy of two eigenstates is identical. Thus we can instead write this double sum as the sum over all statevectors of a degenerate energy, and then sum over all different energies of the eigenstates. 
$$\begin{align}
\lim_{T\to\infty}\left\langle \left\langle M^i\right\rangle\right\rangle&=\sum_n\sum_{a,b\in D_E}c_{E,b}^*c_{E,a}\bra{\phi_{E,b}}M^i\ket{\phi_{E,a}}
\end{align}$$
Suppose a projector onto the energy $E$ eigenspace
$$\begin{align}
P_E&=\sum_{a\in D_E}\ket{\phi_{E,a}}\bra{\phi_{E,a}}
\end{align}$$
Then the de-phased density matrix is
$$\begin{align}
\rho_{D_E}&=\sum_E P_E\rho(0)P_E &&& \rho(0)=\ket{\psi(0)}\bra{\psi(0)}
\end{align}$$
Then the time-averaged magnetization is just
$$\begin{align}
\lim_{T\to\infty}\left\langle \left\langle M^i\right\rangle\right\rangle&=\operatorname{Tr}\left(\rho_{D_E} M^i\right)
\end{align}$$
Computationally, using diagonalization, we can also calculate it as
$$\begin{align}
\lim_{T\to\infty}\left\langle \left\langle M^i\right\rangle\right\rangle
&=\sum_n\left|(V^\dagger\psi_0)_n\right|^2\left(V^\dagger M^z V\right)_{nn}\\
&=\sum_n\left|(V^\dagger\psi_0)_n\right|^2\left(V^\dagger M^z V\right)_{nn}\\
\end{align}$$
where $H=V^\dagger DV$, and only needs to be diagonalized once.
