# PHY.2 - Construct a Physical Analogue from Interactions {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative within the stated use

## PHY.2:1 - Problem frame {#problem-frame}

Use this pattern when you want to understand or investigate a physical situation through another arrangement, and the needed analogue must be built or changed. You may know the target's laws but need an arrangement that makes their consequences accessible. Or you may be exploring an unresolved mechanism and need to construct a physical possibility that produces a consequence worth pursuing.

Here the **target** is the situation about which you want to learn. The **source** is the physical arrangement whose behavior supplies the analogy. The source may first be a thought construction: interacting bodies, material, fields or devices whose behavior can be reasoned about. It can then be expressed mathematically, simulated or built, according to the contribution the work needs.

Start with one target behavior and ask what physical interaction could produce it in a source. If two target parts affect one another, for example, ask what connection in the proposed source transmits that influence. The first result is a source construction, a consequence obtained from it, and an account of what that consequence permits you to infer or try in the target.

You need the relevant physical laws or someone able to supply them, together with the mathematical or qualitative reasoning required by the proposed construction. A ready analogue with a sufficient explanation of its use can be used directly. PHY.1 helps when the remaining difficulty is constructing conditions for a change of scale. C.29.1 helps when the physical constructions are already available and the unresolved work is the correspondence between their mathematical descriptions.

## PHY.2:2 - Problem {#problem}

A resemblance can suggest an analogy while leaving the source unable to produce the behavior that matters. Two components that behave appropriately in isolation can behave differently when connected. A source can also reproduce one target observation through a mechanism that gives a different response to an intervention.

The difficulty is building the source itself. Its components, interactions, preparation and surroundings must jointly produce a useful consequence. When the target mechanism is unresolved, construction and criticism of the source also refine the hypothesis about the target. An unsuccessful source can expose the missing interaction or a physical restriction that the next attempt must address.

## PHY.2:3 - Forces {#forces}

| Choice | What it changes |
| --- | --- |
| Familiar mechanism or relevant behavior | An accessible mechanism helps reasoning only to the extent that its consequences address the target question. |
| Separate components or coupled operation | A connection can impose a constraint, transfer energy, change loading or introduce another state. |
| Manipulable source or faithful target consequence | Making the source easier to prepare and observe can alter a relation needed for the intended inference. |
| Known target law or proposed target mechanism | The former can support a derived transfer; the latter can yield a hypothesis and a discriminating next move. |
| One construction or complementary constructions | Different sources can expose different consequences, while disagreement can locate an unresolved premise. |

## PHY.2:4 - Solution {#solution}

**Choose the target consequence → propose physical mechanisms for it → connect their interactions → recover preparation and correspondence → derive or produce a consequence → use it and revise the construction.**

### PHY.2:4.1 - Choose what the source must help you obtain {#choose-what-the-source-must-help-you-obtain}

State the target question in the terms of the work. You might need a response to an input, a possible mechanism for an observed change, a limit on a proposed behavior, or an arrangement that lets you manipulate an otherwise inaccessible relation. Say what is already known and what remains proposed about the target.

Follow the intended consequence to the relevant participants and interactions. A force on one body may change another through a stored deformation; a change at a boundary may propagate through transport. Recover the target relation that the source must help explain or use. B.5.FM and B.5.TU support this first account and its relation to a theory.

Keep the first construction as small as that question permits. For a question about coupling, two interacting parts can expose what a whole-device sketch leaves implicit. If the target mechanism is unknown, begin with an observed dependence and a proposed way it could arise. The proposal gives something to develop even before a complete target theory is available.

### PHY.2:4.2 - Propose mechanisms by the physical effect they supply {#propose-mechanisms-by-the-physical-effect-they-supply}

Ask what the source must retain, transfer, resist, amplify, constrain or change. Then choose physical processes that can perform those contributions under known laws. These are prompts for selecting relevant effects, not a required inventory of every source.

For example, a mass retains motion while a force changes it; a deformable body stores energy under loading; a capacitor accumulates charge while current flows; a dissipative interaction converts organized motion into less accessible energy. A driven body can maintain motion by drawing on an energy supply. A stochastic transition account can express unresolved switching between physically different states. Choose among such mechanisms from the target relation and the proposed source conditions.

Write or explain the law of each chosen interaction, its participants and its regime. Include direction and sign: a coupling can restore a displacement or increase it. Identify what is being approximated when a law is linearized or treated as instantaneous. When no suitable law is available, retain the interaction as the physical contribution still to be found.

A source can combine contributions from several familiar arrangements. Derive the behavior of that combination. A chain of separately plausible resemblances can leave an unconstructed connection in the middle; locate the participants and interaction at that connection. Mathematical formulation through MMP.10 or MMP.11 makes the resulting conditions easier to solve.

### PHY.2:4.3 - Construct the connection and its effect on the whole {#construct-the-connection-and-its-effect-on-the-whole}

For each connection that carries the target influence, identify what the connected parts share and what each can exchange. Write the interaction conditions together with the component laws. At an electrical junction, current conservation and common voltage connect the components; in a mechanical contact, the allowed motion and transmitted forces do that work. Other interactions need their own physical conditions.

Recover the state needed to continue the coupled behavior. The source may need a relative deformation, stored charge, field or direction of motion that neither isolated-component sketch retained. A.3.3.TR supplies the general state and joint-change construction. Here identify the physical means by which the additional state persists and affects the next change.

Check the physical restrictions that can defeat the construction. For an energy-carrying interaction, account for the relevant storage, exchange, dissipation and driving. A source that uses only passive dissipative elements cannot supply sustained amplification; an active source needs an identified supply. For a transport or switching mechanism, include the travel time, waiting law or constraint that changes the intended result. The useful restriction depends on the source, so follow it to the target consequence.

Use these restrictions to improve the construction. Add the missing coupling, replace an unsuitable element, change a boundary or keep a result limited to the regime the source can produce. If the target's required relation conflicts with the source's physical laws, choose another source or revise the hypothesis. This conflict is an informative result of construction.

### PHY.2:4.4 - Recover preparation, interpretation and available range {#recover-preparation-interpretation-and-available-range}

Describe how the relevant source state starts and how it is driven. The initial deformation of a target spring, for example, can require stored current in an electrical source. Setting every source state to zero would solve a different initial-value problem. Likewise, the preparation of a distribution includes more than its mean when its later behavior depends on that distribution.

Connect each source quantity used in the result to what it represents about the target. Include units and scales: source voltage may represent target velocity through a dimensional conversion, and source time may run faster. Derive that correspondence by substituting the conversion into the laws and preparation. C.29.1 provides the general argument that a source result transfers to the intended mathematical target.

When proposing a material realization, determine whether its components can supply the required signs, ranges and rates together. Include the effect of observing or driving the source if it changes the relevant behavior. A nominally passive observation can load an electrical node; a finite switching time can matter when the requested event is short. C.29.3 supplies the preparation, action and readout relation for physical computation.

For a thought construction, state the physical idealizations on which its consequence depends. That conditional result can already direct a useful change or inquiry. Building an apparatus is a further choice, selected when its outcome would add a worthwhile contribution through C.11.DUA.

### PHY.2:4.5 - Obtain a consequence and determine its reach {#obtain-a-consequence-and-determine-its-reach}

Manipulate the source according to its proposed laws. Start with a small input, a change of one interaction, or a limiting case that exposes how the construction works. Obtain the consequence by a derivation, a qualitative physical argument, a computation or an experiment. Use a known limiting case to find an omitted interaction or a sign error where it can discriminate between constructions.

Trace the obtained consequence back through its physical and mathematical premises. A computation can determine a property of the proposed source model. Interpreting an apparatus reading adds the account of the apparatus. Applying either result to a physical target adds the target correspondence and the physical premises used there. An existing explanation can supply those premises; no new evidence collection follows merely from enumerating them.

If the target mechanism remains proposed, use the result as a consequence of that hypothesis. Ask what change would make competing mechanisms disagree. This can reveal a useful intervention, a different observation interval or a parameter relation to examine. MMP.7 helps when the proposed distinction must be expressed through recorded data; C.11.DUA determines whether obtaining that distinction is worth the effort.

Different sources can contribute complementary results. One may expose an invariant or a bound, another the effect of noise or a difficult regime. Compare them for the usefulness, range and cost of the required contribution. G.5 distinguishes alternatives retained for later choice, non-dominated candidates and a set whose members contribute together. E.23 supports repeated improvement when a stated evaluation can judge the changed source.

### PHY.2:4.6 - Return to the target and change the useful part {#return-to-the-target-and-change-the-useful-part}

Use the result in the target work: choose a preparation, interpret an observation, propose a mechanism, reject a construction, or change the design of an experiment. Explain the physical route that makes the result relevant. EXD.3, in Explanation Design DPF, helps coordinate the words, diagram and equations another participant needs to recover that reasoning. C.2.8 characterizes the structure a recipient can extract with their available preparation and effort.

When a consequence fails or the question changes, locate the affected connection. Did the chosen source law fail, did connection change the source behavior, did computation or observation distort the result, or did the target correspondence omit an important difference? B.5.MPC.R supports this diagnosis. Revise the physical mechanism, state, preparation or correspondence that the failure implicates and retain the contributions that still work.

Keep a newly revealed question when pursuing it could open useful action. The next task can concern the target, the source or their connection. If the new construction changes what participants must produce or how their contributions join, ME.7 helps develop that proposed composition. ME.12 checks claims about the method and its description, and locates the contribution that needs correction.

## PHY.2:7 - Conformance Checklist {#conformance-checklist}

- The target question and the source's intended contribution can be stated in working terms.
- Proposed source mechanisms have physical laws and conditions sufficient for the consequence being obtained, or the unresolved contribution is identified.
- The connection includes the interaction, retained state and physical restrictions that can alter the result.
- Preparation, driving, interpretation and any scale conversions describe the same constructed case.
- A derived or produced consequence leads to an appropriate target inference, intervention, design choice or further question.
- A proposed target mechanism retains the premises still needed to use it; further inquiry is chosen by its possible contribution and cost.
- A changed question or failed consequence returns to the affected mechanism or correspondence while preserving useful existing results.

## PHY.2:9 - Consequences {#consequences}

The method can create a useful source where retrieval of a ready analogy fails. Construction exposes missing interactions, incompatible physical requirements and consequences that were difficult to see in the target. Those discoveries can refine both the source and the question.

Its cost is reasoning about two physical situations and their connection. An elaborate apparatus or simulation can be unnecessary when a short construction already answers the question. The source can also become misleading if its convenient mechanism is carried into the target beyond the inference it supports.

## PHY.2:12 - Relations {#relations}

B.5.FM and B.5.TU connect the target question with an initial physical account and theory. A.3.3.TR supplies the general construction of state and combined change. PHY.1 develops physical similarity conditions when scaling or changing a material is the operative problem.

C.29.1 establishes the correspondence used in inference; C.29.2 formulates the computation; C.29.3 connects a physical realization with preparation and readout. MMP.10 and MMP.11 formulate and develop the mathematical relations. MMP.7 connects a proposed physical distinction with a model of recorded observations. MMP.9 supplies the mathematical reduction when removing a physical state changes the retained evolution.

G.5 distinguishes the results of choosing alternatives or complementary contributions; E.23 governs repeated improvement under a stated evaluation. C.11.DUA selects worthwhile inquiry and use of sufficient results. B.5.MPC and B.5.MPC.R connect the physical, mathematical and computational contributions and locate a failure between them. C.2.8 characterizes extractable structure, and EXD.3 helps express the explanation; ME.7 develops the proposed composition account; ME.12 checks its claims and locates a needed correction.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-phy/contract/PHY-5#root/.6 for physical description and evolution; spec://ai.lev/fpf-think-phy/contract/PHY-9#root/.10 for observation and comparison; spec://ai.lev/fpf-spec/contract/C-29-3#root for computing realization. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-phy/contract/PHY-3#root @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-2
