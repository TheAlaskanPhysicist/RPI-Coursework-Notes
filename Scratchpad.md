



Angular Position Stator
- 3D Joystick with 3 accumulators for Roll, Pitch, Yaw

Angular Velocity Stator
- 3D Joystick with 3 accumulators for Roll, Pitch, Yaw







Angular Control Unit ($\theta_x, \theta_y, \theta_z, \omega_x, \omega_y, \omega_z$)





For each angular direction
1. Set $R=R_0$, and $\dot{R}=0$ (Position Matching)
2. Set $\dot{R}=\dot{R}_0$ and $\ddot{R}=0$ (Velocity Matching)
3. Clamp $|\dot{R}|\le|\dot{R}_0|$ (Velocity Damping)
4. Align $R$ with gravity, and $\dot{R}=0$.


## PD Controller
We want to implement the equation
$$\begin{align}
T&=K_P(\vec\omega_0)\left(\vec\theta_0-\vec\theta\right)+K_D\left(\vec\omega_0-\vec\omega\right)
\end{align}$$
The control table is then as follows



| Control State  | Effect                                                               |
| -------------- | -------------------------------------------------------------------- |
| PD OFF         | Manual Pilot Control                                                 |
| PD ON + GA OFF | Read $\vec\theta_0$ and $\vec\omega_0$ Accumulators (See Next Table) |
| PD ON + GA ON  | Set $\vec\theta_0\sim\text{Gyroline}$ and $\vec\omega_0=0$           |



| PD Non-Gravity (For Each Axis)     | $K_P$  | $\vec\theta_0$ | $K_D$  | $\vec\omega_0$    | Effect            |
| ---------------------------------- | ------ | -------------- | ------ | ----------------- | ----------------- |
| $\vec\theta_0$, $\vec\omega_0=0$   | Const. | Given          | Const. | Given, always $0$ | Position Matching |
| $\vec\theta_0$, $\vec\omega_0\ne0$ | $=0$   | Ignored        | Const. | Given             | Velocity Matching |
Note: $\vec\omega_0$ gets clamped to enforce Velocity Damping.

| PD Gravity (For Each Axis) | $K_P$  | $\vec\theta_0$ | $K_D$                   | $\vec\omega_0$ | Effect         |
| -------------------------- | ------ | -------------- | ----------------------- | -------------- | -------------- |
| ON                         | Const. | Set Auto       | Const., set $0$ for Yaw | Set Auto       | Grav Alignment |




PD Circuit Input Controller ON
1. Roll Axis
	1. If GA: $\vec\theta_0=\text{Gyroline Roll}$, $\vec\omega_0=0$.
	2. If !GA and $\vec\omega_0=0$: $\vec\theta_0=\text{Accum Roll}$, $\vec\omega_0=0$.
	3. If !GA and $\vec\omega_0\ne0$: $K_P=0$, $\vec\omega_0=\text{Accum Roll Vel}$.
2. Pitch Axis
	1. If GA: $\vec\theta_0=\text{Gyroline Pitch}$, $\vec\omega_0=0$.
	2. If !GA and $\vec\omega_0=0$: $\vec\theta_0=\text{Accum Pitch}$, $\vec\omega_0=0$.
	3. If !GA and $\vec\omega_0\ne0$: $K_P=0$, $\vec\omega_0=\text{Accum Pitch Vel}$.
3. Yaw Axis
	1. If GA: $K_P=0$, $\vec\omega_0=0$.
	2. If !GA and $\vec\omega_0=0$: $\vec\theta_0=\text{Accum Yaw}$, $\vec\omega_0=0$.
	3. If !GA and $\vec\omega_0\ne0$: $K_P=0$, $\vec\omega_0=\text{Accum Yaw Vel}$.




Input Schema
1. Manual Pilot 3D Joystick
2. Angular Position 3D Joystick (For setting wanted angle)
	1. Needs a 4-Input Display for current RPY
	2. Reset button
3. Angular Velocity 3D Joystick (For setting wanted angle)
	1. Should have the 4-Input screen for RPY
	2. Should have a reset button for clearing





## Translation RCS
Given 3 speedometers on the spaceship coordinate axis, we can calculate all translation as
$$\begin{align}
v&=s_x\hat{x}+s_y\hat{z}+s_z\hat{z}
\end{align}$$





$$\begin{align}
\lim_{n\to\infty}f_n'(x)
&=\lim_{n\to\infty}\lim_{dx\to0}\dfrac{f_n(x+dx)-f_n(x)}{dx}\\
&=\lim_{n\to\infty}\lim_{dx\to0}\dfrac{\left(1+\frac{x+dx}{n}\right)^n-\left(1+\frac{x}{n}\right)^n}{dx}\\
&=\lim_{n\to\infty}\lim_{dx\to0}\dfrac{\sum_{k=0}^n\binom{n}{k}\left(\frac{x+dx}{n}\right)^k-\sum_{k=0}^n\binom{n}{k}\left(\frac{x}{n}\right)^k}{dx}\\
&=\lim_{n\to\infty}\lim_{dx\to0}\dfrac{\sum_{k=0}^n\binom{n}{k}\frac{1}{n^k}\sum_{l=0}^kx^{k-l}dx^{l}-\sum_{k=0}^n\binom{n}{k}\left(\frac{x}{n}\right)^k}{dx}\\
&=\lim_{n\to\infty}\lim_{dx\to0}\dfrac{1+x+dx+\sum_{k=2}^n\binom{n}{k}\frac{1}{n^k}\sum_{l=0}^kx^{k-l}dx^{l}-1-x-\sum_{k=2}^n\binom{n}{k}\left(\frac{x}{n}\right)^k}{dx}\\
&=\lim_{n\to\infty}\lim_{dx\to0}1+\dfrac{\sum_{k=2}^n\binom{n}{k}\frac{1}{n^k}\sum_{l=0}^kx^{k-l}dx^{l}-\sum_{k=2}^n\binom{n}{k}\left(\frac{x}{n}\right)^k}{dx}\\
\end{align}$$




$$\begin{align}
\lim_{n\to\infty}f_n(x)&=\lim_{n\to\infty}\left(1+\frac{x}{n}\right)^n\\
\lim_{n\to\infty}f_n'(x)&=\left(1+\frac{x}{n}\right)^n\\
\end{align}$$






$$\begin{align}
\lim_{n\to\infty}\frac{f_n'(x)}{f_n(x)}
&=\lim_{n\to\infty}\frac{\left(1+\frac{x}{n}\right)^n}{\left(1+\frac{x}{n}\right)^{n-1}}\\
\lim_{n\to\infty}\frac{f_n'(x)}{f_n(x)}&=\lim_{n\to\infty}\left(1+\frac{x}{n}\right)=1
\end{align}$$

$$\begin{align}
f_n(x)&=\left(1+\frac{x}{n}\right)^n\\
f_n'(x)&=\left(1+\frac{x}{n}\right)^{n-1}\\
f_n''(x)&=\left(1-\frac{1}{n}\right)\left(1+\frac{x}{n}\right)^{n-2}\\
\end{align}$$




$$\begin{align}
\left[-\frac{\hbar^2}{2\mu}\vec\nabla^2-\dfrac{e^2}{4\pi\epsilon_0 r}\right]\psi(r,\theta,\phi)&=E\psi(r,\theta,\phi)
\end{align}$$



