**Author:** Stanley Goodwin
**Date:** March 28th, 2026

---
> We obtained, last semester, that the spatial representation of a free particle in spherical polar coordinates is $\braket{x\lvert Elm}=c_lj_l(kr)Y_l^m(\hat{r})$, where $j_{l}(kr)$ are the spherical Bessel functions (known to be real) and $k=\sqrt{2mE}/\hbar$. Starting from the normalization condition for a free particle
> $$\begin{align}
\braket{E'l'm'\lvert Elm}&=\delta(E-E')\delta_{ll'}\delta_{mm'}
\end{align}$$
> determine the magnitude of the normalization constant $c_l$.

We can insert a completeness relation into the normalization condition:
$$\begin{align}
\braket{E'l'm'\lvert Elm}&=\int\braket{E'l'm'\lvert\vec{x}}\braket{\vec{x}\lvert Elm}\ d^3x\\
&=\int c_{l'}^*j_{l'}^*(k'r)Y_{l'}^{m'*}(\hat{r})\cdot c_lj_l(kr)Y_l^m(\hat{r})\ d^3x\\
&=c_{l'}^*c_l\int r^2j_{l'}^*(k'r)j_l(kr)\ dr\int Y_{l'}^{m'*}(\hat{r})Y_l^m(\hat{r})\ d\Omega\\
&=c_{l'}^*c_l\int r^2j_{l'}^*(k'r)j_l(kr)\ dr\cdot \delta_{ll'}\delta_{mm'}\\
&=|c_{l}|^2\dfrac{\pi}{2k^2}\delta(k-k') \delta_{ll'}\delta_{mm'}\\
\delta(E-E')\delta_{ll'}\delta_{mm'}&=|c_{l}|^2\dfrac{\pi}{2k^2}\dfrac{\hbar^2k}{m}\delta(E-E') \delta_{ll'}\delta_{mm'}
\end{align}$$
Both sides are equal to each other, and so we have the relation:
$$\begin{align}
1&=|c_{l}|^2\dfrac{\pi}{2k^2}\dfrac{\hbar^2k}{m} &\implies&& \Aboxed{|c_{l}|&=\sqrt{\dfrac{2km}{\pi\hbar^2}}}
\end{align}$$
