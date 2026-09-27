


## Time-Independent Perturbation Theory
Suppose we have an unperturbed system that satisfies the Schrodinger equation
$$\begin{align}
\hat{H}_0\ket{\psi}&=E^{(0)}\ket{\psi}
\end{align}$$
We introduce a perturbation $\mathcal{H}$ with a scalar parameter $\lambda$ such that
$$\begin{align}
\hat{H}&=\hat{H}_0+\lambda\mathcal{H} & (\lambda\to1)
\end{align}$$
Substituting this perturbed Hamiltonian into the Schrodinger equation gives
$$\begin{align}
\hat{H}\ket{\psi}&=E\ket{\psi} &\to&&
\left(\hat{H}_0+\lambda \mathcal{H}\right)\ket{\psi}&=\left(E^{(0)}+\varepsilon\right)\ket{\psi}
\end{align}$$
where $\varepsilon$ is the difference in energy in the perturbation. We can rearrange this equation to move the unperturbed operators/scalars to one side, resulting in
$$\begin{align}
\left(\hat{H}_0-E^{(0)}\right)\ket{\psi}&=\left(\varepsilon-\lambda \mathcal{H}\right)\ket{\psi}
\end{align}$$
We now expand $\varepsilon$ and $\ket{\psi}$ into perturbations of increasing order, as in
$$\begin{align}
\ket{\psi}&=\ket{\psi^{(0)}}+\lambda\ket{\psi^{(1)}}+\lambda^2\ket{\psi^{(2)}}+\dots &&&
\varepsilon&=\lambda\varepsilon^{(1)}+\lambda^2\varepsilon^{(2)}+\dots
&&&(\lambda\to1)
\end{align}$$
As $\lambda\to1$, we add each order contribution to arrive to the final true state. Substituting our expansions in as summations yields
$$\begin{align}
&&\left(\hat{H}_0-E^{(0)}\right)\sum_{i=0}^\infty\lambda^i\ket{\psi^{(i)}}&=\sum_{k=0}^\infty\left(\sum_{j=1}^\infty\lambda^j\varepsilon^{(j)}-\lambda \mathcal{H}\right)\lambda^k\ket{\psi^{(k)}}\\
\to&&
\left(\hat{H}_0-E^{(0)}\right)\sum_{i=0}^\infty\lambda^i\ket{\psi^{(i)}}&=\sum_{k=0}^\infty\sum_{j=1}^\infty\lambda^{j+k}\varepsilon^{(j)}\ket{\psi^{(k)}}-\sum_{k=0}^\infty\mathcal{H}\lambda^{k+1}\ket{\psi^{(k)}}
\end{align}$$
We can do some reindexing so that the order of $\lambda$ is the same
$$\begin{align}
&&\left(\hat{H}_0-E^{(0)}\right)\sum_{i=0}^\infty\lambda^i\ket{\psi^{(i)}}&=\sum_{k=0}^\infty\left(\sum_{j=1}^\infty\lambda^j\varepsilon^{(j)}-\lambda \mathcal{H}\right)\lambda^k\ket{\psi^{(k)}}\\
\to&&
\left(\hat{H}_0-E^{(0)}\right)\sum_{i=0}^\infty\lambda^i\ket{\psi^{(i)}}&=\sum_{i=1}^\infty\sum_{j=0}^{i-1}\lambda^{i}\varepsilon^{(i-j)}\ket{\psi^{(j)}}-\sum_{i=1}^\infty\mathcal{H}\lambda^{i}\ket{\psi^{(i-1)}}
\end{align}$$
These summations can be collapsed into the relationship
$$\begin{align}
\left(\hat{H}_0-E^{(0)}\right)\ket{\psi^{(i)}}&=\sum_{j=0}^{i-2}\varepsilon^{(i-j)}\ket{\psi^{(j)}}+\left(\varepsilon^{(1)}-\mathcal{H}\right)\ket{\psi^{(i-1)}}
&&& (i\ge1)
\end{align}$$
Without supposing if the state is degenerate, we want to construct a completeness relation for all non-degenerate states. In our system, that would mean we have the operator
$$\begin{align}
\hat{\Phi}&=\sum_{\phi\not\in D}\ket{\phi^{(0)}}\bra{\phi^{(0)}}
\end{align}$$
where $D$ is the degenerate subspace of our original $\ket{\psi}$. Applying to our system, we get
$$\begin{align}
\ket{\psi^{(i)}}&=
\sum_{\phi\not\in D}\left(\sum_{j=0}^{i-1}\varepsilon^{(i-j)}\dfrac{\left<\phi^{(0)}\middle|\psi^{(j)}\right>}{E^{(0)}_\phi-E^{(0)}_\psi}\right)\ket{\phi^{(0)}}-\sum_{\phi\not\in D}\dfrac{\bra{\phi^{(0)}}\mathcal{H}\ket{\psi^{(i-1)}}}{E^{(0)}_\phi-E^{(0)}_\psi}\ket{\phi^{(0)}}
\end{align}$$
For the first-order correction for the wavefunction, it takes the form
$$\begin{align}
\ket{\psi^{(1)}}&=-\sum_{\phi\not\in D}\dfrac{\bra{\phi^{(0)}}\left(\mathcal{H}-\varepsilon^{(1)}\right)\ket{\psi^{(0)}}}{E^{(0)}_\phi-E^{(0)}_\psi}\ket{\phi^{(0)}}
\end{align}$$
The second-order correction for the wavefunction (after using orthonormality) is
$$\begin{align}
\ket{\psi^{(2)}}&=
\left(\sum_{\phi\not\in D}\varepsilon^{(2)}\dfrac{\left<\phi^{(0)}\middle|\psi^{(0)}\right>}{E^{(0)}_\phi-E^{(0)}_\psi}-\sum_{\phi\not\in D}\varepsilon^{(1)}\dfrac{\bra{\phi^{(0)}}\left(\mathcal{H}-\varepsilon^{(1)}\right)\ket{\psi^{(0)}}}{\left(E^{(0)}_{\phi}-E^{(0)}_\psi\right)^2}-\sum_{\phi\not\in D}\dfrac{\bra{\phi^{(0)}}\mathcal{H}\ket{\psi^{(1)}}}{E^{(0)}_\phi-E^{(0)}_\psi}\right)\ket{\phi^{(0)}}
\end{align}$$
$$\begin{align}
\ket{\psi^{(2)}}&=
\sum_{\phi\not\in D}\ket{\phi^{(0)}}\bra{\phi^{(0)}}\left(\dfrac{\varepsilon^{(2)}}{E^{(0)}_\phi-E^{(0)}_\psi}-\dfrac{\varepsilon^{(1)}}{E^{(0)}_{\phi}-E^{(0)}_\psi}\dfrac{\mathcal{H}-\varepsilon^{(1)}}{E^{(0)}_{\phi}-E^{(0)}_\psi}+\dfrac{\mathcal{H}\hat{\Phi}\left(\mathcal{H}-\varepsilon^{(1)}\right)}{\left(E^{(0)}_\phi-E^{(0)}_\psi\right)\left(H_0-E^{(0)}_\psi\right)}\right)\ket{\psi^{(0)}}
\end{align}$$

