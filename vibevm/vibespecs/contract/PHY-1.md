# PHY.1 - Construct Physical Similarity Across Changed Conditions {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative within the stated use

## PHY.1:1 - Problem frame {#problem-frame}

Use this pattern when you want to learn about a physical situation through another arrangement, but changing its size, material, speed or surroundings changes the effects that produce the answer. You may be designing a smaller experiment, comparing observations made under different conditions, or deciding which part of a previous physical result can be reused.

Start with the quantity or behavior you need to infer about the original situation. Then identify one physical effect whose relative importance could change in the proposed comparison. A smaller object has less weight, for example, but its ability to carry that weight changes by a different factor. That difference can determine how the comparison should be built and loaded.

The result is a set of physically compatible comparison conditions, a justified transfer of a selected result, or a conflict that directs the next construction. Here **physical similarity** means correspondence of the physical behavior needed by the question under stated changes of scale or conditions. Geometric similarity preserves shape under scaling; further conditions can be needed to preserve the relevant behavior.

You need the physical account used in the comparison and the mathematics needed to transform its relations. You can develop that account through B.5.FM and B.5.TU or obtain a missing physical contribution from a collaborator. Algebra and ratios suffice for many first comparisons; fields and time-dependent behavior can require differential equations. A ready comparison whose conditions fit the question can be used directly. If the problem is expressing an already understood account mathematically, MMP.10 supplies that formulation work.

## PHY.1:2 - Problem {#problem}

A physically different experiment can resemble the original while answering a different question. Keeping shape preserves length ratios. It can still change the competition between weight and strength, inertia and friction, propagation and absorption, or reaction and transport. An experiment that preserves a final value can also change the path by which that value is reached.

The difficulty is constructing the conditions of a useful comparison. A familiar dimensionless number can help, but selecting it requires knowing which physical effects it compares. Several relevant conditions can demand incompatible changes to the same material or control. The requested result determines whether that conflict must be removed or whether a more limited comparison will suffice.

## PHY.1:3 - Forces {#forces}

| Choice | What it changes |
| --- | --- |
| Whole behavior or one output | Reproducing one displacement or threshold can require less than reproducing the complete field or time history. |
| Smaller experiment or unchanged balance of effects | Length, area and volume scale differently; material properties and preparation may need to change too. |
| Useful simplification or an omitted mechanism | Removing a small contribution simplifies the comparison, but its effect can accumulate or control behavior near a transition. |
| Mathematical settings or available physical means | Equations may require material properties or forcing that the proposed apparatus cannot supply together. |
| One matched experiment or several complementary results | Combining calculations and observations can answer a question that no single scaled arrangement reproduces. |

## PHY.1:4 - Solution {#solution}

**Choose the result to transfer → recover its physical causes and conditions → express their relative contributions → construct compatible comparison settings → resolve consequential mismatches → use the result and revise it when the question changes.**

### PHY.1:4.1 - Choose the physical result and the proposed change {#choose-the-physical-result-and-the-proposed-change}

Name the original arrangement and the comparison arrangement. Say what each does and what the comparison is intended to reveal. Distinguish a proposed experiment from an observed one.

Specify the result at the detail needed for its use: total extension under a load, the location of a maximum, a response after a stated duration, or a distribution of repeated outcomes. Include the location, interval and preparation when they affect that result. A request for average deformation differs from a request for deformation at every point.

Identify what may change between the arrangements and what is fixed by the proposed work. The available fluid, gravitational acceleration, material, instrument range or support can constrain the construction. A control may be a time history rather than one setting. Preserve any known dependence between settings: changing temperature can alter both viscosity and density.

If the existing physical account already yields a sufficient answer, use it. Constructing another experiment is worthwhile when it supplies a contribution the work still needs. C.11.DUA helps choose between acting on a sufficient answer and obtaining more information.

### PHY.1:4.2 - Recover the interactions that can change the requested result {#recover-the-interactions-that-can-change-the-requested-result}

Follow the physical route by which the proposed input affects the output. Identify the participants, interactions and constraints on that route. Include an exchange across the chosen boundary when it contributes to the result. In a deformation problem, distinguish the force applied at an end from weight distributed through the body. In a transport problem, distinguish material carried by motion from material spread by diffusion.

Use the applicable theory to express those contributions. B.5.TU supplies the passage from theory to the encountered case; A.3.3.TR helps when several interactions determine the same evolving state. State the physical premises still needed rather than filling an unknown interaction with a convenient equation.

Estimate the relative size or time scale of competing effects. Derive that comparison from their laws: which quantity multiplies each term, and what spatial or temporal variation makes the term large? In a regime where one effect is negligible for the output, retain the reason for that simplification and the conditions under which it can fail.

Bring the preparation into the same account. Geometry, contacts, constraints and initial conditions can alter the solution even when the material equations are unchanged. For a field, a boundary condition applies over a surface or interval; matching its value at one point may leave the intended problem different elsewhere.

### PHY.1:4.3 - Express the comparison through meaningful scales {#express-the-comparison-through-meaningful-scales}

Choose reference quantities from the physical question. A reference length might be a gap rather than the total apparatus length; a response time might be compared with the duration of forcing. Explain that choice in the working terms.

For a quantity q, choose a positive reference magnitude Q with the same units and write `q=Q*q_hat`. The number q_hat is its value in that scale. When the law concerns a difference from a reference q0, use `q=q0+Q*q_hat` and carry q0 through the substitution. This matters, for example, when an absolute pressure and a pressure difference enter different relations.

Substitute the scaled quantities into the physical relations. Transform derivatives and integrals too: if `x=L*x_hat` and `t=T*t_hat`, then a time derivative contributes a factor 1/T and a spatial derivative a factor 1/L. Divide each equation by an appropriate nonzero reference contribution. The remaining coefficients show which relative effects must be compared.

For example, in a flow whose speed varies by order U over distance L, characteristic inertial acceleration is `U^2/L`, viscous acceleration is `nu*U/L^2`, and gravitational acceleration is g. Their ratios to the inertial contribution are `nu/(U*L)` and `g*L/U^2`. These ratios compare physical terms. A different physical account can introduce another contribution and another condition.

Scale the geometry and preparation as well as the equations. A prescribed forcing history is compared at corresponding scaled times; a boundary profile at corresponding scaled positions. Keep a separately imposed forcing duration as an independent condition unless the work makes it proportional to the chosen response time.

For many quantities, dimensional analysis can construct dimensionless combinations systematically. Choose a combination whose physical interpretation makes the comparison useful. MATH.11 supports the construction of quantities unchanged by stated transformations. Dimensionless dependence still needs the physical premises that selected the quantities and relations; it can leave an unknown function to be obtained through MMP.11 or other subject work.

### PHY.1:4.4 - Construct settings that supply the needed correspondence {#construct-settings-that-supply-the-needed-correspondence}

Write the original and proposed dimensionless relations together. Set equal the coefficients and preparation features needed by the intended transfer, then solve these conditions jointly with the available physical settings. MMP.10 supplies the constraint formulation when several choices interact.

The result may be a recipe: change length by one factor, forcing by another and reading time by a third. Check that the selected properties describe an available material or realizable arrangement. A material's stiffness and density, for example, may not be independently adjustable. Changing a support or adding a mass changes the physical account as well as a number.

When the scaled equations, domains and preparation coincide, express how a solution in the comparison variables becomes a solution of the original model. Include the output scale. C.29.1 supplies that transfer argument. If the model permits several solutions, the correspondence relates the permitted solutions; identifying one realized history requires the relevant physical preparation or selection conditions. Statistical predictions require the corresponding statistical account.

For a question about one output, try a weaker construction when reproducing the whole problem is unnecessary. Derive how that output depends on the settings and match the dependence needed by the question. Additional loading can reproduce total extension without reproducing local strain, as :5.2 shows. Keep the resulting comparison tied to the output it determines.

### PHY.1:4.5 - Resolve a mismatch by its effect on the answer {#resolve-a-mismatch-by-its-effect-on-the-answer}

If the conditions conflict, identify which physical contribution changes and how that could change the requested result. The conflict can itself rule out the proposed experiment at the chosen settings.

Choose the next move from the remaining physical possibilities. You can change a free setting, construct a different arrangement, retain a simpler physical regime, or derive how the unmatched contribution modifies the output. If several mismatched experiments are to be combined, construct the relation that permits that combination; a fitted relation retains its assumptions and the range over which it can be used. MMP.9 and MMP.11 can supply reduction and constrained model construction for these returns.

A small coefficient can support an approximation when its influence on the output is controlled. Inspect where that argument could fail. Thin boundary layers, a threshold, resonance or a long observation interval can make a nominally small contribution consequential. Derive a useful bound, compare an applicable limiting solution, or obtain a discriminating observation when it can settle the use. C.29.1 carries a bound through the later inference.

Use an existing result when it resolves the mismatch at the required strength. A conditional result or a limit can be enough. Additional measurement is selected by what its possible answers would change, including its cost, through C.11.DUA.

### PHY.1:4.6 - Use the comparison and follow a changed question {#use-the-comparison-and-follow-a-changed-question}

Translate the obtained result into the original quantity, position and time. State the physical conditions on which that translation depends. A short derivation can supply the whole explanation; another contributor needs only the settings, correspondence and unresolved premises that change their use.

If a material experiment performs the comparison, include the effects of preparing, driving and reading it where they affect the inference. C.29.3 supplies this connection when the physical evolution performs a computation. A numerical solution has its own discretization and calculation errors under C.29.2. Keep those errors separate from a changed physical mechanism.

For a changed question, revisit the result first. Asking about a different location, time, range or intervention can make a previously omitted contribution relevant. Retain the conditions that still apply and reconstruct the affected comparison. B.5.MPC.R helps locate a failure across the physical account, mathematical representation and computation.

The useful continuation can be a proposed experiment, a design choice, an interpreted observation, a narrower claim or a new physical question. When the comparison suggests a different way for a team to obtain its result, use ME.7 to describe the proposed operations and their relations. ME.12 checks the claims on which that composition and its description rely and returns a correction to the affected contribution.

## PHY.1:7 - Conformance Checklist {#conformance-checklist}

- The original question identifies the result and the proposed physical change.
- The relations and preparation contain the effects that can alter that result, with unresolved physical premises visible where used.
- Reference scales have physical meanings and compatible units; substitution covers the relevant spatial and temporal conditions.
- The comparison settings satisfy the required conditions together and can be supplied by the proposed arrangement, or their unresolved feasibility is stated.
- A limited or distorted comparison has a derivation or bound for the output it is used to answer.
- The result is interpreted at the original scale, with any preparation, computation and readout losses that change its use.
- A changed question returns to the affected physical contribution; an already sufficient result is used without compulsory extra experiments.

## PHY.1:9 - Consequences {#consequences}

The construction can reveal an impossible experiment before equipment is built. It can also identify useful freedom: a different load, medium, time scale or restricted output may supply the answer with less work. A failed similarity condition becomes a physical design question rather than an unexplained disagreement between experiments.

The price is making the physical premises and coupled settings explicit. A complex account can require several comparisons or a numerical analysis. The method can reduce that work by selecting a sufficient output, but it cannot supply a missing physical law from dimensional consistency alone.

## PHY.1:12 - Relations {#relations}

B.5.FM and B.5.TU supply first-model construction and theory use when the physical account is still being formed. A.3.3.TR supplies state and the joint representation of change. B.5.MPC connects the physical, mathematical and computational contributions; B.5.MPC.R locates a failed connection after a change.

MMP.10 formulates coupled conditions; MMP.11 constructs unknown dependence; MMP.9 derives reduced evolution where eliminating detail exposes an unresolved contribution. MATH.11 constructs invariants from transformation rules. C.29.1 supplies the mathematical transfer or bound, C.29.2 the computation, and C.29.3 its realization through physical action and readout.

C.11.DUA selects further inquiry by what it could change and what it costs. ME.7 develops the proposed composition of the working method; ME.12 checks its claims and description when the comparison changes how participants obtain a result.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-phy/contract/PHY-5#root for consequential omitted effects; mathematical methods for the resulting comparison. @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-1
