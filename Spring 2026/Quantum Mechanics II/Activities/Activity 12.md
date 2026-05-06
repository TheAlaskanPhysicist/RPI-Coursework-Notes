**Author:** Stanley Goodwin
**Date:** April 18th, 2026

---
## Question 1
> Show that $$\left(\tilde{p}\times\tilde{p}\right)f(\vec{x})=ie\vec{B}f(\vec{x})$$ where $\tilde{p}=-i\vec\nabla-e\vec{A}(\vec{x})$, $\vec{A}(\vec{x})$ is the vector potential, and $f(\vec{x})$ is an arbitrary function.

We can substitution our expression for $\tilde{p}$ and simplify to
$$\begin{align}
\left(\tilde{p}\times\tilde{p}\right)f(\vec{x})
&=\left(-\tilde{p}\times-\tilde{p}\right)f(\vec{x})\\
&=\left(i\vec\nabla+e\vec{A}(\vec{x})\right)\times\left(i\vec\nabla f(\vec{x})+e\vec{A}(\vec{x})f(\vec{x})\right)\\
&=i\vec\nabla\times\left(i\vec\nabla f(\vec{x})+e\vec{A}(\vec{x})f(\vec{x})\right)+e\vec{A}(\vec{x})\times\left(i\vec\nabla f(\vec{x})+e\vec{A}(\vec{x})f(\vec{x})\right)\\
&=i^2\vec\nabla\times\left(\vec\nabla f(\vec{x})\right)+ie\vec\nabla\times\left(\vec{A}(\vec{x})f(\vec{x})\right)+ie\vec{A}(\vec{x})\times\left(\vec\nabla f(\vec{x})\right)+e^2\left(\vec{A}(\vec{x})\times\vec{A}(\vec{x})\right)f(\vec{x})
\end{align}$$
We'll need the product rule for the curl
$$\begin{align}
\vec\nabla\times(\vec{F}f)&=\left(\vec\nabla f\right)\times \vec{F}+f\left(\vec\nabla\times\vec{F}\right)
\end{align}$$
In our case, we have
$$\begin{align}
\vec\nabla\times(\vec{A}(\vec{x})f)&=\left(\vec\nabla f(\vec{x})\right)\times \vec{A}(\vec{x})+f(\vec{x})\left(\vec\nabla\times\vec{A}(\vec{x})\right)=-\vec{A}(\vec{x})\times\left(\vec\nabla f(\vec{x})\right)+\left(\vec\nabla\times\vec{A}(\vec{x})\right)f(\vec{x})
\end{align}$$
Substituting back in, we have
$$\begin{align}
\left(\tilde{p}\times\tilde{p}\right)f(\vec{x})
&=-\vec\nabla\times\left(\vec\nabla f(\vec{x})\right)+ie\vec\nabla\times\left(\vec{A}(\vec{x})f(\vec{x})\right)+ie\vec{A}(\vec{x})\times\left(\vec\nabla f(\vec{x})\right)+e^2\left(\vec{A}(\vec{x})\times\vec{A}(\vec{x})\right)f(\vec{x})\\
&=0-\cancel{ie\vec{A}(\vec{x})\times\left(\vec\nabla f(\vec{x})\right)}+ie\left(\vec\nabla\times\vec{A}(\vec{x})\right)f(\vec{x})+\cancel{ie\vec{A}(\vec{x})\times\left(\vec\nabla f(\vec{x})\right)}+0\\
&=ie\left(\vec\nabla\times\vec{A}(\vec{x})\right)f(\vec{x})\\
\Aboxed{\left(\tilde{p}\times\tilde{p}\right)f(\vec{x})&=ie\vec{B}(\vec{x})f(\vec{x})}
\end{align}$$


<div style="page-break-before: always;"></div>*PDF next page*

## Question 2
> Show that $$\left[\alpha_i,\Sigma_j\right]=2i\varepsilon_{ijk}\alpha_k$$ where $\alpha=\begin{bmatrix}0&\vec\sigma\\\vec\sigma&0\end{bmatrix}$ and $\Sigma=\begin{bmatrix}\vec\sigma&0\\0&\vec\sigma\end{bmatrix}$.

Each component has the following form
$$\begin{align}
\alpha_i&=\begin{bmatrix}0&\sigma_i\\\sigma_i&0\end{bmatrix} & \Sigma_j&=\begin{bmatrix}\sigma_j&0\\0&\sigma_j\end{bmatrix}
\end{align}$$
Each matrix product is
$$\begin{align}
\alpha_i\Sigma_j
&=\begin{bmatrix}0&\sigma_i\\\sigma_i&0\end{bmatrix}\begin{bmatrix}\sigma_j&0\\0&\sigma_j\end{bmatrix}
=\begin{bmatrix}0&\sigma_i\sigma_j\\\sigma_i\sigma_j&0\end{bmatrix}\\
\Sigma_j\alpha_i
&=\begin{bmatrix}\sigma_j&0\\0&\sigma_j\end{bmatrix}\begin{bmatrix}0&\sigma_i\\\sigma_i&0\end{bmatrix}
=\begin{bmatrix}0&\sigma_j\sigma_i\\\sigma_j\sigma_i&0\end{bmatrix}
\end{align}$$
The commutator of these two is then
$$\begin{align}
\left[\alpha_i,\Sigma_j\right]
&=\begin{bmatrix}0&\sigma_i\sigma_j\\\sigma_i\sigma_j&0\end{bmatrix}-\begin{bmatrix}0&\sigma_j\sigma_i\\\sigma_j\sigma_i&0\end{bmatrix}\\
&=\begin{bmatrix}0&\sigma_i\sigma_j-\sigma_j\sigma_i\\\sigma_i\sigma_j-\sigma_j\sigma_i&0\end{bmatrix}\\
&=\begin{bmatrix}0&2i\varepsilon_{ijk}\sigma_k\\2i\varepsilon_{ijk}\sigma_k&0\end{bmatrix}\\
&=2i\varepsilon_{ijk}\begin{bmatrix}0&\sigma_k\\\sigma_k&0\end{bmatrix}\\
\Aboxed{\left[\alpha_i,\Sigma_j\right]&=2i\varepsilon_{ijk}\alpha_k}
\end{align}$$
