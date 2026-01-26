## Higher Order Lagrangians
Lagrangian mechanics models the dynamics of a system through a quantity called the Lagrangian. However, to incorporate higher time derivatives into this system, we let:
$$\begin{align}
L\equiv L\left(q^{(0)},q^{(1)}\dots,q^{(k)},t\right)
\end{align}$$
Here, $q^{(0)}=(q_1,q_2,\dots,q_n)$ denotes the configuration of the system, written as an ordered collection of generalized coordinates; likewise, $q^{(i)}$ denotes the ordered collection of $i$th time derivatives of the generalized coordinates. The variable $t$ denotes the time parameter.

The solution to a system in Lagrangian form can be found from solving the system of $(k+1)$-order differential equations from the Euler-Lagrange equation(s) of motion:
$$\begin{align}
\sum_{l=0}^{k}(-1)^l\dfrac{\partial^l}{\partial t^l}\left(\dfrac{\partial L}{\partial q_i^{(l)}}\right)&=0 & \forall i
\end{align}$$
We can make these derivatives into their own independent coordinates. Introduce the following:
$$\begin{align}
Q_i=q^{(i)}
\end{align}$$
Then the momenta are defined as the following:
$$\begin{align}
P_r&=\sum_{s=r+1}^{k}(-1)^{s-r-1}\dfrac{\partial^{s-r-1}}{\partial t^{s-r-1}}\left(\dfrac{\partial L}{\partial q^{(s)}}\right) & r=0,1,\dots,k-1
\end{align}$$
For invertibility, we also have to know that:
$$\begin{align}
\det\left(\dfrac{\partial^2L}{\partial q_i^{(k)}q_j^{(k)}}\right)\ne0
\end{align}$$
If this fails, it imposes constraints as seen in Dirac -Bergmann theory.

The Hamiltonian is then:
$$\begin{align}
H\equiv\sum_{r=0}^{k-1}P_rQ_{r+1}-L\left(q^{(0)},q^{(1)}\dots,q^{(k)},t\right)
\end{align}$$







---
## Higher Order Lagrangians
Let the Lagrangian and Action take the form:
$$\begin{align}
L&\equiv L\left(q^{(0)},q^{(1)},\dots,q^{(n)},t\right) & S[q]&\equiv\int L\left(q^{(0)},q^{(1)}\dots,q^{(n)},t\right)\ dt
\end{align}$$
Taking the differential of the Lagrangian Action, we can see that:
$$\begin{align}
\delta S[q]&=\int_{t_2}^{t_1}\sum_{k=0}^n\left(\dfrac{\partial L}{\partial q^{(k)}}\delta q^{(k)}\right)\ dt
\end{align}$$
We can find the general form of the Integration by Parts as well:
$$\begin{align}
\int_{t_2}^{t_1}\dfrac{\partial L}{\partial q^{(k)}}\delta q^{(k)}dt
&=\left[\sum_{s=0}^{k-1}(-1)^{s}\dfrac{d^{s}}{dt^{s}}\dfrac{\partial L}{\partial q^{(k)}}\delta q^{(k-1-s)}\right]_{t_2}^{t_1}+(-1)^k\dfrac{d^k}{dt^k}\int_{t_2}^{t_1}\dfrac{\partial L}{\partial q^{(k)}}\delta q^{(0)}dt\\
\end{align}$$
Thus the variation in Action is then:
$$\begin{align}
\delta S[q]&=\sum_{k=0}^n\left[\sum_{s=0}^{k-1}(-1)^{s}\dfrac{d^{s}}{dt^{s}}\dfrac{\partial L}{\partial q^{(k)}}\delta q^{(k-1-s)}\right]_{t_2}^{t_1}+\int_{t_2}^{t_1}\left(\sum_{k=0}^n(-1)^k\dfrac{d^k}{dt^k}\dfrac{\partial L}{\partial q^{(k)}}\right)\delta q^{(0)}dt\\
0&=\sum_{k=0}^n(-1)^k\dfrac{d^k}{dt^k}\left(\dfrac{\partial L}{\partial q^{(k)}}\right)\\
\delta S_\text{boundary}[q]&=\sum_{k=0}^n\sum_{s=0}^{k-1}(-1)^{s}\dfrac{d^{s}}{dt^{s}}\dfrac{\partial L}{\partial q^{(k)}}\delta q^{(k-1-s)}
\end{align}$$
Reindexing the sum so that we find different orders of $\delta q$.
$$\begin{align}
\delta S_\text{boundary}[q]&=\sum_{k=0}^{n-1}\underbrace{\left(\sum_{s=k+1}^{n}(-1)^{s-1-k}\dfrac{d^{s-1-k}}{dt^{s-1-k}}\dfrac{\partial L}{\partial q^{(s)}}\right)}_{p^{(k)}}\delta q^{k}\\
\end{align}$$
We can then see a new basis for our canonical coordinates:
$$\begin{align}
q^{(k)}&=\dfrac{d^k}{dt^k}q & p^{(k)}&=\sum_{s=k+1}^{n}(-1)^{s-1-k}\dfrac{d^{s-1-k}}{dt^{s-1-k}}\dfrac{\partial L}{\partial q^{(s)}}
\end{align}$$
We can invert the differential relationship to see that:
$$\begin{align}
\dfrac{\partial L}{\partial q^{(r+1)}}&=\sum_{s=r}^{n-1}\dfrac{d^{s-r}}{dt^{s-r}}p^{(s)}
\end{align}$$
Recalling from the typical derivation of the Hamiltonian system, we have:
$$\begin{align}
q_\text{canonical}&=q & p_\text{canonical}&=\dfrac{\partial L}{\partial\dot{q}}
\end{align}$$
The position coordinate $q$ remains unchanged, and all time derivatives are implicit as expected for typical Lagrangian systems. However, the canonical momentum does change in terms of the other momentum coordinates. Substituting $r=0$ to the 2nd above, we get:
$$\begin{align}
p_\text{canonical}&=\sum_{s=0}^{n-1}\dfrac{d^{s}}{dt^{s}}p^{(s)}
\end{align}$$
This choice of momentum basis is the nature momentum basis, and might not correspond to a true momentum of a system, nor its time derivatives, such as force.

---
## Smooth Coordinates & Lagrangians
Suppose our coordinates are smooth, and thus have infinite differentiability.
Let the Lagrangian and Action take the form:
$$\begin{align}
L&\equiv L\left(\mathfrak{q},t\right) & S[\mathfrak{q}]&\equiv\int L\left(\mathfrak{q},t\right)\ dt
\end{align}$$
where $\mathfrak{q}=\left(q^{(0)},q^{(1)},\dots,q^{(\infty)}\right)$, as in the ordered list of all the coordinates and their time derivatives. indexed $\mathfrak{q}_i=q^{(i)}$, where $i\ge0$.

The Euler-Lagrange Equation for the dynamics of this system can be expressed as:
$$\begin{align}
\sum_{k=0}^\infty(-1)^k\dfrac{d^k}{dt^k}\left(\dfrac{\partial L}{\partial \mathfrak{q}_k}\right)&=\dfrac{\partial L}{\partial q}-\dfrac{d}{dt}\dfrac{\partial L}{\partial\dot{q}}+\dfrac{d^2}{dt^2}\dfrac{\partial L}{\partial\ddot{q}}+\dots=0
\end{align}$$
The new canonical coordinates for position and momentum are then:
$$\begin{align}
\mathfrak{q}_k=q^{(k)}&=\dfrac{d^k}{dt^k}q &&&\mathfrak{p}_k=p^{(k)}&=\sum_{s=k+1}^{\infty}(-1)^{s-1-k}\dfrac{d^{s-1-k}}{dt^{s-1-k}}\dfrac{\partial L}{\partial q^{(s)}}
\end{align}$$
For each index $k$, we have:
$$\begin{align}
\left\{\mathfrak{q}_i,\mathfrak{p}_j\right\}&=\delta_{ij} & 
\left\{\mathfrak{q}_i,\mathfrak{q}_j\right\}&=0 & 
\left\{\mathfrak{p}_i,\mathfrak{p}_j\right\}&=0
\end{align}$$





Suppose we want to do something similar to Hamilton's principle. 
Let $S$ be Hamilton's principle function, $S(\mathfrak{q},t)$, that satisfies:
$$\begin{align}
\mathfrak{p}_k&=\dfrac{\partial S}{\partial\mathfrak{q}_k}
\end{align}$$
Then we can write the Hamiltonian as:
$$\begin{align}
H\left(\mathfrak{q},\mathfrak{p}=\dfrac{\partial S}{\partial\mathfrak{q}},t\right)&=\sum_{k=0}^\infty\dfrac{\partial S}{\partial\mathfrak{q}_k}\partial\mathfrak{q}_{k+1}-L(\mathfrak{q},t)
\end{align}$$
The corresponding Hamilton-Jacobi equation is then:
$$\begin{align}
\dfrac{\partial S}{\partial t}+H\left(\mathfrak{q},\dfrac{\partial S}{\partial\mathfrak{q}},t\right)
\end{align}$$











Note: The canonical momentum here might not necessarily correspond to physical momentum that we would observe in a system. Instead, we would have to invert the relation to find:
$$\begin{align}
p_\text{canonical}&=\sum_{s=0}^{\infty}\dfrac{d^{s}}{dt^{s}}p^{(s)}
\end{align}$$





$$\begin{align}
\dfrac{\partial L}{\partial q^{(r+1)}}&=\sum_{s=r}^{n-1}\dfrac{d^{s-r}}{dt^{s-r}}p^{(s)}
\end{align}$$




Framing it explicitly as a Lie group action in infinite-dimensional phase space could be new?
I haven't found it in literature.
















---

## Example: Second Order Time Lagrangian
Let the Lagrangian and Action take the form:
$$\begin{align}
L&\equiv L\left(q,\dot{q},\ddot{q},t\right) & S[q]&\equiv\int L\left(q,\dot{q},\ddot{q},t\right)\ dt
\end{align}$$
Taking the differential of the Lagrangian Action, we can see that:
$$\begin{align}
\delta S[q]&=\int_{t_2}^{t_1}\left(\dfrac{\partial L}{\partial q}\delta q+\dfrac{\partial L}{\partial\dot{q}}\delta\dot{q}+\dfrac{\partial L}{\partial\ddot{q}}\delta\ddot{q}\right)\ dt
\end{align}$$
For reference, the following Integration by Parts solutions can be used:
$$\begin{align}
\int_{t_2}^{t_1}\dfrac{\partial L}{\partial\dot{q}}\delta\dot{q}\ dt&=
\left[\dfrac{\partial L}{\partial\dot{q}}\delta q\right]_{t_2}^{t_1}
-\int_{t_2}^{t_1}\dfrac{d}{dt}\dfrac{\partial L}{\partial\dot{q}}\delta q\ dt\\
\int_{t_2}^{t_1}\dfrac{\partial L}{\partial\ddot{q}}\delta\ddot{q}\ dt&=
\left[\dfrac{\partial L}{\partial\ddot{q}}\delta\dot{q}-\dfrac{d}{dt}\dfrac{\partial L}{\partial\ddot{q}}\delta q\right]_{t_2}^{t_1}
+\int_{t_2}^{t_1}\dfrac{d^2}{dt^2}\dfrac{\partial L}{\partial\ddot{q}}\delta q\ dt
\end{align}$$
This splits the integral into an integral with a multiplicative factor of $\delta q$ and an evaluation at the bounds of the integral:
$$\begin{align}
\delta S[q]&=\left[\dfrac{\partial L}{\partial\dot{q}}\delta q+\dfrac{\partial L}{\partial\ddot{q}}\delta\dot{q}-\dfrac{d}{dt}\dfrac{\partial L}{\partial\ddot{q}}\delta q\right]_{t_2}^{t_1}+\int_{t_2}^{t_1}\left(\dfrac{\partial L}{\partial q}-\dfrac{d}{dt}\dfrac{\partial L}{\partial\dot{q}}+\dfrac{d^2}{dt^2}\dfrac{\partial L}{\partial\ddot{q}}\right)\delta q\ dt\\
\delta S_\text{boundary}[q]&=\underbrace{\left[\dfrac{\partial L}{\partial\dot{q}}-\dfrac{d}{dt}\dfrac{\partial L}{\partial\ddot{q}}\right]}_{p^{(0)}}\delta q+\underbrace{\left[\dfrac{\partial L}{\partial\ddot{q}}\right]}_{p^{(1)}}\delta\dot{q}=p^{(0)}\delta q^{(0)}+p^{(1)}\delta q^{(1)}\\
\end{align}$$
We can then see a new basis for our canonical coordinates:
$$\begin{align}
q^{(0)}&=q & p^{(0)}&=\dfrac{\partial L}{\partial\dot{q}}-\dfrac{d}{dt}\dfrac{\partial L}{\partial\ddot{q}}\\
q^{(1)}&=\dot q & p^{(1)}&=\dfrac{\partial L}{\partial\ddot{q}}\\
\end{align}$$
Recalling from the typical derivation of the Hamiltonian system, we have:
$$\begin{align}
q_\text{canonical}&=q & p_\text{canonical}&=\dfrac{\partial L}{\partial\dot{q}}
\end{align}$$
Our new coordinates are very similar, and can be substituted as:
$$\begin{align}
q^{(0)}&=q_\text{canonical} & p^{(0)}&=p_\text{canonical}-\dfrac{d}{dt}p^{(1)}\\
q^{(1)}&=\dfrac{d}{dt}q_\text{canonical} & p^{(1)}&=\dfrac{\partial L}{\partial\ddot{q}}\\
\end{align}$$
Switching it around, we can write this instead as:
$$\begin{align}
q_\text{canonical}&=q^{(0)} & p_\text{canonical}&=p^{(0)}+\dfrac{d}{dt}p^{(1)}
\end{align}$$
This shows that adding extra differentials of $q$ only affects the canonical momentum, not the canonical position. It is also apparent from the structure of the mathematics here that this is effectively a perturbative approach to the Lagrangian in time.

However, it should be noted that the configuration (phase) space is larger in the case of $k=2$, since we need to consider both canonical coordinates and both time derivatives.










Together, we see that the new coordinates are as follows:
$$\begin{align}
q^{(0)}&=q=q_\text{canonical} & p^{(0)}&=\dfrac{\partial L}{\partial\dot{q}}-\dfrac{d}{dt}\dfrac{\partial L}{\partial\ddot{q}}=p_\text{canonical}-\dfrac{d}{dt}p^{(1)}\\
q^{(1)}&=\dot{q} & p^{(1)}&=\dfrac{\partial L}{\partial\ddot{q}}
\end{align}$$
The form of $\ddot{q}$ is interesting. We can see its dependence as:
$$\begin{align}
\ddot{q}&=\ddot{q}\left(q^{(0)}, q^{(1)}, p^{(1)}\right)
\end{align}$$
In order for this transformation to be allowed, it must be invertible. Thus:
$$\begin{align}
\dfrac{\partial^2L}{\partial\ddot{q}^2}\ne0
\end{align}$$
The Hamiltonian is then pretty easily shown to be (through Legendre Transform):
$$\begin{align}
H\left(q^{(0)},q^{(1)},p^{(0)},p^{(1)}\right)&=p^{(0)}q^{(1)}+P_1\ddot{q}\left(q^{(0)}, q^{(1)}, p^{(1)}\right)-L\left(q^{(0)}, q^{(1)},\ddot{q}\left(q^{(0)}, q^{(1)}, p^{(1)}\right)\right)
\end{align}$$
The corresponding Hamilton's equations are then:
$$\begin{align}
\dot q^{(0)}&=\dfrac{\partial H}{\partial p^{(0)}} &
\dot p^{(0)}&=-\dfrac{\partial H}{\partial q^{(0)}}\\
\dot q^{(1)}&=\dfrac{\partial H}{\partial p^{(1)}} & 
\dot p^{(1)}&=-\dfrac{\partial H}{\partial q^{(1)}}
\end{align}$$






Well what I'm really looking for is that I wanted to figure out a way to start from the most general form of the lagrangian with coordinates, and then say "Okay, so here's the equations. Now, lets look at the linearization about the null (geodesic?) and see if we get something like Schrodingers' equation? It feels like there should, in the end, be a very obvious construction that allows things like the Euler-Lagrange Equation to more be like e^{Operator} L = 0 (because the order the derivatives keep increasing), and thus we're looking basically at the null space of the Lie Group, and thus there are special Lie Algebra elements and parametrizations that reduce L to 0.



The idea is like this:
$$\begin{align}
\hat{\mathcal{E}}&=\sum_{k=0}^\infty(-1)^k\dfrac{d^k}{dt^k}\dfrac{\partial}{\partial \mathfrak{q}_k} & \hat{\mathcal{E}}L=0
\end{align}$$
Suppose we have a solution $L_0$, then:
$$\begin{align}
\hat{\mathcal{E}}L_0&=0& \implies&&\hat{\mathcal{E}}(L_0+\delta L)&=\hat{\mathcal{E}}\delta L=0
\end{align}$$
Imagine then that $\hat{\mathcal{E}}$ is an element of a Lie Algebra of operators acting on Lagrangians:
$$\begin{align}
\delta L(t)&=e^{i\hat{\mathcal{E}t}}\delta L(0)
\end{align}$$
Different operators -> Different symmetries or conserved flows?

Main idea: "Can I generate the space of all configurations of a smooth coordinate manifold from the local behavior of the geodesic"




Conceptual Idea:
$$\begin{align}
\int_a^bdF&=\int_a^b\dfrac{\partial F}{\partial x}dx\\
\end{align}$$
If there's something about the subspace being complete on a finite interval, then $F$ exists.
If a subspace isn't complete on finite, there does not exist an $F$ (non-elementary function).
Either way, that's why some integrals don't have finite forms, but do have values over the whole interval, as if it was integrated over it's whole subspace, like the completeness relation.

Going from $dF\rightarrow (dF/dx)dx$ is quite literally like projection of $F$ onto an $x$ basis.






