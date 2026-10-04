**Author:** Stanley Goodwin
**Date:** August 31st, 2026

---
## Question 1
> Compute $$\begin{align}\left[a,(a^\dagger)^n\right]\end{align}$$

Let $f_n=\left[a,(a^\dagger)^n\right]$, where $f_1=\left[a,a^\dagger\right]=1$. Using the commutator identity
$$\begin{align}
[A,BC]&=[A,B]C+B[A,C]
\end{align}$$
where $A=a$, $B=a^\dagger$, and $C=(a^\dagger)^{n-1}$, our operation becomes
$$\begin{align}
f_n&=\left[a,a^\dagger(a^\dagger)^{n-1}\right]\\
&=\left[a,a^\dagger\right](a^\dagger)^{n-1}+a^\dagger\left[a,(a^\dagger)^{n-1}\right]\\
f_n&=(a^\dagger)^{n-1}+a^\dagger f_{n-1}
\end{align}$$
Using our base case of $f_1=\left[a,a^\dagger\right]=1$, the recursion simplifies to the direct expression
$$\begin{align}
f_n&=k(a^\dagger)^{n-1}+(a^\dagger)^kf_{n-k}\\
\Aboxed{\left[a,(a^\dagger)^n\right]&=n(a^\dagger)^{n-1}}
\end{align}$$

---
## Question 2
> Compute $$\begin{align}\left[a^\dagger a,(a^\dagger)^n\right]\end{align}$$

Using the commutator identity
$$\begin{align}
[AB,C]&=A[B,C]+[A,C]B
\end{align}$$
where $A=a^\dagger$, $B=a$, and $C=(a^\dagger)^n$, our commutator becomes
$$\begin{align}
\left[a^\dagger a,(a^\dagger)^n\right]
&=a^\dagger\left[a,(a^\dagger)^n\right]+\left[a^\dagger,(a^\dagger)^n\right]a
\end{align}$$
Our first commutator can be found from [[#Question 1]], and the second commutator is $0$, thus
$$\begin{align}
\Aboxed{\left[a^\dagger a,(a^\dagger)^n\right]&=n(a^\dagger)^{n}}
\end{align}$$

---
## Question 3
> What would [[#Question 1]] and [[#Question 2]] equal if you put subscript $\vec{p}$ on the operators on the left-hand side of the commutator and $\vec{q}$ on the right hand side of the commutator?

Each term would have an extra delta function $\delta(\vec{p}-\vec{q})$, thus the identities become
$$\begin{align}
\Aboxed{\left[a_\vec{p},(a_\vec{q}^\dagger)^n\right]&=n(a^\dagger)^{n-1}\delta(\vec{p}-\vec{q})}
\Aboxed{\left[a_\vec{p}^\dagger a_\vec{p},(a_\vec{q}^\dagger)^n\right]&=n(a^\dagger)^{n}\delta(\vec{p}-\vec{q})}
\end{align}$$

---
## Question 4
> From [[#Question 3]], what are the implications for the energy eigenstates of the Klein-Gordon theory?

The occupation at each point in space is independent. Energy eigenstates are dependent on configurations at each site occupation, written as
$$\begin{align}
\mathcal{H}&=E_\vec{p}n_\vec{p}=\sqrt{\vec{p}^2+m^2}\ a_\vec{p}^\dagger a_\vec{p}
&\implies&&
H&=\int\dfrac{d^3p}{(2\pi)^3}\sqrt{p^2+m^2}\ a_\vec{p}^\dagger a_\vec{p}
\end{align}$$
