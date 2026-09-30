# PHY.8 - Infer Macroscopic Physical Behavior from Microscopic Alternatives: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.8:5 - Archetypal Grounding {#archetypal-grounding}

### PHY.8:5.1 - Predict an excited population from a reservoir argument {#predict-an-excited-population-from-a-reservoir-argument}

A device contains N=400 distinguishable, weakly interacting units. Each has a nondegenerate ground state of energy 0 and a nondegenerate excited state of energy Delta. The units have equilibrated with a large reservoir at temperature T. Treat interactions between units and their contribution to the reservoir's temperature change as negligible. An ideal readout counts excited units before appreciable relaxation changes that count.

The physical question is the mean count and its variation between independently repeated equilibrium preparations. The reservoir argument weights a unit's state by the number of compatible reservoir states. With reservoir entropy S_R and Boltzmann constant k_B,

`Omega_R(E-Delta)/Omega_R(E) approximately exp(-Delta/(k_B T))`,

using the first-order entropy change and `dS_R/dE=1/T`. This approximation needs the reservoir's temperature to remain effectively constant over the exchanged energies. The equal weighting used for the combined equilibrium energy shell is a premise of this construction.

Choose `Delta=k_B T ln(3)`. The excited-to-ground weight ratio is 1/3, so the excited probability is p=1/4, not 1/2. Two possible energy values do not receive equal weights under this preparation.

Under the stated independence approximation, the count K is binomial:

`P(K=k) = choose(400,k) (1/4)^k (3/4)^(400-k)`.

It has mean 100 and variance 75, giving a standard deviation about 8.66 units. If the receiving requirement is that the count differs from 100 by less than 50 in at least 96% of preparations, Chebyshev gives `P(|K-100|>=50)<=75/2500=0.03`. That bound already satisfies the requirement; calculating every binomial probability is unnecessary for this decision.

Now suppose the excited energy has three distinguishable states at the same Delta, with the same equilibrium and independence premises. Their total weight is three times larger. The excited probability becomes 1/2, the mean count 200 and the variance 100. The energy gap alone no longer supplies the previous count.

If the device is instead prepared with precisely 100 excited units and isolated during readout, the count variance is zero. Individual units can still each have excited probability 1/4 across a permutation-symmetric preparation. The fixed-total restriction prevents the binomial independence assumption. Use the preparation that the work actually supplies.

### PHY.8:5.2 - Recover collective fluctuations from a prepared joint state {#recover-collective-fluctuations-from-a-prepared-joint-state}

A readout measures the z component of N=100 spin-1/2 systems along one common axis. Write each normalized outcome as s_i=+1 or -1; the physical angular momentum is `(hbar/2) s_i`. The collective normalized signal is `M=sum_i s_i`.

Three ideal preparations give every individual spin equal probabilities of +1 and -1:

| Preparation during readout | Joint property used | Mean M | Variance of M |
| --- | --- | --- | --- |
| Independently prepared maximally mixed spins | Outcomes along the common axis are independent | 0 | 100 |
| Fifty independent singlet pairs | The two outcomes in every pair are opposite | 0 | 0 |
| With equal probabilities, all spins prepared up or all prepared down | Every outcome shares the same prepared sign | 0 | 10000 |

For a singlet pair, the state is `(|up down>-|down up>)/sqrt(2)`. Its ideal common-axis measurements give opposite results, so each pair contributes zero to M. For the last preparation, M itself is +100 or -100 with equal probabilities. The variance entries follow from these joint properties and from addition of independent variances in the first preparation.

A readout designed only from the individual mean would predict the same zero signal in all three cases. Their root-mean-square collective signals are 10, 0 and 100. If saturation occurs when |M| exceeds 50, the last preparation always saturates. The first has probability at most `100/50²=0.04` by the variance bound, and the ideal paired preparation never saturates.

Now retain the paired preparation but read only one spin from each pair. The sum of those fifty outcomes has variance 50, because different pairs were prepared independently. The zero-variance conclusion applied to a complete-pair sum, not to an arbitrary selected subset.

This calculation uses joint states and a stated measurement. Common-axis anticorrelation alone would also be compatible with other preparations; it does not identify the singlet uniquely. Recovering entanglement would require a different question and suitable measurements. Detector errors or correlations between pairs would change the recording law or the preparation premise.

### PHY.8:5.3 - Derive transport from persistent microscopic motion {#derive-transport-from-persistent-microscopic-motion}

Particles move on an unbounded line with speed v>0. Each reverses direction at independent Poisson events of rate alpha>0. Initially each particle is at the origin, with either direction equally likely. This is a physical stochastic model for the motion; its validity must come from the selected mechanism and regime.

Let p_+(x,t) and p_-(x,t) describe position probabilities with positive and negative velocity. The point preparation leaves probability atoms at the unreversed fronts x=+vt and x=-vt; interpret the following density equations in the distributional sense. The transition and transport laws give

`partial_t p_+ = -v partial_x p_+ - alpha p_+ + alpha p_-`,

`partial_t p_- = v partial_x p_- + alpha p_+ - alpha p_-`.

Define total density n=p_++p_- and probability current j=v(p_+-p_-). Adding and subtracting give

`partial_t n = -partial_x j`,

`partial_t j = -v² partial_x n - 2 alpha j`.

The current retains the directional persistence. Eliminating it gives

`partial_tt n + 2 alpha partial_t n = v² partial_xx n`.

For times long compared with `1/(2 alpha)` and spatial variation slow enough for the current to relax, use `j approximately -D partial_x n`, with `D=v²/(2 alpha)`. The resulting diffusion equation is an approximation with physical grounds, not a consequence of fitting a bell-shaped histogram.

The mean position stays zero. For the stated initial preparation, the mean-square displacement is

`E[x(t)²] = (v²/alpha) [t - (1-exp(-2 alpha t))/(2 alpha)]`.

With v=2 cm/s and alpha=1/s, it is about 0.03746 cm² at t=0.1 s. A diffusion calculation would give 0.4 cm², more than ten times as much. At t=20 s, the values are about 78 and 80 cm²: diffusion overestimates this observable by about 2.56% relative to the microscopic model. A 3% tolerance admits the later approximation but not the earlier one.

Changing the requested time therefore changes the needed description. Retain the density-current equations for the early response; use the diffusion reduction when its error is adequate for the requested observable. Boundary arrival probabilities would need their own comparison, since this mean-square agreement does not validate every feature of the distribution.

A simulation that flips velocity with the specified rate implements physical time. A different Markov chain designed to sample a position distribution has no such interpretation merely because its histogram agrees.

## PHY.8:6 - Bias-Annotation {#bias-annotation}

The examples emphasize finite statistics and tractable microscopic laws. Collective behavior can involve phase transitions, long-range coupling, non-equilibrium drive and quantum observables that require more specialized calculations. The reusable move is to connect preparation, weighting, dependence and the used observable; the simple example distributions are not defaults for those cases.

A macroscopic discrepancy can also arise from the recording procedure. Return through MMP.7 when the detector's selection, integration or disturbance changes what is observed.

## PHY.8:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | What fails | Repair |
| --- | --- | --- |
| Equal weights from a count of alternatives | Two energy values are treated as equally likely despite a biased preparation. | Construct the weights from the reservoir, preparation or other applicable grounds. |
| Independence from separate constituents | A common preparation or fixed total disappears from the joint account. | Form the collective law before discarding dependence. |
| Mean as a prediction of every run | An excursion-sensitive device is assessed only at the mean signal. | Compute the fluctuation or threshold consequence needed for that device. |
| Equilibrium without an available settling interval | A stationary distribution replaces the prepared transient. | Compare the relevant relaxation with the observation time. |
| Sampler steps as elapsed time | Artificial moves become a claimed physical transition law. | Separate distribution sampling from a physically calibrated evolution. |
| One successful statistic validates the whole reduction | Mean-square agreement is used to justify a boundary-arrival probability. | Compare the observable that the changed question actually consumes. |

## PHY.8:10 - Architectural Rationale {#architectural-rationale}

The physical choice of alternatives and weights comes before their mathematical aggregation. This preserves the distinction between a distribution that fits records and a mechanism-based account that can predict a changed preparation. MMP.7 supplies the observation-law construction; this pattern supplies the physical grounds that construction needs.

Fluctuations and physical time remain alongside the mean because they can change the use without changing individual statistics. Keeping those relations explicit makes the method transferable from populations and transport to sensing and physical computation.

PHY.5 decides which physical detail can be omitted. Here a statistical consequence can show that an omitted correlation or memory matters, and return that problem to the effective-description method. A complete microscopic theory is unnecessary when a physically justified restricted account already settles the question.

## PHY.8:11 - SoTA-Echoing {#sota-echoing}

[Baldovin, Gradenigo, Vulpiani and Zanghì, *On the foundations of statistical mechanics*](https://arxiv.org/abs/2411.08709), Physics Reports 1132 (2025), provides a current synthesis of equilibrium foundations. Sections 3.4-3.5 distinguish selected macroscopic observables and useful sampling from unrestricted dynamical claims; sections 5.1.3-5.1.5 connect quantum states, reduced states and equilibrium weighting. The method uses these distinctions without making one universal equilibration argument a prerequisite.

Compare the excited-count question in :5.1. A physically appropriate equilibrium ensemble gives the same count law that sufficiently repeated microscopic simulation would estimate, with less trajectory computation. Simulation is useful when interactions or preparation invalidate the simple ensemble calculation. A maximum-entropy inference from supplied constraints is another usable route when those are the available grounds; it does not alone establish a relaxation time or response to changed coupling. The different questions determine which contribution is needed.

[Corominas-Murtra, Hanel and Jizba, *Typicality, entropy and the generalization of statistical mechanics*](https://arxiv.org/abs/2409.06537) examines extensions of typicality beyond the usual independent-constituent setting. Its distinction between probability concentration and unweighted state counts supports :4.4. The present worked calculations use ordinary finite probabilities; generalized entropy is not required for their decisions. Reopen the concentration argument when the changing alternatives or dependencies defeat its current assumptions.

[Korbel and colleagues, *Quo vadis, stochastic thermodynamics?*](https://arxiv.org/abs/2604.26601), 2026, examines hidden variables, memory and limits of thermodynamic interpretation. Sections II and V matter here: a reduced stochastic description may retain memory, and observable irreversibility does not automatically determine physical dissipation. Use a physical energetic account for a heat claim. For the transport question in :5.3, the density-current account and its diffusion reduction answer the same late-time mean-square question; the current adds useful content when the early response is required. A larger microscopic simulation would cost more without improving this already solvable comparison.

The examples are explicit constructions of the method, not reports of validation of particular devices. More demanding equilibrium, quantum or driven-system questions can require specialized physical and mathematical results. Their use retains the preparation, observable and time conditions that make the result transferable.


## PHY.8:End {#end}
