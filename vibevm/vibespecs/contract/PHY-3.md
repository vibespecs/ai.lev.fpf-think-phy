# PHY.3 - Derive a Physical Limit from Permitted Transformations {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative within the stated use

## PHY.3:1 - Problem frame {#problem-frame}

Use this pattern when you need to determine what a physical process or device could accomplish before choosing its detailed mechanism, or when a familiar physical prohibition appears to rule out a proposed change. A candidate may have an acceptable energy balance yet require an unavailable preparation, consume a resource that was omitted, or perform differently on inputs that one device is supposed to handle.

The first useful result is a necessary condition on the requested performance, a conditional exclusion of a class of proposals, or a changed premise that opens a different construction. You obtain it by describing the complete physical transformation and constructing a comparison that the applicable physical laws constrain. “Permitted” here means allowed under those physical premises.

You need a working description of the requested effect, the resources and surrounding systems it may use, and the physical principles relevant to that effect. A qualitative argument can suffice. A quantitative result also needs the quantities and mathematical operations in its chosen comparison. The two worked cases require different preparation: energy exchanges and elementary ratios in the first, state vectors and inner products in the second. Obtain an unfamiliar physical premise or calculation from a suitable source or collaborator and retain the conditions on which its answer depends.

When an established bound already answers the same question under the same physical conditions, apply it directly. A measurement of a particular device, estimation of an unknown parameter and design of a mechanism have their own methods. Return here when their result changes the allowed transformation or the reach of a physical restriction.

## PHY.3:2 - Problem {#problem}

A physical proposal usually names the desired effect more readily than the whole change needed to produce it. “Return the machine to service,” “copy an input” and “extract more work” can leave different resources, input families and end conditions implicit. Those differences determine which physical restrictions apply.

Detailed calculation of one design can reveal its failure while leaving other designs available. Conversely, a quoted limit can be applied outside its premises and suppress a useful construction. The difficulty is to derive a restriction whose physical description covers the proposals being considered, and then use it to decide what to change or investigate.

## PHY.3:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Reach across mechanisms | A bound can guide many designs, but its description must cover every design to which the conclusion is applied. |
| Complete physical change | Preparation, surroundings and restoration can determine the result; describing every microscopic detail would make the first inquiry unusable. |
| Admissible comparison | A simple reference can expose a strong limit, while a mathematically convenient inverse may require a physical operation that is unavailable. |
| Useful idealization | A larger class of ideal operations can yield a bound on real devices; an omitted physical contribution can invalidate that inference. |
| Continued construction | An obstruction can redirect work immediately, while removing that obstruction leaves further realization questions. |

## PHY.3:4 - Solution {#solution}

Construct the complete proposed transformation, identify the physical restrictions shared by its candidate mechanisms, and use an admissible comparison to derive their consequence. Keep the requested performance and its physical conditions attached to the result. Revisit the premise that matters when the resources, input family or required performance changes.

### PHY.3:4.1 - Specify the physical change and what must remain usable {#specify-the-physical-change-and-what-must-remain-usable}

Start with the proposed input and output. Include the range of inputs and the performance required on them. For a machine expected to handle an unknown input, ask whether one fixed arrangement must work throughout that range or whether the arrangement may be chosen after learning the input. For fluctuating processes, distinguish a guarantee on every run from an average or an allowed failure probability. MMP.8 supplies that formulation when the choice or information condition is difficult.

Follow the resources that can participate in the transformation: material, energy, prepared states, information about the input, external controls and connections to the surroundings. Describe their relevant initial and final conditions. A charged auxiliary, a memory that accumulates records and an initially correlated pair can be consumed resources even if the visible output is unchanged. Use the physical theory to decide which such differences matter to the proposed restriction.

For repeated operation, state what the device must remain able to do. Return to an identical state is needed only when the requested operation or the physical argument requires it. If the construction uses a reset, include its physical change and resource use. A device that still performs the next operation can have changed state; a device restored in one observed variable can have exhausted another needed resource. A.3.3.TR helps choose a sufficient state description where these cases are unresolved.

The result is a physical transformation with its allowed side effects and input conditions. Keep an unspecified preparation visible as an unresolved premise. It can be useful to derive a conditional bound before that premise is settled.

### PHY.3:4.2 - Establish which physical restrictions cover the candidate mechanisms {#establish-which-physical-restrictions-cover-the-candidate}

Select the physical account that connects the requested change with a conserved quantity, an ordered change, a preserved relation or another necessary condition. State its regime and the systems to which it applies. A local balance law can require a larger boundary when something crosses it; a law for a closed process can require explicit surroundings when the proposed device exchanges matter or information.

Explain why every device in the proposed conclusion admits the chosen description. MMP.10:4.4 supplies this coverage requirement. Physically, it can mean including a reservoir and its controller, representing an unobserved auxiliary, or admitting all interactions allowed by the theory instead of only one circuit. Restrict the conclusion to the designs described if this coverage remains incomplete.

An enlargement of the allowed class can make exclusion easier: if even a class with additional resources cannot realize the requested transformation, its contained class cannot do so. Show that containment. An approximation chosen because it is easy to calculate does not automatically give such an enlargement; it can remove a coupling or noise source that changes what is possible. When only an approximate account is justified, propagate a suitable error allowance or retain a conditional result at that model's stated scope.

Use B.5.TU to recover the physical theory's premise and its consequence for the case. The output of this step is the applicable restriction and the reason it covers the proposed physical class. Further measurement is useful only if its possible result changes that premise or the next choice; C.11.DUA helps resolve a consequential uncertainty about that effort.

### PHY.3:4.3 - Construct a comparison that exposes the restriction {#construct-a-comparison-that-exposes-the-restriction}

Choose the operation that fits the available physical structure. The following two constructions address different situations and can be used independently.

**Compose with a reference and cancel selected changes.** Use this when an admitted reference process exchanges the relevant quantities or restores a needed condition. Choose the part of the proposal you want to eliminate from the combined account, then determine the reference's direction, amount and preparation that match it. Establish that the reference can perform that operation under the same connecting conditions. For example, two processes may exchange equal energy but require incompatible temperatures, pressures, phases or forms of delivery. Numerical equality alone cannot establish the physical connection.

Combine the proposed and reference operations, including their auxiliaries. Cancel only the matched exchanges or restored states; keep all remaining changes. C.29.BB supplies the accounting for additive quantities. Apply the physical restriction to the composite. If it would have a prohibited net effect, derive the inequality or condition on the original proposal that avoids that effect. A reference may be an ideal process admitted by the theory; building it in a laboratory is unnecessary for this conditional argument. Using the inverse in an equation still requires a reason that the needed physical reverse process is admitted.

**Compare inputs of the same operation.** Use this when one device must perform the requested transformation on a family of inputs and a physical law relates its actions on different inputs. Select inputs whose relation can expose the limitation. Write their proposed outputs, including allowed auxiliary outputs, while holding fixed the device and its input-independent preparation. Derive the relation the law requires between those outputs. If the requested outputs violate it, the common device cannot provide them under the stated conditions.

An auxiliary output may depend on the input even when the initial preparation cannot. Allow that dependence in the comparison. Requiring the auxiliary to return to a fixed state when the proposal permits a changed state would prove a narrower restriction. Conversely, choosing a different apparatus separately for each input would answer a different question from the fixed-device requirement.

These constructions can reveal a remaining physical premise rather than a bound. Name that premise and what supplying it would enable. Forcing either comparison when its connection conditions or input relation are absent adds no physical result.

### PHY.3:4.4 - Derive the consequence with every remaining physical change included {#derive-the-consequence-with-every-remaining-physical-change}

Carry the quantities, signs, state conditions and input relations through the chosen comparison. Interpret each term by the physical contribution it represents. Check that the canceled effects have compatible units and conditions, and that the uncanceled effects describe the complete remaining process.

Obtain the requested inequality, an excluded transformation, or the unresolved condition on which either result depends. When using a mathematical invariant, MATH.11 supplies the derivation from the admitted transformation rules. When a numerical tool performs the algebra, retain the symbolic relation or a sufficient explanation that lets another participant inspect what the computation establishes. C.29.2 and C.29.3 govern a computation whose formulation or realization needs further work.

Distinguish a necessary bound from attainability. A proposed device can satisfy one physical restriction and still fail another, or approach a theoretical limit only as time or another resource grows. The useful output at this step says which candidates have been excluded, which remain under consideration, and which premise or construction controls the next question.

### PHY.3:4.5 - Change the proposal at the premise that controls the result {#change-the-proposal-at-the-premise-that-controls-the-result}

Return the physical consequence in the terms of the working question. For a proposal outside the bound, identify a consequential change: supply a previously forbidden resource, allow a side effect, narrow the input family, relax precision or reliability, or change the condition for reuse. Derive the affected comparison again for the chosen change. Keep the original result for its original premises.

When the obstruction disappears, continue with a mechanism, an approximation or another limiting principle. PHY.2 can help construct a physical analogue for that inquiry; PHY.1 supplies physical similarity if transferring between regimes is the next difficulty. If the new question concerns an unfamiliar mathematical construction, obtain that contribution from Mathematical Thinking. B.5.MPC helps divide and reconnect those contributions across people and AI agents.

Stop the present derivation when its result is sufficient for the next decision. Further information or a physical trial is a separate action whose value depends on what remains unresolved. A concise explanation of the compared transformation and controlling premise is enough when it allows the intended user to continue.

## PHY.3:7 - Conformance Checklist {#conformance-checklist}

- [ ] The requested physical effect includes its input family, performance criterion and relevant preparation.
- [ ] Consumed resources, surrounding systems and any required restoration or continued capability are included where they affect the restriction.
- [ ] The selected physical account has a stated regime and a reason to cover the device class in the conclusion.
- [ ] The comparison uses compatible admitted reference operations, or the same operation on inputs linked by the physical law.
- [ ] The derivation retains uncanceled changes and allowed auxiliary outputs.
- [ ] The result distinguishes the derived necessary condition or exclusion from the still-needed realization.
- [ ] The explanation shows which changed premise would require another derivation and what the current result enables next.

## PHY.3:9 - Consequences {#consequences}

A useful physical limit can be obtained before the internal mechanism is known. It can reduce unproductive design work, expose an omitted resource, or suggest a different input family or performance requirement. The derivation also gives collaborators a physical question to answer: a needed reference process, a covering law or an unsettled preparation.

The cost is obtaining a physical account whose reach matches the conclusion. Stronger exclusion usually needs broader coverage than failure of a candidate design. A conditional result is often sufficient to guide the next step while that coverage is developed. Near a limiting value, finite time, noise, size and implementation constraints can determine whether pursuing it is useful.

## PHY.3:12 - Relations {#relations}

- **B.5.TU and B.5.MPC** supply theory-to-case use and division and reconnection of mathematical, physical and computational work. **B.5.QD** helps develop the next question from an obtained limit or obstruction.
- **A.3.3.TR** supplies a sufficient state description and representation of interacting changes. **C.29.BB** supplies boundary accounting and cancellation for additive quantities.
- **MMP.8 and MMP.10** supply information-conditioned choice, constraint formulation and the coverage requirement for a class-wide conclusion. **MATH.11** supplies mathematical invariant construction and use.
- **PHY.1** supplies physical similarity when the comparison must cross regimes; **PHY.2** constructs a physical analogue for the continuing mechanism question.
- **C.29.1-C.29.3** govern mathematical correspondence, computational formulation and realization where those are unresolved. **ME.7** develops a proposed composition of the work method using the physical result; **ME.12** checks the claims in that account and its description. **C.11.DUA** helps decide whether an additional inquiry can change the useful next action.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-spec/contract/C-29-BB#root for balances; spec://ai.lev/fpf-think-math/contract/MATH-11#root/.20 for invariants or bounds; spec://ai.lev/fpf-think-phy/contract/PHY-2#root for another physical construction. @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-3
