**Author:** Stanley Goodwin
**Date:** April 23rd, 2026

---
## Question 8.9
---
### Question 8.9.A
> Derive the matrices $\gamma^\mu$ from $(8.55)$ and show that they satisfy the Clifford algebra $(8.49)$.$$\begin{align}\alpha&=\begin{bmatrix}0&\sigma\\\sigma&0\end{bmatrix}&\beta&=\begin{bmatrix}1&0\\0&-1\end{bmatrix}&&\text{(8.55)}\end{align}$$$$\begin{align}\left(\gamma^0\right)^2&=1&\left(\gamma^i\right)^2&=-1&\gamma^\mu\gamma^\nu&=-\gamma^\nu\gamma^\mu&&\text{(8.49)}\end{align}$$

By the definitions given in $(8.52)$,
$$\begin{align}
\alpha_i&\equiv\gamma^0\gamma^i & \beta\equiv\gamma^0
\end{align}$$
Our parameter $\beta$ is equal to that of $\gamma_0$ :
$$\begin{align}
\beta&=\begin{bmatrix}\ \mathbb{I}_{2\times2}&0\\0&-\mathbb{I}_{2\times2}\end{bmatrix}
&\implies&&
\gamma^0&=\begin{bmatrix}\ \mathbb{I}_{2\times2}&0\\0&-\mathbb{I}_{2\times2}\end{bmatrix}
\end{align}$$
With a bit of rearranging, we can also solve for $\gamma^i$ using that $\beta^2=\mathbb{I}_{4\times4}$ and is equal to
$$\begin{align}
\alpha_i&\equiv\beta\gamma^i
&\implies&&
\beta\alpha_i&\equiv\beta^2\gamma^i
&\implies&&
\gamma^i&\equiv\beta\alpha_i
\end{align}$$
Substituting our values for $\alpha_i$ and $\beta$, our space gamma matrices are
$$\begin{align}
\gamma^i&=\begin{bmatrix}\ \mathbb{I}_{2\times2}&0\\0&-\mathbb{I}_{2\times2}\end{bmatrix}\begin{bmatrix}0&\sigma^i\ \\\sigma^i&0\end{bmatrix}
&\implies&&
\gamma^i&=\begin{bmatrix}0&\sigma^i\\-\sigma^i&0\end{bmatrix}
\end{align}$$
Now for the Clifford Algebra properties, the first relationship is
$$\begin{align}
\left(\gamma^0\right)^2&=\begin{bmatrix}\ \mathbb{I}_{2\times2}&0\\0&-\mathbb{I}_{2\times2}\end{bmatrix}^2=\mathbb{I}_{4\times4}
&\implies&&
\Aboxed{\left(\gamma^0\right)^2&=1}
\end{align}$$
The second relationship is
$$\begin{align}
\left(\gamma^i\right)^2&=\begin{bmatrix}0&\sigma^i\\-\sigma^i&0\end{bmatrix}^2=\begin{bmatrix}\sigma^i\sigma^i&0\\0&-\sigma^i\sigma^i\end{bmatrix}=-\mathbb{I}_{4\times4}
&\implies&&
\Aboxed{\left(\gamma^i\right)^2&=-1}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


And lastly, the third relationship for anticommutation requires looking at two different conditions, being the product of time and space matrices, and the product of two space matrices.
$$\begin{align}
\left\{\gamma^0,\gamma^i\right\}&=\beta\cdot\beta\alpha_i+\beta\alpha_i\cdot\beta=\alpha_i+(-\alpha_i)=0
&\implies&&
\Aboxed{\gamma^0\gamma^i&=-\gamma^i\gamma^0}
\end{align}$$
The space matrix one is a little more complex
$$\begin{align}
\left\{\gamma^i,\gamma^j\right\}
&=\beta\alpha_i\cdot\beta\alpha_j+\beta\alpha_j\cdot\beta\alpha_i\\
&=(-\alpha_i)\alpha_j+(-\alpha_j)\alpha_i\\
&=-\begin{bmatrix}\sigma^i\sigma^j&0\\0&-\sigma^i\sigma^j\end{bmatrix}-\begin{bmatrix}\sigma^j\sigma^i&0\\0&-\sigma^j\sigma^i\end{bmatrix}\\
&=-\begin{bmatrix}\sigma^i\sigma^j+\sigma^j\sigma^i&0\\0&-(\sigma^i\sigma^j+\sigma^j\sigma^i)\end{bmatrix}\\
&=-\begin{bmatrix}0&0\\0&0\end{bmatrix}\\
\Aboxed{\left\{\gamma^i,\gamma^j\right\}&=0}
\end{align}$$
---
### Question 8.9.B
> Show that $$\begin{align}\gamma^0&=\begin{bmatrix}\ \mathbb{I}_{2\times2}&0\\0&-\mathbb{I}_{2\times2}\end{bmatrix}=\ \mathbb{I}_{2\times2}\otimes\tau_3 & \gamma^i&=\begin{bmatrix}0&\sigma^i\\-\sigma^i&0\end{bmatrix}=\sigma^i\otimes i\tau_2 \end{align}$$where $\mathbb{I}_{2\times2}$ is the identity matrix, and $\sigma^i$ and $\tau^i$ are the Pauli matrices.

The matrix product effectively nests the matrices inside each other. For $\gamma^0$ we have
$$\begin{align}
\mathbb{I}_{2\times2}\otimes\tau_3&=\begin{bmatrix}\begin{bmatrix}1&0\\0&-1\end{bmatrix}&\begin{bmatrix}0&0\\0&0\end{bmatrix}\\\begin{bmatrix}0&0\\0&0\end{bmatrix}&\begin{bmatrix}1&0\\0&-1\end{bmatrix}\end{bmatrix}
\end{align}$$
If instead we reverse the order, $\tau_3\otimes\mathbb{I}_{2\times2}$, we instead get
$$\begin{align}
\tau_3\otimes\mathbb{I}_{2\times2}&=\begin{bmatrix}\begin{bmatrix}1&0\\0&1\end{bmatrix}&\begin{bmatrix}0&0\\0&0\end{bmatrix}\\\begin{bmatrix}0&0\\0&0\end{bmatrix}&-\begin{bmatrix}1&0\\0&1\end{bmatrix}\end{bmatrix}=\begin{bmatrix}\ \mathbb{I}_{2\times2}&0\\0&-\mathbb{I}_{2\times2}\end{bmatrix}
\end{align}$$
From [[#Question 8.9.A|part a]], this is the exact form for the $0$-th gamma matrix, and so
$$\begin{align}
\Aboxed{\gamma^0&=\tau_3\otimes\mathbb{I}_{2\times2}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*


For the other gamma matrices, similar reversal of order is needed
$$\begin{align}
\sigma^1\otimes i\tau_2&=\begin{bmatrix}\begin{bmatrix}0&0\\0&0\end{bmatrix}&i\begin{bmatrix}0&-i\\i&0\end{bmatrix}\\i\begin{bmatrix}0&-i\\i&0\end{bmatrix}&\begin{bmatrix}0&0\\0&0\end{bmatrix}\end{bmatrix}=\begin{bmatrix}0&\sigma^1\\-\sigma^1&0\end{bmatrix}\\
\sigma^2\otimes i\tau_2&=\begin{bmatrix}\begin{bmatrix}0&0\\0&0\end{bmatrix}&-i^2\begin{bmatrix}0&-i\\i&0\end{bmatrix}\\i^2\begin{bmatrix}0&-i\\i&0\end{bmatrix}&\begin{bmatrix}0&0\\0&0\end{bmatrix}\end{bmatrix}=\begin{bmatrix}0&\sigma^2\\-\sigma^2&0\end{bmatrix}\\
\sigma^3\otimes i\tau_2&=\begin{bmatrix}i\begin{bmatrix}0&-i\\i&0\end{bmatrix}&\begin{bmatrix}0&0\\0&0\end{bmatrix}\\\begin{bmatrix}0&0\\0&0\end{bmatrix}&i\begin{bmatrix}0&-i\\i&0\end{bmatrix}\end{bmatrix}=\begin{bmatrix}0&\sigma^3\\-\sigma^3&0\end{bmatrix}\\
\end{align}$$
Once again from [[#Question 8.9.A|part a]], this is the form of the space gamma matrices. Therefore
$$\begin{align}
\Aboxed{\gamma^i&=\sigma^i\otimes i\tau_2}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

## Question 8.11
> Find the eigenvalues for the free-particle Dirac equation $(8.65)$. $$\begin{align}\begin{bmatrix}m&0&p&0\\0&m&0&-p\\p&0&-m&0\\0&-p&0&-m\end{bmatrix}\begin{bmatrix}u_1\\u_2\\u_3\\u_4\end{bmatrix}&=E\begin{bmatrix}u_1\\u_2\\u_3\\u_4\end{bmatrix}&&\text{(8.65)}\end{align}$$

To find the eigenvalues, we set the determinant of the total matrix to be zero, where
$$\begin{align}
\det\begin{bmatrix}
m-E&0&p&0\\
0&m-E&0&-p\\
p&0&-m-E&0\\
0&-p&0&-m-E
\end{bmatrix}&=0
\end{align}$$
This splits into two sub-determinants
$$\begin{align}
(m-E)\det\begin{bmatrix}
m-E&0&-p\\
0&-m-E&0\\
-p&0&-m-E
\end{bmatrix}+
p\det\begin{bmatrix}
0&m-E&-p\\
p&0&0\\
0&-p&-m-E
\end{bmatrix}&=0
\end{align}$$
Since we can choose a row-column for submatrices, this turns into two new sub-determinants
$$\begin{align}
(m-E)(-m-E)\det\begin{bmatrix}
m-E&-p\\
-p&-m-E
\end{bmatrix}+
p(-p)\det\begin{bmatrix}
m-E&-p\\
-p&-m-E
\end{bmatrix}&=0
\end{align}$$
Determinants of $2\times2$ matrices are easy to calculate, and so we have
$$\begin{align}
\left[(m-E)(-m-E)+
p(-p)\right]\left[(m-E)(-m-E)-(-p)(-p)\right]&=0\\
\left[E^2-m^2-
p^2\right]\left[E^2-m^2-
p^2\right]&=0
\end{align}$$
This is a repeated root with the condition
$$\begin{align}
E^2&=p^2+m^2 &\implies&& \Aboxed{E&=\pm\sqrt{p^2+m^2}}
\end{align}$$

<div style="page-break-before: always;"></div>*PDF next page*

## Question 8.12
> Insert one of the four solutions $u_\text{R,L}^{(\pm)}(p)$ from $(8.67)$ into the four vector probability current $(8.58)$ and interpret the result. $$\begin{align}u_\text{R}^{(+)}(p)&=\begin{bmatrix}1\\0\\\tfrac{p}{E_p+m}\\0\end{bmatrix} & u_\text{L}^{(+)}(p)&=\begin{bmatrix}0\\1\\0\\\tfrac{-p}{E_p+m}\end{bmatrix} & u_\text{R}^{(-)}(p)&=\begin{bmatrix}\tfrac{-p}{E_p+m}\\0\\1\\0\end{bmatrix} & u_\text{L}^{(-)}(p)&=\begin{bmatrix}0\\\tfrac{p}{E_p+m}\\0\\1\end{bmatrix}\end{align}$$$$\begin{align}j^\mu&=\bar\Psi\gamma^\mu\Psi && \text{(8.58)}\end{align}$$

For simplicity, I will choose $\Psi=u_\text{R}^{(+)}(p)\cdot e^{-i(E_pt-\vec{p}\cdot\vec{x})}$. The Dirac adjoint is $\bar\Psi\equiv\Psi^\dagger\gamma^0$. Substituting into our current density equation, we get that
$$\begin{align}
j^\mu&=\bar\Psi\gamma^\mu\Psi\\
&=\begin{bmatrix}1&0&\tfrac{p}{E_p+m}&0\end{bmatrix}e^{+i(E_pt-\vec{p}\cdot\vec{x})}\gamma^0\gamma^\mu\begin{bmatrix}1&0&\tfrac{p}{E_p+m}&0\end{bmatrix}^Te^{-i(E_pt-\vec{p}\cdot\vec{x})}\\
&=\begin{bmatrix}1&0&\tfrac{p}{E_p+m}&0\end{bmatrix}\gamma^0\gamma^\mu\begin{bmatrix}1&0&\tfrac{p}{E_p+m}&0\end{bmatrix}^T\\
\end{align}$$
There are two different results for when $\mu=0$ and $\mu=i$. They reduce to
$$\begin{align}
\Aboxed{j^0&=1+\left(\dfrac{p}{E_p+m}\right)^2}
\Aboxed{j^1=j^2&=0}
\Aboxed{j^3&=2\dfrac{p}{E_p+m}}
\end{align}$$
For our chosen direction for the 3rd basis element, the probability density in time seems to effectively be the even-power terms and the probability current is the odd-power terms. How I think of it is like the following polynomial
$$\begin{align}
(x+1)^2&=x^2+2x+1=(1x^2+1x^0)+(2x^1)
\end{align}$$
When it comes to interpreting the results, it looks as if the probability density (time component) are the in-parallel terms ("how much time goes into time") and the same with space, but the current density in space is like a "sheer" (how much time goes into space and vice versa).
