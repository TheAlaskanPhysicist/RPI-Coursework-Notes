Author: Stanley Goodwin
Date: January 27th, 2025

---
## PDF Question
**Note:** In this problem, you must use (and practice) the convention where summation is implied over repeated indices (Einstein notation).

---
### PDF Question 1.A
As a warm-up exercise, show by brute force that the momentum operator $\vec{p}$ is a (Cartesian) vector operator, i.e., it satisfies:
$$\begin{align}
[L_i,p_j]&=i\hbar\epsilon_{ijk}p_k
\end{align}$$
Hint: Write $L_i=\epsilon_{imn}x_mp_n$ and use $[x_m,p_j]=i\hbar\delta_{mj}$.
$$\begin{align}
[L_i,p_j]&=[\epsilon_{imn}x_mp_n,p_j]\\
&=(\epsilon_{imn}x_mp_n)p_j-p_j(\epsilon_{imn}x_mp_n)\\
&=\epsilon_{imn}x_mp_np_j-\epsilon_{imn}p_jx_mp_n
&& (p_j\epsilon_{imn}=\epsilon_{imn}p_j)\\
&=\epsilon_{imn}(x_mp_np_j-p_jx_mp_n)\\
&=\epsilon_{imn}\left(x_mp_np_j-(x_mp_j-i\hbar\delta_{mj})p_n\right)
&& (p_jx_m=x_mp_j-i\hbar\delta_{mj})\\
&=\epsilon_{imn}\left(x_mp_np_j-x_mp_np_j+i\hbar\delta_{mj}p_n\right)
&& (p_jp_n=p_np_j)\\
&=\epsilon_{imn}\left(i\hbar\delta_{mj}p_n\right)\\
&=i\hbar\epsilon_{ijn}p_n\\
\Aboxed{[L_i,p_j]&=i\hbar \epsilon_{ijk}p_k} && \text{(Reindexing }n\rightarrow k)
\end{align}$$
---
### PDF Question 1.B
Recall the QM Runge-Lenz vector from class and the text (Chapter 4.1):
$$\begin{align}
\vec{M}&=\dfrac{1}{2m}\left(\vec p\times\vec L-\vec L\times\vec p\right)-\dfrac{Ze^2}{r}\vec{x}
\end{align}$$
where $r=|\vec{x}|$. Show that:
$$\begin{align}
\vec{L}\cdot\vec{M}&=L_iM_i=0
\end{align}$$
Here, you can use these identities shown earlier:
$[\vec{L},H]=0$ (for Coulomb potential); $[L_i,p_j]=i\hbar\epsilon_{ijk}p_k$.

---
#### 1.B: Dot Product Proof
Start with substituting the Runge-Lenz vector into the dot product:
$$\begin{align}
\vec{L}\cdot\vec{M}&=\vec{L}\cdot\left(\dfrac{1}{2m}\left(\vec p\times\vec L-\vec L\times\vec p\right)-\dfrac{Ze^2}{r}\vec{x}\right)\\
&=\dfrac{1}{2m}\vec L\cdot\left(\vec p\times\vec L\right)-\dfrac{1}{2m}\vec L\cdot\left(\vec L\times\vec p\right)-\dfrac{Ze^2}{r}(\vec{L}\cdot\vec{x})\\
\end{align}$$
From the scalar triple product, we know that:
$$\begin{align}
\vec a\cdot(\vec b\times\vec c)=\vec b\cdot(\vec c\times\vec a)=\vec c\cdot(\vec a\times\vec b)
\end{align}$$
Since these are all identical under cyclic permutation, if any of the vectors are colinear with each other, then the scalar product must be 0:
$$\begin{align}
\vec L\cdot\left(\vec p\times\vec L\right)=\vec p\cdot\left(\vec L\times\vec L\right)=0\\
\vec L\cdot\left(\vec L\times\vec p\right)=\vec p\cdot\left(\vec L\times\vec L\right)=0
\end{align}$$
For the position term, we have to use the definition of the angular momentum $\vec L=\vec x\times\vec p$:
$$\begin{align}
\vec{L}\cdot\vec{x}=\vec{x}\cdot\vec{L}=\vec{x}\cdot(\vec{x}\times\vec{p})=\vec{p}\cdot(\vec{x}\times\vec{x})=0
\end{align}$$
Substituting these back in, we see:
$$\begin{align}
\vec{L}\cdot\vec{M}&=\dfrac{1}{2m}\vec L\cdot\left(\vec p\times\vec L\right)-\dfrac{1}{2m}\vec L\cdot\left(\vec L\times\vec p\right)-\dfrac{Ze^2}{r}(\vec{L}\cdot\vec{x})\\
&=\dfrac{1}{2m}\cdot0-\dfrac{1}{2m}\cdot0-\dfrac{Ze^2}{r}\cdot0\\
\Aboxed{\vec{L}\cdot\vec{M}&=0}
\end{align}$$
Thus concludes the proof.

---
#### 1.B: Tensors Proof
We can write the product of two vectors as:
$$\begin{align}
\vec a\cdot\vec b&=a^ib^i& \vec a\times\vec b&=a^ib^j(\epsilon_{ijk}e_k)
\end{align}$$
The Runge-Lenz vector is then:
$$\begin{align}
\vec{M}&=\dfrac{1}{2m}\left(\vec p\times\vec L-\vec L\times\vec p\right)-\dfrac{Ze^2}{r}\vec{x}\\
&=\dfrac{1}{2m}\left(p^iL^j(\epsilon_{ijk}e_k)-L^ip^j(\epsilon_{ijk}e_k)\right)-\dfrac{Ze^2}{r}x^ke_k\\
&=\dfrac{1}{2m}\left(\epsilon_{ijk}e_k\right)\left(p^iL^j-L^ip^j\right)-\dfrac{Ze^2}{r}x^ke_k\\
&=\dfrac{1}{2m}\left(\epsilon_{ijk}e_k\right)\left(p^i(\epsilon_{nmj}x^np^m)-(\epsilon_{nmi}x^np^m)p^j\right)-\dfrac{Ze^2}{r}x^ke_k\\
&=\dfrac{1}{2m}\left(\epsilon_{ijk}e_k\right)\left(\epsilon_{jnm}p^ix^np^m-\epsilon_{inm}x^np^mp^j\right)-\dfrac{Ze^2}{r}x^ke_k\\
&=\dfrac{1}{2m}\left(\epsilon_{ijk}\epsilon_{jnm}e_kp^ix^np^m-\epsilon_{ijk}\epsilon_{inm}x^np^mp^je_k\right)-\dfrac{Ze^2}{r}x^ke_k\\
M_k&=-\dfrac{1}{2m}\left(\epsilon_{jik}\epsilon_{jnm}\right)p^ix^np^m-\dfrac{1}{2m}\left(\epsilon_{ijk}\epsilon_{inm}\right)x^np^mp^j-\dfrac{Ze^2}{r}x^k\\
&=-\dfrac{1}{2m}\left(\delta_{in}\delta_{km}-\delta_{im}\delta_{kn}\right)p^ix^np^m-\dfrac{1}{2m}\left(\delta_{jn}\delta_{km}-\delta_{jm}\delta_{kn}\right)x^np^mp^j-\dfrac{Ze^2}{r}x^k\\
&=-\dfrac{1}{2m}\left(p^ix^ip^k-p^ix^kp^i\right)-\dfrac{1}{2m}\left(x^jp^kp^j-x^kp^jp^j\right)-\dfrac{Ze^2}{r}x^k\\
&=-\dfrac{1}{2m}\left(p^ix^ip^k-p^ix^kp^i+x^jp^kp^j-x^kp^jp^j\right)-\dfrac{Ze^2}{r}x^k\\
&=-\dfrac{1}{2m}\left((x^ip^i-i\hbar)p^k-(x^kp^i-i\hbar\delta_{ik})p^i+x^jp^kp^j-x^kp^jp^j\right)-\dfrac{Ze^2}{r}x^k\\
&=-\dfrac{1}{2m}\left(x^ip^ip^k-i\hbar p^k-x^kp^ip^i+i\hbar\delta_{ik}p^i+x^jp^kp^j-x^kp^jp^j\right)-\dfrac{Ze^2}{r}x^k\\
&=-\dfrac{1}{2m}\left(x^ip^ip^k+x^jp^jp^k-2x^kp^jp^j\right)-\dfrac{Ze^2}{r}x^k\\
&=-\dfrac{1}{m}\left(x^ip^ip^k-x^kp^jp^j\right)-\dfrac{Ze^2}{r}x^k\\
M_k&=-\dfrac{x^ip^i}{m}p^k+\left(\dfrac{p^jp^j}{m}-\dfrac{Ze^2}{r}\right)x^k\\
\Aboxed{M_i&=-\dfrac{x^jp^j}{m}p^i+\left(\dfrac{p^jp^j}{m}-\dfrac{Ze^2}{r}\right)x^i}
\end{align}$$
We can now substitute this into the definition of the inner product:
$$\begin{align}
L_iM_i&=\left(\epsilon_{ijk}x^jp^k\right)\left(-\dfrac{x^np^n}{m}p^i+\left(\dfrac{p^np^n}{m}-\dfrac{Ze^2}{r}\right)x^i\right)\\
&=-\dfrac{1}{m}\epsilon_{ijk}x^jp^kx^np^np^i+\dfrac{1}{m}\epsilon_{ijk}x^jp^kp^np^nx^i-\dfrac{Ze^2}{r}\epsilon_{ijk}x^jp^kx^i
\end{align}$$
First term:
$$\begin{align}
-\dfrac{1}{m}\epsilon_{ijk}x^jp^kx^np^np^i
&=-\dfrac{1}{m}\epsilon_{ijk}x^jp^kx^np^ip^n\\
&=-\dfrac{1}{m}\epsilon_{ijk}x^jp^k(p^ix^n-i\hbar\delta_{in})p^n\\
&=-\dfrac{1}{m}(\epsilon_{ijk}x^jp^kp^i)x^np^n+\dfrac{i\hbar}{m}(\epsilon_{ijk}x^jp^kp^i)\\
-\dfrac{1}{m}\epsilon_{ijk}x^jp^kx^np^np^i&=-\dfrac{1}{m}\epsilon_{ijk}x^jp^kp^i\left(x^np^n-i\hbar\right)
\end{align}$$
Second term:
$$\begin{align}
\dfrac{1}{m}\epsilon_{ijk}x^jp^kp^np^nx^i
&=\dfrac{1}{m}\epsilon_{ijk}x^jp^kp^n(x^ip^n-i\hbar\delta_{in})\\
&=\dfrac{1}{m}\epsilon_{ijk}x^jp^k(p^nx^i)p^n-\dfrac{i\hbar}{m}\epsilon_{ijk}x^jp^kp^i\\
&=\dfrac{1}{m}\epsilon_{ijk}x^jp^k(x^ip^n-i\hbar\delta_{in})p^n-\dfrac{i\hbar}{m}\epsilon_{ijk}x^jp^kp^i\\
&=\dfrac{1}{m}(\epsilon_{ijk}x^jp^kx^i)p^np^n-\dfrac{2i\hbar}{m}\epsilon_{ijk}x^jp^kp^i\\
\dfrac{1}{m}\epsilon_{ijk}x^jp^kp^np^nx^i&=\dfrac{1}{m}(\epsilon_{ijk}x^jp^kx^i)\left(p^np^n-2i\hbar\right)\\
\end{align}$$
Substituting, we get:
$$\begin{align}
L_iM_i
&=-\dfrac{1}{m}\epsilon_{ijk}x^jp^kx^np^np^i+\dfrac{1}{m}\epsilon_{ijk}x^jp^kp^np^nx^i-\dfrac{Ze^2}{r}\epsilon_{ijk}x^jp^kx^i\\
&=-\dfrac{1}{m}\epsilon_{ijk}x^jp^kp^i\left(x^np^n-i\hbar\right)+\dfrac{1}{m}(\epsilon_{ijk}x^jp^kx^i)\left(p^np^n-2i\hbar\right)-\dfrac{Ze^2}{r}\epsilon_{ijk}x^jp^kx^i\\
&=\epsilon_{ijk}x^jp^kp^i\left(\dfrac{p^np^n-x^np^n-i\hbar}{m}-\dfrac{Ze^2}{r}\right)\\
&=\left(\dfrac{1}{2}\epsilon_{ijk}x^j[p^k,p^i]+\dfrac{1}{2}\epsilon_{ijk}x^j\{p^k,p^i\}\right)\left(\dfrac{p^np^n-x^np^n-i\hbar}{m}-\dfrac{Ze^2}{r}\right)\\
&=\left(0+\dfrac{1}{2}\epsilon_{ijk}x^jP^{ki}\right)\left(\dfrac{p^np^n-x^np^n-i\hbar}{m}-\dfrac{Ze^2}{r}\right)\\
&=\left(+\dfrac{1}{2}\epsilon_{kji}x^jP^{ik}\right)\left(\dfrac{p^np^n-x^np^n-i\hbar}{m}-\dfrac{Ze^2}{r}\right)\\
&=\left(-\dfrac{1}{2}\epsilon_{ijk}x^jP^{ki}\right)\left(\dfrac{p^np^n-x^np^n-i\hbar}{m}-\dfrac{Ze^2}{r}\right)
\end{align}$$
In order for this to occur, we have:
$$\begin{align}
\dfrac{1}{2}\epsilon_{ijk}x^jP^{ki}=-\left(\dfrac{1}{2}\epsilon_{ijk}x^jP^{ki}\right)
\end{align}$$
Thus the inside must be 0 in order for this relation to hold. Therefore, we find that:
$$\begin{align}
L_iM_i
&=\left(-\dfrac{1}{2}\epsilon_{ijk}x^jP^{ki}\right)\left(\dfrac{p^np^n-x^np^n-i\hbar}{m}-\dfrac{Ze^2}{r}\right)\\
&=0\cdot\left(\dfrac{p^np^n-x^np^n-i\hbar}{m}-\dfrac{Ze^2}{r}\right)\\
\Aboxed{L_iM_i&=0}
\end{align}$$
---
## Question 4.3
A quantum-mechanical state $\ket\Psi$ is known to be a simultaneous eigenstate of two Hermitian operators $A$ and $B$ which anti-commute,
$$\begin{align}
AB+BA=0
\end{align}$$
---
### Question 4.3.A
What can you say about the eigenvalues of $A$ and $B$ for state $\ket\Psi$?

We can notice the following:
 - Hermitian $\implies$ $a,b \in\mathbb{R}$
 - Eigenstates $\implies$ $A\ket{\Psi(a,b)}=a\ket{\Psi(a,b)}$, $B\ket{\Psi(a,b)}=b\ket{\Psi(a,b)}$
 - Imposed $\implies$ $\{A,B\}\ket{\Psi(a,b)}=0$
Applying the anti-commutator to our state results in the following:
$$\begin{align}
\{A,B\}\ket{\Psi(a,b)}&=(A B+B A)\ket{\Psi(a,b)}\\
&=A B\ket{\Psi(a,b)}+B A\ket{\Psi(a,b)}\\
&=A b\ket{\Psi(a,b)}+B a\ket{\Psi(a,b)}\\
&=b A\ket{\Psi(a,b)}+a B\ket{\Psi(a,b)} && (a,b\in\mathbb{R}\implies A b=b A,a B=B a)\\
&=b a\ket{\Psi(a,b)}+a b\ket{\Psi(a,b)}\\
&=a b\ket{\Psi(a,b)}+a b\ket{\Psi(a,b)} && (a,b\in\mathbb{R}\implies a b=b a)\\
\Aboxed{0\ket{\Psi(a,b)}&=2a b\ket{\Psi(a,b)}}
\end{align}$$
With the prior assumptions, one of the eigenvalues must be zero (both 0 is trivial).
 - $\forall a\ne0, b=0$, thus is "extremally" incompatible. As in, as incompatible as possible.
 - Likewise, under exchange $a\leftrightarrow b$, they are incompatible.

For a quantum-mechanical state $\ket\Psi$ that is a simultaneous eigenstate of two Hermitian, anti-commuting operators, at least one of the operator eigenvalues must be $0$.

---
### Question 4.3.B
Illustrate your point using parity (chosen to satisfy $\pi=\pi^\dagger=\pi^{-1}$) and momentum operators.

Where $\lambda$ is the eigenvalue of parity (idk what the standard variable is).
$$\begin{align}
\{\pi,p\}\ket{\Psi(\lambda,p')}&=(\pi p+p\pi)\ket{\Psi(\lambda,p')}\\
&=\pi p\ket{\Psi(\lambda,p')}+p\pi\ket{\Psi(\lambda,p')}\\
&=\pi p'\ket{\Psi(\lambda,p')}+p\lambda\ket{\Psi(\lambda,p')}\\
&=p'\pi\ket{\Psi(\lambda,p')}+\lambda p\ket{\Psi(\lambda,p')}
&& (\lambda,p'\in\mathbb{R}\implies\pi p'=p'\pi,\lambda p=p\lambda)\\
&=p'\lambda\ket{\Psi(\lambda,p')}+\lambda p'\ket{\Psi(\lambda,p')}\\
&=\lambda p'\ket{\Psi(\lambda,p')}+\lambda p'\ket{\Psi(\lambda,p')} 
&& (\lambda,p'\in\mathbb{R}\implies\lambda p'=p'\lambda)\\
\Aboxed{0\ket{\Psi(\lambda,p')}&=2\lambda p'\ket{\Psi(\lambda,p')}}
\end{align}$$
Since we know that $\lambda=\pm1$, then $\boxed{p'=0}$ by necessity. Thus non-zero momentum eigenstates cannot have definite parity, but zero momentum eigenstates do have parity.

This makes sense, since if a wave propagates with momentum $p'$ to the right, parity transforms it to momentum to the left, thus is not preserved under the transform. Instead, the basis must be:
$$\begin{align}
\ket{\Psi(\lambda,p')}&=\dfrac{\ket{p}+\lambda\ket{-p}}{\sqrt2} & \lambda&=\pm1
\end{align}$$
Up to a global phase of the state.

---
## Question 4.4
A spin $1/2$ particle is bound to a fixed center by a spherically symmetrical potential.

I particularly hate spherical harmonic notation, so I'm going to use a different one. I will use:
$$\begin{align}
Y_{l,\ s}^{m_l,m_s}&=\ket{l,m_l}\ket{s,m_s}=Y_l^{m_l}\chi^{m_s}_s\\
_CY_{l,\ s}^{j,m_j}&=\ket{l,s,j,m_j}
\end{align}$$
For the coupled basis, we can see that for $l=0,1$, I will have:
$$\begin{align}
_CY_{l=0}^{1/2,+1/2}&=Y_{0,\ 1/2}^{+0,+1/2}
& _CY_{l=1}^{3/2,+3/2}&=Y_{1,\ 1/2}^{+1,+1/2}\\
_CY_{l=0}^{1/2,-1/2}&=Y_{0,\ 1/2}^{+0,-1/2}
& _CY_{l=1}^{3/2,+1/2}&=\sqrt{\dfrac{2}{3}}Y_{1,\ 1/2}^{+0,+1/2}+\sqrt{\dfrac{1}{3}}Y_{1,\ 1/2}^{+1,-1/2}\\
_CY_{l=1}^{1/2,+1/2}&=\sqrt{\dfrac{1}{3}}Y_{1,\ 1/2}^{+0,+1/2}-\sqrt{\dfrac{2}{3}}Y_{1,\ 1/2}^{+1,-1/2} 
& _CY_{l=1}^{3/2,-1/2}&=\sqrt{\dfrac{1}{3}}Y_{1,\ 1/2}^{-1,+1/2}+\sqrt{\dfrac{2}{3}}Y_{1,\ 1/2}^{+0,-1/2}\\
_CY_{l=1}^{1/2,-1/2}&=\sqrt{\dfrac{2}{3}}Y_{1,\ 1/2}^{-1,+1/2}-\sqrt{\dfrac{2}{3}}Y_{1,\ 1/2}^{+0,-1/2}
& _CY_{l=1}^{3/2,-3/2}&=Y_{1,\ 1/2}^{-1,-1/2}
\end{align}$$
For usage later, substitute the uncoupled basis as a product of function to get:
$$\begin{align}
_CY_{l=0}^{1/2,+1/2}&=Y_{0}^{0}\chi^{+1/2}_{1/2} & _CY_{l=1}^{3/2,+3/2}&=Y_{1}^{1}\chi^{+1/2}_{1/2}\\
_CY_{l=0}^{1/2,-1/2}&=Y_{0}^{0}\chi^{-1/2}_{1/2} & _CY_{l=1}^{3/2,+1/2}&=\sqrt{\dfrac{2}{3}}Y_{1}^{0}\chi^{+1/2}_{1/2}+\sqrt{\dfrac{1}{3}}Y_{1}^{1}\chi^{-1/2}_{1/2}\\
_CY_{l=1}^{1/2,+1/2}&=\sqrt{\dfrac{1}{3}}Y_{1}^{0}\chi^{+1/2}_{1/2}-\sqrt{\dfrac{2}{3}}Y_{1}^{1}\chi^{-1/2}_{1/2} &
_CY_{l=1}^{3/2,-1/2}&=\sqrt{\dfrac{1}{3}}Y_{1}^{-1}\chi^{+1/2}_{1/2}+\sqrt{\dfrac{2}{3}}Y_{1}^{0}\chi^{-1/2}_{1/2}\\
_CY_{l=1}^{1/2,-1/2}&=\sqrt{\dfrac{2}{3}}Y_{1}^{-1}\chi^{+1/2}_{1/2}-\sqrt{\dfrac{1}{3}}Y_{1}^{0}\chi^{-1/2}_{1/2} &
_CY_{l=1}^{3/2,-3/2}&=Y_{1}^{-1}\chi^{-1/2}_{1/2}
\end{align}$$
Lastly, we can substitute the spherical harmonic function to have:
$$\begin{align}
_CY_{l=0}^{1/2,+1/2}&=\sqrt{\dfrac{1}{4\pi}}\chi^{+1/2}_{1/2} & _CY_{l=1}^{3/2,+3/2}&=-\sqrt{\dfrac{3}{8\pi}}e^{i\phi}\sin\theta\ \chi^{+1/2}_{1/2}\\
_CY_{l=0}^{1/2,-1/2}&=\sqrt{\dfrac{1}{4\pi}}\chi^{-1/2}_{1/2} & _CY_{l=1}^{3/2,+1/2}&=\sqrt{\dfrac{1}{2\pi}}\cos\theta\ \chi^{+1/2}_{1/2}-\sqrt{\dfrac{1}{8\pi}}e^{i\phi}\sin\theta\ \chi^{-1/2}_{1/2}\\
_CY_{l=1}^{1/2,+1/2}&=\sqrt{\dfrac{1}{4\pi}}\cos\theta\ \chi^{+1/2}_{1/2}+\sqrt{\dfrac{1}{4\pi}}e^{i\phi}\sin\theta\ \chi^{-1/2}_{1/2} &
_CY_{l=1}^{3/2,-1/2}&=\sqrt{\dfrac{1}{8\pi}}e^{-i\phi}\sin\theta\ \chi^{+1/2}_{1/2}+\sqrt{\dfrac{1}{2\pi}}\cos\theta\ \chi^{-1/2}_{1/2}\\
_CY_{l=1}^{1/2,-1/2}&=\sqrt{\dfrac{1}{4\pi}}e^{-i\phi}\sin\theta\ \chi^{+1/2}_{1/2}-\sqrt{\dfrac{1}{4\pi}}\cos\theta\ \chi^{-1/2}_{1/2} &
_CY_{l=1}^{3/2,-3/2}&=\sqrt{\dfrac{3}{8\pi}}e^{-i\phi}\sin\theta\ \chi^{-1/2}_{1/2}
\end{align}$$
---
### Question 4.4.A
Write down the spin angular function $Y_{l=0}^{j=1/2,m_j=1/2}$.

In our case, we're looking at the state where $j=1/2$, $l=0$, and $m_j=+1/2$. From the table list above, we can write the following:
$$\begin{align}
Y_{l=0}^{j=1/2,m_j=1/2}=\ _CY_{l=0}^{1/2,+1/2}&=Y_{0}^{0}\chi^{+1/2}_{1/2}
\end{align}$$
We can read off $Y_0^0$ from the spherical harmonics table, and use the natural basis for spinors:
$$\begin{align}
\Aboxed{Y_{l=0}^{j=1/2,m_j=1/2}&=\sqrt{\dfrac{1}{4\pi}}\begin{bmatrix}1\\0\end{bmatrix}}
\end{align}$$
---
### Question 4.4.B
Express $(\sigma\cdot\vec{x})Y_{l=0}^{j=1/2,m_j=1/2}$ in terms of some other $Y_{l}^{j,m_j}$.

This operator in the front can be written, in spherical coordinates as:
$$\begin{align}
\sigma\cdot\vec{x}&=r(\sigma\cdot\hat{r})=r\begin{bmatrix}\cos\theta&e^{-i\phi}\sin\theta\\e^{+i\phi}\sin\theta&-\cos\theta\end{bmatrix}
\end{align}$$
Then we can multiply this by the result found in A to find:
$$\begin{align}
(\sigma\cdot\vec{x})\ _CY_{l=0}^{1/2,+1/2}
&=(\sigma\cdot\vec{x})\ Y_0^0\chi^{+1/2}_{1/2}\\
&=\sqrt{\dfrac{1}{4\pi}}r\begin{bmatrix}\cos\theta&e^{-i\phi}\sin\theta\\e^{+i\phi}\sin\theta&-\cos\theta\end{bmatrix}\begin{bmatrix}1\\0\end{bmatrix}\\
&=\sqrt{\dfrac{1}{4\pi}}r\begin{bmatrix}\cos\theta\\e^{+i\phi}\sin\theta\end{bmatrix}\\
\end{align}$$
We can use the spherical harmonics to find:
$$\begin{align}
\cos\theta&=\sqrt{\dfrac{4\pi}{3}}Y_{1}^{0}\\
e^{i\phi}\sin\theta&=-\sqrt{\dfrac{8\pi}{3}}Y_{1}^{+1}
\end{align}$$
Substituting, we get:
$$\begin{align}
(\sigma\cdot\vec{x})\ _CY_{l=0}^{1/2,+1/2}
&=\sqrt{\dfrac{1}{4\pi}}r\begin{bmatrix}\cos\theta\\e^{+i\phi}\sin\theta\end{bmatrix}\\
&=\sqrt{\dfrac{1}{4\pi}}r\begin{bmatrix}\sqrt{\tfrac{4\pi}{3}}Y_{1}^{0}\\-\sqrt{\tfrac{8\pi}{3}}Y_{1}^{+1}\end{bmatrix}\\
&=\sqrt{\dfrac{1}{3}}r\begin{bmatrix}Y_{1}^{0}\\-\sqrt{2}Y_{1}^{+1}\end{bmatrix}\\
(\sigma\cdot\vec{x})\ _CY_{l=0}^{1/2,+1/2}&=r\left(\sqrt{\dfrac{1}{3}}Y_{1}^{0}\chi^{+1/2}_{1/2}-\sqrt{\dfrac{2}{3}}Y_{1}^{+1}\chi^{-1/2}_{1/2}\right)
\end{align}$$
Looking at the table, we have:
$$\begin{align}
_CY_{l=1}^{1/2,+1/2}&=\sqrt{\dfrac{1}{3}}Y_{1}^{0}\chi^{+1/2}_{1/2}-\sqrt{\dfrac{2}{3}}Y_{1}^{1}\chi^{-1/2}_{1/2}
\end{align}$$
Thus, in total, we have that:
$$\begin{align}
(\sigma\cdot\vec{x})\ _CY_{l=0}^{1/2,+1/2}
&=\ _CY_{l=1}^{1/2,+1/2}
\end{align}$$
Or to put it back in standard notation:
$$\begin{align}
\Aboxed{(\sigma\cdot\vec{x})\ _CY_{l=0}^{j=1/2,m_j=+1/2}
&=Y_{l=1}^{j=1/2,m_j=+1/2}}
\end{align}$$
---
### Question 4.4.C
Show that your result in (b) is understandable in view of the transformation properties of the operator $\vec{S}\cdot\vec{x}$ under rotations and under space inversion (parity).

We can rewrite $\vec{S}\cdot\vec{x}$ to be in terms of the Pauli vector as $\dfrac{\hbar}{2}\sigma\cdot\vec{x}$. Under parity:
$$\begin{align}
\pi\left(\dfrac{\hbar}{2}\sigma\cdot\vec{x}\right)&=\dfrac{\hbar}{2}\sigma\cdot\pi\left(\vec{x}\right)=\dfrac{\hbar}{2}\sigma\cdot\left(-\vec{x}\right)=-\vec{S}\cdot\vec{x}
\end{align}$$
Under parity, $\vec{S}\cdot\vec{x}$ is odd. Our original state, $l=0$, was even under parity. The $\vec{x}$ effectively adds an angular dependence ($l=1$) to our prior state, thus becoming odd under parity.

---
## Question 4.7
### Question 4.7.A
Let $\psi(\vec{x},t)$ be the wave function of a spinless particle corresponding to a plane-wave in three dimensions. Show that $\psi^*(\vec{x},-t)$ is a wavefunction for the plane wave with the momentum direction reversed.

A three-dimensional plane-wave wavefunction as:
$$\begin{align}
\psi(\vec{x},t)&=A\exp\left(i\vec{k}\cdot\vec{x}-i\omega t\right)
\end{align}$$
Applying time-reversal and complex conjugation, we get:
$$\begin{align}
\psi^*(\vec{x},-t)
&=\left[A\exp\left(i\vec{k}\cdot\vec{x}-i\omega (-t)\right)\right]^*\\
&=\left[A\exp\left(i\vec{k}\cdot\vec{x}+i\omega t\right)\right]^*\\
&=A\exp\left(-i\vec{k}\cdot\vec{x}-i\omega t\right)\\
\Aboxed{\psi^*(\vec{x},-t)&=A\exp\left(i(-\vec{k})\cdot\vec{x}-i\omega t\right)}
\end{align}$$
This operation looks identical to the prior wavefunction with the momentum direction reversed.

---
### Question 4.7.B
Let $\chi(\hat{n})$ be the two-component eigenspinor $\sigma\cdot\hat{n}$ with eigenvalue $+1$. *Using the explicit form of* $\chi(\hat{n})$, in terms of polar and azimuthal angles $\beta$ and $\gamma$ that characterize $\hat{n}$, verify that $-i\sigma_2\chi^*(\hat{n})$ is the two-component eigenspinor with the spin direction reversed.

We can start by writing the eigenspinor in as Euler angles (in the Z-basis):
$$\begin{align}
\chi(\hat{n})&=\begin{bmatrix}\cos(\beta/2)\\e^{i\gamma}\sin(\beta/2)\end{bmatrix}
& \implies &&
\chi^*(\hat{n})&=\begin{bmatrix}\cos(\beta/2)\\e^{-i\gamma}\sin(\beta/2)\end{bmatrix}
\end{align}$$
If I remember correctly, $\sigma_2=\sigma_y$, and so:
$$\begin{align}
-i\sigma_2\chi^*(\hat{n})&=-i\begin{bmatrix}0&-i\\i&0\end{bmatrix}
\begin{bmatrix}\cos(\beta/2)\\e^{-i\gamma}\sin(\beta/2)\end{bmatrix}\\
&=\begin{bmatrix}0&-1\\1&0\end{bmatrix}
\begin{bmatrix}\cos(\beta/2)\\e^{-i\gamma}\sin(\beta/2)\end{bmatrix}\\
\chi(-\hat{n})&=\begin{bmatrix}-e^{-i\gamma}\sin(\beta/2)\\\cos(\beta/2)\end{bmatrix}
\end{align}$$
To verify, we can evaluate the inner product of these two vectors:
$$\begin{align}
\chi(-\hat{n})^\dagger\chi(\hat{n})
&=\begin{bmatrix}-e^{-i\gamma}\sin(\beta/2)\\\cos(\beta/2)\end{bmatrix}^\dagger
\begin{bmatrix}\cos(\beta/2)\\e^{i\gamma}\sin(\beta/2)\end{bmatrix}\\
&=\begin{bmatrix}-e^{i\gamma}\sin(\beta/2)&\cos(\beta/2)\end{bmatrix}
\begin{bmatrix}\cos(\beta/2)\\e^{i\gamma}\sin(\beta/2)\end{bmatrix}\\
&=-e^{i\gamma}\sin(\beta/2)\cos(\beta/2)+\cos(\beta/2)e^{i\gamma}\sin(\beta/2)\\
&=-e^{i\gamma}\sin(\beta/2)\cos(\beta/2)+e^{i\gamma}\sin(\beta/2)\cos(\beta/2)\\
\Aboxed{\chi(-\hat{n})^\dagger\chi(\hat{n})&=0}
\end{align}$$
This is, indeed, the opposite spin state, and thus concludes the proof.

---
## Question 4.10
### Question 4.10.A
For the time-reversal operator $\Theta$, use $\Theta\vec{J}\Theta^{-1}=-\vec{J}$ to show that $\Theta\ket{j,m}\propto\ket{j,-m}$ up to some phase that includes the factor $(-1)^m$. Show that $\Theta\ket{j,m}$, where $\delta$ is independent of $m$.

Not sure where to start, but we can see how $\Theta$ operates on $J_\pm$ and $J_z$:
$$\begin{align}
\Theta J_\pm\Theta^{-1}&=\Theta(J_x\pm iJ_y)\Theta^{-1}\\
&=\Theta J_x\Theta^{-1}\pm \Theta iJ_y\Theta^{-1}\\
&=\Theta J_x\Theta^{-1}\mp i\Theta J_y\Theta^{-1}\\
&=-J_x\pm iJ_y\\
&=-(J_x\mp iJ_y)\\
\Aboxed{\Theta J_\pm\Theta^{-1}&=-J_\pm}\\
\Aboxed{\Theta J_z\Theta^{-1}&=-J_z}
\end{align}$$
If we apply $J_z$ to an arbitrary eigenstate, then time-reverse, we can see that:
$$\begin{align}
J_z\ket{j,m}&=m\ket{j,m}\\
\Theta J_z\ket{j,m}&=\Theta m\ket{j,m}\\
-J_z\Theta\ket{j,m}&=m^*\Theta\ket{j,m}\\
J_z(\Theta\ket{j,m})&=-m(\Theta\ket{j,m})\\
\end{align}$$
For another state, $\ket{j,-m}$, we can also see that:
$$\begin{align}
J_z\ket{j,-m}&=-m\ket{j,-m}
\end{align}$$
Thus, we can conclude that:
$$\begin{align}
\Aboxed{\Theta\ket{j,m}\propto\ket{j,-m}}
\end{align}$$
Phase convention gives the proportionality factor as:
$$\begin{align}
\Aboxed{\Theta\ket{j,m}=e^{i\delta}(-1)^{j-m}\ket{j,-m}}
\end{align}$$
---
### Question 4.10.B
Using the same phase convention, find the time-reversed state corresponding to $\mathcal{D}(R)\ket{j,m}$.
Consider using the infinitesimal form $\mathcal{D}(\hat{n},d\phi)$ and then generalize to finite rotations.

The infinitesimal form of the state can be written as:
$$\begin{align}
\mathcal{D}(\hat{n},d\phi)=e^{-i(\vec{J}\cdot\hat{n})d\phi/\hbar}&\sim1-\dfrac{i}{\hbar}(\vec{J}\cdot\hat{n})d\phi+O(d\phi^2)
\end{align}$$
We can then apply $\Theta$ to this state, and see:
$$\begin{align}
\Theta\ \mathcal{D}(\hat{n},d\phi)\ket{j,m}
&\sim\Theta\left(1-\dfrac{i}{\hbar}(\vec{J}\cdot\hat{n})d\phi+O(d\phi^2)\right)\ket{j,m}\\
&=\Theta\ket{j,m}-\Theta\dfrac{i}{\hbar}(\vec{J}\cdot\hat{n})d\phi\ket{j,m}\\
&=\Theta\ket{j,m}+\dfrac{i}{\hbar}\Theta(\vec{J}\cdot\hat{n})d\phi\ket{j,m}\\
&=\Theta\ket{j,m}+\dfrac{i}{\hbar}(-\vec{J}\cdot\hat{n})d\phi\ \Theta\ket{j,m}\\
&=\left(1-\dfrac{i}{\hbar}(\vec{J}\cdot\hat{n})d\phi\right)\Theta\ket{j,m}\\
\Aboxed{\Theta\ \mathcal{D}(\hat{n},d\phi)\ket{j,m}&=\mathcal{D}(\hat{n},d\phi)\ \Theta\ket{j,m}}
\end{align}$$
For finite intervals, we can do the following:
$$\begin{align}
\Theta\ \mathcal{D}(\hat{n},d\phi)^n\ket{j,m}
&=\underbrace{\Theta\ \mathcal{D}(\hat{n},d\phi)\Theta^{-1}}_{n-1\text{ times}}\Theta\ \mathcal{D}(\hat{n},d\phi)\ket{j,m}\\
&=\mathcal{D}(\hat{n},d\phi)^{n-1}\mathcal{D}(\hat{n},d\phi)\ \Theta\ket{j,m}\\
\lim_{n\rightarrow\infty}\Theta\ \mathcal{D}(\hat{n},d\phi)^n\ket{j,m}&=\lim_{n\rightarrow\infty}\mathcal{D}(\hat{n},d\phi)^{n}\ \Theta\ket{j,m}\\
\Aboxed{\Theta\ \mathcal{D}(\hat{n},\phi)\ket{j,m}&=\mathcal{D}(\hat{n},\phi)\ \Theta\ket{j,m}}
\end{align}$$
Rotation and time-reversing operations are agnostic to order between them.

---
### Question 4.10.C
From these results, prove that, independent of $\delta$, one finds:
$$\begin{align}
\mathcal{D}^{(j)*}_{m',m}(R)&=(-1)^{m-m'}\mathcal{D}^{(j)}_{-m',-m}(R)
\end{align}$$
So we know the following properties:
$$\begin{align}
\Theta\ket{j,m}&=(-1)^{j-m}\ket{j,-m} &\implies&& \ket{j,-m}&\propto(-1)^{j+m}\Theta^{-1}\ket{j,m}\\
\Theta\ \mathcal{D}(R)\ket{j,m}&=\mathcal{D}(R)\ \Theta\ket{j,m}\\
\mathcal{D}^{(j)}_{m',m}(R)&=\bra{j,m'}\ \mathcal{D}(R)\ \ket{j,m}
\end{align}$$
We can use equation 3 using $\Theta\Theta^{-1}=1$:
$$\begin{align}
\mathcal{D}^{(j)}_{m',m}(R)&=\bra{j,m'}\ \mathcal{D}(R)\ \ket{j,m}\\
&=\bra{j,m'}\ \Theta^{-1}\Theta\ \mathcal{D}(R)\ \Theta^{-1}\Theta\ \ket{j,m}\\
&=\bra{j,m'}\ \Theta^{-1}\mathcal{D}(R)\Theta\ \ket{j,m}\\
&=\left(\bra{j,m}\ \Theta\mathcal{D}(R)\Theta^{-1}\ \ket{j,m'}\right)^*\\
&=\left(\bra{j,-m}(-1)^{j+m}\mathcal{D}(R)(-1)^{j+m'}\ket{j,-m'}\right)^*\\
\mathcal{D}^{(j)}_{m',m}(R)&=\left((-1)^{j+m}(-1)^{j+m'}\mathcal{D}^{(j)}_{-m',-m}(R)\right)^*\\
\mathcal{D}^{(j)*}_{m',m}(R)&=(-1)^{2j}(-1)^{m+m'}\mathcal{D}^{(j)}_{-m',-m}(R)\\
\Aboxed{\mathcal{D}^{(j)*}_{m',m}(R)&=(-1)^{m-m'}\mathcal{D}^{(j)}_{-m',-m}(R)}
\end{align}$$
---
### Question 4.10.D
Conclude that we are free to choose $\delta=0$, and $\Theta\ket{j,m}=(-1)^m\ket{j,-m}=i^{2m}\ket{j,-m}$.

Start with our original state:
$$\begin{align}
\Theta\ket{j,m}=e^{i\delta}(-1)^{j-m}\ket{j,-m}
\end{align}$$
Since $(-1)^{2j}=1$, then we can absorb the $j$ into some form of global phase $(\delta=0)$. We can then simplify the state, removing the global phase that changes nothing physically:
$$\begin{align}
\Theta\ket{j,m}&=(-1)^{m}\ket{j,-m}
\end{align}$$
To extend it for $m$ that is half-integer, we can use $i^2=-1$ to then write:
$$\begin{align}
\Aboxed{\Theta\ket{j,m}&=i^{2m}\ket{j,-m}}
\end{align}$$

