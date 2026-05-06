### Spring 2026 - Colloquium 10
**Author:** Stanley Goodwin
**Date:** April 8th, 2026

---
**Title:** *First-principles Prediction of Spin Relaxation, Dephasing and Transport From Density-Matrix Dynamics*
**Speaker:** *Joshua Quinton, Ph.D.* | Newly Graduated, Rensselaer Polytechnic Institute
**Understanding:** <u>High</u>

---
> Briefly describe in words the key concepts of the talk that interested you or if you did not find the talk interesting, why it was not interesting to you.

I found it interesting they use sampling from DFPT with the matrix model to reproduce $T_1$ and $T_2^*$, as well as $T_2$. Spin relaxation has always been a weird interest of mine. I also appreciated the three regimes for the behaviors, and it's quite interesting the intermediate region flatlines for a while. It was also cool to see Perturbation Theory being used in practice.

---
> If you were the speaker what would you do differently?

Not sure. He was very well spoken and his graphics were very nice. The only thing I had noticed is that he filled a lot of the time with "umm" and "uhh" but that seems to be more of an artifact of inexperience in presentation.


<div style="page-break-before: always;"></div>*PDF next page*

#### Abstract
Improved methods for manipulating and detecting spin in materials are needed for advancing the state of the art in spintronics, quantum computing, and quantum information science. Modeling spin properties from first principles allows us to find materials with desirable properties such as long spin lifetimes and strong spin orbit coupling. This work develops new methods for modeling spin dynamics and transport from first principles which are highly versatile and successfully predict properties for a wide range of systems and phenomena. Using density-matrix dynamics, we can predict spin lifetimes in materials and examine non-trivial dependence from external magnetic fields. The interplay of reversible and irreversible spin relaxation processes leads to a complex dependence of spin lifetimes on the direction and magnitude of magnetic fields, relevant for spintronics and quantum information applications. In addition to spin dynamics, we also model spin transport. We introduce a computational framework for first-principles density matrix transport within the Wigner function formalism to predict transport of quantum-mechanical degrees of freedom such as spin over long time and length scales.  This framework facilitates simulation of spin dynamics and transport from first principles, while accounting for electron-phonon scattering at device length scales. Overall, these frameworks are highly general, i.e. not constrained to any specific Hamiltonians, and accurately account for the electron-electron and electron-phonon interactions which dominate spin properties. Ultimately, these approaches expand the set of materials and spin-relevant phenomena that can be studied from first-principles.


<div style="page-break-before: always;"></div>*PDF next page*

#### Notes
 - Spin orbit coupling induces spin mix, momentum scattering May cause spin flip 
	 - Relax Time ~ $k$
 - DP mechanism: Band structure, momentum scatter randoms spin precession behavior
	 - Relax Time ~ $1/k$

Temperature Dependent Effects
- DFT, Perturbation for photons. These methods fail for complex systems like Perovskites
- Effective potential for temperature work well for the method.

High Frequency Phonon Correlation
- Combine molecular trajectory with perturbations sampled from DFPT, he corrects the classical amplitude from the quantum effect, which match nicely.

Dephasing, measuring $T_2$
 - Phonons in complex materials work now from above, now we calc $T_2$.
 - They look at time scale a spin relaxes when it precesses in an external field.
 -  $T_2^*$ has both reversible and irreversible effects

Hamiltonian contains both $L$ and $S$ spin vector, with explicit $g_0$ for $g$-factor Tensor
 - $L$ momentum dependent so g fluctuates so de-phases. 
 - $g$ is not necessarily diagonal.

$T_2$ saturates as Larmor precession approaches momentum scattering timescale (DP-like behavior)
 - Spin scattering changes axis over and over and will eventually randomize. Statistical.
 - Detailed model of relaxation time in terms of the statistics of g-factor!

$T_1$, $T_2$, and $T_2^*$ have nontrivial magnetic field interactions due to g fluctuations.

Spin Transport
 - Wigner function transform -> well model spin transport and statistics thereof.

Lindbladian Scattering (electron phonon)
 - Spatial transport requires a gradient of density functional from Wigner function.

Coherent transport (ballistic)
 - Dephasing stats have differing paths. Phase cancel out at greater distance.
 - Internal B field is k-dependent.
 - Precession compensates for different path lengths, weak dephasing.

Incoherent Transport
 - Out of plane E field, spin life time dependent on spin scattering rate.
 - Like adjusting temperature, 3 different regimes. 
	 - Low scale, free induction. Weak scattering, multiple precession per scatter. Weak effect. 
	 - Mid scale, scatter rate on order of precession, increase spin lifetime. 
	 - High scale, flip increases with spin.
 - We can calculate spin diffusion length. How far does this spin propagate in.
	 - Free induction (length decreases). DP regime scatter length is FIXED from cancelling increase/decrease of effects. At EY regime, length decreases and tau increases.

Transport With Perturbations 
 - Same as before + New Perturbation, using $\left[\hat{H},\rho\right]$ operator
 - We expect Zeeman effect (short), and a classical Lorentz force (long). 
 - We need a semi-local approximation. $\rho$ from $E$ field contribution time evolution is prop to $k$ space advection and coherent evolution.
 - Phase and degenerate subspaces have difficult between nearby $k$ points. 
 - He was careful in account for this effect.

Testing k advection in GaAs, good agreement. 
 - There are spin dependent effects like Rashba-Edelstein effect.
 - We have an uneven splitting with tilting the Fermi surface, the momentum is linked to orthogonal effects (y in x and x in y)
 - This effect can be seen on nonlocal transport geometry. Results agree with literature.

In the future
 - Boundary conditions (diffusive or spec)
 - Mag field contributions
 - Nonlocal spin effects (Spin-Hall effect)
