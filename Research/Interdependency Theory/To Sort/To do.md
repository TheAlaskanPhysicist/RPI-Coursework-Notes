





### Things I'm plotting

**Ground State Energy vs H/J**
The average ground state energy per site.
$$\begin{align}
E_0(H)&=\bra{\psi_0}\hat{H}\ket{\psi_0}
\end{align}$$
**Energy Gap vs H/J**
The difference in energy between the two lowest eigenstates.
 - Calculate the eigenvalue decomp. Find difference of energy.
 - Return as scalar.
$$\begin{align}
\Delta(H)&=E_1-E_0
\end{align}$$
**Ground State Average Spontaneous (Longitudinal) Magnetization vs H/J**
$$\begin{align}
\braket{\hat{M}^z}&=\dfrac{1}{N}\sum_{i=1}^N\braket{\sigma_i^z}
\end{align}$$
**Ground State Average Induced (Transverse) Magnetization vs H/J**
$$\begin{align}
\braket{\hat{M}^x}&=\dfrac{1}{N}\sum_{i=1}^N\braket{\sigma_i^x}
\end{align}$$
**Two-Point Correlation Function vs Index Distance**


**Correlation Length vs Field**


**Susceptibility vs Field**


**Entanglement Entropy vs Field**






### Transverse Field Quantum Ising Model
Hamiltonian
$$\begin{align}
\hat{H}&=-J\sum_{\braket{i,j}} \sigma_i^z\sigma_j^z - H\sum_{i}\sigma_i^x
\end{align}$$
Spontaneous Magnetization (at $T=0$)



Induced (Transverse) Magnetization (at $T=0$)

This will be the graph of $\braket{\hat{M}^x}$ vs $H/J$ at $T=0$.
 - Non-zero on both sides of the critical field
 - Derivative is singular at $H=H_c$

Transverse Susceptibility (at $T=0$)
$$\begin{align}
\chi&=\dfrac{\partial\braket{\hat{M}^x}}{\partial H}
\end{align}$$
This will be the graph of $\chi$ vs $H/J$ at $T=0$.
 - This diverges at $H=H_c$, as expected.



$\bra{\text{First Excited}}\sigma_z\ket{\text{Ground State}}=\text{Spontaneous Magnetization}$.









PV Diagram?

Two-Point Correlation Function
Isothermal compressibility




Things I want to calculate:
 - The Hamiltonian (definition)
 - Partition function $Z(T,H,N)$
 - Helmholtz free energy $F(T,H,N)=-kT\ln Z(T,H,N)$
 - Free energy per spin $f(T,H)=F(T,H,N)/N$
 - Average magnetization $m(T,H)=\dfrac{1}{N}\dfrac{\partial}{\partial(\beta H)}Z(T,H,N)=\dfrac{\partial}{\partial H}f(T,H)$



Ising Model Specific:
Magnetization vs Temperature ($|m|$ vs $T$)
 - Critical Temperature at $|m|=0$ min temperature.
Spontaneous Magnetization
 - $\lim_{H\rightarrow0}m(T,H)$
 - High temperatures $\rightarrow$ 1 solution ($m=0$ stable)
 - Low temperatures $\rightarrow$ 3 solutions ($m=0$ unstable, $m=\pm m_c$ stable)
Variational free energy
 - Equilibrium will result in a magnetization that minimizes var. free energy.
 - The critical magnetic field results in a saddle point at one of the typical minima.
Correlation Length



Magnetic Susceptibility (Zero-Field Magnetization Limit)
$$\begin{align}
\chi&=\lim_{H\rightarrow0}\dfrac{\partial m}{\partial H}
\end{align}$$









### Quantum Ising Model
Start with the Hamiltonian:
$$\begin{align}
\hat{H}&=-J\sum_{\braket{i,j}} \sigma_i\sigma_j - gJ\sum_{i}\sigma_i
\end{align}$$
With probability of state:
$$\begin{align}
P(\ket{\psi})&=\dfrac{1}{Z}e^{-\beta\hat{H}[\psi]}
\end{align}$$





### Paramagnetic Limit ($J\rightarrow0$)
The Hamiltonian:
$$\begin{align}
\hat{H}&=-gJ\sum_{i}\sigma_i
\end{align}$$
The mean magnetization:
$$\begin{align}
\braket{m}&=m(T,H)\\
\lim_{H\rightarrow0}m(T,H)&=0 \ \forall T
\end{align}$$
### Ferromagnetic Limit ($g\rightarrow0$)
The Hamiltonian:
$$\begin{align}
\hat{H}&=-J\sum_{\braket{i,j}} \sigma_i\sigma_j
\end{align}$$
The mean magnetization:
$$\begin{align}
\lim_{H\rightarrow0}m(T,H)&=\begin{cases}
0,&T>T_c\\
\pm m(T),&T\le T_c\\
\end{cases}
\end{align}$$
