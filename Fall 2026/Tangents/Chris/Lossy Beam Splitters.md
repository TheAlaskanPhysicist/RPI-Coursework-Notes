

The question we're effectively trying to answer is if we have a lossy beam-splitter, what inputs must we use such that the output beam-splitter is equivalent to a lossless beam-splitter.




## Single-Photon Case
The general transition matrix equation is
$$\begin{align}
\left[\begin{array}{}
a_{1,0\to1,0}&a_{0,1\to1,0}&a_{0,0\to1,0}\\
a_{1,0\to0,1}&a_{0,1\to0,1}&a_{0,0\to0,1}\\
a_{1,0\to0,0}&a_{0,1\to0,0}&a_{0,0\to0,0}\\
\end{array}\right]
\left[\begin{array}{}a\ket{10}\\b\ket{01}\\c\ket{00}\end{array}\right]
&=\left[\begin{array}{}a'\ket{10}\\b'\ket{01}\\c'\ket{00}\end{array}\right]
\end{align}$$
Assuming that photons cannot be created out of nowhere, then the ideal BS is
$$\begin{align}
\left[\begin{array}{}
a_{1,0\to1,0}&a_{0,1\to1,0}&0\\
a_{1,0\to0,1}&a_{0,1\to0,1}&0\\
a_{1,0\to0,0}&a_{0,1\to0,0}&1\\
\end{array}\right]
\left[\begin{array}{}a\ket{10}\\b\ket{01}\\c\ket{00}\end{array}\right]
&=\left[\begin{array}{}a'\ket{10}\\b'\ket{01}\\0\end{array}\right]
\end{align}$$
If we apply the inverse matrix to both sides, we get that
$$\begin{align}
\left[\begin{array}{}a\ket{10}\\b\ket{01}\\c\ket{00}\end{array}\right]
&\propto\left[\begin{array}{}
a'a_{0,1\to0,1}-b'a_{0,1\to1,0}\\
-a'a_{1,0\to0,1}+b'a_{1,0\to1,0}\\
(a_{1,0\to0,1}a_{0,1\to0,0}-a_{1,0\to0,0}a_{0,1\to0,1})a'+(a_{1,0\to0,0}a_{0,1\to1,0}-a_{1,0\to1,0}a_{0,1\to0,0})b'
\end{array}\right]
\end{align}$$
Assuming that the transition amplitude between $\ket{10}$ and $\ket{01}$ is identical, as well as their transitions to the $\ket{00}$ state being identical, we can assign the variables
$$\begin{align}
t&=a_{0,1\to0,1}=a_{1,0\to1,0} &&\text{Transmit}\\
r&=a_{0,1\to1,0}=a_{1,0\to0.1} &&\text{Reflect}\\
p&=a_{0,1\to0,0}=a_{0,0\to0.1} &&\text{Absorption}
\end{align}$$
so that our matrix becomes
$$\begin{align}
\left[\begin{array}{}a\ket{10}\\b\ket{01}\\c\ket{00}\end{array}\right]
&=\dfrac{1}{t^2-r^2}\left[\begin{array}{}
a't-b'r\\
b't-a'r\\
p(r-t)(a'+b')
\end{array}\right]=
\dfrac{1}{t^2-r^2}\left[\begin{array}{}
t&-r\\
-r&t\\
p(r-t)&p(r-t)
\end{array}\right]
\left[\begin{array}{}a'\\b'\end{array}\right]
\end{align}$$
















Suppose we have an input state $\ket{a,b}$, a lossy beam-splitter $T$, the lossless ideal beam-splitter $T_0$, where the beam-splitters have the effect
$$\begin{align}
T\ket{a^{(N)},b^{(N)}}&=\sum_{n=0}^{N}\sum_{j=0}^n C_{n-j,j}^{(N)}\ket{n-j,j} &&&
C_{n-j,j}^{(N)}&=\bra{n-j,j}T\ket{a^{(N)},b^{(N)}}
\end{align}$$
Where the relationship between the lossy and lossless beam-splitter is
$$\begin{align}
T\ket{a^{(N)},b^{(N)}}&=T_0\ket{a^{(N)},b^{(N)}}+\sum_{n=0}^{N-1}\sum_{j=0}^n C_{n-j,j}^{(N)}\ket{n-j,j} &&&
T\ket{a^{(0)},b^{(0)}}&=T_0\ket{a^{(N)},b^{(N)}}
\end{align}$$
Now suppose we have an input state
$$\begin{align}
\ket{\text{in}}&=\sum_{N=0}^{\mathcal{N}}\alpha_N\ket{a^{(N)},b^{(N)}}
&\text{such that}&&
\sum_{N=0}^{\mathcal{N}}|\alpha_N|^2&=1
\end{align}$$
We can then apply the lossy beam-splitter $T$ to this input state, giving us
$$\begin{align}
T\ket{\text{in}}&=\sum_{N=0}^{\mathcal{N}}\alpha_NT\ket{a^{(N)},b^{(N)}}
\end{align}$$
Expanding our summation using the relationship between $T$ and $T_0$, we get that
$$\begin{align}
T\ket{\text{in}}&=T_0\sum_{N=0}^{\mathcal{N}}\alpha_N\ket{a^{(N)},b^{(N)}}+\sum_{N=1}^{\mathcal{N}}\alpha_N\sum_{n=0}^{N-1}\sum_{j=0}^n C_{n-j,j}^{(N)}\ket{n-j,j}
\end{align}$$
Another thing of note is that if we use the relationship
$$\begin{align}
T\ket{a^{(N-k)},b^{(N-k)}}&=T_0\ket{a^{(N-k)},b^{(N-k)}}+\sum_{n=0}^{N-k-1}\sum_{j=0}^n C_{n-j,j}^{(N-k)}\ket{n-j,j}
\end{align}$$



### Example
Let us do this system for $N=3$. We start with the input state
$$\begin{align}
\ket{\text{in}}&=\alpha_3\ket{a^{(3)},b^{(3)}}+\alpha_2\ket{a^{(2)},b^{(2)}}+\alpha_1\ket{a^{(1)},b^{(1)}}+\alpha_0\ket{a^{(0)},b^{(0)}}
\end{align}$$
Apply the $T$ operator to the first state in the sequence
$$\begin{align}
\alpha_3T\ket{a^{(3)},b^{(3)}}&=\alpha_3T_0\ket{a^{(3)},b^{(3)}}+\alpha_3\sum_{j=0}^2 C_{2-j,j}^{(3)}\ket{2-j,j}+\alpha_3\sum_{j=0}^1 C_{1-j,j}^{(3)}\ket{1-j,j}+\alpha_3C_{0,0}^{(3)}\ket{0,0}
\end{align}$$
Consider now the second state in the sequence
$$\begin{align}
\alpha_2T\ket{a^{(2)},b^{(2)}}&=\alpha_2\sum_{j=0}^2 C_{2-j,j}^{(2)}\ket{2-j,j}+\alpha_2\sum_{n=0}^{1}\sum_{j=0}^n C_{n-j,j}^{(2)}\ket{n-j,j}
\end{align}$$
So have these contributions from the beam-splitter cancel, we can impose
$$\begin{align}
0&=\bra{2-j,j}T\left(\alpha_3\ket{a^{(3)},b^{(3)}}+\alpha_2\ket{a^{(2)},b^{(2)}}\right)\\
(3,2)&=\alpha_3T_0\ket{a^{(3)},b^{(3)}}+\sum_{j=0}^1 \left(\alpha_3C_{1-j,j}^{(3)}+\alpha_2C_{1-j,j}^{(2)}\right)\ket{1-j,j}+\left(\alpha_3C_{0,0}^{(3)}+\alpha_2C_{0,0}^{(2)}\right)\ket{0,0}\\
\end{align}$$
Consider now the third state in the sequence
$$\begin{align}
\alpha_1T\ket{a^{(1)},b^{(1)}}&=\alpha_1\sum_{j=0}^1 C_{1-j,j}^{(1)}\ket{1-j,j}+\alpha_1C_{0,0}^{(1)}\ket{0,0}
\end{align}$$
To have these components cancel, we impose
$$\begin{align}
0&=\bra{1-j,j}T\left(\alpha_3\ket{a^{(3)},b^{(3)}}+\alpha_2\ket{a^{(2)},b^{(2)}}+\alpha_1\ket{a^{(1)},b^{(1)}}\right)\\
(3,2,1)&=\alpha_3T_0\ket{a^{(3)},b^{(3)}}+\left(\alpha_3C_{0,0}^{(3)}+\alpha_2C_{0,0}^{(2)}+\alpha_1C_{0,0}^{(1)}\right)\ket{0,0}
\end{align}$$
Lastly we add in the fourth state in the sequence, which trivially becomes
$$\begin{align}
0&=\bra{0,0}T\left(\alpha_3\ket{a^{(3)},b^{(3)}}+\alpha_2\ket{a^{(2)},b^{(2)}}+\alpha_1\ket{a^{(1)},b^{(1)}}+\alpha_0\ket{a^{(0)},b^{(0)}}\right)\\
T\ket{\text{in}}&=\alpha_3T_0\ket{a^{(3)},b^{(3)}}
\end{align}$$













This can then be expanded into
$$\begin{align}
T\ket{\text{in}}&=\alpha_0T_0\ket{a^{(0)},b^{(0)}}+\sum_{k=1}^{N}\alpha_k\left(T_0\ket{a^{(k)},b^{(k)}}+\sum_{n=0}^{N_k-1}\sum_{j=0}^n C_{n-j,j}^{(k)}\ket{n-j,j}\right)
\end{align}$$
Since we want to construct a statevector such that $T\ket{\text{in}}=T_0\ket{a,b}$, we then have
$$\begin{align}
T_0\ket{a,b}&=T_0\left(\sum_{k=0}^{N}\alpha_k\ket{a^{(k)},b^{(k)}}\right)+\sum_{k=1}^{N}\alpha_k\left(\sum_{n=0}^{k-1}\sum_{j=0}^n C_{n-j,j}^{(k)}\ket{n-j,j}\right)
\end{align}$$
For the 2nd sum, we can see that
$$\begin{align}
T\ket{a^{(k-1)},b^{(k-1)}}&=\sum_{n=0}^{k-1}\sum_{j=0}^n C_{n-j,j}^{(k-1)}\ket{n-j,j} &&&
C_{n-j,j}^{(k-1)}&=\bra{n-j,j}T\ket{a^{(k-1)},b^{(k-1)}}
\end{align}$$












This can be broken apart into the lossy and lossless components
$$\begin{align}
T\ket{\text{in}}&=\sum_{k=0}^{N}\alpha_k\left(
T_0\ket{a^{(k)},b^{(k)}}+\sum_{n=0}^{N_k-1}\sum_{j=0}^n C_{n-j,j}^{(k)}\ket{n-j,j}
\right)
\end{align}$$
We want whatever this input state is to result in $T\ket{\text{in}}=T_0\ket{a,b}=T_0\ket{a^{(0)},b^{(0)}}$, since the $0$th component is the state who has $N=a+b$ photons, while all others are lossy.
$$\begin{align}
T\ket{\text{in}}&=\alpha_0T_0\ket{a^{(0)},b^{(0)}}+
\sum_{k=1}^{N}\alpha_kT_0\ket{a^{(k)},b^{(k)}}+\sum_{k=0}^{N}\alpha_k\sum_{n=0}^{N-k-1}\sum_{j=0}^n C_{n-j,j}^{(k)}\ket{n-j,j}
\end{align}$$
Therefore, to have the result, we require that
$$\begin{align}
0&=-(1-\alpha_0)T_0\ket{a^{(0)},b^{(0)}}+
\sum_{k=1}^{N}\alpha_kT_0\ket{a^{(k)},b^{(k)}}+\sum_{k=0}^{N}\alpha_k\sum_{n=0}^{N-k-1}\sum_{j=0}^n C_{n-j,j}^{(k)}\ket{n-j,j}
\end{align}$$
The first two components are already in terms of $T_0$ as expected, but the 3rd term has components who are in terms of $T$ still, so we'll need to account for that.














For example, let's chose $N=3$, then
$$\begin{align}
T\ket{a,b}&=T_0\ket{a,b}+\sum_{m=0}^2 C_{2-m,m}\ket{2-m,m}+\sum_{m=0}^1 C_{1-m,m}\ket{1-m,m}+C_{0,0}\ket{0,0}
\end{align}$$
For $N=2$, we have that
$$\begin{align}
T\ket{a',b'}&=T_0\ket{a',b'}+\sum_{m=0}^1 C_{1-m,m}'\ket{1-m,m}+\sum_{m=0}^n C_{0,0}'\ket{0,0}
\end{align}$$
The 2nd component sum is
$$\begin{align}
T\alpha\ket{a,b}_2-T\beta\ket{a',b'}&=\sum_{m=0}^2 \left(\alpha C_{2-m,m}-\beta C_{2-m,m}'\right)-\sum_{m=0}^1 \beta C_{1-m,m}'\ket{1-m,m}-\sum_{m=0}^n \beta C_{0,0}'\ket{0,0}
\end{align}$$
Let $\alpha C_{2-m,m}-\beta C_{2-m,m}'=0$, then:
$$\begin{align}
T\alpha\ket{a,b}_2-T\beta\ket{a',b'}&=-\sum_{m=0}^1 \beta C_{1-m,m}'\ket{1-m,m}-\beta C_{0,0}'\ket{0,0}
\end{align}$$
Thus we now have a state:
$$\begin{align}
T\left(\alpha\ket{a,b}-\beta\ket{a',b'}\right)&=\alpha T_0\ket{a,b}+\sum_{m=0}^1 \left(\alpha C_{1-m,m}-\beta C_{1-m,m}'\right)\ket{1-m,m}+\left(\alpha C_{0,0}-\beta C_{0,0}'\right)\ket{0,0}
\end{align}$$
For $N=1$, we have that
$$\begin{align}
T\ket{a'',b''}&=\sum_{m=0}^1 C_{1-m,m}''\ket{1-m,m}+C_{0,0}''\ket{0,0}
\end{align}$$
The 1st component sum is
$$\begin{align}
T\gamma \left(\alpha\ket{a,b}-\beta\ket{a',b'}\right)_1-T\delta\ket{a'',b''}&=\sum_{m=0}^1 \left(\alpha\gamma C_{1-m,m}-\beta\gamma C_{1-m,m}'-\delta C_{1-m,m}''\right)\ket{1-m,m}-\delta C_{0,0}''\ket{0,0}
\end{align}$$
Let $\alpha\gamma C_{1-m,m}-\beta\gamma C_{1-m,m}'-\delta C_{1-m,m}''$, then:
$$\begin{align}
T\gamma \left(\alpha\ket{a,b}-\beta\ket{a',b'}\right)_1-T\delta\ket{a'',b''}&=-\delta C_{0,0}''\ket{0,0}
\end{align}$$
Thus we now have a state
$$\begin{align}
T\left(\alpha\gamma\ket{a,b}-\beta\gamma\ket{a',b'}-\delta\ket{a'',b''}\right)&=\alpha T_0\ket{a,b}+\left(\alpha\gamma C_{0,0}-\beta\gamma C_{0,0}'-\delta C_{0,0}''\right)\ket{0,0}
\end{align}$$
Lastly, for $N=0$:
$$\begin{align}
T\ket{a''',b'''}&=C_{0,0}'''\ket{0,0}
\end{align}$$
The 0th component sum is
$$\begin{align}
T\epsilon\left(\alpha\gamma\ket{a,b}-\beta\gamma\ket{a',b'}-\delta\ket{a'',b''}\right)_0-T\eta\ket{a''',b'''}&=\left(\alpha\gamma\epsilon C_{0,0}-\beta\gamma\epsilon C_{0,0}'-\delta\epsilon C_{0,0}''-\eta C_{0,0}'''\right)\ket{0,0}
\end{align}$$
Let $\alpha\gamma\epsilon C_{0,0}-\beta\gamma\epsilon C_{0,0}'-\delta\epsilon C_{0,0}''-\eta C_{0,0}'''=0$, then finally we have the state
$$\begin{align}
T\left(\alpha\gamma\epsilon\ket{a,b}-\beta\gamma\ket{a',b'}-\delta\ket{a'',b''}\right)&=\alpha\gamma\epsilon T_0\ket{a,b}
\end{align}$$
We can do some redefinition of each of the input parameters, let
$$\begin{align}
\alpha\gamma\epsilon&\to1 & \frac{\beta\gamma\epsilon}{\alpha}&\to\beta & \frac{\delta\epsilon}{\alpha}&\to\gamma & \frac{\eta}{\alpha}\to\delta
\end{align}$$
Therefore to construct the lossless beam-splitter on $\ket{a,b}$, we need input
$$\begin{align}
T\left(\ket{a,b}-\beta\ket{a',b'}-\gamma\ket{a'',b''}-\delta\ket{a''',b'''}\right)&=\alpha T_0\ket{a,b}
\end{align}$$
Where we have the constraints
$$\begin{align}
\bra{2-m,m}T\left(\alpha\ket{a,b}-\beta \ket{a',b'}\right)&=0
\end{align}$$
...


So we do get recursive constraints since these are all in terms of $T$, not $T_0$ (lossless).






















We can split this output state into a lossy and lossless combination
$$\begin{align}
T\ket{a,b}&=\sum_{k=0}^N C_{N-k,k}\ket{N-k,k}+\sum_{n=0}^{N-1}\sum_{m=0}^n C_{n-m,m}\ket{n-m,n}
\end{align}$$
Suppose then we have a state $\ket{a',b'}$ where $a'+b'=N-1$ instead, then we have
$$\begin{align}
T\ket{a',b'}&=\sum_{n=0}^{N'}\sum_{m=0}^n C'_{n-m,m}\ket{n-m,n} & C_{n-m,m}'&=\bra{n-m,m}T\ket{a',b'}
\end{align}$$
The lossy component of $\alpha T\ket{a,b}$ and $\beta T\ket{a',b'}$ together are
$$\begin{align}
\sum_{n=0}^{N-1}\sum_{m=0}^n\bra{n-m,m}T\left[\alpha\ket{a,b}+\beta\ket{a',b'}\right]\ket{n-m,n}
\end{align}$$













Suppose we have an input state
$$\begin{align}
\ket{\text{in}}&=\left|\sum_{n=0}^{N}a_n\ket{n},\sum_{m=0}^{M}b_m\ket{m}\right>
=\sum_{n=0}^{N}\sum_{m=0}^{M}a_nb_m\left|n,m\right>
\end{align}$$
For some Fock state $\ket{n,m}$, the lossy beam-splitter has the effect
$$\begin{align}
T\ket{n,m}&=\sum_{i=0}^{n+m}\sum_{j=0}^i C_{i-j,j}\ket{i-j,j} & C_{i-j,j}&=\bra{i-j,j}T\ket{n,m}
\end{align}$$
Suppose we then measure the state at the transmission site of $B$, then
$$\begin{align}
\bra{a,b}T\ket{n,m}&=\begin{cases}
0&a+b>n+m\\
C_{a,b}&a+b\le n+m\\
\end{cases}
\end{align}$$
For the superposition of Fock input states, we have that
$$\begin{align}
T\ket{\text{in}}&=\sum_{n=0}^{N}\sum_{m=0}^{M}a_nb_m T\left|n,m\right>\\
&=\sum_{a,b=0}^{a+b\le N+M}\sum_{n=0}^{N}\sum_{m=0}^{M}a_nb_m \ket{a,b}\bra{a,b}T\left|n,m\right>\\
&=\sum_{a,b=0}^{a+b\le N+M}\sum_{n=0}^{N}\sum_{m=0}^{M}a_nb_m C_{a,b}\ket{a,b}
\end{align}$$
The transition amplitude of a particular state $\ket{a,b}$ is then
$$\begin{align}
\bra{a,b}T\ket{\text{in}}&=\sum_{n=0}^{N}\sum_{m=0}^{M}a_nb_m C_{a,b}\\
p(a,b)&=\sum_{n=0}^{N}\sum_{m=0}^{M}|a_n|^2|b_m|^2|C_{a,b}|^2
\end{align}$$
The probability of the output state in transmission $A$, given the photon count in $B$, is









Suppose 2 states:
$$\begin{align}
\ket{\phi_5}&=C_{5,0}\ket{5,0}+C_{4,1}\ket{4,1}+C_{3,2}\ket{3,2}+C_{2,3}\ket{2,3}+C_{1,4}\ket{1,4}+C_{0,5}\ket{0,5}\\
\ket{\phi_3}&=C_{3,0}\ket{3,0}+C_{2,1}\ket{2,1}+C_{1,2}\ket{1,2}+C_{0,3}\ket{0,3}
\end{align}$$
A superposition of these Fock states
$$\begin{align}
\alpha\ket{\phi_5}+\beta\ket{\phi_3}
&=\alpha\sum_{n=0}^5\sum_{j=0}^n C_{n-j,j}\ket{n-j,j}+\beta\sum_{n=0}^3\sum_{j=0}^n C_{n-j,j}\ket{n-j,j}\\
&=\alpha\sum_{n=4}^5\sum_{j=0}^n C_{n-j,j}\ket{n-j,j}+\alpha\sum_{n=0}^3\sum_{j=0}^n C_{n-j,j}\ket{n-j,j}+\beta\sum_{n=0}^3\sum_{j=0}^n C_{n-j,j}\ket{n-j,j}\\
\end{align}$$









Suppose an input state $N=N_A+N_B$ :
$$\begin{align}
\ket{\psi_\text{in};N}&=\ket{N_A,N_B}
\end{align}$$
The beam-splitter is a linear map between this input state and the output measurable states
$$\begin{align}
T\ket{\psi_\text{in};N}
&=\sum_{n=0}^N\sum_{j=0}^n\ket{n-j,j}\bra{n-j,j}T\ket{\psi_\text{in};N}\\
&=\sum_{n=0}^N\sum_{j=0}^n\left(\bra{n-j,j}T\ket{\psi_\text{in};N}\right)\ket{n-j,j}\\
T\ket{\psi_\text{in};N}&=\sum_{n=0}^N\sum_{j=0}^nC_{n-j,j}\ket{n-j,j}
\end{align}$$
Project this beam-splitter transformation onto a state $\bra{a,b}$, then we have that
$$\begin{align}
\bra{a,b}T\ket{\psi_\text{in};N}&=\sum_{n=0}^N\sum_{j=0}^nC_{n-j,j}\delta_{a,n-j}\delta_{bj}
\end{align}$$
The probability of finding the state in $\ket{a,b}$ configuration is
$$\begin{align}
|\bra{a,b}T\ket{\psi_\text{in};N}|^2
&=\sum_{n=0}^N\sum_{j=0}^nC_{n-j,j}\delta_{a,n-j}\delta_{bj}\cdot\sum_{n'=0}^N\sum_{j'=0}^{n'}C_{n'-j',j'}^*\delta_{a,n'-j'}\delta_{bj'}\\
&=\sum_{n=0}^N\sum_{j=0}^n\sum_{n'=0}^N\sum_{j'=0}^{n'}C_{n'-j',j'}^*C_{n-j,j}\delta_{a,n-j}\delta_{bj}\delta_{a,n'-j'}\delta_{bj'}\\
&=\sum_{n=b}^{N}\sum_{n'=b}^NC_{n'-b,b}^*C_{n-b,b}\delta_{a,n-b}\delta_{a,n'-b}\\
&=\sum_{n=0}^{N-b}\sum_{n'=0}^{N-b}C_{n',b}^*C_{n,b}\delta_{a,n}\delta_{a,n'}\\
\Aboxed{|\bra{a,b}T\ket{\psi_\text{in};N}|^2&=\left|C_{a,b}\right|^2}
\end{align}$$
The normalization requires that
$$\begin{align}
1&=\sum_{a=0}^N\sum_{b=0}^{N-a}\left|C_{a,b}\right|^2
\end{align}$$





Suppose an input state $N_A+N_B\le N$ :
$$\begin{align}
\ket{\psi_\text{in};N}&=\ket{N_A,N_B}
\end{align}$$
