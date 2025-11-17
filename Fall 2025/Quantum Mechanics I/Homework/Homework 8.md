Author: Stanley Goodwin
Date: November 21st, 2025

---
## Question 3.19
### Question 3.19.A
Using the fact that $J_x,J_y,J_z$ and $J_\pm\equiv J_x\pm iJ_y$ satisfy the usual angular-momentum commutation relations, prove that:
$$\begin{align}
\vec{J}^2=J_z^2+J_+J_--\hbar J_z
\end{align}$$
Start with the definition of $\vec{J}^2=\sum_i J_i^2$, then:
$$\begin{align}
\vec{J}^2&=J_z^2+J_x^2+J_y^2\\
&=J_z^2+(J_x+iJ_y)(J_x-iJ_y)+iJ_xJ_y-iJ_yJ_x\\
&=J_z^2+(J_x+iJ_y)(J_x-iJ_y)+i[J_x,J_y]\\
&=J_z^2+J_+J_-+i(i\hbar J_z)\\
\Aboxed{\vec{J}^2&=J_z^2+J_+J_--\hbar J_z}
\end{align}$$
---
### Question 3.19.B
Using this result, or otherwise, derive the coefficient $c_-$ that appears in:
$$\begin{align}
J_-\ket{j,m}&=c_-\ket{j,m-1}
\end{align}$$
We can take the complex conjugate to also get:
$$\begin{align}
\bra{j,m}J_-^\dagger&=\bra{j,m}J_+=c_-^*\bra{j,m-1}
\end{align}$$
Combining these two, what we can see then is:
$$\begin{align}
\bra{j,m}J_+J_-\ket{j,m}&=c_-^*c_-\braket{j,m-1|j,m-1}=|c_-|^2
\end{align}$$
From the above, we can express $J_+J_-$ in terms of $\vec{J}^2$ and $J_z$ as:
$$\begin{align}
\bra{j,m}J_+J_-\ket{j,m}&=\bra{j,m}\left[\vec{J}^2-J_z^2+\hbar J_z\right]\ket{j,m}\\
&=\bra{j,m}\left[j(j+1)-m^2\hbar^2+\hbar\cdot m\hbar\right]\ket{j,m}\\
&=\bra{j,m}\left[j^2+j-m^2+m\right]\hbar^2\ket{j,m}\\
&=(j+m)(j-m+1)\hbar^2\braket{j,m|j,m}\\
|c_-|^2&=(j+m)(j-m+1)\hbar^2\\
\Aboxed{c_-&=\hbar\sqrt{(j+m)(j-m+1)}}
\end{align}$$
---
## Question 3.25
Suppose a half-integer $l$-value, say $\tfrac{1}{2}$, were allowed for orbital angular momentum. From:
$$\begin{align}
L_+Y_{1/2}^{1/2}(\theta,\phi)&=0
\end{align}$$
we may deduce, as usual,
$$\begin{align}
Y_{1/2}^{1/2}(\theta,\phi)&\propto e^{i\phi/2}\sqrt{\sin\theta}
\end{align}$$
Now try to construct $Y_{1/2}^{-1/2}$, by applying $L_-$ to $Y_{1/2}^{1/2}(\theta,\phi)$ and by using $L_-Y_{-1/2}^{1/2}(\theta,\phi)=0$.

Show that these two procedures lead to contradictory results.
### Using lowering operator
We need to first express the $L_-$ operator in spherical coordinates:
$$\begin{align}
L_-&=\hbar e^{-i\phi}\left(-\dfrac{\partial}{\partial\theta}+i\dfrac{\cos\theta}{\sin\theta}\dfrac{\partial}{\partial\phi}\right)
\end{align}$$
Substituting what we have for $Y_{1/2}^{1/2}(\theta,\phi)$, then:
$$\begin{align}
L_-Y_{1/2}^{1/2}(\theta,\phi)&=\hbar e^{-i\phi}\left(-\dfrac{\partial}{\partial\theta}+i\dfrac{\cos\theta}{\sin\theta}\dfrac{\partial}{\partial\phi}\right)e^{i\phi/2}\sqrt{\sin\theta}\\
&=\hbar e^{-i\phi}\left[-\dfrac{\partial}{\partial\theta}\left(e^{i\phi/2}\sqrt{\sin\theta}\right)+i\dfrac{\cos\theta}{\sin\theta}\dfrac{\partial}{\partial\phi}\left(e^{i\phi/2}\sqrt{\sin\theta}\right)\right]\\
&=\hbar e^{-i\phi}\left[-\left(e^{i\phi/2}\dfrac{\cos\theta}{2\sqrt{\sin\theta}}\right)+i\dfrac{\cos\theta}{\sin\theta}\left(\dfrac{i}{2}e^{i\phi/2}\sqrt{\sin\theta}\right)\right]\\
&=-\hbar e^{-i\phi}e^{i\phi/2}\dfrac{\cos\theta}{2\sqrt{\sin\theta}}\left[1+1\right]\\
\Aboxed{Y_{1/2}^{-1/2}(\theta,\phi)&=-\hbar e^{-i\phi/2}\dfrac{\cos\theta}{\sqrt{\sin\theta}}}
\end{align}$$
### Using the $=0$ condition
$$\begin{align}
L_-Y_{1/2}^{-1/2}(\theta,\phi)&=0\\
\hbar e^{-i\phi}\left(-\dfrac{\partial}{\partial\theta}+i\dfrac{\cos\theta}{\sin\theta}\dfrac{\partial}{\partial\phi}\right)Y_{1/2}^{-1/2}(\theta,\phi)&=0\\
\left(-\dfrac{\partial}{\partial\theta}+i\cot\theta\dfrac{\partial}{\partial\phi}\right)Y_{1/2}^{-1/2}(\theta,\phi)&=0
\end{align}$$
This is just a PDE that can be solved simply from a separation of variables.
Since I already somewhat know the form, let $Y_{1/2}^{-1/2}(\theta,\phi)=e^{-i\phi/2}\Theta(\theta)$
$$\begin{align}
\left(-\dfrac{\partial}{\partial\theta}+i\cot\theta\dfrac{\partial}{\partial\phi}\right)Y_{1/2}^{-1/2}(\theta,\phi)&=0\\
\left(-\dfrac{\partial}{\partial\theta}+i\cot\theta\dfrac{\partial}{\partial\phi}\right)e^{-i\phi/2}\Theta(\theta)&=0\\
\left(-\dfrac{\partial\Theta(\theta)}{\partial\theta}+\left(-\tfrac{i}{2}\right)i\cot\theta\ \Theta(\theta)\right)e^{-i\phi/2}&=0\\
-\dfrac{\partial\Theta(\theta)}{\partial\theta}+\dfrac{1}{2}\cot\theta\ \Theta(\theta)&=0
\end{align}$$
We can then solve this ODE normally:
$$\begin{align}
\dfrac{\partial\Theta(\theta)}{\partial\theta}&=\dfrac{1}{2}\cot\theta\ \Theta(\theta)\\
\int\dfrac{1}{\Theta(\theta)}\dfrac{\partial\Theta(\theta)}{\partial\theta}\ d\theta&=\int\dfrac{1}{2}\cot\theta\ d\theta\\
\ln|\Theta(\theta)|&=\dfrac{1}{2}\ln(\sin\theta)+C\\
\ln|\Theta(\theta)|&=\ln(\sqrt{\sin\theta})+C\\
\Theta(\theta)&\propto\sqrt{\sin\theta}\\
\end{align}$$
Therefore, we find that this function is of the form:
$$\begin{align}
\Aboxed{Y_{1/2}^{-1/2}(\theta,\phi)&\propto e^{-i\phi/2}\sqrt{\sin\theta}}
\end{align}$$
From here, it's very clear to see that these two do *not* produce the same function:
$$\begin{align}
\text{Part A}:&&Y_{1/2}^{-1/2}(\theta,\phi)&\propto e^{-i\phi/2}\dfrac{\cos\theta}{\sqrt{\sin\theta}}\\
\text{Part B}:&&Y_{1/2}^{-1/2}(\theta,\phi)&\propto e^{-i\phi/2}\sqrt{\sin\theta}\\
\end{align}$$
---
## Question 3.29
The goal of this problem is to determine degenerate eigenstates of the three-dimensional isotropic harmonic oscillator written as eigenstates of $\vec{L}^2$ and $L_z$, in terms of the Cartesian eigenstates $\ket{n_x,n_y,n_z}$.
### Question 3.29.A
Show that the angular-momentum operators are given by:
$$\begin{align}
L_i&=i\hbar\epsilon_{ijk}a_ja_k^\dagger\\
\vec{L}^2&=\hbar^2\left[N(N+1)-a_k^\dagger a_k^\dagger a_ja_j\right]
\end{align}$$
where summation is implied over repeated indices, $\epsilon_{ijk}$ is the totally antisymmetric symbol, and $N\equiv a_j^\dagger a_j$ counts the total number of quanta.

From the definitions of linear momentum and angular momentum, we know that:
$$\begin{align}
L_i&=\epsilon_{ijk}x_jp_k
\end{align}$$
This comes from the cross product definition as used in the previous question.

The 3 directions are cartesian, so they all have the same form for creation and annihilation:
$$\begin{align}
a_j&=\sqrt{\dfrac{m\omega}{2\hbar}}x_j+i\dfrac{1}{\sqrt{2m\hbar\omega}}p_j & a_j^\dagger&=\sqrt{\dfrac{m\omega}{2\hbar}}x_j-i\dfrac{1}{\sqrt{2m\hbar\omega}}p_j
\end{align}$$
Rearranging we find that:
$$\begin{align}
a_j+a_j^\dagger&=2\sqrt{\dfrac{m\omega}{2\hbar}}x_j & a_j-a_j^\dagger&=2i\dfrac{1}{\sqrt{2m\hbar\omega}}p_j\\
x_j&=\sqrt{\dfrac{\hbar}{2m\omega}}\left(a_j+a_j^\dagger\right) & p_j&=-i\sqrt{\dfrac{m\hbar\omega}{2}}\left(a_j-a_j^\dagger\right)\\
\end{align}$$
Substitute these definitions in for the angular momentum, then:
$$\begin{align}
L_i&=\epsilon_{ijk}x_jp_k\\
&=-i\epsilon_{ijk}\sqrt{\dfrac{\hbar}{2m\omega}}\sqrt{\dfrac{m\hbar\omega}{2}}\left(a_j+a_j^\dagger\right)\left(a_k-a_k^\dagger\right)\\
&=-i\dfrac{\hbar}{2}\epsilon_{ijk}\left(a_j+a_j^\dagger\right)\left(a_k-a_k^\dagger\right)\\
&=-i\dfrac{\hbar}{2}\epsilon_{ijk}\left(a_ja_k-a_ja_k^\dagger+a_j^\dagger a_k-a_j^\dagger a_k^\dagger\right)\\
&=-i\dfrac{\hbar}{2}\epsilon_{ijk}\left(a_ja_k-a_j^\dagger a_k^\dagger\right)-i\dfrac{\hbar}{2}\epsilon_{ijk}\left(a_j^\dagger a_k-a_ja_k^\dagger\right)\\
&=0-i\dfrac{\hbar}{2}\epsilon_{ijk}[a_j^\dagger,a_k]+i\dfrac{\hbar}{2}\epsilon_{ijk}\left\{a_j,a_k^\dagger\right\}\\
&=0+i\dfrac{\hbar}{2}\epsilon_{ijk}\cdot 2a_j a_k^\dagger\\
\Aboxed{L_i&=i\hbar\epsilon_{ijk}a_j a_k^\dagger}
\end{align}$$
The $\vec{L}^2$ term is pretty simply found using the dot product:
$$\begin{align}
L_i^2&=\left(i\hbar\epsilon_{ijk}a_j a_k^\dagger\right)\left(i\hbar\epsilon_{ij'k'}a_{j'} a_{k'}^\dagger\right)\\
&=-\hbar^2\epsilon_{ijk}\epsilon_{ij'k'}a_j a_k^\dagger a_{j'} a_{k'}^\dagger\\
&=-\hbar^2\left(\delta_{j,j'}\delta_{k,k'}-\delta_{j,k'}\delta_{k,j'}\right)a_j a_k^\dagger a_{j'} a_{k'}^\dagger\\
&=\hbar^2\left(\delta_{j,k'}\delta_{k,j'}a_j a_k^\dagger a_{j'} a_{k'}^\dagger-\delta_{j,j'}\delta_{k,k'}a_j a_k^\dagger a_{j'} a_{k'}^\dagger\right)\\
&=\hbar^2\left(a_j a_k^\dagger a_{k} a_{j}^\dagger-a_j a_k^\dagger a_{j} a_{k}^\dagger\right)\\
&=\hbar^2\left(a_jNa_{j}^\dagger-a_k^\dagger a_{k}^\dagger a_ja_{j}\right)\\
&=\hbar^2\left(N(a_{j}^\dagger a_j+1)-a_k^\dagger a_{k}^\dagger a_ja_{j}\right)\\
\Aboxed{\vec{L}^2&=\hbar^2\left(N(N+1)-a_k^\dagger a_{k}^\dagger a_ja_{j}\right)}
\end{align}$$
---
### Question 3.29.B
Use these relations to express the states $\ket{qlm}=\ket{01m}$, $m=0,\pm1$, in terms of the three eigenstates $\ket{n_x,n_y,n_z}$ that are degenerate in energy. Write down the representation of your answer in coordinate space, and check that the angular and radial dependences are correct.

### Question 3.29.C
Repeat for $\ket{qlm}=\ket{100}$.

### Question 3.29.D
Repeat for $\ket{qlm}=\ket{02m}$, with $m=0,1,$ and $2$.




---
## Question 3.34
Find all nine states $\ket{j,m}$ for $j=2,1,$ and $0$ formed by adding $j_1=1$ and $j_2=1$. Use a simplified notation, where $\ket{j,m}$ is explicit and $\pm,0$ stand for $m_{1,2}=\pm1,0$, respectively, for example:
$$\begin{align}
\ket{1,1}=\dfrac{1}{\sqrt{2}}\ket{+,0}-\dfrac{1}{\sqrt{2}}\ket{0,+}
\end{align}$$
You may also want to make use of the ladder operators $J_\pm$, or recursion relations, as well as orthonormality. Check your answers by finding a table of Clebsch–Gordan coefficients for comparison; see Appendix E.

The 9 different states we can construct are as follows:
$$\begin{align}
&\ket{j=0,m=0}  & &\ket{j=2,m=+2}\\
&               & &\ket{j=2,m=+1}\\
&\ket{j=1,m=+1} & &\ket{j=2,m=\ \ \ 0}\\
&\ket{j=1,m=\ \ \ 0} & &\ket{j=2,m=-1}\\
&\ket{j=1,m=-1} & &\ket{j=2,m=-2}\\
\end{align}$$
However, it wants it in a reduced form, so we can then write it as $\ket{m_1,m_2}$.

We start with the highest state (since it will be unique):
$$\begin{align}
\Aboxed{\ket{2,2}&=\ket{+,+}}
\end{align}$$
Then the following chains of operators:
$$\begin{align}
&&J_-\ket{2,2}&=J_-\ket{+,+}\\
\implies&&\ket{2,1}&\propto\sqrt{2}\ket{0,+}+\sqrt{2}\ket{+,0}\\
\implies&&\Aboxed{\ket{2,1}&=\dfrac{1}{\sqrt{2}}\ket{0,+}+\dfrac{1}{\sqrt{2}}\ket{+,0}}
\end{align}$$
$$\begin{align}
&&J_-\ket{2,1}&=\dfrac{1}{\sqrt{2}}J_-\ket{0,+}+\dfrac{1}{\sqrt{2}}J_-\ket{+,0}\\
\implies&&\ket{2,0}&\propto \sqrt{2}\ket{-,+}+\sqrt{2}\ket{0,0}+\sqrt{2}\ket{0,0}+\sqrt{2}\ket{+,-}\\
&&&\propto 1\ket{-,+}+2\ket{0,0}+1\ket{+,-}\\
\implies&&\Aboxed{\ket{2,0}&=\dfrac{1}{\sqrt{6}}\ket{-,+}+\dfrac{2}{\sqrt{6}}\ket{0,0}+\dfrac{1}{\sqrt{6}}\ket{+,-}}
\end{align}$$
$$\begin{align}
&&J_-\ket{2,0}&=\dfrac{1}{\sqrt{6}}J_-\ket{-,+}+\dfrac{2}{\sqrt{6}}J_-\ket{0,0}+\dfrac{1}{\sqrt{6}}J_-\ket{+,-}\\
\implies&&\ket{2,-1}&\propto 0+1\ket{-,0}+2\ket{-,0}+2\ket{0,-}+1J_-\ket{0,-}+0\\
&&&\propto 3\ket{-,0}+3\ket{0,-}\\
\implies&&\Aboxed{\ket{2,-1}&=\dfrac{1}{\sqrt{2}}\ket{0,-}+\dfrac{1}{\sqrt{2}}\ket{-,0}}
\end{align}$$
$$\begin{align}
&&J_-\ket{2,-1}&=\dfrac{1}{\sqrt{2}}J_-\ket{0,-}+\dfrac{1}{\sqrt{2}}J_-\ket{-,0}\\
\implies&&\ket{2,-2}&\propto 1\ket{-,-}+0+0+1\ket{-,-}\\
\implies&&\Aboxed{\ket{2,-2}&=\ket{-,-}}
\end{align}$$
For the case where $m=+1$, we have 2 different $j$ that satisfy, but must be orthogonal:
$$\begin{align}
\ket{2,1}&=\dfrac{1}{\sqrt{2}}\ket{0,+}+\dfrac{1}{\sqrt{2}}\ket{+,0}\\
\ket{1,1}&=A\ket{0,+}+B\ket{+,0}\\
\braket{2,1|1,1}&=\dfrac{1}{\sqrt{2}}A+\dfrac{1}{\sqrt{2}}B\\
0&=\dfrac{1}{\sqrt{2}}A+\dfrac{1}{\sqrt{2}}B\\
B&=-A\\
\Aboxed{\ket{1,1}&=\dfrac{1}{\sqrt{2}}\ket{0,+}-\dfrac{1}{\sqrt{2}}\ket{+,0}}
\end{align}$$
Similarly we have the same thing for $m=-1$, and so:
$$\begin{align}
\ket{2,1}&=\dfrac{1}{\sqrt{2}}\ket{0,-}+\dfrac{1}{\sqrt{2}}\ket{-,0}\\
\ket{1,1}&=A\ket{0,-}+B\ket{-,0}\\
\braket{2,1|1,1}&=\dfrac{1}{\sqrt{2}}A+\dfrac{1}{\sqrt{2}}B\\
0&=\dfrac{1}{\sqrt{2}}A+\dfrac{1}{\sqrt{2}}B\\
B&=-A\\
\Aboxed{\ket{1,-1}&=\dfrac{1}{\sqrt{2}}\ket{0,-}-\dfrac{1}{\sqrt{2}}\ket{-,0}}
\end{align}$$
Lastly, we have 3 different $j$ that exist for the case of $m=0$. A choice for the $\ket{1,1}$ that makes it super easy to solve the rest is when we say:
$$\begin{align}
\ket{2,0}&=\dfrac{1}{\sqrt{6}}\ket{-,+}+\dfrac{2}{\sqrt{6}}\ket{0,0}+\dfrac{1}{\sqrt{6}}\ket{+,-}\\
\Aboxed{\ket{1,0}&=\dfrac{1}{\sqrt{2}}\ket{-,+}+0\ket{0,0}-\dfrac{1}{\sqrt{2}}\ket{+,-}}\\
\braket{2,0|1,0}&=\dfrac{1}{\sqrt{6}}\dfrac{1}{\sqrt{2}}+\dfrac{2}{\sqrt{6}}\cdot0-\dfrac{1}{\sqrt{6}}\dfrac{1}{\sqrt{2}}=0
\end{align}$$
From there, we do similar to the $m=\pm1$ case since it's a simple matter of algebra:
$$\begin{align}
\ket{2,0}&=\dfrac{1}{\sqrt{6}}\ket{-,+}+\dfrac{2}{\sqrt{6}}\ket{0,0}+\dfrac{1}{\sqrt{6}}\ket{+,-}\\
\ket{1,0}&=\dfrac{1}{\sqrt{2}}\ket{-,+}+0\ket{0,0}-\dfrac{1}{\sqrt{2}}\ket{+,-}\\
\ket{0,0}&=A\ket{-,+}+B\ket{0,0}+C\ket{+,-}\\\\

\braket{2,0|0,0}&=\dfrac{1}{\sqrt{6}}A+\dfrac{2}{\sqrt{6}}B+\dfrac{1}{\sqrt{6}}C\\
0&=\dfrac{2}{\sqrt{6}}A+\dfrac{2}{\sqrt{6}}B\\
B&=-A\\
\braket{1,0|0,0}&=\dfrac{1}{\sqrt{2}}A-\dfrac{1}{\sqrt{2}}C\\
0&=A-C\\
C&=A\\\\
\Aboxed{\ket{0,0}&=\dfrac{1}{\sqrt{3}}\ket{-,+}-\dfrac{1}{\sqrt{3}}\ket{0,0}+\dfrac{1}{\sqrt{3}}\ket{+,-}}
\end{align}$$
All 9 of these match the Clebsch-Gordan coefficients!

---
## Question 3.35
A spin $1/2$ particle is in an orbital angular momentum $l=1$ state.
### Question 3.35.A
Starting with the total angular momentum state $\ket{j,m}=\ket{j,j}$ for $j=3/2$, use the operator $\vec{J}=\vec{L}+\vec{S}$ to construct all the states $\ket{j,m_j}$ in terms of the eigenstates $\ket{l,m_l}$ for $\vec{L}^2$ and $L_z$, and the eigenstates $\ket{1/2,\pm1/2}$ for $\vec{S}^2$ and $S_z$. Check your answers by finding a table of Clebsch–Gordan coefficients for comparison; see Appendix E.

Similar to previous, we can start from the maximum state (unique) and work down:
$$\begin{align}
\ket{j=\tfrac{3}{2},m=\tfrac{3}{2}}&=\ket{l=1,m_l=1}\ket{s=\tfrac{1}{2},m_s=\tfrac{1}{2}}\\
\Aboxed{\ket{\tfrac{3}{2},\tfrac{3}{2}}&=\ket{1,+}\ket{\tfrac{1}{2},+}}
\end{align}$$
A single $J_-=L_-+S_-$ lowering operator then becomes:
$$\begin{align}
J_-\ket{\tfrac{3}{2},\tfrac{3}{2}}&=(L_-+S_-)\ket{1,+}\ket{\tfrac{1}{2},+}\\
&=L_-\ket{1,+}\ket{\tfrac{1}{2},+}+S_-\ket{1,+}\ket{\tfrac{1}{2},+}\\
\hbar\sqrt{3}\ket{\tfrac{3}{2},\tfrac{1}{2}}&=\hbar\sqrt{2}\ket{1,0}\ket{\tfrac{1}{2},+}+\hbar\ket{1,+}\ket{\tfrac{1}{2},-}\\
\Aboxed{\ket{\tfrac{3}{2},\tfrac{1}{2}}&=\sqrt{\dfrac{2}{3}}\ket{1,0}\ket{\tfrac{1}{2},+}+\sqrt{\dfrac{1}{3}}\ket{1,+}\ket{\tfrac{1}{2},-}}
\end{align}$$
Another lowering operator:
$$\begin{align}
J_-\ket{\tfrac{3}{2},\tfrac{1}{2}}&=\sqrt{\dfrac{2}{3}}(L_-+S_-)\ket{1,0}\ket{\tfrac{1}{2},+}+\sqrt{\dfrac{1}{3}}(L_-+S_-)\ket{1,+}\ket{\tfrac{1}{2},-}\\\\
&=\sqrt{\dfrac{2}{3}}L_-\ket{1,0}\ket{\tfrac{1}{2},+}+\sqrt{\dfrac{2}{3}}S_-\ket{1,0}\ket{\tfrac{1}{2},+}\\
&+\sqrt{\dfrac{1}{3}}L_-\ket{1,+}\ket{\tfrac{1}{2},-}+\sqrt{\dfrac{1}{3}}S_-\ket{1,+}\ket{\tfrac{1}{2},-}\\\\
&=\sqrt{\dfrac{2}{3}}\hbar\sqrt{2}\ket{1,-1}\ket{\tfrac{1}{2},+}+\sqrt{\dfrac{2}{3}}\hbar \ket{1,0}\ket{\tfrac{1}{2},-}\\
&+\sqrt{\dfrac{1}{3}}\hbar\sqrt{2}\ket{1,0}\ket{\tfrac{1}{2},-}+\sqrt{\dfrac{1}{3}}\cdot0\hbar \ket{1,+}\ket{\tfrac{1}{2},-}\\\\
2\hbar\ket{\tfrac{3}{2},-\tfrac{1}{2}}&=\sqrt{\dfrac{4}{3}}\hbar\ket{1,-1}\ket{\tfrac{1}{2},+}+\sqrt{\dfrac{8}{3}}\hbar \ket{1,0}\ket{\tfrac{1}{2},-}\\
\Aboxed{\ket{\tfrac{3}{2},-\tfrac{1}{2}}&=\sqrt{\dfrac{1}{3}}\ket{1,-1}\ket{\tfrac{1}{2},+}+\sqrt{\dfrac{2}{3}}\ket{1,0}\ket{\tfrac{1}{2},-}}
\end{align}$$
I could do 1 more lowering operator, but we'll see that they'll become the same state, and thus:
$$\begin{align}
\Aboxed{\ket{\tfrac{3}{2},-\tfrac{3}{2}}&=\ket{1,-1}\ket{\tfrac{1}{2},-}}
\end{align}$$
Once again, these match those found in the Clebsch-Gordon tables.

---
### Question 3.35.B
If the particle is in a total angular-momentum eigenstate with $z$-component $\hbar/2$, calculate the probability of finding the $z$-component of the spin of the particle to have the value $m_s = +1/2$.

Start with the eigenstate for angular momentum in our case:
$$\begin{align}
\ket{\tfrac{3}{2},\tfrac{1}{2}}&=\sqrt{\dfrac{2}{3}}\ket{1,0}\ket{\tfrac{1}{2},+}+\sqrt{\dfrac{1}{3}}\ket{1,+}\ket{\tfrac{1}{2},-}
\end{align}$$
We want to find the probability of the state $\ket{1,0}\ket{\tfrac{1}{2},+}$, and so:
$$\begin{align}
\braket{1,0;\tfrac{1}{2},+|\tfrac{3}{2},\tfrac{1}{2}}
&=\sqrt{\dfrac{2}{3}}\bra{\tfrac{1}{2},+}\braket{1,0|1,0}\ket{\tfrac{1}{2},+}+\sqrt{\dfrac{1}{3}}\bra{\tfrac{1}{2},+}\braket{1,0|1,+}\ket{\tfrac{1}{2},-}\\
&=\sqrt{\dfrac{2}{3}}\bra{\tfrac{1}{2},+}\cdot1\cdot\ket{\tfrac{1}{2},+}+\sqrt{\dfrac{1}{3}}\bra{\tfrac{1}{2},+}\cdot0\cdot\ket{\tfrac{1}{2},-}\\
&=\sqrt{\dfrac{2}{3}}\braket{\tfrac{1}{2},+|\tfrac{1}{2},+}+0\\
\braket{1,0;\tfrac{1}{2},+|\tfrac{3}{2},\tfrac{1}{2}}&=\sqrt{\dfrac{2}{3}}\\
\left|\braket{1,0;\tfrac{1}{2},+|\tfrac{3}{2},\tfrac{1}{2}}\right|^2&=\left(\sqrt{\dfrac{2}{3}}\right)^2\\
\Aboxed{p\left(m_s=+\tfrac{1}{2}|\psi=\ket{\tfrac{3}{2},\tfrac{1}{2}}\right)&=\dfrac{2}{3}}
\end{align}$$

