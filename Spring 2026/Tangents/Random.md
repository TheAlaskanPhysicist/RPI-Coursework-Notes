
We can differentiate both sides with respect to $\lambda$ as:
$$\begin{align}
\dfrac{d}{d\lambda}(n\lambda)&=\dfrac{d}{d\lambda}(2d\sin\theta)\\
n\dfrac{d\lambda}{d\lambda}+\lambda\dfrac{d n}{d\lambda}&=2\dfrac{d(d)}{d\lambda}\sin\theta+2d\dfrac{d\theta}{d\lambda}\dfrac{d}{d\theta}(\sin\theta)\\
n+\lambda\dfrac{d n}{d\lambda}&=2\dfrac{d(d)}{d\lambda}\sin\theta+2d\dfrac{d\theta}{d\lambda}\cos\theta\\
\Aboxed{\dfrac{d\theta}{d\lambda}&=\dfrac{n+\lambda\dfrac{d n}{d\lambda}-2\dfrac{d(d)}{d\lambda}\sin\theta}{2d\cos\theta}}
\end{align}$$
We want to see the behavior of $\theta$ under constant diffraction order $n$ and displacement $d$, and so:
$$\begin{align}
\Aboxed{\dfrac{d\theta}{d\lambda}&=\dfrac{n}{2d}\tan\theta}
\end{align}$$



We want to see the behavior of $\theta$ vs $\lambda$, so we partially differentiate with respect to $\lambda$
$$\begin{align}
\dfrac{\partial}{\partial\lambda}(n\lambda)&=\dfrac{\partial}{\partial\lambda}(2d\sin\theta) &\implies&& 
n&=2d\dfrac{\partial\theta}{\partial\lambda}\cos\theta
\end{align}$$
Rearranging, the relation takes the form:
$$\begin{align} 
\dfrac{\partial\theta}{\partial\lambda}&=\dfrac{n}{2d\cos\theta}=\dfrac{n}{2d}\sec\theta
\end{align}$$
If you substitute our diffraction relation $n\lambda=2d\sin\theta$, we can find finally:
$$\begin{align} 
\dfrac{\partial\theta}{\partial\lambda}&=\dfrac{2d\sin\theta}{2d\lambda\cos\theta}=\dfrac{\tan\theta}{\lambda}
\end{align}$$



$$\begin{align} 
\theta_\text{new}-\theta_\text{old}&=\dfrac{\tan\theta_\text{old}}{\lambda_\text{old}}\left(\lambda_\text{new}-\lambda_\text{old}\right)
\end{align}$$


We need the following expansion for higher-order:
$$\begin{align}
\dfrac{\partial^k}{\partial\lambda^k}f^{(m-1)}(\theta)
&=\dfrac{\partial^{k-1}}{\partial\lambda^{k-1}}\left(\dfrac{\partial}{\partial\lambda}\dfrac{\partial^{m-1}f}{\partial\theta^{m-1}}\right)\\
&=\dfrac{\partial^{k-1}}{\partial\lambda^{k-1}}\left(\dfrac{\partial\theta}{\partial\lambda}\dfrac{\partial^{m}f}{\partial\theta^{m}}\right)\\
\dfrac{\partial^k}{\partial\lambda^k}f^{(m-1)}(\theta)&=\dfrac{\partial\theta}{\partial\lambda}\dfrac{\partial^{k-1}}{\partial\lambda^{k-1}}\left(\dfrac{\partial^{m}f}{\partial\theta^{m}}\right)+\dfrac{\partial^{m}f}{\partial\theta^{m}}\dfrac{\partial^{k}\theta}{\partial\lambda^{k}}
\end{align}$$
Define the following functions for seeing the recursion:
$$\begin{align}
F^{k,m}&=\dfrac{\partial^k}{\partial\lambda^k}f^{(m)}(\theta) &
\Theta^{(k)}&=\dfrac{\partial^k\theta}{\partial\lambda^k}
\end{align}$$
Substituting, we get the following:
$$\begin{align}
F^{k,m-1}&=\Theta^{(1)}F^{k-1,m}+f^{(m)}\Theta^{(k)}
\end{align}$$
If we shift the left to be of the form of the right:
$$\begin{align}
F^{k-1,m}&=\Theta^{(1)}F^{k-2,m+1}+f^{(m+1)}\Theta^{(k-1)}\\
F^{k,m-1}&=\left(\Theta^{(1)}\right)^2F^{k-2,m+1}+f^{(m+1)}\Theta^{(1)}\Theta^{(k-1)}+f^{(m)}\Theta^{(k)}
\end{align}$$
Doing it another time:
$$\begin{align}
F^{k-2,m+1}&=\Theta^{(1)}F^{k-3,m+2}+f^{(m+2)}\Theta^{(k-2)}\\
F^{k,m-1}&=\left(\Theta^{(1)}\right)^3F^{k-3,m+2}+f^{(m+2)}\left(\Theta^{(1)}\right)^2\Theta^{(k-2)}+f^{(m+1)}\Theta^{(1)}\Theta^{(k-1)}+f^{(m)}\Theta^{(k)}
\end{align}$$
We can conjecture the following:
$$\begin{align}
F^{k,m-1}&=\left(\Theta^{(1)}\right)^NF^{k-N,m-1+N}+\sum_{i=0}^{N-1}f^{(m+i)}\left(\Theta^{(1)}\right)^i\Theta^{(k-i)}
\end{align}$$
When we let $N=k$, we get the following:
$$\begin{align}
F^{k,m-1}&=\left(\Theta^{(1)}\right)^kF^{0,k+m-1}+\sum_{i=0}^{k-1}f^{(m+i)}\left(\Theta^{(1)}\right)^i\Theta^{(k-i)}\\
\dfrac{\partial^k}{\partial\lambda^k}f^{(m-1)}&=\left(\Theta^{(1)}\right)^kf^{(k+m-1)}+\sum_{i=0}^{k-1}f^{(m+i)}\left(\Theta^{(1)}\right)^i\Theta^{(k-i)}
\end{align}$$






### Diffraction
Suppose we have the equation:
$$\begin{align}
n\lambda&=2d\sin\theta &\implies&& \lambda&=\dfrac{2d}{n}\sin\theta &\text{or}&& \theta&=\sin^{-1}\left(\dfrac{n\lambda}{2d}\right)
\end{align}$$
Then we have that $f(\theta)=\tfrac{2d}{n}\sin\theta$. The relation we want to look at is the $m=1$ case:
$$\begin{align}
\dfrac{\partial^k}{\partial\lambda^k}f&=\left(\Theta^{(1)}\right)^kf^{(k)}+\sum_{l=0}^{k-1}f^{(l+1)}\left(\Theta^{(1)}\right)^l\Theta^{(k-l)}
\end{align}$$
We can calculate each of these components:
$$\begin{align}
f^{(k)}&=\dfrac{2d}{n}i^{k}\left(\dfrac{e^{i\theta}-(-1)^{k}e^{-i\theta}}{2i}\right)\\
f^{(l+1)}&=\dfrac{2d}{n}i^{l+1}\left(\dfrac{e^{i\theta}-(-1)^{l+1}e^{-i\theta}}{2i}\right)\\
\Theta^{(k-l)}&=\left(\dfrac{n}{2d}\right)^{k-l}\dfrac{\partial^{k-l}}{\partial x^{k-l}}\left[\sin^{-1}\left(x\right)\right],& x&=\dfrac{n\lambda}{2d}\\
\left(\Theta^{(1)}\right)^k&=\left(\dfrac{n}{2d}\right)^{k}\left(\dfrac{\partial}{\partial x}\left[\sin^{-1}\left(x\right)\right]\right)^k\\
\left(\Theta^{(1)}\right)^l&=\left(\dfrac{n}{2d}\right)^{l}\left(\dfrac{\partial}{\partial x}\left[\sin^{-1}\left(x\right)\right]\right)^l
\end{align}$$
Define the following trigonometric functions:
$$\begin{align}
T_k^{(0)}(\theta)&=\begin{cases}
i\sin\theta&k\in\text{Even}\\
\cos\theta&k\in\text{Odd}
\end{cases} &
T_k^{(1)}(\theta)=\dfrac{d}{d\theta}T_k^{(0)}(\theta)=iT_{k+1}^{(0)}(\theta)&=\begin{cases}
i\cos\theta&k\in\text{Even}\\
-\sin\theta&k\in\text{Odd}
\end{cases}
\end{align}$$
Then the $f$ derivatives become:
$$\begin{align}
f^{(k)}&=\dfrac{2d}{n}i^{k-1}T_k^{(0)}(\theta) & 
f^{(l+1)}&=\dfrac{2d}{n}i^{l}T_{l+1}^{(0)}(\theta)=
\end{align}$$
If we substitute this back into our relation, we have:
$$\begin{align}
\dfrac{\partial^k}{\partial\lambda^k}f&=\left(\dfrac{n}{2d}\right)^{k-1}i^{k-1}T_k^{(0)}(\theta)\left(\dfrac{\partial}{\partial x}\left[\sin^{-1}\left(x\right)\right]\right)^k\\
&+\left(\dfrac{n}{2d}\right)^{k-1}\sum_{l=0}^{k-1}i^{l-1}T_l^{(1)}(\theta)\left(\dfrac{\partial}{\partial x}\left[\sin^{-1}\left(x\right)\right]\right)^l\dfrac{\partial^{k-l}}{\partial x^{k-l}}\left[\sin^{-1}\left(x\right)\right]
\end{align}$$
We want to evaluate this system around a known initial condition:
$$\begin{align}
\lambda&=\lambda_0 & x_0&=\dfrac{n\lambda_0}{2d} & \theta_0&=\sin^{-1}\left(x_0\right)
\end{align}$$
We can then write:
$$\begin{align}
\left.\dfrac{\partial^k}{\partial\lambda^k}f\right|_{\lambda=\lambda_0}&=
\left(\dfrac{n}{2d}\right)^{k-1}\left(1-x_0^2\right)^{-k/2}i^{k-1}T_k^{(0)}(\theta_0)\\
&+\left(\dfrac{n}{2d}\right)^{k-1}\left(1-x_0^2\right)^{-k/2}\sum_{l=0}^{k-1}i^{l-1}T_l^{(1)}(\theta_0)\dfrac{P_{k-l-1}(x_0)}{\left(1-x_0^2\right)^{(k-l-1)/2}}
\end{align}$$
Where we have the polynomials:
$$\begin{align}
P_{n-1}(x)&=(1-x^2)^{n-1/2}\dfrac{\partial^{n}}{\partial x^{n}}\left[\sin^{-1}\left(x\right)\right]\\
T_k^{(0)}(\theta)&=\begin{cases}
ix&k\in\text{Even}\\
\sqrt{1-x^2}&k\in\text{Odd}
\end{cases} \\
T_l^{(1)}(\theta)&=\begin{cases}
i\sqrt{1-x^2}&l\in\text{Even}\\
-x&l\in\text{Odd}
\end{cases}
\end{align}$$



















Interesting idea for inverses for a function. Suppose we have a function $y=y(x)$. We want to be able to represent its inverse $x=x(y)$. I postulate we can project this function into this new space.

Any function that is presentable in $x$ can be written as:
$$\begin{align}
f=\int\ket{x}\braket{x\lvert f}=
\end{align}$$












In differentials, we know the following forms bases in space:
$$\begin{align}
\dfrac{d}{dx}&\to\ket{x} & dx\to\bra{x}
\end{align}$$
For an arbitrary function, we can expand in this basis:
$$\begin{align}
f&=\int df=\int\dfrac{df}{dx}dx=\int\braket{f\lvert x}\bra{x}=\int\braket{f\lvert x}\bra{x}=\int\braket{f\lvert x}\bra{x}
\end{align}$$








$$\begin{align}
f&=\int df=\int\dfrac{df}{dx}dx=\int\braket{f\lvert x}\bra{x}=\int\braket{f\lvert x}\bra{x}=\int\braket{f\lvert x}\bra{x}
\end{align}$$
The assumption is that $x$ is a complete basis for this function, which is reasonable on construction.








To do this, we will use the following representation for projection:
$$\begin{align}
f&=\int df=\int\dfrac{df}{dx}dx=\int\braket{f\lvert x}\bra{x}\int\bra{x}\braket{f\lvert x}
\end{align}$$








In product form, we know the following relation generally:
$$\begin{align}
f(x)&=\braket{x\lvert f} &\implies&& \int f(x)\ket{x}&=\int\ket{x}\braket{x\lvert f}
\end{align}$$







Our system has the following representations:
$$\begin{align}
y(x)&=\braket{x\lvert y} & y&=\ket{x}\braket{x\lvert y}\\
x(y)&=\braket{y\lvert x} & x&=\ket{y}\braket{y\lvert x}\\
\end{align}$$
Inverses must satisfy the following property:
$$\begin{align}
f^{-1}(f(x))=f(f^{-1}(x))&=x
\end{align}$$
This relates the following decomposition:
$$\begin{align}
\bra{x}y&=\bra{x}\ket{x}\braket{x\lvert y}\\
\bra{y}x&=\bra{y}\ket{y}\braket{y\lvert x}\\
\end{align}$$





For the function $y(x)$, that means it follows the following relations:
$$\begin{align}
y^\dagger(x)&=\left(\braket{x\lvert y}\right)^\dagger \\
&=\ket{y}^\dagger\bra{x}^\dagger \\
y^\dagger(x)&=\braket{y^*\lvert x^*}
\end{align}$$
This is assuming that the basis orthogonal to allow for the transpose of the vectors.



$$\begin{align}
y(x)&=\braket{x\lvert y} \\
y(x)&=\left(\braket{x\lvert y}\right)^\dagger \\
y&=\ket{x}\braket{x\lvert y}\\

\end{align}$$








We can represent $y$ abstractly, then project onto the $x$ basis to get $y$ as a function of $x$.
$$\begin{align}
\braket{x\lvert y}&=y(x)
\end{align}$$
Based on this structure alone, we can see the inverse is written very similarly:
$$\begin{align}
\braket{y\lvert x}&=x(y)
\end{align}$$
The definition of having an inverse is that both of the following exist for all $x,y$:

We can write this in terms of inner products instead as:








Suppose we have an object $f$. To represent this function in $x$, we do the inner product:

If we want to project this into $y$ instead, where $y=f(x)$, we do the following:
$$\begin{align}
f(x)&=\braket{x\lvert f}=\sum_y\braket{x\lvert y}\braket{y\lvert f}=\sum_y\braket{x\lvert y}f(y)
\end{align}$$


