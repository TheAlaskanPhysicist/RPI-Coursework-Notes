


Suppose we directly send a state over a noisy channel:
$$\begin{align}
\rho_N\ket{\psi}&=\left[aF_N+b(1-F_N)\right]\ket{0}+\left[bF_N+a(1-F_N)\right]\ket{1}
\end{align}$$
When Bob measures this state, we expect that he will get the probabilities:
$$\begin{align}
p(\ket{\psi}=\ket{0})&=\left[aF_N+b(1-F_N)\right]^2\\
p(\ket{\psi}=\ket{1})&=\left[bF_N+a(1-F_N)\right]^2
\end{align}$$
Using Bell Teleportation, we have:
$$\begin{align}
p_m(\ket{\psi}=\ket{\psi}_0)&=(F_B)^m(F_N)^{n-m}\\
\dfrac{p_m(\ket{\psi}=\ket{\psi}_0)}{p_0(\ket{\psi}=\ket{\psi}_0)}&=\left(\dfrac{F_B}{F_N}\right)^{m}
\end{align}$$
If we did this directly to achieve the same rate as using Bell Teleportation, we get:
$$\begin{align}
\dfrac{n'-n}{m}&=\dfrac{\ln(F_B)}{\ln(F_N)}-1
\end{align}$$
Suppose we have a 97% fidelity for Bell States and 75% for normal channel:
$$\begin{align}
n'-n&=m\left(\dfrac{\ln(F_B)}{\ln(F_N)}-1\right)
\end{align}$$






## New Procedure
We (Alice) have a state $\ket\psi=a\ket{0}+b\ket{1}$ we want to transmit to Bob. We also have a shared entangled qubit from a trusted 3rd party with state $\ket{\phi^+}$ at preparation.

When Alice receives the Bell state, it is:
$$\begin{align}
\rho_B\ket{\phi^+}&=F_B\ket{\phi^+}+(1-F_B)\dfrac{\ket{\phi^-}+\ket{\psi^+}+\ket{\psi^-}}{3}\\
&=\dfrac{F_B}{\sqrt{2}}\left(\ket{00}+\ket{11}\right)+\dfrac{1-F_B}{3\sqrt{2}}\left(\ket{00}-\ket{11}+2\ket{01}\right)
\end{align}$$
The combined quantum state is:
$$\begin{align}
S_0=\ket{\psi}\rho_B\ket{\phi^+}&=\dfrac{aF_B}{\sqrt{2}}\left(\ket{0}\ket{00}+\ket{0}\ket{11}\right)+a\dfrac{1-F_B}{3\sqrt{2}}\left(\ket{0}\ket{00}-\ket{0}\ket{11}+2\ket{0}\ket{01}\right)\\
&+\dfrac{bF_B}{\sqrt{2}}\left(\ket{1}\ket{00}+\ket{1}\ket{11}\right)+b\dfrac{1-F_B}{3\sqrt{2}}\left(\ket{1}\ket{00}-\ket{1}\ket{11}+2\ket{1}\ket{01}\right)
\end{align}$$
Alice swaps the state of her Bell State Qubit and the state she wants to transmit:
$$\begin{align}
S_1&=\dfrac{aF_B}{\sqrt{2}}\left(\ket{0}\ket{00}+\ket{1}\ket{01}\right)+a\dfrac{1-F_B}{3\sqrt{2}}\left(\ket{0}\ket{00}-\ket{1}\ket{01}+2\ket{0}\ket{01}\right)\\
&+\dfrac{bF_B}{\sqrt{2}}\left(\ket{0}\ket{10}+\ket{1}\ket{11}\right)+b\dfrac{1-F_B}{3\sqrt{2}}\left(\ket{0}\ket{10}-\ket{1}\ket{11}+2\ket{0}\ket{11}\right)
\end{align}$$
Suppose that Bob now measures his Bell State Qubit:
$$\begin{align}
\sqrt{\dfrac{10F_B^2-2F_B+1}{18}}\bra{0}S_2&=\left(\dfrac{F_B}{\sqrt{2}}+\dfrac{1-F_B}{3\sqrt{2}}\right)\ket{0}(a\ket{0}+b\ket{1})\\
\sqrt{\dfrac{20F_B^2-16F_B+5}{18}}\bra{1}S_2&=\left(\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{0}+\dfrac{4F_B-1}{3\sqrt{2}}\ket{1}\right)\left(a\ket{0}+b\ket{1}\right)\\
\end{align}$$
Alice can choose to measure or not, but will make no difference. Thus, this fails.

If we rearrange the state to the following form:
$$\begin{align}
S_1&=\dfrac{2F_B+1}{3\sqrt{2}}\ket{0}\left(a\ket{0}+b\ket{1}\right)\ket{0}+\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{0}\left(a\ket{0}+b\ket{1}\right)\ket{1}\\
&+\dfrac{4F_B-1}{3\sqrt{2}}\ket{1}\left(a\ket{0}+b\ket{1}\right)\ket{1}
\end{align}$$
Instead, Bob does not measure the state yet, and the state is passed through the channel:
$$\begin{align}
S_2&=\dfrac{2F_B+1}{3\sqrt{2}}\left(F_N\ket{0}+(1-F_N)\ket{1}\right)\left(a\ket{0}+b\ket{1}\right)\ket{0}+\dfrac{2(1-F_B)}{3\sqrt{2}}\left(F_N\ket{0}+(1-F_N)\ket{1}\right)\left(a\ket{0}+b\ket{1}\right)\ket{1}\\
&+\dfrac{4F_B-1}{3\sqrt{2}}\ket{1}\left(a\ket{0}+b\ket{1}\right)\ket{1}
\end{align}$$


























There are two options for splitting here. Either Bob will measure next or the data will be transmit:
$$\begin{align}
\ket{\psi}\rho_B\ket{\phi^+}&\to\dfrac{2F_B+1}{3\sqrt{2}}\ket{0}\left(a\ket{0}+b\ket{1}\right)\ket{0}\\
&+\left(\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{0}+\dfrac{4F_B-1}{3\sqrt{2}}\ket{1}\right)\left(a\ket{0}+b\ket{1}\right)\ket{1}
\end{align}$$
$$\begin{align}
\ket{\psi}\rho_B\ket{\phi^+}&\to\ket{0}\left(a\dfrac{2F_B+1}{3\sqrt{2}}\ket{00}+a\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{01}+b\dfrac{2F_B+1}{3\sqrt{2}}\ket{10}+b\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{11}\right)\\
&+\dfrac{4F_B-1}{3\sqrt{2}}\ket{1}\left(a\ket{0}+b\ket{1}\right)\ket{{1}}
\end{align}$$
Option A: Bob Measures.
$$\begin{align}
\bra{0}S_1&\propto\dfrac{2F_B+1}{3\sqrt{2}}\ket{0}\left(a\ket{0}+b\ket{1}\right)\\
\bra{1}S_1&\propto\left(\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{0}+\dfrac{4F_B-1}{3\sqrt{2}}\ket{1}\right)\left(a\ket{0}+b\ket{1}\right)
\end{align}$$
Then transmitted:
$$\begin{align}
\bra{0}S_1&\to\dfrac{2F_B+1}{3\sqrt{2}}\left(F_N\ket{0}+(1-F_N)\ket{1}\right)\left(a\ket{0}+b\ket{1}\right)\\
\bra{1}S_1&\to\left(-\dfrac{6F_NF_B-3F_N-4F_B+1}{3\sqrt{2}}\ket{0}+\dfrac{6F_NF_B-3F_N-2F_B+2}{3\sqrt{2}}\ket{1}\right)\left(a\ket{0}+b\ket{1}\right)
\end{align}$$
This is agnostic to Alice's measurements, so all that's left is Bob reading the state:
$$\begin{align}
\bra{0}\left(\bra{0}S_1\right)&\to\dfrac{2F_B+1}{3\sqrt{2}}F_N\\
\bra{1}\left(\bra{0}S_1\right)&\to\dfrac{2F_B+1}{3\sqrt{2}}(1-F_N)\\
\bra{0}\left(\bra{1}S_1\right)&\to-\dfrac{6F_NF_B-3F_N-4F_B+1}{3\sqrt{2}}\\
\bra{1}\left(\bra{1}S_1\right)&\to\dfrac{6F_NF_B-3F_N-2F_B+2}{3\sqrt{2}}
\end{align}$$
If no procedure was done, we would have that:
$$\begin{align}
\bra{0}\rho_N\ket{\psi}&=aF_N+b(1-F_N)\\
\bra{1}\rho_N\ket{\psi}&=a(1-F_N)+bF_N
\end{align}$$
We want a fidelity $F_B$ so that the probability is better for all states:
$$\begin{align}
\dfrac{2F_B+1}{3\sqrt{2}}F_N &\ge aF_N+b(1-F_N)\\
\dfrac{2F_B+1}{3\sqrt{2}}(1-F_N) &\ge a(1-F_N)+bF_N\\
\dfrac{6F_NF_B-3F_N-4F_B+1}{3\sqrt{2}} &\ge aF_N+b(1-F_N)\\
F_B&\ge \dfrac{3\sqrt{2}a+3(1+\sqrt{2}b-\sqrt{2}a)F_N-2}{2(3F_N-1)}
\end{align}$$









We are about to transmit this state, so we separate to:
$$\begin{align}
\ket{\psi}\rho_B\ket{\phi^+}&\to\ket{0}\left(a\dfrac{2F_B+1}{3\sqrt{2}}\ket{00}+a\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{01}+b\dfrac{2F_B+1}{3\sqrt{2}}\ket{10}+b\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{11}\right)\\
&+\dfrac{4F_B-1}{3\sqrt{2}}\ket{1}\left(a\ket{0}+b\ket{1}\right)\ket{{1}}
\end{align}$$
Post transmission, the state is:
$$\begin{align}
S&\to\left(F_N\ket{0}+(1-F_N)\ket{1}\right)\left(a\dfrac{2F_B+1}{3\sqrt{2}}\ket{00}+a\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{01}+b\dfrac{2F_B+1}{3\sqrt{2}}\ket{10}+b\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{11}\right)\\
&+\dfrac{4F_B-1}{3\sqrt{2}}\left(F_N\ket{1}+(1-F_N)\ket{0}\right)\left(a\ket{0}+b\ket{1}\right)\ket{{1}}
\end{align}$$













Suppose the following transitions for channels:
$$\begin{align}
\rho_N\ket{\psi}&=F_N\ket{\psi}+(1-F_N)\ket{\neg\psi}
\end{align}$$
For a singular bell state from the dedicated channel has a similar form:
$$\begin{align}
\rho_B\ket{\phi^+}&=F_B\ket{\phi^+}+(1-F_B)\dfrac{\ket{\phi^-}+\ket{\psi^+}+\ket{\psi^-}}{3}
\end{align}$$

As a first example, suppose we have a singular qubit state and a Bell state:
$$\begin{align}
\ket{\psi}\rho_B\ket{\phi^+}&=aF_B\ket{0}\ket{\phi^+}+a(1-F_B)\ket{0}\dfrac{\ket{\phi^-}+\ket{\psi^+}+\ket{\psi^-}}{3}+bF_B\ket{1}\ket{\phi^+}+b(1-F_B)\ket{1}\dfrac{\ket{\phi^-}+\ket{\psi^+}+\ket{\psi^-}}{3}
\end{align}$$
We want to see what the exchange of our data bit with the first Bell state bit does:
$$\begin{align}
\ket{0}\ket{\phi^+}&\to\ket{0}\dfrac{\ket{00}}{\sqrt{2}}+\ket{1}\dfrac{\ket{01}}{\sqrt{2}} & \ket{0}\ket{\phi^-}&\to\ket{0}\dfrac{\ket{00}}{\sqrt{2}}-\ket{1}\dfrac{\ket{01}}{\sqrt{2}} \\
\ket{0}\ket{\psi^+}&\to\ket{0}\dfrac{\ket{01}}{\sqrt{2}}+\ket{1}\dfrac{\ket{00}}{\sqrt{2}} & \ket{0}\ket{\psi^-}&\to\ket{0}\dfrac{\ket{01}}{\sqrt{2}}-\ket{1}\dfrac{\ket{00}}{\sqrt{2}} \\\\
\ket{1}\ket{\phi^+}&\to\ket{0}\dfrac{\ket{10}}{\sqrt{2}}+\ket{1}\dfrac{\ket{11}}{\sqrt{2}} & \ket{1}\ket{\phi^-}&\to\ket{0}\dfrac{\ket{10}}{\sqrt{2}}-\ket{1}\dfrac{\ket{11}}{\sqrt{2}} \\
\ket{1}\ket{\psi^+}&\to\ket{0}\dfrac{\ket{11}}{\sqrt{2}}+\ket{1}\dfrac{\ket{10}}{\sqrt{2}} & \ket{1}\ket{\psi^-}&\to\ket{0}\dfrac{\ket{11}}{\sqrt{2}}-\ket{1}\dfrac{\ket{10}}{\sqrt{2}}
\end{align}$$
Expanding, we get:
$$\begin{align}
\ket{\psi}\rho_B\ket{\phi^+}&=aF_B\left(\ket{0}\dfrac{\ket{00}}{\sqrt{2}}+\ket{1}\dfrac{\ket{01}}{\sqrt{2}}\right)+\dfrac{a(1-F_B)}{3}\left(\ket{0}\dfrac{\ket{00}}{\sqrt{2}}-\ket{1}\dfrac{\ket{01}}{\sqrt{2}}+2\ket{0}\dfrac{\ket{01}}{\sqrt{2}}\right)\\
&+bF_B\left(\ket{0}\dfrac{\ket{10}}{\sqrt{2}}+\ket{1}\dfrac{\ket{11}}{\sqrt{2}}\right)+\dfrac{b(1-F_B)}{3}\left(\ket{0}\dfrac{\ket{10}}{\sqrt{2}}-\ket{1}\dfrac{\ket{11}}{\sqrt{2}}+2\ket{0}\dfrac{\ket{11}}{\sqrt{2}}\right)
\end{align}$$
Rearrange:
$$\begin{align}
S_1=\ket{\psi}\rho_B\ket{\phi^+}&=\dfrac{2F_B+1}{3\sqrt{2}}\ket{0}\left(a\ket{00}+b\ket{10}\right)\\
&+\dfrac{2(1-F_B)}{3\sqrt{2}}\ket{0}\left(a\ket{01}+b\ket{11}\right)\\
&+\dfrac{(4F_B-1)}{3\sqrt{2}}\ket{1}\left(a\ket{01}+b\ket{11}\right)
\end{align}$$
Now we send the first qubit through the noisy channel, so:
$$\begin{align}
S_1=\ket{\psi}\rho_B\ket{\phi^+}&=\dfrac{2F_B+1}{3\sqrt{2}}F_N\ket{0}\left(a\ket{00}+b\ket{10}\right)+\dfrac{2F_B+1}{3\sqrt{2}}(1-F_N)\ket{1}\left(a\ket{00}+b\ket{10}\right)\\
&+\dfrac{2(1-F_B)}{3\sqrt{2}}F_N\ket{0}\left(a\ket{01}+b\ket{11}\right)+\dfrac{2(1-F_B)}{3\sqrt{2}}(1-F_N)\ket{0}\left(a\ket{01}+b\ket{11}\right)\\
&+\dfrac{(4F_B-1)}{3\sqrt{2}}F_N\ket{1}\left(a\ket{01}+b\ket{11}\right)+\dfrac{(4F_B-1)}{3\sqrt{2}}(1-F_N)\ket{1}\left(a\ket{01}+b\ket{11}\right)
\end{align}$$
Now if Alice measures her entangled qubit from the Bell state (qubit 2), we get the following:
$$\begin{align}
\bra{0}S_1&\propto a(2F_B+1)\left[F_N\ket{0}+(1-F_N)\ket{1}\right]\ket{0}\\
&\ \ \ \ +a\left[2(1-F_B)\ket{0}+(4F_B-1)\ket{1}\right]\ket{1}
\end{align}$$
$$\begin{align}
\bra{1}S_1&\propto b(2F_B+1)\left[F_N\ket{0}+(1-F_N)\ket{1}\right]\ket{0}\\
&\ \ \ \ +b\left[2(1-F_B)\ket{0}+(4F_B-1)\ket{1}\right]\ket{1}
\end{align}$$
The result on Bob's side is identical regardless of what she measures. Bob now measures his entangled qubit 








$$\begin{align}
S_2&=\dfrac{F_N}{\sqrt{2}}\ket{0}\left(\dfrac{2F_B+1}{3}a\ket{00}+\dfrac{2(1-F_B)}{3}a\ket{01}+\dfrac{2(1-F_B)}{3}b\ket{11}+\dfrac{2F_B+1}{3}b\ket{10}\right)\\
&+\dfrac{1-F_N}{\sqrt{2}}\ket{1}\left(\dfrac{2F_B+1}{3}a\ket{00}+\dfrac{2(1-F_B)}{3}a\ket{01}+\dfrac{2(1-F_B)}{3}b\ket{11}+\dfrac{2F_B+1}{3}b\ket{10}\right)\\
&+\dfrac{(4F_B-1)F_N}{3\sqrt{2}}\ket{1}\left(a\ket{01}+b\ket{11}\right)+\dfrac{(4F_B-1)(1-F_N)}{3\sqrt{2}}\ket{0}\left(a\ket{01}+b\ket{11}\right)
\end{align}$$






Bob receives the new state, and then measures his side of the bell state (qubit 3), and sees either:
$$\begin{align}
\bra{0}S_2&=\dfrac{2F_B+1}{3\sqrt{2}}\left[F_N\ket{0}+(1-F_N)\ket{1}\right]\left(a\ket{0}+b\ket{1}\right)\\
\bra{1}S_2&=\left[\dfrac{3F_N+4F_B-6F_NF_B-1}{3\sqrt{2}}\ket{0}-\dfrac{3F_N+2F_B-6F_BF_N-2}{3\sqrt{2}}\ket{1}\right]\left(a\ket{0}+b\ket{1}\right)\\
\end{align}$$
Ignoring normalization for obvious reasons, we see that 











We want to transmit our quantum state of the following form:
$$\begin{align}
\ket{\psi}&=a\ket{0}+b\ket{1}
\end{align}$$
However, the transmission is noisy, and has the following effects:
$$\begin{align}
\ket{0}&=F_0\ket{0}+(1-F_0)\ket{1}\\
\ket{1}&=F_1\ket{1}+(1-F_1)\ket{0}\\
\end{align}$$
We want a new encoding scheme that has 2 states and collapses to 1 state:
$$\begin{align}
\ket{\psi}\ket{\phi^+}&=a\ket{0}\dfrac{\ket{00}+\ket{11}}{\sqrt{2}}+b\ket{1}\dfrac{\ket{00}+\ket{11}}{\sqrt{2}}
\end{align}$$
Impose a swapping condition (locally) where 1st bit and second bit get swapped:
$$\begin{align}
S=\ket{\psi}\ket{\phi^+}&=\dfrac{a}{\sqrt{2}}\ket{0}\ket{00}+\dfrac{a}{\sqrt{2}}\ket{0}\ket{11}+\dfrac{b}{\sqrt{2}}\ket{1}\ket{00}+\dfrac{b}{\sqrt{2}}\ket{1}\ket{11}\\
S'&\to \dfrac{a}{\sqrt{2}}\ket{0}\ket{00}+\dfrac{a}{\sqrt{2}}\ket{1}\ket{01}+\dfrac{b}{\sqrt{2}}\ket{0}\ket{10}+\dfrac{b}{\sqrt{2}}\ket{1}\ket{11}\\
&=\ket{0}\dfrac{a\ket{00}+b\ket{10}}{\sqrt{2}}+\ket{1}\dfrac{a\ket{01}+b\ket{11}}{\sqrt{2}}\\
\end{align}$$

























If we allow the interaction of the Bell state to occur before the transmission
$$\begin{align}
\ket{\phi^+}_N\rho_B\ket{\phi^+}_B&=F_B\ket{\phi^+}_N\ket{\phi^+}_B+(1-F_B)\ket{\phi^+}_N\dfrac{\ket{\phi^-}_B+\ket{\psi^+}_B+\ket{\psi^-}_B}{3}
\end{align}$$
Now we transmit the noisy channel state:
$$\begin{align}
(\rho_N\otimes\mathbb{I})\left(\ket{\phi^+}_N\rho_B\ket{\phi^+}_B\right)&=F_BF_N\ket{\phi^+}_N\ket{\phi^+}_B+(1-F_B)F_N\ket{\phi^+}_N\dfrac{\ket{\phi^-}_B+\ket{\psi^+}_B+\ket{\psi^-}_B}{3}\\
&+F_B(1-F_N)\dfrac{\ket{\phi^-}_N+\ket{\psi^+}_N+\ket{\psi^-}_N}{3}\ket{\phi^+}_B+(1-F_B)(1-F_N)\dfrac{\ket{\phi^-}_N+\ket{\psi^+}_N+\ket{\psi^-}_N}{3}\dfrac{\ket{\phi^-}_B+\ket{\psi^+}_B+\ket{\psi^-}_B}{3}
\end{align}$$
If we measure the Bell State first after receiving the message:
$$\begin{align}
\braket{\phi^+_B\lvert \psi}&=F_BF_N\ket{\phi^+}_N+F_B(1-F_N)\dfrac{\ket{\phi^-}_N+\ket{\psi^+}_N+\ket{\psi^-}_N}{3}\\
\braket{\neg\phi^+\lvert \psi}&=
\end{align}$$

