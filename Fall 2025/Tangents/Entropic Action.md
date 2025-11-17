Author: Stanley Goodwin
Date: 11/13/2025

## Main supporting idea
In Quantum Mechanics, we see a lot of different equations that tend to see a form to the following:
$$\begin{align}
e^{-ipx/\hbar} && e^{-iEt/\hbar} && e^{-\tfrac{i}{\hbar}\int p\ dx}
\end{align}$$
But when we look at general mechanics, we see that this new exponential operator in some sense is just a simplification of some general action principle:
$$\begin{align}
e^{-iS/\hbar}
\end{align}$$
This kind of exponential under a Wick rotation effectively turns Minkowski space into Euclidean space, and so what I considered is that perhaps there's an analogous:
$$\begin{align}
e^{-ET^{-1}/k_B}
\end{align}$$
And thus, similar to what I had heard about inverse temperature being analogous to time, what if we consider some generalized Energy per Unit Temperature (Entropy $\Sigma$) as the following:
$$\begin{align}
e^{-\Sigma/k_B}
\end{align}$$


## Wick Transformation
Starting with the transition amplitude concept:
$$\begin{align}
A&=\int \mathcal{D}\phi\ e^{-\tfrac{i}{\hbar}S[\phi]}
\end{align}$$
Applying the wick rotation to it $t=-i\tau$, $S\rightarrow -iS_W$, Minkowski becomes Euclidean:
$$\begin{align}
e^{-\tfrac{i}{\hbar}S[\phi]}\rightarrow e^{\tfrac{1}{\hbar}S_W[\phi]}
\end{align}$$
I'm not sure what we have to do from here, but what we'd do is we extract the $1/\hbar$ and replace it with a $1/k$, which means effectively multiplying it with:
$$\begin{align}
\alpha'=\dfrac{\hbar}{kT}
\end{align}$$
In order to have the "information" be expressed in terms of entropy, the coefficient to transform it is as follow:
$$\begin{align}
\Sigma[\phi]&=\dfrac{\hbar}{k}S_W[\phi]
\end{align}$$
Probability density is just then:
$$\begin{align}
\mathcal{P}[\phi]&\propto e^{-\Sigma[\phi]/k} &\text{or}&&\mathcal{P}[\phi]&\propto e^{-S_W[\phi]/\hbar}\\
Z&=\int \mathcal{D}\phi\ e^{-\Sigma[\phi]/k}
\end{align}$$
We can then define a free energy:
$$\begin{align}
F(T)&=-kT\ln Z(\beta)\\
&=-kT\ln\left(e^{-\Sigma[\phi^*]/k}\right)\\
&=-kT\left(-\Sigma[\phi^*]/k\right)\\
F(T)&=T\cdot\Sigma[\phi^*]
\end{align}$$
This is pretty much the form of purely energy in entropy $TS$. We can then say that around this special field value $\phi^*$, we see that:
$$\begin{align}
\Sigma&=\dfrac{F(T)}{T}
\end{align}$$
So it's the free energy divided by temperature. Quite like entropy. However, it might not have the same characteristics as entropy, and that will be explored further down.

What I conjecture is that **minima** $\Sigma$ are akin to least action, and will correspond to thermodynamic equilibrium with minimal free energy per unit temperature (based off of what I've seen in statistical mechanics over the last 2 years).

## Formalizing
Start with the Minkowski action (as example) for a real scalar field $\phi(x)$:
$$\begin{align}
S[\phi]&=\int\left(\dfrac{1}{2}\partial_\mu\phi\partial^\mu\phi-\dfrac{1}{2}m^2\phi^2\right)\ d^4x
\end{align}$$
Under a wick rotation $t\rightarrow -i\tau$ to get this new Euclidean action $S_E$:
$$\begin{align}
S_E[\phi]&=\int\left(\dfrac{1}{2}(\nabla\phi)^2+\dfrac{1}{2}m^2\phi^2\right)\ d^4x
\end{align}$$
We can then define this entropic action as $\Sigma$:
$$\begin{align}
\Sigma[\phi]&\equiv \dfrac{\hbar}{k}S_E[\phi]
\end{align}$$
We can also define then the local information density as:
$$\begin{align}
\mathcal{E}&=\alpha\left(\dfrac{1}{2}(\nabla\phi)^2+\dfrac{1}{2}m^2\phi^2\right)+\text{const.}
\end{align}$$


## Entropic Noether's Theorem
Let $\phi(x)$ be a field on Euclidean spacetime $x\in\mathbb{R}^d$, then define entropic action:
$$\begin{align}
\Sigma[\phi]&=\int\mathcal{E}\left(\phi, \partial_\mu\phi\right)\ d^dx
\end{align}$$
Under a small field transformation $\phi(x)\rightarrow\phi'(x)+\epsilon\delta\phi(x)$:
$$\begin{align}
\delta\Sigma[\phi]&=\int\left(\dfrac{\partial\mathcal{E}}{\partial\phi}\delta\phi+\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\partial_{\mu}\delta\phi\right)\ d^dx\\
&=\int\left(\dfrac{\partial\mathcal{E}}{\partial\phi}+\partial_{\mu}\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\right)\delta\phi\ d^dx+\epsilon\int\partial_{\mu}\left(\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\delta\phi\right)\ d^dx\\
\end{align}$$
Then define the Noether current density as:
$$\begin{align}
\delta\Sigma[\phi]&=\int\left(\dfrac{\partial\mathcal{E}}{\partial\phi}\delta\phi+\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\partial_{\mu}\delta\phi\right)\ d^dx\\
\Aboxed{j^\mu(x)&=\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\delta\phi-K^\mu(x)}
\end{align}$$
Where $K^\mu$ is any derivative piece that comes from $\delta\mathcal{E}=\partial_\mu K^\mu$ when a change of coordinates happens (transformation) or $\delta\mathcal{E}$ is a divergence.
### Classical Entropic Noether
If the transform is a symmetry of entropy density $\mathcal{E}$ ($\delta\mathcal{E}=\partial_\mu K^\mu$), then:
$$\begin{align}
&&\delta\Sigma[\phi]&=\int\left(\dfrac{\partial\mathcal{E}}{\partial\phi}-\partial_{\mu}\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\right)\delta\phi\ d^dx+\epsilon\int\partial_{\mu}\left(\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\delta\phi\right)\ d^dx\\
\implies&&
\Aboxed{0&=\dfrac{\partial\mathcal{E}}{\partial\phi}-\partial_{\mu}\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}}
\end{align}$$
Since $\delta\Sigma[\phi]$ vanishes, it implies the local conservation law:
$$\begin{align}
j^\mu(x)&=\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\delta\phi-K^\mu(x)\\
\partial_\mu j^\mu(x)&=\partial_\mu\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\delta\phi-\partial_\mu K^\mu(x)\\
&=-\dfrac{\partial\mathcal{E}}{\partial\phi}\delta\phi-\delta\mathcal{E}\\
\Aboxed{\partial_\mu j^\mu(x)&=0}
\end{align}$$
So when this parameter is extremized, the information current is 0.

### Statistical Implication
In the entropic-field statistical theory, the probability weight for configurations is:
$$\begin{align}
\mathcal{P}[\phi]\propto e^{-\Sigma[\phi]/k} \iff \Sigma[\phi]=-k\ln\mathcal{P}[\phi]+C
\end{align}$$
Expectations values are then:
$$\begin{align}
\braket{A}&=\dfrac{1}{Z}\int \mathcal{D}\phi\ A[\phi]\ e^{-\Sigma[\phi]/k} & Z&=\int \mathcal{D}\phi\ e^{-\Sigma[\phi]/k}
\end{align}$$
Under an arbitrary change of variables $\phi(x)\rightarrow\phi'(x)+\epsilon\delta\phi(x)$, if the measure of $\mathcal{D}\phi$ is invariant, the invariance under transform gives:
$$\begin{align}
0&=\int \mathcal{D}\phi\ \delta\left(e^{-\Sigma[\phi]/k}\right)=-\dfrac{\epsilon}{k}\int\mathcal{D}\phi\ \delta\left(\Sigma[\phi]\right)\ e^{-\Sigma[\phi]/k}
\end{align}$$
We expect that variation of entropy $\Sigma$ to vanish, and so:
$$\begin{align}
\braket{\delta\Sigma[\phi]}&=\dfrac{1}{Z}\int\mathcal{D}\phi\ \delta\left(\Sigma[\phi]\right)\ e^{-\Sigma[\phi]/k}=0
\end{align}$$
Then, like before, we can see that:
$$\begin{align}
\Aboxed{\braket{\delta\Sigma[\phi]}&=\braket{\partial_\mu j^\mu(x)}=0}
\end{align}$$
So even under non-extremal values of $\Sigma$, ensemble-averaged information current is conserved, and this the divergence averages to zero under this weighting term.

We can also define a relative information difference:
$$\begin{align}
\Sigma[\phi]-\Sigma'[\phi]&=-k\ln\mathcal{P}[\phi]+C+k\ln\mathcal{Q}[\phi]-C\\
\Delta\Sigma[\phi]&=-k\ln\left(\dfrac{\mathcal{P}[\phi]}{\mathcal{Q}[\phi]}\right)\\
\end{align}$$
Where $\mathcal{Q}$ is the probability at a reference. When integrated over an ensemble:
$$\begin{align}
\mathcal{S}&\equiv -k\int\mathcal{D}\phi\ \mathcal{P}[\phi]\ln\left(\dfrac{\mathcal{P}[\phi]}{\mathcal{Q}[\phi]}\right)
\end{align}$$
I've seen something similar in Statistics so that's why I defined this functional.


## Interpretation
Suppose this value $\Sigma[\phi]$ truly is some measure of *information* functional of a field configuration.
$$\begin{align}
\Sigma[\phi]&=\int\mathcal{E}\left(\phi, \partial_\mu\phi\right)\ d^dx
\end{align}$$
 - When $\Sigma[\phi]$ is high, probability is low, and thus informationally costly.
 - When $\Sigma[\phi]$ is low, probability is high, and thus informationally freer, and/or natural.
The term inside the integrand, $\mathcal{E}(x)$, is the *local information density* at point $x$.
$$\begin{align}
\mathcal{E}&=\alpha\left(\dfrac{1}{2}(\nabla\phi)^2+\dfrac{1}{2}m^2\phi^2\right)+\text{const.}
\end{align}$$
 - The $(\nabla\phi)^2$ term, in some sense, gives an information penalty for large variation in information in field. Smoother fields (less variation) need less information to encode.
 - The $m^2\phi^2$ term gives a penalty to large values in the field, but I'm unsure what the physical interpretation of this would be. Perhaps some notion of higher physical density requiring more information, thus being entropically high to avoid the Pauli exclusion principle?
The Euler-Lagrange equation for Information Density:
$$\begin{align}
&&\delta\Sigma[\phi]&=\int\left(\dfrac{\partial\mathcal{E}}{\partial\phi}+\partial_{\mu}\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\right)\delta\phi\ d^dx+\epsilon\int\partial_{\mu}\left(\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\delta\phi\right)\ d^dx\\
\implies&&
\Aboxed{0&=\dfrac{\partial\mathcal{E}}{\partial\phi}+\partial_{\mu}\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}}
\end{align}$$
 - Extremizes information, which in our case is Least-Information, which means Maximizing entropy. Pretty much identical to least action but in this information space.
 - Classical paths are those of which require are the least informational-complex fields.
 - Quantum fluctuations have configurations weighted by their informational cost.
The partition function becomes some sense of "Total Information Volume":
$$\begin{align}
Z&=\int \mathcal{D}\phi\ e^{-\Sigma[\phi]/k}
\end{align}$$
 - Effectively encodes the information volume of all field configurations, with $\Sigma/k$ being the dimensionless information cost.
Correlators measure in a field that shares information between itself in a field:
$$\begin{align}
G(\vec{x},\vec{x}')&=\braket{\phi(x)\phi(x')}
\end{align}$$
 - How much information about $\phi(x)$ is shared with $\phi(x')$ in the case of a maximum-entropy ensemble (in equilibrium) defined by $\Sigma$.
 - Less correlation means some form of the loss of shared information with distance.
 - The mass $m$ would likely control for the exponential decay, so we would see correlation functions of the form:
$$\begin{align}
G(\vec{x},\vec{x}')&\sim \dfrac{e^{-mr}}{r^{d-2}}
\end{align}$$
 - This means that mass is inversely correlated with length in information space.
	 - Small mass = Information spreads out
	 - Large mass = Information localized
Any symmetry that leaves the information $\Sigma$ invariant implies:
$$\begin{align}
j^\mu(x)&=\dfrac{\partial\mathcal{E}}{\partial(\partial_{\mu}\phi)}\delta\phi-K^\mu(x)\\
\partial_\mu j^\mu(x)&=0
\end{align}$$
 - This defines the sense of "Information charge" since there's an associated current.
 - The directions in configuration space where information cost doesn't change is what a symmetry in $\Sigma$ would actually encode.
 - Continuous symmetries therefore imply **informational degeneracies**.

### Informational Coupling
Starting out with our information density:
$$\begin{align}
\mathcal{E}&=\alpha\left(\dfrac{1}{2}(\nabla\phi)^2+\dfrac{1}{2}m^2\phi^2\right)+\text{const.}
\end{align}$$
We could just as easily add new terms in order to expand the system.

For example, if we wanted correlated information, we could represent a term as:
$$\begin{align}
q\phi^2\chi
\end{align}$$
Information in $\phi$ and $\chi$ are **not independent** but are correlated. Changes in one of the terms automatically enforces a constraint on the other. To be clear $\chi$ is another field like $\phi$. The term $q$ is just some stand-in for a coupling constant.

Interactions could be mutual information terms built into the information functional.


## Example Potential
Suppose we had the following potential in Euclidean Space:
$$\begin{align}
V(\phi)&=-\dfrac{1}{2}m^2\phi^2+\dfrac{1}{4}\lambda\phi^4
\end{align}$$
The field $\phi=0$ has low information density because this is an unstable equilibrium at $0$ by the mass term. However, the $\phi^4$ term will always grow larger than the $\phi^2$ term in the large field limit.

Suppose we have a field value $\phi=\eta$, then:
$$\begin{align}
V'(\eta)&=-m^2\eta+\lambda\eta^3\\
0&=\eta\left(\eta^2-\dfrac{m^2}{\lambda}\right)\\
\end{align}$$
If you check these, you'll see that $\eta=\dfrac{|m|}{\sqrt{\lambda}}$ is a global minimum of information, relative to the previous $0$-field case. However, before this $\lambda$ term, there was only 1 ground state. This is similar to how there are 2 degenerate ground states in the Transverse-Field Ising Model that turn into 1 ground state as you increase the field from 0.

The symmetric state becomes informationally disfavored. The broken symmetry states are informationally preferred, and thus a phase transition occurs.


