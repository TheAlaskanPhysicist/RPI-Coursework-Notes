Author: Stanley Goodwin
Date: September 14th, 2025

---
### Question 1
Consider the Carnot-cycle for the *ideal gas*. Show *explicitly*, that
$$\begin{align}
\dfrac{Q_{\text{low}}}{Q_{\text{high}}}&=\dfrac{T_{\text{low}}}{T_{\text{high}}}
\end{align}$$
I.e., the efficiency of this engine, using ideal gas as the working substance, is $\eta=1-\dfrac{T_{\text{low}}}{T_{\text{high}}}$. 

**Note for Grader:** I didn't want to look up from the textbook, so I rederived it from scratch remembering it's 2 isothermal and 2 adiabatic curves that form a cycle. Hence why I did a lot more work than required, since I didn't remember which parts I needed.

#### Ideal Gas Isotherms ($\Delta T=0$)
For an ideal gas, the internal energy is entirely dependent on the temperature of the gas.
$$\begin{align}
U=Q+W&=N\cdot\dfrac{\text{df}}{2}kT
\end{align}$$
Its differential is then:
$$\begin{align}
dU&=N\cdot\dfrac{\text{df}}{2}k\ dT=0 &\implies&&\Aboxed{dU&=0}\\
dU&=\delta U+\delta W &\implies&&\Aboxed{\delta W&=-\delta Q}
\end{align}$$
We also see its equation of state can be written as:
$$\begin{align}
PV&=NkT&\implies&& \Aboxed{P&=\dfrac{NkT}{V}}
\end{align}$$
To find its work, we can evaluate the following integral:
$$\begin{align}
W_{A\rightarrow B}
&=-\int_{V_A}^{V_B}P\ dV\\
&=-NkT\int_{V_A}^{V_B}\dfrac{1}{V}dV\\
\Aboxed{W_\text{isotherm}&=-NkT\ln\left(\dfrac{V_B}{V_A}\right)}
\end{align}$$
#### Ideal Gas Adiabats ($\Delta Q=0$)
We can write out the expression for internal energy as:
$$\begin{align}
U=Q+W
\end{align}$$
Its differential is then:
$$\begin{align}
dU&=\delta Q+\delta W=0+\delta W &\implies&&\Aboxed{dU&=\delta W}\\
\end{align}$$
The difference in internal energy is directly proportional to the difference in temperature:
$$\begin{align}
dU&=N\cdot\dfrac{\text{df}}{2}k\ dT
\end{align}$$
We can then find that the following relationship between work and internal energy:
$$\begin{align}
-P\ dV&=N\cdot\dfrac{\text{df}}{2}k\ dT&\implies&& \Aboxed{dT&=-\dfrac{\text{2}}{df}\dfrac{P}{Nk}\ dV}
\end{align}$$
From the Ideal Gas equation of state, we know that:
$$\begin{align}
PV&=NkT&\implies&& \Aboxed{dT&=\dfrac{P\ dV+V\ dP}{Nk}}
\end{align}$$
Combining from above, we see that:
$$\begin{align}
-\dfrac{\text{2}}{df}\dfrac{P}{Nk}\ dV&=\dfrac{P\ dV+V\ dP}{Nk}\\
-\dfrac{\text{2}}{df}P\ dV&=P\ dV+V\ dP\\
-\left(\dfrac{\text{2}}{df}+1\right)P\ dV&=V\ dP\\
\Aboxed{\left(\dfrac{\text{2}}{df}+1\right)\dfrac{dV}{V}+\dfrac{dP}{P}&=0}
\end{align}$$
Let the coefficient listed be equal to $\gamma$, then:
$$\begin{align}
\gamma\int\dfrac{dV}{V}+\int\dfrac{dP}{P}&=0\\
\gamma\ln|V|+\ln|P|&=A\\
e^{\gamma\ln|V|+\ln|P|}&=e^A\\
\Aboxed{V^\gamma P&=A'}\\
\end{align}$$
We can also find the temperature relationship:
$$\begin{align}
V^\gamma P&=V^{\gamma-1} PV\\
&=V^{\gamma-1} NkT\\
\text{const.}&=TV^{\gamma-1}\\
\end{align}$$
Since the change in work is the same as the change in internal energy, we find that:
$$\begin{align}
W
&=-\int_{V_A}^{V_B}P\ dV\\
&=-NkT\int_{V_A}^{V_B}\dfrac{1}{V}dV\\
\Aboxed{W_\text{adiabat}&=N\cdot\dfrac{\text{df}}{2}k\ \Delta T}
\end{align}$$

#### The Carnot Cycle
The process of a Carnot engine is as follows:
 - Isothermal Expansion ($\Delta T=0$, $V_A\rightarrow V_B$)
 - Adiabatic Expansion ($T_\text{high}\rightarrow T_\text{low}$, $V_B\rightarrow V_C$)
 - Isothermal Contraction ($\Delta T=0$, $V_C\rightarrow V_D$)
 - Adiabatic Contraction ($T_\text{low}\rightarrow T_\text{high}$, $V_D\rightarrow V_A$)

**Isothermal Expansion**:
$$\begin{align}
\Aboxed{-W_{A\rightarrow B}=Q_\text{high}&=NkT_\text{high}\ln\left(\dfrac{V_B}{V_A}\right)} & \Aboxed{P_AV_A&=P_BV_B}
\end{align}$$
**Adiabatic Expansion**:
$$\begin{align}
\Aboxed{W_{B\rightarrow C}&=-N\cdot\dfrac{\text{df}}{2}k\left(T_\text{high}-T_\text{low}\right)} & \Aboxed{T_\text{high}V_B^{\gamma-1}&=T_\text{low}V_C^{\gamma-1}}
\end{align}$$
**Isothermal Contraction**:
$$\begin{align}
\Aboxed{-W_{C\rightarrow D}&=Q_\text{low}=-NkT_\text{low}\ln\left(\dfrac{V_C}{V_D}\right)}
\end{align}$$
**Adiabatic Contraction**:
$$\begin{align}
\Aboxed{W_{D\rightarrow A}&=N\cdot\dfrac{\text{df}}{2}k\left(T_\text{high}-T_\text{low}\right)} & \Aboxed{T_\text{low}V_D^{\gamma-1}&=T_\text{high}V_A^{\gamma-1}}
\end{align}$$

#### Sum of the Process
Since the Carnot Cycle is an enclosed loop, we know that:
$$\begin{align}
\Delta U&=\Delta Q+W=0 &\implies&& \Aboxed{|W|&=Q_{\text{high}}-Q_{\text{low}}}
\end{align}$$
The efficiency is defined to be:
$$\begin{align}
\eta&\equiv\dfrac{W}{Q_\text{high}}=\dfrac{Q_{\text{high}}-|Q_{\text{low}}|}{Q_\text{high}}=1-\dfrac{|Q_{\text{low}}|}{Q_\text{high}}
\end{align}$$
From our equations above, we can find the ratio of heats as:
$$\begin{align}
\dfrac{Q_{\text{low}}}{Q_\text{high}}&=\dfrac{NkT_\text{low}\ln\left(V_C/V_D\right)}{NkT_\text{high}\ln\left(V_B/V_A\right)}\\
&=\dfrac{T_\text{low}}{T_\text{high}}\dfrac{\ln\left(V_C/V_D\right)}{\ln\left(V_B/V_A\right)}
\end{align}$$
We can use the Adiabatic expressions we obtained earlier for the logarithm part:
$$\begin{align}
T_\text{high}V_B^{\gamma-1}&=T_\text{low}V_C^{\gamma-1}\\
T_\text{low}V_D^{\gamma-1}&=T_\text{high}V_A^{\gamma-1}\\\\
\dfrac{T_\text{low}V_C^{\gamma-1}}{T_\text{low}V_D^{\gamma-1}}&=\dfrac{T_\text{high}V_B^{\gamma-1}}{T_\text{high}V_A^{\gamma-1}}\\
\left(\dfrac{V_C^{\gamma-1}}{V_D^{\gamma-1}}\right.&=\left.\dfrac{V_B^{\gamma-1}}{V_A^{\gamma-1}}\right)^{\tfrac{1}{\gamma-1}}\\\\
\Aboxed{\dfrac{V_C}{V_D}&=\dfrac{V_B}{V_A}}
\\\\
\dfrac{\ln\left(V_C/V_D\right)}{\ln\left(V_B/V_A\right)}&=\dfrac{\ln\left(V_B/V_A\right)}{\ln\left(V_B/V_A\right)}=1
\end{align}$$
Therefore, we can then see that:
$$\begin{align}
\Aboxed{\dfrac{Q_{\text{low}}}{Q_\text{high}}&=\dfrac{T_\text{low}}{T_\text{high}}}
\end{align}$$
Which also shows that:
$$\begin{align}
\eta&=1-\dfrac{|Q_{\text{low}}|}{Q_\text{high}}=1-\dfrac{T_\text{low}}{T_\text{high}}
\end{align}$$

---
### Question 2
Using the equation of state and the expression for the internal energy, find the entropy of the van der Waals gas, $S(E,V)$. **Note:** the number of particles $N$ is fixed.
#### Van der Waals Equations
$$\begin{align}
NkT&=\left(P+a\rho^2\right)\left(V-bN\right), &\rho&=\dfrac{N}{V}\\
P(T,V)&=\dfrac{NkT}{V-bN}-a\left(\dfrac{N}{V}\right)^2\\
U(T,V)&=C_V^\text{ideal}T-a\dfrac{N^2}{V}
\end{align}$$
#### Thermodynamic Relation (for constant $N$)
$$\begin{align}
dU&=T\ dS-P\ dV & \implies && \Aboxed{dS&=\dfrac{1}{T}dU+\dfrac{P}{T}dV}
\end{align}$$
Since we know that $U=U(T,V)$, we can write the differential as:
$$\begin{align}
dU&=\left(\dfrac{\partial U}{\partial T}\right)_VdT+\left(\dfrac{\partial U}{\partial V}\right)_TdV
\end{align}$$
In total, we can then write the entropy as:
$$\begin{align}
\Aboxed{dS&=\dfrac{1}{T}\left(\dfrac{\partial U}{\partial T}\right)_VdT+\left[\dfrac{1}{T}\left(\dfrac{\partial U}{\partial V}\right)_T+\dfrac{P}{T}\right]dV}
\end{align}$$
#### Solving for Entropy
We can calculate some of the partial derivatives:
$$\begin{align}
\left(\dfrac{\partial U}{\partial T}\right)_V
&=\left(\dfrac{\partial}{\partial T}\left[C_V^\text{ideal}T-a\dfrac{N^2}{V}\right]\right)_V\\
&=\left(C_V^\text{ideal}\right)_V\\
\Aboxed{\left(\dfrac{\partial U}{\partial T}\right)_V&=\left(C_V^\text{ideal}\right)_V}
\\\\
\left(\dfrac{\partial U}{\partial V}\right)_T
&=\left(\dfrac{\partial}{\partial V}\left[C_V^\text{ideal}T-a\dfrac{N^2}{V}\right]\right)_T\\
&=\left(a\dfrac{N^2}{V^2}\right)_T\\
\Aboxed{\left(\dfrac{\partial U}{\partial V}\right)_T&=a\dfrac{N^2}{V^2}}
\end{align}$$
Substituting into our entropy system, we see that:
$$\begin{align}
dS&=\dfrac{C_V^\text{ideal}}{T}dT+\left[\dfrac{a}{T}\left(\dfrac{N}{V}\right)^2+\dfrac{P}{T}\right]dV
\end{align}$$
We can now substitute the pressure, and so:
$$\begin{align}
dS&=\dfrac{C_V^\text{ideal}}{T}dT+\left[\dfrac{a}{T}\left(\dfrac{N}{V}\right)^2+\dfrac{P}{T}\right]dV\\
&=\dfrac{C_V^\text{ideal}}{T}dT+\left[\dfrac{a}{T}\left(\dfrac{N}{V}\right)^2+\dfrac{Nk}{V-bN}-\dfrac{a}{T}\left(\dfrac{N}{V}\right)^2\right]dV\\
\Aboxed{dS&=\dfrac{C_V^\text{ideal}}{T}dT+\left[\dfrac{Nk}{V-bN}\right]dV}
\end{align}$$
This is a simple differential equation, since we can integrate each with respect to their differential keeping all other values constant. We assume the lower bound is a reference temperature and volume, otherwise the units don't work out correctly (this is identical to adding a constant).
$$\begin{align}
\int dS&=\int\dfrac{C_V^\text{ideal}}{T}dT+\int\left[\dfrac{Nk}{V-bN}\right]dV\\
S&=C_V^\text{ideal}\int_{T_0}^T\dfrac{1}{T}dT+Nk\int_{V_0}^V\left[\dfrac{1}{V-bN}\right]dV\\
&=C_V^\text{ideal}\left(\ln T-\ln T_0\right)+Nk\left(\ln(V-bN)-\ln(V_0-bN)\right)\\
\Aboxed{S(T,V)&=C_V^\text{ideal}\ln\left(\dfrac{T}{T_0}\right)+Nk\ln\left(\dfrac{V-bN}{V_0-bN}\right)}
\end{align}$$
Lastly, to expand back to the original problem question:
$$\begin{align}
\Aboxed{S(T,V)&=\dfrac{\text{df}}{2}Nk\ln\left(\dfrac{T}{T_0}\right)+Nk\ln\left(\dfrac{V-bN}{V_0-bN}\right)}
\end{align}$$
Where $\text{df}$ is the number of degrees of freedom of the gas.

To find this in terms of internal energy and volume, we can find that $T$ is:
$$\begin{align}
U&=C_V^\text{ideal}T-a\dfrac{N^2}{V}&\implies&&\Aboxed{T(U,V)&=(C_V^\text{ideal})^{-1}\left(U+a\dfrac{N^2}{V}\right)}
\end{align}$$
And so the final entropy equation is:
$$\begin{align}
S(U,V)&=\dfrac{\text{df}}{2}Nk\ln\left(\dfrac{(C_V^\text{ideal})^{-1}\left(U+a\dfrac{N^2}{V}\right)}{(C_V^\text{ideal})^{-1}\left(U+a\dfrac{N^2}{V_0}\right)}\right)+Nk\ln\left(\dfrac{V-bN}{V_0-bN}\right)\\
\Aboxed{S(U,V)&=\dfrac{\text{df}}{2}Nk\ln\left(\dfrac{U+a\dfrac{N^2}{V}}{U_0+a\dfrac{N^2}{V_0}}\right)+Nk\ln\left(\dfrac{V-bN}{V_0-bN}\right)}\\
\text{Or}&\text{ with }S_0\text{ being the reference entropy:}\\
\Aboxed{S(U,V)&=\dfrac{\text{df}}{2}Nk\ln\left(U+a\dfrac{N^2}{V}\right)+Nk\ln\left(V-bN\right)+S_0}
\end{align}$$
---
### Question 3
Determine the relationship between $T$ and $V$ for the (quasistatic) adiabatic process for the van der Waals gas. Then obtain the relationship between $P$ and $V$. Sketch $P(V)$ for the above process and also sketch $P(V)$ for the isothermal process of the van der Waals gas (on the same graph), starting at the same temperature and volume. Compare them and discuss your findings.
#### Adiabatic Process (Van der Waal Gas)
Using what I got in question 1, we can see that:
$$\begin{align}
U&=Q+W&\text{and}&&\Delta Q&=0&\implies&&\Aboxed{dU&=\delta W}\\
\end{align}$$
For our system, we know the internal energy takes the form:
$$\begin{align}
U(T,V)&=C_V^\text{ideal}T-a\dfrac{N^2}{V} & \implies&&\Aboxed{dU(T,V)&=C_V^\text{ideal}dT+a\left(\dfrac{N}{V}\right)^2dV}
\end{align}$$
Equating this to the equation for work ($\delta W=-P\ dV$):
$$\begin{align}
dU(T,V)&=-P\ dV\\
C_V^\text{ideal}dT+a\left(\dfrac{N}{V}\right)^2dV&=-\dfrac{NkT}{V-bN}dV+a\left(\dfrac{N}{V}\right)^2dV\\
C_V^\text{ideal}dT&=-\dfrac{NkT}{V-bN}\\
\dfrac{dT}{T}&=-\dfrac{Nk}{C_V^\text{ideal}}\dfrac{1}{V-bN}dV\\
\int_{T_1}^{T_2}\dfrac{dT}{T}&=-\int_{V_1}^{V_2}\dfrac{Nk}{C_V^\text{ideal}}\dfrac{1}{V-bN}dV\\
\ln\left(\dfrac{T_2}{T_1}\right)&=-\dfrac{Nk}{C_V^\text{ideal}}\ln\left(\dfrac{V_2-bN}{V_1-bN}\right)\\
\ln\left(\dfrac{T_2}{T_1}\right)&=-\dfrac{Nk}{\dfrac{\text{df}}{2}Nk}\ln\left(\dfrac{V_2-bN}{V_1-bN}\right)\\
\dfrac{T_2}{T_1}&=\left(\dfrac{V_2-bN}{V_1-bN}\right)^{-\tfrac{2}{\text{df}}}\\
\left(\dfrac{T_2}{T_1}\right)^{\text{df}}&=\left(\dfrac{V_1-bN}{V_2-bN}\right)^{2}\\
\Aboxed{T_1^{\text{df}}\left(V_1-bN\right)^2&=T_2^{\text{df}}\left(V_2-bN\right)^2}\\
\Aboxed{T\left(V-bN\right)^\tfrac{2}{\text{df}}&=\text{const.}}
\end{align}$$
#### Isothermal Process (Van der Waal Gas)
Since $T$ is constant during this process, we treat it as a constant in the expression:
$$\begin{align}
P(V)&=\dfrac{NkT}{V-bN}-a\left(\dfrac{N}{V}\right)^2\\
\end{align}$$
#### Pressure vs. Volume (Adiabatic)
We can start with the van der Waals pressure relationship:
$$\begin{align}
P(T,V)&=\dfrac{NkT}{V-bN}-a\left(\dfrac{N}{V}\right)^2\\
\end{align}$$
Using our adiabatic relation, we can see that:
$$\begin{align}
T(V)&=\dfrac{\text{const.}}{\left(V-bN\right)^\tfrac{2}{\text{df}}} & \implies &&
\Aboxed{P(V)&=\dfrac{Nk\cdot\text{const.}}{\left(V-bN\right)^{\tfrac{2}{\text{df}}+1}}-a\left(\dfrac{N}{V}\right)^2}
\end{align}$$
For the sake of simplicity, we'll choose the following simplifications:
$$\begin{align}
N&=1 & k&=1 & \text{df}=3 \ \ \text{ (Monotomic Gas)}
\end{align}$$
We then have the following equations:
$$\begin{align}
\Aboxed{P_\text{adiabatic}(V)&=\dfrac{\text{const.}}{\left(V-b\right)^{\tfrac{5}{\text{3}}}}-\dfrac{a}{V^2}}\\
\Aboxed{P_\text{isotherm}(V)&=\dfrac{T_0}{V-b}-\dfrac{a}{V^2}}
\end{align}$$
#### Adiabatic vs. Isothermal Processes
Both processes start at the same Pressure-Volume point $(V_A,P_A)$, and so:
$$\begin{align}
\dfrac{\text{const.}}{\left(V_A-b\right)^{\tfrac{5}{\text{3}}}}-\dfrac{a}{V_A^2}&=\dfrac{T_0}{V_A-b}-\dfrac{a}{V_A^2}\\
\text{const.}\cdot\left(V_A-b\right)&=T_0\left(V_A-b\right)^{\tfrac{5}{\text{3}}}\\
\Aboxed{\text{const.}&=T_0\left(V_A-b\right)^{\tfrac{2}{\text{3}}}}
\end{align}$$
The associated pressure is:
$$\begin{align}
\Aboxed{P(V_A)=P_A&=\dfrac{T_0}{V_A-b}-\dfrac{a}{V_A^2}}
\end{align}$$
You can find a Desmos link [here](https://www.desmos.com/calculator/2wzjd0fsze). All of the following is describing this plot.
Here's a screenshot of it in case it doesn't work:
![[hw1q3.png]]
For changes in volume who are negative $V(t)<V_A$ (compression), the isothermal pressure is less than that of the adiabatic pressure, the same as what we see in ideal gases. The slope of the adiabatic curve is more steep.

For changes in volume who are positive $V(t)>V_A$ (expansion), the isothermal pressure is more than that of the adiabatic pressure, also the same as what we see in ideal gases. The slope of the adiabatic curve is more shallow.

When starting from the shared point, we can see that:
$$\begin{align}
P_\text{adiabatic}(V)&>P_\text{isotherm}(V) &\text{when}&& bN<V&<V_A & \text{(Compression)}\\
P_\text{adiabatic}(V)&<P_\text{isotherm}(V) &\text{when}&& V&>V_A & \text{(Expansion)}\\
\end{align}$$
These hold true for all choices for $\text{df}$, as well. Below I detail some things I noticed that aren't explicitly required by the question to answer.

#### Extra Details
Something of note is if the let the limit of $\text{df}\rightarrow\infty$, we see that:
$$\begin{align}
\lim_{\text{df}\rightarrow\infty}\text{const.}
&=\lim_{\text{df}\rightarrow\infty}T\left(V-bN\right)^\tfrac{2}{\text{df}}\\
&=T\lim_{\text{df}\rightarrow\infty}\left(V-bN\right)^\tfrac{2}{\text{df}}\\
&=T\cdot\left(V-bN\right)^0\\
\text{const.}&=T
\end{align}$$
We can then say that the Isothermal Process is the limit of an adiabatic process as the gas molecules have more and more degrees of freedom. Very interesting.

We can also then see, given the limiting behavior, that:
$$\begin{align}
P_\text{adiabatic}(V)
&\sim\dfrac{1}{\left(V-bN\right)^{\tfrac{2}{\text{df}}+1}}-\dfrac{1}{V^2}\\
P_\text{isotherm}(V)&\sim\dfrac{1}{V-b}-\dfrac{a}{V^2}
\end{align}$$
If we ignore the shared term of $-1/V^2$, we see that the graphs tend to follow the trend of:
$$\begin{align}
P_\text{adiabatic}(V)
&\sim\dfrac{1}{\left(V-bN\right)^{\tfrac{2}{\text{df}}+1}}\\
P_\text{isotherm}(V)&\sim\dfrac{1}{V-b}
\end{align}$$
That term in the exponential controls the kind of decay we see. Similar to to the previous limit:
$$\begin{align}
\lim_{\text{df}\rightarrow\infty}P_\text{adiabatic}(V)
&\sim\lim_{\text{df}\rightarrow\infty}\dfrac{1}{\left(V-bN\right)^{\tfrac{2}{\text{df}}+1}}\\
&\sim\dfrac{1}{\left(V-bN\right)^{0+1}}\\
&\sim\dfrac{1}{\left(V-bN\right)}\\
\Aboxed{\lim_{\text{df}\rightarrow\infty}P_\text{adiabatic}(V)
&\sim P_\text{isotherm}(V)}
\end{align}$$
In the limit as $V\rightarrow\infty$, both pressure curves converge to the same form of $-a/V^2$.

From inspection (specifically from asymptotes), we can see that:
$$\begin{align}
b&<\dfrac{V}{N} &\implies&& \Aboxed{\dfrac{N}{V}&<\dfrac{1}{b}}
\end{align}$$
The physical interpretation of $N/V$ is a number density (particles per unit volume).
The value of $1/b$ acts like a maximum density term of the gas. The parameter $b$ is more like the volume of a particle of gas in the system, since $bN$ turns into a volume.

---
### Question 4
Prove the following important and general thermodynamic relationship:
$$\begin{align}
\left(\dfrac{\partial E}{\partial V}\right)_T=T\left(\dfrac{\partial P}{\partial T}\right)_V-P
\end{align}$$
**Note:** This relationship is independent of the specific substance. It explicitly shows that the equation of state $P(T,V)$ and the internal energy $E(T,V)$ are not independent of each other. 

**Hint:** Start with the First Law, $dE=T\ dS-P\ dV$, then use the appropriate Maxwell relationship to obtain the desired result.

#### Thermodynamic Relation (for constant $N$)
I assume $N$ to be constant given the hint not including any mention of particle count.
$$\begin{align}
dU&=T\ dS-P\ dV
\end{align}$$
We have $E(S,V)$, but we need $E(T,V)$, so let $S=S(T,V)$:
$$\begin{align}
dS&=\left(\dfrac{\partial S}{\partial T}\right)_VdT+\left(\dfrac{\partial S}{\partial V}\right)_TdV
\end{align}$$
Then $dU$ becomes:
$$\begin{align}
dU&=T\left(\left(\dfrac{\partial S}{\partial T}\right)_VdT+\left(\dfrac{\partial S}{\partial V}\right)_TdV\right)-P\ dV\\
\Aboxed{dU&=T\left(\dfrac{\partial S}{\partial T}\right)_VdT+\left(T\left(\dfrac{\partial S}{\partial V}\right)_T-P\right)dV}
\end{align}$$
At constant temperature, we see that:
$$\begin{align}
\left(\partial U\right)_T&=\left(T\left(\dfrac{\partial S}{\partial V}\right)_T-P\right)\partial V\\
\Aboxed{\left(\dfrac{\partial U}{\partial V}\right)_T&=T\left(\dfrac{\partial S}{\partial V}\right)_T-P}
\end{align}$$
Very close, but we need a maxwell relation for the derivative multiplied with the $T$.

#### Finding the Maxwell Relation
**Internal energy:**
$$\begin{align}
dU&=T\ dS-P\ dV
\end{align}$$
Leads to:
$$\begin{align}
\left(\dfrac{\partial U}{\partial S}\right)_V&=T & \left(\dfrac{\partial U}{\partial V}\right)_S&=-P
\end{align}$$
This will not give us the right expression.

**Enthalpy:**
$$\begin{align}
dH&=T\ dS+V\ dP
\end{align}$$
Leads to:
$$\begin{align}
\left(\dfrac{\partial H}{\partial S}\right)_P&=T & \left(\dfrac{\partial H}{\partial P}\right)_S&=V
\end{align}$$
This will not give us the right expression.

**Helmholtz free energy:**
$$\begin{align}
dF&=-P\ dV-S\ dT
\end{align}$$
Leads to:
$$\begin{align}
\left(\dfrac{\partial F}{\partial V}\right)_T&=-P & \left(\dfrac{\partial F}{\partial T}\right)_V&=-S
\end{align}$$
Taking their respective alternate derivatives, we see:
$$\begin{align}
\dfrac{\partial}{\partial T}\left(\dfrac{\partial F}{\partial V}\right)_T&=-\left(\dfrac{\partial P}{\partial T}\right)_V\\
\dfrac{\partial}{\partial V}\left(\dfrac{\partial F}{\partial T}\right)_V&=-\left(\dfrac{\partial S}{\partial V}\right)_T
\end{align}$$
Finally, the right relation. We can see that:
$$\begin{align}
\left(\dfrac{\partial P}{\partial T}\right)_V&=\left(\dfrac{\partial S}{\partial V}\right)_T
\end{align}$$
Therefore, our expression we wanted to prove is thus:
$$\begin{align}
\left(\dfrac{\partial U}{\partial V}\right)_T&=T\left(\dfrac{\partial S}{\partial V}\right)_T-P & \implies\\
\Aboxed{\left(\dfrac{\partial U}{\partial V}\right)_T&=\left(\dfrac{\partial P}{\partial T}\right)_V-P}
\end{align}$$
---
### Question 5
The Joule process (or free expansion). Consider a gas, which expands into a vacuum from $V_1$ to $V_2$ while the system is *thermally isolated*.

Well, thermally isolated means no heat flow, so this is an adiabatic process ($\Delta Q=0$).
A vacuum also doesn't apply pressure, and so no work is done by the gas ($W=0$)

Using what I got in question 1, we can see that:
$$\begin{align}
U&=Q+W&\text{and}&&\Delta Q&=0&\text{and}&&W&=0\implies&&\Aboxed{dU&=0}\\
\end{align}$$
Internal energy is conserved during the Joule process.

#### 5.A
Show that the temperature change during this process is given by:
$$\begin{align}
\Delta T&=T_2-T_1=-\int\dfrac{{T\left(\tfrac{\partial P}{\partial T}\right)_V-P}}{C_V}\ dV
\end{align}$$
The internal energy is best described by $U=U(T,V)$, since we know those variables well:
$$\begin{align}
dU&=\left(\dfrac{\partial U}{\partial T}\right)_VdT+\left(\dfrac{\partial U}{\partial V}\right)_TdV
\end{align}$$
Using the definition of heat capacity at const volume and Question 4's relationship. we see:
$$\begin{align}
0&=C_V(T)\ dT+\left(T\left(\dfrac{\partial P}{\partial T}\right)_V-P\right)dV
\end{align}$$
We can then rearrange to get a relationship for $dT$:
$$\begin{align}
C_V(T)\ dT&=-\left(T\left(\dfrac{\partial P}{\partial T}\right)_V-P\right)dV\\
\Aboxed{dT&=-\dfrac{T\left(\tfrac{\partial P}{\partial T}\right)_V-P}{C_V(T)}dV}
\end{align}$$
To find our goal relation, we integrate both sides to sum all the dynamics:
$$\begin{align}
\int_{T_1}^{T_2} dT&=-\int_{V_1}^{V_2}\dfrac{T\left(\tfrac{\partial P}{\partial T}\right)_V-P}{C_V(T)}dV\\
\Aboxed{\Delta T=T_2-T_1&=-\int_{V_1}^{V_2}\dfrac{T\left(\tfrac{\partial P}{\partial T}\right)_V-P}{C_V(T)}dV}
\end{align}$$
#### 5.B
Calculate the temperature change under the Joule process for the ideal gas.

Given the equation of state:
$$\begin{align}
PV&=NkT&\implies&& P&=\dfrac{NkT}{V}
\end{align}$$
We can find the heat capacity:
$$\begin{align}
\left(\dfrac{\partial U}{\partial T}\right)_V&=C_V=\dfrac{\text{df}}{2}Nk
\end{align}$$
The differential is:
$$\begin{align}
\left(\dfrac{\partial P}{\partial T}\right)_V&=\dfrac{Nk}{V}
\end{align}$$
In total, we can then see that:
$$\begin{align}
\Delta T&=-\int_{V_1}^{V_2}\dfrac{T\left(\tfrac{\partial P}{\partial T}\right)_V-P}{C_V(T)}dV\\
&=-\int_{V_1}^{V_2}\dfrac{T\cdot\tfrac{Nk}{V}-\tfrac{NkT}{V}}{\tfrac{\text{df}}{2}Nk}dV\\
&=-\int_{V_1}^{V_2}\dfrac{0}{\tfrac{\text{df}}{2}Nk}dV\\
\Aboxed{\Delta T&=0}
\end{align}$$
#### 5.C
Calculate the temperature change under the Joule process for the van der Waal gas.

Given the equation of state:
$$\begin{align}
NkT&=\left(P+a\left(\dfrac{N}{V}\right)^2\right)\left(V-bN\right) &\implies && P&=\dfrac{NkT}{V-bN}-a\left(\dfrac{N}{V}\right)^2
\end{align}$$
We can find the heat capacity:
$$\begin{align}
\left(\dfrac{\partial U}{\partial T}\right)_V&=C_V=\dfrac{\text{df}}{2}Nk
\end{align}$$
The differential is:
$$\begin{align}
\left(\dfrac{\partial P}{\partial T}\right)_V&=\dfrac{Nk}{V-bN}
\end{align}$$
In total, we can then see that:
$$\begin{align}
\Delta T&=-\int_{V_1}^{V_2}\dfrac{T\left(\tfrac{\partial P}{\partial T}\right)_V-P}{C_V(T)}dV\\
&=-\int_{V_1}^{V_2}\dfrac{T\cdot\tfrac{Nk}{V-bN}-\tfrac{NkT}{V-bN}+a\left(\tfrac{N}{V}\right)^2}{\tfrac{\text{df}}{2}Nk}dV\\
&=-\int_{V_1}^{V_2}\dfrac{a\left(\tfrac{N}{V}\right)^2}{\tfrac{\text{df}}{2}Nk}dV\\
&=-\dfrac{2aN}{k\cdot\text{df}}\int_{V_1}^{V_2}\dfrac{1}{V^2}dV\\
\Aboxed{\Delta T&=\dfrac{2aN}{k\cdot\text{df}}\left(\dfrac{1}{V_2}-\dfrac{1}{V_1}\right)}
\end{align}$$
Alternatively, leaving heat capacity as $C_V$:
$$\begin{align}
\Aboxed{\Delta T&=\dfrac{aN^2}{C_V}\left(\dfrac{1}{V_2}-\dfrac{1}{V_1}\right)}
\end{align}$$
