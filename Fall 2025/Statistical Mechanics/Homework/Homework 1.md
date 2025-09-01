Author: Stanley Goodwin
Date: September 1st, 2025

---
### Question 1
Consider the Carnot-cycle for the *ideal gas*. Show *explicitly*, that
$$\begin{align}
\dfrac{Q_{\text{low}}}{Q_{\text{high}}}&=\dfrac{T_{\text{low}}}{T_{\text{high}}}
\end{align}$$
I.e., the efficiency of this engine, using ideal gas as the working substance, is $\eta=1-\dfrac{T_{\text{low}}}{T_{\text{high}}}$. 
**Characteristics of an Ideal Gas**
$$\begin{align}
PV&=NkT\\
U&=N\cdot\dfrac{d}{2}kT
\end{align}$$

#### The Carnot Cycle
**Isothermal Expansion ($\Delta T=0$).**
The ideal gas absorbs $Q_\text{high}$ of heat from the hot reservoir at temperature $T_\text{high}$.
The gas expands isothermally ($\Delta T=0$), doing work $W_\text{exp}$.

Since $dU=N\cdot\dfrac{d}{2}k\ dT=0$, then:
$$\begin{align}
dU&=\delta Q+\delta W=0 &\implies&& \Aboxed{\delta W&=-\delta Q}
\end{align}$$
All the heat flow into the gas should do work to remove energy from the gas.

Given an ideal gas, and that $\Delta T=0$, the equation of state reduces to:
$$\begin{align}
PV&=NkT&\implies&& \Aboxed{P&=\dfrac{NkT}{V}}
\end{align}$$
We can then write the energy lost as the gas does work as:
$$\begin{align}
W_{A\rightarrow B}
&=-\int_{V_A}^{V_B}P\ dV\\
&=-NkT_\text{high}\int_{V_A}^{V_B}\dfrac{1}{V}dV\\
\Aboxed{W_{A\rightarrow B}&=-NkT_\text{high}\ln\left(\dfrac{V_B}{V_A}\right)}
\end{align}$$

**Adiabatic Expansion ($\Delta Q=0$).**
The heat flow in this section is $0$, and so:
$$\begin{align}
dU&=\delta Q+\delta W=0+\delta W &\implies&& \Aboxed{dU&=\delta W}
\end{align}$$
We can then find the work for this section as:
$$\begin{align}
\Delta U&=N\cdot\dfrac{d}{2}k\left(T_{\text{low}}-T_{\text{high}}\right)\\
\Delta W_{B\rightarrow C}&=\Delta U\\
\Aboxed{\Delta W_{B\rightarrow C}&=-N\cdot\dfrac{d}{2}k\left(T_{\text{high}}-T_{\text{low}}\right)}
\end{align}$$

**Isothermal Compression ($\Delta T=0$).**
Similar to before, the equation of state is:
$$\begin{align}
PV&=NkT&\implies&& \Aboxed{P&=\dfrac{NkT}{V}}
\end{align}$$
As well as the energy relation:
$$\begin{align}
dU&=\delta Q+\delta W=0 &\implies&& \Aboxed{\delta W&=-\delta Q}
\end{align}$$
We can then write the energy lost as the gas does work as:
$$\begin{align}
W_{C\rightarrow D}
&=-\int_{V_A}^{V_B}P\ dV\\
&=-NkT_\text{high}\int_{V_C}^{V_D}\dfrac{1}{V}dV\\
&=-NkT_\text{high}\ln\left(\dfrac{V_D}{V_C}\right)\\
\Aboxed{W_{C\rightarrow D}&=+NkT_\text{high}\ln\left(\dfrac{V_C}{V_D}\right)}
\end{align}$$

**Adiabatic Compression ($\Delta Q=0$).**
The heat flow in this section is $0$, and so:
$$\begin{align}
dU&=\delta Q+\delta W=0+\delta W &\implies&& \Aboxed{dU&=\delta W}
\end{align}$$
We can then find the work for this section as:
$$\begin{align}
\Delta U&=N\cdot\dfrac{d}{2}k\left(T_{\text{high}}-T_{\text{low}}\right)\\
\Delta W_{D\rightarrow A}&=\Delta U\\
\Aboxed{\Delta W_{D\rightarrow A}&=N\cdot\dfrac{d}{2}k\left(T_{\text{high}}-T_{\text{low}}\right)}
\end{align}$$


#### Sum of the Process
Since the Carnot Cycle is an enclosed loop, we know that:
$$\begin{align}
\Delta U&=\Delta Q+W=0 &\implies&& \Aboxed{|W|&=Q_{\text{high}}-Q_{\text{low}}}
\end{align}$$






$$\begin{align}
W&=W_{A\rightarrow B}+W_{B\rightarrow C}+W_{C\rightarrow D}+W_{D\rightarrow A}\\
&=-NkT_\text{high}\ln\left(\dfrac{V_B}{V_A}\right)-N\cdot\dfrac{d}{2}k\left(T_{\text{high}}-T_{\text{low}}\right)\\
&+NkT_\text{high}\ln\left(\dfrac{V_C}{V_D}\right)+N\cdot\dfrac{d}{2}k\left(T_{\text{high}}-T_{\text{low}}\right)\\
&=-NkT_\text{high}\ln\left(\dfrac{V_B}{V_A}\right)+NkT_\text{high}\ln\left(\dfrac{V_C}{V_D}\right)\\
\end{align}$$











$$\begin{align}
\eta&=\dfrac{W}{Q_\text{high}}
\end{align}$$





Using the expression for Internal Energy, we start with:
$$\begin{align}
dU&=T\ dS-P\ dV
\end{align}$$










(This, of course, just provides an example for Carnot’s principle, that is, all reversible engines operating between the same pair of temperatures have the above optimal efficiency)

**Hint:** Based on the equation of state (EOS), the expression for the internal energy, and the definition of work, find explicitly the heat transferred during the isothermal segments of the cycle, $Q_\text{high}$ and $Q_\text{low}$.

---
### Question 2
Using the equation of state and the expression for the internal energy, find the entropy of the van der Waals gas, $S(E,V)$. **Note:** the number of particles $N$ is fixed.

**Hint:** you may first try to obtain $S(T,V)$ and then using again the expression for the internal energy for the van der Waals gas, obtain $S(T,V)$.

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