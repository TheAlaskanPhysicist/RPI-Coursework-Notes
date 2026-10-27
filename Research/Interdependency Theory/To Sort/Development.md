


## Baseline (The 1D TFIM)
The most general form for the study of this system is
$$\begin{align}
\hat{H}&=-\sum_{\left<i,j\right>}J_{ij}\sigma_i^z\sigma_j^z-\sum_i h_i\sigma_i^x
\end{align}$$


### Inhomogeneous $N=2$
For a chain length of 2, the matrix becomes
$$\begin{align}
\hat{H}_{N=2}&=-\left[\begin{array}{cccc}
J_{12}&h_2&h_1&0\\
h_2&-J_{12}&0&h_1\\
h_1&0&-J_{12}&h_2\\
0&h_1&h_2&J_{12}
\end{array}\right]
\end{align}$$
We get the parity basis elements
$$\begin{align}
\ket{\psi_1^+}&=\dfrac{1}{\sqrt{2}}\left(\ket{\uparrow\uparrow}+\ket{\downarrow\downarrow}\right) &
\ket{\psi_2^+}&=\dfrac{1}{\sqrt{2}}\left(\ket{\uparrow\downarrow}+\ket{\downarrow\uparrow}\right) \\
\ket{\psi_1^-}&=\dfrac{1}{\sqrt{2}}\left(\ket{\uparrow\uparrow}-\ket{\downarrow\downarrow}\right) &
\ket{\psi_2^-}&=\dfrac{1}{\sqrt{2}}\left(\ket{\uparrow\downarrow}-\ket{\downarrow\uparrow}\right)
\end{align}$$
With the energies
$$\begin{align}
E_{P=+1}^\pm&=\pm\sqrt{J_{12}^2+(h_1+h_2)^2} &
E_{P=-1}^\pm&=\pm\sqrt{J_{12}^2+(h_1-h_2)^2}
\end{align}$$
The ground state energy is
$$\begin{align}
E_0&=-\sqrt{J_{12}^2+(h_1+h_2)^2}
\end{align}$$
The energy gap between ground and first excited is
$$\begin{align}
\Delta E&=\sqrt{J_{12}^2+(h_1+h_2)^2}-\sqrt{J_{12}^2+(h_1-h_2)^2}
\end{align}$$
The trace and determinant are
$$\begin{align}
\text{Tr}(\hat{H})&=\sum E=0 & \det\hat{H}&=\left(J_{12}^2+(h_1+h_2)^2\right)\left(J_{12}^2+(h_1-h_2)^2\right)
\end{align}$$
Since the determinant is always greater than 0 for real parameters, there are no zero-energy modes for $N=2$. The ground state can be written as
$$\begin{align}
\ket{\psi_0}&=\cos\left(\tfrac{\theta}{2}\right)\ket{\psi_1^+}+\sin\left(\tfrac{\theta}{2}\right)\ket{\psi_2^+} &
\tan\theta&=\dfrac{h_1+h_2}{J_{12}}
\end{align}$$
The spin-spin entanglement by concurrence is
$$\begin{align}
C\left(\ket{\psi_0}\right)&=\dfrac{|J_{12}|}{\sqrt{J_{12}^2+(h_1+h_2)^2}}
\end{align}$$
Suppose we have a ratio between $h_2=h_1r$, now we can look at limit processes.
$$\begin{align}
\lim_{h_1\to0}E_{P=+1}^\pm&=\pm|J_{12}| &
\lim_{h_1\to0}E_{P=-1}^\pm&=\pm|J_{12}| \\
\lim_{h_1\to0}E_0&=-|J_{12}| &
\lim_{h_1\to0}\Delta E&=0\\
\lim_{h_1\to0}\text{Tr}(\hat{H})&=0 & 
\lim_{h_1\to0}\det\hat{H}&=J_{12}^4 \\
\lim_{h_1\to0}\ket{\psi_0}&=\ket{\psi_1^+} &
\lim_{h_1\to0}C\left(\ket{\psi_0}\right)&=1
\end{align}$$



$$\begin{align}
\lim_{h_1\to\infty}E_{P=+1}^\pm&\sim\pm\sqrt{h_1^2(1+r)^2} &
\lim_{h_1\to\infty}E_{P=-1}^\pm&\sim\pm\sqrt{h_1^2(1-r)^2} \\
\lim_{h_1\to\infty}E_0&\sim-\sqrt{J_{12}^2+h_1^2(1+r)^2} &
\lim_{h_1\to\infty}\Delta E&\sim\sqrt{J_{12}^2+h_1^2(1+r)^2}-\sqrt{J_{12}^2+h_1^2(1-r)^2}\\
\lim_{h_1\to\infty}\text{Tr}(\hat{H})&=0 & 
\lim_{h_1\to\infty}\det\hat{H}&\sim\left(J_{12}^2+h_1^2(1+r)^2\right)\left(J_{12}^2+h_1^2(1-r)^2\right) \\
\lim_{h_1\to\infty}\ket{\psi_0}&=\dfrac{1}{\sqrt{2}}\left(\ket{\psi_2^+}+\ket{\psi_2^+}\right) &
\lim_{h_1\to\infty}C\left(\ket{\psi_0}\right)&=\dfrac{|J_{12}|}{\sqrt{J_{12}^2+h_1^2(1+r)^2}}
\end{align}$$






### Homogeneous $N=2$
For a chain length of 2, the matrix becomes
$$\begin{align}
\hat{H}_{N=2}&=-\left[\begin{array}{cccc}
J&h&h&0\\
h&-J&0&h\\
h&0&-J&h\\
0&h&h&J
\end{array}\right]
\end{align}$$
We get the parity basis elements
$$\begin{align}
\ket{\psi_1^+}&=\dfrac{1}{\sqrt{2}}\left(\ket{\uparrow\uparrow}+\ket{\downarrow\downarrow}\right) &
\ket{\psi_2^+}&=\dfrac{1}{\sqrt{2}}\left(\ket{\uparrow\downarrow}+\ket{\downarrow\uparrow}\right) \\
\ket{\psi_1^-}&=\dfrac{1}{\sqrt{2}}\left(\ket{\uparrow\uparrow}-\ket{\downarrow\downarrow}\right) &
\ket{\psi_2^-}&=\dfrac{1}{\sqrt{2}}\left(\ket{\uparrow\downarrow}-\ket{\downarrow\uparrow}\right)
\end{align}$$
With the energies
$$\begin{align}
E_{P=+1}^\pm&=\pm\sqrt{J^2+(2h)^2} &
E_{P=-1}^\pm&=\pm J
\end{align}$$
The ground state energy is
$$\begin{align}
E_0&=-\sqrt{J^2+(2h)^2}
\end{align}$$
The energy gap between ground and first excited is
$$\begin{align}
\Delta E&=\sqrt{J^2+(2h)^2}-|J|
\end{align}$$
The trace and determinant are
$$\begin{align}
\text{Tr}(\hat{H})&=\sum E=0 & \det\hat{H}&=\left(J^2+(2h)^2\right)\left(J^2\right)
\end{align}$$
Since the determinant is always greater than 0 for real parameters, there are no zero-energy modes for $N=2$. The ground state can be written as
$$\begin{align}
\ket{\psi_0}&=\cos\left(\tfrac{\theta}{2}\right)\ket{\psi_1^+}+\sin\left(\tfrac{\theta}{2}\right)\ket{\psi_2^+} &
\tan\theta&=\dfrac{2h}{J}
\end{align}$$
The spin-spin entanglement by concurrence is
$$\begin{align}
C\left(\ket{\psi_0}\right)&=\dfrac{|J|}{\sqrt{J^2+(2h)^2}}
\end{align}$$
In the low field limit $h/J\to0$, we have that
$$\begin{align}
\lim_{h\to0}E_{P=+1}^\pm&=\pm\left[|J|+\frac{2}{|J|}h^2\right] &
\lim_{h\to0}E_{P=-1}^\pm&=\pm|J| \\
\lim_{h\to0}E_0&=-\left[|J|+\frac{2}{|J|}h^2\right] &
\lim_{h\to0}\Delta E&=\frac{2}{|J|}h^2 \\
\lim_{h\to0}\text{Tr}(\hat{H})&=0 & 
\lim_{h\to0}\det\hat{H}&=J^4+4J^2h^2 \\
\lim_{h\to0}\tan\theta&=\dfrac{2}{J}h &
\lim_{h\to0}\ket{\psi_0}&=\ket{\psi_1^+}+\dfrac{h}{J}\ket{\psi_2^+}\\
\lim_{h/J\to0}C\left(\ket{\psi_0}\right)&=1-\frac{2}{J^2}h^2
\end{align}$$
In the high field limit $h/J\to\infty$, we have that
$$\begin{align}
\lim_{h\to\infty}E_{P=+1}^\pm&=\pm2|h| &
\lim_{h\to\infty}E_{P=-1}^\pm&=\pm J \\
\lim_{h\to\infty}E_0&=-2|h| &
\lim_{h\to\infty}\Delta E&=2|h|-|J|\\
\lim_{h\to\infty}\text{Tr}(\hat{H})&=0 & 
\lim_{h\to\infty}\det\hat{H}&=4J^2h^2 \\
\lim_{h\to\infty}\theta&=\dfrac{\pi}{2} &
\lim_{h\to\infty}\ket{\psi_0}&=\dfrac{1}{\sqrt{2}}\left(\ket{\psi_1^+}+\ket{\psi_2^+}\right)\\
\lim_{h/J\to\infty}C\left(\ket{\psi_0}\right)&=\left|\frac{J}{2h}\right|
\end{align}$$
Better writing of this is needed.















$$\begin{align}
\lim_{h/J\to0}E_{P=+1}^\pm&=\pm\sqrt{1+\left(\frac{2h}{J}\right)^2}|J| &
\lim_{h/J\to0}E_{P=-1}^\pm&=\pm J \\
\lim_{h/J\to0}E_0&=-\sqrt{1+\left(\frac{2h}{J}\right)^2}|J| &
\lim_{h/J\to0}\Delta E&=|J|\left(\sqrt{1+\left( \frac{2h}{J} \right)^2}-1\right) \\
\lim_{h/J\to0}\text{Tr}(\hat{H})&=0 & 
\lim_{h/J\to0}\det\hat{H}&=J^4\left(1+\left(\frac{2h}{J}\right)^2\right) \\
\lim_{h/J\to0}\tan\theta&=\dfrac{2h}{J} &
\lim_{h/J\to0}\ket{\psi_0}&=\cos\left(\tfrac{\theta}{2}\right)\ket{\psi_1^+}+\sin\left(\tfrac{\theta}{2}\right)\ket{\psi_2^+}\\
\lim_{h/J\to0}C\left(\ket{\psi_0}\right)&=\dfrac{1}{\sqrt{1+\left(\frac{2h}{J} \right)^2}}
\end{align}$$