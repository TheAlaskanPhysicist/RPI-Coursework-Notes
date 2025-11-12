## Covariant Operator Dynamics and Quantum Uncertainty in Relativistic Systems
---







$$\begin{align}
[\hat{X}^\mu,\hat{P}^\nu]&=i\hbar g^{\mu\nu} & 
[\hat{X}^\mu,\hat{X}^\nu]&=0 & 
[\hat{P}^\mu,\hat{P}^\nu]&=0
\end{align}$$





In Classical Mechanics, $\vec{x}$ and $\vec{p}$ are independent because they are uncorrelated.
In Non-Relativistic Quantum Mechanics, momentum is related to space by:
$$\begin{align}
\vec{p}&=\hbar\vec{k} & \vec{k}\ _{\text{FT}}\iff_{\text{IFT}}\ \vec{x}
\end{align}$$
Where there's a correlation since $\vec{k}$ and $\vec{x}$ are Fourier duals of each other satisfying:
$$\begin{align}
\braket{(\Delta x)^2}\braket{(\Delta p_x)^2}&\ge\dfrac{\hbar^2}{4}\\
[\hat{x},\hat{p}]&=i\hbar
\end{align}$$
What we can see immediately from the Fourier transform:
$$\begin{align}
\mathcal{F}[f(x)]&=\int_{-\infty}^\infty e^{-i\vec{k}\cdot\vec{x}} f(x)\ dx
\end{align}$$
The relation for the expected value from the exponential term has the following relation that:
$$\begin{align}
x&,k & \rightarrow&& \alpha x&,k/\alpha 
\end{align}$$
When it comes to the metric, then, it scales as this new term such that the following condition is satisfied:
$$\begin{align}
[\hat{X}^\mu,\hat{P}^\nu]&=i\hbar g^{\mu\nu}
\end{align}$$
However, how does one interpret a negative in this commutation, conceptually?
They should result in the same output for uncertainties, since they deal with the absolute value of the expected value, and thus any relation must at least stay within "reason".


## Quantum Operator Mechanics
#### Operator Definitions
Canonical operators:
$$\begin{align}
\hat{X}& && \text{(4-Position Operator)}\\
\hat{T}&=\hat{X}^0 && \text{(Time Operator)}\\
\hat{X}^i& && \text{(Space Operator)}\\
\hat{P}& && \text{(4-Momentum Operator)}\\
\hat{E}&=\hat{X}^0 && \text{(Energy Operator)}\\
\hat{P}_i& && \text{(Momentum Operator)}\\
\end{align}$$
Hermitian Momentum:
$$\begin{align}
\Aboxed{\hat{\Pi}_\mu&=-i\hbar\nabla_\mu+q\mathcal{A}_\mu(\hat{X})+\dfrac{i\hbar}{2}\Gamma^\alpha_{\alpha\mu}(\hat{X})}
\end{align}$$
$$\begin{align}
\hat{\chi}_\mu&=q\mathcal{B}_\mu(\hat{P})+\dfrac{i\hbar}{2}\Gamma^\alpha_{\alpha\mu}(\hat{P})\\
\hat{\Pi}_\mu&=-i\hbar\nabla_\mu+q\mathcal{A}_\mu(\hat{X})+\dfrac{i\hbar}{2}\Gamma^\alpha_{\alpha\mu}(\hat{X})
\end{align}$$
The covariant derivative:
$$\begin{align}
\text{Scalar} && \nabla_\mu\phi&=\partial_\mu\phi\\
\text{Vector} && \nabla_\mu V^\alpha&=\partial_\mu V^\alpha+\Gamma_{\mu\beta}^\alpha V^\beta\\
\text{Covector} && \nabla_\mu W_\alpha&=\partial_\mu W_\alpha-\Gamma_{\mu\alpha}^\beta W_\beta\\
\text{Spinor} && \nabla_\mu\psi&=\partial_\mu\psi+\dfrac{1}{4}\omega_{\mu ab}\gamma^a\gamma^b\psi
\end{align}$$
---
#### Operator Commutators
Position-Position Commutator
$$\begin{align}
[\hat{X}^\mu,\hat{X}^\nu]&=[\hat{X}^\mu,\hat{X}_\nu]=[\hat{X}_\mu,\hat{X}_\nu]=0\\
\end{align}$$
Position-Momentum Commutator
$$\begin{align}
[\hat{X}^\mu,\hat{\Pi}^\nu]&=i\hbar g^{\mu\nu}(\hat{X}) & \hat{\Pi}^\nu&=g^{\nu\alpha}\hat{\Pi}_\alpha\\
[\hat{X}^\mu,\hat{\Pi}_\nu]&=i\hbar\delta^\mu_\nu & \delta^\mu_\nu&=\partial_\nu\xi^\mu & \text{(Canonical Relation)}\\
[\hat{X}_\mu,\hat{\Pi}_\nu]&=i\hbar g_{\mu\nu}(\hat{X}) & \hat{X}_\mu&=g_{\mu\alpha}\hat{X}^\alpha
\end{align}$$
Momentum-Momentum Commutator
$$\begin{align}
[\hat{\Pi}_\mu,\hat{\Pi}_\nu]&=-\hbar^2\mathcal{R}_{\mu\nu}+i\hbar q\hat{\mathcal{F}}_{\mu\nu}(\hat{X})\\
[\hat{\Pi}_\mu,\hat{\Pi}^\nu]&=\left(-\hbar^2\mathcal{R}_{\mu\alpha}+i\hbar q\hat{\mathcal{F}}_{\mu\alpha}(\hat{X})\right)g^{\nu\alpha}(\hat{X})\\
[\hat{\Pi}^\mu,\hat{\Pi}^\nu]&=\left(-\hbar^2\mathcal{R}_{\alpha\beta}+i\hbar q\hat{\mathcal{F}}_{\alpha\beta}(\hat{X})\right)g^{\mu\alpha}g^{\nu\beta}(\hat{X})
\end{align}$$
where $\mathcal{R}_{\mu\nu}$ is the covariant commutator of covariant derivatives acting in the chosen representation:
$$\begin{align}
\text{Scalar:}&& \mathcal{R}_{\mu\nu}&=0\\
\text{Vector:}&& \mathcal{R}_{\mu\nu}V^\alpha&=\mathcal{R}_{\beta\mu\nu}^\alpha V^\beta\\
\text{Spinor:}&& \mathcal{R}_{\mu\nu}\psi&=\dfrac{1}{4}R_{ab\mu\nu}\gamma^a\gamma^b\psi\\
\end{align}$$







### Required Equations from Mechanics
#### Fundamental covariant algebra

Position-Momentum Commutator (Canonical Relation)

Momentum-Momentum Commutator (Curvature)
$$\begin{align}

\end{align}$$

#### Mixed Variants
Position-Momentum Commutator
$$\begin{align}

\end{align}$$

Momentum-Momentum Commutator

#### Observer-Projected Algebra
Frame Position-Position Commutator
$$\begin{align}
[\hat{X}^{(a)},\hat{X}^{(b)}]&=[e^{(a)}_\mu\hat{X}^\mu,e^{(b)}_\nu\hat{X}^\nu]=0
\end{align}$$
Frame Position-Momentum Commutator
$$\begin{align}
[\hat{X}^{(a)},\hat{P}_{(b)}]&=[e^{(a)}_\mu\hat{X}^\mu,e_{(b)}^\nu\hat{P}_\nu]=i\hbar\delta_{b}^a
\end{align}$$
Momentum-Momentum Commutator
$$\begin{align}
[\hat{P}_{(a)},\hat{P}_{(b)}]&=[e_{(a)}^\mu\hat{P}_\mu,e_{(b)}^\nu\hat{P}_\nu]=-\hbar^2e_{(a)}^\mu e_{(b)}^\nu\mathcal{R}_{\mu\nu}
\end{align}$$


### Heisenberg Equation of Motion (Free Particle)
Define the Hamiltonian as the following:
$$\begin{align}
\hat{H}&=\dfrac{1}{2}\left(\hat{P}_\mu\hat{P}^\mu+\hat{M}^2(\hat{X})\right)
\end{align}$$
Where $\hat{M}$ is the mass operator (since I know GR messes this up).

The general form of the EOM is:
$$\begin{align}
\dfrac{d\hat{O}}{d\tau}&=\dfrac{[\hat{O},\hat{H}]}{i\hbar}+\dfrac{\partial\hat{O}}{\partial\tau}
\end{align}$$
And so we find for 4-position:
$$\begin{align}
\dfrac{d\hat{X}^\mu}{d\tau}&=\dfrac{[\hat{X}^\mu,\hat{H}]}{i\hbar}\\
&=\dfrac{1}{2i\hbar}\left[\hat{X}^\mu,\hat{P}_\nu\hat{P}^\nu+\hat{M}^2(\hat{X})\right]\\
&=\dfrac{1}{2i\hbar}\left[\hat{X}^\mu,\hat{P}_\nu\hat{P}^\nu\right]+0\\
&=\dfrac{1}{2i\hbar}\left[\hat{X}^\mu,\hat{P}_\nu\right]\hat{P}^\nu+\dfrac{1}{2i\hbar}\hat{P}_\nu\left[\hat{X}^\mu,\hat{P}^\nu\right]\\
&=\dfrac{1}{2i\hbar}i\hbar\delta^\mu_\nu\hat{P}^\nu+\dfrac{1}{2i\hbar}\hat{P}_\nu i\hbar g^{\mu\nu}\\
&=\dfrac{1}{2}\left(\delta^\mu_\nu\hat{P}^\nu+ g^{\mu\nu}\hat{P}_\nu\right)\\
&=\dfrac{1}{2}\left(\hat{P}^\mu+\hat{P}^\mu\right)\\
\Aboxed{\dfrac{d\hat{X}^\mu}{d\tau}&=\hat{P}^\mu}
\end{align}$$
For 4-momentum:
$$\begin{align}
\dfrac{d\hat{P}_\mu}{d\tau}&=\dfrac{[\hat{P}_\mu,\hat{H}]}{i\hbar}\\
&=\dfrac{1}{i\hbar}\left[\hat{P}_\mu,\dfrac{1}{2}\left(\hat{P}_\nu\hat{P}^\nu+\hat{M}^2(\hat{X})\right)\right]\\
&=\dfrac{1}{2i\hbar}\left[\hat{P}_\mu,\hat{P}_\nu\hat{P}^\nu\right]+\dfrac{1}{2i\hbar}\left[-i\hbar\partial_\mu,\hat{M}^2(\hat{X})\right]\\
&=\dfrac{1}{2i\hbar}\left[\hat{P}_\mu,\hat{P}_\nu\right]\hat{P}^\nu+\dfrac{1}{2i\hbar}\hat{P}_\nu\left[\hat{P}_\mu,\hat{P}^\nu\right]-\dfrac{1}{2i\hbar}i\hbar\partial_\mu M^2(\hat{X})\\
&=-\dfrac{\hbar}{2i}\left(\mathcal{R}_{\mu\nu}\hat{P}^\nu+\hat{P}_\nu\mathcal{R}_{\mu}^\nu\right)-\dfrac{1}{2}\partial_\mu M^2(\hat{X})\\
\Aboxed{\dfrac{d\hat{P}_\mu}{d\tau}&=\dfrac{i\hbar}{2}\left\{\hat{P}^\nu,\mathcal{R}_{\mu\nu}\right\}-\dfrac{1}{2}\partial_\mu M^2(\hat{X})}
\end{align}$$


### Heisenberg Equation of Motion (Gauge Field)
Define the Hamiltonian as the following:
$$\begin{align}
\hat{H}&=\dfrac{1}{2}\left(\hat{\Pi}_\nu\hat{\Pi}^\nu+\hat{M}^2(\hat{X})\right)\\
\hat{\Pi}_\nu&=\hat{P}_\nu-q\mathcal{A}_\nu(\hat{X})
\end{align}$$
Where $\hat{M}$ is the mass operator, and $\mathcal{A}_\mu(\hat{X})$ is any gauge field acting on the particle.

The general form of the EOM is:
$$\begin{align}
\dfrac{d\hat{O}}{d\tau}&=\dfrac{[\hat{O},\hat{H}]}{i\hbar}+\dfrac{\partial\hat{O}}{\partial\tau}
\end{align}$$
And so we find for 4-position:
$$\begin{align}
\dfrac{d\hat{X}^\mu}{d\tau}&=\dfrac{[\hat{X}^\mu,\hat{H}]}{i\hbar}=\hat{\Pi}^\mu
\end{align}$$
For 4-momentum:
$$\begin{align}
\dfrac{d\hat{P}^\mu}{d\tau}&=\dfrac{[\hat{X}^\mu,\hat{H}]}{i\hbar}=q\hat{\Pi}^\mu\mathcal{F}_{\mu\nu}+\dfrac{i\hbar}{2}\left\{\hat{P}^\nu,\mathcal{R}_{\mu\nu}\right\}-\dfrac{1}{2}\partial_\mu M^2(\hat{X})
\end{align}$$