### Spring 2026 - Colloquium 4
**Author:** Stanley Goodwin
**Date:** February 25th, 2026

---
**Title:** *Photonic Quantum Experiments: From Single Photons to Optical Event*
**Speaker:** *Lorenzo Procopio, Ph.D.* | Paderborn University
**Understanding:** <u>High</u>

---
> Briefly describe in words the key concepts of the talk that interested you or if you did not find the talk interesting, why it was not interesting to you.

I definitely found the Quantum Mechanics with quaternions to be the most interesting part. Quantum mechanics with certain group-theoretic objects has always been a fascination of mine.

The other part I found very interesting was encoding a superposition of unitary operations. Given that most computation in modern computers is done with a multiplexer, and that the first bits of an instruction is effectively routing to a physical implementation of an algorithm, it is definitely a important part creating a general-purpose, programmable, quantum computer.

---
> If you were the speaker what would you do differently?

I think connecting it to well-demonstrated quantum algorithms would have been helpful for explaining the purpose of the results that were presented. 

I didn't full understand his answer to my question about higher-order operator permutations and what we'd be able to determine from certain classes of unitary operations. I think going further in-depth in this part would have been an excellent addition to the presentation.


<div style="page-break-before: always;"></div>*PDF next page*

#### Abstract
In this talk, I will present a research program aimed at translating fundamental theoretical ideas—such as hypercomplex extensions of quantum theory, indefinite causal order, and quantum fields in curved spacetime—into experimentally testable photonic systems. By combining single-photon platforms, engineered metamaterials, and ultrafast nonlinear fiber dynamics, we develop controllable laboratory architectures that enable quantitative investigations of foundational questions in quantum theory and analogue gravity. This approach establishes photonics not only as a carrier of quantum information, but as a versatile platform for engineering quantum operations, causal structures, and effective spacetime geometries.


<div style="page-break-before: always;"></div>*PDF next page*

#### Notes
 - Micro-ring resonators! Dr. Howland did work with those. SPDC for entangled photons.
 - Single Photon Diffraction, Non locality from coincidence in entangled.

Quantum with Quaternions 
- Interesting because of anti-commutativity
 - Interferometer with phase shift material in different orderings to see phase shift
 - shift was demonstrated non-zero.

Negative Index Refract Materials
- Refraction then immediate mirroring from normal

Quantum Causality
 - Causal: $A|B$, $B|A$, or $A\text{ indep. }B$.
 - Bayesian Superposition, like state superposition but of causal $A\to B$ and $B\to A$
 - The quantum switch: $\ket{b}\ket{p}$, where if $b$ is $0$ we apply $U_2U_1$, and if $1$ then $U_1U_2$.
 - If $b$ is $\ket{+}$, we get a state of commutator and anticommutator states on $\ket{p}$
 - If we assert $[U_1,U_2]=0$, we expect that state to never appear.
 - Interesting, these seems like the balanced vs tautology Deusch-Jozsa Algorithm.
 - Assume it commutes or anti-commutes, then it will be certain for any size.
 - We can extend this to multi operators to $N$ unitaries with Hadamard controls
 - Combinatorics has $N!$ ways of permutation 

Optical Event Horizon
 - Can extreme non-linear optics tell us information about black holes?
 - Analogue Gravity (Field Theory, GR, and Lab. Mimic physical processes

Question to Ask
 - For N>2, is the circuit for mutual commutivity between all operators, or is there more information we can extract from the multiplexing. What if there is a language of quantum operators that may not be unitary? Like a quantum algebra for computing?
