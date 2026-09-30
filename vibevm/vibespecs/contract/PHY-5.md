# PHY.5 - Choose an Effective Physical Description by Scales and Couplings {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## PHY.5:1 - Problem frame {#problem-frame}

Use this pattern when a physical question leaves you uncertain which motions, interactions or material details its description must retain. Resolving every microscopic change may be impractical. Omitting a fast motion or a small interaction may change the answer that matters.

Begin with one consequence: a response over a stated interval, a propagation speed, an accumulated exchange, or a distribution of outcomes. Choose one proposed omission and follow how it could affect that consequence. A simpler account with a justified range of use, or a reason to restore the omitted contribution, is a useful first result.

An *effective physical description* here describes the physical behavior needed at chosen scales without resolving every underlying process. Unresolved processes can still contribute through response coefficients, constraints, dependence on earlier states or fluctuations. The method helps choose and examine that description across physical branches.

You need to identify the physical participants, explain the interactions relevant to the question and compare their characteristic sizes or rates. A qualitative separation can direct the next construction. The examples add their own mathematical preparation: elementary differential equations for the motor, waves for the discrete chain, and covariance for thermal motion.

When a known physical account already answers the question under the intended conditions, use it. PHY.1 supplies similarity between changed arrangements; PHY.2 constructs an analogue from physical interactions. MMP.9 supplies mathematical reduction once the governing relations and retained quantities have been chosen. Use this pattern for the physical choice of those quantities, relations and conditions.

## PHY.5:2 - Problem {#problem}

A detailed account can obscure the mechanism that determines a response. A convenient coarse account can erase the same mechanism. The relevant distinction depends on the question: a description may preserve a mean displacement while losing its spread, or preserve slow motion while losing an initial torque.

A comparison of isolated time scales also misses how parts interact. A rapidly adjusting part can exert a sustained force. Unresolved molecular motion can produce both drag and continuing fluctuations. A small length can become consequential when the imposed variation approaches that length.

The task is to retain the physical influence required by the intended result, while choosing how much of its underlying process to describe.

## PHY.5:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Resolution and usable explanation | More resolved variables can expose a mechanism while making the relevant consequence harder to obtain. |
| Scale separation and coupling | A fast process can relax quickly yet continue to alter the slow behavior through its response. |
| Mean response and variability | An average can settle one question while missing fluctuations that determine another. |
| Local approximation and changed conditions | A useful omission can fail at a boundary, during preparation or after the work changes the forcing. |
| Available grounds and further inquiry | Existing laws and bounds may settle the choice; an unresolved physical premise can sometimes justify a targeted comparison. |

## PHY.5:4 - Solution {#solution}

**Choose the consequence → locate its physical influences → compare their scales in the coupled situation → retain the needed effects of unresolved processes → test the resulting answer → use it or restore the consequential difference.**

### PHY.5:4.1 - Choose the physical consequence and its resolution {#choose-the-physical-consequence-and-its-resolution}

State what the answer will let someone interpret, choose or do. Identify the relevant quantity and how it is used: an instantaneous value, a time integral, a spatial average, a peak, a correlation or a probability can require different descriptions of the same situation.

Include the preparation, forcing, spatial range and observation interval when they affect that answer. For example, the first moment after switching can include a motion that has already decayed when a later reading is taken. A question about a wave's arrival concerns a propagating disturbance and the wavelengths present in it.

Use the working question to choose adequate resolution. If a bound already determines the choice, recovering a detailed trajectory may add nothing to that choice. C.11.DUA helps when the value of further inquiry is uncertain. B.5.MPC connects the mathematical result and its conditions to the physical question.

### PHY.5:4.2 - Locate the interactions and compare their scales {#locate-the-interactions-and-compare-their-scales}

Follow the influence from preparation or input to the consequence. Identify what stores, transports, exchanges or dissipates the quantities involved. Include a boundary, contact, surrounding medium or measuring interaction when it carries an influence on that consequence.

Obtain the governing physical relations at the detail needed for this comparison. A studied theory, measured response or working hypothesis can supply them; retain which of these is being used. PHY.4 helps constrain an unresolved law. MMP.11 constructs its remaining mathematical family.

Derive characteristic sizes or rates from these relations and the proposed regime. Compare contributions to the same physical change. For time scales, compare relaxation with the fastest relevant forcing and with the interval of use. For spatial scales, compare a variation length with the scale of material structure or transport. An energy comparison may determine which states can be appreciably excited.

Inspect the coupled arrangement. A coupling can change a relaxation rate or create a collective mode. For a proposed rapidly adjusting state, ask whether small departures from its proposed response actually decay while the retained variables change. A response near loss of stability can become slow even though one component, considered alone, relaxes rapidly.

Scaling the equations as in PHY.1 makes these comparisons explicit. Keep the physical reason for each scale: a narrow gap, driving period or relaxation distance can matter more than the size of the whole apparatus.

### PHY.5:4.3 - Choose how unresolved processes enter the retained account {#choose-how-unresolved-processes-enter-the-retained-account}

Select the variables and interactions needed by the consequence. They may describe individual participants or collective quantities such as a displacement field, concentration or slowly changing amplitude.

For a part that adjusts rapidly, first determine what it adjusts *to*. Substitute that response into its coupling with the retained part. The resulting force, constraint or transport remains in the effective account. In the motor example, eliminating rapidly changing current retains its effect on torque and damping.

For a collection of unresolved processes, determine which of their effects remain:

- a mean response changes the retained forces or transport coefficients;
- a delayed response makes current change depend on earlier states;
- fluctuations produce a spread of possible changes around a mean response;
- a persistent unresolved mode may require another retained state.

Choose among these from the physical preparation and interactions. Eliminating variables mathematically can expose a memory term even in deterministic dynamics. A statistical description additionally needs grounds for the distribution of unresolved states. MMP.7 supplies probability composition for a specified information and recording situation; it does not choose the physical preparation.

An effective coefficient can be obtained from a more detailed description, existing measurements or a constrained response law. Compare the predicted quantity in a regime where the two descriptions apply and choose the coefficient to preserve that contribution. This matching can be useful even when no complete microscopic theory is available. Carry the range and remaining uncertainty that change its later use.

### PHY.5:4.4 - Construct the approximation and its first omitted contribution {#construct-the-approximation-and-its-first-omitted-contribution}

Use MMP.9 for the mathematical elimination or retained-state evolution. Keep the physical assumptions that permit the construction alongside its result.

For a rapidly relaxing state, examine its initial departure and response to changing inputs. Replacing it by a steady response is useful when the remaining departure has sufficiently little effect on the requested consequence. The motor calculation below derives that departure instead of assigning it zero at the initial instant.

For a spatial or energy expansion, choose the ratio in which the description is expanded and compare the first omitted contribution with the retained ones. The ratio and its powers come from the physical relations. In the chain example, expansion in the small ratio of lattice spacing a to wavelength lambda, or equivalently in `q*a=2*pi*a/lambda`, yields a continuum wave description and its leading correction.

When unresolved correlations persist over the interval of interest, retain their delayed influence or add variables that reproduce it. Replacing a delayed response by an instantaneous one needs a comparison of that response time with the retained motion and driving. A mathematically equivalent auxiliary state is another way to calculate the memory; its interpretation as a material component requires a separate physical account.

Maintain the relevant exchanges and constraints through the approximation. Recover the condition for a balance or an allowed motion when changing the variables or boundaries. C.29.BB supplies the common balance construction.

### PHY.5:4.5 - Judge the influence on the requested answer {#judge-the-influence-on-the-requested-answer}

Follow the approximation through to the actual output. A small state error can grow under differentiation, accumulation, feedback or a sensitive later choice. MATH.20 supplies bounds. If the consequence is obtained in another mathematical account, C.29.1 establishes what transfers between the accounts.

Examine conditions suggested by the construction itself. An omitted initial transient matters when the reading moves into it. A spatial approximation becomes suspect when the wavelength approaches the unresolved structure. A weak loss can determine a resonant response. A nearly unstable mode can defeat the earlier time-scale separation. Use the conditions that affect the proposed account.

For a statistical description, compare the statistic the work uses. Preserving an average response need not preserve a variance or a transition probability. In thermal motion, eliminating velocity while retaining random forcing can preserve long-time displacement statistics. Deleting that forcing gives a different result.

A derivation, an existing limiting result or a suitable comparison can settle the choice. If a physical premise remains unresolved, identify a feasible change of preparation or readout for which the plausible accounts give different useful answers. Obtain that comparison when its possible outcomes warrant the effort. A conditional physical conclusion can remain useful while a stronger claim is unresolved.

### PHY.5:4.6 - Use the account and reopen the affected physical choice {#use-the-account-and-reopen-the-affected-physical-choice}

Return the answer with the conditions needed to use it. These may be expressed in a short derivation, an annotated model or an ordinary explanation.

Choose what the work now permits: use the simpler computation, interpret a measurement, change a drive, retain a fluctuation model, or restore an interaction. If several accounts provide complementary consequences, retain their respective uses. When a choice among available descriptions matters, C.11 supplies the comparison, including whether more inquiry is worth its cost. Use G.5 when the retained set itself must be stated: distinguish alternatives for later choice from descriptions used together for a named result. E.23 supports improvement when the chosen characteristics can judge a change.

For a new question or failed prediction, return to the influence whose omission is implicated. Change the physical variables, coupling, preparation or range, then redo the affected reduction and interpretation. B.5.MPC.R helps separate a physical-account failure from a mathematical or computational one.

The result can also change the method of work. A team may calculate a slow response with one model and delegate a short transient to another. ME.7 describes those contributions and their joins; ME.12 examines the claims needed for the combination. Each result retains the physical conditions that make it usable by the next participant.

## PHY.5:7 - Conformance Checklist {#conformance-checklist}

- The intended consequence specifies the physical quantity, relevant preparation, range and interval.
- The comparison uses the coupled physical arrangement and explains the characteristic scales.
- Each omitted process retains any mean response, constraint, delayed influence or fluctuation needed by that consequence.
- The approximation follows from stated physical relations or remains an identified hypothesis.
- A bound or comparison reaches the actual requested output, including a relevant initial or boundary contribution.
- A changed condition that can defeat the selected description leads back to the implicated physical choice.
- Existing results are used when sufficient; further inquiry is selected for what it could change.

## PHY.5:9 - Consequences {#consequences}

A useful effective account makes a physical mechanism easier to reason about and calculate with. Its stated regime supports a targeted return when the forcing, observation or intended action changes.

The choice costs physical analysis and sometimes a comparison with a richer account. It saves work when those results permit a cheaper calculation or a clearer explanation. A range without adequate scale separation can require a coupled, memory-bearing or more resolved description.

## PHY.5:12 - Relations {#relations}

- **B.5.TU and PHY.4:** supply application of a physical theory and constraints on an unresolved law.
- **A.3.3.TR and C.29.BB:** supply common state, interaction and balance constructions used by the physical account.
- **MMP.9:** supplies elimination and reduced evolution; **MMP.7/.11** supply probability composition and constrained response families.
- **MATH.20** bounds the unresolved contribution; **C.29.1** establishes transfer of a bound or consequence between mathematical accounts.
- **PHY.1/.2/.3:** use the chosen description in similarity, analogue construction and physical limits.
- **C.11.DUA and C.11:** examine the value of further inquiry and choose among available descriptions.
- **G.5 and E.23:** state retained alternatives or jointly used descriptions when needed, and guide improvement by the chosen characteristics.
- **B.5.MPC.R and ME.7/.12:** return to a failed contribution and revise the method that uses the physical result.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-mmp/contract/MMP-9#root for mathematical elimination; spec://ai.lev/fpf-think-phy/contract/PHY-6#root/.8 when evolution or collective preparation matters. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-phy/contract/PHY-1#root, spec://ai.lev/fpf-think-phy/contract/PHY-2#root @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-5
