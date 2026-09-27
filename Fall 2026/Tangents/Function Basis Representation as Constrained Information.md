Date: 7/22/2026

I've recently had thoughts about representations when it comes to functions. Over a particular domain, there is a large set of functions that can exist in the space, but the choice of ones basis is usually influenced by the constraints of the system. In this document, I would like to elaborate more on this system as a concept and rediscover function spaces.

Suppose that we have some domain $D$, then there exists a set of functions that exist on this domain without all other previous constraint. Suppose then we introduce a basis onto this set. In an incompressible world of highest information entropy, we would expect that the set of all functions uses each basis equally as often, the same way that in 3D space that you are just as likely to move in forward and back in each axis, so any choice of basis would represent the system with the same "efficiency." However, what we know is that a lot of systems are constrained function spaces, and such constraints would bias a uniform basis system to a set of basis elements that are more likely used, and thus a uniform basis system would be overly encoding.

## Idea 1: Compression of Sets of Numbers
Suppose we have a set of numbers valid in any choice of domain. If the set of all subsets of this domain is uniformly selected (and thus not not constructed by some underlying pattern), we would expect that any subset with $N$ elements could only be encoded minimally akin to trying to compress random noise. While there exists schemes for individual subsets, or groups of subsets, for all subsets there is a local minimum in how we encode these systems.

Now suppose instead we require that the scheme selection for subsets is patterned such as the prime numbers. Sets of prime numbers aren't uniformly sampled, and instead do have a pattern. The naive way to pattern such sets is for the "index" to be the prime numbers themselves. This would be identical to the set of $N$ primes being the numbers in and of themselves. An alternative scheme that yields the same outcome, but is real-world smaller is using the index of each prime in the sequence they are generated. I.e. the set of $N$ primes is represented by their indices. However, in terms of information, these representations are actually identically complex, as the isomorphism of prime value to prime index is 1:1.


## Ideas 2: Functional Compression
The main premise of this idea stems from starting from an example of degree-$n$ polynomials. Suppose we have a domain of all polynomials of degree $n$ or lower, then a trivial basis for the set of all these functions would be
$$\begin{align}
\mathbb{R}_n[x]:\left\{1,x,x^2,\dots\right\}
\end{align}$$
however this is predicated on the idea that each coefficient for these powers of $x$ are equally represented on the space of functions we want to later model. Since our function space is *all* degree-$n$ polynomials, and that elements of this space are assumed to be sampled from uniformly, then our choice of basis doesn't actually matter in terms of compressibility. We could just as easily write a basis like
$$\begin{align}
\mathbb{R}_n[x]:\left\{3,\pi x-e,x^2-x,\dots\right\}
\end{align}$$
or really any other basis thereof since the span of this basis is identical. For our later discussion, we'll want to impose that the sampling from this space *might not be uniform*, and so there might exist bases that require less information to encode.

Suppose now we have the set of all degree 2 polynomials over all real numbers. We will also constraint the space of sampled functions to be of polynomials with *real* roots, where the weight of polynomials with complex roots is $0$, and the weight of polynomials with real roots is identical between all. The naive representation for our basis would start similar to previous, being
$$\begin{align}
\mathbb{R}_2[x]:\left\{1,x,x^2\right\}\to f(x)=ax^2+bx+c
\end{align}$$
With the imposed condition that the roots must be real, we need that
$$\begin{align}
b^2-4ac&\ge0 &\to&& c\le \frac{b^2}{4a}
\end{align}$$
We went from our parameter space being $\mathbb{R}\backslash{\{0\}}\times\mathbb{R}^2$ to now being smaller because of this conditional. For $a\gt0$, the set of $(b,c)$ pairs is all points *outside* the parabola $\frac{b^2}{4a}$. For $a<0$, the set of $(b,c)$ pairs is all points *inside* the parabola $\frac{b^2}{4a}$. Something of note is that for $a$ and $-a$ choices, the total area of outside and inside the parabola is the set of all $(b,c)$ pairs, but this only accounts for a total half of the points it covered initially. When $a>0$, there are more $(b,c)$ pair points, which means that this basis is not the most optimal in order to decrease information. Effectively, this condition removes half of the $(b,c)$ points, but unbalanced for the sign of $a$.

## Idea 3: PCA
We'll want to use statistics to solve this kind of problem, especially ones that come from arbitrary weights and conditions. Suppose we have polynomials of degree $N$ such that
$$\begin{align}
\mathbb{R}_N[x]:\left\{1,x,x^2,x^3,\dots\right\}\to f(a_0,a_1,a_2,\dots;x)=a_0+a_1x+a_2x^2+a_3x^3+\dots
\end{align}$$
These polynomials can be represented as a column vector $\vec{a}$. The weighted mean of the polynomials in this vector form is then
$$\begin{align}
\vec\mu&=\int_{\mathbb{R}^N}p(\vec{a})\ \vec{a}\ d^Na &&& \int_{\mathbb{R}^N}p(\vec{a})\ d^Na&=1
\end{align}$$
The covariance of the polynomials vector is then
$$\begin{align}
\Sigma&=\int_{\mathbb{R}^N}p(\vec{a})(\vec{a}-\vec\mu)(\vec{a}-\vec\mu)^T\ d^Na
\end{align}$$
This matrix can then be used to find the eigenvalues/eigenvectors. The magnitude of the eigenvalues gives the notion of how strongly weighted that polynomial basis element is.

### PCA with Real-Root Degree-2 Polynomials
For the set of all degree 2 polynomials, we now impose the condition so that the probability of accessing a complex-root polynomial is 0, and all else are equally weighted. The solution to optimize the basis for this kind of system is
$$\begin{align}
\mathbb{R}_2[x]:\left\{1+x^2,x,1-x^2\right\}\to f(x)=a(1+x^2)+bx+c(1-x^2)
\end{align}$$
