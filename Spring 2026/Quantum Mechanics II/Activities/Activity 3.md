Stanley Goodwin, 1/28/2025

---
Consider the two-state problem with the Hamiltonian
$$\begin{align}
H&=E_1^{(0)}\ket{1^{(0)}}\bra{1^{(0)}}+E_2^{(0)}\ket{2^{(0)}}\bra{2^{(0)}}+\lambda V_{12}\ket{1^{(0)}}\bra{2^{(0)}}+\lambda V_{21}\ket{2^{(0)}}\bra{1^{(0)}}
\end{align}$$
where $\lambda$ is real and $E_1^{(0)}<E_2^{(0)}$ without loss of generality. In the basis $\left\{\ket{1^{(0)}},\ket{2^{(0)}}\right\}$, this Hamiltonian can be represented as:
$$\begin{align}
H=\begin{bmatrix}E_1^{(0)}&\lambda V_{12}\\\lambda V_{21}&E_2^{(0)}\end{bmatrix}
\end{align}$$
### Part A
Find the exact eigenvalues of this Hamiltonian, $E_{1,2}(\lambda)$:
$$\begin{align}
\det\left(H-\mathcal{E}\mathbb{I}\right)&=\left|\begin{array}{cc}E_1^{(0)}-\mathcal{E}&\lambda V_{12}\\\lambda V_{21}&E_2^{(0)}-\mathcal{E}\end{array}\right|\\
0&=\left(E_1^{(0)}-\mathcal{E}\right)\left(E_2^{(0)}-\mathcal{E}\right)-(\lambda V_{12})(\lambda V_{21})\\
0&=\mathcal{E}^2-\left(E_1^{(0)}+E_2^{(0)}\right)\mathcal{E}+\left(E_1^{(0)}E_2^{(0)}-\lambda^2 V_{12}V_{21}\right)
\end{align}$$
The solutions to $\mathcal{E}$ are of the form of the quadratic equation, thus:
$$\begin{align}
\mathcal{E}&=\dfrac{\left(E_1^{(0)}+E_2^{(0)}\right)}{2}\pm\sqrt{\dfrac{\left(E_1^{(0)}+E_2^{(0)}\right)^2}{4}-\left(E_1^{(0)}E_2^{(0)}-\lambda^2 V_{12}V_{21}\right)}\\
&=\dfrac{\left(E_1^{(0)}+E_2^{(0)}\right)}{2}\pm\sqrt{\dfrac{\left(E_1^{(0)}\right)^2+2E_1^{(0)}E_2^{(0)}+\left(E_2^{(0)}\right)^2}{4}-\left(E_1^{(0)}E_2^{(0)}-\lambda^2 V_{12}V_{21}\right)}\\
&=\dfrac{\left(E_1^{(0)}+E_2^{(0)}\right)}{2}\pm\sqrt{\dfrac{\left(E_1^{(0)}\right)^2-2E_1^{(0)}E_2^{(0)}+\left(E_2^{(0)}\right)^2}{4}+\lambda^2 V_{12}V_{21}}\\
\Aboxed{\mathcal{E}_{1,2}&=\dfrac{\left(E_2^{(0)}+E_1^{(0)}\right)}{2}\pm\sqrt{\dfrac{\left(E_2^{(0)}-E_1^{(0)}\right)^2}{4}+\lambda^2 V_{12}V_{21}}}
\end{align}$$
### Part B
Expand the eigenvalues in $\lambda$ up to the lowest-order non-vanishing corrections:
$$\begin{align}
\mathcal{E}_{1,2}&=\dfrac{\left(E_2^{(0)}+E_1^{(0)}\right)}{2}\pm\sqrt{\dfrac{\left(E_2^{(0)}-E_1^{(0)}\right)^2}{4}+\lambda^2 V_{12}V_{21}}\\
&\approx\dfrac{\left(E_2^{(0)}+E_1^{(0)}\right)}{2}\pm\left(\sqrt{\dfrac{\left(E_2^{(0)}-E_1^{(0)}\right)^2}{4}}+\dfrac{V_{12}V_{21}}{2\sqrt{\tfrac{\left(E_2^{(0)}-E_1^{(0)}\right)^2}{4}}}\lambda^2+O(\lambda^4)\right)\\
&\approx\dfrac{E_2^{(0)}+E_1^{(0)}}{2}\pm\left(\dfrac{E_2^{(0)}-E_1^{(0)}}{2}+\dfrac{V_{12}V_{21}}{E_2^{(0)}-E_1^{(0)}}\lambda^2\right)\\
\mathcal{E}_{1,2}&=\dfrac{E_2^{(0)}\pm E_2^{(0)}}{2}+\dfrac{E_1^{(0)}\mp E_1^{(0)}}{2}\pm\dfrac{V_{12}V_{21}}{E_2^{(0)}-E_1^{(0)}}\lambda^2
\end{align}$$
Thus we have:
$$\begin{align}
\Aboxed{\mathcal{E}_{+}&\approx E_2^{(0)}+\dfrac{V_{12}V_{21}}{E_2^{(0)}-E_1^{(0)}}\lambda^2}\\
\Aboxed{\mathcal{E}_{-}&\approx E_1^{(0)} -\dfrac{V_{12}V_{21}}{E_2^{(0)}-E_1^{(0)}}\lambda^2}
\end{align}$$
### Part C
Consider $\lambda V$ as a perturbation and write the above Hamiltonian as:
$$\begin{align}
H_0&=\begin{bmatrix}E_1^{(0)}&0\\0&E_2^{(0)}\end{bmatrix} &
\lambda V&=\begin{bmatrix}0&\lambda V_{12}\\\lambda V_{21}&0\end{bmatrix} &
\end{align}$$
Find the lowest-order non-vanishing energy correction to the initial energies.

Well from the equation in class:
$$\begin{align}
E_n^{(2)}&=\sum_{k\ne n}\dfrac{|\bra{k^{(0)}}\lambda V\ket{n^{(0)}}|^2}{E_n^{(0)}-E_k^{(0)}}=\sum_{k\ne n}\dfrac{\lambda^2 |V_{kn}|^2}{E_n^{(0)}-E_k^{(0)}}
\end{align}$$
Since there are only two states, these are just the non-diagonal term:
$$\begin{align}
E_n^{(2)}&=\dfrac{\lambda^2 |V_{kn}|^2}{E_n^{(0)}-E_k^{(0)}}\\
E_1^{(2)}&=\dfrac{\lambda^2 |V_{21}|^2}{E_1^{(0)}-E_2^{(0)}}=-\dfrac{\lambda^2 |V_{21}|^2}{E_2^{(0)}-E_1^{(0)}}\\
E_2^{(2)}&=\dfrac{\lambda^2 |V_{12}|^2}{E_2^{(0)}-E_1^{(0)}}\\
\end{align}$$
The magnitude squared makes these identical, and thus:
$$\begin{align}
\Aboxed{E_1^{(2)}&=-\dfrac{V_{12}V_{21}}{E_2^{(0)}-E_1^{(0)}}\lambda^2}\\
\Aboxed{E_2^{(2)}&=+\dfrac{ |V_{12}|^2}{E_2^{(0)}-E_1^{(0)}}\lambda^2}\\
\end{align}$$
The total energy after correction is then just:
$$\begin{align}
\Aboxed{\mathcal{E}_{+}&= E_2^{(0)}+\dfrac{V_{12}V_{21}}{E_2^{(0)}-E_1^{(0)}}\lambda^2}\\
\Aboxed{\mathcal{E}_{-}&= E_1^{(0)} -\dfrac{V_{12}V_{21}}{E_2^{(0)}-E_1^{(0)}}\lambda^2}
\end{align}$$
Which is the same as the previous part.