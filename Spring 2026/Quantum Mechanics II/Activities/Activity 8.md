**Author:** Stanley Goodwin
**Date:** April 8th, 2026

---
> Show that the current four-vector,
> $$\begin{align}
j^\mu\equiv\dfrac{i}{2m}\left[\psi^*\partial^\mu\psi-\psi\ \partial^\mu\psi^*\right]
\end{align}$$
> where $\psi(\vec{x},t)$ is a solution to the Klein-Gordon equation, satisfies the continuity equation
> $$\begin{align}
\partial_\mu j^\mu&=0
\end{align}$$

If we apply the differential operator to the current above, we can use the chain rule to find
$$\begin{align}
\partial_\mu j^\mu&\equiv\dfrac{i}{2m}\partial_\mu\left[\psi^*\partial^\mu\psi-\psi\ \partial^\mu\psi^*\right]\\
&=\dfrac{i}{2m}\left[\cancel{\partial_\mu\psi^*\partial^\mu\psi}+\psi^*\partial_\mu\partial^\mu\psi-\cancel{\partial_\mu\psi\ \partial^\mu\psi^*}-\psi\ \partial_\mu\partial^\mu\psi^*\right]
\end{align}$$
From the Klein-Gordon equation, we know the relationship
$$\begin{align}
(\partial_\mu\partial^\mu+m^2)\psi&=0 &\implies&& \partial_\mu\partial^\mu\psi&=-m^2\psi
\end{align}$$
Substituting, we see that:
$$\begin{align}
\partial_\mu j^\mu&=\dfrac{i}{2m}\left[\psi^*\partial_\mu\partial^\mu\psi-\psi\ \partial_\mu\partial^\mu\psi^*\right]\\
&=\dfrac{i}{2m}\left[-m^2\psi^*\psi+m^2\psi\psi^*\right]\\
\Aboxed{\partial_\mu j^\mu&=0}
\end{align}$$
