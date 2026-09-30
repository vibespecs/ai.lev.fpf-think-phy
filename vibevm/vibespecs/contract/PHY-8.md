# PHY.8 - Infer Macroscopic Physical Behavior from Microscopic Alternatives {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## PHY.8:1 - Problem frame {#problem-frame}

Use this pattern when you need to explain or predict collective physical behavior from possible microscopic states or histories. The difficulty is deciding which alternatives matter, why they receive particular weights, and whether their aggregate represents the observation you need. Many constituents can produce a stable average, persistent fluctuations or a response that depends on preparation.

The first result is a collective prediction with its physical grounds: a distribution of an observable, its mean and relevant fluctuations, or an evolution law at the required scale. If different plausible preparations give different answers, retain that difference and identify what would settle it.

Here *microscopic* and *macroscopic* refer to levels of physical description. A microscopic description retains distinctions that the selected collective observable combines. The method can apply to a small system's aggregate as well as a large population; the approximation of a stable macroscopic value requires its own grounds.

You need to interpret the physical preparation and interactions, and to understand the probability operations used in the calculation. Quantum cases require the corresponding state and measurement rules. A collaborator can supply those mathematical operations while you retain the question and physical interpretation. The worked cases state their additional branch-specific premises.

Use a direct balance or an established effective law when it already gives the needed consequence with adequate conditions. Construct the microscopic account when fluctuations, changed preparation or a proposed mechanism can alter that consequence. PHY.5 helps choose which detail to retain.

## PHY.8:2 - Problem {#problem}

A correct average can answer the wrong physical question. A detector saturates on individual excursions, not on the ensemble mean. A system prepared in one part of its state space need not explore all alternatives during the observation. Separate constituents can share a preparation that makes their fluctuations add together.

The weighting is also a physical choice. Counting possible states does not by itself make them equally probable. Fitting a distribution to a signal does not establish the microscopic mechanism that produces it. A numerical sequence can sample the desired distribution without representing the time evolution of the system.

The task is to carry physical preparation and interaction through the statistical construction to the consequence that will be used.

## PHY.8:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Microscopic detail and useful aggregate | A detailed account can explain a changed response, while an unchanged total may need only a balance. |
| State counting and preparation | Many alternatives are possible, but the preparation and dynamics can weight them differently. |
| Typical behavior and rare outcomes | A narrow central range can support ordinary operation while missing a consequential excursion. |
| Individual properties and collective dependence | Local statistics can be unchanged while correlations alter the whole. |
| Long-time theory and available time | A limiting result may be valid yet unavailable within the observation interval. |
| Sampling economy and physical meaning | An efficient sampler can obtain a statistic without reproducing physical motion. |

## PHY.8:4 - Solution {#solution}

**Choose the collective consequence → construct the microscopic alternatives and their weights → derive the observable statistics → test the relevant fluctuations and times → revise the implicated physical premise.**

### PHY.8:4.1 - Specify the observable and how it will be used {#specify-the-observable-and-how-it-will-be-used}

Name the physical quantity, spatial extent and observation interval. Decide whether the work needs a value at one time, a time average, a response after an intervention or the chance of crossing a threshold. These uses can require different statistics from the same system.

Relate the observable to the retained microscopic description. In a classical account, write it as a function of the state, or of a history when the measurement integrates over time. Include a measurement response when it changes the answer. MMP.7 constructs the probability law of the recorded outcome from a subject law and a recording procedure.

Separate physical variation from uncertainty about a fixed parameter. A rate that changes among preparations, an unknown common rate and a fresh independent rate for each constituent describe different arrangements. Keep a fixed unknown parameter explicit unless a probability law over it is warranted for the intended inference.

### PHY.8:4.2 - Construct admissible alternatives and their weighting grounds {#construct-admissible-alternatives-and-their-weighting-grounds}

Choose the microscopic variables and their physical constraints. Use the theory and preparation to determine possible states, conserved quantities, accessible transitions and coupling to the surroundings. Preserve collective restrictions: fixing total energy or particle number can couple otherwise separate constituents.

Then say what supports the weights. A controlled preparation can supply frequencies; an admitted dynamical law can transport an initial distribution; an equilibrium argument can supply a statistical ensemble under its physical assumptions. An ensemble is a statistical description of possible preparations or states, not an additional physical population that must exist.

For an equilibrium construction, identify what the surroundings hold fixed and what can be exchanged. If a weakly coupled subsystem exchanges energy with a large equilibrated reservoir, a canonical distribution may be appropriate. If the total energy is fixed, begin with that restriction instead. Retain state multiplicities: several distinct states with one energy contribute separately. Check equivalence of proposed ensembles for the observable and regime being used before substituting one for another.

A maximum-entropy inference selects a distribution relative to specified alternatives, a reference measure and constraints. It can provide a useful conditional prediction. Its inferential grounds remain distinct from an argument that this preparation physically equilibrates to that distribution.

For a quantum account, use the prepared state and the relevant observable or measurement operators. A density operator can represent a subsystem correlated with its environment. Its decomposition into weighted pure states need not identify a unique physical preparation. Compute the probabilities of the chosen measurement using the theory; do not replace the state by presumed simultaneous values for incompatible measurements.

If the grounds leave several weightings possible, carry their different consequences far enough to see whether the unresolved choice matters. A bound or a common consequence can already answer the work question.

### PHY.8:4.3 - Derive the collective law without discarding dependence {#derive-the-collective-law-without-discarding-dependence}

Obtain the observable's distribution by combining the admissible alternatives with their weights. For a classical state X with probability law P and an observable Y=g(X), the probability of a set B of outcomes is

`P(Y in B) = integral 1[g(x) in B] P(dx)`.

The symbol 1 is one when its bracketed condition holds and zero otherwise. Use a weighted sum for a discrete state set. A non-ideal recording procedure adds its conditional response through MMP.7.

For a quantum state rho and an ideal measurement of observable A, outcome probabilities follow from the corresponding measurement projectors. When the second moment is finite, the mean is `Tr(rho A)` and the variance is `Tr(rho A²) - Tr(rho A)²`. Here Tr denotes the trace, and A represents the physical observable under the selected measurement. When the required moments are not finite, use the outcome distribution or a relevant bounded event instead of these finite-moment summaries. Other measurement arrangements require their own operators and response.

Retain correlations while forming collective quantities. For a finite collection of jointly defined classical outcomes X_i with finite second moments,

`E[sum_i X_i] = sum_i E[X_i]`,

`Var(sum_i X_i) = sum_i Var(X_i) + 2 sum_(i<j) Cov(X_i,X_j)`.

Linearity of the mean needs no independence assumption. The variance equals the sum of individual variances when the total covariance contribution, `2 sum_(i<j) Cov(X_i,X_j)`, is zero. Pairwise zero covariance is sufficient, and independence is a stronger sufficient condition. Retain the dependence supplied by the physical arrangement.

A mean may be all that the question needs. When excursions matter, derive a relevant variance, tail probability or bound. Preserve units and the normalization used for comparison: the variance of a total and that of a per-constituent average differ by the square of the constituent count.

### PHY.8:4.4 - Establish when the aggregate represents a typical observation {#establish-when-the-aggregate-represents-a-typical-observation}

Compare the predicted spread with the tolerance or decision in the work. For any scalar observable Y with finite variance and positive tolerance epsilon, Chebyshev's inequality gives

`P(|Y-E[Y]| >= epsilon) <= Var(Y)/epsilon²`.

This can settle a sufficient bound without reconstructing the whole distribution. If the bound is too loose to decide, a sharper calculation may help. Its cost is justified by the unresolved decision, not by the mere availability of another statistical method.

For an average over N constituents, the variance is bounded by a constant times 1/N when the sum of relevant covariances is bounded above by a constant times N. A common fluctuating influence can instead make the total variance grow as N². Inspect the physical dependence that determines this scaling. Increasing the number of constituents then has different effects on reliability.

Keep a probability claim relative to its measure. A set containing most of the probability need not contain most of the unweighted alternatives. Conversely, a large count of states says little about the prepared distribution until its weights are supplied.

Decide whether a finite system and the requested observable permit the limiting argument. Correlation lengths comparable to system size, constraints, long-range interactions or operation near a transition can invalidate the approximation used to obtain concentration. Return to the physical account when that invalidation changes the required result; do not require a thermodynamic limit for an already sufficient finite calculation.

### PHY.8:4.5 - Connect ensemble behavior to physical time {#connect-ensemble-behavior-to-physical-time}

An ensemble mean at time t and a time average along one history answer different questions. To use the latter as an estimate of the former, examine the relevant dynamics, preparation and observation duration.

Derive or obtain a relaxation or correlation time for the selected observable. Compare it with the duration available and with any external drive. A stationary distribution can exist while equilibration is too slow for the experiment. An invariant portion of state space can preserve dependence on the initial preparation. A theorem about an infinite-time average supplies no finite settling time by itself.

For a stationary scalar process A(t) with covariance C(tau)=Cov(A(t),A(t+tau)), the variance of its average over duration T is

`Var(A_bar_T) = (2/T²) integral from 0 to T of (T-tau) C(tau) d tau`.

This relation assumes finite second moments and a well-defined time integral. Use it, or a suitable finite-sample counterpart, when the accuracy of time averaging matters. Long correlations reduce the gain from repeated measurements; drawing more points from the same slow fluctuation does not make them independent.

If an eliminated variable leaves memory in the retained evolution, keep that memory or restore a sufficient state through PHY.5 and MMP.9. Decide which description serves the time-dependent question. A stationary histogram alone does not establish the transition law, response time or heat dissipation.

### PHY.8:4.6 - Compute, compare and return to the physical premise {#compute-compare-and-return-to-the-physical-premise}

Use a finite enumeration, analytical calculation or numerical sampler appropriate to the selected statistic. C.29.2 helps formulate the computation. Check that the computation implements the chosen state space, preparation, dependence and observable.

A Monte Carlo sampler can deliberately use artificial transitions to obtain a distribution. Interpret its steps as physical time only when a separate physical transition law and time calibration justify that use. Convergence of a numerical estimate, statistical concentration of the physical observable and adequacy of the microscopic account are different questions.

Make the comparison that can change the work decision. A small case can reveal a lost correlation. An available observation can distinguish two preparations. A changed observation interval can expose an invalid equilibrium approximation. Retain a sufficient conditional answer when further evidence would not justify its cost; C.11.DUA governs that choice.

Return to the implicated premise: the prepared state, weighting, interaction, measurement response or time-scale assumption. Preserve unaffected balances and mathematical consequences. The next question may concern controlling fluctuations, constructing a different preparation or choosing a more informative observable.

## PHY.8:7 - Conformance Checklist {#conformance-checklist}

- The requested observable, preparation and observation interval are recoverable.
- The microscopic alternatives and their weights have stated physical or inferential grounds.
- Collective constraints and relevant correlations survive the aggregation.
- The statistic answers the intended use, including a fluctuation or tail question when one matters.
- A concentration or equilibration argument has conditions appropriate to the finite system and observation.
- Computational transitions are interpreted as physical time only with a supporting physical law.
- A changed result returns to the implicated premise, while a sufficient conditional answer can remain in use.

## PHY.8:9 - Consequences {#consequences}

A collective prediction becomes revisable through its physical premises. A team can assign construction of the preparation and microscopic law, probability calculation, numerical estimation and interpretation to different contributors while retaining what each result assumes.

The work can avoid both unnecessary microscopic simulation and an unjustified average. A bound can finish the present decision; a correlation or finite-time effect can instead open a different preparation, observation or physical account.

## PHY.8:12 - Relations {#relations}

- **PHY.5:** chooses an effective physical description and restores an omitted coupling, state or memory when its consequence matters.
- **PHY.6 and C.29.BB:** construct the balance and response relations retained in collective evolution.
- **MMP.7:** composes the physical subject law with the recording procedure and derives the law of the recorded data.
- **MMP.9:** derives a reduced evolution from a more detailed mathematical account under stated assumptions.
- **B.5.MPC** connects the mathematical consequence to the physical question; **C.29.2** formulates any needed computation.
- **C.16.MR:** identifies the measurement relation whose physical and statistical realization is being used.
- **B.5.MPC.R:** repairs the implicated physical, mathematical or computational contribution and its affected uses.
- **C.11.DUA:** chooses whether resolving an uncertainty warrants further work or a sufficient conditional result should be used.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-mmp/contract/MMP-7#root for probability composition; spec://ai.lev/fpf-think-mmp/contract/MMP-9#root for reduction; spec://ai.lev/fpf-think-phy/contract/PHY-6#root for the required physical evolution. @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-8
