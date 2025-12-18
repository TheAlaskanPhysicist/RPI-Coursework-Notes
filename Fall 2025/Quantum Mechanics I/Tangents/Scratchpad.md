




$$\begin{align}
\mathcal{L}'&=\bar\psi'\left(i\gamma^\mu\partial_\mu-m\right)\psi'\\
&=\bar\psi U^\dagger\left(i\gamma^\mu\partial_\mu-m\right)U\psi\\
&=\bar\psi\left(i\gamma^\mu\partial_\mu-m\right)\psi+\bar\psi U^\dagger\left(i\gamma^\mu\partial_\mu U\right)\psi\\
&=\mathcal{L}+\bar\psi\left(i\gamma^\mu U^\dagger\partial_\mu U\right)\psi\\
0&=\bar\psi\left(i\gamma^\mu U^\dagger\partial_\mu U\right)\psi\\
\end{align}$$
Let $U=e^{i\phi}$, then:
$$\begin{align}
0&=\bar\psi\left(i\gamma^\mu U^\dagger\partial_\mu U\right)\psi\\
0&=\bar\psi\left(i\gamma^\mu e^{-i\phi}\partial_\mu e^{i\phi}\right)\psi\\
0&=\bar\psi\left(i^2\gamma^\mu e^{-i\phi} e^{i\phi}\partial_\mu\phi\right)\psi\\
0&=\bar\psi\left(\gamma^\mu\partial_\mu\phi\right)\psi\\
0&=\gamma^\mu\partial_\mu\phi\\
\end{align}$$









Suppose the following:
$$\begin{align}
\mathcal{L}&=\bar\psi\left(i\gamma^\mu\partial_\mu-m\right)\psi
\end{align}$$
We want to impose that $\mathcal{L}$ is invariant under $U(1)$ symmetries.
$$\begin{align}
\psi&\mapsto e^{iq\alpha(x)}\psi & \bar\psi&\mapsto\bar\psi e^{-iq\alpha(x)}
\end{align}$$
Then we can see:
$$\begin{align}
\mathcal{L}'&=\bar\psi'\left(i\gamma^\mu\partial_\mu-m\right)\psi'\\
&=\bar\psi e^{-iq\alpha(x)}\left(i\gamma^\mu\partial_\mu-m\right)e^{iq\alpha(x)}\psi\\
&=\bar\psi e^{-iq\alpha(x)}i\gamma^\mu\partial_\mu\left(e^{iq\alpha(x)}\psi\right)-m\bar\psi\psi\\
&=\bar\psi e^{-iq\alpha(x)}i\gamma^\mu\partial_\mu\left(e^{iq\alpha(x)}\right)\psi+\bar\psi e^{-iq\alpha(x)}e^{iq\alpha(x)}i\gamma^\mu\partial_\mu\psi-m\bar\psi\psi\\
\mathcal{L}'&=\bar\psi e^{-iq\alpha(x)}i\gamma^\mu\partial_\mu\left(e^{iq\alpha(x)}\right)\psi+\mathcal{L}\\
\mathcal{L}'-\mathcal{L}&=\bar\psi e^{-iq\alpha(x)}i^2q\gamma^\mu\partial_\mu\left(\alpha(x)\right)e^{iq\alpha(x)}\psi\\
0&=\bar\psi\left(\gamma^\mu\partial_\mu\alpha(x)\right)\psi\\
\Aboxed{0&=\gamma^\mu\partial_\mu\alpha(x)}
\end{align}$$



Suppose we have the following gauge field:
$$\begin{align}
A_\mu'&=U(A_\mu+i\partial_\mu)U^\dagger\\
\psi'&=U\psi
\end{align}$$
Then we have:
$$\begin{align}
\partial_\mu\psi'&=(\partial_\mu U)\psi+U(\partial_\mu\psi)\\
A_\mu'\psi'&=U(A_\mu+i\partial_\mu)\psi
\end{align}$$
