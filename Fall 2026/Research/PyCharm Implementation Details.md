

## Hamiltonian Datatypes

### Model Types
We want to have a comprehensive list of Hamiltonians we would potentially want in our experimentation and messing around. The most obvious way is to list every permutation, but that will lead to a lot of duplication under Unitary Equivalence.
#### The 1D Local Models
Ignoring cross-cartesian interactions, there are only 6 couplings needed to describe up to 2nd order interactions between sites. These are
$$\begin{align}
\hat{H}&=-\sum_{\left<i,j\right>}\left(J_{ij}^x\sigma_i^x\sigma_j^x+J_{ij}^y\sigma_i^y\sigma_j^y+J_{ij}^z\sigma_i^z\sigma_j^z\right)-\sum_i\left(h_i^x\sigma_i^x+h_i^y\sigma_i^y+h_i^z\sigma_i^z\right)
\end{align}$$
If we impose spatial translation invariance (homogenous chain), as well fixing our global rotation gauge to have all interactions occur within the $xz$ plane, then we get the Hamiltonian
$$\begin{align}
\hat{H}&=
\underbrace{-j\sum_{\left<a,b\right>}\sigma_a^z\sigma_b^z}_{\substack{\text{Classical Order} \\ \text{Ising Coupling}}}
\ \underbrace{-h^x\sum_i\sigma_i^x}_{\substack{\text{Local Quantum} \\ \text{Fluctuation}}}
\ \underbrace{-f\sum_{\left<a,b\right>}\sigma_a^x\sigma_b^x}_{\substack{\text{Interdependent} \\ \text{Fluctuation Coupling}}}
\ \underbrace{-h^z\sum_i\sigma_i^z}_{\substack{\text{Symmetry-Breaking} \\ \text{Longitudinal Field}}}
\end{align}$$
In terms of our paper, these can be written instead with the labels
$$\begin{align}
\hat{H}&=
\underbrace{-j\sum_{\left<a,b\right>}\sigma_a^z\sigma_b^z}_{\substack{\text{Bistable Memory} \\ \text{Energy Wells}}}
\ \underbrace{-h^x\sum_i\sigma_i^x}_{\substack{\text{Transverse} \\ \text{Tunneling} \\ \text{Inducer}}}
\ \underbrace{-f\sum_{\left<a,b\right>}\sigma_a^x\sigma_b^x}_{\substack{\text{Non-Local} \\ \text{Cascading Feedback}}}
\ \underbrace{-h^z\sum_i\sigma_i^z}_{\substack{\text{Hysteresis Bias} \\ \text{Sweep Parameter}}}
\end{align}$$
In code, I'll then implement the following Hamiltonians:
$$\begin{align}
\hat{H}_\text{TFIM}&=-j\sum_{\left<a,b\right>}\sigma_a^z\sigma_b^z-h^x\sum_i\sigma_i^x\\
\hat{H}_\text{LTFIM}&=-j\sum_{\left<a,b\right>}\sigma_a^z\sigma_b^z-h^x\sum_i\sigma_i^x-h^z\sum_i\sigma_i^z\\
\hat{H}_\text{QH, Local}&=-j\sum_{\left<a,b\right>}\sigma_a^z\sigma_b^z-h^x\sum_i\sigma_i^x-f\sum_{\left<a,b\right>}\sigma_a^x\sigma_b^x\\
\hat{H}_\text{QH, Global}&=-j\sum_{\left<a,b\right>}\sigma_a^z\sigma_b^z-h^x\sum_i\sigma_i^x-f\sum_{a\ne b}\sigma_a^x\sigma_b^x\\
\hat{H}_\text{EQH, Local}&=-j\sum_{\left<a,b\right>}\sigma_a^z\sigma_b^z-h^x\sum_i\sigma_i^x-f\sum_{\left<a,b\right>}\sigma_a^x\sigma_b^x-h^z\sum_i\sigma_i^z\\
\hat{H}_\text{EQH, Global}&=-j\sum_{\left<a,b\right>}\sigma_a^z\sigma_b^z-h^x\sum_i\sigma_i^x-f\sum_{a\ne b}\sigma_a^x\sigma_b^x-h^z\sum_i\sigma_i^z\\
\end{align}$$
Our investigation is on $\hat{H}_\text{QH, Global}$, but the others could be helpful for modeling what we already expect, as well as for phenomena that might be missing.





