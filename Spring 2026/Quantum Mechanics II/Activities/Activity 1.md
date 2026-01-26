Stanley Goodwin, 1/16/2026

---
### Question
Using the explicit form of:
$$\begin{align}
Y_l^m&=(-1)^m\sqrt{\dfrac{(2l+1)(l-m)!}{4\pi(l+m)!}}P_l^m(\cos\theta)e^{im\phi}
\end{align}$$
for positive $m$, where:
$$\begin{align}
P_l^{|m|}(\cos\theta)&=\dfrac{(-1)^{l+m}}{2^l l!}\dfrac{(l+|m|)!}{(l-|m|)!}\sin(\theta)^{-|m|}\left(\dfrac{d}{d(\cos\theta)}\right)^{l-|m|}\sin(\theta)^{2l}
\end{align}$$
we can readily show that:
$$\begin{align}
Y_l^m\rightarrow(-1)^{l}Y_l^m
\end{align}$$
Prove it!

---
### Proof
Under the parity transform $\pi$, we know that:
$$\begin{align}
r&\rightarrow r & \theta&\rightarrow\pi-\theta & \phi&\rightarrow\pi+\phi
\end{align}$$
Applying this to $P_l^m$, we see:
$$\begin{align}
\pi P_l^{|m|}(\cos\theta)&=\dfrac{(-1)^{l+m}}{2^l l!}\dfrac{(l+|m|)!}{(l-|m|)!}\sin(\pi-\theta)^{-|m|}\left(\dfrac{d}{d\left(\cos(\pi-\theta)\right)}\right)^{l-|m|}\sin(\pi-\theta)^{2l}\\
&=\dfrac{(-1)^{l+m}}{2^l l!}\dfrac{(l+|m|)!}{(l-|m|)!}\sin(\theta)^{-|m|}\left(\dfrac{d}{d\left(-\cos(\theta)\right)}\right)^{l-|m|}\sin(\theta)^{2l}\\
&=\dfrac{(-1)^{l+m}}{2^l l!}\dfrac{(l+|m|)!}{(l-|m|)!}\sin(\theta)^{-|m|}\left(\dfrac{1}{-1}\dfrac{d}{d\left(\cos(\theta)\right)}\right)^{l-|m|}\sin(\theta)^{2l}\\
&=(-1)^{-(l-|m|)}\cdot\dfrac{(-1)^{l+m}}{2^l l!}\dfrac{(l+|m|)!}{(l-|m|)!}\sin(\theta)^{-|m|}\left(\dfrac{d}{d\left(\cos(\theta)\right)}\right)^{l-|m|}\sin(\theta)^{2l}\\
\Aboxed{\pi P_l^{|m|}(\cos\theta)&=(-1)^{-(l-|m|)}\cdot P_l^{|m|}(\cos\theta)}
\end{align}$$
We can do the same for $Y_l^m$, so that:
$$\begin{align}
\pi Y_l^m&=(-1)^m\sqrt{\dfrac{(2l+1)(l-m)!}{4\pi(l+m)!}}\pi\left( P_l^m(\cos\theta)e^{im\phi}\right)\\
&=(-1)^m\sqrt{\dfrac{(2l+1)(l-m)!}{4\pi(l+m)!}}\pi\left( P_l^m(\cos\theta)\right)\pi\left(e^{im\phi}\right)\\
&=(-1)^m\sqrt{\dfrac{(2l+1)(l-m)!}{4\pi(l+m)!}}\left((-1)^{-(l-|m|)}\cdot P_l^{|m|}(\cos\theta)\right)\left(e^{im(\pi+\phi)}\right)\\
&=(-1)^{-(l-|m|)}e^{im\pi}\cdot(-1)^m\sqrt{\dfrac{(2l+1)(l-m)!}{4\pi(l+m)!}}P_l^{|m|}(\cos\theta)e^{im\phi}\\
&=(-1)^{-(l-|m|)}(-1)^m\cdot Y_l^m\\
&=(-1)^{-l}(-1)^{|m|+m}Y_l^m\\
&=(-1)^{l}\cdot 1\cdot Y_l^m\\
\pi Y_l^m&=(-1)^{l}Y_l^m\\
\Aboxed{Y_l^m&\rightarrow(-1)^{l}Y_l^m}
\end{align}$$
---