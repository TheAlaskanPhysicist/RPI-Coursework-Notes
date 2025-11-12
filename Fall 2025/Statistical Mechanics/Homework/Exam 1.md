Author: Stanley Goodwin
Date: November 11th, 2025

---
## Question 1
This is a (mostly) **numerical/computational exercise** testing the Central Limit Theorem (CLT). You have to use, employ, write, code, etc. your own worksheet or code (using Matlab, Maple, Mathematica, Python, C, C++, etc.) and generate your own data and prepare your own plots. 

Consider $N$ random variables with **uniform distribution** in the $(0,1)$ interval, $x_i\in U(0,1), i\in\left\{1,2,\dots,N\right\}$.

**Disclaimer:** I did use Numpy Docs in my IDE (PyCharm) in order to know the available functions since the manual Python implementations were *really* slow.

---
### Question 1.I
Generate the sum of $N=100$ *independent* uniformly random variables on $(0,1)$:
$$\begin{align}
y_N&=x_1+x_2+\dots+x_N
\end{align}$$
I.e. $x_i$ is sampled from the uniform distribution on interval $(0,1)$.

Generate $M=10^6$ datapoints that sample $y_N$, denoted as $\left\{y_{N,j}\right\}_{j=1}^M$.

We have the probability density function:
$$\begin{align}
\rho_1(x)&=\begin{cases}1& 0\lt x\lt 1\\0&\text{otherwise}\end{cases}
\end{align}$$
---
<div style="page-break-before: always;"></div>



#### Question 1.I.A
Numerically estimate the mean of $y_N$ using $\left\{y_{N,j}\right\}_{j=1}^M$.
$$\begin{align}
\bar{y}_{N,M}&=\dfrac{1}{M}\sum_{j=1}^M y_{N,j}
\end{align}$$
Then calculate $\mu_{y_N}$ (the population mean) using the individual independent variables $x_i\in U(0,1)$.
Compare $\bar{y}_{N,M}$ to $\mu_{y_N}$ (express $\bar{y}_{N,M}|\mu_{y_N}$ in terms of $N$ and $\bar{x}|\mu_x$ respectively).

**Numerically Approximating** $\bar{y}_{N,M}$
I used the following lambda expression for calculating a single sample of $y_N$:
```python
# Generate a random number uniformly distributed between 0 and 1  
import numpy as np  
y_N = lambda n: sum(np.random.rand() for _ in range(n))
```
I ran this for a million iterations, then found the mean with the following:
```python
N, M = 100, 1_000_000  
y_N_mean = sum(y_N(N) for _ in range(M)) / M

# Much faster implementation used later as well
N, M = 100, 1_000_000
y_N_values = np.sum(np.random.rand(M, N), axis=1)  # List of y values
y_N_variance = y_N_values.mean()                   # Built-In mean function
```
It took 1 minutes 20 seconds to calculate, but the value I achieved was:
$$\begin{align}
\Aboxed{\bar{y}_{100,10^6}&=50.002242395999104}
\end{align}$$
To mention, the `np.random.rand()` returns values $x_i\in[0,1)$, but the contribution from 0 is so small that it doesn't change the outcome.
<div style="page-break-before: always;"></div>

**Analytically Constructing** $\mu_{y_N}$
The expected value of a single $x_i$ is:
$$\begin{align}
\mathbb{E}[x]&=\int_{-\infty}^\infty x\rho_1(x)\ dx=\int_{-\infty}^0 0\ dx+\int_{0}^1 x\ dx+\int_{1}^\infty 0\ dx=0+\left.\dfrac{x^2}{2}\right|_{0}^1+0\\
\Aboxed{\mathbb{E}[x]&=\dfrac{1}{2}}
\end{align}$$
Since are independent variables of each other, then:
$$\begin{align}
\mathbb{E}[y]&=\sum_{i=1}^N\mathbb{E}[x_i] &\implies&& \Aboxed{\mu_{y_N}&=\dfrac{1}{2}N}
\end{align}$$
For our case of $N=100$, we expect:
$$\begin{align}
\Aboxed{\mu_{y_{100}}&=50} & \Aboxed{\bar{y}_{100,10^6}&=50.0022\dots}
\end{align}$$
This is almost exactly what we got for the random samples we got from coding it up.
See Appendix 1 for the derivation of the true distribution.

---
#### Question 1.I.B
Numerically estimate the variance of $y$ using $\left\{y_j\right\}_{j=1}^M$.
$$\begin{align}
s_{y_{N,M}}^2&=\dfrac{1}{M-1}\sum_{j=1}^M (y_{N,j}-\bar{y}_{N,M})^2\approx\dfrac{1}{M}\sum_{j=1}^M (y_{N,j}-\bar{y}_{N,M})^2
\end{align}$$
Then calculate $\sigma^2_{y_{N}}$ (the population variance) using the individual independent variables.
Compare $s^2_{y_{N,M}}$ to $\sigma^2_{y_{N}}$ (express $s^2_{y_{N,M}}|\sigma^2_{y_{N}}$ in terms of $N$ and $s_x^2|\sigma_x^2$ respectively).

**Numerically Approximating** $s_{y_{N,M}}^2$
We initialize a list of values as:
```python
import numpy as np  
N, M = 100, 1_000_000  
y_N_values = np.sum(np.random.rand(M, N), axis=1)  # List of y values
y_N_variance = y_N_values.var()                    # Built-In variance function
```
It took less than a second to calculate, but the value I found was:
$$\begin{align}
\Aboxed{s_{y_{N,M}}^2&=8.331946615495198}
\end{align}$$

<div style="page-break-before: always;"></div>
**Analytically Constructing** $\sigma^2_{y_{N}}$
The expected value of a single $x_i^2$ is:
$$\begin{align}
\mathbb{E}[x^2]&=\int_{-\infty}^\infty x^2\rho_1(x)\ dx=\int_{-\infty}^0 0\ dx+\int_{0}^1 x^2dx+\int_{1}^\infty 0\ dx=0+\left.\dfrac{x^3}{3}\right|_{0}^1+0\\
\Aboxed{\mathbb{E}[x^2]&=\dfrac{1}{3}}
\end{align}$$
$$\begin{align}
\sigma^2_{x}&=\mathbb{E}[x^2]-\mathbb{E}[x]^2=\dfrac{1}{3}-\left(\dfrac{1}{2}\right)^2=\dfrac{4}{3\cdot4}-\dfrac{3}{4\cdot3}\\
\Aboxed{\sigma^2_{x}&=\dfrac{1}{12}}
\end{align}$$
Since are independent variables of each other, then in the CLT limit:
$$\begin{align}
\sigma^2_{y_{N}}&=\sum_{i=1}^N\sigma^2_{x_i}\\
\Aboxed{\sigma^2_{y_{N}}&=\dfrac{1}{12}N}
\end{align}$$
For our case of $N=100$, we expect:
$$\begin{align}
\Aboxed{\sigma^2_{y_{N}}&=8.333\bar{3}} & \Aboxed{s_{y_{N,M}}^2&=8.3319\dots}
\end{align}$$
This is almost exactly what we got for the random samples.


#### Question 1.I.C
Construct a normalized histogram (say using $B=50$ bins between $[y_\text{min}, y_\text{max}]$ with bin size $\Delta y=(y_\text{max}-y_\text{min})/B$) using your raw data $\left\{y_j\right\}_j^M$. From your histogram, construct a normalized probability density $p_N(y)$ (see part II for what graphs to plot).

After going through all the data, it gave the following output:
![[1.I.C.png]]
I'm not sure how well the colors will come out, so I will explain:
The histogram well matches the Gaussian I plotted from the theoretical values.

---
### Question 1.II
Perform and repeat the above procedure (I.e. I.a and I.b) for three more different values of the "system size", $N=200,400,1000$. I.e. you have now performed a statistical analysis for four system sizes $N=100,200,400,1000$.

---
<div style="page-break-before: always;"></div>

#### Question 1.II.A
Prepare a table for $\bar{y}_N$ and $\sigma_{y,N}=\sqrt{\sigma_{y,N}^2}$ (see below) with both numerical and analytic results for different $N$ values. Then plot $\bar{y}$ and $\sigma_{y,N}=\sqrt{\sigma_{y,N}^2}$ separately (put numerical and analytic results on the same graph) as a function of the system size $N$ (in subscripts I refer to the system size dependence of these quantities). Obviously, you should have 4 data points for each quantity.

| $N$    | $\bar{y}_N$ (Numerical) | $\bar{y}_N$ (Analytic) | $\sigma_{y,N}$ (Numerical) | $\sigma_{y,N}$ (Analytic)    |
| ------ | ----------------------- | ---------------------- | -------------------------- | ---------------------------- |
| $100$  | $49.9961\dots$          | $100/2=50$             | $2.8856\dots$              | $\sqrt{100/12}\approx2.887$  |
| $200$  | $99.9985\dots$          | $200/2=100$            | $4.0813\dots$              | $\sqrt{200/12}\approx4.082$  |
| $400$  | $199.9999\dots$         | $400/2=200$            | $5.7705\dots$              | $\sqrt{400/12}\approx5.774$  |
| $1000$ | $500.0035\dots$         | $1000/2=500$           | $9.1292\dots$              | $\sqrt{1000/12}\approx9.129$ |
The code to get the numerical values is identical to the previous section, just changing $N$ in $y$.
```python
# Means for different N  
print(f"N = 100: ", np.sum(np.random.rand(1_000_000, 100), axis=1).mean())  
print(f"N = 200: ", np.sum(np.random.rand(1_000_000, 200), axis=1).mean())  
print(f"N = 400: ", np.sum(np.random.rand(1_000_000, 400), axis=1).mean())  
print(f"N = 1000: ", np.sum(np.random.rand(1_000_000, 1000), axis=1).mean())  
  
# Standard deviations for different N  
print(f"N = 100: ", np.sum(np.random.rand(1_000_000, 100), axis=1).std())  
print(f"N = 200: ", np.sum(np.random.rand(1_000_000, 200), axis=1).std())  
print(f"N = 400: ", np.sum(np.random.rand(1_000_000, 400), axis=1).std())  
print(f"N = 1000: ", np.sum(np.random.rand(1_000_000, 1000), axis=1).std())
```
After some more code, here's the results I got in plot form:
![[1.II.A.1.png]]
![[1.II.A.2.png]]
If the colors are hard to see, it's because they're overlapping. What we can see is that both distributions match up extremely well. The mean seems to be linear (as expected) and the standard deviation takes on a $\sqrt{N}$ distribution.

---
<div style="page-break-before: always;"></div>

#### Question 1.II.B
Plot the normalized probability densities $p_N(y)$ on the same graph for the four system sizes ($N=100,200,400,1000$). Must attach the plot, have axis labels, axis scales, and legends indicating which data points are for which $N$.

While you had mentioned to have $50$ bins, it got worse and worse resolution as I went out, so I didn't force the range on it, and so the bins are only over the point that actually exist.
![[1.II.B.1.png]]
There are 4 different distributions, in order of Red, Green, Blue, Orange corresponding to $N=100,200,400,1000$ respectively. I also plotted 4 darker versions with the true Gaussian distribution to show how they are very close (hence the dashed lines around the peaks).

---
<div style="page-break-before: always;"></div>

#### Question 1.II.C
Perform the following scaling transformation for each system size:
$$\begin{align}
\tilde{y}_N&=\dfrac{y-\bar{y}}{\sigma_{y,N}} & \tilde{p}_N&=\sigma_{y,N}p_N(y)
\end{align}$$
Plot $\tilde{p}_N(\tilde{y})$ for all four system sizes, again, on the same graph. Also on the same graph, plot an appropriate theoretical model (limit probability density) which is motivated by the CLT. Must attach the plot, have axis labels, axis scales, and legends indicating which data points are for which $N$.
![[1.II.C.1.png]]
I'm not sure how well color will come through, but after scaling the variables appropriately, we get the same distribution, which is expected because we normalized this into a $z$ distribution, and so it should be independent of $N$.

---
<div style="page-break-before: always;"></div>

## Question 2
Consider a cubic volume $V=L^3$ of a classical ideal *monatomic* gas of charged particles *in a uniform electric field* $\vec{E}=-E\hat{z}$. Each atom has mass $m$ and charge $q$. Take the bottom of the container to be $z=0$, and the top to be $z=L$. You should ignore the Coulomb interaction between particles, and ***only include the coupling with the electric field***. Working in the *canonical ensemble*:

To find the electric potential energy, we can see that:
$$\begin{align}
V(z)&=-q\int_{0}^z\vec{E}\cdot\hat{z}\ dz & \implies && \Aboxed{V(z)&=qEz}
\end{align}$$
And thus the Hamiltonian is then:
$$\begin{align}
\Aboxed{\hat{H}&=\sum_{i=1}^{N}\dfrac{\vec{p}_i^2}{2m}+qEz_i}
\end{align}$$
---
<div style="page-break-before: always;"></div>

### Question 2.A
Determine the average *total energy* $U$ and the heat capacity $C_V$ of the system.

Since these particles are independent of each other, and likely indistinguishable, then we can find the partition function of 1 particle, raise it to the power of $N$, and divide by $N!$:
$$\begin{align}
Z_1&=\int e^{-\beta\hat{H}_1}\dfrac{d^{3}p\ d^{3}q}{h^{3}}\\
&=\dfrac{1}{h^3}\int e^{-\beta\vec{p}^2/2m -\beta qEz}d^{3}p\ d^{3}q\\
&=\dfrac{1}{h^3}\int e^{-\beta\vec{p}^2/2m}d^{3}p\int e^{-\beta qEz}dx\ dy\ dz\\
&=\dfrac{1}{h^3}\int_0^\infty e^{-\beta p^2/2m}\ 4\pi p^2dp\cdot L^2\int_0^L e^{-\beta qEz}dz
\end{align}$$
Let $u=\sqrt{\dfrac{\beta}{2m}}p \implies p=\sqrt{\dfrac{2m}{\beta}}u$, $dp=\sqrt{\dfrac{2m}{\beta}}du$, then:
$$\begin{align}
Z_1&=\dfrac{4\pi}{h^3}\int_0^\infty p^2e^{-\beta p^2/2m}\ dp\cdot L^2\int_0^L e^{-\beta qEz}dz\\
&=\dfrac{4\pi}{h^3}\left(\sqrt{\dfrac{2m}{\beta}}\right)^3\cdot\dfrac{1}{2}\int_{-\infty}^\infty u^2e^{-u^2}\ du\cdot L^2\left.\dfrac{e^{-\beta qEz}}{\beta qE}\right|_L^0\\
&=\dfrac{2\pi}{h^3}\left(\sqrt{\dfrac{2m}{\beta}}\right)^3\dfrac{\sqrt{\pi}}{2}\cdot L^2\left(\dfrac{1}{\beta qE}-\dfrac{e^{-\beta qEL}}{\beta qE}\right)\\
&=\dfrac{(2\pi m)^{3/2}}{h^3}\dfrac{L^2}{\beta^{5/2} qE}\left(1-e^{-\beta qEL}\right)\\
\Aboxed{Z_1&=\dfrac{L^2(2\pi m)^{3/2}}{qEh^3}\beta^{-5/2}\left(1-e^{-\beta qEL}\right)}
\end{align}$$
The whole partition function is then:
$$\begin{align}
Z_N&=\dfrac{1}{N!}Z_1^N\\
&=\dfrac{1}{N!}\left[\dfrac{L^2(2\pi m)^{3/2}}{qEh^3}\beta^{-5/2}\left(1-e^{-\beta qEL}\right)\right]^N\\
\Aboxed{Z_N&=\dfrac{1}{N!}\left[\dfrac{L^2(2\pi m)^{3/2}}{qEh^3}\right]^N\beta^{-5N/2}\left(1-e^{-\beta qEL}\right)^N}
\end{align}$$
<div style="page-break-before: always;"></div>

To find the expected value of internal energy:
$$\begin{align}
U&=-\dfrac{\partial}{\partial\beta}\ln Z_N\\
&=-\dfrac{\partial}{\partial\beta}\ln\left(\dfrac{1}{N!}\left[\dfrac{L^2(2\pi m)^{3/2}}{qEh^3}\right]^N\beta^{-5N/2}\left(1-e^{-\beta qEL}\right)^N\right)\\
&=-\dfrac{\partial}{\partial\beta}\left[\ln\left(\dfrac{1}{N!}\left[\dfrac{L^2(2\pi m)^{3/2}}{qEh^3}\right]^N\right)-\dfrac{5}{2}N\ln\left(\beta\right)+N\ln\left(1-e^{-\beta qEL}\right)\right]\\
&=\dfrac{5}{2}N\dfrac{\partial}{\partial\beta}\ln\left(\beta\right)-N\dfrac{\partial}{\partial\beta}\ln\left(1-e^{-\beta qEL}\right)\\
&=\dfrac{5}{2}N\dfrac{1}{\beta}-N\dfrac{1}{1-e^{-\beta qEL}}\dfrac{\partial}{\partial\beta}\left(1-e^{-\beta qEL}\right)\\
&=\dfrac{5}{2}N\dfrac{1}{\beta}-NqEL\dfrac{e^{-\beta qEL}}{1-e^{-\beta qEL}}\\
\Aboxed{U&=\dfrac{5}{2}NkT-\dfrac{NqEL}{e^{qEL/kT}-1}}
\end{align}$$
The heat capacity at constant volume is pretty simple to then calculate:
$$\begin{align}
C_V&=\left(\dfrac{\partial U}{\partial T}\right)_{V,N}\\
&=\dfrac{\partial}{\partial T}\left(\dfrac{5}{2}NkT-\dfrac{NqEL}{e^{qEL/kT}-1}\right)\\
&=\dfrac{5}{2}Nk\dfrac{\partial}{\partial T}\left(T\right)-NqEL\dfrac{\partial}{\partial T}\left(\dfrac{1}{e^{qEL/kT}-1}\right)\\
&=\dfrac{5}{2}Nk+NqEL\dfrac{1}{\left(e^{qEL/kT}-1\right)^2}\dfrac{\partial}{\partial T}\left(e^{qEL/kT}-1\right)\\
&=\dfrac{5}{2}Nk+NqEL\dfrac{1}{\left(e^{qEL/kT}-1\right)^2}e^{qEL/kT}\dfrac{\partial}{\partial T}\left(\dfrac{qEL}{kT}\right)\\
\Aboxed{C_V&=\dfrac{5}{2}Nk-N\dfrac{(qEL)^2}{kT^2}\dfrac{e^{qEL/kT}}{\left(e^{qEL/kT}-1\right)^2}}
\end{align}$$
---
<div style="page-break-before: always;"></div>

### Question 2.B
Study the small-field behavior $\left(\tfrac{EqL}{kT}\ll1\right)$ of $U$. Discuss whether your results.

This small field behavior is equivalent of the fraction approaching zero, so:
$$\begin{align}
U_{E=0}&=\lim_{EqL/kT\rightarrow0}\dfrac{5}{2}NkT-\dfrac{NqEL}{e^{qEL/kT}-1}\\
&=\lim_{EqL/kT\rightarrow0}\dfrac{5}{2}NkT-NkT\dfrac{(qEL/kT)}{e^{qEL/kT}-1}\\
&=\dfrac{5}{2}NkT-NkT\lim_{z\rightarrow0}\dfrac{z}{e^{z}-1}\\
&\approx\dfrac{5}{2}NkT-NkT\lim_{z\rightarrow0}\dfrac{z}{(1+z)-1}\\
&=\dfrac{5}{2}NkT-NkT\lim_{z\rightarrow0}\dfrac{z}{z}\\
\Aboxed{U_{E=0}&=\dfrac{3}{2}NkT}
\end{align}$$
We can show both ways for the heat capacity as well:
$$\begin{align}
C_{V,E=0}&=\lim_{EqL/kT\rightarrow0}\dfrac{5}{2}Nk-N\dfrac{(qEL)^2}{kT^2}\dfrac{e^{qEL/kT}}{\left(e^{qEL/kT}-1\right)^2}\\
&=\dfrac{5}{2}Nk-\lim_{EqL/kT\rightarrow0}Nk\left(\dfrac{qEL}{kT}\right)^2\dfrac{e^{qEL/kT}}{\left(e^{qEL/kT}-1\right)^2}\\
&=\dfrac{5}{2}Nk-Nk\lim_{z\rightarrow0}z^2\dfrac{e^{z}}{\left(e^{z}-1\right)^2}\\
&=\dfrac{5}{2}Nk-Nk\lim_{z\rightarrow0}z^2\dfrac{1+z}{\left((1+z)-1\right)^2}\\
&=\dfrac{5}{2}Nk-Nk\lim_{z\rightarrow0}z^2\dfrac{1+z}{z^2}\\
&=\dfrac{5}{2}Nk-Nk\lim_{z\rightarrow0}(1+z)\\
\Aboxed{C_{V,E=0}&=\dfrac{3}{2}Nk}
\end{align}$$
Or the more simple way:
$$\begin{align}
\Aboxed{C_{V,E=0}&=\left(\dfrac{\partial U_{E=0}}{\partial T}\right)_{V,N}=\dfrac{3}{2}Nk}
\end{align}$$
In the 0-field limit, we'd expect that the system returns to a 3D ideal gas with just the momentum contributions, and so the internal energy and heat capacities should be that of the ideal gas.


<div style="page-break-before: always;"></div>

## Question 3
Consider the non-interacting, *extreme-relativistic* ($\varepsilon(p)=pc$) quantum gas with spin $s$ in a *three-dimensional* box of volume $V$. Working in the grand canonical ensemble:

The energy of a particle in this system is:
$$\begin{align}
\varepsilon_{\vec{k},s}&=\hbar c|\vec{k}|
\end{align}$$
There is no spin dependence, and thus is a degree of freedom of sorts.

The general form of the grand partition function a non-interacting quantum gas is:
$$\begin{align}
Z&=\prod_{\vec{k},s}\dfrac{1}{1\pm e^{-\beta(\varepsilon_{\vec{k},s}-\mu)}} &\implies && \ln Z&=-\sum_{\vec{k},s}\ln\left(1\pm e^{-\beta(\varepsilon_{\vec{k},s}-\mu)}\right)
\end{align}$$
Where I use the top sign as the Fermion, and the lower sign for Boson.
I keep forgetting the convention so I'm outlining it here explicitly.

From Lecture 10, we can then turn it into an integral for the case of a large box ($V^{1/3}\gg1$):
$$\begin{align}
\ln Z&=-\sum_{\vec{k},s}\ln\left(1\pm e^{-\beta(\varepsilon_{\vec{k},s}-\mu)}\right)\\
&=-(2s+1)\left(\dfrac{L}{2\pi}\right)^3\int\ln\left(1\pm e^{-\beta(\varepsilon_{\vec{k},s}-\mu)}\right)\ d^3k\\
&=-(2s+1)\left(\dfrac{L}{2\pi}\right)^3\int_0^\infty\ln\left(1\pm e^{-\beta(\hbar ck-\mu)}\right)\ 4\pi k^2\ dk\\
&=-\dfrac{2s+1}{2\pi^2}V\int_0^\infty k^2\ln\left(1\pm e^{-\beta(\hbar ck-\mu)}\right)\ dk\\
\end{align}$$
<div style="page-break-before: always;"></div>

Also from Lecture 10, we must do an integration by parts:
$$\begin{align}
u&=\ln\left(1\pm e^{-\beta(\hbar ck-\mu)}\right)\\
dv&=k^2 dk
\end{align}$$
We then find:
$$\begin{align}
\ln Z&=-\dfrac{2s+1}{2\pi^2}V\int_0^\infty k^2\ln\left(1\pm e^{-\beta(\hbar ck-\mu)}\right)\ dk\\\\
&=-\dfrac{2s+1}{2\pi^2}V\left.\dfrac{k^3}{3}\ln\left(1\pm e^{-\beta(\hbar ck-\mu)}\right)\right|_0^\infty+\dfrac{2s+1}{2\pi^2}V\int_0^\infty\dfrac{k^3}{3}\dfrac{\mp\beta\hbar c\cdot e^{-\beta(\hbar ck-\mu)}}{1\pm e^{-\beta(\hbar ck-\mu)}}\ dk\\
&=-\dfrac{2s+1}{2\pi^2}V\left(0-0\right)\mp\dfrac{2s+1}{6\pi^2}V(\beta\hbar c)\int_0^\infty k^3\dfrac{1}{e^{\beta(\hbar ck-\mu)}\pm 1}\ dk\\
&=\mp\dfrac{2s+1}{6\pi^2}V\dfrac{\beta\hbar c}{(\beta\hbar c)^4}\int_0^\infty (\beta\hbar c)^3k^3\dfrac{1}{e^{-\mu/kT}e^{(\beta\hbar c)k}\pm 1}\ (\beta\hbar c)dk\\
\end{align}$$
Let $z^{-1}=e^{-\mu/kT}$ and $x=(\beta\hbar c)k\implies dx=(\beta\hbar c)dk$, then:
$$\begin{align}
\ln Z&=\mp\dfrac{2s+1}{6\pi^2}V\dfrac{\beta\hbar c}{(\beta\hbar c)^4}\int_0^\infty \dfrac{(\beta\hbar c)^3k^3}{e^{-\mu/kT}e^{(\beta\hbar c)k}\pm 1}\ (\beta\hbar c)dk\\
&=\mp\dfrac{2s+1}{6\pi^2}\dfrac{V}{(\beta\hbar c)^3}\int_0^\infty \dfrac{x^3}{z^{-1}e^{x}\pm 1}dx
\end{align}$$
In class, we use the Fermi-Dirac ($+$) and Bose-Einstein ($-$) integrals:
$$\begin{align}
f^{\pm}_\nu(z)&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty\dfrac{x^{\nu-1}}{z^{-1}e^{x}\pm1}dx
\end{align}$$
We can simplify the system to:
$$\begin{align}
\ln Z&=\mp\dfrac{2s+1}{6\pi^2}\dfrac{V}{(\beta\hbar c)^3}\dfrac{\Gamma(4)}{\Gamma(4)}\int_0^\infty \dfrac{x^{4-1}}{z^{-1}e^{x}\pm 1}dx\\
&=\mp\dfrac{2s+1}{\pi^2}\dfrac{V}{(\beta\hbar c)^3}f^{\pm}_4\left(z\right)\\
\Aboxed{\ln Z&=\mp\dfrac{(2s+1)}{\pi^2}V\left(\dfrac{kT}{\hbar c}\right)^3f^{\pm}_4\left(e^{\mu/kT}\right)}
\end{align}$$
---
<div style="page-break-before: always;"></div>

### Question 3.A
Show that $PV=\text{const.} E$ (Explicitly derive this relationship with the precise value of $\text{const.}$).

It took me so long to figure out the identity that makes this trivial:
$$\begin{align}
f^{\pm}_\nu(z)&=\dfrac{1}{\Gamma(\nu)}\int_0^\infty\dfrac{x^{\nu-1}}{z^{-1}e^{x}\pm1}dx\\
\Aboxed{z\dfrac{\partial}{\partial z}f^{\pm}_\nu(z)&=f^{\pm}_{\nu-1}(z)}
\end{align}$$
To find the expected value of internal energy $U$:
$$\begin{align}
Z&=\text{Tr}\left(e^{-\beta(\hat{H}-\mu\hat{N})}\right)\\
\left(\dfrac{\partial Z}{\partial\beta}\right)_{V,\mu}&=-\left(\hat{H}-\mu\hat{N}\right)Z\\
\braket\hat{H}&=-\left(\dfrac{\partial\ln Z}{\partial\beta}\right)_{V,\mu}+\mu\braket\hat{N}\\
\end{align}$$
This gives us the internal energy, but it depends on the expected number of particles:
$$\begin{align}
Z&=\text{Tr}\left(e^{-\beta(\hat{H}-\mu\hat{N})}\right)\\
\left(\dfrac{\partial Z}{\partial\mu}\right)_{V,T}&=\beta\hat{N}\cdot Z\\
\braket\hat{N}&=\dfrac{1}{\beta}\left(\dfrac{\partial\ln Z}{\partial\mu}\right)_{V,T}
\end{align}$$
Combining these two together, we get total internal energy:
$$\begin{align}
\Aboxed{U&=\dfrac{\mu}{\beta}\left(\dfrac{\partial\ln Z}{\partial\mu}\right)_{V,T}-\left(\dfrac{\partial\ln Z}{\partial\beta}\right)_{V,\mu}}
\end{align}$$
So the chemical potential derivative is:
$$\begin{align}
\left(\dfrac{\partial\ln Z}{\partial\mu}\right)_{V,T}
&=\mp\dfrac{(2s+1)}{\pi^2}V\left(\dfrac{kT}{\hbar c}\right)^3\dfrac{\partial}{\partial \mu}f^{\pm}_4\left(z\right)\\
&=\mp\dfrac{(2s+1)}{\pi^2}V\left(\dfrac{kT}{\hbar c}\right)^3\dfrac{\partial z}{\partial\mu}\dfrac{\partial}{\partial z}f^{\pm}_4\left(z\right)\\
&=\mp\dfrac{(2s+1)}{\pi^2}V\left(\dfrac{kT}{\hbar c}\right)^3\dfrac{z}{kT}\dfrac{\partial}{\partial z}f^{\pm}_4\left(z\right)\\
&=\mp\dfrac{1}{kT}\dfrac{(2s+1)}{\pi^2}V\dfrac{(kT)^3}{(\hbar c)^3}f^{\pm}_{4}(z)\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}\\
\Aboxed{\left(\dfrac{\partial\ln Z}{\partial\mu}\right)_{V,T}&=\beta\ln Z\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}}
\end{align}$$
The thermodynamic beta term derivative:
$$\begin{align}
\left(\dfrac{\partial\ln Z}{\partial\beta}\right)_{V,\mu}
&=\mp\dfrac{(2s+1)}{\pi^2}\dfrac{V}{(\hbar c)^3}\dfrac{\partial}{\partial\beta}\left(\beta^{-3}f^{\pm}_4\left(z\right)\right)\\
&=\mp\dfrac{(2s+1)}{\pi^2}\dfrac{V}{(\hbar c)^3}\dfrac{\partial}{\partial\beta}\left(\beta^{-3}\right)f^{\pm}_4\left(z\right)\mp\dfrac{(2s+1)}{\pi^2}\dfrac{V}{(\hbar c)^3}\beta^{-3}\dfrac{\partial}{\partial\beta}\left(f^{\pm}_4\left(z\right)\right)\\
&=-3kT\ln Z\mp\dfrac{(2s+1)}{\pi^2}\dfrac{V}{(\hbar c)^3}\beta^{-3}\dfrac{\partial z}{\partial\beta}\dfrac{\partial}{\partial z}\left(f^{\pm}_4\left(z\right)\right)\\
&=-3kT\ln Z\mp\dfrac{(2s+1)}{\pi^2}\dfrac{V}{(\hbar c)^3}\beta^{-3}\mu z\dfrac{\partial}{\partial z}f^{\pm}_4\left(z\right)\\
&=-3kT\ln Z\mp\mu\dfrac{(2s+1)}{\pi^2}\dfrac{V}{(\hbar c)^3}\beta^{-3} f^{\pm}_4\left(z\right)\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}\\
\Aboxed{\left(\dfrac{\partial\ln Z}{\partial\beta}\right)_{V,\mu}&=-3kT\ln Z+\mu \ln Z\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}}
\end{align}$$
Substituting in for internal energy:
$$\begin{align}
U&=\dfrac{\mu}{\beta}\left(\dfrac{\partial\ln Z}{\partial\mu}\right)_{V,T}-\left(\dfrac{\partial\ln Z}{\partial\beta}\right)_{V,\mu}\\
&=\dfrac{\mu}{\beta}\left(\beta\ln Z\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}\right)-\left(-3kT\ln Z+\mu \ln Z\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}\right)\\
&=3kT\ln Z+\mu\ln Z\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}-\mu\ln Z\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}\\
\Aboxed{U&=3kT\ln Z}
\end{align}$$
What we know from the Grand Canonical Ensemble is that:
$$\begin{align}
\phi(T,V,\mu)&=-kT\ln Z\\
\phi(T,V,\mu)&=-PV\\
\end{align}$$
Setting these equal, we get:
$$\begin{align}
PV&=kT\ln Z\\
&=\dfrac{1}{3}\cdot 3kT\ln Z\\
\Aboxed{PV&=\dfrac{1}{3}U}
\end{align}$$
From lecture, this is what we expected, since it's a linear dispersion in 3 dimensions.

---
<div style="page-break-before: always;"></div>

### Question 3.B
Show that:
$$\begin{align}
N&=(2s+1)\dfrac{V}{\lambda^3}f_3^\pm(z)
\end{align}$$
Where $\lambda=\dfrac{1}{2\pi^{1/3}}\dfrac{hc}{kT}$, $z=e^{\mu/kT}$, and $f_{\nu}^\pm=\dfrac{1}{\Gamma(\nu)}\displaystyle\int_{0}^\infty\dfrac{x^{\nu-1}}{z^{-1}e^x\pm 1}$.

I used my previous results from 3.A to evaluate the derivative:
$$\begin{align}
\braket\hat{N}&=\dfrac{1}{\beta}\left(\dfrac{\partial\ln Z}{\partial\mu}\right)_{V,T}\\
&=\dfrac{1}{\beta}\beta\ln Z\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}\\
&=\mp\dfrac{(2s+1)}{\pi^2}V\left(\dfrac{kT}{\hbar c}\right)^3f^{\pm}_4\left(z\right)\dfrac{f^{\pm}_3\left(z\right)}{f^{\pm}_4\left(z\right)}\\
&=\mp\dfrac{(2s+1)}{\pi^2}V\left(\dfrac{kT}{\hbar c}\right)^3f^{\pm}_3\left(z\right)\\
&=\mp(2s+1)V\dfrac{(2\pi^{1/3})^3}{\pi^2\cdot8\pi}\left(\dfrac{kT}{\hbar c}\right)^3f^{\pm}_3\left(z\right)\\
&=\mp(2s+1)V\left(\dfrac{2\pi^{1/3}kT}{2\pi\hbar c}\right)^3f^{\pm}_3\left(z\right)\\
&=\mp(2s+1)V\left(\dfrac{1}{2\pi^{1/3}}\dfrac{hc}{kT}\right)^{-3}f^{\pm}_3\left(z\right)\\
&=\mp(2s+1)V\lambda^{-3}f^{\pm}_3\left(z\right)\\
\Aboxed{N&=(2s+1)\dfrac{V}{\lambda^{3}}f^{\pm}_3\left(z\right)}
\end{align}$$
---
<div style="page-break-before: always;"></div>


### Question 3.C
Obtain the exact expression for energy $E$ of the system.

We just substitute the expression for $\ln Z$ in for internal energy.
$$\begin{align}
U&=3kT\ln Z\\
&=\mp3kT\dfrac{(2s+1)}{\pi^2}V\left(\dfrac{kT}{\hbar c}\right)^3f^{\pm}_4\left(z\right)\\
\Aboxed{E&=\dfrac{3(2s+1)}{\pi^2}V\dfrac{k^4T^4}{\hbar^3 c^3}f^{\pm}_4\left(z\right)}
\end{align}$$
Or in terms of Lambda, we can write:
$$\begin{align}
E&=3kT\dfrac{(2s+1)}{\pi^2}V\left(\dfrac{kT}{\hbar c}\right)^3f^{\pm}_4\left(z\right)\\
&=3(2s+1)kT\cdot V\dfrac{(2\pi^{1/3})^3}{8\pi^3}\left(\dfrac{kT}{\hbar c}\right)^3f^{\pm}_4\left(z\right)\\
&=3(2s+1)kT\cdot V\left(2\pi^{1/3}\dfrac{kT}{2\pi\hbar c}\right)^3f^{\pm}_4\left(z\right)\\
&=3(2s+1)kT\cdot V\left(\dfrac{1}{2\pi^{1/3}}\dfrac{hc}{kT}\right)^{-3}f^{\pm}_4\left(z\right)\\
\Aboxed{E&=3(2s+1)\dfrac{V}{\lambda^3}kTf^{\pm}_4\left(z\right)}
\end{align}$$
---
<div style="page-break-before: always;"></div>


### Question 3.D
Now consider the case when $\lambda^3\dfrac{N}{V}\ll1$ (high-temperature or low-density limit), also meaning $z\ll1$. Obtain the ***energy*** as a function of $T,V,N$ and the ***equation of motion*** to up *first order* in $\lambda^3\dfrac{N}{V}$. Note that after using the small-$z$ approximation for $f_{\nu}^\pm(z)$:
$$\begin{align}
f_{\nu}^\pm(z)&=\sum_{l=1}^\infty(\mp1)^{l-1}\dfrac{z^l}{l^\nu}=z\mp\dfrac{z^2}{2^\nu}+\dfrac{z^3}{3^\nu}\mp\dots
\end{align}$$
$z$ must be eliminated from the equations in favor of $\lambda^3\dfrac{N}{V}$. To this end, you should use the equation above for $N$.

Start with the previous number equation:
$$\begin{align}
N&=(2s+1)\dfrac{V}{\lambda^{3}}f^{\pm}_3\left(z\right)\\
\lambda^3\dfrac{N}{V}&\approx(2s+1)\left(z\mp\dfrac{z^2}{2^3}+O(z^3)\right)\\
\end{align}$$
I'm just going to guess, let $\chi=\lambda^3\dfrac{N}{V}$, and we want $z=A_1\chi+A_2\chi^2+O(\chi^3)$:
$$\begin{align}
\chi&=(2s+1)\left(z\mp\dfrac{z^2}{2^3}+O(z^3)\right)\\
\chi&=(2s+1)\left(A_1\chi+A_2\chi^2\mp\dfrac{A_1^2\chi^2}{8}+O(\chi^3)\right)\\
\end{align}$$
Then we have the 2 following conditions for small $\chi$:
$$\begin{align}
1\chi&=(2s+1)A_1\chi &\implies && A_1&=\dfrac{1}{(2s+1)}\\
0\chi^2&=(2s+1)\left(A_2\mp\dfrac{A_1^2}{8}\right)\chi^2 &\implies && A_2&=\pm\dfrac{1}{8}\dfrac{1}{(2s+1)^2}\\
\end{align}$$
We then have our approximation for $z$ as:
$$\begin{align}
\Aboxed{z&=\dfrac{1}{(2s+1)}\chi\pm\dfrac{1}{8}\dfrac{1}{(2s+1)^2}\chi^2}
\end{align}$$
<div style="page-break-before: always;"></div>

With our energy equation:
$$\begin{align}
E&=3(2s+1)\dfrac{V}{\lambda^3}kTf^{\pm}_4\left(z\right)\\
&\approx3(2s+1)\dfrac{V}{\lambda^3}kT\left(z\mp\dfrac{z^2}{2^4}+O(z^3)\right)\\
&\approx3(2s+1)\dfrac{V}{\lambda^3}kT\left(\dfrac{1}{(2s+1)}\chi\pm\dfrac{1}{8}\dfrac{1}{(2s+1)^2}\chi^2\mp\dfrac{1}{16}\dfrac{1}{(2s+1)^2}\chi^2+O(\chi^3)\right)\\
&\approx3(2s+1)\dfrac{V}{\lambda^3}kT\left(\dfrac{1}{(2s+1)}\chi\pm\dfrac{1}{16}\dfrac{1}{(2s+1)^2}\chi^2\right)\\
&=3\dfrac{V}{\lambda^3}kT\chi\pm\dfrac{3}{16}\dfrac{1}{(2s+1)}\dfrac{V}{\lambda^3}kT\chi^2\\
&=3\dfrac{V}{\lambda^3}kT\lambda^3\dfrac{N}{V}\pm\dfrac{3}{16}\dfrac{1}{(2s+1)}\dfrac{V}{\lambda^3}kT\left(\lambda^3\dfrac{N}{V}\right)^2\\
\Aboxed{E(T,V,N)&=3NkT\pm\dfrac{3}{16}\dfrac{1}{(2s+1)}\dfrac{\lambda^3N}{V}NkT}
\end{align}$$
The equation of state for this system is then:
$$\begin{align}
PV&=\dfrac{1}{3}U\\
P(T,V,N)&=\dfrac{1}{3V}\cdot 3NkT\pm\dfrac{3}{16}\dfrac{1}{(2s+1)}\dfrac{\lambda^3N}{V}NkT\\
\Aboxed{P(T,V,N)&=\dfrac{NkT}{V}\left(1\pm\dfrac{3}{16}\dfrac{1}{(2s+1)}\lambda^3N\right)}
\end{align}$$
The question asked about an "equation of motion" but I assumed this meant the equation of state, so I provided the EOS in terms of pressure.

---
<div style="page-break-before: always;"></div>


### Question 3.E
Calculate the ***entropy*** of the system in the same order of approximation.

I can't think of a clever way to solve this without the way I think is most verbose:
$$\begin{align}
-PV&=U-TS-\mu N\\
S&=\dfrac{U+PV-\mu N}{T}\\
S&=\dfrac{4}{3}\dfrac{U}{T}-\dfrac{\mu}{T}N\\
\end{align}$$
We can calculate $\mu$ in terms of $z$ by:
$$\begin{align}
z&=e^{\mu/kT} & \implies && \mu=kT\ln z
\end{align}$$
And thus finding that $\mu N$ is:
$$\begin{align}
\mu N&=NkT\ln z\\
&\approx NkT\ln\left(\dfrac{1}{(2s+1)}\chi\pm\dfrac{1}{8}\dfrac{1}{(2s+1)^2}\chi^2\right)\\
&\approx NkT\ln\left(\dfrac{\chi}{(2s+1)}\left[1\pm\dfrac{1}{8}\dfrac{1}{(2s+1)}\chi\right]\right)\\
&=NkT\ln\left(\dfrac{\chi}{(2s+1)}\right)+NkT\ln\left(1\pm\dfrac{1}{8}\dfrac{1}{(2s+1)}\chi\right)\\
\Aboxed{\mu N&\approx NkT\ln\left(\dfrac{\chi}{(2s+1)}\right)\pm\dfrac{1}{8}NkT\dfrac{1}{(2s+1)}\chi}
\end{align}$$
We can then calculate the Entropy from these parameter as:
$$\begin{align}
S&=\dfrac{4}{3}\dfrac{1}{T}\left(3NkT\pm\dfrac{3}{16}\dfrac{1}{(2s+1)}\dfrac{\lambda^3N}{V}NkT\right)\\
&\ \ \ \ \ -\dfrac{1}{T}\left(NkT\ln\left(\dfrac{\lambda^3N/V}{(2s+1)}\right)\pm\dfrac{1}{8}NkT\dfrac{1}{(2s+1)}\dfrac{\lambda^3N}{V}\right)\\\\
&=4Nk\pm\dfrac{1}{4}\dfrac{1}{(2s+1)}\dfrac{\lambda^3N}{V}Nk-Nk\ln\left(\dfrac{\lambda^3N/V}{(2s+1)}\right)\mp\dfrac{1}{8}\dfrac{1}{(2s+1)}\dfrac{\lambda^3N}{V}Nk\\
&=4Nk\pm\dfrac{1}{8}\dfrac{1}{(2s+1)}\dfrac{\lambda^3N}{V}Nk-Nk\ln\left(\dfrac{\lambda^3N/V}{(2s+1)}\right)\\\\
\Aboxed{S(T,V,N)&=Nk\left[4-\ln\left(\dfrac{\lambda^3N/V}{(2s+1)}\right)\pm\dfrac{1}{8}\dfrac{1}{(2s+1)}\dfrac{\lambda^3N}{V}\right]}
\end{align}$$
---
<div style="page-break-before: always;"></div>


## Question 4
Consider a $d$-dimensional ideal Bose gas of spin $s=0$ particles with a linear dispersion relation $\varepsilon(p)=\gamma p$, in a $d$-dimensional bx of volume $V=L^d$ ($\gamma$ is a material-specific constant).

Note: The following expression might be useful:
$$\begin{align}
\Gamma(\nu)\zeta(\nu)&=\displaystyle\int_{0}^\infty\dfrac{x^{\nu-1}}{e^x-1}
\end{align}$$
Where $\zeta(\nu)$ is the Riemann Zeta Function defined as:
$$\begin{align}
\zeta(\nu)&=\sum_{n=1}^\infty\dfrac{1}{n^\nu} & \zeta(2)&=\dfrac{\pi^2}{6} & \zeta(4)&=\dfrac{\pi^4}{90}
\end{align}$$
---
### Question 4.A
What is the critical dimension $d_c$ above which Bose-Einstein condensation exists?

We want to find when the number of particles in the excited state is undefined.
Only when it is defined is when a condensate can exist.

Start with the number of particles at energy $E\propto p\ne 0$:
$$\begin{align}
\braket{n_p}&=\dfrac{1}{z^{-1}e^{\beta\varepsilon(p)}-1}
\end{align}$$
The total number of non-ground states is then:
$$\begin{align}
N_{p\ne0}&=\sum_{p\ne0}\dfrac{1}{z^{-1}e^{\beta\varepsilon(p)}-1}\\
&=\dfrac{L^d}{(2\pi\hbar)^d}\int\dfrac{1}{z^{-1}e^{\beta\varepsilon(p)}-1}d^dp\\
&=\dfrac{L^d}{(2\pi\hbar)^d}\int\dfrac{1}{z^{-1}e^{\beta\varepsilon(p)}-1}\Omega_dp^{d-1}\ dp\\
&=\dfrac{V\Omega_d}{(2\pi\hbar)^d}\int_{0}^{\infty}\dfrac{p^{d-1}}{z^{-1}e^{\beta\gamma p}-1}dp\\
&=\dfrac{V\Omega_d}{(2\pi\hbar)^d(\beta\gamma)^d}\int_{0}^{\infty}\dfrac{(p\beta\gamma)^{d-1}}{z^{-1}e^{\beta\gamma p}-1}\ \beta\gamma dp\\
&=\dfrac{V\Omega_d}{(2\pi\hbar)^d(\beta\gamma)^d}\int_{0}^{\infty}\dfrac{x^{d-1}}{z^{-1}e^{x}-1}dx
\end{align}$$
<div style="page-break-before: always;"></div>

At the critical point, we know that $\mu=0 \implies z=1$, and so:
$$\begin{align}
N_{p\ne0}&=\dfrac{V\Omega_d}{(2\pi\hbar)^d(\beta\gamma)^d}\int_{0}^{\infty}\dfrac{x^{d-1}}{z^{-1}e^{x}-1}dx\\
&=\dfrac{V\Omega_d}{(2\pi\hbar)^d(\beta\gamma)^d}\int_{0}^{\infty}\dfrac{x^{d-1}}{e^{x}-1}dx\\
\Aboxed{N_{p\ne0}&=\dfrac{V\Omega_d}{(2\pi\hbar)^d(\beta\gamma)^d}\Gamma(d)\zeta(d)}
\end{align}$$
Where $\Omega_d$ is the surface area of the unit ball in $d$ dimensions (I don't remember the exact form).

What we know about the Riemann Zeta function is that it exists:
$$\begin{align}
&d>1\implies \zeta(d) & &\text{(Convergence of Summation)}
\end{align}$$
So the critical dimension is as follows:
$$\begin{align}
\Aboxed{d_c&=1} &\text{because}&& d>1
\end{align}$$
It only condenses for $2$-Dimensions and higher.

---
### Question 4.B
For $d>d_c$, what is the Bose-Einstein critical temperature $T_c$? Express it as a function of the density $N/V$.
$$\begin{align}
N&=\dfrac{V\Omega_d}{(2\pi\hbar)^d(\beta\gamma)^d}\Gamma(d)\zeta(d)\\
N&=\dfrac{V\Omega_d k^dT_c^d}{(2\pi\hbar)^d\gamma^d}\Gamma(d)\zeta(d)\\
T_c^d&=\dfrac{(2\pi)^d}{\Omega_d}\dfrac{(\hbar\gamma/k)^d}{\Gamma(d)\zeta(d)}\dfrac{N}{V}\\
T_c(N/V)&=\dfrac{\hbar\gamma}{k}\left[\dfrac{(2\pi)^d}{\Omega_d}\dfrac{1}{\Gamma(d)\zeta(d)}\right]^{1/d}\left[\dfrac{N}{V}\right]^{1/d}
\end{align}$$
Wait I found it. $\Omega_d=2\pi^{d/2}/\Gamma(d/2)$, and so:
$$\begin{align}
\Aboxed{T_c(N/V)&=2\sqrt{\pi}\dfrac{\hbar\gamma}{k}\left[\dfrac{\Gamma(d/2)}{2\Gamma(d)\zeta(d)}\right]^{1/d}\left[\dfrac{N}{V}\right]^{1/d}}\\
\Aboxed{T_c(\rho)&=2\sqrt{\pi}\dfrac{\hbar\gamma}{k}\left[\dfrac{\Gamma(d/2)}{2\Gamma(d)\zeta(d)}\right]^{1/d}\rho^{1/d}}
\end{align}$$
---
<div style="page-break-before: always;"></div>


### Question 4.C
Consider this system for $d>d_c$ and $T<T_c$. Show that:
$$\begin{align}
\dfrac{N_0}{N}&=1-\left(\dfrac{T}{T_c}\right)^\sigma
\end{align}$$
where $N_0/N$ is the fraction of particles in the ground state below $T_c$ and determine the exponent $\sigma$ as a function of dimension $d$.
$$\begin{align}
N_{p\ne0}&=\dfrac{V\Omega_d(kT)^d}{(2\pi\hbar\gamma)^d}\Gamma(d)\zeta(d)\\
N&=\dfrac{V\Omega_d(kT_c)^d}{(2\pi\hbar\gamma)^d}\Gamma(d)\zeta(d)\\
\end{align}$$
Dividing both equations from each other, we see:
$$\begin{align}
\dfrac{N_{p\ne0}}{N}&=\dfrac{\dfrac{V\Omega_d(k)^d}{(2\pi\hbar\gamma)^d}\Gamma(d)\zeta(d)}{\dfrac{V\Omega_d(k)^d}{(2\pi\hbar\gamma)^d}\Gamma(d)\zeta(d)}\dfrac{T^d}{T_c^d}\\
\dfrac{N-N_0}{N}&=\dfrac{T^d}{T_c^d}\\
1-\dfrac{N_0}{N}&=\left(\dfrac{T}{T_c}\right)^d\\
\Aboxed{\dfrac{N_0}{N}&=1-\left(\dfrac{T}{T_c}\right)^d}
\end{align}$$
And so our exponent $\sigma$ is just:
$$\begin{align}
\Aboxed{\sigma&=d} & d&>d_c & T<T_c
\end{align}$$
---
<div style="page-break-before: always;"></div>

### Question 4.D
Consider this system for $d>d_c$ and $T<T_c$. Find the internal energy $E(T,V)$.
$$\begin{align}
E(T,V)&=\dfrac{V\Omega_d}{(2\pi\hbar)^d}\int_{0}^\infty\dfrac{\varepsilon(p)\cdot p^{d-1}}{z^{-1}e^{\beta\varepsilon(p)}-1}dp\\
&=\dfrac{V\Omega_d}{(2\pi\hbar)^d}\int_{0}^\infty\dfrac{\gamma p\cdot p^{d-1}}{e^{\beta\gamma p}-1}dp\\
&=\dfrac{V\Omega_d\gamma}{(2\pi\hbar)^d(\beta\gamma)^{d+1}}\int_{0}^\infty\dfrac{(\beta\gamma p)^{(d+1)-1}}{e^{\beta\gamma p}-1}\ \beta\gamma dp\\
&=\dfrac{V\Omega_d\gamma}{(2\pi\hbar)^d(\beta\gamma)^{d+1}}\int_{0}^\infty\dfrac{x^{(d+1)-1}}{e^{x}-1}\ dx\\
&=\dfrac{V\Omega_d\gamma}{(2\pi\hbar)^d(\beta\gamma)^{d+1}}\Gamma(d+1)\zeta(d+1)\\
\Aboxed{E(T,V)&=\dfrac{\Omega_d\Gamma(d+1)\zeta(d+1)}{(2\pi)^d}\dfrac{V k^{d+1}}{\hbar^d\gamma^{d}}T^{d+1}}
\end{align}$$
Or alternatively:
$$\begin{align}
\Aboxed{E(T,V)&=\dfrac{\zeta(d+1)\Gamma(d+1)}{2^{d-1}\pi^{d/2}\cdot\Gamma(d/2)}\dfrac{V k^{d+1}}{\hbar^d\gamma^{d}}T^{d+1}}
\end{align}$$
---
<div style="page-break-before: always;"></div>


### Question 4.E
Consider this system for $d>d_c$ and $T<T_c$. Find the specific heat $C_V$.
$$\begin{align}
\left(\dfrac{\partial E}{\partial T}\right)_{V}&=\dfrac{\partial}{\partial T}\left(\dfrac{\zeta(d+1)\Gamma(d+1)}{2^{d-1}\pi^{d/2}\cdot\Gamma(d/2)}\dfrac{V k^{d+1}}{\hbar^d\gamma^{d}}T^{d+1}\right)\\
&=\dfrac{\zeta(d+1)\Gamma(d+1)}{2^{d-1}\pi^{d/2}\cdot\Gamma(d/2)}\dfrac{V k^{d+1}}{\hbar^d\gamma^{d}}(d+1)T^{d}\\
\Aboxed{C_V&=\dfrac{\zeta(d+1)\Gamma(d+2)}{2^{d-1}\pi^{d/2}\cdot\Gamma(d/2)}\dfrac{V k^{d+1}}{\hbar^d\gamma^{d}}\cdot T^{d}}
\end{align}$$
---
### Question 4.F
Consider this system for $d>d_c$ and $T<T_c$. Obtain an expression for pressure $P(T,N/V)$ of the system. Does it actually depend on density? How do you interpret this result.

Well we can actually learn something from Question 3, where we know for a grand canonical ensemble, we have the following relationship:
$$\begin{align}
\phi&=-PV\\
PV&=\dfrac{1}{d}E
\end{align}$$
Where the $1$ is from the linear dispersion, and $d$ is the dimension of the system:
$$\begin{align}
PV&=\dfrac{1}{d}E\\
P&=\dfrac{1}{Vd}\dfrac{\zeta(d+1)\Gamma(d+1)}{2^{d-1}\pi^{d/2}\cdot\Gamma(d/2)}\dfrac{V k^{d+1}}{\hbar^d\gamma^{d}}T^{d+1}\\
\Aboxed{P&=\dfrac{1}{d}\dfrac{\zeta(d+1)\Gamma(d+1)}{2^{d-1}\pi^{d/2}\cdot\Gamma(d/2)}\dfrac{k^{d+1}}{\hbar^d\gamma^{d}}T^{d+1}}
\end{align}$$
Pressure is related to temperature and the dimension, but has no dependence on $N$ or $V$. Since particles in the ground state do not contribute to the pressure, it has no repulsion in the ground state, and thus it is independent of the density (in this limit).

---
<div style="page-break-before: always;"></div>


### Question 4.G
Consider this system for $d>d_c$ and $T<T_c$. Obtain the entropy $S(T,V)$.
$$\begin{align}
\phi&=-PV=-\dfrac{1}{d}E
\end{align}$$
We know the following:
$$\begin{align}
S(T,V)&=-\left(\dfrac{\partial\phi}{\partial T}\right)_{V,\mu}\\
&=\dfrac{1}{d}\left(\dfrac{\partial E}{\partial T}\right)_{V,\mu}\\
\Aboxed{S(T,V)&=\dfrac{1}{d}\dfrac{\zeta(d+1)\Gamma(d+2)}{2^{d-1}\pi^{d/2}\cdot\Gamma(d/2)}\dfrac{k^{d+1}}{\hbar^d\gamma^{d}}\cdot VT^{d}}
\end{align}$$
---
<div style="page-break-before: always;"></div>












## Appendix I
We have the probability density function:
$$\begin{align}
\rho_1(x)&=\begin{cases}1& 0\le x\le 1\\0&\text{otherwise}\end{cases}
\end{align}$$
We can calculate the characteristic function ($\Phi(k)=\left\langle e^{ikx}\right\rangle$) as:
$$\begin{align}
\Phi_1(k)&=\int_{-\infty}^\infty e^{ikx}\rho_1(x)\ dx\\
&=\int_{-\infty}^0 e^{ikx}\cdot0\ dx+\int_{0}^1 e^{ikx}\cdot1\ dx+\int_{1}^\infty e^{ikx}\cdot0\ dx\\
&=0+\left.\dfrac{e^{ikx}}{ik}\right|_{x=0}^{x=1}+0\\
&=\dfrac{e^{ik}}{ik}-\dfrac{1}{ik}\\
\Phi_1(k)&=\dfrac{e^{ik}-1}{ik}\\
\end{align}$$
Since these are independent random variables, we know that:
$$\begin{align}
\Phi_N(k)&=\left(\dfrac{e^{ik}-1}{ik}\right)^N
\end{align}$$
We can then reverse the transformation:
$$\begin{align}
\rho_N(y)
&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-izy}\Phi_N(z)\ dz\\
&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-iyz}\dfrac{\left(e^{iz}-1\right)^N}{(iz)^N}\ dz\\
&=\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-iyz}\sum_{k=0}^N\dfrac{N!}{(N-k)!\cdot k!}\dfrac{\left(e^{iz}\right)^{k}\left(-1\right)^{N-k}}{(iz)^N}\ dz\\
&=\sum_{k=0}^N\dfrac{N!}{(N-k)!\cdot k!}\left(-1\right)^{N-k}\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-iyz}\dfrac{e^{ikz}}{(iz)^N}\ dz\\
&=\sum_{k=0}^N\dfrac{N!}{(N-k)!\cdot k!}\left(-1\right)^{N-k}\dfrac{1}{2\pi}\int_{-\infty}^\infty \dfrac{e^{-i(y-k)z}}{(iz)^N}\ dz\\
\end{align}$$
Let $\eta=y-k$, then:
$$\begin{align}
\rho_N(y)
&=\sum_{k=0}^N\dfrac{N!}{(N-k)!\cdot k!}\left(-1\right)^{N-k}\cdot\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\eta z}\dfrac{1}{(iz)^N}\ dz\\
\end{align}$$
We need to use complex analysis to solve this system. Lets look at the contour integral:
$$\begin{align}
\oint_\Gamma f(z)\ dz&=\lim_{\epsilon\rightarrow0^+}\int_{\pi}^{2\pi} f(\epsilon e^{i\phi})\ i\epsilon e^{i\phi} \ d\phi+\lim_{\epsilon\rightarrow0^+}\int_\epsilon^\infty f(x)\ dx\\
&\ \ \ \ +\lim_{\epsilon\rightarrow0^+}\int_{-\infty}^{-\epsilon} f(x)\ dx+\lim_{R\rightarrow\infty}\int_0^{\pi}f(Re^{i\phi})\ iRe^{i\phi}\ d\phi
\end{align}$$



CONTOUR INTEGRAL HERE



$$\begin{align}
\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\eta z}\dfrac{1}{(iz)^N}\ dz
&=\dfrac{1}{2\pi}\cdot2\pi i\cdot\text{Res}\left(\dfrac{e^{-i\eta z}}{(iz)^N}, z=0\right)\\
&=i\cdot\dfrac{1}{(N-1)!}\lim_{z\rightarrow0}\dfrac{d^{N-1}}{dz^{N-1}}\left(z^N\cdot\dfrac{e^{-i\eta z}}{(iz)^N}\right)\\
&=i^{1-N}\cdot\dfrac{1}{(N-1)!}\lim_{z\rightarrow0}\dfrac{d^{N-1}}{dz^{N-1}}\left(e^{-i\eta z}\right)\\
&=i^{1-N}\cdot\dfrac{1}{(N-1)!}(-i\eta)^{N-1}\lim_{z\rightarrow0}e^{-i\eta z}\\
&=i^{1-N}(-i)^{N-1}\cdot\dfrac{\eta^{N-1}}{(N-1)!}\cdot1\\
\Aboxed{\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\eta z}\dfrac{1}{(iz)^N} dz&=\dfrac{\eta^{N-1}}{(N-1)!}H(\eta)}
\end{align}$$
Substituting back in, we get:
$$\begin{align}
\rho_N(y)
&=\sum_{k=0}^N\dfrac{N!}{(N-k)!\cdot k!}\left(-1\right)^{N-k}\cdot\dfrac{1}{2\pi}\int_{-\infty}^\infty e^{-i\eta z}\dfrac{1}{(iz)^N}\ dz\\
&=\sum_{k=0}^N\dfrac{N!}{(N-k)!\cdot k!}\left(-1\right)^{N-k}\cdot\dfrac{\eta^{N-1}}{(N-1)!}H(\eta)\\
&=\dfrac{1}{(N-1)!}\sum_{k=0}^N\left(-1\right)^{N-k}\binom{N}{k}(y-k)^{N-1}H(y-k)
\end{align}$$
For $H(\eta)=1$, then $\eta>0\implies y-k>0\implies k<y$. All terms above that are 0:
$$\begin{align}
\rho_N(y)
&=\dfrac{1}{(N-1)!}\sum_{k=0}^N\left(-1\right)^{N-k}\binom{N}{k}(y-k)^{N-1}H(y-k)\\
\rho_N(y)&=\dfrac{1}{(N-1)!}\sum_{k=0}^{k<y}\left(-1\right)^{N-k}\binom{N}{k}(y-k)^{N-1},\ \ \  0\le y\le N\\
\Aboxed{\rho_N(y)&=\dfrac{1}{(N-1)!}\sum_{k=0}^{k<y}\left(-1\right)^{k}\binom{N}{k}(k-y)^{N-1},\ \ \  0\le y\le N}
\end{align}$$
