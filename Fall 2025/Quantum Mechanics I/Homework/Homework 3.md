Author: Stanley Goodwin
Date: September 29th, 2025

---
## Question 2.3
An electron is subject to a uniform, time-independent magnetic field of strength $B$ in the positive z-direction. At $t = 0$ the electron is known to be in an eigenstate of $\vec{S}\cdot\vec{n}$ with eigenvalue $\hbar/2$, where $\hat{n}$ is a unit vector, lying in the $xz$-plane, that makes an angle $\beta$ with the $z$-axis.

We can find the Hamiltonian as:
$$\begin{align}
\hat{H}&=-\left(\dfrac{e}{m_ec}\right)\vec{S}\cdot\vec{B} &\implies&& \Aboxed{\hat{H}&=-\left(\dfrac{eB}{m_ec}\right)S_z}
\end{align}$$
Since we're writing everything in terms of the $z$-basis, we know the energies are:
$$\begin{align}
E_\pm&=\mp\dfrac{e\hbar B}{2m_ec}
\end{align}$$
The initial state is a little more difficult, but the general form is:
$$\begin{align}
\ket{\chi^n_+}&=\cos\left(\frac{\beta}{2}\right)\ket{\chi^z_+}+\sin\left(\frac{\beta}{2}\right)\ket{\chi^z_-}
\end{align}$$
The "$xz$-plane" technically has 2 solutions ($\pm$), but I chose the $\phi=0$ for simplicity.

---
### Question 2.3.A
Obtain the probability for finding the electron in the $S_x=\hbar/2$ state as a function of time.

We can find the time-evolution operator $U(t;0)$ for this system as being:
$$\begin{align}
U(t;0)&=e^{-\tfrac{i}{\hbar}\hat{H}t}
\end{align}$$
When we apply this operator on our initial state, we can see that:
$$\begin{align}
U(t;0)\ket{\chi^n_+}&=e^{-\tfrac{i}{\hbar}\hat{H}t}\cos\left(\frac{\beta}{2}\right)\ket{\chi^z_+}+e^{-\tfrac{i}{\hbar}\hat{H}t}\sin\left(\frac{\beta}{2}\right)\ket{\chi^z_-}\\
&=\cos\left(\frac{\beta}{2}\right)e^{-\tfrac{i}{\hbar}\hat{H}t}\ket{\chi^z_+}+\sin\left(\frac{\beta}{2}\right)e^{-\tfrac{i}{\hbar}\hat{H}t}\ket{\chi^z_-}\\
\end{align}$$
The Hamiltonian applied to eigenstates of the $z$-basis allows us to reduce it to:
$$\begin{align}
U(t;0)\ket{\chi^n_+}&=e^{-\tfrac{i}{\hbar}\left(+\tfrac{e\hbar B}{2m_ec}\right)t}\cos\left(\frac{\beta}{2}\right)\ket{\chi^z_+}+e^{-\tfrac{i}{\hbar}\left(-\tfrac{e\hbar B}{2m_ec}\right)t}\sin\left(\frac{\beta}{2}\right)\ket{\chi^z_-}\\
&=e^{-i\left(\tfrac{eB}{2m_ec}\right)t}\cos\left(\frac{\beta}{2}\right)\ket{\chi^z_+}+e^{+i\left(\tfrac{eB}{2m_ec}\right)t}\sin\left(\frac{\beta}{2}\right)\ket{\chi^z_-}\\
\end{align}$$
To find the inner product with the $\ket{+x}$ state, we can write this as:
$$\begin{align}
\bra{\chi^x_+}U(t;0)\ket{\chi^n_+}
&=e^{-i\left(\tfrac{eB}{2m_ec}\right)t}\cos\left(\frac{\beta}{2}\right)\braket{\chi^x_+|\chi^z_+}+e^{+i\left(\tfrac{eB}{2m_ec}\right)t}\sin\left(\frac{\beta}{2}\right)\braket{\chi^x_+|\chi^z_-}\\
&=\dfrac{1}{\sqrt{2}}e^{-i\left(\tfrac{eB}{2m_ec}\right)t}\cos\left(\frac{\beta}{2}\right)+\dfrac{1}{\sqrt{2}}e^{+i\left(\tfrac{eB}{2m_ec}\right)t}\sin\left(\frac{\beta}{2}\right)\\
\bra{\chi^x_+}U(t;0)\ket{\chi^n_+}&=\dfrac{1}{\sqrt{2}}e^{-i\left(\tfrac{eB}{2m_ec}\right)t}\left[\cos\left(\frac{\beta}{2}\right)+e^{i\left(\tfrac{eB}{m_ec}\right)t}\sin\left(\frac{\beta}{2}\right)\right]\\
\end{align}$$
Now we just find the square modulus:
$$\begin{align}
\left|\bra{\chi^x_+}U(t;0)\ket{\chi^n_+}\right|^2
&=\left(\dfrac{1}{\sqrt{2}}\right)^2\left|e^{-i\left(\tfrac{eB}{2m_ec}\right)t}\right|^2\left|\cos\left(\frac{\beta}{2}\right)+e^{i\left(\tfrac{eB}{m_ec}\right)t}\sin\left(\frac{\beta}{2}\right)\right|^2\\
&=\dfrac{1}{2}\cdot1\cdot\left[\cos\left(\frac{\beta}{2}\right)+e^{-i\left(\tfrac{eB}{m_ec}\right)t}\sin\left(\frac{\beta}{2}\right)\right]\left[\cos\left(\frac{\beta}{2}\right)+e^{i\left(\tfrac{eB}{m_ec}\right)t}\sin\left(\frac{\beta}{2}\right)\right]\\
&=\dfrac{1}{2}\cdot1\cdot\left[\cos^2\left(\frac{\beta}{2}\right)+2\dfrac{e^{+i\left(\tfrac{eB}{m_ec}\right)t}+e^{-i\left(\tfrac{eB}{m_ec}\right)t}}{2}\sin\left(\frac{\beta}{2}\right)\cos\left(\frac{\beta}{2}\right)+\sin^2\left(\frac{\beta}{2}\right)\right]\\
\Aboxed{p(\psi=\ket{\chi^x_+})&=\dfrac{1}{2}\cdot\left[1+\cos\left(\dfrac{eB}{m_ec}t\right)\sin\left(\beta\right)\right]}
\end{align}$$
---
### Question 2.3.B
Find the expectation value of $S_x$ as a function of time.
$$\begin{align}
\braket{S_x}&=\dfrac{\hbar}{2}p(\psi=\ket{\chi^x_+})-\dfrac{\hbar}{2}p(\psi=\ket{\chi^x_-})\\
&=\dfrac{\hbar}{2}p(\psi=\ket{\chi^x_+})-\dfrac{\hbar}{2}\left[1-p(\psi=\ket{\chi^x_+})\right]\\
&=\dfrac{\hbar}{2}\left[2p(\psi=\ket{\chi^x_+})-1\right]\\
&=\dfrac{\hbar}{2}\left[1+\cos\left(\dfrac{eB}{m_ec}t\right)\sin\left(\beta\right)-1\right]\\
\Aboxed{\braket{S_x}&=\dfrac{\hbar}{2}\cos\left(\dfrac{eB}{m_ec}t\right)\sin\left(\beta\right)}
\end{align}$$
---
### Question 2.3.C
For your own peace of mind show that your answers make good sense in the extreme cases:
1. $\beta\rightarrow0$
2. $\beta\rightarrow\pi/2$
**Part 1**
$$\begin{align}
\ket{\chi^n_+}&=\ket{\chi^z_+}\\
U(t;0)\ket{\chi^n_+}&=e^{-i\left(\tfrac{eB}{2m_ec}\right)t}\ket{\chi^z_+}\\
\end{align}$$
$$\begin{align}
p(\psi=\ket{\chi^x_+})&=\dfrac{1}{2}\cdot\left[1+\cos\left(\dfrac{eB}{m_ec}t\right)\sin\left(0\right)\right]=\dfrac{1}{2}
\end{align}$$
$$\begin{align}
\braket{S_x}&=\dfrac{\hbar}{2}\cos\left(\dfrac{eB}{m_ec}t\right)\sin\left(0\right)=0
\end{align}$$
These are all consistent with an initial state in the positive $z$ direction.

**Part 2**
$$\begin{align}
\ket{\chi^n_+}&=\dfrac{1}{\sqrt{2}}\ket{\chi^z_+}+\dfrac{1}{\sqrt{2}}\ket{\chi^z_-}=\ket{\chi^x_+}\\
U(t;0)\ket{\chi^n_+}&=\dfrac{1}{\sqrt{2}}e^{-i\left(\tfrac{eB}{2m_ec}\right)t}\left[\ket{\chi^z_+}+e^{i\left(\tfrac{eB}{m_ec}\right)t}\ket{\chi^z_-}\right]\\
\end{align}$$
$$\begin{align}
p(\psi=\ket{\chi^x_+})&=\dfrac{1}{2}\cdot\left[1+\cos\left(\dfrac{eB}{m_ec}t\right)\sin\left(\dfrac{\pi}{2}\right)\right]\\
&=\dfrac{1}{2}\cdot\left[1+\cos\left(\dfrac{eB}{m_ec}t\right)\right]\\
p(\psi=\ket{\chi^x_+})&=\cos^2\left(\dfrac{eB}{2m_ec}t\right)
\end{align}$$
$$\begin{align}
\braket{S_x}&=\dfrac{\hbar}{2}\cos\left(\dfrac{eB}{m_ec}t\right)\sin\left(\dfrac{\pi}{2}\right)=\dfrac{\hbar}{2}\cos\left(\dfrac{eB}{m_ec}t\right)\\
\end{align}$$
All seems consistent!

---
## Question 2.4
### Question 2.4.A
Derive the neutrino oscillation probability (2.65).

Lets represent the real neutrinos as a linear combination of some eigenstate neutrino.
$$\begin{align}
\ket{\nu_e}&=\cos\theta\ \ket{\nu_1}-\sin\theta\ \ket{\nu_2}\\
\ket{\nu_\mu}&=\sin\theta\ \ket{\nu_1}+\cos\theta\ \ket{\nu_2}\\
\end{align}$$
Starting with an electron neutrino, we can time evolve it so that:
$$\begin{align}
U(t;0)\ket{\nu_e}&=e^{-\tfrac{i}{\hbar}\hat{H}t}\cos\theta\ \ket{\nu_1}-e^{-\tfrac{i}{\hbar}\hat{H}t}\sin\theta\ \ket{\nu_2}\\
\end{align}$$
For these neutrino states, they have associated Hamiltonian energies equal to that of the relativistic energy equation from above, and so:
$$\begin{align}
U(t;0)\ket{\nu_e}&=e^{-\tfrac{i}{\hbar}E_1t}\cos\theta\ \ket{\nu_1}-e^{-\tfrac{i}{\hbar}E_2t}\sin\theta\ \ket{\nu_2}\\
\end{align}$$
To find the probability of $\ket{\nu_e}$ later, we multiply both sides by $\bra{\nu_e}$:
$$\begin{align}
\bra{\nu_e}U(t;0)\ket{\nu_e}
&=\left(\cos\theta\ \bra{\nu_1}-\sin\theta\ \bra{\nu_2}\right)U(t;0)\ket{\nu_e}\\
&=e^{-\tfrac{i}{\hbar}E_1t}\cos^2\theta+e^{-\tfrac{i}{\hbar}E_2t}\sin^2\theta
\end{align}$$
To find probability, we just find the square modulus, and so:
$$\begin{align}
\left|\bra{\nu_e}U(t;0)\ket{\nu_e}\right|^2
&=\left(e^{\tfrac{i}{\hbar}E_1t}\cos^2\theta+e^{\tfrac{i}{\hbar}E_2t}\sin^2\theta\right)\left(e^{-\tfrac{i}{\hbar}E_1t}\cos^2\theta+e^{-\tfrac{i}{\hbar}E_2t}\sin^2\theta\right)\\
&=\left(\cos^4\theta+\sin^4\theta+2\dfrac{e^{\tfrac{i}{\hbar}(E_1-E_2)t}+e^{-\tfrac{i}{\hbar}(E_1-E_2)t}}{2}\cos^2\theta \sin^2\theta\right)\\
&=1-4\left(\dfrac{1-\cos\left(\tfrac{E_1-E_2}{\hbar}t\right)}{2}\right)\sin^2\theta\cos^2\theta\\
&=1-\sin^2(2\theta)\sin^2\left(\tfrac{E_1-E_2}{2\hbar}t\right)\\
\end{align}$$
We can approximate the energy of each neutrino as:
$$\begin{align}
E^2-(\vec{p}c)^2&=(mc^2)^2\implies E\approx pc\left(1+\dfrac{(mc)^2}{2p^2}\right)\\
E_1-E_2&=\dfrac{c^4}{2pc}\left(m_1^2-m_2^2\right)\\
&=\Delta m^2c^4\dfrac{1}{2pc}
\end{align}$$
Substituting, we see:
$$\begin{align}
\left|\bra{\nu_e}U(t;0)\ket{\nu_e}\right|^2
&=1-\sin^2(2\theta)\sin^2\left(\tfrac{E_1-E_2}{2\hbar}t\right)\\
&=1-\sin^2(2\theta)\sin^2\left(\tfrac{\Delta m^2c^4\tfrac{1}{2pc}}{2\hbar}t\right)\\
&=1-\sin^2(2\theta)\sin^2\left(\Delta m^2c^4\dfrac{t}{4\hbar pc}\right)\\
\end{align}$$
The last bit of the proof is that we let $L=ct$ be the flight distance of the neutrino (conversion between time and distance traveled), and that for small-mass neutrinos, $E\approx pc$. And so:
$$\begin{align}
\left|\bra{\nu_e}U(t;0)\ket{\nu_e}\right|^2
&=1-\sin^2(2\theta)\sin^2\left(\Delta m^2c^4\dfrac{t}{4\hbar p c}\right)\\
&=1-\sin^2(2\theta)\sin^2\left(\Delta m^2c^4\dfrac{ct}{4\hbar p c\cdot c}\right)\\
\Aboxed{p(\nu_e\rightarrow \nu_e)&=1-\sin^2(2\theta)\sin^2\left(\Delta m^2c^4\dfrac{L}{4E\hbar c}\right)}
\end{align}$$
---
### Question 2.4.B
Use part A it, along with Figure 2.2, to estimate the values of $\Delta m^2c^4$ (in units of $\text{eV}^2$) and $\theta$.

Approximately peak-to-peak of the sine wave has the following characteristics:
$$\begin{align}
\Delta\left(\dfrac{L_0}{E_{\nu_e}}\right)&\approx70\dfrac{\text{km}}{\text{MeV}}-35\dfrac{\text{km}}{\text{MeV}}=35\dfrac{\text{km}}{\text{MeV}}
\end{align}$$
We expect that the sine wave goes through a full cycle during this, and so:
$$\begin{align}
\Delta m^2c^4\dfrac{1}{4\hbar c}\dfrac{L}{E}&=2\pi &\implies&& \Delta m^2c^4&=8\pi\hbar c\left(\dfrac{L}{E}\right)^{-1}
\end{align}$$
For our system, we want this in different units, so I'm going to convert as needed:
$$\begin{align}
35\dfrac{\text{km}}{\text{MeV}}&=35\cdot10^{-3}\dfrac{\text{m}}{\text{eV}}\\
\hbar c&=\dfrac{1240}{2\pi}\cdot10^{-9}\ \text{eV}\ \text{m}
\end{align}$$
Substituting, we see that:
$$\begin{align}
\Delta m^2c^4&=8\pi\hbar c\left(\dfrac{L}{E}\right)^{-1}\\
&=8\pi\cdot\dfrac{1240}{2\pi}\cdot10^{-9}\ \text{eV}\ \text{m}\cdot\left(35\cdot10^{-3}\dfrac{\text{m}}{\text{eV}}\right)^{-1}\\
&=4\cdot1240\cdot10^{-9}\ \text{eV}\ \text{m}\cdot\dfrac{10^3}{35}\dfrac{\text{eV}}{\text{m}}\\
&=\dfrac{4\cdot1240}{35}10^{-6}\text{eV}^2\\
&=\dfrac{4\cdot1240}{35}10^{-6}\text{eV}^2\\
\Aboxed{\Delta m^2c^4&\approx1.4171\cdot10^{-4}\text{eV}^2}
\end{align}$$
You can do something similar for the half-period for the 2 differences:
$$\begin{align}
\Delta\left(\dfrac{L_0}{E_{\nu_e}}\right)_1&\approx50\dfrac{\text{km}}{\text{MeV}}-35\dfrac{\text{km}}{\text{MeV}}=15\dfrac{\text{km}}{\text{MeV}}\\
\Delta\left(\dfrac{L_0}{E_{\nu_e}}\right)_2&\approx70\dfrac{\text{km}}{\text{MeV}}-50\dfrac{\text{km}}{\text{MeV}}=20\dfrac{\text{km}}{\text{MeV}}
\end{align}$$
With the half-period being $\pi$, and so:
$$\begin{align}
\Delta m^2c^4\dfrac{1}{4\hbar c}\dfrac{L}{E}&=\pi &\implies&& \Delta m^2c^4&=4\pi\hbar c\left(\dfrac{L}{E}\right)^{-1}
\end{align}$$
For the two values, we get the following:
$$\begin{align}
\Delta m^2c^4&\approx1.6533\cdot10^{-4}\text{eV}^2\\
\Delta m^2c^4&\approx1.2400\cdot10^{-4}\text{eV}^2
\end{align}$$
Doing the statistics on these 3 (I know it's a small number), I get:
$$\begin{align}
\Aboxed{\mu_{\Delta m^2c^4}&=1.4368\cdot10^{-4}\text{eV}^2}\\
\sigma_{\Delta m^2c^4}&=0.2074\cdot10^{-4}\text{eV}^2
\end{align}$$
---
## Question 2.6
Consider a particle in one dimension whose Hamiltonian is given by:
$$\begin{align}
\hat{H}&=\dfrac{p^2}{2m}+V(x)
\end{align}$$
By calculating $[[\hat{H},x], x]$, prove:
$$\begin{align}
\sum_{a'}\left|\bra{a''}x\ket{a'}\right|^2\left(E_{a'}-E_{a''}\right)&=\dfrac{\hbar^2}{2m}
\end{align}$$
where $\ket{a'}$ is an energy eigenket with eigenvalue $E_a'$.
$$\begin{align}
[\hat{H},x]\ket{a'}&=\left(\dfrac{p^2}{2m}+V(x)\right)x\ket{a'}-x\left(\dfrac{p^2}{2m}+V(x)\right)\ket{a'}\\
&=\dfrac{1}{2m}\left[p^2,x\right]\ket{a'}+\left[V(x),x\right]\ket{a'}\\
&=-\dfrac{1}{2m}\left(\left[x,p\right]p+p\left[x,p\right]\right)\ket{a'}+0\ket{a'}\\
[\hat{H},x]\ket{a'}&=\left(-\dfrac{i\hbar}{m}p\right)\ket{a'}\\
\end{align}$$
Then:
$$\begin{align}
[[\hat{H},x], x]\ket{a'}&=\left[\left(-\dfrac{i\hbar}{m}p\right), x\right]\ket{a'}\\
&=-\dfrac{i\hbar}{m}\left[p,x\right]\ket{a'}\\
&=\dfrac{i\hbar}{m}\cdot i\hbar\ket{a'}\\
\Aboxed{[[\hat{H},x], x]\ket{a'}&=-\dfrac{\hbar^2}{m}\ket{a'}}
\end{align}$$
To calculate the expected value, we can do the following:
$$\begin{align}
[[\hat{H},x], x]&=[\hat{H},x]x-x[\hat{H},x]\\
&=\hat{H}x^2-2x\hat{H}x+x^2\hat{H}\\
\Aboxed{\bra{a''}[[\hat{H},x], x]\ket{a''}&=\bra{a''}\hat{H}x^2\ket{a''}-2\bra{a''}x\hat{H}x\ket{a''}+\bra{a''}x^2\hat{H}\ket{a''}}
\end{align}$$
Lets do these one at a time:
$$\begin{align}
\bra{a''}\hat{H}x^2\ket{a''}
&=\sum_{a'''}\sum_{a'}\bra{a''}\hat{H}\ket{a'''}\bra{a'''}x\ket{a'}\bra{a'}x\ket{a''}\\
&=\sum_{a'''}\sum_{a'}E_{a'''}\braket{a''|a'''}\bra{a'''}x\ket{a'}\bra{a'}x\ket{a''}\\
&=\sum_{a'''}\sum_{a'}E_{a'''}\delta_{a''a'''}\bra{a'''}x\ket{a'}\bra{a'}x\ket{a''}\\
&=E_{a''}\sum_{a'}\bra{a''}x\ket{a'}\bra{a'}x\ket{a''}\\
&=E_{a''}\sum_{a'}\bra{a''}x\ket{a'}\left(\bra{a''}x\ket{a'}\right)^\dagger\\
\Aboxed{\bra{a''}\hat{H}x^2\ket{a''}&=E_{a''}\sum_{a'}\left|\bra{a''}x\ket{a'}\right|^2}
\end{align}$$
$$\begin{align}
\bra{a''}x^2\hat{H}\ket{a''}
&=\sum_{a'''}\sum_{a'}\bra{a''}x\ket{a'''}\bra{a'''}x\ket{a'}\bra{a'}\hat{H}\ket{a''}\\
&=\sum_{a'''}\sum_{a'}E_{a''}\bra{a''}x\ket{a'''}\bra{a'''}x\ket{a'}\braket{a'|a''}\\
&=\sum_{a'''}\sum_{a'}E_{a''}\bra{a''}x\ket{a'''}\bra{a'''}x\ket{a'}\delta_{a'a''}\\
&=\sum_{a'''}E_{a''}\bra{a''}x\ket{a'''}\bra{a'''}x\ket{a''}\\
\Aboxed{\bra{a''}x^2\hat{H}\ket{a''}&=\sum_{a'}E_{a''}\left|\bra{a'}x\ket{a''}\right|^2} \text{ after reindexing}
\end{align}$$
$$\begin{align}
\bra{a''}x\hat{H}x\ket{a''}
&=\sum_{a'''}\sum_{a'}\bra{a''}x\ket{a'''}\bra{a'''}\hat{H}\ket{a'}\bra{a'}x\ket{a''}\\
&=\sum_{a'''}\sum_{a'}E_{a'}\bra{a''}x\ket{a'''}\braket{a'''|a'}\bra{a'}x\ket{a''}\\
&=\sum_{a'''}\sum_{a'}E_{a'}\bra{a''}x\ket{a'''}\delta_{a'a'''}\bra{a'}x\ket{a''}\\
\bra{a''}x\hat{H}x\ket{a''}&=\sum_{a'}E_{a'}\bra{a''}x\ket{a'}\bra{a'}x\ket{a''}\\
\Aboxed{\bra{a''}x\hat{H}x\ket{a''}&=\sum_{a'}E_{a'}\left|\bra{a''}x\ket{a'}\right|^2}
\end{align}$$
Combined, we see:
$$\begin{align}
\bra{a''}[[\hat{H},x], x]\ket{a''}&=\bra{a''}\hat{H}x^2\ket{a''}-2\bra{a''}x\hat{H}x\ket{a''}+\bra{a''}x^2\hat{H}\ket{a''}\\
&=E_{a''}\sum_{a'}\left|\bra{a''}x\ket{a'}\right|^2+\sum_{a'}E_{a''}\left|\bra{a'}x\ket{a''}\right|^2-2\sum_{a'}E_{a'}\left|\bra{a''}x\ket{a'}\right|^2\\
&=\sum_{a'}\left(E_{a''}+E_{a''}-2E_{a'}\right)\left|\bra{a''}x\ket{a'}\right|^2\\
\Aboxed{\bra{a''}[[\hat{H},x], x]\ket{a''}&=2\sum_{a'}\left(E_{a''}-E_{a'}\right)\left|\bra{a''}x\ket{a'}\right|^2}
\end{align}$$
From our original calculation of $[[\hat{H},x], x]$, we know that:
$$\begin{align}
\Aboxed{\bra{a''}[[\hat{H},x], x]\ket{a''}&=-\dfrac{\hbar^2}{m}}
\end{align}$$
Seeing these equal, we see:
$$\begin{align}
2\sum_{a'}\left(E_{a''}-E_{a'}\right)\left|\bra{a''}x\ket{a'}\right|^2&=-\dfrac{\hbar^2}{m}\\
\Aboxed{\sum_{a'}\left(E_{a'}-E_{a''}\right)\left|\bra{a''}x\ket{a'}\right|^2&=\dfrac{\hbar^2}{2m}}
\end{align}$$
Thus concludes the proof.

---
## Question 2.7
Consider a particle in three dimensions whose Hamiltonian is given by:
$$\begin{align}
\hat{H}&=\dfrac{\vec{p}^2}{2m}+V(\vec{x})
\end{align}$$
By calculating $[\vec{x}\cdot\vec{p},\hat{H}]$, obtain:
$$\begin{align}
\dfrac{d}{dt}\left\langle\vec{x}\cdot\vec{p}\right\rangle&=\left\langle\dfrac{\vec{p}^2}{m}\right\rangle-\left\langle\vec{x}\cdot\vec\nabla V\right\rangle
\end{align}$$
To identify the preceding relation with the quantum-mechanical analogue of the virial theorem it is essential that the left-hand side vanish. Under what condition would this happen?
### Question 2.7.A
$$\begin{align}
[\vec{x}\cdot\vec{p},\hat{H}]&=-[\hat{H},\vec{x}]\cdot\vec{p}-\vec{x}\cdot[\hat{H},\vec{p}]\\
&=[\vec{x},\hat{H}]\cdot\vec{p}+\vec{x}\cdot[\vec{p},\hat{H}]\\
&=\left[\vec{x},\dfrac{\vec{p}^2}{2m}+V(\vec{x})\right]\cdot\vec{p}+\vec{x}\cdot\left[\vec{p},\dfrac{\vec{p}^2}{2m}+V(\vec{x})\right]\\
&=\dfrac{1}{2m}\left[\vec{x},\vec{p}^2\right]\cdot\vec{p}+\vec{x}\cdot\left[\vec{p},V(\vec{x})\right]\\
&=\dfrac{2i\hbar}{2m}\vec{p}\cdot\vec{p}+\vec{x}\cdot\left[\vec{p},V(\vec{x})\right]\\
\Aboxed{[\vec{x}\cdot\vec{p},\hat{H}]&=\dfrac{i\hbar}{m}\vec{p}^2-i\hbar\vec{x}\cdot\vec\nabla V(\vec{x})}
\end{align}$$
From class, we've usually seen the commutator divided by $i\hbar$, and so:
$$\begin{align}
\Aboxed{\dfrac{[\vec{x}\cdot\vec{p},\hat{H}]}{i\hbar}&=\dfrac{\vec{p}^2}{m}-\vec{x}\cdot\vec\nabla V(\vec{x})}
\end{align}$$
If we take the expected values of both sides, then:
$$\begin{align}
\Aboxed{\dfrac{\langle[\vec{x}\cdot\vec{p},\hat{H}]\rangle}{i\hbar}&=\left\langle\dfrac{\vec{p}^2}{m}\right\rangle-\left\langle\vec{x}\cdot\vec\nabla V\right\rangle}
\end{align}$$
This is exactly equal to the rate change of the first operator, and so:
$$\begin{align}
\dfrac{d}{dt}\langle\vec{x}\cdot\vec{p}\rangle&=\dfrac{\langle[\vec{x}\cdot\vec{p},\hat{H}]\rangle}{i\hbar} &\implies&& \Aboxed{\dfrac{d}{dt}\langle\vec{x}\cdot\vec{p}\rangle&=\left\langle\dfrac{\vec{p}^2}{m}\right\rangle-\left\langle\vec{x}\cdot\vec\nabla V\right\rangle}
\end{align}$$
### Question 2.7.B
When the left-hand side is 0, we see the following relationship:
$$\begin{align}
\left\langle\dfrac{\vec{p}^2}{m}\right\rangle&=-\left\langle\vec{x}\cdot-\vec\nabla V\right\rangle
\end{align}$$
It looks almost like the work kinetic-energy theorem, where:
$$\begin{align}
\Delta W+\Delta\text{KE}&=0
\end{align}$$
For classical systems, this would akin to:
$$\begin{align}
\dfrac{\vec{p}^2}{2m}+\vec{F}\cdot\vec{x}&=0
\end{align}$$
If I were to conjecture, the required condition is that the system is in an *energy eigenstate*.
 - I.e. conserved energy systems. Bound systems of discrete, unchanging, energy.
 - This feels like it should also relate to an action minimum, since it doesn't change with respect to time when it reaches this equilibrium.

---
## Question 2.10
Let $\ket{a'}$ and $\ket{a''}$ be eigenstates of a Hermitian operator $A$ with eigenvalues $a'$ and $a''$, respectively $(a'=a'')$. The Hamiltonian operator is given by:
$$\begin{align}
\hat{H}&=\ket{a'}\delta\bra{a''}+\ket{a''}\delta\bra{a'}
\end{align}$$
where $\delta$ is just a real number.

---
### Question 2.10.A
Clearly, $\ket{a'}$ and $\ket{a''}$ are not eigenstates of the Hamiltonian. Write down the eigenstates of the Hamiltonian. What are their energy eigenvalues?
$$\begin{align}
\hat{H}&=\begin{bmatrix}0&\delta\\\delta&0\end{bmatrix}
\end{align}$$
I've done this one 100 times because it's the same decomposition as the $S_x$ matrix:
$$\begin{align}
\lambda_1&=-\delta & \vec{\lambda_1}&=\dfrac{1}{\sqrt2}\ket{a'}-\dfrac{1}{\sqrt2}\ket{a''}\\
\lambda_2&=+\delta & \vec{\lambda_2}&=\dfrac{1}{\sqrt2}\ket{a'}+\dfrac{1}{\sqrt2}\ket{a''}
\end{align}$$
Therefore, the energy eigenvalues are:
$$\begin{align}
\Aboxed{E\in\{-\delta,+\delta\}}
\end{align}$$
---
### Question 2.10B
Suppose the system is known to be in state $\ket{a'}$ at $t = 0$. Write down the state vector in the Schrödinger picture for $t < 0$.
$$\begin{align}
U(t;0)\ket{a'}&=e^{-\tfrac{i}{\hbar}\hat{H}t}\dfrac{\ket{\lambda_1}+\ket{\lambda_2}}{\sqrt{2}}\\
\Aboxed{\ket{a'; t}&=\dfrac{1}{\sqrt2}e^{+\tfrac{i}{\hbar}\delta t}\ket{\lambda_1}+\dfrac{1}{\sqrt2}e^{-\tfrac{i}{\hbar}\delta t}\ket{\lambda_2}}
\end{align}$$
---
### Question 2.10.C
What is the probability for finding the system in $\ket{a''}$ for $t < 0$ if the system is known to be in state $\ket{a'}$ at $t = 0$?
$$\begin{align}
\left|\braket{a''|a'; t}\right|^2&=\left|\left(\dfrac{1}{\sqrt2}\bra{\lambda_1}-\dfrac{1}{\sqrt2}\bra{\lambda_2}\right)\left(\dfrac{1}{\sqrt2}e^{+\tfrac{i}{\hbar}\delta t}\ket{\lambda_1}+\dfrac{1}{\sqrt2}e^{-\tfrac{i}{\hbar}\delta t}\ket{\lambda_2}\right)\right|^2\\
&=\left|\left(\dfrac{1}{2}e^{+\tfrac{i}{\hbar}\delta t}-\dfrac{1}{2}e^{-\tfrac{i}{\hbar}\delta t}\right)\right|^2\\
&=\dfrac{1}{4}\left(e^{-\tfrac{i}{\hbar}\delta t}-e^{+\tfrac{i}{\hbar}\delta t}\right)\left(e^{+\tfrac{i}{\hbar}\delta t}-e^{-\tfrac{i}{\hbar}\delta t}\right)\\
&=\dfrac{1}{4}\left(2-2\dfrac{e^{+2\tfrac{i}{\hbar}\delta t}+e^{-2\tfrac{i}{\hbar}\delta t}}{2}\right)\\
&=\dfrac{1}{2}\left(1-\cos\left(\tfrac{2\delta t}{\hbar}\right)\right)\\
\Aboxed{P(\ket{a'; t}&=\sin^2\left(\tfrac{\delta}{\hbar}t\right)}
\end{align}$$
---
### Question 2.10.D
Can you think of a physical situation corresponding to this problem?

The only thing I can think of (since I noted earlier that the eigenstates look like $S_x$) is if we have a spin-$1/2$ particle in a uniform, static, magnetic field pointed in the X axis.

At $t=0$, it's in the Z Spin-Up state $\chi_+^z$, and our measurements are happening in the $X$ basis.

Final Answer: A particle with spin in a magnetic field $\vec{B}=B\hat{x}$, with the $t=0$ state being $\ket{\chi_+^z}$.
