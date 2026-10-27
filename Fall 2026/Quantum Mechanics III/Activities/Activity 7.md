**Author:** Stanley Goodwin
**Date:** October 16th, 2026

---
## Question 1
> Perform the $p^0$ integration in $$D(x-y)=\int\dfrac{d^4p}{(2\pi)^4}\dfrac{ie^{-ip\cdot(x-y)}}{p^2-m^2}$$for each of the four pole prescriptions. Relate these four results to various two-point vacuum expectation values of the Klein-Gordon scalar field.

We can split the integration into the space and time integrals
$$\begin{align}
D(x-y)&=\int\dfrac{d^4p}{(2\pi)^4}\dfrac{ie^{-ip\cdot(x-y)}}{p^2-m^2}\\
&=\int\dfrac{d^3p}{(2\pi)^3}e^{+i\vec{p}\cdot(\vec{x}-\vec{y})}\int\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}
\end{align}$$
### Solutions for $x_0>y_0$
When this condition is satisfied, this imposes that integration needs to take place in the lower-half plane so that $e^{-iz}$ converges for imaginary components. Thus we have the four pole prescriptions:
$$\begin{align}
A_c&\equiv\left[-R,-E_\vec{p}-\epsilon\right]\cup
\left[-E_\vec{p}+\epsilon,+E_\vec{p}-\epsilon\right]\cup
\left[E_\vec{p}+\epsilon,+R\right]+\left\{Re^{-i\phi}|0<\phi<\pi\right\}\\
\Gamma_{--}&=A_c\cup\left\{-E_\vec{p}-\epsilon e^{-i\phi}|0<\phi<\pi\right\}\cup\left\{+E_\vec{p}-\epsilon e^{-i\phi}|0<\phi<\pi\right\}\\
\Gamma_{-+}&=A_c\cup\left\{-E_\vec{p}-\epsilon e^{-i\phi}|0<\phi<\pi\right\}\cup\left\{+E_\vec{p}-\epsilon e^{+i\phi}|0<\phi<\pi\right\}\\
\Gamma_{+-}&=A_c\cup\left\{-E_\vec{p}-\epsilon e^{+i\phi}|0<\phi<\pi\right\}\cup\left\{+E_\vec{p}-\epsilon e^{-i\phi}|0<\phi<\pi\right\}\\
\Gamma_{++}&=A_c\cup\left\{-E_\vec{p}-\epsilon e^{+i\phi}|0<\phi<\pi\right\}\cup\left\{+E_\vec{p}-\epsilon e^{+i\phi}|0<\phi<\pi\right\}
\end{align}$$
In the limit as $\epsilon\to0^+$ and $R\to\infty$, and by Jordan's Lemma, the contributions from the circular contours enclosing the singularities and the circular contour at infinity also tends to zero, we then have that the principle parts of these integrals are equal to the residues of the enclosed singularities to the path $\Gamma$. Therefore
$$\begin{align}
\Gamma_{--}:&&&\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=-2\pi i\cdot\dfrac{i}{2\pi}\left[\operatorname*{Res}_{z=+E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}+\operatorname*{Res}_{z=-E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}\right]\\
\Gamma_{-+}:&&&\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=-2\pi i\cdot\dfrac{i}{2\pi}\left[\operatorname*{Res}_{z=-E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}\right]\\
\Gamma_{+-}:&&&\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=-2\pi i\cdot\dfrac{i}{2\pi}\left[\operatorname*{Res}_{z=+E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}\right]\\
\Gamma_{++}:&&&\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=-2\pi i\cdot\dfrac{i}{2\pi}\left[0\right]
\end{align}$$
After substituting the residues
$$\begin{align}
\operatorname*{Res}_{z=+E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}
&=\lim_{z\to+E_{\vec{p}}}(z-E_\vec{p})\dfrac{e^{-iz(x_0-y_0)}}{(z-E_\vec{p})(z+E_\vec{p})}
=+\dfrac{e^{-iE_\vec{p}(x_0-y_0)}}{2E_\vec{p}}\\
\operatorname*{Res}_{z=-E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}
&=\lim_{z\to-E_{\vec{p}}}(z+E_\vec{p})\dfrac{e^{-iz(x_0-y_0)}}{(z-E_\vec{p})(z+E_\vec{p})}
=-\dfrac{e^{+iE_\vec{p}(x_0-y_0)}}{2E_\vec{p}}
\end{align}$$
we get that the integrals for each are
$$\begin{align}
\Gamma_{--}:&&&
\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}
=+iE_\vec{p}\sin\left(E_\vec{p}(x_0-y_0)\right)\theta(x_0-y_0)\\
\Gamma_{-+}:&&&
\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}
=-\dfrac{e^{+iE_\vec{p}(x_0-y_0)}}{2E_\vec{p}}\theta(x_0-y_0)\\
\Gamma_{+-}:&&&
\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}
=+\dfrac{e^{-iE_\vec{p}(x_0-y_0)}}{2E_\vec{p}}\theta(x_0-y_0)\\
\Gamma_{++}:&&&
\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=0
\end{align}$$
### Solutions for $x_0<y_0$
For these solutions, we now integrate in the upper-half plane. This means that the integrations that contain the singularities are now opposite where every $\Gamma_-\leftrightarrow\Gamma_+$, and that the residue calculations are $+2\pi i$ since we're going counterclockwise, thus:
$$\begin{align}
\Gamma_{++}:&&&\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=2\pi i\cdot\dfrac{i}{2\pi}\left[\operatorname*{Res}_{z=+E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}+\operatorname*{Res}_{z=-E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}\right]\\
\Gamma_{+-}:&&&\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=2\pi i\cdot\dfrac{i}{2\pi}\left[\operatorname*{Res}_{z=-E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}\right]\\
\Gamma_{-+}:&&&\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=2\pi i\cdot\dfrac{i}{2\pi}\left[\operatorname*{Res}_{z=+E_{\vec{p}}}\dfrac{e^{-iz(x_0-y_0)}}{z^2-E_\vec{p}^2}\right]\\
\Gamma_{--}:&&&\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=2\pi i\cdot\dfrac{i}{2\pi}\left[0\right]
\end{align}$$
Substituting our expressions in now, we get that
$$\begin{align}
\Gamma_{++}:&&&
\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}
=-iE_\vec{p}\sin\left(E_\vec{p}(x_0-y_0)\right)\theta(y_0-x_0)\\
\Gamma_{+-}:&&&
\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}
=+\dfrac{e^{+iE_\vec{p}(x_0-y_0)}}{2E_\vec{p}}\theta(y_0-x_0)\\
\Gamma_{-+}:&&&
\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}
=-\dfrac{e^{-iE_\vec{p}(x_0-y_0)}}{2E_\vec{p}}\theta(y_0-x_0)\\
\Gamma_{--}:&&&
\mathcal{P}\int_{-\infty}^\infty\dfrac{dp^0}{2\pi}\dfrac{ie^{-ip^0\cdot(x_0-y_0)}}{(p^0)^2-E_\vec{p}^2}=0
\end{align}$$
### All-Together
From here, we can combine them pairwise to get nice solutions
$$\begin{align}
\Gamma_{--}:&&
G_A&=iE_\vec{p}\sin\left(E_\vec{p}(x_0-y_0)\right)\theta(x_0-y_0)\\
\Gamma_{++}:&&
G_R&=iE_\vec{p}\sin\left(E_\vec{p}(y_0-x_0)\right)\theta(y_0-x_0)\\
\Gamma_{-+}:&&
G_F^{(1)}&=-\dfrac{e^{+iE_\vec{p}|x_0-y_0|}}{2E_\vec{p}}\\
\Gamma_{+-}:&&
G_F^{(2)}&=+\dfrac{e^{-iE_\vec{p}|x_0-y_0|}}{2E_\vec{p}}
\end{align}$$
---


