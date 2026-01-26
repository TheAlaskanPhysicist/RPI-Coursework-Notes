# A Review of Analytical Mechanics
## Chapter 1.1
These are the notes for the 3rd course in Classical Mechanics at MIT. It is assumed that you have knowledge of Classical Mechanics II before this course. Some references:
 - Goldstein, Poole & Safko, *Classical Mechanics*, 3rd edition.
 - Landau and Lifshitz vol.6, *Fluid Mechanics*.
 - Symon, *Mechanics* for reading material on non-viscous fluids.
 - Strogatz, *Nonlinear Dynamics and Chaos*.
 - Review: Landau & Lifshitz vol.1, *Mechanics*. (Typically used for the prerequisite Classical Mechanics II course and hence useful here for review)

---
## Chapter 1.2
### Newtonian Mechanics
Newtonian mechanics models the dynamics of particles by coordinate trajectories parametrized by time. Newton's second law, $\vec{F}=m\vec{a}$, holds in inertial frames. Non-inertial frames generally have fictitious forces based on coordinate transformation, such as centrifugal forces and the Coriolis effect. Primes will be used to denote coordinate transformations.

In polar coordinates:
$$\begin{align}
\vec{r}&=r\hat{r}\\
\dot{\vec{r}}&=\underbrace{\dot{r}\hat{r}}_{\text{Linear velocity}}+\underbrace{r\dot\theta\hat\theta}_{\text{Angular velocity}}\\
\ddot{\vec{r}}&=\underbrace{\ddot{r}\hat{r}}_{\text{Linear acceleration}}+\underbrace{2\dot{r}\dot\theta\hat\theta}_{\text{Coriolis effect}}+\underbrace{r\left(\ddot\theta\hat\theta-\dot\theta^2\hat{r}\right)}_{\text{Centrifugal force}}\\
\end{align}$$
Even if $\ddot{\vec{r}}=0$, we cannot have a general form as simple as $F_q=m\ddot{q}$. In general, curvilinear coordinates are non-inertial frames, since fictious forces are required to describe why the trajectory remains inertial. This is why we call them "fictitious" forces.

---
### Lagrangian Mechanics
Lagrangian mechanics models the dynamics of a system through a quantity called the Lagrangian:
$$\begin{align}
L\equiv L\left(q,\dot{q},t\right)
\end{align}$$
Here, $q=(q_1,q_2,\dots,q_n)$ denotes the configuration of the system, written as an ordered collection of generalized coordinates; likewise, $\dot{q}=(\dot{q}_1,\dot{q}_2,\dots,\dot{q}_n)$ denotes the ordered collection of time derivatives of the generalized coordinates. The variable $t$ denotes the time parameter.

We often write the form of the Lagrangian in terms of the Kinetic and Potential energies of the system. The most general case is as follows:
$$\begin{align}
L\left(q,\dot{q},t\right)&=\underbrace{T\left(q,\dot{q},t\right)}_\text{Kinetic Energy}-\underbrace{V\left(q,\dot{q},t\right)}_\text{Potential Energy}
\end{align}$$
The solution to a system in Lagrangian form can be found from solving the system of second-order differential equations from the Euler-Lagrange equation(s) of motion:
$$\begin{align}
\dfrac{d}{dt}\left(\dfrac{\partial L}{\partial\dot{q}_i}\right)-\dfrac{\partial L}{\partial q_i}&=0 & \forall i
\end{align}$$
These equations involve $\ddot{q}$ and reproduce Newton's second law. Hamilton's principle, also known as the Principle of Stationary Action:
$$\begin{align}
\delta S&=\delta\int_{t_1}^{t_2}L\left(q,\dot{q},t\right)\ dt=0
\end{align}$$
There are several advantages to using the Lagrangian formalism:
1. It is easier to work with scalars $T$ and $V$ than vectors like $\vec{F}$.
2. The Euler-Lagrange equations are invariant under choice of coordinates.
	1. We can use Euler-Lagrange equations for non-inertial coordinates.
	2. We can formulate $L$ in whatever coordinates are easiest, then change to convenient variables that better describe the symmetry of the system.
3. It is very easy to add constraints to the Lagrangian, such as parametric pathing.

## Hamiltonian Mechanics
In Hamiltonian mechanics, the canonical momenta $p_i\equiv\dfrac{\partial L}{\partial\dot{q}_i}$ are promoted to coordinates on equal footing with the generalized coordinates $q_i$. These coordinates, $(q,p)$ are called canonical variables, and the space of canonical variables is known as *phase space*.