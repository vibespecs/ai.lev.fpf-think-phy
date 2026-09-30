# PHY.6 - Construct Physical Evolution from Balances and Response Laws {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## PHY.6:1 - Problem frame {#problem-frame}

Use this pattern when you can identify physical participants and their interactions, but cannot yet say how their coupled situation will evolve. You may know what is conserved while lacking the law that determines an exchange rate. You may have equations for each part while their connection or initial preparation remains inconsistent.

Start with the consequence you need: an initial response, a trajectory, a transported amount, a settled state or a distribution of outcomes. Choose the participants, exchanges and response laws needed for that consequence. A usable first result is a coupled physical description from which the consequence follows, or an identified missing response or incompatible condition that tells you what to resolve next.

Here a *response law* relates a physical interaction or change to the conditions on which it depends. A constitutive law is one such relation for a material or component. The method constructs an account from physical balances, response laws and preparation; it works across physical branches.

You need to identify the physical quantities and interpret the proposed relations and their conditions. The worked cases add their own preparation: elementary motion and energy calculations, a spatial continuity equation, and charge storage. These are different demonstrations of the same construction.

If a known physical account already supplies the required result, use it. If a balance alone settles the question, stop there. C.29.BB supplies that general balance method. Use PHY.5 when choosing which physical detail to retain; use this pattern when assembling the retained physical relations. Once that account is settled, MMP.10 and C.29.2 help formulate and obtain its mathematical consequences.

## PHY.6:2 - Problem {#problem}

A balance says how accumulation relates to transfer and production. It can leave the transfer itself unknown. Adding a convenient rate formula may complete an equation system while describing the wrong physical interaction.

Combining individually useful descriptions adds another difficulty. A contact may store a quantity, a connection may impose a constraint, and two parts may use different signs or reference frames. Initial values acceptable to each isolated part can be impossible after they are connected. A solver can then fail for a physical reason, or return a result for a preparation different from the intended one.

The task is to construct mutually compatible physical relations and preparation, then derive the consequence that the work needs.

## PHY.6:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| General balance and particular response | Conservation restricts change; material and interaction laws determine much of the remaining behavior. |
| Reusable parts and coupled behavior | A part's relation can remain useful while its boundary conditions change when connected. |
| Ideal connection and physical preparation | An ideal constraint can simplify later evolution while excluding the supplied initial state. |
| Physical detail and sufficient answer | A total or a bound may answer the question even when a detailed trajectory remains undetermined. |
| Available grounds and conditional use | An established response supports a stronger physical claim than an untested working hypothesis, while both can support useful conditional reasoning. |

## PHY.6:4 - Solution {#solution}

**Choose the consequence → identify participants and exchanges → supply response laws → connect the relations → make the preparation consistent → derive and use the needed consequence.**

### PHY.6:4.1 - Choose the consequence and physical participants {#choose-the-consequence-and-physical-participants}

State what the answer will let someone interpret, choose or do. Identify the quantity, interval and preparation that matter. A peak response, a total transferred amount and a settled value can require different accounts of the same arrangement.

Choose the physical participants and their boundaries at a useful resolution. Locate the interactions that can affect the answer, including supports, surrounding media and measurement when relevant. Distinguish a quantity stored in a participant from a quantity passing through its boundary. Include storage in a contact or field when omitting it would change the consequence.

Use PHY.5 to resolve a consequential choice of scale or omitted interaction. A spatial field, a few aggregate variables and individual particles are possible descriptions; their physical adequacy depends on the question and regime.

### PHY.6:4.2 - Construct the balances with physical meanings {#construct-the-balances-with-physical-meanings}

Use C.29.BB to choose the additive quantity, common interval, signs, transfers and internal production. Write each term with its physical meaning and compatible units. For vector quantities, use a common frame or an explicit transformation between frames.

For a fixed spatial region, a useful form is

`rate of stored quantity = inward transfer - outward transfer + internal production.`

A local continuity equation expresses the same relation for a density and its flux. The choice of quantity determines the production term: a chemical species can be consumed while the atoms it contains remain in reaction products. A closed boundary alone does not make every selected quantity constant.

Identify which terms remain undetermined. A momentum balance may still need forces; a species balance may need transport and reaction rates. If the requested total already follows without those details, retain that consequence and avoid completing an unnecessary model.

### PHY.6:4.3 - Supply the response and configuration relations {#supply-the-response-and-configuration-relations}

For each unresolved interaction that affects the answer, state how its response depends on the physical conditions. Use an applicable theory, an established material response, an available measurement or a stated working hypothesis. PHY.4 helps constrain a law whose form is unknown; MMP.11 helps represent its remaining freedom.

Recover the conditions under which the relation is used. Does it describe the current state, dependence on earlier states, a spatial gradient, an average response or fluctuations? Does it assume a settled contact, a constant material parameter or a particular preparation? Supply the configuration relations needed to connect that response to the retained variables.

Keep physical restrictions that the chosen description relies on. A passive damping law transfers mechanical energy into other forms; it does not destroy total energy. If that heating changes the response during the intended use, include the resulting dependence. A fitted or learned response can also supply a relation, but its physical restrictions and usable range must come from its construction or grounds, not from the fact that it produces numbers.

When several physically plausible laws remain, derive what each changes in the requested consequence. A bound or a conditional answer may be sufficient. Seek another observation or a more detailed account when its possible result can change the work; C.11.DUA helps decide that inquiry.

### PHY.6:4.4 - Connect the physical relations before choosing a solving order {#connect-the-physical-relations-before-choosing-a-solving-order}

State what a connection makes common and what it transfers. Match quantities, units, frames and orientations at that connection. Equal values require a physical reason: two locations in contact can still have a finite resistance or an intervening store. If the connection has its own consequential dynamics, describe those dynamics.

Combine the part balances through the common transfer. Transfers internal to the combined boundary cancel when they describe the same exchange over the same interval. Retain conversions between quantities and energy forms. For an energetic connection, derive its power expression from the physical variables; variable names such as *potential* and *flow* alone do not establish their product as power.

Keep the equations as simultaneous relations while constructing the physical account. They can include derivatives, algebraic constraints, spatial dependence or statistical response. In a differential-algebraic description, some relations constrain values while others describe change. Which variable is solved for is a later mathematical or computational choice; changing that order need not change the physical interaction.

Eliminate a variable only while retaining the relation or reconstruction needed by later use. MMP.9 supplies mathematical reduction and MMP.10 supplies a formulation for the chosen analysis. If two parts disagree at their connection, return to their quantity meanings and physical assumptions before changing a solver.

### PHY.6:4.5 - Make the preparation compatible with the connected account {#make-the-preparation-compatible-with-the-connected-account}

Supply the independent initial, boundary and driving conditions needed by the requested evolution. Substitute the proposed preparation into the connected relations. Solve for dependent initial values and reactions. Preserve the difference between a physical initial condition and a numerical starting guess.

A motion constraint also constrains admissible initial velocity. An electrical connection can constrain initial potentials. A spatial description needs boundary conditions appropriate to its transport and response. Determine which conditions can be chosen freely and which follow from the others.

An equation count can expose an omitted relation, but equal counts do not establish a consistent or uniquely determined problem. Examine the dependence of the actual relations and the existence conditions needed for the intended result. C.29.2 supplies the subsequent computational formulation; a solver diagnostic can help locate a problem without deciding whether the physical preparation should change.

If the preparation is incompatible, identify the conflict and its physical alternatives. Correct a mistaken initial value, relax an unjustified ideal constraint, or describe the interaction that establishes the new state. Choose among these from the actual preparation. Do not silently substitute an easier initial state.

### PHY.6:4.6 - Derive the consequence and return through the implicated premise {#derive-the-consequence-and-return-through-the-implicated-premise}

Obtain the first result at the resolution the question needs. This may be an initial derivative, an integrated balance, a limiting state or a computed evolution. B.5.MPC connects the mathematical result and its conditions to the physical question.

Use checks that can distinguish a wrong construction for this use. Combining part balances can expose a duplicated exchange; an energy calculation can expose a sign error or an omitted conversion; substituting the preparation can expose an impossible constraint. A limiting case or available observation can test a disputed physical premise. Passing one such check establishes only what it examines.

Distinguish a consequence of the stated equations from evidence that those equations describe the intended situation. Numerical accuracy concerns how the chosen consequence was obtained. Physical adequacy concerns the premises, preparation and interactions represented. Keep those qualifications with the result, without requiring new evidence when the conditional result already serves the work.

When the question, preparation or connection changes, revisit the affected relations. Retain contributions whose conditions still hold. An unresolved exchange law directs work to physical theory or response characterization; inconsistent coupled quantities direct work to the connection; an adequate account with an inaccurate computed result directs work to the computation. B.5.MPC.R supplies the broader repair when physical, mathematical and computational contributions need to change together.

## PHY.6:7 - Conformance Checklist {#conformance-checklist}

- The intended physical consequence and relevant preparation determine the scope of the construction.
- Each balance names the selected quantity, physical transfers and any production or conversion.
- Response and configuration relations supply the dependencies needed for the answer, with their physical grounds and conditions.
- Connected descriptions agree on exchanged quantities, signs, units and frames; consequential connection storage or dynamics remain represented.
- Independent initial and boundary conditions are compatible with the coupled relations, and dependent conditions are derived.
- The first consequence is obtained or a particular missing response or incompatible preparation directs the next work.
- Checks and further inquiry concern what can change the intended use; mathematical consequence, computational accuracy and physical adequacy remain distinguishable.

## PHY.6:9 - Consequences {#consequences}

The construction makes a physical account easier to use and divide among contributors. A specialist can supply a response law or preparation condition while another derives or computes its consequence. The connection states what each contribution must mean for the combined result.

Balances expose some construction errors cheaply. They leave many response questions open, so a balanced model can still be physically inadequate. Complex constraints, unresolved responses or changing regimes can require more physical work before the desired prediction becomes available. A conditional result or a narrower consequence can remain useful during that work.

## PHY.6:12 - Relations {#relations}

- **C.29.BB:** constructs balances across chosen boundaries and distinguishes transfer from production.
- **B.5.TU, PHY.4 and PHY.5:** supply theory use, constraints on an unknown law and the choice of effective physical detail.
- **MMP.10 and C.29.2:** formulate the selected mathematical question and obtain its result; **MMP.9** supplies mathematical reduction when needed.
- **MMP.11:** represents the freedom left in a response law after applicable constraints.
- **A.3.3.TR:** supplies common construction and composition of relations between states; the present method supplies the physical response and preparation.
- **B.5.MPC** connects the consequence to the physical question; **B.5.MPC.R** repairs a failed connection among physical, mathematical and computational contributions.
- **PHY.1 and PHY.2:** use the constructed physical account for similarity and analogue construction.
- **C.11.DUA:** decides whether resolving another physical uncertainty can improve the work enough to justify the inquiry.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-spec/contract/C-29-BB#root for balances; spec://ai.lev/fpf-think-mmp/contract/MMP-10#root for coupled equations; spec://ai.lev/fpf-spec/contract/C-29-2#root for computational formulation. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-think-phy/contract/PHY-10#root, spec://ai.lev/fpf-think-phy/contract/PHY-5#root, spec://ai.lev/fpf-think-phy/contract/PHY-7#root, spec://ai.lev/fpf-think-phy/contract/PHY-8#root @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-6
