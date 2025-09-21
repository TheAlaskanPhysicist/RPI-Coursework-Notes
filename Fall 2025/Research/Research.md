
Network theory being a representation of states and connections between them seems very similar to a configuration space under a small deviation.

The topology of such a configuration space seems very similar to network theory.
 - Continuous vs Discrete?



$$\begin{align}
\dfrac{17x^2+33x+10}{(x-1)(x+1)^2}&=\dfrac{17x^2+34x+17}{(x-1)(x+1)^2}+\dfrac{17x^2-x-7}{(x-1)(x+1)^2}\\
&=\dfrac{17}{(x-1)}-\dfrac{x+7}{(x-1)(x+1)^2}\\
&=\dfrac{17}{(x-1)}-\dfrac{x-1}{(x-1)(x+1)^2}-\dfrac{8}{(x-1)(x+1)^2}\\
\dfrac{17x^2+33x+10}{(x-1)(x+1)^2}&=\dfrac{15}{(x-1)}+\dfrac{2}{x+1}+\dfrac{3}{(x+1)^2}\\
\int\dfrac{17x^2+33x+10}{(x-1)(x+1)^2}\ dx&=15\ln(x-1)+2\ln(x+1)-\dfrac{3}{x+1}\\
\end{align}$$

$$\begin{align}
\dfrac{8}{(x-1)(x+1)^2}&=\dfrac{2}{(x-1)}-\dfrac{2x+6}{(x+1)^2}\\
&=\dfrac{2}{(x-1)}-\dfrac{2}{x+1}-\dfrac{4}{(x+1)^2}
\end{align}$$
$$\begin{align}

\end{align}$$





Entropy is the quantity of the following:
$$\begin{align}
S&=-k\sum_{s\in C}p_s\ln p_s
\end{align}$$



























Consider a system of a set microstates $W$. We want to talk about macrostates.
 - Uniform distribution (or that of maximal entropy) acts like an "identity"
 - Least entropy system also seems to be like an "identity"

Multiplicity deals with how a configuration can be rearranged to have the same physical properties.
In the space of multiplicity, if we consider the state $M_0$ to be the state of maximal multiplicity, we can see that deviations of that multiplicity result from some transformation between states.

Let $n_E$ be the number of states with energy $E$. The multiplicity is:
$$\begin{align}
M&=\dfrac{N!}{\prod_E n_E!} & N&=\sum_E n_E & \text{where}&& E^0&=\sum_E E\cdot n_E
\end{align}$$
The maximal multiplicity is satisfied when the number of particles in each state is equal.
With finite energies, this can get complicated, since that constrains the number of particle states, but it will always try to make a uniform set of states.

What we know is that, when probabilities of individual microstates are equal, then:
$$\begin{align}
S&=\ln\Omega
\end{align}$$
Where $\Omega$ is the number of microstates.





Suppose the current macro-state for $E=5$ and $N=5$ is $(1,1,1,1,1)$.
There is a transform that allows us to do the following:
$$\begin{align}
(1,1,1,1,1)\rightarrow(2,1,1,1,0)
\end{align}$$
This goes from a multiplicity of $120$ to $60$.


5 places to place 2
4 places to place 1
3 places to place 1     / 3! for permutations
2 places to place 1
1 place to place 0