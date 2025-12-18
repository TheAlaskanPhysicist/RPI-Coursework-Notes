Author: Stanley Goodwin
Date: December 8th, 2025

---
## Question 3.32
What is the physical significance of the operators:
$$\begin{align}
K_+&\equiv a_+^\dagger a_-^\dagger & K_-&\equiv a_+a_-
\end{align}$$
in Schwinger's scheme for angular momentum? Give the non-vanishing matrix elements of $K_{\pm}$.
$$\begin{align}
j&=\dfrac{n_++n_-}{2} & m&=\dfrac{n_+-n_-}{2}
\end{align}$$
Applying the $K_\pm$ operator, we see:
$$\begin{align}
K_+\ket{n_+,n_-}&=a_+^\dagger a_-^\dagger\ket{n_+,n_-}\\
\Aboxed{K_+\ket{n_+,n_-}&=\sqrt{(n_++1)(n_-+1)}\ket{n_++1,n_-+1}}\\\\
K_-\ket{n_+,n_-}&=a_+a_-\ket{n_+,n_-}\\
\Aboxed{K_-\ket{n_+,n_-}&=\sqrt{n_+n_-}\ket{n_+-1,n_--1}}
\end{align}$$
The elements are then:
$$\begin{align}
\Aboxed{\bra{n_++1,n_-+1}K_+\ket{n_+,n_-}&=\sqrt{(n_++1)(n_-+1)}}\\
\Aboxed{\bra{n_+-1,n_--1}K_-\ket{n_+,n_-}&=\sqrt{n_+n_-}}
\end{align}$$
Converting into $j,m$ notation, we can see that:
$$\begin{align}
j&=\dfrac{n_++n_-}{2}&\rightarrow&& j&=\dfrac{(n_++1)+(n_-+1)}{2}=\dfrac{n_++n_-}{2}+1\\
m&=\dfrac{n_+-n_-}{2}&\rightarrow&& m&=\dfrac{(n_++1)-(n_-+1)}{2}=\dfrac{n_+-n_-}{2}\\
\end{align}$$
Therefore the transformation does:
$$\begin{align}
\Aboxed{j&\rightarrow j+1} & \Aboxed{m&\rightarrow m}
\end{align}$$
Representing these states in $\ket{j,m}$ notation, we see:
$$\begin{align}
\bra{j+1,m}K_+\ket{j,m}&=\sqrt{(j+m+1)(j-m+1)}\\
\bra{j-1,m}K_-\ket{j,m}&=\sqrt{(j+m)(j-m)}
\end{align}$$
All other elements of these matrices are 0. Representing in matrix form:
$$\begin{align}
\Aboxed{\bra{j',m'}K_+\ket{j,m}&=\sqrt{(j+m+1)(j-m+1)}\delta_{j',j+1}\delta_{m',m}}\\
\Aboxed{\bra{j',m'}K_-\ket{j,m}&=\sqrt{(j+m)(j-m)}\delta_{j',j-1}\delta_{m',m}}
\end{align}$$
The physical interpretation of this operator is that it changes the total angular momentum number of a state without changing the magnetic quantum number associated with it. 

---
## Question 3.38
### Question 3.38.A
Consider a system with $j=1$, Explicitly write:
$$\begin{align}
\bra{j=1,m'}J_y\ket{j=1,m}
\end{align}$$
in $3\times3$ matrix form.

The $j=1$ (spin-1) system has 3 basis elements:
$$\begin{align}
\{\ket{-},\ket{0},\ket{+}\}
\end{align}$$
We can express $J_y$ as the difference of $J_+$ and $J_-$ so we can apply it to a state
$$\begin{align}
J_y=\dfrac{J_+-J_-}{2i}
\end{align}$$
where these two operators are defined as
$$\begin{align}
J_+\ket{j,m}&=\sqrt{j(j+1)-m(m+1)}\ket{j,m+1}\\
J_-\ket{j,m}&=\sqrt{j(j+1)-m(m-1)}\ket{j,m-1}\\
\end{align}$$
Applying these operators to the 3 states, then:
$$\begin{align}
J_+\ket{-}&=\sqrt{1(1+1)-(-1)(-1+1)}\ket{j,-1+1} & \Aboxed{J_+\ket{-}&=\sqrt{2}\ket{j,0}}\\
J_+\ket{0}&=\sqrt{1(1+1)-0(0+1)}\ket{j,0+1} & \Aboxed{J_+\ket{0}&=\sqrt{2}\ket{j,1}}\\
J_+\ket{+}&=\sqrt{1(1+1)-1(1+1)}\ket{j,1+1} & \Aboxed{J_+\ket{+}&=0}\\\\
J_-\ket{-}&=\sqrt{1(1+1)-(-1)(-1-1)}\ket{j,-1-1} & \Aboxed{J_-\ket{-}&=0}\\
J_-\ket{0}&=\sqrt{1(1+1)-0(0-1)}\ket{j,0-1} & \Aboxed{J_-\ket{0}&=\sqrt{2}\ket{j,-1}}\\
J_-\ket{+}&=\sqrt{1(1+1)-1(1-1)}\ket{j,1-1} & \Aboxed{J_-\ket{+}&=\sqrt{2}\ket{j,0}}
\end{align}$$
These operators can then be written as:
$$\begin{align}
J_+&=\hbar\begin{bmatrix}0&\sqrt2&0\\0&0&\sqrt2\\0&0&0\end{bmatrix} & J_-&=\hbar\begin{bmatrix}0&0&0\\\sqrt2&0&0\\0&\sqrt2&0\end{bmatrix}
\end{align}$$
Our operator $J_y$ is then just:
$$\begin{align}
J_y&=\dfrac{J_+-J_-}{2i}\\
&=\dfrac{1}{2i}\left(\hbar\begin{bmatrix}0&\sqrt2&0\\0&0&\sqrt2\\0&0&0\end{bmatrix}-\hbar\begin{bmatrix}0&0&0\\\sqrt2&0&0\\0&\sqrt2&0\end{bmatrix}\right)\\
J_y&=\dfrac{\hbar\sqrt{2}}{2i}\begin{bmatrix}0&1&0\\-1&0&1\\0&-1&0\end{bmatrix}
\end{align}$$
This is exactly what our answer should be, as expected.

---
### Question 3.38.B
Show that, for $j=1$ only, is it legitimate to replace $e^{-iJ_y\beta/\hbar}$ by:
$$\begin{align}
1-i\left(\dfrac{J_y}{\hbar}\right)\sin\beta-\left(\dfrac{J_y}{\hbar}\right)^2(1-\cos\beta)
\end{align}$$
We should express $J_y$ in a more simpler fashion, and so:
$$\begin{align}
J_y&=\hbar\dfrac{1}{\sqrt{2}}\begin{bmatrix}0&-i&0\\i&0&-i\\0&i&0\end{bmatrix}\\
\end{align}$$
It is pretty trivial to see that:
$$\begin{align}
\dfrac{J_y^3}{\hbar^3}&=\dfrac{J_y}{\hbar} &\implies&& \Aboxed{J_y^{2k+1}&=\hbar^{2k}J_y}\\
\dfrac{J_y^4}{\hbar^4}&=\dfrac{J_y^2}{\hbar^2} &\implies&& \Aboxed{J_y^{2k}&=\hbar^{2k-2}J_y^2}\\
\end{align}$$
If we expand our exponential as a Taylor series, then we can see:
$$\begin{align}
e^{-iJ_y\beta/\hbar}
&=\sum_{n=0}^\infty\dfrac{(-i\beta/\hbar)^n}{n!}J_y^n\\
&=1+\sum_{n=1}^\infty\dfrac{(-i\beta/\hbar)^{2n}}{(2n)!}J_y^{2n}+\sum_{n=0}^\infty\dfrac{(-i\beta/\hbar)^{2n+1}}{(2n+1)!}J_y^{2n+1}\\
&=1+\sum_{n=1}^\infty\dfrac{(-i\beta/\hbar)^{2n}}{(2n)!}\hbar^{2n-2}J_y^2+\sum_{n=0}^\infty\dfrac{(-i\beta/\hbar)^{2n+1}}{(2n+1)!}\hbar^{2n}J_y\\
&=1+\dfrac{J_y^2}{\hbar^2}\sum_{n=1}^\infty\dfrac{(-i\beta/\hbar)^{2n}}{(2n)!}\hbar^{2n}+\dfrac{J_y}{\hbar}\sum_{n=0}^\infty\dfrac{(-i\beta/\hbar)^{2n+1}}{(2n+1)!}\hbar^{2n+1}\\
&=1+\dfrac{J_y^2}{\hbar^2}\sum_{n=1}^\infty\dfrac{i^{2n}(\beta)^{2n}}{(2n)!}-\dfrac{J_y}{\hbar}\sum_{n=0}^\infty\dfrac{i^{2n+1}(\beta)^{2n+1}}{(2n+1)!}\\
&=1+\dfrac{J_y^2}{\hbar^2}\sum_{n=1}^\infty\dfrac{(-1)^n(-\beta)^{2n}}{(2n)!}-i\dfrac{J_y}{\hbar}\sum_{n=0}^\infty\dfrac{(-1)^n(\beta)^{2n+1}}{(2n+1)!}\\
&=1+\dfrac{J_y^2}{\hbar^2}\left(-1+\cos\beta\right)-i\dfrac{J_y}{\hbar}\sin\beta\\
\Aboxed{e^{-iJ_y\beta/\hbar}&=1-i\dfrac{J_y}{\hbar}\sin\beta-\dfrac{J_y^2}{\hbar^2}\left(1-\cos\beta\right)}
\end{align}$$
---
### Question 3.38.C
Using (b), prove:
$$\begin{align}
d^{(j=1)}(\beta)&=\begin{bmatrix}
\tfrac{1}{2}(1+\cos\beta) & -\tfrac{1}{\sqrt2}\sin\beta & \tfrac{1}{2}(1-\cos\beta)\\
\tfrac{1}{\sqrt2}\sin\beta & \cos\beta & -\tfrac{1}{\sqrt2}\sin\beta\\
\tfrac{1}{2}(1-\cos\beta) & \tfrac{1}{\sqrt2}\sin\beta & \tfrac{1}{2}(1+\cos\beta)
\end{bmatrix}
\end{align}$$
Using our form for $J_y$, and calculating $J^2$:
$$\begin{align}
J_y&=\hbar\dfrac{1}{\sqrt{2}}\begin{bmatrix}0&-i&0\\i&0&-i\\0&i&0\end{bmatrix}\\
J_y^2&=\dfrac{\hbar^2}{2}\begin{bmatrix}1&0&-1\\0&2&0\\-1&0&1\end{bmatrix}\\
\end{align}$$
We can substitute the exponential as:
$$\begin{align}
e^{-iJ_y\beta/\hbar}&=1-i\dfrac{J_y}{\hbar}\sin\beta-\dfrac{J_y^2}{\hbar^2}\left(1-\cos\beta\right)\\
&=\mathbb{I}-i\dfrac{1}{\sqrt{2}}\begin{bmatrix}0&-i&0\\i&0&-i\\0&i&0\end{bmatrix}\sin\beta-\dfrac{1}{2}\begin{bmatrix}1&0&-1\\0&2&0\\-1&0&1\end{bmatrix}\left(1-\cos\beta\right)\\
&=\mathbb{I}+\begin{bmatrix}0&-\tfrac{1}{\sqrt{2}}\sin\beta&0\\\tfrac{1}{\sqrt{2}}\sin\beta&0&-\tfrac{1}{\sqrt{2}}\sin\beta\\0&\tfrac{1}{\sqrt{2}}\sin\beta&0\end{bmatrix}+\begin{bmatrix}-\tfrac{1}{2}(1-\cos\beta)&0&\tfrac{1}{2}(1-\cos\beta)\\0&-(1-\cos\beta)&0\\\tfrac{1}{2}(1-\cos\beta)&0&-\tfrac{1}{2}(1-\cos\beta)\end{bmatrix}\\
&=\begin{bmatrix}
1-\tfrac{1}{2}(1-\cos\beta)&-\tfrac{1}{\sqrt{2}}\sin\beta&\tfrac{1}{2}(1-\cos\beta)\\
\tfrac{1}{\sqrt{2}}\sin\beta&1-(1-\cos\beta)&-\tfrac{1}{\sqrt{2}}\sin\beta\\
\tfrac{1}{2}(1-\cos\beta)&\tfrac{1}{\sqrt{2}}\sin\beta&1-\tfrac{1}{2}(1-\cos\beta)\end{bmatrix}\\
e^{-iJ_y\beta/\hbar}&=\begin{bmatrix}
\tfrac{1}{2}(1+\cos\beta)&-\tfrac{1}{\sqrt{2}}\sin\beta&\tfrac{1}{2}(1-\cos\beta)\\
\tfrac{1}{\sqrt{2}}\sin\beta&\cos\beta&-\tfrac{1}{\sqrt{2}}\sin\beta\\
\tfrac{1}{2}(1-\cos\beta)&\tfrac{1}{\sqrt{2}}\sin\beta&\tfrac{1}{2}(1+\cos\beta)\end{bmatrix}
\end{align}$$
Thus concludes the proof of this operation.

---
## Question 3.42
Consider a spherical tensor of rank 1 (vector):
$$\begin{align}
V^{(1)}_{\pm1}&=\mp\dfrac{V_x\pm iV_y}{\sqrt2}, & V_{0}^{(1)}=V_z
\end{align}$$
Using the expression for $d^{j=1}$ given in Problem 3.38, evaluate
$$\begin{align}
V_q'&=\sum_{q'}d_{qq'}(\beta)V_{q'}
\end{align}$$
and show that your results are just what you expect from the transformation properties of $V_{x,y,z}$ under rotations about the $y$-axis.

Start with the matrix:
$$\begin{align}
d^{(j=1)}(\beta)&=\begin{bmatrix}
\tfrac{1}{2}(1+\cos\beta) & -\tfrac{1}{\sqrt2}\sin\beta & \tfrac{1}{2}(1-\cos\beta)\\
\tfrac{1}{\sqrt2}\sin\beta & \cos\beta & -\tfrac{1}{\sqrt2}\sin\beta\\
\tfrac{1}{2}(1-\cos\beta) & \tfrac{1}{\sqrt2}\sin\beta & \tfrac{1}{2}(1+\cos\beta)
\end{bmatrix}
\end{align}$$
For the 3 components, we see:
$$\begin{align}
V_{-1}'&=V_{-1}\tfrac{1}{2}(1+\cos\beta)-V_0\tfrac{1}{\sqrt2}\sin\beta+V_{+1}\tfrac{1}{2}(1-\cos\beta)\\
V_{0}'&=V_{-1}\tfrac{1}{\sqrt2}\sin\beta+V_0\cos\beta-V_{+1}\tfrac{1}{\sqrt2}\sin\beta\\
V_{+1}'&=V_{-1}\tfrac{1}{2}(1-\cos\beta)+V_0\tfrac{1}{\sqrt2}\sin\beta+V_{+1}\tfrac{1}{2}(1+\cos\beta)
\end{align}$$
We can rearrange the coefficients to:
$$\begin{align}
V_{-1}'&=\tfrac{V_{-1}+V_{+1}}{2}+\left(\tfrac{V_{-1}-V_{+1}}{2}\cos\beta-\tfrac{V_0}{\sqrt2}\sin\beta\right)\\
V_{0}'&=\sqrt2\left(\tfrac{V_{-1}-V_{+1}}{2}\sin\beta+\tfrac{V_0}{\sqrt{2}}\cos\beta\right)\\
V_{+1}'&=\tfrac{V_{-1}+V_{+1}}{2}-\left(\tfrac{V_{-1}-V_{+1}}{2}\cos\beta-\tfrac{V_0}{\sqrt2}\sin\beta\right)
\end{align}$$
If we invert the expressions of the elements, we see:
$$\begin{align}
&&V^{'}_{+1}&=-\dfrac{V_x'+iV_y'}{\sqrt2} & V^{'}_{-1}&=\dfrac{V_x'-iV_y'}{\sqrt2}\\
\implies&&V_x'&=\dfrac{V^{'}_{-1}-V^{'}_{+1}}{\sqrt2} & V_y'&=i\dfrac{V^{'}_{-1}+V^{'}_{+1}}{\sqrt2}
\end{align}$$
Substituting our expressions back in, we see:
$$\begin{align}
V_x'&=\dfrac{V^{'}_{-1}-V^{'}_{+1}}{\sqrt2}\\
&=\dfrac{\tfrac{V_{-1}+V_{+1}}{2}+\left(\tfrac{V_{-1}-V_{+1}}{2}\cos\beta-\tfrac{V_0}{\sqrt2}\sin\beta\right)-\tfrac{V_{-1}+V_{+1}}{2}+\left(\tfrac{V_{-1}-V_{+1}}{2}\cos\beta-\tfrac{V_0}{\sqrt2}\sin\beta\right)}{\sqrt2}\\
&=2\dfrac{\tfrac{V_{-1}-V_{+1}}{2}\cos\beta-\tfrac{V_0}{\sqrt2}\sin\beta}{\sqrt2}\\
&=\tfrac{\sqrt{2}}{2}(V_{-1}-V_{+1})\cos\beta-V_0\sin\beta\\
\Aboxed{V_x'&=V_x\cos\beta-V_z\sin\beta}\\\\
V_y'&=i\dfrac{V^{'}_{-1}+V^{'}_{+1}}{\sqrt2}\\
&=i\dfrac{\tfrac{V_{-1}+V_{+1}}{2}+\left(\tfrac{V_{-1}-V_{+1}}{2}\cos\beta-\tfrac{V_0}{\sqrt2}\sin\beta\right)+\tfrac{V_{-1}+V_{+1}}{2}-\left(\tfrac{V_{-1}-V_{+1}}{2}\cos\beta-\tfrac{V_0}{\sqrt2}\sin\beta\right)}{\sqrt2}\\
\Aboxed{V_y'&=i\dfrac{V_{-1}+V_{+1}}{\sqrt2}}\\\\
V_z'&=V'_0\\
V_z'&=\tfrac{\sqrt2}{2}(V_{-1}-V_{+1})\sin\beta+V_0\cos\beta\\
\Aboxed{V_z'&=V_x\sin\beta+V_z\cos\beta}
\end{align}$$
What is immediately apparent is that $V_y=V_y'$, which is expected for a rotation about the Y axis.

In addition, the $V_x$ and $V_z$ look to be a rotated version of their original state, given by:
$$\begin{align}
\begin{bmatrix}V_x'\\V_z'\end{bmatrix}&=\begin{bmatrix}\cos\beta&-\sin\beta\\\sin\beta&\cos\beta\end{bmatrix}\begin{bmatrix}V_x\\V_z\end{bmatrix}\\
\end{align}$$
This is, indeed, a rotation matrix around a circle, though with the angle reversed. This is a matter of convention, however, so realistically it does not make a difference in the end.

---
## Question 3.45
For this kind of tensor, it can be split into 3 parts:
$$\begin{align}
T&=\text{Scalar}+\text{Anti-Symmetric Vector}+\text{Symmetric 2-Tensor}\\
T^{(2)}_{\pm2}&=x^2-y^2\pm 2ixy\\
T^{(2)}_{\pm1}&=(x\pm iy)z\\
T^{(2)}_{0}&=3z^2-r^2\\
\end{align}$$
### Question 3.45.A
Write $xy$, $xz$, and $(x^2-y^2)$ as components of the components of a spherical (irreducible) tensor of rank $2$.

From the above, we can see that:
$$\begin{align}
T^{(2)}_{\pm2}&=x^2-y^2\pm 2ixy\\
T^{(2)}_{\pm1}&=(x\pm iy)z\\
T^{(2)}_{0}&=3z^2-r^2\\
\end{align}$$
The only terms that have $xy$ in it is $T^{(2)}_{\pm2}$, and so:
$$\begin{align}
&&T^{(2)}_{+2}&=x^2-y^2+2ixy\\
-&&T^{(2)}_{-2}&=x^2-y^2-2ixy\\
&&T^{(2)}_{+2}-T^{(2)}_{-2}&=(x^2-y^2+2ixy)-(x^2-y^2-2ixy)\\
&&T^{(2)}_{+2}-T^{(2)}_{-2}&=4ixy\\
&&\Aboxed{xy&=\dfrac{T^{(2)}_{+2}-T^{(2)}_{-2}}{4i}}
\end{align}$$
For the $(x^2-y^2)$ term, once again only the $T^{(2)}_{\pm2}$, and so:
$$\begin{align}
&&T^{(2)}_{+2}&=x^2-y^2+2ixy\\
+&&T^{(2)}_{-2}&=x^2-y^2-2ixy\\
&&T^{(2)}_{+2}+T^{(2)}_{-2}&=(x^2-y^2+2ixy)+(x^2-y^2-2ixy)\\
&&T^{(2)}_{+2}+T^{(2)}_{-2}&=2(x^2-y^2)\\
&&\Aboxed{(x^2-y^2)&=\dfrac{T^{(2)}_{+2}+T^{(2)}_{-2}}{2}}
\end{align}$$
Lastly, for $xz$, those come from the $T^{(2)}_{\pm1}$ term, and so:
$$\begin{align}
&&T^{(2)}_{+1}&=(x+iy)z\\
+&&T^{(2)}_{-1}&=(x-iy)z\\
&&T^{(2)}_{+1}-T^{(2)}_{-1}&=(x+iy)z+(x-iy)z\\
&&T^{(2)}_{+1}-T^{(2)}_{-1}&=2xz\\
&&\Aboxed{xz&=\dfrac{T^{(2)}_{+1}-T^{(2)}_{-1}}{2}}
\end{align}$$
---
### Question 3.45.B
The expectation value
$$\begin{align}
Q&\equiv e\bra{j,j}(3z^2-r^2)\ket{j,j}
\end{align}$$
is know the the *quadrupole* moment. Evaluate
$$\begin{align}
e\bra{j,m'}(x^2-y^2)\ket{j,j}
\end{align}$$
(where $m'=j,j-1,j-2,\dots$) in terms of $Q$ and appropriate Clebsch-Gordan coefficients.

First off, we can use our expected value with the Wigner-Eckart Theorem as:
$$\begin{align}
\bra{j,m}T^{(k)}_{q}\ket{j',m'}&=\dfrac{\bra{j}\ ||T^{(k)}||\ \ket{j'}}{\sqrt{2j+1}}\braket{j',m',k,q|j, m}\\
\bra{j,j}T^{(2)}_{0}\ket{j,j}&=\dfrac{\bra{j}\ ||T^{(2)}||\ \ket{j}}{\sqrt{2j+1}}\braket{j,j,2,0|j, j}\\\\
Q&\equiv e\bra{j,j}T^{(2)}_{0}\ket{j,j}\\
Q&=e\dfrac{\bra{j}\ ||T^{(2)}||\ \ket{j}}{\sqrt{2j+1}}\braket{j,j,2,0|j, j}\\
\Aboxed{\dfrac{Q/e}{\braket{j,j,2,0|j, j}}&=\dfrac{\bra{j}\ ||T^{(2)}||\ \ket{j}}{\sqrt{2j+1}}}
\end{align}$$
We can now evaluate the problem's statement:
$$\begin{align}
e\bra{j,m'}(x^2-y^2)\ket{j,j}&=e\bra{j,m'}\dfrac{T^{(2)}_{+2}+T^{(2)}_{-2}}{2}\ket{j,j}\\
&=\dfrac{e}{2}\left[\bra{j,m'}T^{(2)}_{+2}\ket{j,j}+\bra{j,m'}T^{(2)}_{-2}\ket{j,j}\right]\\
\end{align}$$
Similar to before, we can evaluate these using the Wigner-Eckart Theorem:
$$\begin{align}
\bra{j,m}T^{(k)}_{q}\ket{j',m'}&=\dfrac{\bra{j}\ ||T^{(k)}||\ \ket{j'}}{\sqrt{2j+1}}\braket{j',m',k,q|j, m}\\\\
\bra{j,m'}T^{(2)}_{-2}\ket{j,j}&=\dfrac{\bra{j}\ ||T^{(2)}||\ \ket{j}}{\sqrt{2j+1}}\braket{j,j,2,-2|j,m'}\\
\bra{j,m'}T^{(2)}_{+2}\ket{j,j}&=\dfrac{\bra{j}\ ||T^{(2)}||\ \ket{j}}{\sqrt{2j+1}}\braket{j,j,2,+2|j,m'}
\end{align}$$
Under these conditions, selections rules force:
$$\begin{align}
T^{(2)}_{-2}: && m'&=j-2 && \text{Satisfiable}\\
T^{(2)}_{+2}: && m'&=j+2 && \text{Unsatisfiable}\\
\end{align}$$
Thus, only the $T^{(2)}_{-2}$ will be non-zero, and so:
$$\begin{align}
e\bra{j,m'}(x^2-y^2)\ket{j,j}
&=\dfrac{e}{2}\left[\bra{j,m'}T^{(2)}_{+2}\ket{j,j}+\bra{j,m'}T^{(2)}_{-2}\ket{j,j}\right]\\
&=\dfrac{e}{2}\bra{j,m'}T^{(2)}_{-2}\ket{j,j}\\
&=\dfrac{e}{2}\dfrac{\bra{j}\ ||T^{(2)}||\ \ket{j}}{\sqrt{2j+1}}\braket{j,j,2,-2|j,j-2}
\end{align}$$
We can substitute our expression for $Q$ from earlier, and so:
$$\begin{align}
e\bra{j,m'}(x^2-y^2)\ket{j,j}
&=\dfrac{e}{2}\dfrac{\bra{j}\ ||T^{(2)}||\ \ket{j}}{\sqrt{2j+1}}\braket{j,j,2,-2|j,j-2}\\
&=\dfrac{e}{2}\dfrac{Q/e}{\braket{j,j,2,0|j, j}}\braket{j,j,2,-2|j,j-2}\\
\Aboxed{e\bra{j,m'}(x^2-y^2)\ket{j,j}&=\dfrac{Q}{2}\dfrac{\braket{j,j,2,-2|j,j-2}}{\braket{j,j,2,0|j, j}}}
\end{align}$$
