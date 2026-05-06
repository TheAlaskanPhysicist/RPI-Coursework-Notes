**Author:** Stanley Goodwin
**Date:** April 11th, 2026
**Note:** Adjusted to 2023 schedule, this replaces activity 9

---
## Question 1
> Starting from the "composite" version of the Klein-Gordon equation for a free particle, show...
> $$i\partial_tY(\vec{x},t)=\left[-\dfrac{1}{2m}\vec\nabla^2(\tau_3+i\tau_2)+m\tau_3\right]Y(\vec{x},t)$$
---
### Question 1.A
> ... that the two eigenvalues are (indeed) $E=\pm E_p=\pm\sqrt{p^2+m^2}$

Suppose the Ansatz for $Y(\vec{x},t)$ (totally not inspired by [[#Question 1.B|part b]]) is of the form
$$\begin{align}
Y(\vec{x},t)&=\begin{bmatrix}c_+\\c_-\end{bmatrix}e^{-i(Et-\vec{p}\cdot\vec{x})}
\end{align}$$
Substituting this ansatz into the Klein-Gordon equation, we get that
$$\begin{align}
-i^2E\begin{bmatrix}c_+\\c_-\end{bmatrix}e^{-i(Et-\vec{p}\cdot\vec{x})}
&=\left[-\dfrac{1}{2m}(i\vec{p})^2\begin{bmatrix}1&1\\-1&-1\end{bmatrix}+m\begin{bmatrix}1&0\\0&-1\end{bmatrix}\right]\begin{bmatrix}c_+\\c_-\end{bmatrix}e^{-i(Et-\vec{p}\cdot\vec{x})}\\
E\begin{bmatrix}c_+\\c_-\end{bmatrix}
&=\begin{bmatrix}\tfrac{p^2}{2m}+m&\tfrac{p^2}{2m}\\
-\tfrac{p^2}{2m}&-\tfrac{p^2}{2m}-m\end{bmatrix}\begin{bmatrix}c_+\\c_-\end{bmatrix}
\end{align}$$
This is an energy-eigenvalue problem, so we can move everything to one side to the form
$$\begin{align}
\begin{bmatrix}
E-\left(\tfrac{p^2}{2m}+m\right)&-\tfrac{p^2}{2m}\\
+\tfrac{p^2}{2m}&E+\left(\tfrac{p^2}{2m}+m\right)\end{bmatrix}\begin{bmatrix}c_+\\c_-\end{bmatrix}&=\begin{bmatrix}0\\0\end{bmatrix}
\end{align}$$
Ignoring the trivial solution $c_+=c_-=0$, this can only occur if the determinant is zero
$$\begin{align}
\left(E-(\tfrac{p^2}{2m}+m)\right)\left(E+(\tfrac{p^2}{2m}+m)\right)-\left(\dfrac{p^2}{2m}\right)\left(-\dfrac{p^2}{2m}\right)&=0
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


The first product is a difference of squares, and the other is just kinetic energy squared
$$\begin{align}
E^2-\cancel{\left(\dfrac{p^2}{2m}\right)^2}-2m\left(\dfrac{p^2}{2m}\right)-m^2+\cancel{\left(\dfrac{p^2}{2m}\right)^2}&=0 &\implies&& E^2-p^2-m^2&=0
\end{align}$$
Rearranging to isolate the energy eigenstate values, we get the values
$$\begin{align}
E^2&=p^2+m^2 &\implies&& \Aboxed{E_\pm&=\pm\sqrt{p^2+m^2}}
\end{align}$$
---
### Question 1.B
> ... the corresponding eigenvectors are
> $$\begin{align}
Y_\pm(\vec{x},t)&=N\begin{bmatrix}m\pm E\\m\mp E\end{bmatrix}e^{-i(\pm Et-\vec{p}\cdot\vec{x})}
\end{align}$$

We start with the result of the ansatz substitution into the Klein-Gordon equation from [[#Question 1.A|part a]]
$$\begin{align}
E\begin{bmatrix}c_+\\c_-\end{bmatrix}
&=\begin{bmatrix}\tfrac{p^2}{2m}+m&\tfrac{p^2}{2m}\\
-\tfrac{p^2}{2m}&-\tfrac{p^2}{2m}-m\end{bmatrix}\begin{bmatrix}c_+\\c_-\end{bmatrix}
\end{align}$$
Using our eigenvalues of $E=E_\pm$ and splitting this into a system of equations, we have that
$$\begin{align}
E_\pm c_+&=\left(\tfrac{p^2}{2m}+m\right)c_+ +\tfrac{p^2}{2m}c_-
&\implies&&
0&=\left[\left(\tfrac{p^2}{2m}+m\right)-E_\pm\right] c_++\tfrac{p^2}{2m}c_-
\\
E_\pm c_-&=-\tfrac{p^2}{2m}c_+ -\left(\tfrac{p^2}{2m}+m\right)c_-
&\implies&&
0&=\tfrac{p^2}{2m}c_+ +\left[\left(\tfrac{p^2}{2m}+m\right)+E_\pm\right]c_-
\end{align}$$
The relationship between the two coefficients can be found from either equation
$$\begin{align}
\tfrac{p^2}{2m}c_+&=-\left[\left(\tfrac{p^2}{2m}+m\right)+E_\pm\right]c_- 
&\implies&&
p^2c_+&=-\left[p^2+m^2+m^2+2mE_\pm\right]c_- 
\end{align}$$
On both sides, we can use the relationship of our eigenvalues $E^2=p^2+m^2$ :
$$\begin{align}
\left(E_\pm^2-m^2\right)c_+&=-\left[E_\pm^2+2mE_\pm+m^2\right]c_-\\
\left(m-E_\pm\right)\left(m+E_\pm\right)c_+&=\left(m+E_\pm\right)^2c_-\\
\left(m-E_\pm\right)c_+&=\left(m+E_\pm\right)c_-
\end{align}$$
Using this relationship, we can then write the eigenvectors (using $E_\pm=\pm E$)
$$\begin{align}
Y_\pm(\vec{x},t)&=\dfrac{c_+}{m+E_\pm}\begin{bmatrix}m+E_\pm\\m-E_\pm\end{bmatrix}e^{-i(E_\pm t-\vec{p}\cdot\vec{x})} &\implies&&
\Aboxed{Y_\pm(\vec{x},t)&=\dfrac{c_+}{m\pm E}\begin{bmatrix}m\pm E\\m\mp E\end{bmatrix}e^{-i(\pm Et-\vec{p}\cdot\vec{x})}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 1.C
> Determine the normalization factor $N$ such that $\rho(\vec{x},t)\equiv j^0=Y^\dagger\tau_3Y=\pm1$ for each solution.

Starting with our eigenvector equation given as
$$\begin{align}
Y_\pm(\vec{x},t)&=N\begin{bmatrix}m\pm E\\m\mp E\end{bmatrix}e^{-i(\pm Et-\vec{p}\cdot\vec{x})}
\end{align}$$
The product $Y^\dagger\tau_3Y$, when combining like terms, is
$$\begin{align}
Y^\dagger\tau_3Y
&=N^2\begin{bmatrix}m\pm E & m\mp E\end{bmatrix}\begin{bmatrix}1&0\\0&-1\end{bmatrix}\begin{bmatrix}m\pm E\\m\mp E\end{bmatrix}\\
\pm 1&=N^2\left[\left(m\pm E\right)^2-\left(m\mp E\right)^2\right]\\
\pm 1&=N^2\left[\pm2mE\pm2mE\right]\\
\pm 1&=\pm4mEN^2
\end{align}$$
Thus our normalization factor is
$$\begin{align}
N^2&=\dfrac{1}{4mE} &\implies&& \Aboxed{N&=\dfrac{1}{2\sqrt{mE}}}
\end{align}$$
It is the same value for both eigenstates.

---
### Question 1.D
> Write down the positive and negative energy free-particle solutions for a particle *at rest*.

The general solution for the eigenstates, before we let $p=0$, is
$$\begin{align}
Y_\pm(\vec{x},t)&=\dfrac{1}{2\sqrt{mE}}\begin{bmatrix}m\pm E\\m\mp E\end{bmatrix}e^{-i(\pm Et-\vec{p}\cdot\vec{x})}
\end{align}$$
At rest, $E=m$, and so we have the two solutions
$$\begin{align}
\Aboxed{Y_+(\vec{x},t)&=\begin{bmatrix}1\\0\end{bmatrix}e^{-i(Et-\vec{p}\cdot\vec{x})}} &
\Aboxed{Y_-(\vec{x},t)&=\begin{bmatrix}0\\1\end{bmatrix}e^{+i(Et+\vec{p}\cdot\vec{x})}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

## Question 2
> Starting from $$\partial_t\rho=\partial_t\left(Y^\dagger\tau_3Y\right)=\left(\partial_tY^\dagger\right)\tau_3Y+Y^\dagger\tau_3\left(\partial_tY\right)$$
> and using again $$i\partial_tY(\vec{x},t)=\left[-\dfrac{1}{2m}\vec\nabla^2(\tau_3+i\tau_2)+m\tau_3\right]Y(\vec{x},t)$$

---
### Question 2.A
> Show that a continuity equation $\partial_t\rho+\vec\nabla\cdot\vec{j}=0$ is satisfied with $$\vec{j}=\dfrac{1}{2mi}\left[Y^\dagger(1+\tau_1)\left(\vec\nabla Y\right)-\left(\vec\nabla Y^\dagger\right)(1+\tau_1)Y\right]$$

Our Klein-Gordon equation gives us some assistance in finding the gradient terms
$$\begin{align}
&& \tau_3\cdot i\partial_tY(\vec{x},t)&=\tau_3\left[-\dfrac{1}{2m}\vec\nabla^2(\tau_3+i\tau_2)+m\tau_3\right]Y(\vec{x},t) \\
\implies&& \left[m-i\partial_t\tau_3\right]Y(\vec{x},t)&=\dfrac{1}{2m}\vec\nabla^2(1+\tau_1)Y(\vec{x},t)
\end{align}$$
Likewise, for the complex conjugate eigenfunction, we can use the adjoint operator
$$\begin{align}
&&
\left\{\left[m-i\partial_t\tau_3\right]Y(\vec{x},t)\right\}^\dagger&=\left\{\dfrac{1}{2m}\vec\nabla^2(1+\tau_1)Y(\vec{x},t)\right\}^\dagger \\
\implies&&
Y^\dagger(\vec{x},t)\left[m+i\partial_t\tau_3\right]&=\dfrac{1}{2m}\vec\nabla^2 Y^\dagger(\vec{x},t)(1+\tau_1)
\end{align}$$
Taking the divergence of the current density, we have
$$\begin{align}
\vec\nabla\cdot\vec{j}&=\dfrac{1}{2mi}\left[Y^\dagger(1+\tau_1)\vec\nabla^2Y-\vec\nabla^2Y^\dagger(1+\tau_1)Y\right]+\text{canceling terms}\\
&=\dfrac{1}{i}\left[Y^\dagger\left[mY-i\partial_t\tau_3Y\right]-\left[mY^\dagger+i\partial_tY^\dagger\tau_3\right]Y\right]\\
&=\dfrac{1}{i}\left[\cancel{mY^\dagger Y}-iY^\dagger\tau_3\partial_tY-\cancel{mY^\dagger Y}-i\partial_tY^\dagger\tau_3Y\right]\\
&=-\left[Y^\dagger\tau_3\partial_tY+\partial_tY^\dagger\tau_3Y\right]\\
\Aboxed{\vec\nabla\cdot\vec{j}&=-\partial_t\left(Y^\dagger\tau_3Y\right)}
\end{align}$$
Adding the charge density rate of change to the divergence of current density gives
$$\begin{align}
\Aboxed{\partial_t\rho+\vec\nabla\cdot\vec{j}=\partial_t\left(Y^\dagger\tau_3Y\right)-\partial_t\left(Y^\dagger\tau_3Y\right)=0}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

### Question 2.B
> Show that for free-particle solutions $\vec{j}=\dfrac{\vec{p}}{m}Y^\dagger(1+\tau_1)Y=\dfrac{\vec{p}}{E}$, regardless of $E=\pm E$.

We start with the form of the eigenstates
$$\begin{align}
Y_\pm(\vec{x},t)&=\dfrac{1}{2\sqrt{mE}}\begin{bmatrix}m\pm E\\m\mp E\end{bmatrix}e^{-i(\pm Et-\vec{p}\cdot\vec{x})}
\end{align}$$
Using the equation for $\vec{j}$ from [[#Question 2.A|part a]], we get
$$\begin{align}
\vec{j}&=\dfrac{1}{2mi}\left[Y^\dagger(1+\tau_1)\left(\vec\nabla Y\right)-\left(\vec\nabla Y^\dagger\right)(1+\tau_1)Y\right]\\
&=\dfrac{2\vec{p}i}{8m^2Ei}\begin{bmatrix}m\pm E\\m\mp E\end{bmatrix}^T\begin{bmatrix}1&1\\1&1\end{bmatrix}\begin{bmatrix}m\pm E\\m\mp E\end{bmatrix}\\
&=\dfrac{\vec{p}}{4m^2E}\begin{bmatrix}m\pm E\\m\mp E\end{bmatrix}^T\begin{bmatrix}2m\\2m\\\end{bmatrix}\\
&=\dfrac{2m\vec{p}}{4m^2E}\begin{bmatrix}m\pm E+m\mp E\\\end{bmatrix}\\
&=\dfrac{\vec{p}}{2mE}\cdot2m\\
\Aboxed{\vec{j}&=\dfrac{\vec{p}}{E}}
\end{align}$$
