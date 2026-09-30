# PHY.9 - Construct a Measuring Interaction for a Physical Distinction: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.9:5 - Archetypal Grounding {#archetypal-grounding}

### PHY.9:5.1 - Make mass affect the observation {#make-mass-affect-the-observation}

Two bodies fall in a sufficiently uniform gravitational field with negligible drag. The equation `m a=m g` gives a=g. Timing their fall cannot distinguish their masses in this idealization, even though gravity exerts different forces.

Choose instead a known horizontal applied force F whose generation does not depend on the unknown mass. Track the body's acceleration under that force. With other horizontal forces negligible, `m a=F` gives `m=F/a` for nonzero a. The physical change is from a force proportional to the unknown mass to an independently supplied force.

Now a constant horizontal force offset b matters during the short observation. Use two otherwise identical preparations with applied forces +F and -F. Assume the same b and the same mass in both, and measure their initial accelerations:

`m a_+=F+b`, `m a_-=-F+b`.

Subtracting gives

`m=2F/(a_+-a_-)`.

With F=6 N, a_+=4 m/s² and a_-=-2 m/s², the mass is 2 kg and b=2 N. Using only F/a_+ would give 1.5 kg. The controlled reversal made mass distinguishable from the shared force offset.

The two preparations must preserve that offset. Velocity-dependent drag need not do so after the trajectories diverge. Measuring comparable initial responses, including the changed drag law, or selecting another arrangement can repair that use. Taking more samples of two physically different offsets does not justify the shared-b subtraction.

The acceleration readout and the force reference retain their own calibration and uncertainty. A decision whose margin exceeds those effects can use the mass estimate; a tighter use returns to the consequential contribution.

### PHY.9:5.2 - Separate pressure from the probe's surface force {#separate-pressure-from-the-probe-s-surface-force}

A large liquid reservoir maintains an unknown gauge pressure p during a small probe's readout. A vertical circular capillary opens to the atmosphere. Let rho be liquid density, g gravitational acceleration, r the tube radius and h the meniscus height above the pressure reference. Assume hydrostatic equilibrium and a capillary regime in which the meniscus curvature is described by the wetting angle theta.

Hydrostatic pressure and the surface-pressure jump give

`p=rho g h - s/r`, where `s=2 gamma cos(theta)`

and gamma is surface tension. The height responds to the wanted pressure and to the capillary surface force.

If s is unknown but the same surface condition can be prepared in two narrow tubes of radii r_1 and r_2, use

`rho g h_1=p+s/r_1`, `rho g h_2=p+s/r_2`.

For distinct radii,

`p=rho g (r_1 h_1-r_2 h_2)/(r_1-r_2)`.

Take rho g=10000 Pa/m, r_1=0.1 mm, r_2=0.2 mm, h_1=0.20 m and h_2=0.15 m. The inferred pressure is 1000 Pa and s=0.10 N/m. Interpreting the first height as p=rho g h_1 would give 2000 Pa. Both narrow radii must remain within the chosen capillary approximation.

Now suppose the two surfaces have different, unknown wetting conditions. The equations contain separate s_1 and s_2. The cancellation no longer determines p: two readings with three unknown quantities leave a consequential freedom. Restore the common surface condition, use useful bounds on the surface terms, or select another pressure-sensitive interaction.

The reservoir premise also matters. If filling the capillary changes the pressure whose earlier value was wanted, include the reservoir-probe volume and pressure relation through PHY.6 and C.16.MR. The maintained-pressure calculation cannot by itself recover that earlier value.

### PHY.9:5.3 - Prepare a probe whose phase difference can be read {#prepare-a-probe-whose-phase-difference-can-be-read}

An ideal two-level probe couples to a constant classical field B through

`H=(hbar gamma B/2) sigma_z`,

where gamma is a known coupling coefficient and sigma_z has eigenvalues +1 and -1 for states |0> and |1>. Treat the field as unchanged by this probe during the interrogation time t. The wanted quantity is B within a supplied range.

Prepare |0>. Evolution multiplies it by a global phase; measurements of this state cannot reveal that phase. Increasing t alone does not create a readable field dependence.

Instead prepare `|+>=(|0>+|1>)/sqrt(2)`. Evolution produces a relative phase `phi=gamma B t`. Reading sigma_z still gives equal probabilities and is uninformative about phi. A controlled rotation before detection permits a sigma_x or sigma_y measurement. Their means are cos(phi) and sin(phi), so the two preparations for readout can recover phase modulo 2 pi. Each mean requires the corresponding repeated preparation and measurement.

For gamma=1 rad/(s·field-unit), t=1 s and B=pi/3 field-units, the ideal means are 1/2 and sqrt(3)/2. They select phi=pi/3 modulo 2 pi. A supplied range `-pi < gamma B t <= pi` makes that field value unique.

If the field may instead lie between -4 pi and 4 pi field-units, the same records admit several values. Shorten the initial interrogation, for example to t=0.1 s with the same gamma: the whole supplied range then lies inside the unambiguous phase interval. A later longer interrogation can refine a value once the remaining range supports its interpretation.

Coherence loss, imperfect rotations or an uncertain gamma change the response law. They can be included or constrained where the required estimate needs them. The local phase response alone is not a claim that arbitrarily long interrogation or another quantum resource improves every sensing task.

## PHY.9:6 - Bias-Annotation {#bias-annotation}

The examples use controllable idealized arrangements to expose the construction. A field situation may limit access, preparation, reversibility or repeated sampling. Use those limits in choosing the interaction rather than treating the ideal case as an available apparatus.

Quantum sensing is one implementation of a wider physical move. Classical comparisons, chemical response and mechanical probes can serve the same construction when their physical relations and receiving use fit.

## PHY.9:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | What fails | Repair |
| --- | --- | --- |
| The quantity appears, so it is measured | Mass cancels from ideal falling acceleration. | Derive the complete response and choose a coupling that retains the wanted dependence. |
| Responsive interaction, insensitive readout | A relative phase changes while a population measurement stays constant. | Choose preparation and readout together with the interaction. |
| Common offset by notation | Two preparations use one symbol for physically different influences. | Establish the shared condition or retain separate contributions. |
| More readings resolve every ambiguity | Repetition improves a statistic without separating compatible target values. | Change the interaction or use the sufficient compatible range. |
| Correction without the coupled arrangement | Probe loading is removed by a formula from another physical setup. | Derive the effect for the actual target and probe conditions. |
| Maximum local slope means best measurement | A periodic response leaves widely separated possibilities indistinguishable. | Compare the required range, resources and attainable distinctions. |

## PHY.9:10 - Architectural Rationale {#architectural-rationale}

The measurement relation and the measuring interaction solve connected difficulties. A relation can be derived for a fixed setup that is incapable of resolving the wanted difference. Constructing a different coupling, preparation or reference changes what the relation can supply.

This physical construction links theory to observation and intervention. It also links physical computing to readout: a physical state can carry a computed result that the chosen observation does not distinguish. The mathematical and statistical interpretation remains with the corresponding methods; it receives the interaction and its conditions.

## PHY.9:11 - SoTA-Echoing {#sota-echoing}

The [VIM definitions of measurement principle](https://jcgm.bipm.org/vim/en/2.4.html) and [measurand](https://jcgm.bipm.org/vim/en/2.3.html) distinguish the phenomenon supporting a measurement from the quantity sought under specified conditions. [JCGM GUM-6:2020](https://www.bipm.org/documents/20126/2071204/JCGM_GUM_6_2020.pdf/d4e77d99-3870-0908-ff37-c1b6a230a337?download=true&t=1775224426559&version=1.15), especially sections 7.2 and 9, explains theoretical, empirical and hybrid response models and effects of realizing a measurement.

Compare the two mass procedures in :5.1. Timing ideal free fall is simpler but supplies no mass distinction. A known-force comparison supplies it at the cost of a force reference and acceleration readout. Reversal adds another preparation only when separating the force offset matters. Neither a more accurate clock nor more identical falls supplies the missing physical dependence.

[Degen, Reinhard and Cappellaro, *Quantum Sensing*](https://arxiv.org/abs/1611.02427), Reviews of Modern Physics 89 (2017), is a foundational synthesis of preparation, coupling, control and readout. [Pezzè and Smerzi, *Advances in multiparameter quantum sensing and metrology*](https://arxiv.org/abs/2502.17396), 2025, extends the selection question to several parameters, incompatible optimal measurements and finite resources. The adopted contribution is the joint choice of probe, encoding and readout; a quantum sensitivity bound needs its own estimation and attainability assumptions.

For the phase question in :5.3, the same Hamiltonian with an eigenstate probe gives no observable phase, while a superposition and suitable readout do. Short interrogation resolves the wider range; longer interrogation can improve local sensitivity while requiring range information and adequate coherence. More complex entangled or adaptive arrangements require a comparison under the actual resource and uncertainty conditions, not an advantage inferred from their name.

The [2026 amendment to JCGM 100](https://doi.org/10.59161/PPDI3267) explicitly addresses significant nonlinearity in both a measurement estimate and its uncertainty. It supports returning from a local sensitivity approximation when the receiving calculation depends on curvature. The applicable mathematical inference remains separate from construction of the physical coupling.

The numerical cases are constructed demonstrations under stated laws and idealizations. A changed material, interaction, preparation or readout range reopens the corresponding physical premise.


## PHY.9:End {#end}
