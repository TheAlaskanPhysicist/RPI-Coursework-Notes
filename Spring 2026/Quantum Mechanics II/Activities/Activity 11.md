**Author:** Stanley Goodwin
**Date:** April 13th, 2026

---
## Question 1
> Prove the continuity equation $$\dfrac{\partial\rho}{\partial t}+\vec\nabla\cdot\vec{J}=0$$ where $\rho=\Psi^\dagger\Psi$, $\vec{J}=\Psi^\dagger\vec\alpha\Psi$, and $\Psi(\vec{x},t)$ satisfies the Dirac equation $$i\partial_t\Psi=\left[\vec\alpha\cdot(-i\vec\nabla)+\beta m\right]\Psi$$

It will be useful to write the Dirac equation for both $\Psi$ and $\Psi^\dagger$, being
$$\begin{align}
i\partial_t\Psi&=-i\vec\alpha\cdot\vec\nabla\Psi+m\beta\Psi
&\implies&& 
i\partial_t\Psi^\dagger &=-i\vec\nabla\Psi^\dagger\cdot\vec\alpha-m\Psi^\dagger\beta
\end{align}$$
If we differentiate $\rho$ with respect to time, we can use the relations to find
$$\begin{align}
i\partial_t\rho&=i\partial_t(\Psi^\dagger\Psi)\\
&=(i\partial_t\Psi^\dagger)\Psi+\Psi^\dagger(i\partial_t\Psi)\\
&=(-i\vec\nabla\Psi^\dagger\cdot\vec\alpha-m\Psi^\dagger\beta)\Psi+\Psi^\dagger(-i\vec\alpha\cdot\vec\nabla\Psi+m\beta\Psi)\\
&=-i\left(\vec\nabla\Psi^\dagger\cdot\vec\alpha\right)\Psi-\cancel{m\Psi^\dagger\beta\Psi}-i\Psi^\dagger\left(\vec\alpha\cdot\vec\nabla\Psi\right)+\cancel{m\Psi^\dagger\beta\Psi}\\
&=-i\left[\left(\vec\nabla\Psi^\dagger\cdot\vec\alpha\right)\Psi+\Psi^\dagger\left(\vec\alpha\cdot\vec\nabla\Psi\right)\right]\\
&=-i\vec\nabla\cdot\left(\Psi^\dagger\vec\alpha\Psi\right)\\
i\partial_t\rho&=-i\vec\nabla\cdot\vec{J}\\
\Aboxed{\partial_t\rho+\vec\nabla\cdot\vec{J}&=0}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

## Question 2
---
### Question 2.A
> For a free particle $\Psi\propto e^{-ip_\mu x^\mu}$, show that $\left(\gamma^\mu p_\mu-m\right)\Psi=0$.

We can write our free particle wavefunction and the momentum operator in spacetime as
$$\begin{align}
\Psi&\equiv Ce^{-ip_\mu x^\mu} & p_\mu&=i\dfrac{\partial}{\partial x^\mu}
\end{align}$$
We now act the operator $\left(\gamma^\mu p_\mu-m\right)$ on $\Psi$ to find
$$\begin{align}
\left(\gamma^\mu p_\mu-m\right)\Psi
&=\left(i\gamma^\mu\dfrac{\partial}{\partial x^\mu}-m\right)Ce^{-ip_\mu x^\mu}\\
&=i\gamma^\mu\dfrac{\partial}{\partial x^\mu}Ce^{-ip_\mu x^\mu}-mCe^{-ip_\mu x^\mu}\\
&=i\gamma^\mu(-ip_\mu)Ce^{-ip_\mu x^\mu}-mCe^{-ip_\mu x^\mu}\\
&=\gamma^\mu p_\mu Ce^{-ip_\mu x^\mu}-mCe^{-ip_\mu x^\mu}\\
&=\left(\gamma^\mu p_\mu-m\right)Ce^{-ip_\mu x^\mu}
\end{align}$$
In order for this to be zero for all points in spacetime, we have that
$$\begin{align}
\Aboxed{\left(\gamma^\mu p_\mu-m\right)C&=0}
\end{align}$$
Not sure if this is what was being asked for. But another way is to apply
$$\begin{align}
\left(\gamma^\mu p_\mu-m\right)\left(\gamma^\nu p_\nu+m\right)C&=(p^2-m^2)C=0
\end{align}$$
Since $C$ was arbitrary, we could change the definition to be so that
$$\begin{align}
\Psi&\equiv\left(\gamma^\nu p_\nu+m\right)Ce^{-ip_\mu x^\mu}=C'(p)e^{-ip_\mu x^\mu}
\end{align}$$
Hopefully this is somewhat what you were intending.


<div style="page-break-before: always;"></div>*PDF next page*

### Question 2.B
> For a free particle $\Psi\propto e^{-ip_\mu x^\mu}$, show that $\bar\Psi\left(\gamma^\mu p_\mu-m\right)=0$.

Since we already proved the Dirac equation satisfiability for our plane wave, we can use it to solve for the Dirac adjoint (I remembered the name!)
$$\begin{align}
\left(\gamma^\mu p_\mu-m\right)\Psi&=0 & \bar\Psi&\equiv\Psi^\dagger\gamma^0
\end{align}$$
Start with taking the Hermitian conjugate of the Dirac equation
$$\begin{align}
\left(\gamma^\mu p_\mu-m\right)\Psi&=0 &\implies&& \Psi^\dagger\left(\gamma^{\dagger\mu} p_\mu-m\right)&=0
\end{align}$$
We need the Hermitian conjugate of the gamma matrices. After some experimenting, we find the following relationship that will be helpful in simplifying
$$\begin{align}
\gamma^0\gamma^{\dagger\mu}\gamma^0&=\gamma^\mu
&\implies&&
\gamma^{\dagger\mu}&=\gamma^0\gamma^\mu\gamma^0
\end{align}$$
as well as $(\gamma^0)^2=1$, so we can add it as a factor on $m$. Substituting, we have then that
$$\begin{align}
\Psi^\dagger\left(\gamma^{\dagger\mu} p_\mu-m\right)
&=\Psi^\dagger\left(\gamma^0\gamma^\mu\gamma^0p_\mu-m\gamma^0\gamma^0\right)\\
&=\Psi^\dagger\left(\gamma^0\gamma^\mu p_\mu\gamma^0-\gamma^0m\gamma^0\right)\\
0&=\Psi^\dagger\gamma^0\left(\gamma^\mu p_\mu-m\right)\gamma^0\\
\end{align}$$
We can multiply $\gamma^0$ to the right of each side, and use $\bar\Psi\equiv\Psi^\dagger\gamma^0$ to finally arrive to
$$\begin{align}
\Aboxed{\bar\Psi\left(\gamma^\mu p_\mu-m\right)&=0}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 2.C
> For a free particle $\Psi\propto e^{-ip_\mu x^\mu}$, show that $j^\mu=\bar\Psi\gamma^\mu\Psi=\dfrac{p^\mu}{m}\bar\Psi\Psi$.

From [[#Question 2.A|part a]] and [[#Question 2.B|part b]], we can write them to be the equivalences
$$\begin{align}
\gamma^\mu p_\mu\Psi&=m\Psi &\text{and}&& \bar\Psi\gamma^\mu p_\mu&=m\bar\Psi
\end{align}$$
I assume we are allowed to set the definition of current $j^\mu\equiv\bar\Psi\gamma^\mu\Psi$. From the form of the Dirac equation, contract both sides by $p_\mu$. Being careful with rearrangement, we get that
$$\begin{align}
p_\mu j^\mu&=\bar\Psi\left(\gamma^\mu p_\mu\right)\Psi
\end{align}$$
The last 3 terms look like our Dirac equation, so we can substitute the equivalence in have
$$\begin{align}
p_\mu j^\mu&=m\bar\Psi\Psi
\end{align}$$
Time to use the metric tensor. Start by using the metric tensor to make momentum contravariant, then multiply both sides by $g^{\nu\lambda}p_\nu$. Procedurally, it looks like
$$\begin{align}
p_\mu j^\mu&=m\bar\Psi\Psi \\
g_{\mu\nu}p^\nu j^\mu&=m\bar\Psi\Psi \\
g_{\mu\nu}g^{\nu\lambda}p_\nu p^\nu j^\mu&=g^{\nu\lambda}p_\nu m\bar\Psi\Psi\\
\delta_\mu^\lambda\cdot m^2\cdot j^\mu&=g^{\nu\lambda}p_\nu m\bar\Psi\Psi\\
j^\mu&=g^{\nu\mu}p_\nu \dfrac{m}{m^2}\bar\Psi\Psi\\
j^\mu&=g^{\mu\nu}p_\nu \dfrac{1}{m}\bar\Psi\Psi\\
\Aboxed{j^\mu&=\dfrac{p^\mu}{m}\bar\Psi\Psi}
\end{align}$$
