

Intent: When I was a student I was frustrated with how disconnected a lot of topics are, and absolutely hated Jackson's electrodynamics since it was not a competent tool to teach from.
I wanted to make a book that was both useful when an expert and also a student guide into thinking abstractly to formulate theoretical physics like this.






## Chapter 1: Electromagnetic Fields
Electromagnetism is a cause-response theory between electromagnetic charge/current sources and their associated electromagnetic fields.

### Electromagnetic Charge & Current
The most fundamental discretization of charge and current is a moving point charge, historically referenced to as an *electric monopole*. There is also, in principle, another type of point-like charge—the *magnetic monopole*—which would act as a "magnetic charge." However, due to the well-established absence of  experimental evidence for such particles, we will ignore them in this section. Magnetic monopoles will be discussed in a separate, purely theoretical section later, where we explore their implications based on the same formalism developed here.

Utilizing the Dirac delta distribution, the electric charge and electric current (hereafter referred to simply as charge and current) densities associated with a point particle of charge $q$ are:
$$\begin{align}
\rho(\vec{r},t)&=q\ \delta\left(\vec{r}-\vec{r}_0(t)\right) && \text{(S1.1)} &
\vec{J}(\vec{r},t)&=q\ \vec{v}_0(t)\ \delta\left(\vec{r}-\vec{r}_0(t)\right) && \text{(S1.2)}
\end{align}$$
Here, $q$ is the *electric charge* scalar, representing the "strength" of the particle's electromagnetic presence in vacuum, $\vec{r}_0(t)$ is the position of the particle, and $\vec{v}_0(t)=\dot{\vec{r}}_0(t)$ is its velocity.

---
#### Conservation of Charge
From these definitions of a point particle's charge and current, we can examine their time and space variations directly. Suppose we differentiate the charge density with respect to time:
$$\begin{align}
\dfrac{\partial\rho}{\partial t}(\vec{r},t)&=\dfrac{\partial}{\partial t}\left[q\ \delta\left(\vec{r}-\vec{r}_0(t)\right)\right]=-q\vec{v}_0(t)\cdot\vec\nabla\delta\left(\vec{r}-\vec{r}_0(t)\right) && \text{(S1.3)}
\end{align}$$
Similarly, taking the divergence of the current density yields:
$$\begin{align}
\vec{\nabla}\cdot\vec{J}(\vec{r},t)&=\vec{\nabla}\cdot\left[q\ \vec{v}_0(t)\ \delta\left(\vec{r}-\vec{r}_0(t)\right)\right]=+q\vec{v}_0(t)\cdot\vec\nabla\delta\left(\vec{r}-\vec{r}_0(t)\right) && \text{(S1.4)}
\end{align}$$
Notice that these two contributions are equal in magnitude, but opposite in sign. Adding equations $\text{S1.3}$ and $\text{S1.4}$ gives:
$$\begin{align}
\dfrac{\partial\rho}{\partial t}(\vec{r},t)+\vec{\nabla}\cdot\vec{J}(\vec{r},t)&=0 && \text{(S1.5)}
\end{align}$$
This relation is known as the *continuity equation*. It expresses a local property at every point in space: the rate of change of charge at a point is exactly balanced by the next current flowing into or out of that point.

---
### Electromagnetic Forces and Fields
To study the motion of charges and currents, we begin by examining the *forces* that act on individual point particles. These forces determine how charges move through space, connecting the presence of charge and current to measurable electromagnetic effects.

---
#### Point Charges: Instantaneous Forces
The first description of the interaction between stationary point charges is Coulomb's law, formulated in the late 18th century. A point charge $q$ at position $\vec{r}$ in the presence of another stationary charge $q'$ at position $\vec{r}'$ experiences a force:
$$\begin{align}
\vec{F}_{E}(\vec{r})&=\dfrac{qq'}{4\pi\epsilon_0}\cdot\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3} && \text{(S1.6, J1.2)}
\end{align}$$
For moving charges, there is a magnetic analogue to Coulomb's law. A point charge $q$ moving at velocity $\vec{v}$ in the presence of another moving charge $q'$ with velocity $\vec{v}'$ experiences a force:
$$\begin{align}
\vec{F}_{B}(\vec{r})&=\dfrac{\mu_0(q\vec{v}\times q'\vec{v}')}{4\pi}\times\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3} && \text{(S1.7)}
\end{align}$$
The magnetic force can also be expressed in a form directly analogous to Coulomb's law:
$$\begin{align}
\vec{F}_{B}(\vec{r})&=\dfrac{\mu_0\vec{j}\times\vec{j}'}{4\pi}\times\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}, \ \ \ \ \vec{j}=q\vec{v} && \text{(S1.8)}
\end{align}$$
These forces are structurally very similar: both depend on the "strength" of the sources (charge or current) and the relative position vector $\vec{r}-\vec{r}'$, with the magnetic force additionally depending on the velocities and acting in a direction generally perpendicular to motion.

It is important to note that these expressions describe *instantaneous interactions only*, as these are only valid for charges moving at constant velocity. If either charge accelerates the forces are no longer fully captured by these formulas, because accelerating charges emit electromagnetic radiation. The complete dynamics of accelerating charges require the full, time-dependent Maxwell equations, which will be discussed in later sections.

---
#### Point Charges: Field Formalism
To simplify the description of forces on a test particle, we abstract the effects of sources into fields. A point charge $q$ at position $\vec{r}'$ produces an *electric field* at position $\vec{r}$, defined such that a test charge $q_\text{test}$ experiences an electric force:
$$\begin{align}
\vec{F}_E(\vec{r})&=q_\text{test}\vec{E}(\vec{r})
\end{align}$$
For a stationary point charge, the field reduces to the familiar Coulomb form:
$$\begin{align}
\vec{E}(\vec{r})&=\dfrac{q}{4\pi\epsilon_0}\cdot\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3} && \text{(S1.9, J1.3)}
\end{align}$$
Similarly, for a moving point charge $q$ produces a *magnetic field* at position $\vec{r}$, defined such that a test charge moving with velocity $\vec{v}$ experiences a magnetic force:
$$\begin{align}
\vec{F}_E(\vec{r})&=q_\text{test}\vec{v}\times\vec{B}(\vec{r})
\end{align}$$
For a point charge moving with velocity $\vec{v}'$, the magnetic field takes analogous Coulomb form:
$$\begin{align}
\vec{B}(\vec{r})&=\dfrac{\mu_0(q\vec{v}')}{4\pi}\times\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3} && \text{(S1.10)}
\end{align}$$
In terms of point currents $\vec{j}=q\vec{v}'$, this can also be written as:
$$\begin{align}
\vec{B}(\vec{r})&=\dfrac{\mu_0\vec{j}}{4\pi}\times\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3} && \text{(S1.11)}
\end{align}$$
These definitions provide a convenient abstraction: the electric field depends only on the source charge and its position, while the magnetic field depends on the source current and its position. Forces on test charges can be computed directly from these fields without re-evaluating interactions from each individual source.

---
#### Superposition of Fields
The electric and magnetic fields obey a simple and powerful property: *linearity*. The total field produced by multiple sources is the vector sum of the field produced by each source individually.

For a system of discrete point charges $q_i$ and positions $\vec{r}_i$ and velocities $\vec{v}_i$, the total electric and magnetic fields at a point $\vec{r}$ are:
$$\begin{align}
\vec{E}(\vec{r})&=\sum_i\dfrac{q_i}{4\pi\epsilon_0}\cdot\dfrac{\vec{r}-\vec{r}_i}{|\vec{r}-\vec{r}_i|^3} && \text{(S1.12, J1.4)}\\
\vec{B}(\vec{r})&=\sum_i\dfrac{\mu_0\vec{j}_i}{4\pi}\times\dfrac{\vec{r}-\vec{r}_i}{|\vec{r}-\vec{r}_i|^3}, \ \ \ \ \vec{j}_i=q_i\vec{v}_i && \text{(S1.13)}
\end{align}$$
For continuous distribution of charges and current, the sums are replaced by integrals over the source densities $\rho(\vec{r}',t)$ and $J(\vec{r}',t)$:
$$\begin{align}
\vec{E}(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\int\rho(\vec{r}',t)\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}\ d^3r' && \text{(S1.14, J1.5)}\\
\vec{B}(\vec{r},t)&=\dfrac{\mu_0}{4\pi}\int J(\vec{r}',t)\times\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}\ d^3r' && \text{(S1.15)}
\end{align}$$
This continuous magnetic field expression is recognized historically as the *Biot-Sovart law* for steady currents, while the continuous electric field generalizes Coulomb's law to extended charge distributions. This superposition principle lets us to construct fields for arbitrarily complex arrangements by summing or integrating contributions from elementary sources. It is also possible to construct discrete source distributions using the Dirac delta function, which is left as an exercise to the reader (Hint: use $S1.1$ and $S1.2$, as well as the superposition principle).

---
### Lorentz Force Law
The motion of a charged particle in the presence of electric and magnetic fields is governed by the *Lorentz force*. A point charge $q$ located at $\vec{r}(t)$ and moving with velocity $\vec{v}(t)$ experiences a force given as the sum of electric and magnetic forces:
$$\begin{align}
\vec{F}(\vec{r},t)&=q\left[\vec{E}(\vec{r},t)+\vec{v}\times\vec{B}(\vec{r},t)\right] && \text{(S1.16)}
\end{align}$$
Here, $\vec{E}$ and $\vec{B}$ are the electric and magnetic fields at the particle's position. The electric term acts along the direction of the field, while the magnetic term is perpendicular to both the velocity and the magnetic field, producing a force that can curve the particle’s trajectory.

If the charge is stationary $(\vec{v}=0)$, the Lorentz force reduces to the familiar Coulomb force. For moving charges, the magnetic contribution arises naturally, reflecting the coupling between motion and magnetic fields.

The Lorentz force law provides a general and compact description of how charges respond to electromagnetic fields. It also forms the basis for deriving equations of motion in more specific situations, including electrostatics, magnetostatics, and full electrodynamics in later chapters.

---
### Electromechanical Work & Magnetomechanical Torque
Up to this point, we have reformulated electromagnetic interactions in terms of fields and potentials. However, our ultimate goal remains practical: to determine the motion of charges and currents. Dynamics is governed by forces and force-like quantities, and in mechanics these manifest most naturally through *work* and *torque*. We therefore return to a mechanical viewpoint, now expressed in the language of fields and potentials. 

The Lorentz force law gives the force density acting on a distribution of charge and current:
$$\begin{align}
\vec{f}(\vec{r},t)&=\rho(\vec{r},t)\vec{E}(\vec{r},t)+\vec{j}(\vec{r},t)\times\vec{B}(\vec{r},t) && \text{(S2.6)}
\end{align}$$
From this expression, work and torque follow directly.

---
#### Electromechanical Work
The total work done by the electromagnetic field on a charge distribution over a region $\Omega$ is:
$$\begin{align}
W&=\int_\Omega\vec{f}(\vec{r},t)\cdot d\vec{r}=\int_\Omega\rho(\vec{r},t)\vec{E}(\vec{r},t)\cdot d\vec{r} && \text{(S2.7)}
\end{align}$$
The magnetic contribution is always perpendicular to the velocity of the charges and therefore performs no work. Only the electric field contributes to changes in kinetic energy.

---
#### Magnetomechanical Torque
While magnetic fields do not perform work, they do generate torque.

The torque density about the origin is
$$\begin{align}
\vec{\tau}(\vec{r},t)=\vec{r}\times\vec{f}(\vec{r},t)&=\vec{r}\times\left(\vec{j}(\vec{r},t)\times\vec{B}(\vec{r},t)\right) && \text{(S2.9)}
\end{align}$$
For a localized current distribution, this leads in the static limit to the familiar dipole torque form,
$$\begin{align}
\vec{\tau}&=\vec{\mu}\times\vec{B}
\end{align}$$
where $\vec{\mu}$​ is the magnetic dipole moment.

Thus, magnetic fields govern rotational effects.

---
#### Separation of Roles
We observe a structural distinction:
- The electric field couples to charge density $\rho$ and is responsible for energy transfer through work.
- The magnetic field couples to current density $\vec{J}$ and is responsible for transverse forces and torque.
- The magnetic force is always orthogonal to velocity and therefore cannot change kinetic energy.
- A static electric field, being conservative, cannot generate torque on a stationary point charge.
This separation is not arbitrary; it follows directly from the structure of the Lorentz force and ultimately from the definitions of the scalar and vector potentials.

In this way, the decomposition of electromagnetic interactions into electric and magnetic components reflects a deeper mechanical split between energy-changing and direction-changing effects.

---
### Maxwell's Equations


---
### Electromagnetic Wave Equation



We will return to this after we discuss potentials and electromagnetic media.




---
## Chapter 2: Electromagnetic Potentials
To describe the electric and magnetic fields in a more general and often more mathematically convenient way, we introduce the *scalar potential* $\Phi(\vec{r},t)$ and the *vector potential* $\vec{A}(\vec{r},t)$. These potentials encode the fields through the relations:
$$\begin{align}
\vec{E}(\vec{r},t)&=-\vec\nabla\Phi(\vec{r},t)-\dfrac{\partial\vec{A}}{\partial t}(\vec{r},t),&\vec{B}(\vec{r},t)&=\vec\nabla\times\vec{A}(\vec{r},t) && \text{(S2.1)}
\end{align}$$
Here, $\Phi$ captures contributions analogous to the *electrostatic potential*, while $\vec{A}$ accounts for effects due to *moving charges and currents*, naturally giving rise to the magnetic field.

---
### Point Charges: Field Formalism
For a single point charge $q$ at position $\vec{r}_0(t)$ with velocity $\vec{v}_0(t)$, the corresponding point current is $\vec{j}=q\vec{v}_0$. The *instantaneous potentials* at a field point $\vec{r}$ are then:
$$\begin{align}
\Phi(\vec{r},t)&=\dfrac{q}{4\pi\epsilon_0}\dfrac{1}{|\vec{r}-\vec{r}_0(t)|} && \text{(S2.2)}\\
\vec{A}(\vec{r},t)&=\dfrac{\mu_0\vec{j}}{4\pi}\dfrac{1}{|\vec{r}-\vec{r}_0(t)|} 
&& \text{(S2.3)}
\end{align}$$
 - For stationary charges, $\vec{A}$ vanishes and $\Phi$ reduces to the Coulomb potential.
 - For moving charges, $\vec{A}$ captures the magnetic contribution, with the current $\vec{j}$ as the source.

---
### Superposition of Potentials
Similar to our electric and magnetic fields obey a linear superposition, our scalar and vector potentials also allow for superposition. As in, the total potential produced by multiple sources is the sum of the potential produced by each source individually. As for why we know that our potentials are allowed to be so simply added, that an exercise for the reader to prove that fields that have linearity imply potentials that share this property.

For a system of discrete point charges $q_i$ and positions $\vec{r}_i$ and currents $\vec{j}_i=q\vec{v}_i$, the total scalar and vector potentials at a point $\vec{r}$ are:
$$\begin{align}
\Phi(\vec{r},t)&=\sum_i\dfrac{q_i}{4\pi\epsilon_0}\dfrac{1}{|\vec{r}-\vec{r}_i|}, &
\vec{A}(\vec{r},t)&=\sum_i\dfrac{\mu_0\vec{j}_i}{4\pi}\dfrac{1}{|\vec{r}-\vec{r}_i|} && \text{(S2.4)}
\end{align}$$
For continuous distribution of charges and currents, the sums are replaced by integrals over the source densities $\rho(\vec{r}',t)$ and $J(\vec{r}',t)$:
$$\begin{align}
\Phi(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\int\rho(\vec{r}',t)\dfrac{1}{|\vec{r}-\vec{r}'|}\ d^3r', & \vec{A}(\vec{r},t)&=\dfrac{\mu_0}{4\pi}\int J(\vec{r}',t)\dfrac{1}{|\vec{r}-\vec{r}'|}\ d^3r' && \text{(S2.5)}
\end{align}$$
Given that our integrations no longer require worrying about vector directions directly or through cross product, these expressions are much more simple to use in modeling systems.

---
### Gauge Freedom
Preserves the fields with a different potential
Show it in terms of the equations for fields and how we can add a function that doesn't affect the physical fields.


---
### Electromagnetic Potential Wave Equation

Derivation from Maxwell's equations


#### Decoupled Potentials (Lorenz Gauge)
Pure electromagnetic potential wave equations


---
## Chapter 3: Vacuum Electrostatics
No current, steady-state solution

---
## Chapter 4: Vacuum Magnetostatics
Steady-state currents

---
## Chapter 5: Electromagnetic Media

### Electric Displacement Field
### Magnetic Displacement Field
### Linear Medium Approximation

---
## Chapter 6: Medium Electrostatics
No current, steady-state solution

---
## Chapter 7: Medium Magnetostatics
Steady-state currents

---
## Chapter 8: Medium Electrodynamics (Optics)


---
## Chapter 9: Vacuum Electrodynamics
Current exists, charges exist


---
## Chapter 10: Relativistic Electrodynamics
Constant $c$ problem, retarded potentials, Faraday tensor


---
## Chapter 11: Early Quantum Electrodynamics
Aranov Bohm Effect, corrections to hydrogen atom, atomics.



---
## Chapter 12: Modern Quantum Electrodynamics
Quantum Field Theory's version of Electrodynamics


---
## Chapter 13: Exploration of the Magnetic Monopole

Dirac quantization, adjustment to Maxwell's equations, parity of time and space, swapping space and time to give monopoles, etc.
















Chapter 2 Homework Question:
Given that our electric and magnetic fields allow for linear superposition over a sum of its composite sources, why are the scalar and vector potentials also allowed to be superimposed? Prove that superimposition of fields implies that the potentials must also.