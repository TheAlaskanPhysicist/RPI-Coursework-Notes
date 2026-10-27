We begin with the start of the Heisenberg Model with the constraints that the spins are being measured in the $z$-basis, and the magnetic field is transverse, and so $H=h\sigma^x$.
$$\begin{align}
H&=-J\sum_j\sigma^z_{j}\sigma^z_{j+1}-h\sum_j\sigma^x_{j}+\sum_{j,k}f_{\left|j-k\right|}\sigma^x_{j} \sigma^x_{k}
\end{align}$$
How to solve this system:


Temperature in 2D Ising is akin to Transverse Field Strength of 1D Heisenberg.




### Notes from Meeting 10/6

Let's look at these different system individually
#### Dipole interaction only
$$\begin{align}
H&=-J\sum_j\sigma^z_{j}\sigma^z_{j+1}
\end{align}$$
For this system, these are only the couplings that exist between the different spins, and thus they will all want to align in the case of $T=0$ since there's no perturbation.
There are 2 eigenstates and eigenvalues:
$$\begin{align}
\psi_+&=\ket{\uparrow\uparrow\uparrow\dots\uparrow}+\text{small fluctuations}\\
\psi_-&=\ket{\downarrow\downarrow\downarrow\dots\downarrow}+\text{small fluctuations}\\
\end{align}$$
They have identical energies:
$$\begin{align}
E_+&=E_-
\end{align}$$
Since there are no other contributions to the Hamiltonian.

The magnetization transition for this system is a first-order transition.
It is discontinuous when the free energy is equal to that of the $T=0$ state.

#### Magnetic Field Interaction only
$$\begin{align}
H&=-h\sum_j\sigma^x_{j}
\end{align}$$
What we see is there is a spontaneous magnetization with any amount of field $h$.
This will only have 1 eigenstate and eigenvalue:
$$\begin{align}
\psi_0&=\ket{+++\dots+}\ +\text{small fluctuations}\\
\end{align}$$
#### The Ising Model
For a typical Ising model, there's a contest between both terms that result in 
$$\begin{align}
H&=-J\sum_j\sigma^z_{j}\sigma^z_{j+1}-h\sum_j\sigma^x_{j}
\end{align}$$
For low fields $h$, we see the same characteristics of it by itself.

There are 2 eigenstates and eigenvalues:
$$\begin{align}
\psi_+&=\ket{\uparrow\uparrow\uparrow\dots\uparrow}+\text{small fluctuations}\\
\psi_-&=\ket{\downarrow\downarrow\downarrow\dots\downarrow}+\text{small fluctuations}\\
\end{align}$$
They have identical energies:
$$\begin{align}
E_+&=E_-
\end{align}$$

For strong $h$, we can neglect dipole-dipole interactions, and so we see:
$$\begin{align}
\psi_0&=\ket{+++\dots+}\ +\text{small fluctuations}\\
\end{align}$$

This system has a 2nd-order transition of magnetization.
At low $h$, the dipoles strongly couple, so $\braket{\mu_z}=\pm|s|$.
At high $h$, the dipoles align with the transverse magnetic field, so $\braket{\mu_z}=0$.


### The Transverse Coupling
Start with the Hamiltonian:
$$\begin{align}
H&=-J\sum_j\sigma^z_{j}\sigma^z_{j+1}-h\sum_j\sigma^x_{j}+\sum_{j,k}f_{\left|j-k\right|}\sigma^x_{j} \sigma^x_{k}
\end{align}$$
We want to know the characteristics of the mean magnetization of this system.

We also know for the case of $f_{\left|j-k\right|}=0$, we recover that of the typical Ising Model.

However, what we want to show is that we can induce a mixed-order transition in state-space.
 - That's the whole point of the paper.

We want to eventually develop a deeper theory as to why this is the way it is.



### The Project
We want to construct this Hamiltonian using matrices and Qiskit.
We want to evolve an initial state $\ket{\uparrow\uparrow\uparrow\dots\uparrow}$ through time steps to get a sense of the dynamics of the system over time.

We choose a transverse magnetic field $h<h_\text{critical}$, but $h-h_\text{critical}\approx 0^{-}$ (just under spontaneous):
$$\begin{align}
\ket{\psi(t)}&=e^{-i\hat{H}t/\hbar}\ket\psi
\end{align}$$
Under a small field $h$ we expect that the state won't change much over time, and have a small amount of the state go away from the initial.

Then we start to add in the coupling constant $f_{\left|j-k\right|}$, a small amount, in order to see if we can induce a system where we have a mixed-transition state.
 - $\braket{\mu_z}$ has a  2nd order transition up until a critical point $h=a^-$, then there's a discontinuous 1st order transition to the ground state at $h=a^-$, then $\braket{\mu_z}=0$ as expected.

