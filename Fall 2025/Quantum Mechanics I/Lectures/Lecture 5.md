Author: Stanley Goodwin
Date: XX, 2025

---
### Position, Momentum, and Translations
Define an infinitesimal spatial translation:
$$\begin{align}
J(dx)\ket{x}=\ket{x+dx}
\end{align}$$
Suppose we linearize this system about the point $x$ so $J(0)=\mathbb{I}$.

Let the operator have the following form:
$$\begin{align}
J(dx)&=e^{-ik\cdot dx}
\end{align}$$
When applied to a state $\ket{x}$, we see that:
$$\begin{align}
\left[J(dx),e^{-ik\cdot dx}\right]\ket{x}&=J(dx)e^{-ik\cdot dx}\ket{x}-e^{-ik\cdot dx}J(dx)\ket{x}\\
J(dx)e^{-ik\cdot dx}\ket{x}-\left[J(dx),e^{-ik\cdot dx}\right]\ket{x}&=e^{-ik\cdot dx}\ket{x+dx}\\


\end{align}$$


&=\sum_{n=0}^\infty\dfrac{\left(-ik\cdot dx\right)^n}{n!}\ket{x}
...





From observation, we can see the following ideals:
$$\begin{align}
J(-dx)J(dx)\ket{x}&=\ket{x} &\implies&& J(dx)^{-1}=J(-dx)\\
J^\dagger(dx)J(dx)\ket{x}&=\ket{x} &\implies&& J(dx)^{-1}=J^\dagger(dx)\\
J(dx)J(dx)\ket{x}&=J(2dx)\ket{x} &\implies&& J^a(dx)=J^\dagger(a\cdot dx)\\
\end{align}$$

