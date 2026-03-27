Author: Stanley Goodwin
Date: March 13th, 2026

---
## Problem 1
Use perturbation theory to calculate the effect of the proton's finite size on the $n=1$ and $n=2$ energy levels of the hydrogen atom. Assume the proton is a uniformly charged sphere of radius $R$. Give a physical explanation for why the $l=1$ shifts are so much smaller than for $l=0$.

---
### Coulomb Potential of Finite-Radius Proton
For a uniform sphere of charge $Q$ and radius $R$ , Gauss's law makes this trivial.

The charge enclosed in a sphere of radius $r$ is simply the ratio of volumes inside, and $Q$ outside:
$$\begin{align}
q_\text{enc}(r)&=\begin{cases}
Q\tfrac{r^3}{R^3},&0\le r<R\\
Q,&r\ge R
\end{cases}
\end{align}$$
Since $\vec{E}$ and $d\vec{S}$ point radially outward, Gauss's law simplifies to:
$$\begin{align}
E\cdot4\pi r^2&=\dfrac{q_\text{enc}(r)}{\epsilon_0} &\implies&& \vec{E}(r)&=\dfrac{Q}{4\pi\epsilon_0}\begin{cases}
\tfrac{r}{R^3},&0\le r<R\\
\tfrac{1}{r^2},&r\ge R
\end{cases}
\end{align}$$
Since the electric field is radially-symmetric, the potential is simply the antiderivative of the electric field with respect to radius $r$, and so:
$$\begin{align}
V_\text{naive}(r)&=-\dfrac{Q}{4\pi\epsilon_0}\begin{cases}
\tfrac{r^2}{2R^3},&0\le r<R\\
-\tfrac{1}{r},&r\ge R
\end{cases}
\end{align}$$
However, the potential must be continuous at $r=R$ (no interface charge), and so adjusted:
$$\begin{align}
\dfrac{Q}{4\pi\epsilon_0}\dfrac{1}{R}&=-\dfrac{Q}{8\pi\epsilon_0R^3}R^2+V_0 &\implies&& V_0&=3\dfrac{Q}{8\pi\epsilon_0}\dfrac{1}{R}
\end{align}$$
For simplicity later, we can break this potential into two parts (and using $Q=+e$):
$$\begin{align}
V_\text{in}(r)&=\dfrac{e}{4\pi\epsilon_0}\dfrac{3R^2-r^2}{2R^3},&0\le r<R\\
V_\text{out}(r)&=\dfrac{e}{4\pi\epsilon_0}\dfrac{1}{r},&r\ge R
\end{align}$$



### Hydrogen Atom ($r<R$)
For radii inside the radius of the proton, our Hamiltonian takes the form:
$$\begin{align}
H&=-\dfrac{\hbar^2}{2m}\vec\nabla^2-\dfrac{e^2}{4\pi\epsilon_0}\dfrac{3R^2-r^2}{2R^3}
\end{align}$$
Since we know the solutions to the hydrogen atom for a point-like proton centered at the origin, we want to find a perturbation that converts it into our Hamiltonian. Our choices are:
$$\begin{align}
H_0&=-\dfrac{\hbar^2}{2m}\vec\nabla^2-\dfrac{e^2}{4\pi\epsilon_0r}\\
V&=+\dfrac{e^2}{4\pi\epsilon_0r}-\dfrac{e^2}{4\pi\epsilon_0}\dfrac{3R^2-r^2}{2R^3}
\end{align}$$
Our perturbative potential cancels with the point potential and replaces it with the new one.

The first-order energy correction is always easy to remember, since it is just the expected value of the perturbation potential of the zeroth-order states. After some cleanup, the energy difference is:
$$\begin{align}
\left\langle V\right\rangle&=\dfrac{e^2}{4\pi\epsilon_0}\left\langle\dfrac{1}{r}\right\rangle-\dfrac{3e^2}{8\pi\epsilon_0 R}\left\langle 1\right\rangle+\dfrac{e^2}{8\pi\epsilon_0R^3}\left\langle r^2\right\rangle
\end{align}$$
For the sake of using the textbook, I will drop the $4\pi\epsilon_0$ for the Gauss units version instead:
$$\begin{align}
\left\langle V\right\rangle&=e^2\left\langle\dfrac{1}{r}\right\rangle-\dfrac{3e^2}{2R}\left\langle 1\right\rangle+\dfrac{e^2}{2R^3}\left\langle r^2\right\rangle
\end{align}$$
These expected values are of the original hydrogen states, so we can use Appendix B.6 of our textbook in order to find the expected values above (B.59 to be exact, with $Z=1$):
$$\begin{align}
\left\langle\dfrac{1}{r}\right\rangle
&=\dfrac{1}{n^2a_0} &&& \left\langle r^2\right\rangle
&=\dfrac{a_0^2n^2}{2}\left[5n^2+1-3l(l+1)\right]
\end{align}$$
Substituting into our energy correction (now labelled $E_{n,l}^{(1)}=\left\langle V\right\rangle$), we have:
$$\begin{align}
E_{n,l}^{(1)}&=\dfrac{e^2}{n^2a_0}-\dfrac{3e^2}{2R}+\dfrac{e^2}{2R^3}\dfrac{a_0^2n^2}{2}\left[5n^2+1-3l(l+1)\right]
\end{align}$$
Note #2 mentioning we should consider answers only of the leading order $R/a_0$, so we can write each term with factored out components as:
$$\begin{align}
E_{n,l}^{(1)}&=\dfrac{e^2}{a_0}\left(\dfrac{1}{n^2}-\dfrac{3}{2}\left(\dfrac{a_0}{R}\right)+\dfrac{n^2}{4}\left(\dfrac{a_0}{R}\right)^3\left[5n^2+1-3l(l+1)\right]\right)\\
&=\dfrac{e^2}{a_0}\left(\dfrac{a_0}{R}\right)^3\left(\dfrac{1}{n^2}\left(\dfrac{R}{a_0}\right)^3-\dfrac{3}{2}\left(\dfrac{R}{a_0}\right)^2+\dfrac{n^2}{4}\left[5n^2+1-3l(l+1)\right]\right)
\end{align}$$



Just to the leading order of $R/a_0$, the potential in the small-proton regime is:
$$\begin{align}
\Aboxed{\lim_{R/a_0\ll1}E_{n,l}^{(1)}&=\dfrac{e^2a_0^2}{4R^3}n^2\left[5n^2+1-3l(l+1)\right]} && \text{Gaussian Units}\\
\Aboxed{\lim_{R/a_0\ll1}E_{n,l}^{(1)}&=\dfrac{e^2a_0^2}{16\pi\epsilon_0R^3}n^2\left[5n^2+1-3l(l+1)\right]} && \text{SI Units}\\
\end{align}$$
---
### Effect on Energy Levels ($R\ll a_0$)
For proton radii who are relatively small compared to the Bohr radius, we have the expressions from the previous section:
$$\begin{align}
\lim_{R/a_0\ll1}E_{n,l}^{(1)}&=\dfrac{e^2a_0^2}{16\pi\epsilon_0R^3}n^2\left[5n^2+1-3l(l+1)\right]
\end{align}$$
Something of note, this energy is not dependent on magnetic quantum number.

For the case of $n=1$, $l=0$ by necessity, and so we find:
$$\begin{align}
\lim_{R/a_0\ll1}E_{1,0}^{(1)}&=6\cdot\dfrac{e^2a_0^2}{16\pi\epsilon_0R^3}
\end{align}$$
For the case of $n=2$, we have both $l=0$ and $l=1$ to consider, and so:
$$\begin{align}
\lim_{R/a_0\ll1}E_{2,0}^{(1)}&=84\cdot\dfrac{e^2a_0^2}{16\pi\epsilon_0R^3} & \lim_{R/a_0\ll1}E_{2,1}^{(1)}&=60\cdot\dfrac{e^2a_0^2}{16\pi\epsilon_0R^3}\\
\end{align}$$
We can rewrite these to be a bit clearer, and so we then have:
$$\begin{align}
\Aboxed{E_\text{1s}^{(1)}&=\dfrac{3}{2}\dfrac{e^2a_0^2}{4\pi\epsilon_0R^3}} &
\Aboxed{E_\text{2s}^{(1)}&=21\dfrac{e^2a_0^2}{4\pi\epsilon_0R^3}} &
\Aboxed{E_\text{2p}^{(1)}&=15\dfrac{e^2a_0^2}{4\pi\epsilon_0R^3}}
\end{align}$$
In terms of total energy after the first-order correction, we have instead:
$$\begin{align}
\Aboxed{E_\text{1s}&\approx-\dfrac{me^4}{2(4\pi\epsilon_0)^2\hbar^2}\left(1-3\dfrac{a_0^3}{R^3}\right)} \\
\Aboxed{E_\text{2s}&\approx-\dfrac{me^4}{2(4\pi\epsilon_0)^2\hbar^2}\left(\dfrac{1}{4}-42\dfrac{a_0^3}{R^3}\right)} \\
\Aboxed{E_\text{2p}&\approx-\dfrac{me^4}{2(4\pi\epsilon_0)^2\hbar^2}\left(\dfrac{1}{4}-30\dfrac{a_0^3}{R^3}\right)}
\end{align}$$
<div style="page-break-before: always;"></div>



### Orbital Energy Difference ($R\ll a_0$)
To answer the question about why $l=1$ and $l=0$ shifts are different, we can substitute in:
$$\begin{align}
\lim_{R/a_0\ll1}E_{n,0}^{(1)}&=\dfrac{e^2a_0^2}{16\pi\epsilon_0R^3}n^2\left[5n^2+1\right] &&& \lim_{R/a_0\ll1}E_{n,1}^{(1)}&=\dfrac{e^2a_0^2}{16\pi\epsilon_0R^3}n^2\left[5n^2-5\right]
\end{align}$$
The difference in the energy between $l=1$ and $l=0$ is:
$$\begin{align}
\lim_{R/a_0\ll1}E_{n,1}^{(1)}-E_{n,0}^{(1)}&=-\dfrac{3e^2a_0^2}{8\pi\epsilon_0R^3}n^2 &&& (n&\ge2)
\end{align}$$
In SI units, and using the definition of the Bohr radius, we can write the energy difference as:
$$\begin{align}
\lim_{R/a_0\ll1}E_{n,1}^{(1)}-E_{n,0}^{(1)}&=-\dfrac{3}{8\pi^2(R/a_0)^3}\dfrac{(hc)^2}{a_0^2\cdot mc^2}n^2 &&& (n&\ge2)
\end{align}$$
We can make the substitutions $hc=1240\text{ eV nm}$, $mc^2=0.511\cdot10^6\text{ eV}$, $a_0=5.29\cdot10^{-2}\text{ nm}$.
If we represent the ratio of proton volume $V_p$ to Bohr volume $V_B$ as a constant $\kappa=V_p/V_B$:
$$\begin{align}
\lim_{\kappa\ll1}E_{n,1}^{(1)}-E_{n,0}^{(1)}&\approx-\dfrac{40.855}{\kappa}n^2\text{ eV} &&& (n&\ge2)
\end{align}$$
The difference in the energy of $p$- and $s$-orbitals grows increasingly big as the square of $n$.

As for the *physical* reason this takes place, the $p$-orbitals vanish at the origin, which is much more apparent when looking at the form of the radial wavefunction (also Appendix B.6):
$$\begin{align}
R_{21}(r)&=\left(\dfrac{1}{2a_0}\right)^{3/2}\dfrac{r}{\sqrt{3}a_0}e^{-r/2a_0}
\end{align}$$
The linear component forces the probability density to decay near the origin, and so when our proton radius is very small, the interior contribution becomes vanishingly small. This is *not* the case for the $s$-orbital, since even at $r=0$, there's a constant probability density.

This actually occurs for all higher-order orbitals, since we can see the difference in the energy of an orbital from the $s$-orbital is:
$$\begin{align}
\lim_{R/a_0\ll1}E_{n,l}^{(1)}-E_{n,0}^{(1)}&=-\dfrac{3e^2a_0^2}{16\pi\epsilon_0R^3}n^2\cdot l(l+1)
\end{align}$$
Similar to the radial function before, what I suspect is that we have a proportionality:
$$\begin{align}
R_{nl}(r)&\sim\left(\dfrac{r}{a_0}\right)^l &&& 1\le l&<n &\land&& n\ge2
\end{align}$$
Thus, higher values of $l$ have much faster decays since $0\le r\le R\ll a_0$.



## Problem 2
This was the question I did in class.

---
## Problem 3
Two spin-$\text{1/2}$ particles are coupled by the effective Hamiltonian
$$\begin{align}
H&=\underbrace{A\vec{S}_1\cdot\vec{S}_2}_{H_0}+\underbrace{\tfrac{eB}{mc}\left(S_{1z}-S_{2z}\right)}_{V}
\end{align}$$
where $A>0$ is a coupling constant and $B$ is the external magnetic field. Our choice of $V$ as a perturbation can be justified for small applied magnetic fields.

---
### Problem 3.A
Find the eigenkets and eigenvalues of the unperturbed Hamiltonian $H_0=A\vec{S}_1\cdot\vec{S}_2$. Noting that $\vec{J}=\vec{S}_1+\vec{S}_2$ , where $\vec{J}$ is the total angular momentum, and using an appropriate basis to begin with, this task can be accomplished almost immediately, as opposed to brute-force diagonalization.

Hint: please use the following $\left\{\ket{jm}\right\}$ basis for the total spin (where $\vec{J}$ and $J_z$ are diagonal) *and stick to this labeling to have a common ground in our notation*:
$$\begin{align}
\ket{1}&\equiv\ket{0\ \ \ \ 0}=\dfrac{1}{\sqrt{2}}\left(\ket{+-}-\ket{-+}\right)\\
\ket{2}&\equiv\ket{1-\!1}=\ket{--}\\
\ket{3}&\equiv\ket{1\ \ \ \ 0}=\dfrac{1}{\sqrt{2}}\left(\ket{+-}+\ket{-+}\right)\\
\ket{4}&\equiv\ket{1+\!1}=\ket{++}
\end{align}$$
We can rewrite the Hamiltonian in terms of angular momenta as the following:
$$\begin{align}
\vec{J}^2&=\vec{S}_1^2+\vec{S}_2^2+2\vec{S}_1\cdot\vec{S}_2 &\implies&& \vec{S}_1\cdot\vec{S}_2&=\dfrac{1}{2}\left(\vec{J}^2-\vec{S}_1^2-\vec{S}_2^2\right)
\end{align}$$
Since we're working on solely spin-$\text{1/2}$ individual states, this product simplifies:
$$\begin{align}
\vec{S}_1^2=\vec{S}_2^2&=\dfrac{3}{4}\hbar^2 &\implies&& \vec{S}_1\cdot\vec{S}_2&=\dfrac{\hbar^2}{2}\left(\dfrac{\vec{J}^2}{\hbar^2}-\dfrac{3}{2}\right)
\end{align}$$
<div style="page-break-before: always;"></div>



For $\vec{J}^2$, we can notice that we can quickly find the solution for all of our choice of basis:
$$\begin{align}
\vec{J}^2\ket{1}&=0\hbar^2\ket{1} & \vec{J}^2\ket{n}&=2\hbar^2\ket{n}, \ n=2,3,4
\end{align}$$
Thus, applying our Hamiltonian to these 4 coupled states, we find that:
$$\begin{align}
H_0\ket{1}&=A\dfrac{\hbar^2}{2}\left(0-\dfrac{3}{2}\right)\ket{1}=-\dfrac{3}{4}A\hbar^2\ket{1} & 
H_0\ket{2}&=A\dfrac{\hbar^2}{2}\left(2-\dfrac{3}{2}\right)\ket{2}=+\dfrac{1}{4}A\hbar^2\ket{2} \\
H_0\ket{3}&=A\dfrac{\hbar^2}{2}\left(2-\dfrac{3}{2}\right)\ket{3}=+\dfrac{1}{4}A\hbar^2\ket{3} & 
H_0\ket{4}&=A\dfrac{\hbar^2}{2}\left(2-\dfrac{3}{2}\right)\ket{4}=+\dfrac{1}{4}A\hbar^2\ket{4}
\end{align}$$
These are all eigenstates of the Hamiltonian, and so in summary:
$$\begin{align}
E_1&=-\dfrac{3}{4}A\hbar^2 & 
\ket{1}&=\dfrac{1}{\sqrt{2}}\left(\ket{+-}-\ket{-+}\right)\\
E_2&=+\dfrac{1}{4}A\hbar^2 & 
\ket{2}&=\ket{--}\\
E_3&=+\dfrac{1}{4}A\hbar^2 & 
\ket{3}&=\dfrac{1}{\sqrt{2}}\left(\ket{+-}+\ket{-+}\right)\\
E_4&=+\dfrac{1}{4}A\hbar^2 & 
\ket{4}&=\ket{++}
\end{align}$$
The coupled basis makes this system trivial because of the dot product depending on $\vec{J}^2$ and the individual magnitude squared of each component spin.

---
### Problem 3.B
Use degenerate or non-degenerate perturbation theory (higher-order if necessary) in the appropriate subspaces to obtain the lowest-order non-vanishing corrections to the energy levels.

From our eigenstate basis in [[#Problem 3.A]], we see a three-fold degeneracy for $j=1$ states. We want to similarly represent the perturbation in this basis.

If we apply our perturbation operation on a general state (uncoupled), we see that:
$$\begin{align}
V\ket{m_1m_2}
&=\dfrac{eB}{mc}\left(S_{1z}\ket{m_1}\ket{m_2}-\ket{m_1}S_{2z}\ket{m_2}\right)\\
&=\dfrac{eB\hbar}{mc}\left(m_1-m_2\right)\ket{m_1m_2}
\end{align}$$
These are eigenvalues associated with each uncoupled state:
$$\begin{align}
E_{--}&=0 & E_{+-}&=+\dfrac{eB\hbar}{mc} & E_{-+}&=-\dfrac{eB\hbar}{mc} & E_{++}&=0
\end{align}$$



States $\ket{2},\ket{4}$ are trivial since they are the same as each spin pointing in the same direction. However, for states $\ket{1},\ket{3}$, the application of the perturbation on each uncoupled basis component results in the following:
$$\begin{align}
V\ket{1}&=\dfrac{eB\hbar}{mc}\ket{3} & V\ket{3}&=\dfrac{eB\hbar}{mc}\ket{1}\\
\end{align}$$
Therefore, in the coupled basis, we can represent the operation as:
$$\begin{align}
V&=\dfrac{eB\hbar}{mc}\left(\ket{3}\bra{1}+\ket{1}\bra{3}\right)
\end{align}$$
The diagonal of this the perturbation is all $0$s, so there is no first-order energy correction.

As for the second-order energy corrections, the matrix simplifies immensely. Our state $\ket{1}$ is of different energy as the others, and so we can use the non-degenerate equation:
$$\begin{align}
E_1^{(2)}
&=\dfrac{\left|\bra{3}V\ket{1}\right|^2}{E_1^{(0)}-E_3^{(0)}}\\
&=-\dfrac{1}{A\hbar^2}\left|\dfrac{eB\hbar}{mc}\right|^2\\
\Aboxed{E_1^{(2)}&=-\dfrac{e^2B^2}{Am^2c^2}}
\end{align}$$
State $\ket{3}$ can also be done in this subspace since it doesn't couple with $\ket{2},\ket{4}$, and so:
$$\begin{align}
E_3^{(2)}
&=\dfrac{\left|\bra{1}V\ket{3}\right|^2}{E_3^{(0)}-E_1^{(0)}}\\
&=+\dfrac{1}{A\hbar^2}\left|\dfrac{eB\hbar}{mc}\right|^2\\
\Aboxed{E_3^{(2)}&=+\dfrac{e^2B^2}{Am^2c^2}}
\end{align}$$
Therefore, all together, we have the following energies of each coupled state:
$$\begin{align}
E_1&=-\dfrac{3}{4}A\hbar^2-\dfrac{e^2B^2}{Am^2c^2} & 
\ket{1}&=\dfrac{1}{\sqrt{2}}\left(\ket{+-}-\ket{-+}\right)\\
E_2&=+\dfrac{1}{4}A\hbar^2 & 
\ket{2}&=\ket{--}\\
E_3&=+\dfrac{1}{4}A\hbar^2+\dfrac{e^2B^2}{Am^2c^2} & 
\ket{3}&=\dfrac{1}{\sqrt{2}}\left(\ket{+-}+\ket{-+}\right)\\
E_4&=+\dfrac{1}{4}A\hbar^2 & 
\ket{4}&=\ket{++}
\end{align}$$
<div style="page-break-before: always;"></div>



## Problem 4
A particle of mass $m$ and energy $E>0$ moves in one dimension through an infinite series of equally-spaced $\delta$-function potentials:
$$\begin{align}
V(x)&=\dfrac{\hbar^2}{2m}\lambda\sum_{n=-\infty}^\infty\delta(x-na), &&& (\lambda>0).
\end{align}$$
---
### Problem 4A
Derive the proper continuity or discontinuity for $\psi(x)$ and $d\psi/dx$ at $x=0$.

I had a bit of difficulty writing this in a coherent way. There were many different ways I could talk about it and prove it, but I'll use my what I learned in my undergraduate quantum class.

At the point $x=0$, the Hamiltonian in position representation takes the following form:
$$\begin{align}
H&=-\dfrac{\hbar^2}{2m}\dfrac{d^2}{dx^2}+\dfrac{\hbar^2}{2m}\lambda\delta(x)
\end{align}$$
Applying this to a general state $\psi(x)$, we can integrate over a small interval $|x|<\epsilon\ll a$ :
$$\begin{align}
H\psi(x)&=-\dfrac{\hbar^2}{2m}\dfrac{d^2}{dx^2}\psi(x)+\dfrac{\hbar^2}{2m}\lambda\delta(x)\psi(x)\\
\lim_{\epsilon\to0^+}\int_{-\epsilon}^{+\epsilon} E\psi(x)\ dx&=-\dfrac{\hbar^2}{2m}\lim_{\epsilon\to0^+}\int_{-\epsilon}^{+\epsilon}\psi''(x)\ dx+\dfrac{\hbar^2}{2m}\lambda\lim_{\epsilon\to0^+}\int_{-\epsilon}^{+\epsilon}\delta(x)\psi(x)\ dx\\
0&=-\dfrac{\hbar^2}{2m}\left(\lim_{\epsilon\to0^+}\psi'(\epsilon)-\lim_{\epsilon\to0^-}\psi'(\epsilon)\right)+\dfrac{\hbar^2}{2m}\lambda\psi(0)\\
\lambda\psi(0)&=\lim_{\epsilon\to0^+}\psi'(\epsilon)-\lim_{\epsilon\to0^-}\psi'(\epsilon)
\end{align}$$
Therefore any discontinuity in the slope of the wavefunction is directly related to $\lambda$.

As for the continuity of the general wavefunction, I had originally written steps with limits and using calculus to prove that the function must be continuous at $x=0$. We can exploit that the full expression for the potential has discrete translation symmetry:
$$\begin{align}
V(x+a)&=V(x)
\end{align}$$
Whatever solution we get for the wavefunction of this potential, the state must also be continuous at the boundaries since the left-side wavefunction approaching $\psi(a)$ is equivalent to $\psi(0)$ by translation, and thus the wavefunction is continuous. 
<div style="page-break-before: always;"></div>



Writing the wavefunction continuity as a limit equation, we can write both conditions as:
$$\begin{align}
\Aboxed{\lim_{\epsilon\to0^+}\psi(\epsilon)-\lim_{\epsilon\to0^-}\psi(\epsilon)&=0} &
\Aboxed{\lim_{\epsilon\to0^+}\psi'(\epsilon)-\lim_{\epsilon\to0^-}\psi'(\epsilon)&=\lambda\psi(0)}
\end{align}$$
We can also extend these for all potential spikes since they are periodic:
$$\begin{align}
\lim_{x\to na^+}\psi(\epsilon)-\lim_{x\to na^-}\psi(\epsilon)&=0 &
\lim_{x\to na^+}\psi'(\epsilon)-\lim_{x\to na^-}\psi'(\epsilon)&=\lambda\lim_{x\to na}\psi(x) &
n\in\mathbb{Z}
\end{align}$$
In terms of rewriting limits as explicit values inside the wavefunction, which is *technically* abuse of notation, more succinctly gets the point across:
$$\begin{align}
\Aboxed{\psi(na^+)-\psi(na^-)&=0} &
\Aboxed{\psi'(na^+)-\psi'(na^-)&=\lambda\psi(na)} &
n\in\mathbb{Z}
\end{align}$$
Physically, these conditions enforce that the wavefunction is continuous across the potential barrier spike and that the slope of the wavefunction can jump discontinuously, but that such discontinuity must be equal to $\lambda$ times the value of the wavefunction at that point.

---
### Problem 4B
Write $\psi(x)=Ae^{ik'x}+Be^{-ik'x}$ for $-a<x<0$, where $k'=\sqrt{2mE}/\hbar$. Use Bloch's Theorem, $\psi(x+a)=e^{ika}\psi(x),\ k\in\mathbb{R}$ , to derive an expression for $\psi(x)$ in the region $0<x<a$.

We are given the wavefunction ANSATZ:
$$\begin{align}
\psi(x)&=Ae^{ik'x}+Be^{-ik'x}
\end{align}$$
If this equation is value for the interval $-a<x<0$, if we let $x\to x-a$, then the interval becomes:
$$\begin{align}
-a<x-a&<0 &\implies&&0<x&<a
\end{align}$$
Bloch's Theorem for this shift is similar, and takes the following form:
$$\begin{align}
\psi(x-a)&=e^{-ika}\psi(x)
\end{align}$$
We can also manually make the substitution $x\to x-a$ into our ANSATZ:
$$\begin{align}
\psi(x-a)&=Ae^{ik'(x-a)}+Be^{-ik'(x-a)} &\implies&& e^{-ika}\psi(x)&=(Ae^{-ik'a})e^{ik'x}+(Be^{ik'a})e^{-ik'x}
\end{align}$$
Dividing both sides by the exponential attached to the wavefunction, we find:
$$\begin{align}
\Aboxed{\psi(x)&=(Ae^{i(k-k')a})e^{+ik'x}+(Be^{i(k+k')a})e^{-ik'x}}
\end{align}$$
<div style="page-break-before: always;"></div>



### Problem 4C
Using your result from [[#Problem 4A]] and [[#Problem 4B]], obtain the equation which provides the allowed values of $k'$. Show that this equation implies a *band structure*.

The shared point in problem 4B is $x=0$, so we'll want to look at the behavior there. Once again, because of discrete translation symmetry, this is universal for the whole system.

Approaching $x=0$ from the left side $(x\to0^-)$, the wavefunction and its derivative are:
$$\begin{align}
\lim_{x\to0^-}\psi(x)&=Ae^{+ik'0}+Be^{-ik'0}=A+B \\
\lim_{x\to0^-}\psi'(x)&=ik'\left(Ae^{+ik'0}-Be^{-ik'0}\right)=ik'(A-B)
\end{align}$$
Similarly, approaching $x=0$ from the right, we see:
$$\begin{align}
\lim_{x\to0^+}\psi(x)
&=(Ae^{i(k-k')a})e^{ik'0}+(Be^{i(k+k')a})e^{-ik'0}
=Ae^{i(k-k')a}+Be^{i(k+k')a} \\
\lim_{x\to0^+}\psi'(x)
&=ik'\left((Ae^{i(k-k')a})e^{ik'0}-(Be^{i(k+k')a})e^{-ik'0}\right)
=ik'\left(Ae^{i(k-k')a}-Be^{i(k+k')a}\right)
\end{align}$$
Using the two conditions from part 4A and rearranging, we find that:
$$\begin{align}
A\left(e^{i(k-k')a}-1\right)+B\left(e^{i(k+k')a}-1\right)&=0\\
A\left(ik'e^{i(k-k')a}-ik'-\lambda \right)-B\left(ik'e^{i(k+k')a}-ik'+\lambda \right)&=0
\end{align}$$
If we imagine $A,B$ the components of a vector, then we have a matrix times a vector becoming the null vector, and since $A=B=0$ is the trivial solution, then this matrix needs to have a determinant of $0$. Since it's a 2x2 matrix, it's pretty easy to calculate:
$$\begin{align}
0&=\left(e^{i(k-k')a}-1\right)\left(ik'e^{i(k+k')a}-ik'+\lambda\right)+\left(e^{i(k+k')a}-1\right)\left(ik'e^{i(k-k')a}-ik'-\lambda\right)\\\\
&=\left(ik'e^{i(k-k')a}e^{i(k+k')a}-e^{i(k-k')a}ik'+\lambda e^{i(k-k')a}\right)+\left(-ik'e^{i(k+k')a}+ik'-\lambda\right)\\
&+\left(ik'e^{i(k+k')a}e^{i(k-k')a}-ik'e^{i(k+k')a}-\lambda e^{i(k+k')a}\right)+\left(-ik'e^{i(k-k')a}+ik'+\lambda\right)\\\\
&=4ik'e^{ika}\dfrac{e^{ika}+e^{-ika}}{2}-4ik'e^{ika}\dfrac{e^{ik'a}+e^{-ik'a}}{2}-2i\lambda e^{ika}\dfrac{e^{ik'a}-e^{-ik'a}}{2i}\\
\Aboxed{0&=\cos\left(ka\right)-\cos\left(k'a\right)-\dfrac{\lambda}{2k'} \sin\left(k'a\right)}
\end{align}$$
The condition that $k'$ must satisfy is a lot nicer than I expected, and takes the form:
$$\begin{align}
\Aboxed{\cos\left(ka\right)&=\cos\left(k'a\right)+\dfrac{\lambda a}{2(k'a)} \sin\left(k'a\right)}
\end{align}$$



As for why this implies band structure? I can definitely see that there is a lot of solutions to this system. Cosine is bounded by $\pm1$, so we can see the boundary on the other side as:
$$\begin{align}
-1\le\cos\left(k'a\right)+\dfrac{\lambda a}{2(k'a)} \sin\left(k'a\right)\le 1
\end{align}$$
There are some values of $k'$ that are allowed, and others who are not. In the case of no potential, we *technically* have a band structure, it's just one huge band that spans all momentum eigenstates. However, when we add in this periodic potential, the new sine term shifts solutions that once were valid just a little too high, and thus those solutions are no longer valid.

What I found interesting is that any infinitesimal potential causes countably infinite invalid momentum eigenstates to appear, and splits from a single-degeneracy gap value into a double-degeneracy gap in momentum space because of the extremal value of cosine. I.e. when the cosine is exactly $\pm1$, there is only **one** disallowed momentum eigenstate every $\pi$ radians. Any infinitesimal choice of $\lambda$ instantaneously disallows **two** disallowed momentum eigenstates every $\pi$ radians.

Also, we can actually simplify this condition more, surprisingly. All the way back in my 10th grade, I had been messing around in Desmos and stumbled upon a way to add a $\sin$ and $\cos$ of the same input, even with different magnitudes from triangles. The equation I wrote was the following:
$$\begin{align}
A\cos\left(x\right)+B\sin\left(x\right)&=\sqrt{A^2+B^2}\sin\left(x+\tan^{-1}\left(\dfrac{A}{B}\right)\right)
\end{align}$$
This actually also works with $A,B$ being functions of $x$, but you do have to note that the equation might require a $\operatorname{sgn}\left(x\right)$ depending on the odd and evenness of $A$ and $B$. For our condition, the equation simplifies to the following (verified with Desmos):
$$\begin{align}
-1\le\sqrt{1+\dfrac{(\lambda a)^2}{4(k'a)^2}}\sin\left(k'a+\tan^{-1}\left(2\dfrac{k'a}{\lambda a}\right)\right)\operatorname{sgn}\left(k'a\right)\le 1
\end{align}$$
Given the symmetry of the system, it's actually perfect to take its absolute value:
$$\begin{align}
\left|\sqrt{1+\dfrac{(\lambda a)^2}{4(k'a)^2}}\sin\left(k'a+\tan^{-1}\left(2\dfrac{k'a}{\lambda a}\right)\right)\left(k'a\right)\right|\le 1
\end{align}$$
If you're interested, [here](https://www.desmos.com/calculator/qslxslbuxg) is my graph I used to talk about this condition. I also use this graph in problem 4D and it was a lot of fun to make it since it's interactive!
<div style="page-break-before: always;"></div>



### Problem 4D
Set $\lambda a=40$, and *obtain numerical values* for the lower and upper boundaries of $k'a$ for the first five energy bands. Use a computer to plot the band structure.

From [[#Problem 4C]], we have the following condition:
$$\begin{align}
-1\le\cos\left(k'a\right)+\dfrac{\lambda a}{2(k'a)} \sin\left(k'a\right)\le 1
\end{align}$$
If I remember correctly, the $ka,k'a$ products are called reduced wavevectors or something like crystal momentum. Since the condition is over all momentum eigenstates $\ket{\kappa}$ and gets truncated with higher values of $\lambda a$, let $\boxed{\kappa=k'a}$ so that $\kappa$ is the nondimensionalized parameter of allowed momentum eigenstates (makes graphing much easier and more stable). Using this new parameter, and the problem's value for $\lambda a$, our condition to plot is: 
$$\begin{align}
\left|\cos\kappa+20\dfrac{\sin\kappa}{\kappa}\right|&\le1 &&& (\kappa&=k'a)
\end{align}$$
For an interactive graph for this problem, I made a Desmos graph [here](https://www.desmos.com/calculator/qslxslbuxg). As for finding the actual bands, I wrote a small python program for finding zeros of the following equations:
$$\begin{align}
\cos\kappa+20\dfrac{\sin\kappa}{\kappa}-1&=0 &&& \cos\kappa+20\dfrac{\sin\kappa}{\kappa}+1&=0
\end{align}$$
Since the band structure is symmetric in $k\to-k$, I only had to guess from the positive side and then reflect it. In the case of no potential, being $\lambda a=0$, we expect extremes at $\kappa=n\pi$. For $0<\lambda a\ll1$, the extremes split in two centered at $\kappa=n\pi$, so when I implemented my zeros algorithm, I had it run twice with a $\pm d\kappa$ offset to start so I'd capture both sides of the bands.

The question asks for the first 5 bands, so I ran 10 zeros-searches on $\kappa=n\pi\pm d\kappa$ for $n=1,\dots,5$, alternating the search between the $+1$ and $-1$ critical value. A table of my findings are below:

| Band # | Raw Interval ($\kappa=ka$)         | Band Interval ($ka$) | Band Size ($ka$) |
| ------ | ---------------------------------- | -------------------- | ---------------- |
| 1      | $(02.857740022428,03.14159265359)$ | $(2.8578,3.1415)$    | $0.2838$         |
| 2      | $(05.725545175030,06.28318530718)$ | $(5.7256,6.2831)$    | $0.5576$         |
| 3      | $(08.611602826237,09.42477796077)$ | $(8.6117,9.4247)$    | $0.8131$         |
| 4      | $(11.521115865418,12.56637061436)$ | $(11.5212,12.5663)$  | $1.0452$         |
| 5      | $(14.456219543254,15.70796326795)$ | $(14.4563,15.7079)$  | $1.2517$         |



Graphically, in [Desmos](https://www.desmos.com/calculator/qslxslbuxg), this is what it appeared as:
![[bandgaps.png]]
Normally I would have plotted it in another software, but I am very tired. It was really fun to do this problem though, it's very interesting.

**End of Document**