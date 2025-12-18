## Question 1
The phenomenological (coarse-grained) Landau free-energy density of a system is given by
$$\begin{align}
\mathfrak{L}\left(\phi(\vec{r}),h(\vec{r}),t\right)&=\dfrac{\lambda}{2}\left(\nabla^2\phi\right)^2+\dfrac{1}{2}bt\phi^2+\dfrac{1}{8}d\phi^8-h(\vec{r})\phi(\vec{r})
\end{align}$$
where $\lambda>0$, $b>0$, and $d>0$ are constants, and $t$ is the reduced temperature.

---
### Question 1.A
Determine the critical exponents $\beta$, $\delta$, $\gamma$, and $\alpha$. Some exponents may have to be considered above and below $T_c$ for proper treatment.
$$\begin{align}
\dfrac{\delta\mathfrak{L}}{\delta\phi}
&=\dfrac{\delta}{\delta\phi}\left(\dfrac{\lambda}{2}\left(\nabla^2\phi\right)^2+\dfrac{1}{2}bt\phi^2+\dfrac{1}{8}d\phi^8-h(\vec{r})\phi(\vec{r})\right)\\
&=\dfrac{\lambda}{2}\nabla^4\dfrac{\delta\phi^2}{\delta\phi}+\dfrac{1}{2}bt\dfrac{\delta\phi^2}{\delta\phi}+\dfrac{1}{8}d\dfrac{\delta\phi^8}{\delta\phi}-h(\vec{r})\dfrac{\delta\phi}{\delta\phi}\\
&=\dfrac{\lambda}{2}\nabla^4\cdot2\phi+\dfrac{1}{2}bt\cdot2\phi+\dfrac{1}{8}d\cdot8\phi^7-h(\vec{r})\cdot1\\
\dfrac{\delta\mathfrak{L}}{\delta\phi}&=\lambda\nabla^4\phi+bt\phi+d\phi^7-h(\vec{r})\\
\end{align}$$
At equilibrium, $h(\vec{r})=h$ and $\phi=\braket{\phi}\implies\nabla^n\phi=0$, and so:
$$\begin{align}
0&=bt\phi+d\phi^7-h
\end{align}$$
#### Spontaneous Magnetization $(\beta)$
At the zero-field limit ($h=0$), our equation of state is:
$$\begin{align}
0&=bt\phi+d\phi^7&\implies&&\phi\left(\dfrac{bt}{d}+\phi^6\right)&=0
\end{align}$$
For $t>0$, this expression is imaginary, and thus a real field cannot exist:
$$\begin{align}
\phi&=\pm\sqrt[6]{-\dfrac{bt}{d}} &\implies && \Re(\phi)=0
\end{align}$$
For $t<0$, this expression is actually real, and so the field can exist with value:
$$\begin{align}
\phi&=\pm\sqrt[6]{-\dfrac{bt}{d}} &\implies && \phi&=\pm\sqrt[6]{\dfrac{b}{d}}|t|^{1/6}
\end{align}$$
<div style="page-break-before: always;"></div>




Combining the two domains, we get:
$$\begin{align}
\phi&=\begin{cases}
0 & t>0\\
\pm\sqrt[6]{\dfrac{b}{d}}|t|^{1/6} & t<0\\
\end{cases}
\end{align}$$
The order parameter is very clear to see, being the exponent on $|t|$, and so:
$$\begin{align}
\phi&\sim|t|^{1/6} &\land&& \phi&\sim|t|^{\beta} & \implies && \Aboxed{\beta&=\dfrac{1}{6}}
\end{align}$$
#### Critical Isotherm $\left(\delta\right)$
The critical isotherm is when $T=T_c$, and so $t=0$. Our equation of state reduces to:
$$\begin{align}
0&=d\phi^7-h &\implies&& h&=d\phi^7
\end{align}$$
The parameter can be found by evaluating the logic equation:
$$\begin{align}
h&\sim\phi^{7} &\land&& h&\sim\phi^{\delta} & \implies && \Aboxed{\delta&=7}
\end{align}$$
#### Susceptibility $\left(\gamma\right)$
Using our equilibrium equation earlier (non-zero magnetic field), we can find:
$$\begin{align}
h&=bt\phi+d\phi^7\\
\dfrac{\partial h}{\partial\phi}&=bt+7d\phi^6\\
\chi=\dfrac{\partial\phi}{\partial h}&=\dfrac{1}{bt+7d\phi^6}\\
\end{align}$$
For $t>0$, we know our field $\phi=0$ (from part A), and so:
$$\begin{align}
\chi&=\dfrac{1}{bt+7d\cdot0}=\dfrac{1}{b}|t|^{-1}\\
\end{align}$$
For $t<0$, we know our field $\phi^6=\dfrac{b}{d}|t|$ (from part A), and so:
$$\begin{align}
\chi&=\dfrac{1}{bt+7d\cdot\tfrac{b}{d}|t|}\\
&=\dfrac{1}{-b|t|+7b|t|}\\
\chi&=\dfrac{1}{6b}|t|^{-1}
\end{align}$$
Both cases are in terms $|t|^{-1}$, and we can find the exponent as:
$$\begin{align}
\chi&\sim|t|^{-1} &\land&& \chi&\sim|t|^{-\gamma} & \implies && \Aboxed{\gamma&=1}
\end{align}$$
#### Heat Capacity $\left(\alpha,h=0\right)$
From class, we could write $F$ in terms of $\mathfrak{L}$ as:
$$\begin{align}
F(t,h)&=\mathfrak{L}\left(\phi(t,h),h,t\right)\\
F(t,0)&=\dfrac{1}{2}bt\phi(t,0)^2+\dfrac{1}{8}d\phi(t,0)^8
\end{align}$$
For $t>0$, we know our field $\phi=0$ (from part A), and so:
$$\begin{align}
F(t,0)&=0 & t>0
\end{align}$$
For $t<0$, we know our field $\phi^2=\left(\dfrac{b}{d}|t|\right)^{1/3}$ (from part A), and so:
$$\begin{align}
F(t,0)&=\dfrac{1}{2}bt\phi(t,0)^2+\dfrac{1}{8}d\phi(t,0)^8\\
&=\dfrac{1}{2}bt\left(\dfrac{b}{d}|t|\right)^{1/3}+\dfrac{1}{8}d\left(\dfrac{b}{d}|t|\right)^{4/3}\\
&=-\dfrac{1}{2}\dfrac{b^{4/3}}{d^{1/3}}|t|^{4/3}+\dfrac{1}{8}\dfrac{b^{4/3}}{d^{1/3}}|t|^{4/3}\\
F(t,0)&=-\dfrac{3}{8}\dfrac{b^{4/3}}{d^{1/3}}|t|^{4/3} \ \ \ \ \ \ t<0
\end{align}$$
Combining, we get:
$$\begin{align}
F(t,0)&=\begin{cases}
0 & t>0\\
-\dfrac{3}{8}\dfrac{b^{4/3}}{d^{1/3}}|t|^{4/3} & t<0\\
\end{cases}
\end{align}$$
The heat capacity is defined as as:
$$\begin{align}
C_{h=0}&=\lim_{h\rightarrow0}T\left(\dfrac{\partial S}{\partial T}\right)_h=\lim_{h\rightarrow0}T\left(\dfrac{\partial}{\partial T}\cdot-\dfrac{\partial F}{\partial T}\right)_h\\
C_{h=0}&=-\lim_{h\rightarrow0}T\left(\dfrac{\partial^2 F}{\partial T^2}\right)_h
\end{align}$$
Using our function from before, we get:
$$\begin{align}
C_{h=0}&=T\begin{cases}
0 & t>0\\
-\dfrac{1}{6}\dfrac{b^{4/3}}{d^{1/3}}|t|^{-2/3} & t<0\\
\end{cases}\\
\end{align}$$
Thus, for the exponents on $|t|$ can be shown to be:
$$\begin{align}
C_{h=0}&\sim0 &\land&& C_{h=0}&\sim|t|^{-\alpha} & \implies && \Aboxed{\alpha_{t>0}&=0\text{ or DNE}}\\
C_{h=0}&\sim|t|^{-2/3} &\land&& C_{h=0}&\sim|t|^{-\alpha} & \implies && \Aboxed{\alpha_{t<0}&=2/3}
\end{align}$$
---
### Question 1.B
In order to determine the critical exponent for the correlation length $\left(\xi\sim |t|^{-\nu}\right)$, obtain a particle differential equation (PDE) for the two-point correlation function $G(\vec{r})$, and then apply a Fourier transform to find $\tilde{G}(\vec{k})$. You can then simply read off the correlation length by dimensional analysis. (Again, above and below $T_c$ for proper treatment is necessary)

Further, employ the susceptibility sum rule (as derived in class/notes) to check that your answer for $\gamma$ in part (A) checks out.

#### Two-Point Correlation Function PDE
We'll need to take the differential with respect to the $h(\vec{r})$ field such that:
$$\begin{align}
\dfrac{\delta}{\delta h(\vec{r}')}\dfrac{\delta\mathfrak{L}}{\delta\phi}
&=\dfrac{\delta}{\delta h(\vec{r}')}\left(\lambda\nabla^4\phi(\vec{r})+bt\phi(\vec{r})+d\phi(\vec{r})^7-h(\vec{r})\right)\\
&=\lambda\nabla^4\dfrac{\delta\phi(\vec{r})}{\delta h(\vec{r}')}+bt\dfrac{\delta\phi(\vec{r})}{\delta h(\vec{r}')}+d\dfrac{\delta\phi(\vec{r})^7}{\delta h(\vec{r}')}-\dfrac{\delta h(\vec{r})}{\delta h(\vec{r}')}
\end{align}$$
At the equilibrium condition $\dfrac{\delta\mathfrak{L}}{\delta\phi}=0$ and $h(\vec{r})=H$, then it simplifies to:
$$\begin{align}
\lambda\nabla^4\dfrac{\delta\phi(\vec{r})}{\delta h(\vec{r}')}+bt\dfrac{\delta\phi(\vec{r})}{\delta h(\vec{r}')}+7d\phi(\vec{r})^6\dfrac{\delta\phi(\vec{r})}{\delta h(\vec{r}')}-\dfrac{\delta h(\vec{r})}{\delta h(\vec{r}')}
&=\dfrac{\delta}{\delta h(\vec{r}')}\dfrac{\delta\mathfrak{L}}{\delta\phi}\\\\
\left(\lambda\nabla^4+bt+7d\phi^6\right)\chi(\vec{r},\vec{r}')-\delta(\vec{r}-\vec{r}')&=0\\
\Aboxed{\left(\lambda\nabla^4+bt+7d\phi^6\right)\chi(\vec{r},\vec{r}')&=\delta(\vec{r}-\vec{r}')}
\end{align}$$
This is just a differential equation in the form of a Green's function. From my notes, magnetic susceptibility and the Green's function are scalar multiples of each other, and so:
$$\begin{align}
\Aboxed{\left(\lambda\nabla^4+bt+7d\phi^6\right)G(\vec{r}-\vec{r}')&=kT\delta(\vec{r}-\vec{r}')}\\
\left(\nabla^4+\dfrac{bt}{\lambda}+\dfrac{7d}{\lambda}\phi^6\right)G(\vec{r}-\vec{r}')&=\dfrac{kT}{\lambda}\delta(\vec{r}-\vec{r}')\\
\end{align}$$
<div style="page-break-before: always;"></div>






#### Correlation Lengths
For $t>0$, we know our field $\phi=0$ (from part A), and so:
$$\begin{align}
\left(\nabla^4+\dfrac{bt}{\lambda}\right)G(\vec{r}-\vec{r}')&=\dfrac{kT}{\lambda}\delta(\vec{r}-\vec{r}')
\end{align}$$
Like you said about dimensional analysis, we expect that:
$$\begin{align}
\Aboxed{\xi(t)&=\sqrt[4]{\dfrac{\lambda}{bt}}\ \ \ \ \ \ t>0}
\end{align}$$
For $t<0$, we know our field $\phi^6=\dfrac{b}{d}|t|$ (from part A), and so:
$$\begin{align}
\left(\nabla^4-\dfrac{b|t|}{\lambda}+\dfrac{b}{d}|t|\dfrac{7d}{\lambda}\right)G(\vec{r}-\vec{r}')&=\dfrac{kT}{\lambda}\delta(\vec{r}-\vec{r}')\\
\left(\nabla^4+\dfrac{6b|t|}{\lambda}\right)G(\vec{r}-\vec{r}')&=\dfrac{kT}{\lambda}\delta(\vec{r}-\vec{r}')
\end{align}$$
Through similar dimensional analysis, we expect that:
$$\begin{align}
\Aboxed{\xi(t)&=\sqrt[4]{\dfrac{\lambda}{6b|t|}}\ \ \ \ \ \ t<0}
\end{align}$$
The correlation function for both sides of $t=0$ is then:
$$\begin{align}
\xi(t)&=\begin{cases}
\sqrt[4]{\dfrac{\lambda}{b|t|}} & t>0\\
\sqrt[4]{\dfrac{\lambda}{6b|t|}} & t<0\\
\end{cases}
\end{align}$$
#### Fourier Transform of Two-Point Correlation Function
If we apply the Fourier transform to this PDE, we find that:
$$\begin{align}
\left(\nabla^4+\xi^{-4}(t)\right)G(\vec{r}-\vec{r}')&=\dfrac{kT}{\lambda}\delta(\vec{r}-\vec{r}') & \implies &&\left(\vec{k}^4+\xi^{-4}(t)\right)\tilde{G}(\vec{k})&=\dfrac{kT}{\lambda}\cdot1
\end{align}$$
Rearranging for the Green's Function, we see:
$$\begin{align}
\Aboxed{\tilde{G}(\vec{k})&=\dfrac{kT}{\lambda}\dfrac{1}{\vec{k}^4+\xi^{-4}(t)}}
\end{align}$$
<div style="page-break-before: always;"></div>





#### Susceptibility Sum Rule
Using the expression we have from class, the susceptibility can be found as:
$$\begin{align}
\chi_T&=\dfrac{1}{kT}\int G(\vec{r})\ d^dr\\
&=\dfrac{1}{kT}\lim_{\vec{k}\rightarrow0}\tilde{G}(\vec{k})\\
&=\dfrac{1}{kT}\lim_{\vec{k}\rightarrow0}\dfrac{kT}{\lambda}\dfrac{1}{\vec{k}^4+\xi^{-4}(t)}\\
&=\dfrac{1}{\lambda}\xi^{4}(t)\\
\chi_T&=\dfrac{1}{b}|t|^{-1}\begin{cases}
1 & t>0\\
1/6 & t<0\\
\end{cases}
\end{align}$$
From here it's very clear to see that this recovers $\boxed{\gamma=1}$

---
### Question 1.C
Are these results that you obtained above expected to be valid in three dimensions?
(I.e. use the Ginzburg criterion applied to this Landau free-energy density to determine the upper critical dimension for this model).

For reference, in part A we found that:
$$\begin{align}
\beta&=\dfrac{1}{6} & \delta&=7 & \gamma&=1 & \alpha_{t>0}&=0 & \alpha_{t<0}&=2/3
\end{align}$$
The critical dimension is written as, and so:
$$\begin{align}
d_c&=\dfrac{\gamma+2\beta}{\nu}=\dfrac{1+2\cdot\tfrac{1}{6}}{\tfrac{1}{2}}=2+\dfrac{2}{3}
\end{align}$$
For this model, all dimensions $\boxed{d\ge3}$ should work well in the mean field limit.
So a three-dimensional space would have this model work just fine.

---
<div style="page-break-before: always;"></div>




## Question 2
Consider the ferromagnetic Ising model on a *star-like network* of $N$ nodes.
I.e. $N-1$ nodes are connected to the center one with a coupling constant $-J$.
The external field $H$ is the same for all spins.

---
### Question 2.A
Write down the Hamiltonian for this system.
$$\begin{align}
\Aboxed{\mathcal{H}&=-J\sum_{i=2}^Ns_1s_i-H\sum_{i=1}^Ns_i}
\end{align}$$
Where $s_1$ is defined to be the central spin of the system. Alternatively, we can write it as:
$$\begin{align}
\mathcal{H}&=-Hs_1-(Js_1+H)\sum_{i=2}^Ns_i
\end{align}$$
This will turn out to be easier later, but I will choose to reindex so that:
$$\begin{align}
\mathcal{H}&=-Hs_0-(Js_0+H)\sum_{i=1}^{N'}s_i & N'&=N-1
\end{align}$$
---
<div style="page-break-before: always;"></div>




### Question 2.B
Calculate the partition function $\mathcal{Z}_N(K,h)$, where $K=\beta J$, $h=\beta H$, and $\beta=1/kT$.
$$\begin{align}
\mathcal{Z}_N(K,h)&=\sum_{\{s_i\}}e^{-\beta\mathcal{H}[\{s_i\}]}\\
&=\sum_{\{s_i\}}e^{-\beta\left(-Hs_0-(Js_0+H)\sum_{i=1}^{N'}s_i\right)}\\
&=\sum_{\{s_i\}}e^{\beta Hs_0+(\beta Js_0+\beta H)\sum_{i=1}^{N'}s_i}\\
\mathcal{Z}_N(K,h)&=\sum_{\{s_i\}}e^{hs_0+(Ks_0+h)\sum_{i=1}^{N'}s_i}\\
\end{align}$$
To solve this analytically (brute-force), since $s_i=\pm1$, energies are akin to binary, and so we can exploit combinatorics to solve this system. Denote $n_k$ as the number of microstates of $k$ up spins (ignoring $s_0$) are pointing up in a particular microstate, and $E_k$ as the energy of this macro-state.
$$\begin{align}
n_k&=\dfrac{1}{k!}\dfrac{N'!}{(N'-k)!} & E_k&=-(Ks_0+h)(N'-2k)=(Ks_0+h)\sum_{i=1}^{N'}s_i
\end{align}$$
Some examples are as follow (as much for you as for me):
$$\begin{align}
n_0&=1 & E_k&=-N'(Ks_0+h) && \text{All Spin Down}\\
n_1&=N' & E_k&=-(N'-2)(Ks_0+h) && \text{Singular Up State}\\
\vdots\\
n_{N'/2}&=\dfrac{N'!}{(N'/2)!^2} & E_k&=0 && \text{Equal Shares of Spins}\\
\end{align}$$
We can rewrite the partition function in terms of this macro-state interpretation:
$$\begin{align}
\mathcal{Z}_N(K,h)&=\sum_{s_0=\pm1}e^{hs_0}\sum_{k=0}^{N'}\dfrac{1}{k!}\dfrac{N'!}{(N'-k)!}e^{-(Ks_0+h)(N'-2k)}\\
&=\sum_{s_0=\pm1}e^{hs_0}\sum_{k=0}^{N'}\dfrac{1}{k!}\dfrac{N'!}{(N'-k)!}\left(e^{-(Ks_0+h)}\right)^{N'-k}\left(e^{+(Ks_0+h)}\right)^{k}\\
&=\sum_{s_0=\pm1}e^{hs_0}\left(e^{-(Ks_0+h)}+e^{+(Ks_0+h)}\right)^{N'}\\
&=\sum_{s_0=\pm1}2^{N'}e^{hs_0}\cosh\left(Ks_0+h\right)^{N'}\\
&=2^{N'}e^{h}\cosh\left(K+h\right)^{N'}+2^{N'}e^{-h}\cosh\left(-K+h\right)^{N'}\\
\Aboxed{\mathcal{Z}_N(K,h)&=2^{N-1}\left(e^{h}\cosh\left(K+h\right)^{N-1}+e^{-h}\cosh\left(K-h\right)^{N-1}\right)}
\end{align}$$
---
<div style="page-break-before: always;"></div>





### Question 2.C
Obtain the free energy per spin in the thermodynamic limit, i.e.
$$\begin{align}
f(K,h)&=-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln\mathcal{Z}_N(K,h)
\end{align}$$
Taking the limit properly is the essence of this problem. The sign of $h$ does matter, so you should carefully examine the two cases when $h>0$ and $h<0$.

Suppose $h>0$:
$$\begin{align}
f(K,h)&=-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln\mathcal{Z}_N(K,h)\\
&=-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln2^{N-1}-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln\left(e^{h}\cosh\left(K+h\right)^{N-1}+e^{-h}\cosh\left(K-h\right)^{N-1}\right)\\
&\approx-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{N-1}{N}\ln2-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln\left(e^{h}\cosh\left(K+h\right)^{N-1}\right)\\
&=-\dfrac{1}{\beta}\ln2-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln\left(e^{h}\right)-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{N-1}{N}\ln\cosh\left(K+h\right)\\
&=-\dfrac{1}{\beta}\ln2-\dfrac{1}{\beta}\ln\cosh\left(K+h\right)\\
\Aboxed{f(K,h)&\approx-\dfrac{1}{\beta}\ln\left[2\cosh\left(K+h\right)\right],\ \ \ \ \ h>0}
\end{align}$$
Suppose $h<0$:
$$\begin{align}
f(K,h)&=-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln\mathcal{Z}_N(K,h)\\
&=-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln2^{N-1}-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln\left(e^{h}\cosh\left(K+h\right)^{N-1}+e^{-h}\cosh\left(K-h\right)^{N-1}\right)\\
&\approx-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{N-1}{N}\ln2-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln\left(e^{-h}\cosh\left(K-h\right)^{N-1}\right)\\
&=-\dfrac{1}{\beta}\ln2-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{1}{N}\ln\left(e^{-h}\right)-\dfrac{1}{\beta}\lim_{N\rightarrow\infty}\dfrac{N-1}{N}\ln\cosh\left(K-h\right)\\
&=-\dfrac{1}{\beta}\ln2-\dfrac{1}{\beta}\ln\cosh\left(K-h\right)\\
\Aboxed{f(K,h)&\approx-\dfrac{1}{\beta}\ln\left[2\cosh\left(K-h\right)\right],\ \ \ \ \ h<0}
\end{align}$$
We can then express it over its full domain as:
$$\begin{align}
\Aboxed{f(K,h)&=-\dfrac{1}{\beta}\ln\left[2\cosh\left(K+|h|\right)\right]}
\end{align}$$
The free energy per spin is agnostic to the direction of the magnetic field, which makes sense since reversing all the spins and the field should lead to the same system.






### Question 2.D
Find the average magnetization per spin $m(K,h)$. Now take the limits when $h\rightarrow\pm0$, i.e. obtain the expression for the spontaneous magnetization of the start network system. Sketch $m$ vs $h$ for fixed $K\ne0$ and also for $K=0$.

Average magnetization is simply expressed as:
$$\begin{align}
m(K,h)&=-\left(\dfrac{\partial f}{\partial H}\right)_T=-\beta\left(\dfrac{\partial f}{\partial h}\right)_K\\
&=-\beta\dfrac{\partial}{\partial h}\left(-\dfrac{1}{\beta}\ln\left[2\cosh\left(K+|h|\right)\right]\right)\\
&=\dfrac{\partial}{\partial h}\left(\ln\left[2\cosh\left(K+|h|\right)\right]\right)\\
&=\dfrac{1}{2\cosh\left(K+|h|\right)}\dfrac{\partial}{\partial h}\left(2\cosh\left(K+|h|\right)\right)\\
&=\dfrac{2\sinh\left(K+|h|\right)}{2\cosh\left(K+|h|\right)}\dfrac{\partial}{\partial h}\left(K+|h|\right)\\
\Aboxed{m(K,h)&=\tanh\left(K+|h|\right)\ \text{sign}(h)}
\end{align}$$
For the limit of $h\rightarrow\pm0$, the magnetization becomes:
$$\begin{align}
\lim_{m\rightarrow0^{\pm}}m(K,h)&=\lim_{m\rightarrow0^{\pm}}\tanh\left(K+|h|\right)\ \text{sign}(h)\\
&=\tanh\left(K+0\right)\lim_{m\rightarrow0^{\pm}}\text{sign}(h)\\
\Aboxed{m(K,0^{\pm})&=\pm\tanh\left(K\right)}
\end{align}$$
Graphically, we can see:
![[question_2D.png]]
For $K\ne0$, there is a discontinuity in the magnetization since there is a preference for spins to align with each other. At $K=0$, they no longer interact, and thus align with the magnetic field.

---
### Question 2.E
Obtain the Isotherm susceptibility $\chi_T=\left(\dfrac{\partial m}{\partial H}\right)_T=\beta\left(\dfrac{\partial m}{\partial h}\right)_K$. Take the $h\rightarrow\pm0$ limits, and sketch your analytical result $\chi_T$ vs $T$.

Just another differential to calculate:
$$\begin{align}
\chi_T(K,h)&=\left(\dfrac{\partial m}{\partial H}\right)_T=\beta\left(\dfrac{\partial m}{\partial h}\right)_K\\
&=\beta\dfrac{\partial}{\partial h}\left(\tanh\left(K+|h|\right)\ \text{sign}(h)\right)\\
&=\beta\ \text{sech}^2\left(K+|h|\right)\dfrac{\partial}{\partial h}\left(K+|h|\right)\text{sign}(h)\\
&=\beta\ \text{sech}^2\left(K+|h|\right)\ \text{sign}(h)^2\\
\Aboxed{\chi_T(K,h)&=\beta\ \text{sech}^2\left(K+|h|\right)}
\end{align}$$
For the limit of $h\rightarrow\pm0$, the susceptibility becomes:
$$\begin{align}
\lim_{m\rightarrow0^{\pm}}\chi_T(K,h)&=\lim_{m\rightarrow0^{\pm}}\beta\ \text{sech}^2\left(K+|h|\right)\\
\Aboxed{\chi_T(K,0^{\pm})&=\beta\ \text{sech}^2\left(K\right)}
\end{align}$$
Graphically, we can see:
![[question_2E.png]]
The magnetic susceptibility is independent of the direction of the magnetic field, which makes sense, since it only should depend on the magnitude of the field in the $z$ axis. Moreover, we see that there is no susceptibility at $T=0$ for either system. Strongly-coupled particle won't be effected much by an external magnetic field, even at $T=0$, and only in the case that $J=0$ do we see a discontinuity (infinite susceptibility) since the particles are non-interacting.

---
<div style="page-break-before: always;"></div>




## Question 3
In this problem, you will consider the *renormalization of the external field $h$ in the two-dimensional Ising model on a triangular lattice* (i.e. continue to use the framework we have developed in class/notes). It turns out that to obtain the effect of the RG on the external field (in the crudest approximation), we can consider the 0th-order in the potential $V$ (where the potential $V$ including the inter-block contribution of the nearest-neighbor spin-spin coupling).

Using the real-space renormalization group framework from class (i.e. performing the partial summations over the original local spin variables to obtain the renormalized block-spin Hamiltonian), we have
$$\begin{align}
e^{\mathcal{H}'[\{s_I\}]}&=\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]}\\
\end{align}$$
where $\sum_{\{s_i\}}'(\dots)$ is the partial summation using the "majority-rule" on the triangular lattice as developed and employed in class/notes. Capturing the effects of the change in the external field under renormalization, we also have:
$$\begin{align}
e^{\mathcal{H}'[\{s_I\}]+\delta\mathcal{H}'[\{s_I\}]}&=\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]+\delta \mathcal{H}[\{s_i\}]}\\
\delta\mathcal{H}[\{s_I\}]&=\delta h\sum_{i}S_i=\delta h\sum_{I}\sum_{i\in I}S^I_i\\
\delta\mathcal{H}'[\{s_I\}]&=\delta h'\sum_{I}S^I\\
\end{align}$$
(In the notation above, $\delta h=h-h^*$) and $\delta h'=h'-h^*$, and we know that $h^*=0$.)
Since we are considering the RG flow in the vicinity of the critical point, both $\delta h$ and $\delta h'$, and in turn, $\delta H$ and $\delta H'$ are small.

---
### Question 3.A
Combining Eqs. (1) and (2) in this limit, show that:
$$\begin{align}
\delta\mathcal{H}'[\{s_I\}]&\approx\dfrac{\sum'_{\{s_i\}}e^{\mathcal{H}[\{s_i\}]}\ \delta\mathcal{H}[\{s_i\}]}{\sum'_{\{s_i\}}e^{\mathcal{H}[\{s_i\}]}}=\braket{\delta\mathcal{H}[\{s_i\}]}
\end{align}$$
where $\mathcal{H}[\{s_i\}]=K\sum_{\braket{i,j}}S_iS_j$, the Hamiltonian in zero field. Employing the same decomposition to intra- and inter-block couplings as in class/notes, to 0th order of the inter-block couplings, eq. (3) becomes:
$$\begin{align}
\delta\mathcal{H}'[\{s_I\}]\approx\braket{\delta\mathcal{H}[\{s_i\}]}_o
\end{align}$$
where now the "partial average" $\braket{\dots}_o$ is taken, using the intra-block Hamiltonian, $\mathcal{H}_0[\{s_i\}]=K\sum_{I}\sum_{i,j\in I}S_iS_j$, as defined in class/notes, and $K=K^*$ (where $e^{4K^*}=1+2\sqrt{2}$ as obtained in class for the critical RG fixed point for $K$).

We can exploit these small variations to expand around the original Hamiltonian as:
$$\begin{align}
e^{\mathcal{H}'[\{s_I\}]+\delta\mathcal{H}'[\{s_I\}]}&=\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]+\delta \mathcal{H}[\{s_i\}]}\\
e^{\mathcal{H}'[\{s_I\}]}\left(1+\delta\mathcal{H}'[\{s_I\}]+\dots\right)&=\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]}\left(1+\delta\mathcal{H}[\{s_i\}]+\dots\right)\\
e^{\mathcal{H}'[\{s_I\}]}+e^{\mathcal{H}'[\{s_I\}]}\delta\mathcal{H}'[\{s_I\}]&\approx\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]}+\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]}\delta\mathcal{H}[\{s_i\}]
\end{align}$$
Using the relation:
$$\begin{align}
e^{\mathcal{H}'[\{s_I\}]}&=\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]}\\
\end{align}$$
This summation simplifies to (in the limit as $\delta\rightarrow0$):
$$\begin{align}
e^{\mathcal{H}'[\{s_I\}]}+e^{\mathcal{H}'[\{s_I\}]}\delta\mathcal{H}'[\{s_I\}]&=\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]}+\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]}\delta\mathcal{H}[\{s_i\}]\\
\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]}\delta\mathcal{H}'[\{s_I\}]&=\sum_{\{s_i\}}'e^{\mathcal{H}[\{s_i\}]}\delta\mathcal{H}[\{s_i\}]\\
\Aboxed{\delta\mathcal{H}'[\{s_I\}]&=\dfrac{\sum'_{\{s_i\}}e^{\mathcal{H}[\{s_i\}]}\delta\mathcal{H}[\{s_i\}]}{\sum'_{\{s_i\}}e^{\mathcal{H}[\{s_i\}]}}}
\end{align}$$
This is also an expected value term, and so we can write the final result:
$$\begin{align}
\Aboxed{\delta\mathcal{H}'[\{s_I\}]&=\dfrac{\sum'_{\{s_i\}}e^{\mathcal{H}[\{s_i\}]}\delta\mathcal{H}[\{s_i\}]}{\sum'_{\{s_i\}}e^{\mathcal{H}[\{s_i\}]}}=\braket{\delta\mathcal{H}[\{s_i\}]}}
\end{align}$$
---
### Question 3.B
Using the above guidance, obtain the RG eigenvalue $\Lambda_h$ and the exponent $y_h$ ($\Lambda_h=l^{y_h}$) associated with the external field $h$.

My notes on this part aren't as good as my other sections, so I'll try my best here. Starting with:
$$\begin{align}
\delta\mathcal{H}'[\{s_I\}]&\approx\braket{\delta\mathcal{H}[\{s_i\}]}_o\\
\delta\mathcal{H}[\{s_I\}]&=\delta h\sum_{i}S_i=\delta h\sum_{I}\sum_{i\in I}S^I_i\\
\delta\mathcal{H}'[\{s_I\}]&=\delta h'\sum_{I}S^I
\end{align}$$
From the first equation with the second equation, we get (with majority rule):
$$\begin{align}
\delta\mathcal{H}'[\{s_I\}]&\approx\left\langle\delta h\sum_{I}\sum_{i\in I}S^I_i\right\rangle_o\approx\delta h\sum_{I}\left\langle\sum_{i\in I}S^I_i\right\rangle_o
\end{align}$$
$$\begin{align}
\left\langle\sum_{i\in I}S^I_i\right\rangle_o
&=\dfrac{\sum(s_1+s_2+s_3)e^{K^*(s_1s_2+s_2s_3+s_3s_1)}}{\sum e^{K^*(s_1s_2+s_2s_3+s_3s_1)}}\\
&=\dfrac{(\pm3)e^{K^*(+3)}+3(\pm1)e^{K^*(-1)}}{e^{K^*(+3)}+3e^{K^*(-1)}}\\
\left\langle\sum_{i\in I}S^I_i\right\rangle_o&=3\ \text{sign}(S^I)\cdot\dfrac{e^{3K^*}+e^{-K^*}}{e^{3K^*}+3e^{-K^*}}\\
\end{align}$$
From above, we can also see that:
$$\begin{align}
\delta h'\sum_{I}S^I&\approx\delta h\sum_{I}\left\langle\sum_{i\in I}S^I_i\right\rangle_o\\
\sum_{I}\delta h'\cdot S^I&\approx\sum_{I}\delta h\cdot3\ \text{sign}(S^I)\cdot\dfrac{e^{3K^*}+e^{-K^*}}{e^{3K^*}+3e^{-K^*}}\\
\delta h'\cdot S^I&\approx\delta h\cdot S^I\dfrac{e^{3K^*}+e^{-K^*}}{e^{3K^*}+3e^{-K^*}}\\
\Aboxed{\dfrac{\delta h'}{\delta h}&\approx\dfrac{e^{3K^*}+e^{-K^*}}{e^{3K^*}+3e^{-K^*}}}
\end{align}$$
I didn't find it in my notes, but I do remember this ratio being $\Lambda_h$, or at least proportional to it:
$$\begin{align}
\dfrac{\delta h'}{\delta h}&\approx\dfrac{e^{3K^*}+e^{-K^*}}{e^{3K^*}+3e^{-K^*}}\cdot\dfrac{e^{K^*}}{e^{K^*}}\\
&=\dfrac{e^{4K^*}+1}{e^{4K^*}+3}\\
&\approx\dfrac{(1+2\sqrt{2})+2}{(1+2\sqrt{2})+3}\\
\Lambda_h^{-1}&=\dfrac{2+2\sqrt{2}}{4+2\sqrt{2}}\\
\Aboxed{\Lambda_h&=\sqrt{2}}
\end{align}$$
I had to look back at the lecture, but our length $l=\sqrt{3}$, and so:
$$\begin{align}
\Lambda_h&=l^{y_h} &\implies&& \Aboxed{y_h&=\dfrac{\ln\Lambda_h}{\ln l}=\dfrac{\ln\sqrt{2}}{\ln\sqrt{3}}\approx 0.6309\dots}
\end{align}$$
