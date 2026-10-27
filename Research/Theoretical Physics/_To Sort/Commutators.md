




## Ensemble Relationships
$$\begin{align}
Z(T,V,\mu)&=\text{Tr}\left(e^{-\beta(\hat{H}-\mu\hat{N})}\right)
\end{align}$$
$$\begin{align}
\hat{\rho}&=\dfrac{1}{Z}e^{-\beta(\hat{H}-\mu\hat{N})}\\
\braket{\hat{A}}&=\text{Tr}\left(\hat{\rho}\hat{A}\right)
\end{align}$$
$$\begin{align}
\phi(T,V,\mu)&=-kT\ln Z(T,V,\mu)
\end{align}$$
$$\begin{align}
d\phi&=\left(\dfrac{\partial\phi}{\partial T}\right)_{V,\mu}dT+\left(\dfrac{\partial\phi}{\partial V}\right)_{T,\mu}dV+\left(\dfrac{\partial\phi}{\partial\mu}\right)_{T,V}d\mu
\end{align}$$
$$\begin{align}
S&=-\left(\dfrac{\partial\phi}{\partial T}\right)_{V,\mu} & P&=-\left(\dfrac{\partial\phi}{\partial V}\right)_{T,\mu} & N&=-\left(\dfrac{\partial\phi}{\partial\mu}\right)_{T,V}
\end{align}$$








## Relativistic Free Particle
We have the Hamiltonian:
$$\begin{align}
\hat{H}&=\dfrac{1}{2m}\hat{P}_\mu\hat{P}^\mu
\end{align}$$
With the dynamics:
$$\begin{align}
\dfrac{\partial\hat{X}^\mu}{\partial\tau}&=\dfrac{i}{\hbar}\left[\hat{H},\hat{X}^\mu\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}\left[\hat{P}^2,\hat{X}^\mu\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}(-2i\hbar \hat{P}^\mu)\\
\Aboxed{\dfrac{\partial\hat{X}^\mu}{\partial\tau}&=\dfrac{\hat{P}^\mu}{m}}
\end{align}$$
$$\begin{align}
\dfrac{\partial\hat{P}^\mu}{\partial\tau}&=\dfrac{i}{\hbar}\left[\hat{H},\hat{P}^\mu\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}\left[\hat{P}^2,\hat{\hat{P}}^\mu\right]\\
\Aboxed{\dfrac{\partial\hat{P}^\mu}{\partial\tau}&=0}
\end{align}$$
Momentum is constant, and so we can integrate the first equation of motion:
$$\begin{align}
\dfrac{\partial\hat{X}^\mu}{\partial\tau}&=\dfrac{\hat{P}^\mu}{m}\\
\int\dfrac{\partial\hat{X}^\mu}{\partial\tau}d\tau&=\int\dfrac{\hat{P}^\mu}{m}d\tau\\
\Aboxed{\hat{X}^\mu(\tau)&=\hat{X}^\mu(0)+\dfrac{\hat{P}^\mu}{m}\tau}
\end{align}$$
To find the expectation value of position, we do like we would in normal mechanics:
$$\begin{align}
\braket{\hat{X}^\mu(\tau)}&=\bra{\Psi}\hat{X}^\mu(\tau)\ket{\Psi}\\
&=\bra{\Psi}\hat{X}^\mu(0)\ket{\Psi}+\dfrac{\tau}{m}\bra{\Psi}\hat{P}^\mu\ket{\Psi}\\
\Aboxed{\braket{\hat{X}^\mu(\tau)}&=\braket{\hat{X}^\mu(0)}+\dfrac{\tau}{m}\braket{\hat{P}^\mu(\tau)}}
\end{align}$$



### Path Integral
Since our wavefunction is universal and unchanging, we have to be a bit creative:
$$\begin{align}
K(X_f^\mu,X_i^\mu;\tau)&=\int_{X^\mu(0)=X_0^\mu}^{X^\mu(\tau)=X_f^\mu}\mathcal{D}[X^\mu(\tau')]\exp\left(\dfrac{i}{\hbar}\int_{0}^\tau L(X^\mu(\tau'), \dot{X}^\mu(\tau'),\tau')\ d\tau'\right)
\end{align}$$
Where the non-hat 4-vectors are the eigenvalues of their respective operators:
$$\begin{align}
\hat{X}^\mu(\tau)\ket{X^\mu}&=X^\mu(\tau)\ket{X^\mu} & \hat{P}^\mu(\tau)\ket{P^\mu}&=P^\mu(\tau)\ket{P^\mu}
\end{align}$$

### For the Free Particle
The eigenvalues are:
$$\begin{align}
X^\mu(\tau)&=X^\mu(0)+\dfrac{P^\mu(0)}{m}\tau\\
P^\mu(\tau)&=P^\mu(0)\\
\end{align}$$
And the Lagrangian is:
$$\begin{align}
L(X_\mu(\tau),\dot{X}_\mu(\tau),\tau)=\dfrac{1}{2}m\dot{X}_\mu(\tau)\dot{X}^\mu(\tau)
\end{align}$$
So the propagator is then:
$$\begin{align}
K(X_f^\mu,X_i^\mu;\tau)&=\int_{X^\mu(0)=X_0^\mu}^{X^\mu(\tau)=X_f^\mu}\mathcal{D}[X^\mu(\tau')]\exp\left(\dfrac{i}{\hbar}\int_{0}^\tau \dfrac{1}{2}m\dot{X}_\mu(\tau')\dot{X}^\mu(\tau')\ d\tau'\right)
\end{align}$$
And the wavefunction at proper time (when measured at a location):
$$\begin{align}
\Psi(X_f^\mu;\tau)&=\int K(X_f^\mu,X_i^\mu;\tau)\braket{X_i^\mu|\Psi}\ d^4X_i^\mu
\end{align}$$





















## Spacetime Field (3+1)
We have a set of operators:
$$\begin{align}
\hat{X}^\mu&=\left(c\hat{T},\hat{X},\hat{Y},\hat{Z}\right)\\
\hat{P}^\mu&=\left(\hat{E}/c,\hat{P}_x,\hat{P}_y,\hat{P}_z\right)\\
\end{align}$$
With the associated commutator relation:
$$\begin{align}
[\hat{X}^\mu,\hat{P}^\nu]&=i\hbar |g^{\mu\nu}|
\end{align}$$

$$\begin{align}
ddd
\end{align}$$







## Spacetime Field (1+1)
We have the commutator relations:

We introduce 2 discrete modes:
$$\begin{align}
\hat{a}_1,\hat{a}_1^\dagger && \hat{a}_2,\hat{a}_2^\dagger && [\hat{a}_i,\hat{a}_j^\dagger]&=\delta_{ij}
\end{align}$$
Which then defines the number operator:
$$\begin{align}
\hat{N}&=\hat{a}_1^\dagger\hat{a}_1+\hat{a}_2^\dagger\hat{a}_2
\end{align}$$
We also have the Hamiltonian with a (constant) vector potential:
$$\begin{align}
\hat{H}&=\dfrac{1}{2m}\left(\hat{P}_\mu-q\hat{A}_\mu\right)\left(\hat{P}^\mu-q\hat{A}^\mu\right)\\
\end{align}$$
If we let $\hat{P}_\mu=\hbar k_\mu(\hat{a}_\mu^\dagger+\hat{a}_\mu^\dagger)$:
$$\begin{align}
\hat{H}\ket{n_1,n_2}&=\sum_{i=1}^2\dfrac{1}{2m}\left(\hbar k_i(\hat{a}_i^\dagger+\hat{a}_i^\dagger)-qA_i\right)^2\ket{n_1,n_2}\\
\end{align}$$
Then we have the density operator:
$$\begin{align}
\hat{\rho}&=\dfrac{1}{Z}e^{-\beta(\hat{H}-\mu\hat{N})}
\end{align}$$
And partition function:
$$\begin{align}
\hat{\rho}&=\sum_{n_1,n_2=0,1}e^{-\beta(\hat{H}-\mu\hat{N})}
\end{align}$$














If we were to add a 4-potential to our system so that:
$$\begin{align}
\hat{H}&=\dfrac{1}{2m}\left(\hat{P}_\mu-q\hat{A}_\mu\right)\left(\hat{P}^\mu-q\hat{A}^\mu\right)
\end{align}$$
Going through the same system, we can then see:
$$\begin{align}
\Aboxed{\dfrac{\partial\hat{X}^\mu}{\partial\tau}&=\dfrac{1}{m}\hat{P}^\mu-\dfrac{q}{m}\hat{A}^\mu(\hat{X})}\\
\Aboxed{\dfrac{\partial \hat{P}^\mu}{\partial\tau}&=\dfrac{q}{m}\left(\hat{P}^\nu-q\hat{A}^\nu(\hat{X})\right)\partial_\mu\hat{A}_\nu(\hat{X})}\\
\end{align}$$
And for the higher squared operators:
$$\begin{align}
\Aboxed{\dfrac{\partial}{\partial\tau}\hat{X}^2&=-\dfrac{2}{m}\ \hat{X}\cdot\left(\hat{P}^\nu-q\hat{A}^\nu(\hat{X})\right)}\\
\Aboxed{\dfrac{\partial}{\partial\tau}\hat{P}^2&=2\dfrac{q}{m}\hat{P}^\nu\left(\hat{P}^\nu-q\hat{A}^\nu(\hat{X})\right)\partial_\mu\hat{A}_\nu(\hat{X})}\\
\end{align}$$

$$\begin{align}
\hat{H}&=\sqrt{c^2\hat{P}^2+m^2c^4}
\end{align}$$