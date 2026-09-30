# PHY.4 - Constrain an Unknown Physical Law by Transforming the Situation {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## PHY.4:1 - Problem frame {#problem-frame}

Use this pattern when an observed or proposed physical effect needs an account, but the interaction law is not supplied. A detailed mechanism may be unresolved and a familiar analogue may be inadequate. You can still ask how the situation could be changed, what would remain physically equivalent, and which responses those comparisons allow.

Start with one physical response or relation needed by the work. Describe its participants, preparation and relevant surroundings. Construct one comparison that could rule out a proposed dependence or restrict its form. A conditional restriction, together with the dependence it leaves unresolved, is a useful first result.

The method uses transformations justified for the physical situation: changes of position, orientation, scale, preparation, participant assignment or other relevant conditions. It combines their consequences with applicable dimensions, balances and dissipation. The question selects which of these contributions is useful.

You need enough physical understanding to propose the comparison and explain its conditions. Obtain an unfamiliar physical premise from a suitable account or collaborator. A qualitative comparison can already change the next move. The vector example additionally uses rotations and dot products; the chamber example uses elementary algebra and particle balance. Their branch-specific preparation belongs to those examples.

If an established interaction law already answers the question under the intended conditions, apply it. PHY.1 develops physical similarity across changed conditions, PHY.2 constructs a physical analogue, and PHY.3 derives a performance limit from permitted transformations. Return here when the unresolved contribution is the form of the interaction law itself.

## PHY.4:2 - Problem {#problem}

A formula can be easy to calculate with while admitting a physically impossible direction, an unjustified dependence or an omitted influence. Choosing the formula first can hide those differences.

Conversely, an appeal to symmetry or conservation can appear to determine a law while leaving important functions or parameters free. The task is to obtain the restriction that follows from the physical comparison and carry its remaining freedom into the next construction or inquiry.

## PHY.4:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Unknown mechanism and usable physical grounds | Partial knowledge can constrain the law, while a premise about an omitted influence can invalidate the constraint. |
| Changed description and changed experiment | Coordinates can change without changing the situation; changing the apparatus alone can alter its relation to the surroundings. |
| Strong restriction and remaining freedom | A direction, sign or balance can be established while the magnitude law remains unknown. |
| Idealized comparison and intended use | A conditional law family can guide work before all its physical premises have been resolved for an application. |

## PHY.4:4 - Solution {#solution}

**Local mantra:** recover the physical situation; construct its transformations; justify the comparison; restrict the relation; retain its unknown part; use the consequence or revise the premise.

### PHY.4:4.1 - Recover the participants and the relation being sought {#recover-the-participants-and-the-relation-being-sought}

Name what interacts, what is prepared, what can be exchanged and what response matters. Include surrounding bodies, material state, fields or boundaries when they can change that response. An omitted orientation or stored state may matter more than an additional numerical parameter.

Choose candidate quantities from that physical account. Explain how each quantity describes a participant, preparation or interaction. A.3.3.TR supports constructing a state that distinguishes different possible continuations; here the physical account supplies what retains and changes that state.

Decide what kind of relation is being proposed. An instantaneous mean response `y=F(x)` assumes that the chosen current inputs determine that mean. Memory, unresolved states or several possible responses can require a history, additional state, a probability law or a relation admitting several outputs. MMP.10 and MMP.11 express those mathematical choices after the physical conditions are identified.

Retain the status of the premises. A studied physical law, an idealization and a proposed hypothesis can all support reasoning, with different conditions on its use. Use the resulting conditional consequence when it already answers the present question.

### PHY.4:4.2 - Construct the transformation of the situation {#construct-the-transformation-of-the-situation}

Describe what happens to every relevant participant and condition under the proposed change. If an apparatus is rotated, what happens to gravity, nearby surfaces, an applied field and its preparation? If two participants are exchanged, which material properties and connections move with them?

Separate two comparisons:

- **Changed coordinates:** the same physical situation is expressed with different components or labels. Transform every quantity representing that situation consistently.
- **Changed physical situation:** participants or conditions are changed. Explain which physical premise predicts corresponding behavior in the new situation.

For an isotropic material, all spatial directions are physically equivalent under the stated conditions. An oriented material can also be described in rotated coordinates; its material direction must then rotate in the description. These are different premises for restricting a response.

Select the actual transformation class. A justified rotation condition supplies rotation consequences. Reflection, time reversal, scaling or exchange requires its own physical grounds when used. PHY.1 supplies the detailed work for a scaling comparison.

A thought comparison can be enough. When a physical premise is unsettled, identify a rival case that could make the responses differ. C.11.DUA helps decide whether resolving that difference is worth the work needed now.

### PHY.4:4.3 - Turn the comparison into a constraint on the unknown relation {#turn-the-comparison-into-a-constraint-on-the-unknown-relation}

Specify how inputs and responses transform. If x changes by T and y by U, a proposed response function has the comparison condition:

`F(T(x))=U(F(x))`.

For a reversible symmetry of a relation R, the corresponding condition is `R(x,y) iff R(T(x),U(y))`. This permits constraining an account before choosing a direction in which to solve it.

Derive the restriction. One useful move is to hold the input fixed under some allowed transformations. The output must then remain fixed under its corresponding transformations. Another is to compare inputs related by a transformation: a value chosen at one constrains the value at the other. MATH.13 develops these mathematical consequences once the physical action has been supplied.

For example, in three-dimensional space, rotations about a nonzero vector w leave w fixed. A vector response determined only by w and unchanged physical conditions must therefore lie along w: any perpendicular component would turn. Rotations between equal-length velocities then make the scalar coefficient depend only on their length. The physical work is establishing that no additional direction or state must also be supplied; :5.1 makes those assumptions explicit.

If a proposed input was held fixed even though the physical transformation changes it, restore that input and repeat the derivation. The anisotropic case in :5.2 shows how the changed argument opens additional response directions.

### PHY.4:4.4 - Combine applicable dimensions, balances and dissipation {#combine-applicable-dimensions-balances-and-dissipation}

Use the physical restrictions relevant to the requested consequence:

- **Dimensions:** terms combined as one physical quantity need compatible units. Determine the dimensions of remaining coefficients and arguments. PHY.1 supplies dimensionless similarity groups when scale is part of the question.
- **Balance:** account for the relevant quantity retained, transferred, supplied or lost across the chosen boundary. A flux entering and leaving a region can differ when the region stores the quantity.
- **Dissipation or passivity:** identify the exchange whose sign is constrained and the regime in which the constraint holds. For an instantaneous passive resistive force at relative velocity w, the mechanical power condition is `F(w) dot w <= 0`.

Derive each condition at its stated scope. A storage element can temporarily return energy that it received earlier; its instantaneous power need not satisfy the memoryless resistance condition. Including storage changes the applicable balance and inequality.

Combine the constraints and examine whether any candidate remains. If they conflict, return to the assumptions or allowed class that caused the conflict. If they leave several laws, express the unresolved function, parameter or state dependence. Symmetry and dimensions often narrow a family without selecting one member.

### PHY.4:4.5 - Obtain the needed consequence and choose the next use {#obtain-the-needed-consequence-and-choose-the-next-use}

Use the constraint for the original question. It may reject an impossible response direction, locate a missing input, restrict a learned or symbolic model, bound a consequence, or identify a condition under which competing laws disagree.

MMP.11 supplies a mathematical family respecting the physical constraints. When a quantitative value is needed, an interaction theory, interpreted observations or another appropriate method can constrain its remaining freedom. C.16.IR handles inference from interpreted indications; MMP.7 formulates a probability law for recorded data when the inference uses that form. C.29.2 supplies a computational formulation.

Choose further work from the unresolved consequence. A direction or family-wide bound may already suffice. If a missing magnitude changes the decision, obtain the needed contribution at a useful range and precision. A proposed experiment or simulation should discriminate something that matters to that next move.

When a changed situation gives a response outside the family, inspect the physical comparison before adding arbitrary terms. A preferred direction, external drive, stored state or different regime can change the family itself. Retain earlier consequences where their premises still hold.

## PHY.4:7 - Conformance Checklist {#conformance-checklist}

For the restriction being used:

- The physical response or relation, participants, preparation and relevant surroundings are recoverable.
- The transformation states what changes and what remains physically comparable.
- The mathematical input and output transformations follow that physical account.
- Each dimensional, balance or dissipation constraint has applicable physical premises.
- The derived consequence distinguishes what is constrained from what remains unknown.
- The result changes a construction, interpretation, prediction or next inquiry.
- A changed physical condition returns to the affected premise and constraint.

## PHY.4:9 - Consequences {#consequences}

Useful physical restrictions become available before a complete mechanism or fitted law is known. They can guide formulation, reject an incompatible model or direct a discriminating inquiry. The remaining freedom also becomes a specific task rather than an implicit assumption.

The result is conditional on the physical comparison. An added direction, stored state or changed regime can reopen the law family. This makes the dependence of the conclusion inspectable and supports retaining the portions that still apply.

## PHY.4:12 - Relations {#relations}

- **PHY.1** constructs physical similarity and scale-dependent comparisons.
- **PHY.2** constructs a physical analogue or proposed mechanism from interactions.
- **PHY.3** derives a physical performance limit from the permitted transformations.
- **MATH.13** derives mathematical consequences of a supplied symmetry.
- **MMP.10 and MMP.11** formulate compatible conditions and relations with unresolved dependence.
- **A.3.3.TR** supplies common state and joint-change construction.
- **C.29.1, C.29.2 and C.29.3** connect correspondence, computational formulation and physical realization.
- **C.16.IR and MMP.7** support interpreted indications and the probability law used for recorded observations.
- **C.11.DUA** compares the value and effort of resolving a remaining physical question.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-math/contract/MATH-13#root for a symmetry consequence; spec://ai.lev/fpf-think-mmp/contract/MMP-11#root for an unknown response family. @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-4
