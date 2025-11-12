Author: Stanley Goodwin
Date: November 2nd, 2025

---
## Question 2.37
Consider an electron confined to the interior of a hollow cylindrical shell whose axis coincides with the $z$-axis. The wave function is required to vanish on the inner and outer walls, $\rho=\rho_a$ and $\rho_b$, and also at the top and bottom, $z = 0$ and $L$.

---
### Question 2.37.A
Find the energy eigenfunctions. (Do not bother with normalization.) Show that the energy eigenvalues are given by:
$$\begin{align}
E_{lmn}&=\dfrac{\hbar^2}{2m_e}\left[k_{mn}^2+\left(\dfrac{l\pi}{L}\right)^2\right]
\end{align}$$
where $k_{mn}$ is the $n$-th root of the transcendental equation:
$$\begin{align}
J_m(k_{mn}\rho_b)N_m(k_{mn}\rho_a)-N_m(k_{mn}\rho_b)J_m(k_{mn}\rho_a)&=0
\end{align}$$
Also find the velocity $v$ for the linear (i.e. incorrect classical) path.

We start with the 3D Schrodinger Equation, and use that the system is a cylinder:
$$\begin{align}
-\dfrac{2m}{\hbar^2}\hat{H}\psi&=\dfrac{1}{r}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial\psi}{\partial r}\right)+\dfrac{1}{r^2}\dfrac{\partial^2\psi}{\partial \phi^2}+\dfrac{\partial^2\psi}{\partial z^2}
\end{align}$$
With each coordinate being orthogonal, let $\psi$ be the product of 3 independent functions:
$$\begin{align}
-\dfrac{2m_e}{\hbar^2}\hat{H}\cdot R(r)\Phi(\phi)Z(z)&=\dfrac{1}{r}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)\Phi(\phi)Z(z)+\dfrac{1}{r^2}\dfrac{\partial^2\Phi(\phi)}{\partial \phi^2}R(r)Z(z)+\dfrac{\partial^2Z(z)}{\partial z^2}R(r)\Phi(\phi)\\
-\dfrac{2mE_{\psi}}{\hbar^2}&=\dfrac{1}{rR(r)}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)+\dfrac{1}{r^2\Phi(\phi)}\dfrac{\partial^2\Phi(\phi)}{\partial \phi^2}+\dfrac{1}{Z(z)}\dfrac{\partial^2Z(z)}{\partial z^2}\\
\end{align}$$
Because I already have an idea for how this PDE is solved, lets do $Z$ and $\Phi$ first:
$$\begin{align}
\dfrac{1}{Z(z)}\dfrac{\partial^2Z(z)}{\partial z^2}&=-k_z^2\\
\dfrac{\partial^2Z(z)}{\partial z^2}&=-k_z^2Z(z)\\
Z(z)&=A_z\sin(k_zz)+B_z\cos(k_zz)\\
Z(0)&=A_z\cdot0+B_z\cdot1=0\\
Z(L)&=A_z\sin\left(k_zL\right)=0\\\\
\Aboxed{Z_l(z)&=A_z\sin\left(k_zz\right), \ \ \ k_z=\dfrac{l\pi}{L}}
\end{align}$$
$$\begin{align}
\dfrac{1}{\Phi(\phi)}\dfrac{\partial^2\Phi(\phi)}{\partial \phi^2}&=-m^2\\
\dfrac{\partial^2\Phi(\phi)}{\partial \phi^2}&=-m^2\Phi(\phi)\\
\Phi_m(\phi)&=A_\phi e^{im\phi}+B_\phi e^{-im\phi}\\
\Phi_{-m}(\phi)&=A_\phi e^{-im\phi}+B_\phi e^{+im\phi}\\
\Aboxed{\Phi_m(\phi)&=A_\phi e^{im\phi}}
\end{align}$$
Substituting these back in, we see:
$$\begin{align}
-\dfrac{2mE_{\psi}}{\hbar^2}&=\dfrac{1}{rR(r)}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)+\dfrac{1}{r^2\Phi(\phi)}\dfrac{\partial^2\Phi(\phi)}{\partial \phi^2}+\dfrac{1}{Z(z)}\dfrac{\partial^2Z(z)}{\partial z^2}\\
-\dfrac{2mE_{\psi}}{\hbar^2}&=\dfrac{1}{rR(r)}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)-m^2\dfrac{1}{r^2}\dfrac{\Phi(\phi)}{\Phi(\phi)}-k_z^2\dfrac{Z(z)}{Z(z)}\\
-\dfrac{2mE_{\psi}}{\hbar^2}&=\dfrac{1}{rR(r)}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)-\dfrac{m^2}{r^2}-k_z^2\\
0&=\dfrac{r}{R(r)}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)+\left(\dfrac{2mE_{\psi}}{\hbar^2}-k_z^2\right)r^2-m^2\\
\end{align}$$
Let $k_r^2=\dfrac{2mE_{\psi}}{\hbar^2}-k_z^2$, then:
$$\begin{align}
0&=r\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)+\left(k_r^2r^2-m^2\right)R(r)\\
0&=r^2\dfrac{\partial^2R(r)}{\partial r^2}+r\dfrac{\partial R(r)}{\partial r}+\left(k_r^2r^2-m^2\right)R(r)\\
\end{align}$$
I had to look up the Bessel functions because it's been forever since I've used them.
However, they solve this system, and so:
$$\begin{align}
R(r)&=A_rJ_m(k_rr)+B_rN_m(k_rr)\\
R(\rho_a)&=A_rJ_m(k_r\rho_a)+B_rN_m(k_r\rho_a)=0\\
R(\rho_b)&=A_rJ_m(k_r\rho_b)+B_rN_m(k_r\rho_b)=0\\
\end{align}$$
I think we need to make this represented as a matrix:
$$\begin{align}
\begin{bmatrix}J_m(k_r\rho_a)&N_m(k_r\rho_a)\\J_m(k_r\rho_b)&N_m(k_r\rho_b)\end{bmatrix}\begin{bmatrix}A_r\\B_r\end{bmatrix}&=\begin{bmatrix}0\\0\end{bmatrix}\\
\end{align}$$
To have this system become null regardless of coefficient, the determinant must be 0:
$$\begin{align}
J_m(k_r\rho_a)N_m(k_r\rho_b)-J_m(k_r\rho_b)N_m(k_r\rho_a)&=0
\end{align}$$
Going back to the beginning. We know that this wavefunction is parametrized by 3 values:
$$\begin{align}
\hat{H}\psi_{lmn}&=E_{lmn}\psi_{lmn}
\end{align}$$
Our wavenumber(s) are dependent on energy, and so:
$$\begin{align}
k_z&=\dfrac{l\pi}{L}\\
k_r^2&=\dfrac{2m_eE_{lmn}}{\hbar^2}-\left(\dfrac{l\pi}{L}\right)^2\\
\Aboxed{E_{lmn}&=\dfrac{\hbar^2}{2m_e}\left[k_{nm}^2+\left(\dfrac{l\pi}{L}\right)^2\right]}
\end{align}$$
Our wavenumber in the radial direction is also parametrized by $n,m$, and so:
$$\begin{align}
\Aboxed{J_m(k_{nm}\rho_a)N_m(k_{nm}\rho_b)-J_m(k_{nm}\rho_b)N_m(k_{nm}\rho_a)&=0}
\end{align}$$
#### Velocity
It took me a while to understand what it was asking, but I think it's just the following:
$$\begin{align}
T&=E_{lmn}\\
\dfrac{1}{2}m_e v^2&=\dfrac{\hbar^2}{2m_e}\left[k_{nm}^2+\left(\dfrac{l\pi}{L}\right)^2\right]\\
v^2&=\dfrac{\hbar^2}{m_e^2}\left[k_{nm}^2+\left(\dfrac{l\pi}{L}\right)^2\right]\\
\Aboxed{|v|&=\dfrac{\hbar}{m_e}\sqrt{k_{nm}^2+\left(\dfrac{l\pi}{L}\right)^2}}
\end{align}$$
---
### Question 2.37.B
Repeat the same problem when there is a uniform magnetic field $\vec{B}=B\hat{z}$ for $0<\rho<\rho_a$. Note that the energy eigenvalues are influenced by the magnetic field even though the electron never "touches" the magnetic field.

Introducing this new field term (I've seen this field 100 times before so I know the answer):
$$\begin{align}
\vec{A}&=\dfrac{\Phi}{2\pi r}\hat{\phi} & \vec\nabla\times\vec A&=\vec{B}
\end{align}$$
The equation for the Hamiltonian is then:
$$\begin{align}
\hat{H}\psi&=\dfrac{1}{2m}\left(-i\hbar\vec\nabla-q\vec{A}\right)^2\psi\\
&=\dfrac{1}{2m}\left[\left(i\hbar\vec\nabla\right)\left(i\hbar\vec\nabla\right)+\left(i\hbar\vec\nabla\right)\left(q\vec{A}\right)+\left(q\vec{A}\right)\left(i\hbar\vec\nabla\right)+\left(q\vec{A}\right)\left(q\vec{A}\right)\right]\psi\\
&=\dfrac{1}{2m}\left[\left(i\hbar\vec\nabla\right)\left(i\hbar\vec\nabla \psi\right)+\left(i\hbar\vec\nabla\right)\left(q\vec{A}\psi\right)+\left(q\vec{A}\right)\left(i\hbar\vec\nabla \psi\right)+\left(q\vec{A}\right)\left(q\vec{A}\psi\right)\right]\\
&=\dfrac{1}{2m}\left[-\hbar^2\vec\nabla^2+i\hbar q\left(\vec\nabla\cdot\vec{A}\right)\psi+i\hbar q \vec{A}\cdot\vec\nabla\psi+i\hbar q\vec{A}\cdot\vec\nabla \psi+q^2\vec{A}^2\psi\right]\\
&=-\dfrac{\hbar^2}{2m}\vec\nabla^2+\dfrac{i\hbar q}{2m}\left(\vec\nabla\cdot\vec{A}\right)\psi+\dfrac{2i\hbar q}{2m} \vec{A}\cdot\vec\nabla\psi+\dfrac{q^2}{2m}\vec{A}^2\psi\\
\hat{H}\psi&=-\dfrac{\hbar^2}{2m}\vec\nabla^2+\dfrac{i\hbar q}{2m}\left(\vec\nabla\cdot\vec{A}\right)\psi+\dfrac{i\hbar q}{m} \vec{A}\cdot\vec\nabla\psi+\dfrac{q^2}{2m}\vec{A}^2\psi\\
\end{align}$$
We're going to need our relationships for the Vector Potential:
$$\begin{align}
\vec\nabla&=\dfrac{1}{r}\dfrac{\partial}{\partial\phi}\hat\phi+\dots & \vec{A}&=\dfrac{\Phi}{2\pi r}\hat{\phi}
\end{align}$$
$$\begin{align}
\vec\nabla\cdot\vec{A}&=\dfrac{1}{r}\dfrac{\partial}{\partial\phi}\hat\phi\cdot\dfrac{\Phi}{2\pi r}\hat{\phi}\\
&=\dfrac{1}{r}\dfrac{\partial}{\partial\phi}\dfrac{\Phi}{2\pi r}\\
\Aboxed{\vec\nabla\cdot\vec{A}&=0}\\\\
\vec{A}\cdot\vec\nabla&=\dfrac{\Phi}{2\pi r}\hat{\phi}\cdot\dfrac{1}{r}\dfrac{\partial}{\partial\phi}\hat\phi\\
\Aboxed{\vec{A}\cdot\vec\nabla&=\dfrac{\Phi}{2\pi r^2}\dfrac{\partial}{\partial\phi}}\\\\
\Aboxed{\vec{A}^2&=\dfrac{\Phi^2}{4\pi^2 r^2}}
\end{align}$$
Substituting, we get:
$$\begin{align}
\hat{H}\psi&=-\dfrac{\hbar^2}{2m}\vec\nabla^2+\dfrac{i\hbar q}{2m}\left(\vec\nabla\cdot\vec{A}\right)\psi+\dfrac{i\hbar q}{m} \vec{A}\cdot\vec\nabla\psi+\dfrac{q^2}{2m}\vec{A}^2\psi\\
&=-\dfrac{\hbar^2}{2m}\vec\nabla^2+\dfrac{i\hbar q\Phi}{2\pi mr^2}\dfrac{\partial\psi}{\partial\phi}+\dfrac{q^2\Phi^2}{8\pi^2 mr^2}\psi\\
\end{align}$$
Lets use our solutions from earlier:
$$\begin{align}
\psi&=R(r)\Phi(\phi)Z(z) & \Phi(\phi)&=e^{im\phi}
\end{align}$$
Then we can see:
$$\begin{align}
\hat{H}&=-\dfrac{\hbar^2}{2m}\left(\dfrac{1}{rR(r)}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)+\dfrac{1}{r^2\Phi(\phi)}\dfrac{\partial^2\Phi(\phi)}{\partial \phi^2}+\dfrac{1}{Z(z)}\dfrac{\partial^2Z(z)}{\partial z^2}\right)\\
&+\dfrac{i\hbar q\Phi}{2\pi mr^2\Phi(\phi)}\dfrac{\partial\Phi(\phi)}{\partial\phi}+\dfrac{q^2\Phi^2}{8\pi^2 mr^2}\\\\
-\dfrac{2m_e}{\hbar^2}E_{nlm}&=\dfrac{1}{rR(r)}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)-\dfrac{m^2}{r^2}+\dfrac{1}{Z(z)}\dfrac{\partial^2Z(z)}{\partial z^2}+\dfrac{2m q\Phi}{h r^2}-\dfrac{q^2\Phi^2}{h^2 r^2}\\
-\dfrac{2m_e}{\hbar^2}E_{nlm}r^2&=\dfrac{r^2}{rR(r)}\dfrac{\partial}{\partial r}\left(r\dfrac{\partial R(r)}{\partial r}\right)-m^2-k_z^2r^2+\dfrac{2m q\Phi}{h}-\dfrac{q^2\Phi^2}{h^2}\\
0&=\dfrac{r^2}{R(r)}\dfrac{\partial^2R(r)}{\partial r^2}+\dfrac{r}{R(r)}\dfrac{\partial R(r)}{\partial r}+\left[\left(\dfrac{2m_e}{\hbar^2}E_{nlm}-k_z^2\right)r^2-\left(m^2+\dfrac{q^2\Phi^2}{h^2}-\dfrac{2m q\Phi}{h}\right)\right]\\
0&=r^2\dfrac{\partial^2R(r)}{\partial r^2}+r\dfrac{\partial R(r)}{\partial r}+\left[\left(\dfrac{2m_e}{\hbar^2}E_{nlm}-k_z^2\right)r^2-\left(m^2+\dfrac{q^2\Phi^2}{h^2}-\dfrac{2m q\Phi}{h}\right)\right]R(r)\\
\end{align}$$
Let the following values exist:
$$\begin{align}
k_{nm}^2&=\dfrac{2m_e}{\hbar^2}E_{nlm}-k_z^2\\
\alpha^2&=m^2-\dfrac{2m q\Phi}{h}+\dfrac{q^2\Phi^2}{h^2}
\end{align}$$
Therefore:
$$\begin{align}
0&=r^2\dfrac{\partial^2R(r)}{\partial r^2}+r\dfrac{\partial R(r)}{\partial r}+\left(k_{nm}^2r^2-\alpha^2\right)R(r)\\
\end{align}$$
Since it's now in the proper form, we then have the solutions:
$$\begin{align}
\Aboxed{R(r)&=AJ_\alpha(k_{nm}r)+BN_\alpha(k_{nm}r)}\\
\Aboxed{Z_l(z)&=\sin\left(k_zz\right)}\\
\Aboxed{\Phi_m(\phi)&=e^{im\phi}}
\end{align}$$
Under the following conditions:
$$\begin{align}
k_z&=\dfrac{l\pi}{L}\\
k_{nm}^2&=\dfrac{2m_e}{\hbar^2}E_{nlm}-k_z^2\\
\alpha^2&=m^2-\dfrac{2m q\Phi}{h}+\dfrac{q^2\Phi^2}{h^2}\\
0&=J_\alpha(k_{nm}\rho_a)N_\alpha(k_{nm}\rho_b)-J_\alpha(k_{nm}\rho_b)N_\alpha(k_{nm}\rho_a)
\end{align}$$
Lets take a closer look at $\alpha$:
$$\begin{align}
\alpha^2&=m^2-\dfrac{2m q\Phi}{h}+\dfrac{q^2\Phi^2}{h^2}\\
&=m^2-\dfrac{2m q\Phi}{h}+\left(-\dfrac{1}{2}\dfrac{2m q\Phi}{h}\right)^2\dfrac{q^2\Phi^2}{h^2}-\left(-\dfrac{1}{2}\dfrac{2m q\Phi}{h}\right)^2\\
&=\left(m-\dfrac{q\Phi}{h}\right)^2+\dfrac{q^2\Phi^2}{h^2}-\left(\dfrac{q\Phi}{h}\right)^2\\
\alpha^2&=\left(m-\dfrac{q\Phi}{h}\right)^2+0\\
\Aboxed{\alpha&=m-\dfrac{q\Phi}{h}=m-\nu}
\end{align}$$
There we go. And so!
$$\begin{align}
\Aboxed{R(r)&=AJ_{m-\nu}(k_{nm}r)+BN_{m-\nu}(k_{nm}r)} & \Aboxed{Z_l(z)&=\sin\left(\dfrac{l\pi}{L}z\right)} & \Aboxed{\Phi_m(\phi)&=e^{im\phi}}
\end{align}$$
Under the conditions:
$$\begin{align}
k_{nm}^2&=\dfrac{2m_e}{\hbar^2}E_{nlm}-\left(\dfrac{l\pi}{L}\right)^2, \ \ \ \nu=\dfrac{q\Phi}{h}\\
0&=J_{m-\nu}(k_{nm}\rho_a)N_{m-\nu}(k_{nm}\rho_b)-J_{m-\nu}(k_{nm}\rho_b)N_{m-\nu}(k_{nm}\rho_a)
\end{align}$$
Lastly, I still have all of this written in terms of flux, and so energy:
$$\begin{align}
\Aboxed{E_{nlm}(\nu)&=\dfrac{\hbar^2}{2m_e}\left[k_{nm}(\nu)^2+\left(\dfrac{l\pi}{L}\right)^2\right]}
\end{align}$$
It might look like the energy is the same, but $k_{mn}$ is dependent on $\nu$, with condition:
$$\begin{align}
\Aboxed{J_{m-\nu}(k_{nm}\rho_a)N_{m-\nu}(k_{nm}\rho_b)-J_{m-\nu}(k_{nm}\rho_b)N_{m-\nu}(k_{nm}\rho_a)&=0}
\end{align}$$
---
### Question 2.37.C
Compare, in particular, the ground state of the $B=0$ problem with that of the $B\ne0$ problem. Show that if we require the ground-state energy to be unchanged in the presence of $B$, we obtain "flux quantization"
$$\begin{align}
\pi\rho_a^2 B&=\dfrac{2\pi N\hbar c}{e}
\end{align}$$
Lets start with the equation we have for energy:
$$\begin{align}
E_{nlm}(\nu)&=\dfrac{\hbar^2}{2m_e}\left[k_{nm}(\nu)^2+\left(\dfrac{l\pi}{L}\right)^2\right]
\end{align}$$
When $B=0$, there is no field, and therefore $\nu=\dfrac{q\Phi}{h}=0$, with energy:
$$\begin{align}
_{B=0}E_{nlm}(0)&=\dfrac{\hbar^2}{2m_e}\left[k_{nm}(0)^2+\left(\dfrac{l\pi}{L}\right)^2\right]
\end{align}$$
The ground state is $n=1,l=1,m=0$, and so:
$$\begin{align}
_{B=0}E_{\text{ground}}&=\dfrac{\hbar^2}{2m_e}\left[k_{10}(0)^2+\left(\dfrac{\pi}{L}\right)^2\right]\\
0&=J_{0}(k_{10}\rho_a)N_{0}(k_{10}\rho_b)-J_{0}(k_{10}\rho_b)N_{0}(k_{10}\rho_a)
\end{align}$$
With an added flux, the magnetic quantum number changes:
$$\begin{align}
E_{\text{ground}}(\nu)&=\dfrac{\hbar^2}{2m_e}\left[k_{10}(\nu)^2+\left(\dfrac{\pi}{L}\right)^2\right]\\
0&=J_{-\nu}(k_{10}\rho_a)N_{-\nu}(k_{10}\rho_b)-J_{-\nu}(k_{10}\rho_b)N_{-\nu}(k_{10}\rho_a)
\end{align}$$
The question wants the energy to be unchanged, and so:
$$\begin{align}
_{B=0}E_{\text{ground}}&=E_{\text{ground}}(\nu)\\
\dfrac{\hbar^2}{2m_e}\left[k_{10}(0)^2+\left(\dfrac{\pi}{L}\right)^2\right]&=\dfrac{\hbar^2}{2m_e}\left[k_{10}(\nu)^2+\left(\dfrac{\pi}{L}\right)^2\right]\\
k_{10}(0)^2+\left(\dfrac{\pi}{L}\right)^2&=k_{10}(\nu)^2+\left(\dfrac{\pi}{L}\right)^2\\
k_{10}(0)^2&=k_{10}(\nu)^2\\
\Aboxed{|k_{10}(0)|&=|k_{10}(\nu)|}
\end{align}$$
I assume what you expect me to write is "the periodicity of the Bessel function enforces that $\nu$ is an integer" but as to actually why? All I know is that $J_{-\nu}=(-1)^\nu J_{\nu}$, but you wouldn't believe how long it took to find that relation.

Therefore, the flux is quantized since $\nu$ is quantized, and so:
$$\begin{align}
\Phi&=\iint\vec{B}\cdot\vec{n}\ dA\\
&=\int_0^{2\pi}\int_0^{\rho_a}B\ r\ dr\ d\phi\\
&=2\pi\left.B\dfrac{r^2}{2}\right|_0^{\rho_a}\\
\Aboxed{\Phi&=\pi\rho_a^2B}
\end{align}$$
$$\begin{align}
\nu&=\dfrac{e\Phi}{h} & \implies && \Phi&=\dfrac{2\pi\hbar\nu}{e}
\end{align}$$
Combining, we get (and substituting $\nu=N$):
$$\begin{align}
\Aboxed{\pi\rho_a^2B&=\dfrac{2\pi\hbar N}{e}}
\end{align}$$
I have 0 idea where we're getting a $c$ from but all I can assume is that the textbook uses Gaussian units (I hate Gaussian units) instead of SI units.

---
## Question 2.49
An electron moves in the presence of a uniform magnetic field in the z-direction ($\vec{B}=B\hat{z}$).
### Question 2.49.A
Evaluate $\left[\Pi_x,\Pi_y\right]$, where:
$$\begin{align}
\Pi_x&=p_x-\dfrac{e}{c}A_x\\
\Pi_y&=p_y-\dfrac{e}{c}A_y
\end{align}$$
Not sure what to say. I just need a spacer:
$$\begin{align}
\left[\Pi_x,\Pi_y\right]&=\Pi_x\Pi_y-\Pi_y\Pi_x\\
&=\left(p_x-\dfrac{e}{c}A_x\right)\left(p_y-\dfrac{e}{c}A_y\right)-\left(p_y-\dfrac{e}{c}A_y\right)\left(p_x-\dfrac{e}{c}A_x\right)\\
&=\left(p_xp_y-\dfrac{e}{c}A_xp_y-\dfrac{e}{c}p_xA_y+\dfrac{e^2}{c^2}A_xA_y\right)-\left(p_yp_x-\dfrac{e}{c}A_yp_x-\dfrac{e}{c}p_yA_x+\dfrac{e^2}{c^2}A_yA_x\right)\\
&=p_xp_y-p_yp_x-\dfrac{e}{c}\left(A_xp_y-p_yA_x\right)-\dfrac{e}{c}\left(p_xA_y-A_yp_x\right)+\dfrac{e^2}{c^2}\left(A_xA_y-A_yA_x\right)\\
&=[p_x,p_y]-\dfrac{e}{c}\left[A_x,p_y\right]-\dfrac{e}{c}\left[p_x,A_y\right]+\dfrac{e^2}{c^2}\left[A_x,A_y\right]
\end{align}$$
Using what we had in the textbook:
$$\begin{align}
\left[F(\vec{x}),p_i\right]&=i\hbar\dfrac{\partial F}{\partial x_i}\\
\left[p_i,p_j\right]&=0\\
\left[A_i,A_j\right]&=0\\
\end{align}$$
And so we then have:
$$\begin{align}
\left[\Pi_x,\Pi_y\right]&=[p_x,p_y]-\dfrac{e}{c}\left[A_x,p_y\right]-\dfrac{e}{c}\left[p_x,A_y\right]+\dfrac{e^2}{c^2}\left[A_x,A_y\right]\\
&=0-\dfrac{e}{c}i\hbar\dfrac{\partial A_x}{\partial y}+\dfrac{e}{c}i\hbar\dfrac{\partial A_y}{\partial x}+0\\
&=\dfrac{i\hbar e}{c}\left(\dfrac{\partial A_y}{\partial x}-\dfrac{\partial A_x}{\partial y}\right)\\
&=-\dfrac{i\hbar e}{c}\left(\dfrac{\partial A_x}{\partial y}-\dfrac{\partial A_y}{\partial x}\right)\\
\end{align}$$
This looks like the curl, so we can then find the final relationship as:
$$\begin{align}
\Aboxed{\left[\Pi_x,\Pi_y\right]&=-\dfrac{i\hbar e}{c}B_z}\\
\end{align}$$
---
### Question 2.49.B
By comparing the Hamiltonian and the commutation relation obtained in (a) with those of the one-dimensional oscillator problem, show how we can immediately write the energy eigenvalues as:
$$\begin{align}
E_{k,n}&=\dfrac{\hbar^2k^2}{2m}+\left(\dfrac{|eB|\hbar}{mc}\right)\left(n+\dfrac{1}{2}\right)
\end{align}$$
where $\hbar k$ is the continuous eigenvalue of the $p_z$ operator and $n\ge0$.

I'm going to just take a wild guess:
$$\begin{align}
H_{x,y}&=\dfrac{\Pi_x^2}{2m}+\dfrac{\Pi_y^2}{2m}\\
&=\dfrac{1}{2m}\left(\Pi_x^2+\Pi_y^2\right)\\
&=\dfrac{1}{2m}\left(\Pi_x+i\Pi_y\right)\left(\Pi_x-i\Pi_y\right)+i\dfrac{\left[\Pi_x,\Pi_y\right]}{2m}\\
&=\dfrac{1}{2m}\left(\Pi_x+i\Pi_y\right)\left(\Pi_x-i\Pi_y\right)+\dfrac{\hbar eB_z}{2mc}\\
&=\dfrac{\hbar eB_z}{mc}\left(\dfrac{c}{2\hbar eB_z}\left(\Pi_x+i\Pi_y\right)\left(\Pi_x-i\Pi_y\right)+\dfrac{1}{2}\right)\\
&=\dfrac{\hbar eB_z}{mc}\left(\dfrac{\left(\Pi_x+i\Pi_y\right)}{\sqrt{2\hbar eB_z/c}}\dfrac{\left(\Pi_x-i\Pi_y\right)}{\sqrt{2\hbar eB_z/c}}+\dfrac{1}{2}\right)\\
\end{align}$$
Interesting, so these are like the creation and annihilation operator:
$$\begin{align}
a&=\dfrac{\Pi_x-i\Pi_y}{\sqrt{2\hbar eB_z/c}} & a^\dagger&=\dfrac{\Pi_x+i\Pi_y}{\sqrt{2\hbar eB_z/c}}
\end{align}$$
If do you the math, it does actually have the same commutator.

Therefore we have:
$$\begin{align}
H_{x,y}&=\dfrac{\hbar eB_z}{mc}\left(a^\dagger a+\dfrac{1}{2}\right)\\
\end{align}$$
Our total energy is the total Hamiltonian:
$$\begin{align}
H&=H_z+H_{x,y}=\dfrac{\hbar^2k^2}{2m}+\dfrac{\hbar eB_z}{mc}\left(a^\dagger a+\dfrac{1}{2}\right)\\
\Aboxed{E_{k,n}&=\dfrac{\hbar^2k^2}{2m}+\left(\dfrac{|eB|\hbar}{mc}\right)\left(n+\dfrac{1}{2}\right)}
\end{align}$$
Looks good to me!

---
## Question 3.3
Find, by explicit construction using Pauli matrices, the eigenvalues for the Hamiltonian:
$$\begin{align}
\hat{H}&=-\dfrac{2\mu}{\hbar}\vec{S}\cdot\vec{B}
\end{align}$$
for a spin particle in the presence of a magnetic field $\vec{B}=B_x\hat{x}+B_y\hat{y}+B_z\hat{z}$.
$$\begin{align}
\hat{H}&=-\dfrac{2\mu}{\hbar}\vec{S}\cdot\vec{B}\\
&=-\dfrac{2\mu}{\hbar}\left(B_x\sigma_x+B_y\sigma_y+B_z\sigma_z\right)\\
&=-\dfrac{2\mu}{\hbar}\left(B_x\begin{bmatrix}0&1\\1&0\end{bmatrix}+B_y\begin{bmatrix}0&-i\\i&0\end{bmatrix}+B_z\begin{bmatrix}1&0\\0&-1\end{bmatrix}\right)\\
\hat{H}&=-\dfrac{2\mu}{\hbar}\begin{bmatrix}B_z&B_x-iB_y\\B_x+iB_y&-B_z\end{bmatrix}
\end{align}$$
From here, we just diagonalize using eigenvalue-eigenvectors (let $\kappa=-\tfrac{2\mu}{\hbar}$):
$$\begin{align}
\det\left(\hat{H}-\lambda\mathbb{I}\right)&=\left|\begin{array}{cc}\kappa B_z-\lambda&\kappa(B_x-iB_y)\\\kappa(B_x+iB_y)&-\kappa B_z-\lambda\end{array}\right|\\
&=(\lambda+\kappa B_z)(\lambda-\kappa B_z)-\kappa^2(B_x+iB_y)(B_x-iB_y)\\
&=\lambda^2-\kappa^2 B_z^2-\kappa^2(B_x^2+B_y^2)\\
0&=\lambda^2-\kappa^2(B_x^2+B_y^2+B_z^2)\\
\lambda^2&=\kappa^2(B_x^2+B_y^2+B_z^2)\\
\Aboxed{\lambda&=\pm\tfrac{2\mu}{\hbar}|\vec{B}|}
\end{align}$$
---
## Question 3.4
Consider the 2×2 matrix defined by
$$\begin{align}
U&=\dfrac{a_0+i\vec\sigma\cdot\vec{a}}{a_0-i\vec\sigma\cdot\vec{a}}
\end{align}$$
where $a_0$ is a real number and $\vec{a}$ is a three-dimensional vector with real components
### Question 3.4.A
Prove that $U$ is unitary and unimodular.

This system is isomorphic to the Quaternions, so this makes it really simple:
$$\begin{align}
U^\dagger&=\left(\dfrac{a_0+i\vec\sigma\cdot\vec{a}}{a_0-i\vec\sigma\cdot\vec{a}}\right)^\dagger\\
&=\left((a_0+i\vec\sigma\cdot\vec{a})\dfrac{1}{a_0-i\vec\sigma\cdot\vec{a}}\right)^\dagger\\
&=\left(\dfrac{1}{a_0-i\vec\sigma\cdot\vec{a}}\right)^\dagger\left(a_0+i\vec\sigma\cdot\vec{a}\right)^\dagger\\
&=\left(\dfrac{1}{a_0+i\vec\sigma\cdot\vec{a}}\right)\left(a_0-i\vec\sigma\cdot\vec{a}\right)\\
U^\dagger&=\dfrac{a_0-i\vec\sigma\cdot\vec{a}}{a_0+i\vec\sigma\cdot\vec{a}}
\end{align}$$
We can then do the product of the two:
$$\begin{align}
\Aboxed{U^\dagger U&=\dfrac{a_0-i\vec\sigma\cdot\vec{a}}{a_0+i\vec\sigma\cdot\vec{a}}\cdot\dfrac{a_0+i\vec\sigma\cdot\vec{a}}{a_0-i\vec\sigma\cdot\vec{a}}=1}
\end{align}$$
For unimodularity:
$$\begin{align}
\det(a_0+i\vec\sigma\cdot\vec{a})&=a_0^2+|\vec{a}|^2\\
\det(a_0-i\vec\sigma\cdot\vec{a})&=a_0^2+|\vec{a}|^2\\
\det(U)&=\det\left((a_0+i\vec\sigma\cdot\vec{a})(a_0-i\vec\sigma\cdot\vec{a})^{-1}\right)\\
&=\dfrac{\det\left(a_0+i\vec\sigma\cdot\vec{a}\right)}{\det\left(a_0-i\vec\sigma\cdot\vec{a}\right)}\\
&=\dfrac{a_0^2+|\vec{a}|^2}{a_0^2+|\vec{a}|^2}\\
\Aboxed{\det(U)&=+1}\\
\end{align}$$
---
### Question 3.4.B
In general, a 2×2 unitary unimodular matrix represents a rotation in three dimensions. Find the axis and angle of rotation appropriate for $U$ in terms of $a_0, a_1, a_2, a_3$.

Doing this in the $\text{SU(2)}$ group is miserable. Attempting to convert to $\mathfrak{su}(2)$:
$$\begin{align}
U&=\dfrac{a_0+i\vec\sigma\cdot\vec{a}}{a_0-i\vec\sigma\cdot\vec{a}}\\
&=\dfrac{a_0+i\vec\sigma\cdot\vec{a}}{a_0-i\vec\sigma\cdot\vec{a}}\dfrac{a_0+i\vec\sigma\cdot\vec{a}}{a_0+i\vec\sigma\cdot\vec{a}}\\
&=\dfrac{(a_0+i\vec\sigma\cdot\vec{a})^2}{a_0^2+|\vec{a}|^2}\\
&=\dfrac{a_0^2+2ia_0\vec\sigma\cdot\vec{a}-|\vec{a}|^2}{a_0^2+|\vec{a}|^2}\\
\Aboxed{U&=\dfrac{a_0^2-|\vec{a}|^2}{a_0^2+|\vec{a}|^2}\mathbb{I}+i\dfrac{2a_0}{a_0^2+|\vec{a}|^2}\vec\sigma\cdot\vec{a}}
\end{align}$$
What we know is that the standard form for exponentials for Lie Group <-> Lie Algebras:
$$\begin{align}
e^{i\tfrac{\theta}{2}\vec\sigma\cdot\hat{n}}&=\cos\left(\tfrac{\theta}{2}\right)\mathbb{I}+i\sin\left(\tfrac{\theta}{2}\right)\vec\sigma\cdot\hat{n}
\end{align}$$
We can compare them, and see:
$$\begin{align}
\dfrac{a_0^2-|\vec{a}|^2}{a_0^2+|\vec{a}|^2}&=\cos\left(\tfrac{\theta}{2}\right)\\
\dfrac{2a_0}{a_0^2+|\vec{a}|^2}\vec\sigma\cdot\vec{a}&=\sin\left(\tfrac{\theta}{2}\right)\vec\sigma\cdot\hat{n}\\
\dfrac{2a_0|\vec{a}|}{a_0^2+|\vec{a}|^2}\vec\sigma\cdot\dfrac{\vec{a}}{|\vec{a}|}&=\sin\left(\tfrac{\theta}{2}\right)\vec\sigma\cdot\hat{n}\\
\dfrac{2a_0|\vec{a}|}{a_0^2+|\vec{a}|^2}\vec\sigma\cdot\hat{a}&=\sin\left(\tfrac{\theta}{2}\right)\vec\sigma\cdot\hat{n}
\end{align}$$
What we see then is:
$$\begin{align}
\cos\left(\tfrac{\theta}{2}\right)&=\dfrac{a_0^2-|\vec{a}|^2}{a_0^2+|\vec{a}|^2}\\
\sin\left(\tfrac{\theta}{2}\right)&=\dfrac{2a_0|\vec{a}|}{a_0^2+|\vec{a}|^2}\\
\hat{n}&=\hat{a}
\end{align}$$
**The rotation axis is the direction of the $\vec{a}$ vector**.

To find the angle, then we just need to use the relationships above:
$$\begin{align}
\dfrac{\sin\left(\tfrac{\theta}{2}\right)}{\cos\left(\tfrac{\theta}{2}\right)}&=\dfrac{\tfrac{2a_0|\vec{a}|}{a_0^2+|\vec{a}|^2}}{\tfrac{a_0^2-|\vec{a}|^2}{a_0^2+|\vec{a}|^2}}\\
\tan\left(\dfrac{\theta}{2}\right)&=\dfrac{2a_0|\vec{a}|}{a_0^2-|\vec{a}|^2}\\
\tan\left(\dfrac{\theta}{2}\right)&=\dfrac{2(|\vec{a}|/a_0)}{1-(|\vec{a}|/a_0)^2}
\end{align}$$
I want to use a double angle formula because it might turn out nicer:
$$\begin{align}
\tan(\theta/2)&=\dfrac{2\tan(\theta/4)}{1-\tan^2(\theta/4)}
\end{align}$$
Aha, I was correct. And so:
$$\begin{align}
\tan\left(\dfrac{\theta}{4}\right)&=\dfrac{|\vec{a}|}{a_0}\\
\Aboxed{\theta&=4\tan^{-1}\left(\dfrac{|\vec{a}|}{a_0}\right)}
\end{align}$$
So what we see is that it's a rotation around the $\vec{a}$ axis, by angle $\theta=4\tan^{-1}\left(\dfrac{|\vec{a}|}{a_0}\right)$.
