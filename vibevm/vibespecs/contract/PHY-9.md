# PHY.9 - Construct a Measuring Interaction for a Physical Distinction {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## PHY.9:1 - Problem frame {#problem-frame}

Use this pattern when a physical difference matters to the work, but the available arrangement does not make that difference observable. You may need to choose a sensing effect, prepare a reference, separate a wanted response from another influence, or change a probe that disturbs its subject.

The first result is a proposed measuring interaction with a usable response: what to prepare, what to couple, what to observe, and which physical differences the response can resolve. It can remain conditional on an identified coupling, calibration or operating range.

C.16.MR constructs the relation between a sought property and an indication. This method develops its physical realization when that realization is missing or inadequate. The work concerns designing an interaction, before or after a measurement exists. It need not produce a new instrument; changing a preparation or comparison can suffice.

You need to interpret the relevant physical theory and the conditions under which its effect occurs. Mathematical or experimental collaborators can supply calculations and implementation while you retain the wanted distinction. The examples supply their additional mechanical, fluid and quantum premises.

Use an existing arrangement and calibration when they already resolve the question. If the physical arrangement is suitable and only inference from its records remains, use C.16.IR or MMP.7. A more elaborate sensor is unnecessary when the present response already supports the decision.

## PHY.9:2 - Problem {#problem}

A property can affect a physical system without appearing in the chosen readout. Mass occurs in the force and inertia of a falling body but cancels from ideal gravitational acceleration. A field can change a quantum state's phase while the selected measurement remains insensitive to it.

A responsive instrument can also confuse the sought property with its own interaction. A capillary responds to pressure through a liquid column, but surface forces contribute to the height. Repeating the same reading more precisely does not separate those contributions.

The difficulty is to construct a physical comparison that exposes the wanted difference under the available conditions.

## PHY.9:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Coupling and selectivity | A strong response can amplify an unwanted influence as well as the target. |
| Preparation and observation | The same interaction can be informative for one prepared state and uninformative for another. |
| Reference and portability | A comparison can remove an unknown contribution while depending on shared physical conditions. |
| Signal and disturbance | The probe can make a difference visible while changing the quantity whose earlier value was wanted. |
| Local sensitivity and usable range | A steep response can improve a local estimate while leaving distant possibilities indistinguishable. |
| Improved measurement and effort | Another interaction is useful only when its added distinction matters enough to the receiving work. |

## PHY.9:4 - Solution {#solution}

**Choose the wanted distinction → select a responsive physical effect → construct the preparation and comparison → derive the readout and its disturbance → determine what can be resolved → revise the arrangement where needed.**

### PHY.9:4.1 - Specify the physical distinction and conditions {#specify-the-physical-distinction-and-conditions}

Name two physical possibilities that the work needs to distinguish, or a quantity range within which an estimate is needed. State where and when the property is sought. A pressure before connecting a probe and the pressure maintained during readout can be different targets.

Choose the needed consequence. Detecting a change, estimating a value and deciding which side of a limit applies place different demands on the same arrangement. C.16 provides the characteristic and scale; C.16.IR determines what a given indication can resolve.

Include the conditions the work permits you to change. A prepared reference, imposed force, interrogation time or detector orientation is a potential experimental choice only when it can actually be controlled.

### PHY.9:4.2 - Choose an effect that carries the distinction into a response {#choose-an-effect-that-carries-the-distinction-into-a-response}

Find a physical interaction through which the sought difference changes a state, transition, force, flow or other observable response. Derive that dependence far enough to see whether the proposed readout retains it. PHY.4 can constrain an unknown law; PHY.6 or PHY.7 can construct the relevant physical evolution.

Compare a small number of plausible arrangements. For each, ask what differs in the predicted readout between the selected physical possibilities under the same preparation. Reject an insensitive arrangement for this question even if it uses a well-established effect. The falling-body case in :5.1 shows why the occurrence of a quantity in one equation is insufficient.

Identify what supplies a reference. A known imposed quantity, a second preparation or a stable response can make the comparison interpretable. State the physical relation that allows the reference to be transported into this measurement. Numerical labels on two devices do not establish that relation.

Retain an unknown coupling as unknown. An available bound or a calibration can be enough; a proposed response without grounds for its coupling remains conditional. Select new characterization only when it can change the intended use.

### PHY.9:4.3 - Construct the preparation and comparison {#construct-the-preparation-and-comparison}

Specify how the subject, probe and reference are prepared before coupling. Then choose what is held fixed, what is varied and what is read. Include the order when the first interaction changes the next state.

Use a differential, reversed, ratio or null comparison when its physical invariance removes a consequential influence. Derive the cancellation from the arrangement. For example, reversing a known applied force while preserving a common force offset changes the wanted response but leaves the offset shared. A reversal that also changes the offset does not support that subtraction.

For a quantum probe, choose a prepared state, the parameter-dependent interaction and the measurement together. The physical interaction may be described by a channel taking rho to rho_theta; measurement operators E_k give outcome probabilities `P(k|theta)=Tr(rho_theta E_k)`. Here rho is the prepared state, theta the sought parameter, and the positive operators E_k sum to the identity. If those probabilities do not change with theta, that preparation and readout supply no information about it.

A reference can also select which part of a response is read. A phase-sensitive measurement needs a phase reference; a differential displacement needs a reference position. Preserve the conditions that make this reference stable during the comparison.

### PHY.9:4.4 - Include the effect of measuring on the subject {#include-the-effect-of-measuring-on-the-subject}

Construct the coupled subject-probe account for the duration that matters. Determine whether connecting the probe changes the sought quantity, changes only another quantity, or leaves its relevant value effectively unchanged. Use the physical coupling rather than a universal claim that measurement must disturb the target.

If the wanted value precedes coupling, derive how it can be recovered from the disturbed response, or change the arrangement to reduce the consequential disturbance. Keep uncertainty in that recovery. When correction is poorly determined, a different interaction or a conditional range can be more useful than more decimal places.

Compare the retained effect with the allowed error or decision margin. Loading, finite response time and backaction matter through their consequences for this question. PHY.5 helps justify an approximation. A usable result does not require modeling every interaction.

A nondestructive or non-demolition measurement protects a specified property under particular conditions; it does not establish that every later use of the subject is unaffected. Preserve any disturbance that changes the receiving experiment or work.

### PHY.9:4.5 - Determine the distinctions the readout supports {#determine-the-distinctions-the-readout-supports}

Compose the physical response with the actual recording procedure through C.16.MR. Use MMP.7 when the conclusion requires a probability law for those records. Retain common influences, saturation, timing and finite resolution when they affect the conclusion.

Determine whether different target values remain compatible with the same possible records. If they do, identify which interaction, preparation or readout could separate the relevant alternatives. A local slope measures a local response; it does not resolve a periodic ambiguity or a shared unknown parameter.

Use the uncertainty or error model appropriate to the inference. Strongly nonlinear conversion can change both an estimate and its uncertainty; do not assume that converting an average is equivalent to averaging the converted quantity. Apply the necessary mathematical propagation or inference method, rather than treating a sensitivity coefficient as a complete answer.

When several parameters or performance goals matter, compare achievable combinations under the available resources. Different measurements can favor different parameters. Use C.16 to characterize those combinations and C.11 when choosing between available arrangements.

### PHY.9:4.6 - Obtain a first result and revise the physical arrangement {#obtain-a-first-result-and-revise-the-physical-arrangement}

Work one admissible preparation through to a predicted readout and an interpreted result. This can reveal an unresolved physical relation before an instrument is built. It also gives collaborators a concrete construction to implement or compare.

Change a condition that could defeat the intended use. Check the shared premise of a subtraction, the range of an inverse, the time available for a response or the disturbance caused by the probe. Return to the smallest implicated part of the arrangement.

Use available observations where they can change confidence or selection. C.11.DUA helps choose between another measurement, a conditional result and proceeding with uncertainty. A statistical comparison or a calibration certificate does not substitute for a missing physical response.

Return the proposed arrangement, its preparation and readout, the result it supports and the conditions that would change that use. The next work may be implementation, calibration, inference or a different measuring interaction. PHY.10 constructs a physical test when the purpose is to separate rival accounts.

## PHY.9:7 - Conformance Checklist {#conformance-checklist}

- The target distinction includes the physical conditions under which it is sought.
- The proposed interaction makes that distinction affect the selected readout.
- Preparation, reference and comparison operations are physically interpretable.
- A cancellation or transferred calibration retains its shared physical premises.
- Disturbance and finite response are included when they change the wanted result.
- Local sensitivity is not substituted for resolution over the required range.
- The first result, remaining ambiguity and useful return to the arrangement are clear.

## PHY.9:9 - Consequences {#consequences}

The measurement can be improved by changing how information is physically produced. Better inference remains useful, but its contribution is tied to an interpretable preparation and response.

Different contributors can construct the coupling, calculate the response, prepare the reference and infer the result without losing the common physical question. When an existing arrangement suffices, the method ends with its use.

## PHY.9:12 - Relations {#relations}

- **C.16.MR:** constructs and composes the relation from the sought property and measuring arrangement to an indication.
- **C.16.IR:** determines which target distinctions a supplied indication or response relation can resolve.
- **PHY.4, PHY.6 and PHY.7:** constrain a physical law or construct the evolution needed to derive a response.
- **PHY.5:** determines whether an interaction, disturbance or response time can be neglected for the intended consequence.
- **PHY.8 and MMP.7:** construct physical statistics and the probability law of recorded outcomes when variation and recording affect the result.
- **PHY.10:** uses a measuring interaction in a physical test separating rival accounts.
- **C.29.2** formulates the needed computation; **B.5.MPC** connects what it produces with the mathematical claim and the physical question.
- **C.16 and C.11:** characterize attainable performance and resource combinations, then choose among available arrangements.
- **C.11.DUA:** selects further measurement or inquiry by what it can change and the effort it requires.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-spec/contract/C-16-MR#root for the measurement relation; spec://ai.lev/fpf-spec/contract/C-16-IR#root for inference from indications; spec://ai.lev/fpf-think-phy/contract/PHY-10#root for competing physical accounts. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-phy/contract/PHY-10#root, spec://ai.lev/fpf-think-phy/contract/PHY-2#root @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-9
