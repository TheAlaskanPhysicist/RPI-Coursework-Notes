
It has always bothered me that space and time are not treated as observables. While it might not work in the non-relativistic sense, I intend to work through the consequences of this claim.



### First Idea (Forced Uncertainty)
Let the following commutators exist:
$$\begin{align}
[\hat{X}^\mu,\hat{P}^\nu]&=i\hbar g^{\mu\nu} & 
[\hat{X}^\mu,\hat{X}^\nu]&=0 & 
[\hat{P}^\mu,\hat{P}^\nu]&=0
\end{align}$$
Some of the commutators we then get are as follows:
$$\begin{align}
[\hat{X}^\nu,\hat{P}^2]&=+2i\hbar P^\nu & [\hat{X}^2,\hat{P}^\nu]&=+2i\hbar X^\nu
\end{align}$$
$$\begin{align}
[\hat{X}^2,\hat{P}^2]&=4i\hbar\ \hat{X}\cdot\hat{P}\\
\end{align}$$
Using general uncertainty, we then see that:
$$\begin{align}
\Delta\hat{X}^\mu\ \Delta\hat{P}^\nu &=\dfrac{\hbar}{2}|g^{\mu\nu}|\\
\Delta\hat{X}^2\ \Delta\hat{P}^2 &= 2\hbar\left|\braket{\hat{X}\cdot\hat{P}}\right|
\end{align}$$
### Dynamics
Now, for our Dynamics, we can use Heisenberg's equations of motion (free particle):
$$\begin{align}
\dfrac{\partial X^\mu}{\partial\tau}&=\dfrac{i}{\hbar}\left[\hat{H},\hat{X}^\mu\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}\left[P^2,\hat{X}^\mu\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}(-2i\hbar P^\mu)\\
\Aboxed{\dfrac{\partial X^\mu}{\partial\tau}&=\dfrac{P^\mu}{m}}
\end{align}$$
$$\begin{align}
\dfrac{\partial P^\mu}{\partial\tau}&=\dfrac{i}{\hbar}\left[\hat{H},\hat{P}^\mu\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}\left[P^2,\hat{P}^\mu\right]\\
\Aboxed{\dfrac{\partial P^\mu}{\partial\tau}&=0}
\end{align}$$
We can calculate these for the squared operators:
$$\begin{align}
\dfrac{\partial }{\partial\tau}\hat{X}^2
&=\dfrac{i}{\hbar}\left[\hat{H},\hat{X}^2\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}\left[P^2,\hat{X}^2\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}(4i\hbar\ \hat{X}\cdot\hat{P})\\
\Aboxed{\dfrac{\partial }{\partial\tau}\hat{X}^2&=-\dfrac{2}{m}\ \hat{X}\cdot\hat{P}}
\end{align}$$
$$\begin{align}
\dfrac{\partial}{\partial\tau}\hat{P}^2&=\dfrac{i}{\hbar}\left[\hat{H},\hat{P}^2\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}\left[P^2,\hat{P}^2\right]\\
\Aboxed{\dfrac{\partial }{\partial\tau}\hat{P}^2&=0}
\end{align}$$
Momentum squared is constant along its worldline (mass-shell is preserved) and $X^2$ evolves linearly as the inner product of $X\cdot P$.

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





























---






With the general uncertainty principle:
$$\begin{align}
\braket{\Delta A}^2\braket{\Delta B}^2\ge\dfrac{1}{4}\left|\braket{[A,B]}^2\right|\\
\braket{\Delta A}\braket{\Delta B}\ge\dfrac{1}{2}\left|\braket{[A,B]}\right|\\
\end{align}$$
Using $A=\hat{X}^2$ and $B=\hat{P}^2$, we see that:
$$\begin{align}
\braket{\hat{X}^2}\braket{\hat{P}^2}\ge\dfrac{1}{2}\cdot\left|\braket{[\hat{X}^2,\hat{P}^2]}\right|\\
\end{align}$$
Finding the commutator:

Then the uncertainty relation is then:
$$\begin{align}
\braket{\hat{X}^2}\braket{\hat{P}^2}\ge\dfrac{1}{2}\cdot\left|\braket{[\hat{X}^2,\hat{P}^2]}\right|\\
\end{align}$$














### First Idea
Let the following commutators exist:
$$\begin{align}
[\hat{X}^\mu,\hat{P}^\nu]&=i\hbar g^{\mu\nu} & 
[\hat{X}^\mu,\hat{X}^\nu]&=0 & 
[\hat{P}^\mu,\hat{P}^\nu]&=0
\end{align}$$
Then lets look at the commutation of momentum-squared and position:
$$\begin{align}
[\hat{P}^2,\hat{X}^\nu]&=[\hat{P}_\mu\hat{P}^\mu,\hat{X}^\nu]\\
&=\hat{P}_\mu[\hat{P}^\mu,\hat{X}^\nu]+[\hat{P}_\mu,\hat{X}^\nu]\hat{P}^\mu\\
&=\hat{P}_\mu[\hat{P}^\mu,\hat{X}^\nu]+[g_{\mu\alpha}\hat{P}^\alpha,\hat{X}^\nu]\hat{P}^\mu\\
\Aboxed{[\hat{P}^2,\hat{X}^\nu]&=-2i\hbar p^\nu}
\end{align}$$
However, this is an issue since this interferes with the mass shell, since we expect:
$$\begin{align}
[\hat{P}^2,\hat{X}^\nu]&=[m^2c^2,\hat{X}^\nu]\\
&=m^2c^2[1,\hat{X}^\nu]\\
\Aboxed{[\hat{P}^2,\hat{X}^\nu]&=0}
\end{align}$$
We can see the same thing for the spacetime interval:
$$\begin{align}
\Aboxed{[\hat{X}^2,\hat{P}^\nu]&=2i\hbar x^\nu}
\end{align}$$
To fix this, the commutator must be updated to something that satisfies the above.

To allow this to satisfy, we can conjecture the following transformation:
$$\begin{align}
[\hat{X}^\mu,\hat{P}^\nu]&=i\hbar \Phi^{\mu\nu}(X,P)
\end{align}$$
To force the following conditions:
$$\begin{align}
[\hat{P}^2,\hat{X}^\nu]&=0 & [\hat{X}^2,\hat{P}^\nu]&=0
\end{align}$$
We see that $\Phi^{\mu\nu}(X,P)$ must have the form:
$$\begin{align}
\Aboxed{\Phi^{\mu\nu}(X,P)&=g^{\mu\nu}-\dfrac{\hat{X}^\mu\hat{X}^\nu}{X^2}-\dfrac{\hat{P}^\mu\hat{P}^\nu}{P^2}+\text{possible mixed terms}}
\end{align}$$


Let the following commutator exist:
$$\begin{align}
[\hat{X}^\mu,\hat{P}^\nu]&=i\hbar\left(g^{\mu\nu}-\dfrac{\hat{X}^\mu\hat{X}^\nu}{X^2}-\dfrac{\hat{P}^\mu\hat{P}^\nu}{P^2}\right)=i\hbar\Phi^{\mu\nu}(X,P)
\end{align}$$
Then the Hamiltonian can be written as:
$$\begin{align}
\hat{H}=\dfrac{1}{2m}\hat{P}^2
\end{align}$$
Heisenberg's equations of motion then say:
$$\begin{align}
\dfrac{\partial x^\mu}{\partial\tau}&=\dfrac{i}{\hbar}\left[\hat{H},x^\mu\right]\\
&=\dfrac{i}{\hbar}\dfrac{1}{2m}\left(-2i\right)\\
\end{align}$$




















We'll work in special relativity, as I do not want to use GR until absolutely necessary.

In our case of flat spacetime, then we see:
$$\begin{align}
[\hat{X}^0,\hat{P}^0]&=i\hbar\\
[\hat{X}^i,\hat{P}^j]&=i\hbar\delta^{ij}\\
\end{align}$$
We should also expect that the operators obey special relativity, and so:
$$\begin{align}
[\hat{X}^\mu,\hat{X}_\mu]&=\tau^2c^2\hat{I}\\
[\hat{P}^\mu,\hat{P}_\mu]&=m^2c^2\hat{I}
\end{align}$$
Uncertainty relationships should then follow as:
$$\begin{align}
\Delta\hat{X}^\mu\Delta\hat{P}^\nu&\ge\dfrac{\hbar}{2}|g^{\mu\nu}|
\end{align}$$



### Random Dirac
So what I remember is that the gamma matrices satisfy:
$$\begin{align}
\{\gamma^\mu,\gamma^\nu\}&=2g^{\mu\nu}I
\end{align}$$
Using my commutation relation above, we can see that:
$$\begin{align}
\{\gamma^\mu,\gamma^\nu\}&=2\dfrac{[\hat{X}^\mu,\hat{P}^\nu]}{i\hbar}I\\
\end{align}$$





$$\begin{align}
\left(i\hbar\gamma^\mu\partial_\mu-mc\right)\psi(x)=0
\end{align}$$
