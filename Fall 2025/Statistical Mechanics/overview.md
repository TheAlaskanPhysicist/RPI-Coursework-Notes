
$$\begin{align}
T(\dot x_1,\dot x_2)&=\dfrac{1}{2}m\dot{x}_1^2+\dfrac{1}{2}m\dot{x}_2^2\\
V(x_1,x_2)&=\dfrac{1}{2}k(x_1-0)^2+\dfrac{1}{2}k(x_2-x_1)^2+\dfrac{1}{2}k(L-x_2)^2
\end{align}$$
Lagrangian:
$$\begin{align}
\mathcal{L}&=\dfrac{1}{2}m\left(\dot{x}_1^2+\dot{x}_2^2\right)-k(x_1^2+x_2^2-x_1x_2-Lx_2)\\
\dfrac{\partial\mathcal{L}}{\partial x_1}&=-k(2x_1-x_2)\\
\dfrac{d}{dt}\dfrac{\partial\mathcal{L}}{\partial x_1}&=\ddot{x}_1\\
\dfrac{\partial\mathcal{L}}{\partial x_2}&=-k(2x_2-x_1-L)\\
\dfrac{d}{dt}\dfrac{\partial\mathcal{L}}{\partial x_2}&=\ddot{x}_2\\
\end{align}$$
Two equations:
$$\begin{align}
\ddot{x}_1&=-k(2x_1-x_2)\\
\ddot{x}_2&=-k(2x_2-x_1)\\
\end{align}$$
$$\begin{align}
\ddot{\vec{x}}&=\begin{bmatrix}-2&1\\1&-2\end{bmatrix}\vec{x}\\
\vec\lambda_{-3}&=\dfrac{1}{\sqrt2}\begin{bmatrix}-1\\+1\end{bmatrix}\\
\vec\lambda_{-1}&=\dfrac{1}{\sqrt2}\begin{bmatrix}+1\\+1\end{bmatrix}\\
\end{align}$$



$$\begin{align}
L&=\dot{q}_1^2+\dfrac{\dot{q}_2^2}{a+bq_1^2}+k_1q_1^2+k_2\dot{q}_1\dot{q}_2\\
p_1=\dfrac{\partial L}{\partial\dot{q}_1}&=2\dot{q}_1+k_2\dot{q}_2\\
p_2=\dfrac{\partial L}{\partial\dot{q}_2}&=\dfrac{2\dot{q}_2}{a+bq_1^2}+k_2\dot{q}_1
\end{align}$$
$$\begin{align}
\vec{p}&=\begin{bmatrix}2&k_2\\k_2&\dfrac{2}{a+bq_1^2}\end{bmatrix}\dot{\vec{q}}\\
\end{align}$$
$$\begin{align}
\dot{\vec{q}}&=\dfrac{1}{\dfrac{4}{a+bq_1^2}-k_2^2}\begin{bmatrix}\dfrac{2}{a+bq_1^2}&-k_2\\-k_2&2\end{bmatrix}\vec{p}\\
\end{align}$$

$$\begin{align}
\dot{\vec{q}}_1&=\dfrac{1}{\dfrac{4}{a+bq_1^2}-k_2^2}\left(\dfrac{2}{a+bq_1^2}p_1-k_2p_2\right)\\
\dot{\vec{q}}_2&=\dfrac{1}{\dfrac{4}{a+bq_1^2}-k_2^2}\left(-k_2p_1+2p_2\right)\\
\end{align}$$


$$\begin{align}
\mathcal{H}&=p_1\dot{q}_1+p_2\dot{q}_2-L
\end{align}$$






