# PHY.10 - Construct a Physical Test That Separates Rival Accounts {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## PHY.10:1 - Problem frame {#problem-frame}

Use this pattern when competing physical accounts remain compatible with what has been observed, and the work needs a distinction between them. The missing contribution is a physical test: a preparation, intervention or understood comparison whose recorded consequences can separate the relevant alternatives.

A resistor and a capacitor can produce identical current traces under one imposed voltage history. Changing that history can expose the difference between dissipation and storage. A decaying collective signal can also hide different individual dynamics; a suitable intervention can make those dynamics distinguishable.

The first result is a proposed physical comparison, with the response each account permits, the conditions needed to produce and read it, and what the possible outcomes would change. It can reveal that the available apparatus cannot make the wanted distinction. A performed test adds observations and an interpretation under those conditions.

You need the physical meaning and applicable laws of the accounts being compared. Mathematical, computational and experimental collaborators can supply particular derivations and implementations. B.5.TC helps align the accounts when their questions or predicted quantities still differ. PHY.9 constructs a missing measuring interaction.

Use an existing discriminating observation or sufficient comparison directly. Leave the difference unresolved when it does not change the intended use, or when acting with the remaining uncertainty is preferable to another test.

## PHY.10:2 - Problem {#problem}

Agreement with an observed response can have several physical explanations. A parameter can compensate for a missing interaction. A particular drive can make two response laws coincide. Different hidden dynamics can produce the same aggregate decay.

Collecting more data under the same uninformative conditions can leave the disagreement intact. Conversely, changing conditions to enlarge a predicted difference can introduce a new interaction, defeat the detector or leave the range in which either account was proposed.

A discrepancy also tests the combined account of the subject, preparation and observation. It need not identify the disputed physical premise by itself. The practitioner needs a comparison that exposes that premise while retaining the alternatives introduced by the apparatus and operating conditions.

## PHY.10:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Discrimination and estimation | Better knowledge of one account's parameters can leave its difference from another account unresolved. |
| Larger contrast and changed regime | A stronger intervention can expose the wanted effect while adding another physical mechanism. |
| Control and feasibility | A mathematically useful input need not be physically preparable with the available actuator, subject and resources. |
| Shared conditions and informative change | A comparison needs enough continuity to interpret a difference, while the test deliberately changes something. |
| Specific prediction and uncertain premises | Different nominal predictions can overlap after consequential parameter and apparatus uncertainty is included. |
| Useful criticism and effort | A simple consequence can settle the working question while a more elaborate experiment promises broader knowledge at greater cost. |

## PHY.10:4 - Solution {#solution}

**Locate the consequential physical difference → find a condition that exposes it → construct the preparation and readout → compare the permitted responses → use the result and locate any defeated premise → develop the next useful test or stop.**

### PHY.10:4.1 - State which physical disagreement matters {#state-which-physical-disagreement-matters}

Ask the accounts the same physical question under corresponding conditions. Recover what each treats as the subject, its state, its interactions and the measured quantity. Use B.5.TC if the apparent conflict instead concerns different questions, representations or approximations.

State the consequence the work needs to distinguish. It may concern a law, an omitted interaction, stored state, a response time or another physical dependence. A distinction matters through what it changes in explanation, prediction, construction or subsequent inquiry.

Retain the parameter freedom that each account still has. An account with an adjustable coefficient is a family of possible responses, not just the curve at one fitted value. Include the available information that restricts that freedom. Do not choose a new parameter value independently at every observation unless the account itself permits that dependence.

Identify the auxiliary premises on which the comparison turns. For a driven specimen, these can include its preparation, the applied input, its coupling to surroundings and the relation between its response and the recorded indication. A test of the specimen's law can fail because one of these premises fails.

### PHY.10:4.2 - Find a physical change that makes the accounts diverge {#find-a-physical-change-that-makes-the-accounts-diverge}

Trace the disputed difference forward to an observable consequence. Then ask which feasible change exposes it. For example:

- Change an amplitude, scale or operating regime when the accounts predict different dependence on it.
- Change the time course of a drive when the earlier input made different response laws coincide.
- Interrupt, reverse or refocus an interaction when the accounts retain different state or memory.
- Use a symmetry or balance when one account requires a response to vanish or remain within a bound.

Choose the change from the physical dependence at issue. PHY.4 supplies law constraints, PHY.5 examines a regime change and PHY.6-.8 derive the corresponding evolution or collective response.

Recompute both accounts under the proposed change. A prediction under the original preparation cannot be compared with a rival's prediction under the new one. Retain any changed interaction that can imitate or obscure the intended difference.

If intervention on the subject is unavailable, look for an accessible physical contrast: for example, a naturally varying condition with an understood relation to the accounts. Identify other differences between the observed situations. Their effects remain part of the comparison; naming the contrast does not make it controlled.

### PHY.10:4.3 - Construct the experiment that can realize the contrast {#construct-the-experiment-that-can-realize-the-contrast}

Translate the mathematical change into physical preparation and operation. Identify the means of imposing the input, the initial or boundary conditions it requires, and the observable response. Include timing when a transient, memory or change of state is decisive.

Determine which shared conditions must survive. Maintaining geometry, material state or a reference can be more consequential than increasing the number of readings. When the intervention itself changes one of these conditions, either include that change in both predictions or construct another contrast.

Derive the subject-apparatus response far enough to establish that the difference reaches the recorded indication. PHY.9 constructs a missing coupling, reference or readout; C.16.MR represents the resulting measurement relation. A detector that clips both predictions to the same indication cannot implement their proposed separation.

Account for feasibility through the parts that can change this design. Available force, pulse duration, preparation time or observation range can rule out a proposed contrast or leave it conditional. An established apparatus or supplied capability can settle those questions without rebuilding its justification. If the required operation remains unavailable, return that specific limit or choose another contrast.

Use a reference or control for a named alternative explanation. A no-drive comparison can reveal an offset; a reference pulse can bound a control error. Add it when the result can change the interpretation.

### PHY.10:4.4 - Compare the responses that can actually be distinguished {#compare-the-responses-that-can-actually-be-distinguished}

For each candidate design, obtain the readouts allowed by each physical account, including consequential parameter freedom and uncertainty in preparation, conversion and recording. MMP.7 supplies a probability law when records are random; C.16.IR helps determine what an indication can resolve.

Disjoint bounded response ranges give a particularly simple separation under their premises. If the ranges overlap, some outcomes can still discriminate the accounts while others remain compatible with both. Equal expected values likewise need not mean equal distributions or equal time dependence.

When discrimination depends on statistical evidence, use the appropriate model-comparison method with its dependence, sampling and error assumptions. Repeated readings do not automatically supply independent trials. A mathematical design criterion is useful only after the physical design and the interpretation of its records are supplied.

Compare designs on the distinction needed by the work and their full resource demand. A more informative record about one parameter need not be more informative about the rival mechanisms. Use a cheap sufficient contrast before constructing a costly optimization. C.11 compares available options; C.11.DUA addresses the value of another observation or computation.

Before performing the comparison, make its outcome interpretation clear enough to resist changing the question after seeing the result. State what would remain compatible with each account and which apparatus or preparation failure could mimic the disputed effect. The existing explanation or protocol can carry this reasoning.

### PHY.10:4.5 - Obtain the result and locate the failed premise {#obtain-the-result-and-locate-the-failed-premise}

Work the proposed preparation through to the predicted indication before committing the apparatus. This can expose an uninformative design or missing physical contribution without a new experiment.

When observations are obtained, interpret them under the stated recording and physical conditions. A response compatible with one supplied account and incompatible with another narrows this comparison. It does not exclude physical accounts that were never represented in the alternative set.

If the result disagrees with both, inspect the consequential premise rather than forcing a winner. Separate a computational error, an incorrect readout relation, an unachieved preparation and a defeated physical account. Follow the dependence of the failed prediction to identify a useful return. A supplied bound on an apparatus effect can sometimes exclude that explanation; when it cannot, retain the competing interpretations.

An agreement can also reveal a design limit. Determine whether the test retained the distinction it was meant to expose. If both accounts predict the observed outcome within the relevant uncertainty, report that limited result and preserve any unaffected consequence.

Reuse a result for the preparation, response range and question it supports. A successful test of a small-signal account does not determine its response after a regime-changing drive.

### PHY.10:4.6 - Revise the account or develop the next contrast {#revise-the-account-or-develop-the-next-contrast}

Return the interpreted result and the physical reason for the next move. This may be use of a sufficient account, a narrower parameter range, an added interaction, a different preparation or readout, or an unresolved difference that the work can tolerate.

Develop a subsequent test from what remains unresolved. One outcome can identify which regime, hidden state or control error matters next. Sequential design can exploit that information, but a complete sequence need not be invented when one comparison already supplies the useful result.

When a revision changes the physical account, propagate it to the mathematical formulation, computation and interpretation that depend on it. Use B.5.RR and B.5.MPC.R for the corresponding reasoning and cross-contribution revision.

Stop when the obtained distinction suffices, or when no worthwhile available test changes the present use. Preserve a promising unresolved physical question when it opens a useful later construction or investigation.

## PHY.10:7 - Conformance Checklist {#conformance-checklist}

- The accounts answer the same physical question under corresponding conditions.
- Their remaining parameter freedom and consequential auxiliary premises are retained.
- The proposed physical change makes a difference in an observable response.
- Preparation, drive and readout can realize that change, or their unresolved limit is stated.
- Discrimination is judged with the relevant physical and recording uncertainty.
- Possible results retain their different implications, including agreement with several accounts or disagreement with all supplied accounts.
- The first result and subsequent physical, mathematical or computational return are usable.

## PHY.10:9 - Consequences {#consequences}

Physical comparison becomes a construction that can change what is observable. Its result can be a discriminating experiment, a useful limit on current apparatus, an improved account or a justified stop.

The calculation, apparatus and interpretation can be developed by different contributors while retaining the common physical disagreement. The cost is concentrated on the dependencies that determine the comparison. A result may remain local even when it resolves the present work.

## PHY.10:12 - Relations {#relations}

- **B.5.TC and B.5.TU:** align the theoretical comparison and construct a missing application of an account.
- **PHY.4-.8:** constrain a law and derive the physical response to a changed preparation or interaction.
- **PHY.9 and C.16.MR:** construct the measuring interaction and its relation to the recorded indication.
- **C.16.IR and MMP.7:** determine what the indication resolves and supply the applicable recording probability law.
- **PHY.1-.3:** receive a discriminating comparison when similarity, a physical analogue or a limiting transformation needs examination.
- **C.11 and C.11.DUA:** compare available designs and the value of further inquiry.
- **B.5.RR and B.5.MPC.R:** revise the affected reasoning and its physical, mathematical and computational contributions.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-phy/contract/PHY-9#root for a needed readout; spec://ai.lev/fpf-think-phy/contract/PHY-6#root for evolution; spec://ai.lev/fpf-spec/contract/B-5-TC#root for theoretical comparison. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-phy/contract/PHY-9#root @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-10
