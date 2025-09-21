Author: Stanley Goodwin
Date: September 14th, 2025

---

### Question 1.3
For spin $1/2$ state $\ket{S_x;+}$, evaluate both sides of the inequality:
$$\begin{align}
\left\langle(\Delta A)^2\right\rangle\left\langle(\Delta B)^2\right\rangle\ge\dfrac{1}{4}\left|\left\langle[A,B]\right\rangle\right|^2
\end{align}$$
for the operators $A=S_x$ and $B=S_y$, and show that the inequality is satisfied.
Repeat for operators $A=S_z$ and $B=S_y$.

---
#### Case 1
$$\begin{align}
\braket{(\Delta S_x)^2}\ket{S_x;+}
&=\braket{(S_x)^2}\ket{S_x;+}-\braket{(S_x)}^2\ket{S_x;+}\\
&=\dfrac{\hbar^2}{4}\ket{S_x;+}-\left(\dfrac{\hbar}{2}\right)^2\ket{S_x;+}\\
&=\left(\dfrac{\hbar^2}{4}-\dfrac{\hbar^2}{4}\right)\ket{S_x;+}\\
\Aboxed{\braket{(\Delta S_x)^2}\ket{S_x;+}&=0}
\end{align}$$
This also implies that:
$$\begin{align}
\braket{(\Delta S_x)^2}\ket{S_x;+}
&=\braket{(S_x)^2}\ket{S_x;+}-\braket{(S_x)}^2\ket{S_x;+}\\
&=\dfrac{\hbar^2}{4}\ket{S_x;+}-\left(\dfrac{\hbar}{2}\right)^2\ket{S_x;+}\\
&=\left(\dfrac{\hbar^2}{4}-\dfrac{\hbar^2}{4}\right)\ket{S_x;+}\\
\Aboxed{\braket{(\Delta S_x)^2}\braket{(\Delta S_y)^2}\ket{S_x;+}&=0}
\end{align}$$
For the other side:
$$\begin{align}
\dfrac{1}{4}\left|\left\langle[S_x,S_y]\right\rangle\right|^2\ket{S_x;+}
&=\dfrac{1}{4}\left|i\hbar\braket{S_z}\right|^2\ket{S_x;+}\\
&=\dfrac{1}{4}\left|i\hbar\right|^2\braket{S_z}^2\ket{S_x;+}\\
&=\dfrac{1}{4}\left|i\hbar\right|^2\cdot0^2\ket{S_x;+}\\
\Aboxed{\dfrac{1}{4}\left|\left\langle[S_x,S_y]\right\rangle\right|^2\ket{S_x;+}&=0}
\end{align}$$
Through substitution, we can see that:
$$\begin{align}
\left\langle(\Delta S_x)^2\right\rangle\left\langle(\Delta S_y)^2\right\rangle&\ge\dfrac{1}{4}\left|\left\langle[S_x,S_y]\right\rangle\right|^2 & \implies\\
\Aboxed{0&\ge0}
\end{align}$$
---
#### Case 2
$$\begin{align}
\braket{(\Delta S_z)^2}\braket{(\Delta S_y)^2}\ket{S_x;+}
&=\braket{(\Delta S_z)^2}\left(\braket{(\Delta S_y)^2}\ket{S_x;+}\right)\\
&=\braket{(\Delta S_z)^2}\left(\dfrac{\hbar^2}{4}-0^2\right)\ket{S_x;+}\\
&=\dfrac{\hbar^2}{4}\left(\braket{(\Delta S_z)^2}\right)\ket{S_x;+}\\
&=\dfrac{\hbar^2}{4}\left(\dfrac{\hbar^2}{4}-0^2\right)\ket{S_x;+}\\
\Aboxed{\braket{(\Delta S_z)^2}\braket{(\Delta S_y)^2}\ket{S_x;+}&=\dfrac{\hbar^4}{16}\ket{S_x;+}}
\end{align}$$
For the other side:
$$\begin{align}
\dfrac{1}{4}\left|\left\langle[S_z,S_y]\right\rangle\right|^2\ket{S_x;+}
&=\dfrac{1}{4}\left|-i\hbar\braket{S_x}\right|^2\ket{S_x;+}\\
&=\dfrac{1}{4}\left|-i\hbar\right|^2\braket{S_x}^2\ket{S_x;+}\\
&=\dfrac{1}{4}\left|i\hbar\right|^2\cdot\left(\dfrac{\hbar}{2}\right)^2\ket{S_x;+}\\
&=\dfrac{\hbar^2}{4}\cdot\dfrac{\hbar^2}{4}\ket{S_x;+}\\
\Aboxed{\dfrac{1}{4}\left|\left\langle[S_z,S_y]\right\rangle\right|^2\ket{S_x;+}&=\dfrac{\hbar^4}{16}\ket{S_x;+}}
\end{align}$$
Through substitution, we can see that:
$$\begin{align}
\left\langle(\Delta S_z)^2\right\rangle\left\langle(\Delta S_y)^2\right\rangle&\ge\dfrac{1}{4}\left|\left\langle[S_z,S_y]\right\rangle\right|^2 & \implies\\
\Aboxed{\dfrac{\hbar^4}{16}&\ge\dfrac{\hbar^4}{16}}
\end{align}$$
---
### Question 1.7
#### 1.7.A
Consider 2 kets $\ket{\alpha}$ and $\ket{\beta}$. Suppose both are representable in the basis $\ket{a'},\ket{a''},\ket{a'''},\dots$
Find the matrix representation of the operator $\ket\alpha\bra\beta$ in this basis.
$$\begin{align}
\ket{\alpha}&=\sum_n\left(\braket{a^{(n)}|\alpha}\right)\ket{a^{(n)}}\\
\bra{\beta}&=\sum_m\left(\braket{a^{(m)}|\beta}\right)^\dagger\bra{a^{(m)}}\\
\end{align}$$
We can then write the outer product as:
$$\begin{align}
\ket{\alpha}\bra{\beta}
&=\sum_n\left(\braket{a^{(n)}|\alpha}\right)\ket{a^{(n)}}\cdot \sum_m\left(\braket{a^{(m)}|\beta}\right)^\dagger\bra{a^{(m)}}\\
\Aboxed{\ket{\alpha}\bra{\beta}&=\sum_n\sum_m\left[\left(\braket{a^{(n)}|\alpha}\right) \left(\braket{a^{(m)}|\beta}\right)^*\right]\ket{a^{(n)}}\bra{a^{(m)}}}
\end{align}$$
Since we consider bra and ket vectors to be row and column vectors respectively, this is also the matrix form of the system. Since this is unbounded in size, I will not write this as a matrix, but I can express this as a linear transform tensor as (assuming Einstein notation):
$$\begin{align}
\ket{\alpha}\bra{\beta}&=L_{nm}\ket{a^{(n)}}\bra{a^{(m)}}\\
L_{nm}&=\left(\braket{a^{(n)}|\alpha}\right) \left(\braket{a^{(m)}|\beta}\right)^*
\end{align}$$
I guess if we wanted to write it as an explicit matrix, we can write it as:
$$\begin{align}
\ket{\alpha}\bra{\beta}
&=\begin{bmatrix}\left(\braket{a^{(1)}|\alpha}\right) \left(\braket{a^{(1)}|\beta}\right)^*&\left(\braket{a^{(1)}|\alpha}\right) \left(\braket{a^{(2)}|\beta}\right)^* &\dots\\
\left(\braket{a^{(2)}|\alpha}\right) \left(\braket{a^{(1)}|\beta}\right)^*&\left(\braket{a^{(2)}|\alpha}\right) \left(\braket{a^{(2)}|\beta}\right)^* &\dots\\
\vdots&\vdots&\ddots\end{bmatrix}
\end{align}$$
Summation is significantly nicer looking, so I hope we continue to use it instead.

---

#### 1.7.B
We now consider a spin $1/2$ system and let $\ket{\alpha}$ and $\ket{\beta}$ be $\ket{S_z;+}$ and $\ket{S_x;+}$ respectively.
Write down the explicit square matrix that corresponds to $\ket\alpha\bra\beta$ in the $z$ basis.
$$\begin{align}
\ket{\alpha}&=\ket{S_z;+}\\
\bra{\beta}&=\bra{S_x;+}=\dfrac{1}{\sqrt{2}}\bra{S_z;+}+\dfrac{1}{\sqrt{2}}\bra{S_z;-}\\
\end{align}$$
Since our basis is $z$, we know the basis vectors in terms of rows and columns, and so:
$$\begin{align}
\ket{\alpha}&=\begin{bmatrix}1\\0\end{bmatrix}\\
\bra{\beta}&=\dfrac{1}{\sqrt{2}}\begin{bmatrix}1&1\end{bmatrix}
\end{align}$$
The outer product is then:
$$\begin{align}
\ket{\alpha}\bra{\beta}
&=\begin{bmatrix}1\\0\end{bmatrix}\cdot\dfrac{1}{\sqrt{2}}\begin{bmatrix}1&1\end{bmatrix}\\
&=\dfrac{1}{\sqrt{2}}\begin{bmatrix}1\\0\end{bmatrix}\begin{bmatrix}1&1\end{bmatrix}\\
\ket{\alpha}\bra{\beta}&=\dfrac{1}{\sqrt{2}}\begin{bmatrix}1&1\\0&0\end{bmatrix}
\end{align}$$
---
### Question 1.10
Using the orthonormality of $\ket{+}$ and $\ket-$, prove:
$$\begin{align}
[S_i,S_j]&=i\hbar\epsilon_{ijk}S_k & \{S_i,S_j\}&=\dfrac{\hbar^2}{2}\delta_{ij}
\end{align}$$
Where (+,- notation actually sucks, using arrows instead):
$$\begin{align}
S_x&=\dfrac{\hbar}{2}\left(\ket\uparrow\bra\downarrow+\ket\downarrow\bra\uparrow\right)\\
S_y&=i\dfrac{\hbar}{2}\left(\ket\downarrow\bra\uparrow-\ket\uparrow\bra\downarrow\right)\\
S_z&=\dfrac{\hbar}{2}\left(\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)\\
\end{align}$$
#### Proof of $[S_x,S_y]$
$$\begin{align}
S_xS_y&=\dfrac{\hbar}{2}\cdot i\dfrac{\hbar}{2}\left(\ket\uparrow\bra\downarrow+\ket\downarrow\bra\uparrow\right)\left(\ket\downarrow\bra\uparrow-\ket\uparrow\bra\downarrow\right)\\
&=i\dfrac{\hbar^2}{4}\left(\ket\uparrow\bra\downarrow\ket\downarrow\bra\uparrow+\ket\downarrow\bra\uparrow\ket\downarrow\bra\uparrow-\ket\uparrow\bra\downarrow\ket\uparrow\bra\downarrow-\ket\downarrow\bra\uparrow\ket\uparrow\bra\downarrow\right)\\
&=i\dfrac{\hbar^2}{4}\left(\ket\uparrow1\bra\uparrow+\ket\downarrow0\bra\uparrow-\ket\uparrow0\bra\downarrow-\ket\downarrow1\bra\downarrow\right)\\
&=i\dfrac{\hbar^2}{4}\left(\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)\\
&=i\dfrac{\hbar}{2}\cdot\dfrac{\hbar}{2}\left(\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)\\
\Aboxed{S_xS_y&=i\dfrac{\hbar}{2}S_z}
\end{align}$$
We exploit that $S_x, S_y$ and $S_z$ are Hermitian so:
$$\begin{align}
S_xS_y&=i\dfrac{\hbar}{2}S_z\\
S_x^\dagger S_y^\dagger &=i\dfrac{\hbar}{2}S_z\\
\left(S_yS_x\right)^\dagger&=i\dfrac{\hbar}{2}S_z\\
S_yS_x&=-i\dfrac{\hbar}{2}S_z^\dagger\\
\Aboxed{S_yS_x&=-i\dfrac{\hbar}{2}S_z}
\end{align}$$
In total:
$$\begin{align}
[S_x,S_y]&=S_xS_y-S_yS_x\\
&=i\dfrac{\hbar}{2}S_z-\left(-i\dfrac{\hbar}{2}S_z\right)\\
\Aboxed{[S_x,S_y]&=+i\hbar S_z}\\
\Aboxed{[S_y,S_x]&=-i\hbar S_z}\\
\end{align}$$
#### Proof of $[S_y,S_z]$
$$\begin{align}
S_yS_z&=i\dfrac{\hbar}{2}\cdot\dfrac{\hbar}{2}\left(\ket\downarrow\bra\uparrow-\ket\uparrow\bra\downarrow\right)\left(\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)\\
&=i\dfrac{\hbar}{2}\cdot\dfrac{\hbar}{2}\left(\ket\downarrow\bra\uparrow\ket\uparrow\bra\uparrow-\ket\uparrow\bra\downarrow\ket\uparrow\bra\uparrow-\ket\downarrow\bra\uparrow\ket\downarrow\bra\downarrow+\ket\uparrow\bra\downarrow\ket\downarrow\bra\downarrow\right)\\
&=i\dfrac{\hbar}{2}\cdot\dfrac{\hbar}{2}\left(\ket\downarrow1\bra\uparrow-\ket\uparrow0\bra\uparrow-\ket\downarrow0\bra\downarrow+\ket\uparrow1\bra\downarrow\right)\\
&=i\dfrac{\hbar}{2}\cdot\dfrac{\hbar}{2}\left(\ket\downarrow\bra\uparrow+\ket\uparrow\bra\downarrow\right)\\
\Aboxed{S_yS_z&=i\dfrac{\hbar}{2}S_x}
\end{align}$$
We exploit that $S_x, S_y$ and $S_z$ are Hermitian so:
$$\begin{align}
S_yS_z&=i\dfrac{\hbar}{2}S_x\\
S_y^\dagger S_z^\dagger &=i\dfrac{\hbar}{2}S_x\\
\left(S_zS_y\right)^\dagger&=i\dfrac{\hbar}{2}S_x\\
S_zS_y&=-i\dfrac{\hbar}{2}S_x^\dagger\\
\Aboxed{S_zS_y&=-i\dfrac{\hbar}{2}S_x}
\end{align}$$
In total:
$$\begin{align}
[S_y,S_z]&=S_yS_z-S_zS_y\\
&=i\dfrac{\hbar}{2}S_x-\left(-i\dfrac{\hbar}{2}S_x\right)\\
\Aboxed{[S_y,S_z]&=+i\hbar S_x}\\
\Aboxed{[S_z,S_y]&=-i\hbar S_x}\\
\end{align}$$
#### Proof of $[S_z,S_x]$
$$\begin{align}
S_zS_x&=\dfrac{\hbar}{2}\cdot\dfrac{\hbar}{2}\left(\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)\left(\ket\uparrow\bra\downarrow+\ket\downarrow\bra\uparrow\right)\\
&=\dfrac{\hbar}{2}\cdot\dfrac{\hbar}{2}\left(\ket\uparrow\bra\uparrow\ket\uparrow\bra\downarrow-\ket\downarrow\bra\downarrow\ket\uparrow\bra\downarrow+\ket\uparrow\bra\uparrow\ket\downarrow\bra\uparrow-\ket\downarrow\bra\downarrow\ket\downarrow\bra\uparrow\right)\\
&=\dfrac{\hbar}{2}\cdot\dfrac{\hbar}{2}\left(\ket\uparrow1\bra\downarrow-\ket\downarrow0\bra\downarrow+\ket\uparrow0\bra\uparrow-\ket\downarrow1\bra\uparrow\right)\\
&=i\dfrac{\hbar}{2}\cdot -i\dfrac{\hbar}{2}\left(\ket\uparrow\bra\downarrow-\ket\downarrow\bra\uparrow\right)\\
\Aboxed{S_zS_x&=i\dfrac{\hbar}{2}S_y}
\end{align}$$
We exploit that $S_x, S_y$ and $S_z$ are Hermitian so:
$$\begin{align}
S_zS_x&=i\dfrac{\hbar}{2}S_y\\
S_z^\dagger S_x^\dagger &=i\dfrac{\hbar}{2}S_y\\
\left(S_xS_z\right)^\dagger&=i\dfrac{\hbar}{2}S_y\\
S_xS_z&=-i\dfrac{\hbar}{2}S_y^\dagger\\
\Aboxed{S_xS_z&=-i\dfrac{\hbar}{2}S_y}
\end{align}$$
In total:
$$\begin{align}
[S_z,S_x]&=S_zS_x-S_xS_z\\
&=i\dfrac{\hbar}{2}S_y-\left(-i\dfrac{\hbar}{2}S_y\right)\\
\Aboxed{[S_z,S_x]&=+i\hbar S_y}\\
\Aboxed{[S_x,S_z]&=-i\hbar S_y}\\
\end{align}$$
#### Anti-Commutator
To show the anti-commutator relations, I'll exploit knowing the commutators from previous proof.
$$\begin{align}
\{S_j,S_i\}&=S_jS_i+S_iS_j\\
&=S_jS_i-S_iS_j+2S_iS_j\\
&=[S_j,S_i]+2S_iS_j\\
\{S_j,S_i\}&=-[S_i,S_j]+2S_iS_j\\
\end{align}$$
For non-equal indices of $i,j$, we can then see:
$$\begin{align}
\{S_y,S_x\}&=-[S_x,S_y]+2S_xS_y\\
&=-\left(i\hbar S_z\right)+2\left(i\dfrac{\hbar}{2}S_z\right)\\
&=-\left(i\hbar S_z\right)+\left(i\hbar S_z\right)\\
\Aboxed{\{S_y,S_x\}&=0}\\\\
\{S_z,S_y\}&=-[S_y,S_z]+2S_yS_z\\
&=-\left(i\hbar S_x\right)+2\left(i\dfrac{\hbar}{2}S_x\right)\\
&=-\left(i\hbar S_x\right)+\left(i\hbar S_x\right)\\
\Aboxed{\{S_z,S_y\}&=0}\\\\
\{S_x,S_z\}&=-[S_z,S_x]+2S_zS_x\\
&=-\left(i\hbar S_y\right)+2\left(i\dfrac{\hbar}{2}S_y\right)\\
&=-\left(i\hbar S_y\right)+\left(i\hbar S_y\right)\\
\Aboxed{\{S_x,S_z\}&=0}\\
\end{align}$$
For equal indices:
$$\begin{align}
\{S_i,S_i\}&=-[S_i,S_i]+2S_iS_i\\
&=2S_iS_i\\
\Aboxed{\{S_i,S_i\}&=2|S_i|^2}\\
\Aboxed{\{S_i,S_j\}&=2S_iS_j\cdot\delta_{ij}}\\
\end{align}$$
For the equal-index products, we have:
$$\begin{align}
S_x^2&=\left(\dfrac{\hbar}{2}\right)^2\left(\ket\uparrow\bra\downarrow+\ket\downarrow\bra\uparrow\right)^2\\
&=\left(\dfrac{\hbar}{2}\right)^2\left(\ket\uparrow\bra\downarrow\ket\uparrow\bra\downarrow+\ket\downarrow\bra\uparrow\ket\uparrow\bra\downarrow+\ket\uparrow\bra\downarrow\ket\downarrow\bra\uparrow+\ket\downarrow\bra\uparrow\ket\downarrow\bra\uparrow\right)\\
&=\left(\dfrac{\hbar}{2}\right)^2\left(\ket\uparrow0\bra\downarrow+\ket\downarrow1\bra\downarrow+\ket\uparrow1\bra\uparrow+\ket\downarrow0\bra\uparrow\right)\\
&=\left(\dfrac{\hbar}{2}\right)^2\left(\ket\downarrow\bra\downarrow+\ket\uparrow\bra\uparrow\right)\\
S_x^2&=\left(\dfrac{\hbar}{2}\right)^2\mathbb{I}\\
\Aboxed{\{S_x,S_x\}&=\dfrac{\hbar^2}{2}}\\\\

S_y^2&=\left(i\dfrac{\hbar}{2}\right)^2\left(\ket\downarrow\bra\uparrow-\ket\uparrow\bra\downarrow\right)^2\\
&=\left(i\dfrac{\hbar}{2}\right)^2\left(\ket\downarrow\bra\uparrow\ket\downarrow\bra\uparrow-\ket\uparrow\bra\downarrow\ket\downarrow\bra\uparrow-\ket\downarrow\bra\uparrow\ket\uparrow\bra\downarrow+\ket\uparrow\bra\downarrow\ket\uparrow\bra\downarrow\right)\\
&=-\left(\dfrac{\hbar}{2}\right)^2\left(\ket\downarrow0\bra\uparrow-\ket\uparrow1\bra\uparrow-\ket\downarrow1\bra\downarrow+\ket\uparrow0\bra\downarrow\right)\\
&=-\left(\dfrac{\hbar}{2}\right)^2\left(-\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)\\
S_y^2&=\left(\dfrac{\hbar}{2}\right)^2\mathbb{I}\\
\Aboxed{\{S_y,S_y\}&=\dfrac{\hbar^2}{2}}\\\\

S_z^2&=\left(\dfrac{\hbar}{2}\right)^2\left(\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)^2\\
&=\left(\dfrac{\hbar}{2}\right)^2\left(\ket\uparrow\bra\uparrow\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\ket\uparrow\bra\uparrow-\ket\uparrow\bra\uparrow\ket\downarrow\bra\downarrow+\ket\downarrow\bra\downarrow\ket\downarrow\bra\downarrow\right)\\
&=\left(\dfrac{\hbar}{2}\right)^2\left(\ket\uparrow1\bra\uparrow-\ket\downarrow0\bra\uparrow-\ket\uparrow0\bra\downarrow+\ket\downarrow1\bra\downarrow\right)\\
&=\left(\dfrac{\hbar}{2}\right)^2\left(\ket\uparrow\bra\uparrow+\ket\downarrow\bra\downarrow\right)\\
S_z^2&=\left(\dfrac{\hbar}{2}\right)^2\mathbb{I}\\
\Aboxed{\{S_z,S_z\}&=\dfrac{\hbar^2}{2}}
\end{align}$$
#### Combining all together
For the commutator:
$$\begin{align}
[S_x,S_x]&=0 & [S_x,S_y]&=+i\hbar S_z & [S_x,S_z]&=-i\hbar S_y\\
[S_y,S_x]&=-i\hbar S_z & [S_y,S_y]&=0 & [S_y,S_z]&=+i\hbar S_x\\
[S_z,S_x]&=+i\hbar S_y & [S_z,S_y]&=-i\hbar S_x & [S_z,S_z]&=0\\
\end{align}$$
Defined a new tensor, Levi-Civita:
$$\begin{align}
\epsilon_{ijk}&=\begin{cases}+1 & \text(i\rightarrow j\rightarrow k)\\-1 & \text(i\leftarrow j\leftarrow k)\\0&\text(i=j)\end{cases}
\end{align}$$
We can finally express the commutator as:
$$\begin{align}
\Aboxed{[S_i,S_j]&=i\hbar\epsilon_{ijk}S_k}
\end{align}$$
For the anti-commutator:
$$\begin{align}
\{S_x,S_x\}&=\hbar^2/2 & \{S_x,S_y\}&=0 & \{S_x,S_z\}&=0\\
\{S_y,S_x\}&=0& \{S_y,S_y\}&=\hbar^2/2 & \{S_y,S_z\}&=0\\
\{S_z,S_x\}&=0 & \{S_z,S_y\}&=0 & \{S_z,S_z\}&=\hbar^2/2\\
\end{align}$$
We can finally express the commutator as:
$$\begin{align}
\Aboxed{\{S_i,S_j\}&=\dfrac{\hbar^2}{2}\delta_{ij}}
\end{align}$$
---
### Question 1.11
Construct $\ket{S\cdot\hat{n};+}$ such that:
$$\begin{align}
S\cdot\hat{n}\ket{S\cdot\hat{n};+}&=\dfrac{\hbar}{2}\ket{S\cdot\hat{n};+}
\end{align}$$
where $\hat{n}$ is characterized by the angles shown in the figure.
Express your answer as a linear combination of $\ket+$ and $\ket-$.

We can write the vector $\hat{n}$ in spherical coordinates as:
$$\begin{align}
\hat{n}&=\sin\beta\cos\alpha\ \hat{x}+\sin\beta\sin\alpha\ \hat{y}+\cos\beta\ \hat{z}
\end{align}$$
The spin basis is in the direction of this $\hat{n}$ vector, and so:
$$\begin{align}
S\cdot\hat{n}&=S_x\sin\beta\cos\alpha+S_y\sin\beta\sin\alpha+S_z\cos\beta
\end{align}$$
Writing these 3 matrices in the $z$-basis, we get:
$$\begin{align}
S\cdot\hat{n}&=\dfrac{\hbar}{2}\left(\ket\uparrow\bra\downarrow+\ket\downarrow\bra\uparrow\right)\sin\beta\cos\alpha\\
&-i\dfrac{\hbar}{2}\left(\ket\uparrow\bra\downarrow-\ket\downarrow\bra\uparrow\right)\sin\beta\sin\alpha\\
&+\dfrac{\hbar}{2}\left(\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)\cos\beta
\end{align}$$
$$\begin{align}
S\cdot\hat{n}&=\dfrac{\hbar}{2}\sin\beta\left(\cos\alpha-i\sin\alpha\right)\ket\uparrow\bra\downarrow+\dfrac{\hbar}{2}\sin\beta\left(\cos\alpha+i\sin\alpha\right)\ket\downarrow\bra\uparrow+\dfrac{\hbar}{2}\cos\beta\left(\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)\\
&=\dfrac{\hbar}{2}\left[e^{-i\alpha}\sin\beta\ \ket\uparrow\bra\downarrow+e^{i\alpha}\sin\beta\ \ket\downarrow\bra\uparrow+\cos\beta\left(\ket\uparrow\bra\uparrow-\ket\downarrow\bra\downarrow\right)\right]\\
\end{align}$$
In matrix form, we see that:
$$\begin{align}
S\cdot\hat{n}&=\dfrac{\hbar}{2}\begin{bmatrix}\cos\beta&e^{-i\alpha}\sin\beta\\e^{i\alpha}\sin\beta&\cos\beta\end{bmatrix}
\end{align}$$
We want to find $\ket{S\cdot\hat{n};+}$ so that the condition is met:
$$\begin{align}
S\cdot\hat{n}\ket{S\cdot\hat{n};+}&=\dfrac{\hbar}{2}\ket{S\cdot\hat{n};+}
\end{align}$$
Substituting, we find the following expression:
$$\begin{align}
\dfrac{\hbar}{2}\begin{bmatrix}\cos\beta&e^{-i\alpha}\sin\beta\\e^{i\alpha}\sin\beta&-\cos\beta\end{bmatrix}\begin{bmatrix}a\\b\end{bmatrix}&=\dfrac{\hbar}{2}\begin{bmatrix}a\\b\end{bmatrix}
\end{align}$$
This is just an eigenvalue/eigenvector problem:
$$\begin{align}
\begin{bmatrix}\cos\beta-\lambda&e^{-i\alpha}\sin\beta\\e^{i\alpha}\sin\beta&-\cos\beta-\lambda\end{bmatrix}\begin{bmatrix}a\\b\end{bmatrix}&=0
\end{align}$$
$$\begin{align}
\det\begin{bmatrix}\cos\beta-\lambda&e^{-i\alpha}\sin\beta\\e^{i\alpha}\sin\beta&-\cos\beta-\lambda\end{bmatrix}&=0\\
\left(\lambda-\cos\beta\right)\left(\lambda+\cos\beta\right)-e^{-i\alpha}\sin\beta e^{i\alpha}\sin\beta&=0\\
\lambda^2-\cos^2\beta-e^{-i\alpha}e^{i\alpha}\sin^2\beta&=0\\
\cos^2\beta+\sin^2\beta&=\lambda^2\\
\Aboxed{\lambda&=\pm1}
\end{align}$$
The $\lambda=+1$ state corresponds to the $\ket{S\cdot\hat{n};+}$ state, and so:
$$\begin{align}
\begin{bmatrix}\cos\beta&e^{-i\alpha}\sin\beta\\e^{i\alpha}\sin\beta&-\cos\beta\end{bmatrix}\begin{bmatrix}a\\b\end{bmatrix}&=+1\begin{bmatrix}a\\b\end{bmatrix}
\end{align}$$
Leaving us with:
$$\begin{align}
\begin{array}{c}
a\cos\beta+b\ e^{-i\alpha}\sin\beta&=a\\
a\ e^{i\alpha}\sin\beta-b\cos\beta&=b
\end{array}\\\\
\begin{array}{c}
b\ e^{-i\alpha}\sin\beta&=a(1-\cos\beta)\\
a\ e^{i\alpha}\sin\beta&=b(1+\cos\beta)
\end{array}
\end{align}$$
Solving for $b$, we see that:
$$\begin{align}
b&=\dfrac{(1-\cos\beta)}{e^{-i\alpha}\sin\beta}a\\
&=e^{i\alpha}\dfrac{2}{\sin\beta}\dfrac{1-\cos\beta}{2}a\\
&=e^{i\alpha}\dfrac{2}{2\sin\left(\tfrac{\beta}{2}\right)\cos\left(\tfrac{\beta}{2}\right)}\sin^2\left(\dfrac{\beta}{2}\right)a\\
b&=e^{i\alpha}\tan\left(\dfrac{\beta}{2}\right)a
\end{align}$$
Since $|a|^2+|b|^2=1$, we know that:
$$\begin{align}
a^2+|e^{i\alpha}|^2\tan^2\left(\dfrac{\beta}{2}\right)a^2&=1\\
a^2\left(1+\tan^2\left(\dfrac{\beta}{2}\right)\right)&=1\\
a^2\sec^2\left(\dfrac{\beta}{2}\right)&=1\\
\Aboxed{\cos\left(\dfrac{\beta}{2}\right)&=|a|}
\end{align}$$
Since phases don't really care about their value, just their difference, let $|a|=a$. Then:
$$\begin{align}
\ket{S\cdot\hat{n};+}&=\begin{bmatrix}\cos\left(\tfrac{\beta}{2}\right)\\e^{i\alpha}\tan\left(\tfrac{\beta}{2}\right)\cos\left(\tfrac{\beta}{2}\right)\end{bmatrix}\\
&=\begin{bmatrix}\cos\left(\tfrac{\beta}{2}\right)\\e^{i\alpha}\sin\left(\tfrac{\beta}{2}\right)\end{bmatrix}\\
\Aboxed{\ket{S\cdot\hat{n};+}&=\cos\left(\tfrac{\beta}{2}\right)\ket++e^{i\alpha}\sin\left(\tfrac{\beta}{2}\right)\ket-}
\end{align}$$
This correctly matches the value given in the book to compare against.