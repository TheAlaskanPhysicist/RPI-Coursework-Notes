

Intent: When I was a student I was frustrated with how disconnected a lot of topics are, and absolutely hated Jackson's electrodynamics since it was not a competent tool to teach from.
I wanted to make a book that was both useful when an expert and also a student guide into thinking abstractly to formulate theoretical physics like this.





---
## Chapter 1: Foundations of Electromagnetism
Electromagnetism is one of the foundational theories of modern physics, explaining how electric and magnetic phenomena arise from the motion and distribution of electric charge. The theory's roots date back to the 19th century, when *Benjamin Franklin* (in the 1750s) coined the term *electricity* and first identified charge as a fundamental property of matter. As work continued through the 19th and early 20th centuries, the discovery of electromagnetic *fields* and their interdependence—culminating in *Maxwell’s Equations* (1860s)—shaped the way we understand interactions between charges and currents.

For those technically-inclined: electromagnetism is a cause-response theory between electromagnetic charge/current sources and their associated electromagnetic fields.

---
### 1.1 Introduction to Electromagnetism
In order to study electromagnetism, we must first understand its *sources*: *electric charge* and *electric current*. A century before Maxwell, *Benjamin Franklin* introduced the concept of *electric charge* as a property of matter, and *Charles-Augustin de Coulomb* quantified the force between charges in 1785. Later, in the 19th century, *Hans Christian Ørsted* and *André-Marie Ampère* discovered the relationship between electric currents and magnetic fields, leading to the development of *electrodynamics*.

Historically, the simplest model of electromagnetism involved *electric monopoles*—point charges with either positive or negative charge. *Electric currents*, which are the flows of electric charge, were introduced later, especially with the understanding that charge motion could produce magnetic fields. The concept of current density was formalized, and as we will see, it plays a crucial role in understanding how moving charges generate electromagnetic fields.

There is also, in principle, another type of point-like charge—the *magnetic monopole*—which would act as a source of "magnetic charge." However, it has been well-established that such particles are absent from our universe, despite their allowance in the theory. For the purposes of education, we will focus primarily on **electric** charge and current, deferring the exploration of magnetic monopoles to a later section, where we'll address their theoretical implications. Due to their omission, the remainder of the chapters will assume electric charges and currents, unless otherwise specified.

---
#### 1.1A The Dirac Delta Function
It is often helpful to model systems as a collection of points in order to understand larger, continuous distributions in a given volume. This approach is akin to taking an object and dividing it into ever-smaller grids, approaching an infinite number of divisions. In electromagnetism, many phenomena involve point sources—like point charges and currents—where all the "action" happens at a particular location in space. To describe these point-like phenomena mathematically, we use the *Dirac delta function*, introduced by physicist Paul Dirac in 1930.

The Dirac delta function was developed to represent idealized, point-like sources; it allows us to capture the behavior of these sources in continuous media, offering a rigorous procedure for describing phenomena localized at a single point in space. The delta function helps simplify the translation of these localized point sources into useful mathematical expressions.

The Dirac delta function is defined as:
$$\begin{align}
\delta(x)&=\begin{cases}
\infty,&x=0\\
0,&x\ne0
\end{cases}&& \text{(S1.1)}
\end{align}$$
This function, while seemingly odd given the non-finite value at $x=0$, has special properties that make it useful in physics and mathematics. The delta function is normalized over its domain:
$$\begin{align}
\int_{-\infty}^\infty\delta(x)\ dx&=1 && \text{(S1.2)}
\end{align}$$
Though $\delta(x)$ is zero everywhere except for $x=0$, its total effect over the domain is equal to $1$.

Perhaps more importantly, the delta function has the following integral-reducing property:
$$\begin{align}
\int_{-\infty}^\infty f(x)\delta(x-a)\ dx&=f(a) && \text{(S1.3)}
\end{align}$$
This property allows the delta function to effectively "undo" the integration of its contents—picking out the value of the function $f(x)$ at the point $x=a$. In practical terms, this means that the delta function can effectively isolate the value of a quantity at a specific point, making it an effective tool for representing point-like sources, such as point charge or current.

Technically, the Dirac delta function isn't a "true" function in the conventional sense. It is not a function defined at every point in space, but rather a *distribution*—a mathematical object that makes sense primarily when integrated against other functions. It is part of a class often described as a *generalized function*, which has more relaxed constraints than standard functions.

With its infinite value at one point and zero elsewhere, the delta function doesn't behave like traditional functions. Instead, it serves as a shorthand tool for solving problems where point-like phenomena occur. This distinction is important: although the delta function acts like a function in many contexts, it is ultimately a mathematical abstraction used to simplify and generalize the treatment of point sources in physics and other related fields.

---
### 1.2 Charge and Current Densities
To proceed with the study of electromagnetic fields and potentials, we must first mathematically describe the *sources* of electromagnetism: *electric charge* and *electric current*. A point particle with charge $q$, located at position $\vec{r}_0(t)$, and moving with velocity $\vec{v}_0(t)=\dot{\vec{r}}_0(t)$, produces localized charge and current densities in space.

The *electric charge density* $\rho(\vec{r},t)$ associated with this point charge is given by:
$$\begin{align}
\rho(\vec{r},t)&=q\ \delta\left(\vec{r}-\vec{r}_0(t)\right) && \text{(S1.4)}
\end{align}$$
In its construction, the delta function $\delta$ localizes the charge to the position of the charge $\vec{r}_0(t)$. The magnitude of the charge, $q$, represents the "strength" of the particle's electromagnetic presence at that point. Effectively, this charge density acts as a *point source* of charge, which will later be used to derive the resultant fields it produces.

In addition to charge, *electric current density* $\vec{J}(\vec{r},t)$ is needed to describe the flow of charge. The current density due to a moving point charge is given by:
$$\begin{align}
\vec{J}(\vec{r},t)&=q\vec{v}_0(t)\ \delta\left(\vec{r}-\vec{r}_0(t)\right) && \text{(S1.5)}
\end{align}$$
Here, the current density is also localized to the position $\vec{r}_0(t)$, and the velocity $\vec{v}_0(t)$ of the moving charge scales the total current. The product of charge $q$ and velocity $\vec{v}_0(t)$ represents the current associated with the particle's motion at that particular instant.

To simplify this expression, we introduce a new quantity, the *point current* $\vec{j}$, defined as:
$$\begin{align}
\vec{j}&=q\vec{v}_0(t) && \text{(S1.6)}\\
\vec{J}(\vec{r},t)&=\vec{j}\ \delta\left(\vec{r}-\vec{r}_0(t)\right) && \text{(S1.7)}
\end{align}$$
This defines the "strength" of the current due to the moving point charge. The new current $\vec{j}$ is analogous to charge $q$, in the sense that it describes the *presence* of electromagnetic quantities at the location of the point particle.

Thus, we have two analogous quantities for describing the sources of a point particle:
- Charge density $\rho(\vec{r},t)$ which localizes **charge** at the position of the moving charge, and
- Current density $\vec{J}(\vec{r},t)$ which localizes the **current** at the position of the moving charge.

In later sections, our choice in defining point current $\vec{j}$ will help aid in showing the parallels in the equations of electric and magnetic fields, as well as their intercoupling.

---
#### 1.2A Conservation of Charge
Now that we have defined the *charge density* $\rho(\vec{r},t)$ and *current density* $\vec{J}(\vec{r},t)$ for a point particle, we can examine their variations over time and space to understand how charge behaves in a dynamical system. 

Suppose we differentiate the charge density with respect to time. Using $\text{S1.4}$, we have:
$$\begin{align}
\dfrac{\partial\rho}{\partial t}&=\dfrac{\partial}{\partial t}\left[q\ \delta\left(\vec{r}-\vec{r}_0(t)\right)\right]=-q\vec{v}_0(t)\cdot\vec\nabla\delta\left(\vec{r}-\vec{r}_0(t)\right) && \text{(S1.8)}
\end{align}$$
With the application of the chain rule, we see that the rate change in charge density involves the particle's velocity $\vec{v}_0(t)$ and the gradient of the delta function, enforcing locality.

Similarly, we take the divergence of the current density $\vec{J}(\vec{r},t)$, as given by $\text{S1.5}$:
$$\begin{align}
\vec{\nabla}\cdot\vec{J}&=\vec{\nabla}\cdot\left[q\vec{v}_0(t)\ \delta\left(\vec{r}-\vec{r}_0(t)\right)\right]=+q\vec{v}_0(t)\cdot\vec\nabla\delta\left(\vec{r}-\vec{r}_0(t)\right) && \text{(S1.9)}
\end{align}$$
The divergence of the current density reflects the change in the amount of charge flowing into or out of a region, again involving the particle's velocity $\vec{v}_0(t)$ and gradient of the delta function.

Notice that equations $\text{S1.8}$ and $\text{S1.9}$ are of equal magnitude, but opposite signs. Added together:
$$\begin{align}
\dfrac{\partial\rho}{\partial t}(\vec{r},t)+\vec{\nabla}\cdot\vec{J}(\vec{r},t)&=0 && \text{(S1.10)}
\end{align}$$
This equation is known as the *continuity equation*; it expresses the local balance between the rate of change of charge density at a point and the current flowing into or out of that point. In essence, the continuity equation asserts that charge cannot be created or destroyed; it can only flow or accumulate in different regions of space. This property is known as *charge conservation*.

The continuity equation is foundational in electromagnetism because it ensures that the total charge in a closed system remains constant over time, and that any loss of charge within an enclosed volume can only occur through a current through its surface. This will play an important role as we begin exploring the dynamics of electric and magnetic fields in later chapters.

---



### 1.3 Forces in Electromagnetism
To study the motion of charges and currents, we first need to understand the *forces* that act on individual point particles. The study of forces in electromagnetism began in earnest with the development of Coulomb's law, which describes the interaction between stationary point charges. From this basic law, a more general theory of electromagnetic forces was developed, taking into account moving charges and their corresponding magnetic effects. These forces determine how charges move through space, connecting the presence of charge and current to measurable electromagnetic effects; this interplay forms the foundation of much of electromagnetism.

The forces on charges can be classified into two categories:
 - Electric forces, which act between stationary or moving charges due to their electric fields.
 - Magnetic forces, which arise from the motion of charges and their associated magnetic fields.

It is important to note that the equations we use to describe these forces are only valid under ***instantaneous interactions only***. This means that these equations assume charges are moving at constant velocities. If the charges are accelerating, the forces are no longer fully captured by these formulas because accelerating charges emit electromagnetic radiation (light). The full dynamics of accelerating charges requires the more complex, time-dependent Maxwell equations, which we will explore in later sections. However, if the charges are relatively slow, these equations are excellent approximations for most dynamics on the human scale.

---
#### 1.3A Instantaneous Forces (Point Sources)
The first description of the interaction between stationary point charges is *Coulomb's law*, formulated by *Charles-Augustin de Coulomb* in 1785. For two point charges, $q$ and $q'$, located at positions $\vec{r}$ and $\vec{r}'$, the electric force $\vec{F}_{E}$​ that one charge exerts on the other is given by:
$$\begin{align}
\vec{F}_{E}(\vec{r})&=\dfrac{qq'}{4\pi\epsilon_0}\cdot\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3} && \text{(S1.11, J1.2)}
\end{align}$$
This equation describes the force between stationary charges, where the force is directed along the line connecting the two charges and inversely proportional to the square of the distance between them. The constant $\epsilon_0$ is the permittivity of free space, which relates the strength of the electric force in a vacuum.

For moving charges, the situation is slightly different. When charges are in motion, they generate magnetic fields that can exert forces on other moving charges. The magnetic force $\vec{F}_{B}$ on a charge $q$ moving with velocity $\vec{v}$ in the presence of another moving charge $q'$ with velocity $\vec{v}'$ is given by:
$$\begin{align}
\vec{F}_{B}(\vec{r})&=\dfrac{\mu_0(q\vec{v}\times q'\vec{v}')}{4\pi}\times\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3} && \text{(S1.12)}
\end{align}$$
Here, $\mu_0​$ is the permeability of free space, and the cross product between the velocities shows that the magnetic force acts perpendicular to both the velocities and the displacement vector between the charges. In this form, the magnetic force depends not just on the magnitude of the charges, but also on their velocities.

This equation can be rewritten using the point current from equation $\text{S1.6}$ :
$$\begin{align}
\vec{F}_{B}(\vec{r})&=\dfrac{\mu_0\vec{j}\times\vec{j}'}{4\pi}\times\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}, &\vec{j}&=q\vec{v} && \text{(S1.13)}
\end{align}$$
We can draw parallels between both force equations if we perform the following exchanges:
- Cross product $(\times)$ $\leftrightarrow$ Scalar product $(\cdot)$
- Point current $(\ \vec{j}\ )$ $\leftrightarrow$ point charge $(q)$.

These forces are structurally very similar: both depend on the "strength" of the sources (charge or current) and the relative position vector $\vec{r}-\vec{r}'$, with the magnetic force additionally depending on the velocities and acting in a direction generally perpendicular to displacement.

As a reminder, these equations are only valid when neither charges are accelerating, whether linearly or angularly.

---
#### 1.3B Superposition Instantaneous Forces (Point Sources)
The electric and magnetic forces we’ve described so far apply to individual pairs of charges or currents. However, in most real systems, we deal with multiple charges or currents interacting simultaneously. A key principle in electromagnetism is the *superposition principle*, which states that the total force on a particle is simply the sum (or integral) of the forces due to each source independently. This principle holds for both electric and magnetic forces and is fundamental to the way we calculate forces in systems with multiple sources. We will also see later that their associated fields also obey this principle of superposition.

The electric force between two point charges $q_i$ and $q_j$, located at positions $\vec{r}_i$ and $\vec{r}_j$ is given by Coulomb's law (equation $\text{S1.11})$:
$$\begin{align}
\vec{F}_{E,ij}&=\dfrac{q_iq_j}{4\pi\epsilon_0}\cdot\dfrac{\vec{r}_i-\vec{r}_j}{|\vec{r}_i-\vec{r}_j|^3} && \text{(S1.11)}
\end{align}$$
The total electric force acting on charge $i$ due to all other charges (to avoid singularities) in the system is found by summing the forces from each other charge $j$ :
$$\begin{align}
\vec{F}_{E}(\vec{r}_i,t)&=\sum_{j\ne i}\dfrac{q_iq_j}{4\pi\epsilon_0}\cdot\dfrac{\vec{r}_i-\vec{r}_j}{|\vec{r}_i-\vec{r}_j|^3} && \text{(S1.14)}
\end{align}$$
For moving charges, we must account for the magnetic forces as well. The force on a moving charge $q_i$ with velocity $\vec{v}_i$, in the presence of another moving charge $q_j$ with velocity $\vec{v}_j$ is given by the magnetic counterpart of Coulomb's law (equation $\text{S1.13})$:
$$\begin{align}
\vec{F}_{B,ij}&=\dfrac{\mu_0\vec{j}_i\times\vec{j}'_j}{4\pi}\times\dfrac{\vec{r}_i-\vec{r}_j}{|\vec{r}_i-\vec{r}_j|^3}, &\vec{j}_i&=q_i\vec{v}_i && \text{(S1.13)}
\end{align}$$
The cross products between the velocities results in the force being perpendicular to both velocities and the displacement vector between the particles.

The total magnetic force acting on current $i$ due to all other currents in the system is:
$$\begin{align}
\vec{F}_{B}(\vec{r}_i,t)&=\sum_{j\ne i}\dfrac{\mu_0\vec{j}_i\times\vec{j}'_j}{4\pi}\times\dfrac{\vec{r}_i-\vec{r}_j}{|\vec{r}_i-\vec{r}_j|^3}, &\vec{j}_i&=q_i\vec{v}_i && \text{(S1.15)}
\end{align}$$
Similar to the electric force, the total magnetic force on charge $i$ is obtained by summing the forces from each of the charges $j$. 

---
#### 1.3C Instantaneous Forces (Continuum Sources)
When the sources of charge or current are distributed continuously in space (rather than being discrete point charges), the superposition principle still applies. The total force on a external particle is the integral of the forces from all the charge or current elements in the system. This allows us to handle systems with continuous distributions, such as charge or current densities.

For a continuous distribution of charge, described by the charge density $\rho(\vec{r}',t)$, the electric force on an external charge $q$ at position $\vec{r}$​ is given by:
$$\begin{align}
\vec{F}_E(\vec{r},t)&=\int\dfrac{q\rho(\vec{r}',t)}{4\pi\epsilon_0}\cdot\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}\ d^3r' && \text{(S1.16)}
\end{align}$$
The integral has the action of summing all the forces from all charge elements, with $\rho(\vec{r}')$ representing the charge density at position $\vec{r}'$.

Similarly, for a continuous distribution of current $\vec{J}(\vec{r}',t)$, the magnetic force on an external current element with velocity $\vec{v}$ at position $\vec{r}$​ is
$$\begin{align}
\vec{F}_B(\vec{r},t)&=\int\dfrac{\mu_0\vec{j}\times\vec{J}(\vec{r}',t)}{4\pi}\times\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}\ d^3r' && \text{(S1.17)}
\end{align}$$
where $\vec{j}=q\vec{v}$ represents the point current of the external charge.

As far as creating continuous distributions, we've reached somewhat of a limit. With discrete charges/currents, we were able to select distinct point charges to have our forces be applied to. However, in the conversion to continuous sources, we've somewhat lost the meaning of what charge exactly our force is being applied to. What we're encountering here is actually the central premise to an abstraction of these forces which, near the end of this chapter, we will see are the first hint of formalizing electric and magnetic fields.

---
### 1.4 Work & Energy in Electromagnetism
Electromagnetic interactions are not limited to the simple attraction or repulsion of charges; they also give rise to more complex phenomena, such as the transfer of energy and the generation of rotational motion. These interactions, described by the Lorentz force, combine both electric and magnetic contributions to force, and they play a pivotal role in electromechanical systems, where charges and currents are the sources of work and torque. While we have previously explored electromagnetic interactions in terms of forces, the ultimate goal is to understand how these interactions govern the motion of charges and currents. 

In classical mechanics, forces manifest through work and torque, and we now shift back to a mechanical viewpoint, using the language of electromagnetism to describe how electric fields transfer energy through work and how magnetic fields generate torque. This chapter begins by examining how electric potential energy is transferred when charges move, followed by an exploration of how magnetic fields, through their forces on moving charges, generate torque in systems like motors and generators. By examining both electric and magnetic effects, we can understand how energy is stored, transferred, and converted in electromagnetic systems.

---
#### 1.4A Electric Potential Energy
In electromagnetism, *electric potential energy* refers to the energy stored in a system due to the relative positions of charges, which is directly related to the forces acting between them. The potential energy of a system of charges quantifies the energy that would be required to assemble that system from infinitely separated charges, where no forces are acting.

For a single point charge $q$ in a electrostatic configuration, the potential energy is a result of its interaction with other charges in the system. For example, if a charge $q$ at position $\vec{r}$ is in the presence of a stationary charge $q'$ at position $\vec{r}'$​, the electric potential energy $U$ associated with this mutual interaction is:
$$\begin{align}
U&=\dfrac{qq'}{4\pi\epsilon_0}\dfrac{1}{|\vec{r}-\vec{r}'|} && \text{(S1.18)}
\end{align}$$
This expression shows that the electric potential energy is directly related to the magnitude of the charges and inversely related to the distance between them. The work required to move a charge in the presence of another charge depends on this potential energy, as the force between charges can be thought of as arising from their mutual potential energy.

For a system of multiple charges, the total potential energy is the sum of the potential energies due to each pair of charges. For discrete point charges $q_i$ at positions $\vec{r}_i$​, the total potential energy $U_\text{total}$​ of the system is given by the sum of all pairwise interactions:
$$\begin{align}
U_\text{total}&=\sum_{i<j}\dfrac{q_iq_j}{4\pi\epsilon_0}\dfrac{1}{|\vec{r}_i-\vec{r}_j|}=\dfrac{1}{2}\sum_{i\ne j}\dfrac{q_iq_j}{4\pi\epsilon_0}\dfrac{1}{|\vec{r}_i-\vec{r}_j|} && \text{(S1.19)}
\end{align}$$
This formula accounts for the fact that each pair of charges in the system interacts with a force that contributes to the system's overall potential energy.

The electric potential energy in a system determines how much work is required to assemble the system or move charges within it. For example, when charges move from regions of higher potential energy to lower potential energy, they do so under the influence of electric forces. This movement is a form of *work* being done by or on the system, converting potential energy into kinetic energy, or vice versa, depending on the direction of movement.

---
#### 1.4B Electromechanical Work
In electromagnetism, _work_ is the energy transferred to or from a system when a force causes a charge to move over a displacement. The electric force, $\vec{F}_E$, acts on a point charge $q$ and moves it from an initial position $\vec{r}_1$ to a final position $\vec{r}_2$. The work done by the electric force in this process is given by the line integral of the force along the path of motion:
$$\begin{align}
W&=\int_{\vec{r}_1}^{\vec{r}_2}\vec{F}_E(\vec{r},t)\cdot d\vec{r} && \text{(S1.18)}
\end{align}$$
where $\vec{F}_E(\vec{r},t)$ is the electric force at the position $\vec{r}$ at time $t$. The work is directly related to how the charge interacts with the electric field along the path, transferring energy as the charge moves.

When dealing with a system of multiple charges, the total work done is the sum of the work done on each individual charge. This can be represented by integrating the work expression over the distribution of charges, considering each charge's displacement and the forces acting on it.

For electrostatic systems, where the electric force is _conservative_—meaning that the curl of the force is zero $(\vec\nabla\times\vec{F}=0)$—the work done by the force is *path-independent*. In these systems, the work can be conveniently written in terms of the *potential energy* at the initial and final positions:
$$\begin{align}
W&=U(\vec{r}_2)-U(\vec{r}_1) && \text{(S1.19)}
\end{align}$$
where $U(\vec{r})$ represents the potential energy associated with the position $\vec{r}$ of the charge. This formulation reflects the fact that the work done in moving a charge in a conservative field depends only on the change in potential energy between the initial and final positions, not on the specific path taken.

The rate at which work is done, or the rate at which energy is transferred to or from a moving charge, is known as *power*. The power $P$ delivered by the electric force is the time derivative of the work:
$$\begin{align}
P=\dfrac{dW}{dt}&=\dfrac{d}{dt}\int_{\vec{r}_1}^{\vec{r}_2}\vec{F}_E(\vec{r},t)\cdot d\vec{r} && \text{(S1.20)}
\end{align}$$
This expression represents the instantaneous rate of energy transfer as the charge moves under the influence of the electric force, quantifying how quickly the system is transferring energy.

---
#### 1.4C Magnetomechanical Torque
In mechanics, *torque* refers to the rotational force exerted on a system. In electromagnetism, magnetic fields do not perform work in the traditional sense, but they can generate rotational effects on objects carrying currents. This is especially important in systems such as electric motors, where magnetic torque plays a critical role in mechanical motion.

The torque density at a point $\vec{r}$ due to a current distribution is given by the cross product of the position vector $\vec{r}$ and the force density $\vec{f}_B(\vec{r},t)$ acting at that point:
$$\begin{align}
\vec{\tau}(\vec{r},t)=\vec{r}\times\vec{f}(\vec{r},t)&=\vec{r}\times\left(\vec{J}(\vec{r},t)\times\vec{B}(\vec{r},t)\right) && \text{(S1.21)}
\end{align}$$
where $\vec{J}(\vec{r},t)$ is the current density at position $\vec{r}$, and $\vec{B}(\vec{r},t)$ is the magnetic field at the same location. This expression represents the torque generated by the interaction of the current distribution with the magnetic field.

In the static case (when the currents are steady), this expression simplifies to the familiar result for the torque on a magnetic dipole:
$$\begin{align}
\vec{\tau}&=\vec{\mu}\times\vec{B}
\end{align}$$
where $\vec{\mu}$ is the magnetic dipole moment of the system, defined as:
$$\begin{align}
\vec{\mu}&=\int\vec{r}\times\vec{J}(\vec{r},t)\ d^3r
\end{align}$$
This expression describes the torque on a current loop or dipole in the presence of a magnetic field. The torque causes the current loop to rotate, and the rate at which it rotates depends on the strength of the magnetic field and the orientation of the current distribution relative to the field.

Magnetic torque is fundamentally different from work because it does not change the kinetic energy of a system. Instead, it only alters the rotational motion of the system, as the force is always perpendicular to the velocity of the moving charges. This is a key distinction between the electric and magnetic contributions to electromagnetic systems: while the electric force can change the kinetic energy of a charge (doing work), the magnetic force only affects the direction of motion, leading to torque.

---

In the previous sections, we’ve discussed how electric and magnetic forces act on charges and currents, resulting in mechanical effects such as work and torque. These forces, while both fundamental to electromagnetism, play distinct roles in the way they influence systems. To fully understand their contributions to energy transfer and motion, it’s essential to separate and highlight these roles:

 - *Electric Forces*: The electric field couples to the *charge density* $\rho(\vec{r},t)$ and is responsible for transferring energy through *work*. When a charge moves within an electric field, the field does work on the charge, transferring energy and altering the charge’s potential energy. This is the mechanism that powers systems like capacitors, where energy is stored and released as the charge moves in response to the field.

 - *Magnetic Forces*: The magnetic field couples to the *current density* $\vec{J}(\vec{r},t)$ and generates *torque*. A magnetic field affects moving charges by altering their direction of motion without changing their kinetic energy. This torque-producing effect is central to the operation of devices like electric motors and generators, where magnetic fields cause rotation by applying forces perpendicular to the velocity of the current-carrying conductors.

This distinction between electric and magnetic forces is not just a matter of convenience; it reflects a deeper mechanical separation within the structure of the *Lorentz force*. The electric field, through its coupling with charge density, is associated with energy transfer (work), while the magnetic field, interacting with currents, is responsible for rotational motion (torque). Importantly, the magnetic force is always orthogonal to velocity, meaning it does not do work—it only changes the direction of motion, which is the key to generating torque.

This structural division underpins the way electromagnetism operates in practical systems. *Electric fields* are fundamental in systems where energy transfer is key—whether in static fields (as with capacitors) or dynamic systems (such as electric circuits). On the other hand, *magnetic fields* play a crucial role in systems that rely on rotational motion and torque, from motors to particle accelerators.

Thus, understanding this separation helps to frame the roles of electric and magnetic fields within the larger picture of electromagnetism. As we move forward in the text, we'll build on these distinctions to explore more complex systems where both electric and magnetic effects are at play, but always with the understanding that the forces act in complementary yet distinct ways: one to transfer energy through work, the other to generate torque through rotational motion.

---
### 1.5 The Emergence of Electromagnetic Fields
Up until this point, we have considered point charges and currents as the sources of electromagnetic forces. We've observed how these sources act individually on one another, and we have introduced the concepts of work and torque. However, as we move toward more complex systems, the notion of a discrete point charge becomes increasingly less practical, especially when dealing with continuous charge distributions. The next natural step is to consider how these distributions lead to new quantities that extend the idea of forces into fields.

In electromagnetism, the _field_ is the fundamental object through which we describe the influence of charges and currents. However, to reach a clear definition of the field, we must understand how to represent the force interactions between charges in the continuum limit, as we break them down into infinitesimally small volumes.

Consider a volume of space containing a continuous distribution of charge, where each infinitesimal volume element contributes a portion of the total charge. In such a system, it is possible to "isolate" a small volume, which, in the limit as the volume approaches zero, represents an infinitesimally small charge. At this point, the force felt by an arbitrary test particle becomes a function of the density of charge within this volume.

Mathematically, as the volume $V$ around a charge becomes infinitesimally small, the total force $F$ exerted on a test charge within that volume approaches a limit. This can be expressed as:
$$\begin{align}
\lim_{V\to0}F&=\lim_{V\to0}\int_V\vec{f}(\vec{r},t)\ dV
\end{align}$$
Where $\vec{f}(\vec{r})$ is the infinitesimal force density at each point in the volume. As we make the volume smaller, the total force behaves in such a way that it can be expressed as the derivative of force with respect to charge:
$$\begin{align}
\lim_{V\to0}\dfrac{dF}{dQ}
\end{align}$$
Here, $Q = \int_V \rho(\vec{r}, t)\ dV$ is the total charge within the volume, and $\rho(\vec{r}, t)$ is the charge density at each point.

This equation marks the beginning of our formalization of the electric field, which emerges from the concept of force per unit charge in the infinitesimal limit. The force density itself, which becomes the source of the electric field, is a direct consequence of the charge density $\rho(\vec{r}, t)$ in the same way that we previously described forces between discrete charges.

Similarly, we can consider the force density produced by currents. As we move toward continuous distributions of current, this leads to the birth of the magnetic field, which behaves in much the same way as the electric field, except with current density $\vec{J}$ replacing charge density $\rho$.

Thus, the electric and magnetic fields arise naturally from the consideration of infinitesimal charge and current distributions. This development sets the stage for the formal definitions and equations of electromagnetism, which we will explore in the next chapters. Fields are no longer seen as abstract constructs but as essential quantities that mediate the interactions between charges and currents in space and time.

---
## Chapter 2: Electromagnetic Field Theory












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
#### Superposition of Vector Fields
The electric and magnetic fields obey a simple and powerful property: *linearity*. The total field produced by multiple sources is the vector sum of the field produced by each source individually.

For a system of discrete point charges $q_i$ and positions $\vec{r}_i$ and velocities $\vec{v}_i$, the total electric and magnetic fields at a point $\vec{r}$ are:
$$\begin{align}
\vec{E}(\vec{r})&=\sum_i\dfrac{q_i}{4\pi\epsilon_0}\cdot\dfrac{\vec{r}-\vec{r}_i}{|\vec{r}-\vec{r}_i|^3} && \text{(S1.12, J1.4)}\\
\vec{B}(\vec{r})&=\sum_i\dfrac{\mu_0\vec{j}_i}{4\pi}\times\dfrac{\vec{r}-\vec{r}_i}{|\vec{r}-\vec{r}_i|^3}, \ \ \ \ \vec{j}_i=q_i\vec{v}_i && \text{(S1.13)}
\end{align}$$
For continuous distribution of charges and current, the sums are replaced by integrals over the source densities $\rho(\vec{r}',t)$ and $J(\vec{r}',t)$:
$$\begin{align}
\vec{E}(\vec{r},t)&=\dfrac{1}{4\pi\epsilon_0}\int\rho(\vec{r}',t)\cdot\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}\ d^3r' && \text{(S1.14, J1.5)}\\
\vec{B}(\vec{r},t)&=\dfrac{\mu_0}{4\pi}\int J(\vec{r}',t)\times\dfrac{\vec{r}-\vec{r}'}{|\vec{r}-\vec{r}'|^3}\ d^3r' && \text{(S1.15)}
\end{align}$$
This continuous magnetic field expression is recognized historically as the *Biot-Sovart law* for steady currents, while the continuous electric field generalizes Coulomb's law to extended charge distributions. This superposition principle lets us to construct fields for arbitrarily complex arrangements by summing or integrating contributions from elementary sources. It is also possible to construct discrete source distributions using the Dirac delta function, which is left as an exercise to the reader (Hint: use $S1.1$ and $S1.2$, as well as the superposition principle).

---
### Lorentz Force Law
The motion of a charged particle in the presence of electric and magnetic fields is governed by the *Lorentz force*. A point charge $q$ located at $\vec{r}(t)$ and moving with velocity $\vec{v}(t)$ experiences a force given as the sum of electric and magnetic forces:
$$\begin{align}
\vec{F}(\vec{r},t)&=q\left[\vec{E}(\vec{r},t)+\vec{v}\times\vec{B}(\vec{r},t)\right] && \text{(S1.16)}
\end{align}$$
Here, $\vec{E}$ and $\vec{B}$ are the electric and magnetic fields at the particle's position. The electric term acts along the direction of the field, while the magnetic term is perpendicular to both the velocity and the magnetic field, producing a force that can curve the particle's trajectory.

If the charge is stationary $(\vec{v}=0)$, the Lorentz force reduces to the familiar Coulomb force. For moving charges, the magnetic contribution arises naturally, reflecting the coupling between motion and magnetic fields.

The Lorentz force law provides a general and compact description of how charges respond to electromagnetic fields. It also forms the basis for deriving equations of motion in more specific situations, including electrostatics, magnetostatics, and full electrodynamics in later chapters.

---

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
### Point Charges: Potential Field Formalism
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