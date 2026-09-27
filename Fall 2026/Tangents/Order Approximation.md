



Suppose we have a phase space of particles, what is the best way to describe the system in a finite number of parameters? That is the question I work with.

The same way that a Taylor Series can be made, I think order parameters tend to be similar. There could be approximation that can't be "done with a Taylor series" like $e^{-1/x}$.

What of order parameters are similar to $\frac{1}{(z-z_0)^p}$, so first order has a scale factor 1.



Critical points act like a singularities. It is a perturbative approach.



Start with a spinor Hamiltonian
$$\begin{align}
H&=\sum_{a\in\left\{1,x,y,z\right\}}\bigotimes_{i=1}^L\sigma^{a_i}_i
\end{align}$$






When doing a Taylor Series, we assume to some effect that the weight of the likelihood of an element from a domain is uniform. For example, in approximating $\sin(x)$ over $x\in\mathbb{R}$, the likelihood of choosing any particular value for $x$ is equal. This is why better approximation methods exist for restricted domains, where we have a "weighting" of $1$ for elements in that domain, and $0$ for elements outside that domain.

The difficulty is when a function has a singularity at a point $x=a$. This becomes more transparent when our domain is finite, so that weighting are like probabilities.

Suppose we have a function $f(x)$ that is defined for all integers between $c_1$ and $c_2$. We know that for each element in the domain, there is an associated weight (unnormalized probability) that encodes the level of "importance" of that element. For example, if this function almost always have an input of $c_1$, then an approximation should prioritize getting $f(c_1)$ more accurate as opposed to others, if needed.

The Taylor Series, in a sense, is when we have a domain of uniform weights. This breaks when we have singularities, since certain value of $f(x=a)$ are undefined or genuinely infinite.


## Example of Approximations
Suppose we have the function $f(x)=x^2$ over the interval $x\in[0,1]$. We can associate a "cost" and minimize an approximation in a basis by selecting appropriate values. If each element of the domain is equally likely, then each cost weight is identical. If certain numbers are more likely to end up as inputs, then the function can be skewed more to accurately represent their approximations for those values, even at the cost of others.

In the case where a weight is extremely high around a point $x=a$, with all other inputs combined being unlikely, then the constant approximation is best for $0$th and $1$st order. If there are two points who are very likely, and all others combined are less, then the approximation is a perfect line through those $2$ points within tolerance.

Singularities effectively hijack the weighting function $w(x)$ by making their value much higher. In that case, after normalization, all other weights $w(x\ne a)$ are very small, so their error contribution are small. The function "prioritizes" the value $x=a$, because in most cases being the input being $x=a$ the best response it has with 1 number is just the value $f(a)$. 