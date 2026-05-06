


## Title Slide
Modeling Interdependency-Driven Quantum Phase Transition on Hardware


### What is Interdependency?
Local changes in the structure of a graph -> Non-Local effects somewhere else
- Picture of Electrical Grid
- Interdependency causes abrupt changes instead of smooth changes


### How it has been used already
Coupled fluctuations have already been used for percolation theory and multiplex networks, and more recently in adaptive Ising models and systems of higher-order interactions.
 - These use coupled local fluctuations to create positive feedback cascading
 - These drive mixed-order phase transitions

### The Problem
The physics of mixed-order phase transitions is not determined yet. While similar to spinodal points, a explanatory model of causal physics is still missing. 
 - Given a model, how can we find a spinodal point by derivation or heuristic?
 - Spinodal systems are typically mean-field, where critical exp are independent of dimension.

Quantum phase transitions are a result of quantum fluctuation instead of thermal.

### Our Hamiltonian
We start with a transverse-field quantum Ising model Hamiltonian, and introduce a long-range coupling 



We start with a Quantum Spin Model Hamiltonian
Image of Local Coupling Here
Add in a transverse field to induce Quantum state fluctuation
Image of TFIM here
Lastly, we add in an interdependency term that couples the transverse fields at different sites non-locally.


Why?
 - This model is exactly solvable in the infinite-range-coupling limit.
 - Exhibits Spinodal points (square-root singularities observed classically)

We claim that this Quantum Interdependency model is equivalent to a Classical Disordered model


## Application to Modern Quantum Computing
This model is implementable on near-term quantum circuits
 - TODO



$$\begin{align}
\mathcal{H}&=-J\sum_{i=1}^L\sigma_i^z\sigma_{i+1}^z-h\sum_{i=1}^L\sigma_i^x-\sum_{i,j=1}^Lf_{|i-j|}\sigma_i^x\sigma_{j}^x
\end{align}$$


  



