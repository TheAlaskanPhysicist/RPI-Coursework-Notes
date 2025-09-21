Author: Stanley Goodwin
Date: September 21st, 2025

---
### Question 1.12
The Hamiltonian operator for a two-state system is given by:
$$\begin{align}
H&=a\left(\ket1\bra1-\ket2\bra2+\ket1\bra2+\ket2\bra1\right)
\end{align}$$
where $a$ is a number with the dimension of energy. Find the energy eigenvalues and the corresponding energy eigenstates (as linear combinations of $|1〉$ and $|2〉$).

We can write this in matrix form using $\ket1=\begin{bmatrix}1\\0\end{bmatrix}$ and $\ket2=\begin{bmatrix}0\\1\end{bmatrix}$ as:
$$\begin{align}
H&=a\begin{bmatrix}1&1\\1&-1\end{bmatrix}
\end{align}$$
The eigenvalues are found by finding $\lambda$ such that:
$$\begin{align}
\det\left(H-\lambda\mathbb{I}\right)&=0\\
\det\left(a\begin{bmatrix}1&1\\1&-1\end{bmatrix}-\lambda\mathbb{I}\right)&=0\\
\det\left(\begin{bmatrix}a-\lambda&a\\a&-a-\lambda\end{bmatrix}\right)&=0\\
(a-\lambda)(-a-\lambda)-a^2&=0\\
(\lambda-a)(\lambda+a)-a^2&=0\\
\lambda^2-a^2-a^2&=0\\
\lambda^2&=2a^2\\
\Aboxed{\lambda&=\pm a\sqrt2}
\end{align}$$
To find the eigenstates, we can substitute these values of $\lambda$ back in:
$$\begin{align}
a\begin{bmatrix}1&1\\1&-1\end{bmatrix}\vec\lambda_{+1}&=+a\sqrt2\vec\lambda_{+1}\\
\begin{bmatrix}1&1\\1&-1\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}&=\sqrt2\begin{bmatrix}x\\y\end{bmatrix}
\end{align}$$
$$\begin{align}
x+y&=\sqrt2 x & x-y&=\sqrt2 y\\
y&=(\sqrt2-1) x & x&=(\sqrt2+1) y\\
\end{align}$$
$$\begin{align}
\Aboxed{\vec\lambda_{+1}&=\dfrac{1}{\sqrt{2(1+\sqrt2)}}\begin{bmatrix}1+\sqrt2\\1\end{bmatrix}}
\end{align}$$
The other vector:
$$\begin{align}
a\begin{bmatrix}1&1\\1&-1\end{bmatrix}\vec\lambda_{-1}&=-a\sqrt2\vec\lambda_{-1}\\
\begin{bmatrix}1&1\\1&-1\end{bmatrix}\begin{bmatrix}x\\y\end{bmatrix}&=-\sqrt2\begin{bmatrix}x\\y\end{bmatrix}
\end{align}$$
$$\begin{align}
x+y&=-\sqrt2 x & x-y&=-\sqrt2 y\\
y&=(\sqrt2+1) x & x&=(1-\sqrt2) y\\
\end{align}$$
$$\begin{align}
\Aboxed{\vec\lambda_{-1}&=\dfrac{1}{\sqrt{2(1+\sqrt2)}}\begin{bmatrix}1\\1+\sqrt2\end{bmatrix}}\\
\text{or}&\text{ alternatively:}\\
\Aboxed{\vec\lambda_{-1}&=\dfrac{1}{\sqrt{2(2-\sqrt2)}}\begin{bmatrix}1-\sqrt2\\1\end{bmatrix}}
\end{align}$$
All together, we have the 2 eigenstate and value pairs:
$$\begin{align}
\lambda&=+a\sqrt2 & \vec\lambda_{+1}&=\dfrac{1}{\sqrt{2(1+\sqrt2)}}\begin{bmatrix}1+\sqrt2\\1\end{bmatrix}\\
\lambda&=-a\sqrt2 & \vec\lambda_{-1}&=\dfrac{1}{\sqrt{2(1+\sqrt2)}}\begin{bmatrix}1\\1+\sqrt2\end{bmatrix}\\
\end{align}$$
---
### Question 1.15
A beam of spin $1/2$ atoms goes through a series of Stern-Gerlach type measurements as follows.
1) The first measurement accepts $s_z=+\tfrac{1}{2}\hbar$ and rejects $s_z=-\tfrac{1}{2}\hbar$ atoms.
2) The first measurement accepts $s_n=+\tfrac{1}{2}\hbar$ and rejects $s_n=-\tfrac{1}{2}\hbar$ atoms.
3) The first measurement accepts $s_z=-\tfrac{1}{2}\hbar$ and rejects $s_z=+\tfrac{1}{2}\hbar$ atoms.
Where $s_n$ is a spin measurement that lies in the $xz$-plane at angle $\beta$ from the $+z$ axis.

---
#### Question 1.15.A
We can represent these measurements as a chain of projections:
**Note:** I'm using $\chi$ for spinor states, since this is what I learned in undergraduate (Griffith's).
$$\begin{align}
\ket{\psi_f}&=\mathbb{I}\cdot\mathbb{I}\cdot\mathbb{I}\cdot\ket{\psi_0}\\
&=\ket{\chi^Z_-}\bra{\chi^Z_-}\cdot\ket{\chi^n_+}\bra{\chi^n_+}\cdot\ket{\chi^Z_+}\bra{\chi^Z_+}\cdot\ket{\psi_0}\\
\Aboxed{\ket{\psi_f}&=\ket{\chi^Z_-}\braket{\chi^Z_-|\chi^n_+}\braket{\chi^n_+|\chi^Z_+}\braket{\chi^Z_+|\psi_0}}
\end{align}$$
For a generalized spinor in the $xz$-plane, we can write its basis states as:
$$\begin{align}
\ket{+n}&=\cos\left(\frac{\beta}{2}\right)\ket{\chi^Z_+}+\sin\left(\frac{\beta}{2}\right)\ket{\chi^Z_-}
\end{align}$$
There is no azimuthal phase since it's in the $xz$ plane, where the $y$ component is 0.
The first measurement is the initial condition of the system so $\braket{\chi^Z_+|\psi_0}=1$:
$$\begin{align}
\ket{\psi_f}&=\ket{\chi^Z_-}\braket{\chi^Z_-|\chi^n_+}\braket{\chi^n_+|\chi^Z_+}\braket{\chi^Z_+|\psi_0}\\
\braket{\chi^Z_-|\psi_f}&=\sin\left(\frac{\beta}{2}\right)\cdot\cos\left(\frac{\beta}{2}\right)\cdot1\\
\braket{\chi^Z_-|\psi_f}&=\dfrac{1}{2}\sin\beta\\
\end{align}$$
Assuming the initial intensity $I_0$, then the ration of output intensity to input intensity is:
$$\begin{align}
\dfrac{I}{I_0}&=\left|\braket{\chi^Z_-|\psi_f}\right|^2\\
&=\left|\dfrac{1}{2}\sin\beta\right|^2\\
\Aboxed{\dfrac{I}{I_0}&=\dfrac{1}{4}\sin^2\beta}
\end{align}$$
---
#### Question 1.15.B
Over the range of angles $\beta\in[0,2\pi)$, we can find its maxima using its derivatives:
$$\begin{align}
\dfrac{d}{d\theta}\left(\dfrac{1}{4}\sin^2\beta\right)&=\dfrac{1}{4}\cdot2\sin\beta\cdot\cos\beta\\
0&=\dfrac{1}{4}\cdot\sin2\beta\\
0&=\sin2\beta\\
\beta&=\dfrac{1}{2}\sin^{-1}(0)\\
\beta&\in\left\{0,\tfrac{\pi}{2},\pi,\tfrac{3\pi}{2}\right\}
\end{align}$$
To know which are maxima, lets look at the 2nd derivative:
$$\begin{align}
\dfrac{d^2}{d\theta^2}\left(\dfrac{1}{4}\sin^2\beta\right)
&=\dfrac{1}{4}\cdot\dfrac{d}{d\theta}\left(\sin2\beta\right)\\
&=\dfrac{1}{4}\cdot\cos2\beta\cdot2\\
&=\dfrac{1}{2}\cdot\cos2\beta\\
\Aboxed{\text{sign}&=\cos2\beta}
\end{align}$$
For the 4 different values:
$$\begin{align}
\beta&=0 & \cos2\cdot0&=+1>0 & \text{Minimum}\\
\beta&=\tfrac{\pi}{2} & \cos2\cdot\tfrac{\pi}{2}&=-1<0 & \text{Maximum}\\
\beta&=\pi & \cos2\cdot\pi&=+1>0 & \text{Minimum}\\
\beta&=\tfrac{3\pi}{2} & \cos2\cdot\tfrac{3\pi}{2}&=-1<0 & \text{Maximum}\\
\end{align}$$
Intensity is maximized at $\beta\in\left\{\tfrac{\pi}{2},\tfrac{3\pi}{2}=-\tfrac{\pi}{2}\right\}$, and so in total:
$$\begin{align}
\beta&=+\dfrac{\pi}{2} & \dfrac{I}{I_0}&=\dfrac{1}{4}=25\%\\
\beta&=-\dfrac{\pi}{2} & \dfrac{I}{I_0}&=\dfrac{1}{4}=25\%
\end{align}$$
---
### Question 1.30
#### Question 1.30.A
Let $x$ and $p_x$ be the coordinate and linear momentum in one dimension.
Evaluate the classical Poisson bracket $[x,F(p_x)]_\text{classical}$.
$$\begin{align}
[x,F(p_x)]_\text{Poisson}&=\dfrac{\partial x}{\partial x}\dfrac{\partial F(p_x)}{\partial p_x}-\dfrac{\partial x}{\partial p_x}\dfrac{\partial F(p_x)}{\partial x}\\
&=1\cdot\dfrac{\partial F(p_x)}{\partial p_x}-0\cdot0\\
\Aboxed{[x,F(p_x)]_\text{Poisson}&=\dfrac{\partial F(p_x)}{\partial p_x}}
\end{align}$$
---
#### Question 1.30.B
Let $x$ and $p_x$ be the corresponding quantum-mechanical operators this time.
Evaluate the commutator:
$$\begin{align}
\left[x,e^{\tfrac{ip_xa}{\hbar}}\right]&=x\sum_{n\ge0}\dfrac{\left(\tfrac{ip_xa}{\hbar}\right)^n}{n!}-\sum_{n\ge0}\dfrac{\left(\tfrac{ip_xa}{\hbar}\right)^n}{n!}x\\
&=\sum_{n\ge0}\dfrac{\left(\tfrac{ia}{\hbar}\right)^n}{n!}\left(xp_x^n-p_x^nx\right)\\
&=\sum_{n\ge0}\dfrac{1}{n!}\left(\dfrac{ia}{\hbar}\right)^n\left[x,p_x^n\right]\\
&=\dfrac{1}{0!}\left(\dfrac{ia}{\hbar}\right)^0\left[x,\mathbb{I}\right]+\sum_{n\ge1}\dfrac{1}{n!}\left(\dfrac{ia}{\hbar}\right)^n\left[x,p_x^n\right]\\
\left[x,e^{\tfrac{ip_xa}{\hbar}}\right]&=\sum_{n\ge1}\dfrac{1}{n!}\left(\dfrac{ia}{\hbar}\right)^n\left[x,p_x^n\right]\\
\end{align}$$
We need to evaluate the commutator at different powers of $p_x$:
$$\begin{align}
\left[x,p_x^n\right]&=\sum_{k=0}^{n-1}p_x^k[x,p_x]p_x^{n-1-k}\\
&=i\hbar\sum_{k=0}^{n-1}p_x^kp_x^{n-1-k}\\
&=i\hbar\sum_{k=0}^{n-1}p_x^{n-1}\\
&=i\hbar([n-1]-[0]+1)p_x^{n-1}\\
\left[x,p_x^n\right]&=i\hbar\cdot np_x^{n-1}\\
\end{align}$$
Substituting, we find that:
$$\begin{align}
\left[x,e^{\tfrac{ip_xa}{\hbar}}\right]&=\sum_{n\ge1}\dfrac{1}{n!}\left(\dfrac{ia}{\hbar}\right)^n\left[x,p_x^n\right]\\
&=\sum_{n\ge1}\dfrac{1}{n!}\left(\dfrac{ia}{\hbar}\right)^ni\hbar\cdot np_x^{n-1}\\
&=i\hbar\cdot \dfrac{ia}{\hbar}\sum_{n\ge1}\dfrac{1}{(n-1)!}\left(\dfrac{ip_xa}{\hbar}\right)^{n-1}\\
&=-a\sum_{m\ge1}\dfrac{1}{m!}\left(\dfrac{ip_xa}{\hbar}\right)^{m}\\
\Aboxed{\left[x,e^{\tfrac{ip_xa}{\hbar}}\right]&=-ae^{\tfrac{ip_xa}{\hbar}}}
\end{align}$$
---
#### Question 1.30.C
Use that result to show the exponential is an eigenstate of coordinate operator $x$:
$$\begin{align}
\left[x,e^{\tfrac{ip_xa}{\hbar}}\right]&=-ae^{\tfrac{ip_xa}{\hbar}}\\
xe^{\tfrac{ip_xa}{\hbar}}&=-ae^{\tfrac{ip_xa}{\hbar}}+e^{\tfrac{ip_xa}{\hbar}}x\\
xe^{\tfrac{ip_xa}{\hbar}}&=e^{\tfrac{ip_xa}{\hbar}}(x-a)\\
xe^{\tfrac{ip_xa}{\hbar}}\ket{x'}&=e^{\tfrac{ip_xa}{\hbar}}(x-a)\ket{x'}\\
x\left(e^{\tfrac{ip_xa}{\hbar}}\ket{x'}\right)&=(x'-a)\left(e^{\tfrac{ip_xa}{\hbar}}\ket{x'}\right)\\
\end{align}$$
The operator $x$ on state $\ket{x'}$ has the eigenvalue of $\boxed{x'-a}$.

---
### Question 1.31
#### Question 1.31.A
On p. 247, Gottfried (1966) states that:
$$\begin{aligned}[]
[x_i,G(\vec{p})]&=i\hbar\dfrac{\partial G}{\partial p_i} & [p_i,F(\vec{x})]&=-i\hbar\dfrac{\partial F}{\partial x_i}
\end{aligned}$$
can be "easily derived" from the fundamental commutation relations for all functions of $F$ and $G$ that can be expressed as power series in their arguments. Verify this statement.

For analytic functions $F$ and $G$, we can express them as a power series as:
$$\begin{align}
F(\vec{x})&=\sum_{n=0}^\infty f_{n}\cdot(\vec{x})^n & G(\vec{p})&=\sum_{n=0}^\infty g_{n}\cdot(\vec{p})^n
\end{align}$$
Writing the first commutator:
$$\begin{aligned}[]
[x_i,G(\vec{p})]
&=x_i\sum_{n=0}^\infty g_{n}\cdot(\vec{p})^n-\sum_{n=0}^\infty g_{n}\cdot(\vec{p})^nx_i\\
&=\sum_{n=0}^\infty g_{n}\cdot\left(x_i(\vec{p})^n-(\vec{p})^nx_i\right)\\
&=\sum_{n=0}^\infty g_{n}\left[x_i,\vec{p}^n\right]\\
\end{aligned}$$
Similar to a previous problem:
$$\begin{align}
\left[x_i,p_j^n\right]&=i\hbar\cdot np_i^{n-1}\delta_{ij}\\
\end{align}$$
Substituting, we get:
$$\begin{aligned}[]
[x_i,G(\vec{p})]
&=\sum_{n=0}^\infty g_{n}\left[x_i,\vec{p}^n\right]\\
&=\sum_{n=0}^\infty g_{n}\cdot i\hbar np_i^{n-1}\\
&=i\hbar\sum_{n=0}^\infty g_{n}\cdot np_i^{n-1}\\
&=i\hbar\sum_{n=0}^\infty g_{n}\dfrac{\partial}{\partial p_i}\left(p_i^{n}\right)\\
&=i\hbar\dfrac{\partial}{\partial p_i}\sum_{n=0}^\infty g_{n}\left(p_i^{n}\right)\\
&=i\hbar\dfrac{\partial}{\partial p_i}\sum_{n=0}^\infty g_{n}\left(\vec{p}^{n}\right)\\
&=i\hbar\dfrac{\partial}{\partial p_i}G(\vec{p})\\
\Aboxed{[x_i,G(\vec{p})]&=i\hbar\dfrac{\partial G}{\partial p_i}}
\end{aligned}$$
Writing the second commutator:
$$\begin{aligned}[]
[p_i,F(\vec{x})]
&=p_i\sum_{n=0}^\infty f_{n}\cdot(\vec{x})^n-\sum_{n=0}^\infty f_{n}\cdot(\vec{x})^np_i\\
&=\sum_{n=0}^\infty f_{n}\cdot\left(p_i(\vec{x})^n-(\vec{x})^np_i\right)\\
&=\sum_{n=0}^\infty f_{n}\left[p_i,\vec{x}^n\right]\\
\end{aligned}$$
Similar to a previous problem:
$$\begin{align}
\left[p_i,x_j^n\right]&=-i\hbar\cdot nx_i^{n-1}\delta_{ij}\\
\end{align}$$
Substituting, we get:
$$\begin{aligned}[]
[p_i,F(\vec{x})]
&=\sum_{n=0}^\infty f_{n}\left[p_i,\vec{x}^n\right]\\
&=\sum_{n=0}^\infty f_{n}\cdot (-i\hbar) nx_i^{n-1}\\
&=-i\hbar\sum_{n=0}^\infty f_{n}\cdot nx_i^{n-1}\\
&=i\hbar\sum_{n=0}^\infty f_{n}\dfrac{\partial}{\partial x_i}\left(x_i^{n}\right)\\
&=i\hbar\dfrac{\partial}{\partial x_i}\sum_{n=0}^\infty f_{n}\left(x_i^{n}\right)\\
&=i\hbar\dfrac{\partial}{\partial x_i}\sum_{n=0}^\infty f_{n}\left(\vec{x}^{n}\right)\\
&=i\hbar\dfrac{\partial}{\partial p_i}F(\vec{x})\\
\Aboxed{[p_i,F(\vec{x})]&=i\hbar\dfrac{\partial F}{\partial x_i}}
\end{aligned}$$
---
#### Question 1.31.B
Evaluate $[x^2,p^2]$. Compare your result with the classical Poisson bracket $[x^2,p^2]_\text{classical}$.

In Quantum Mechanics:
$$\begin{aligned}[]
[x^2,p^2]&=[x^2,p]p+p[x^2,p]\\
&=-[p,x^2]p-p[p, x^2]\\
&=-([p,x]x+x[p,x])p-p([p,x]x+x[p,x])\\
&=-[p,x]xp-x[p,x]p-p[p,x]x-px[p,x]\\
&=[x,p]xp+x[x,p]p+p[x,p]x+px[x,p]\\
&=i\hbar\left(xp+xp+px+px\right)\\
&=2i\hbar\left(xp+px\right)\\
\Aboxed{[x^2,p^2]&=2i\hbar\left\{x,p\right\}}\\
&=2i\hbar\left(px-xp+2xp\right)\\
&=4i\hbar\cdot xp+2i\hbar\left(-i\hbar\right)\\
\Aboxed{[x^2,p^2]&=4i\hbar\cdot xp+2\hbar^2}
\end{aligned}$$
In Classical Mechanics:
$$\begin{aligned}[]
[x^2,p^2]_\text{Poisson}&=\dfrac{\partial(x^2)}{\partial x}\dfrac{\partial(p^2)}{\partial p}-\dfrac{\partial(x^2)}{\partial p}\dfrac{\partial(p^2)}{\partial x}\\
&=2x\cdot2p-0\cdot0\\
\Aboxed{[x^2,p^2]_\text{Poisson}&=4xp}
\end{aligned}$$
They are very similar, especially in the classical limit as $\hbar\rightarrow0$.

---
### Question 1.36
#### Question 1.36.A
Prove the following:
$$\begin{align}
\bra{p'}x\ket\alpha&=i\hbar\dfrac{\partial}{\partial p'}\braket{p'|\alpha}\\
\bra{\beta}x\ket\alpha&=\int \phi_\beta(p')^*\cdot i\hbar\dfrac{\partial}{\partial p'}\phi_\alpha(p')\ dp'
\end{align}$$
Where $\phi_\alpha(p')=\braket{p'|\alpha}$ and $\phi_\beta(p')=\braket{p'|\beta}$ are momentum-space wavefunctions.

For expression 1:
$$\begin{align}
\bra{p'}x\ket\alpha&=\bra{p'}x\int\ket{p}\braket{p|\alpha}\ dp\\
&=\int\bra{p'}x\ket{p}\braket{p|\alpha}\ dp\\
&=\int i\hbar\dfrac{\partial}{\partial p'}\delta(p-p')\braket{p|\alpha}\ dp\\
&=i\hbar\dfrac{\partial}{\partial p'}\int \delta(p-p')\braket{p|\alpha}\ dp\\
\Aboxed{\bra{p'}x\ket\alpha&=i\hbar\dfrac{\partial}{\partial p'}\braket{p'|\alpha}}
\end{align}$$
For expression 2:
$$\begin{align}
\bra{\beta}x\ket\alpha&=\int\braket{\beta|p'}\bra{p'}x\ket{\alpha}\ dp'\\
&=\int\braket{p'|\beta}^*i\hbar\dfrac{\partial}{\partial p'}\braket{p'|\alpha}\ dp'\\
\Aboxed{\bra{\beta}x\ket\alpha&=i\hbar\int\phi_\beta(p')^*\dfrac{\partial}{\partial p'}\phi_\alpha(p')\ dp'}
\end{align}$$
---
#### Question 1.36.B
What is the physical significance of:
$$\begin{align}
\exp\left(\dfrac{ix\Xi}{\hbar}\right)
\end{align}$$
Where $x$ is a the position operator and $\Xi$ is some number with the dimension of momentum.
Justify your answer.

The parameter $\Xi$ is an element of the Lie algebra of inverse displacement divided by $\hbar$.
Therefore, $\Xi$ is the generator of momentum translation.

The exponential, then, is the operator that translates a wavefunction such that:
$$\begin{align}
\exp\left(\dfrac{ix\Xi}{\hbar}\right)\ket{p}&=\ket{p-\Xi}
\end{align}$$
I.e. similar to the spatial translation operator, this is a momentum translation operator (or a speedup operator). It's naturally expressed on a momentum eigenstate so show that it translates the momentum eigenstate by $\Xi$.