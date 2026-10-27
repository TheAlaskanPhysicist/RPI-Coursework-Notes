
### Abstract
Current idea:
Simulations of interdependence in a 1D quantum Ising model.

**Verbosely:**
We explore how adding interdependence between sites modifies quantum phase transitions in a 1D quantum Ising model. Using Python/Qiskit simulations, we measure magnetization and track critical behavior as the interdependence strength varies. Our results reveal shifts in transition points and the emergence of temporal plateaus in magnetization dynamics.

### Background
Explain the following:
Quantum phase transitions (sudden change in ground state properties at zero temperature).
1D quantum Ising model (without the interdependence terms)
Interdependency: explain in plain language
 - coupling of control parameters across sites leading to cascading effects
 - non-local interactions causing emergent behavior
Simple diagram of spins showing nearest-neighbor vs interdependent coupling lines?
 - Showing physically what the interdependence Hamiltonian encodes.

What to do about theory? Cite current work by Dr. Meng?

### Observations
What I've actually done so far:
Modeled Hamiltonian with interdependence term $f_{|i-j|}$.
Ran simulations for $2\le N<13$ spins, varying magnetic field $H$ and interdependence $f_{|i-j|}$.
Measured observables: Magnetization. Energy at some point?

Perhaps a flow chart of how the process goes along:
 - Construct the Hamiltonian
 - Represent it in matrix form
And then either of the following:
 - Diagonalize and find the eigenenergy and eigenstates.
 - Choose the state of lowest energy.
 - Find the magnetization of the this state.
Or the other method:
 - Construct a time evolution operator
 - Construct an initial state
 - Evolve the state and measure its magnetization at every timestep
 - Take the time-averaged mean of the magnetization to find the equilibrium magnetization state.


Mention the use of Qiskit and Python, and why this directly works with Quantum Computers as all these operations are just quantum gates.


### Results
I'll want a 1D plot iterating over $H$ like in the typical model, but show the graph in the background for different interdependency strengths.
 - If there's very little difference, find another method to show the shift in the critical transition $H$.

A 2D plot of the surface of magnetization parametrized by $H, f_{|i-j|}$ could show more obvious shifts in behavior, especially if we use a color map for heights (like a complex function).

Might be worth to construct a table for critical values of $H$ parametrized by $f_{|i-j|}$, to show the change in this transition period.

If I can explicitly show a 2nd order phase transition followed by a 1st order phase transition, that pretty much makes the entire poster worth talking about.

"briefly interpret trends (“Higher interdependence shifts the critical field to larger values and introduces a temporal plateau in magnetization”)." or something to that effect


### Discussion
Summarize what the plots show (not what they are, but their consequences)
If possible, mention the connection to the classical analogue of this system.

Write about open questions and the next steps in this research project, to show that I'm committed to seeing this become more and more put together.


### References
Whatever paper is the original 1D quantum Ising model (easy citation required).
Dr. Meng's work of this kind currently in development or already published?
Qiskit and Python references.



















Here's what I have written for the Registration Abstract:
```
Interdependency, a concept originating in network science, describes how coupling control parameters across distant parts of a system can trigger cascading effects and novel critical phenomena.  We extend this concept into quantum physics by incorporating a non-local "interdependent" term into the one-dimensional transverse-field quantum Ising model.  This additional coupling links quantum fluctuations between distant spins rather than nearest neighbors, introducing a form of global correlation.  Preliminary simulations indicate that, with sufficient strength and range, interdependency can drive a mixed-order quantum phase transition;  these exhibit non-trivial critical exponents that align with those found in corresponding classical systems.
```
This isn't what will likely be on the poster, since that one will look a lot more like the abstract you provided