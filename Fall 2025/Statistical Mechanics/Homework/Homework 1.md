Author: Stanley Goodwin
Date: September 1st, 2025

---
### Question 1
Consider the Carnot-cycle for the *ideal gas*. Show *explicitly*, that
$$\begin{align}
\dfrac{Q_{\text{low}}}{Q_{\text{high}}}&=\dfrac{T_{\text{low}}}{T_{\text{high}}}
\end{align}$$
I.e., the efficiency of this engine, using ideal gas as the working substance, is $\eta=1-\dfrac{T_{\text{low}}}{T_{\text{high}}}$. 

(This, of course, just provides an example for Carnot’s principle, that is, all reversible engines operating between the same pair of temperatures have the above optimal efficiency)

**Hint:** Based on the equation of state (EOS), the expression for the internal energy, and the definition of work, find explicitly the heat transferred during the isothermal segments of the cycle, $Q_\text{high}$ and $Q_\text{low}$.


**Note for Grader:** I didn't want to look up from the textbook, so I rederived it from scratch remembering it's 2 isothermal and 2 adiabatic curves that form a cycle. Hence why I did a lot more work than required, since I didn't remember which parts I needed.


#### Ideal Gas Isotherms ($\Delta T=0$)
For an idea gas, the internal energy is entirely dependent on the temperature of the gas.
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

**Hint:** you may first try to obtain $S(T,V)$ and then using again the expression for the internal energy for the van der Waals gas, obtain $S(E,V)$.

**Van der Waals Equations**
$$\begin{align}
NkT&=\left(P+a\rho^2\right)\left(V-bN\right), &\rho&=\dfrac{N}{V}\\
P&=\dfrac{NkT}{V-bN}-a\left(\dfrac{N}{V}\right)^2
\end{align}$$
**Thermodynamic Relation**
$$\begin{align}
dU&=T\ dS-P\ dV & \implies && \Aboxed{dS&=\dfrac{1}{T}dU+\dfrac{P}{T}dV}
\end{align}$$
We can substitute the pressure in with the above, and so:
$$\begin{align}
dS&=\dfrac{1}{T}dU+\dfrac{P}{T}dV\\
&=\dfrac{1}{T}dU+\dfrac{1}{T}\left(\dfrac{NkT}{V-bN}-a\left(\dfrac{N}{V}\right)^2\right)dV\\
&=\dfrac{1}{T}dU+\left(\dfrac{Nk}{V-bN}-a\dfrac{1}{T}\left(\dfrac{N}{V}\right)^2\right)dV\\
\end{align}$$






$$\begin{align}

\end{align}$$



We can do some substitutions to arrive to the entropy vs volume:
$$\begin{align}
dS&=\dfrac{1}{T}dU+\dfrac{P}{T}dV\\
\dfrac{dS}{dV}&=\dfrac{1}{T}\dfrac{d}{dV}\left(N\cdot\dfrac{\text{df}}{2}kT+\dfrac{aN^2}{V}\right)+\dfrac{1}{T}\left(kT\dfrac{\rho}{1-b\rho}+a\rho^2\right)\\
&=-\dfrac{aN^2}{T}\dfrac{1}{V^2}+k\dfrac{\rho}{1-b\rho}+\dfrac{a\rho^2}{T}\\
\Aboxed{\dfrac{dS}{dV}&=k\dfrac{\rho}{1-b\rho}}
\end{align}$$
We can then integrate from all of space into this small volume V:
$$\begin{align}
\int dS&=\int_{\infty}^VNk\dfrac{1}{V-bN}dV\\
&=\int_{\infty}^VNk\dfrac{1}{V-bN}dV\\
\end{align}$$





---
### Question 3
Determine the relationship between $T$ and $V$ for the (quasistatic) adiabatic process for the van der Waals gas. Then obtain the relationship between $P$ and $V$. Sketch $P(V)$ for the above process and also sketch $P(V)$ for the isothermal process of the van der Waals gas (on the same graph), starting at the same temperature and volume. Compare them and discuss your findings.

---
### Question 4
Prove the following important and general thermodynamic relationship:
$$\begin{align}
\left(\dfrac{\partial E}{\partial V}\right)_T=T\left(\dfrac{\partial P}{\partial T}\right)_V-P
\end{align}$$
**Note:** This relationship is independent of the specific substance. It explicitly shows that the equation of state $P(T,V)$ and the internal energy $E(T,V)$ are not independent of each other. 

**Hint:** Start with the First Law, $dE=T\ dS-P\ dV$, then use the appropriate Maxwell relationship to obtain the desired result.

---
### Question 5
The Joule process (or free expansion). Consider a gas, which expands into a vacuum from $V_1$ to $V_2$ while the system is *thermally isolated*.
#### 5.A
Show that the temperature change during this process is given by:
$$\begin{align}
\Delta T&=T_2-T_1=-\int\dfrac{{T\left(\tfrac{\partial P}{\partial T}\right)_V-P}}{C_V}\ dV
\end{align}$$
#### 5.B
Calculate the temperature change under the Joule process for the ideal gas.

#### 5.C
Calculate the temperature change under the Joule process for the van der Waal gas.