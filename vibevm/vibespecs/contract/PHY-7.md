# PHY.7 - Obtain Motion from a Physical Variational Principle {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Usable, evolving
> **Normativity:** Normative

## PHY.7:1 - Problem frame {#problem-frame}

Use this pattern when you need to derive physical evolution from a principle that compares possible histories. The difficulty may be choosing the physical action, incorporating a constraint, or deciding which changes of a history the principle permits. A correct variation of the wrong physical formulation can give a precise but unusable equation.

The first result is an equation of motion, a boundary condition or a conserved consequence with the physical assumptions needed to use it. Sometimes the result is a particular unresolved interaction or constraint rule that must be supplied before the derivation can answer the question.

An *action* assigns a scalar to a history in the chosen physical description. *Stationarity* means that its first variation vanishes for the specified allowed changes. The physical theory supplies the reason to impose that condition. MATH.10 supplies the mathematical reasoning about variations; this method constructs and interprets its physical premises.

You need to identify the physical quantities and understand the proposed principle's range. You also need enough mathematical preparation to interpret a variation, or another contributor who can perform it and explain its result. The examples use elementary constrained mechanics, a charged particle and a continuous field. Their branch-specific laws are stated in the cases.

Use an existing equation or PHY.6's balances and response laws when they already answer the question economically. A variational formulation is useful when it simplifies constrained motion, carries interactions across coordinate changes, exposes a symmetry, or produces both interior and boundary equations. It need not be constructed for every physical problem.

## PHY.7:2 - Problem {#problem}

Writing `L=T-V` and applying the Euler-Lagrange formula leaves important physical work hidden. Which interactions are represented by the potential? Does a moving support contribute to the velocity? Which endpoint quantities are fixed? Can the constraint really be imposed on every varied history?

These choices can change the resulting motion. A missing velocity-dependent interaction can leave the energy apparently reasonable while removing a force. Discarding a boundary term can replace a loaded boundary by a free one. Extending a rule for position constraints to a different kind of constraint can select a different evolution.

## PHY.7:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Compact principle and physical content | One scalar can generate several equations, but every consequential interaction still needs a physical basis. |
| Convenient coordinates and retained motion | Eliminating a constraint can simplify the calculation while concealing a moving support or an omitted degree of freedom. |
| Interior equations and boundaries | Integration by parts exposes both; the physical preparation decides which boundary variations remain free. |
| Mathematical comparison and physical evolution | Nearby histories define a variation; the predicted motion is selected and used with its own preparation. |
| Reusable formalism and cost | A common derivation helps repeated changes, while a direct balance may obtain one consequence with less work. |

## PHY.7:4 - Solution {#solution}

**Choose the physical principle → represent the histories and interactions → state the allowed variations → derive the interior and boundary conditions → interpret the consequence → revise the implicated premise.**

### PHY.7:4.1 - Choose a principle for the physical question {#choose-a-principle-for-the-physical-question}

State the consequence needed and the physical situation it concerns. Choose the retained participants, interactions and regime. PHY.5 helps decide which physical detail matters.

Recover an applicable variational principle from the physical theory, or propose one with a stated physical basis and conditional use. Identify what it assigns to a history and what property the realized history is required to have. A stationary action, minimum energy at equilibrium and a dissipative variational rule impose different conditions. Select the one appropriate to the question.

For a smooth classical configuration history `q(t)`, a common form is

`S[q] = integral from t0 to t1 of L(q,qdot,t) dt`,

where `L` is the Lagrangian. A field description can instead integrate a density over space and time. The following steps show how to use such a principle; another physical principle can require a different functional or variation rule.

If the action or its physical grounds are missing, identify the interaction or assumption needed to construct them. A balance with a response law may settle the immediate question while the variational formulation remains open. The availability of a differentiation tool does not resolve that physical choice.

### PHY.7:4.2 - Construct the histories and their action {#construct-the-histories-and-their-action}

Choose coordinates or fields that represent the retained physical configuration. State how they recover the physical quantities needed by the question. Include the time dependence of that recovery: for a position `r=F(q,t)`, velocity is `r_dot=F_q*qdot+F_t`. The second term describes motion of the chosen mapping, such as a moving support.

For a classical mechanical description with the appropriate conservative interactions, construct kinetic energy from those velocities and potential energy from the interactions, then use `L=T-V`. Check the interaction rather than infer this form from the word *energy*. A velocity-dependent coupling, a dissipative interaction or an eliminated environment can require another term or another principle.

Keep relevant boundary contributions. Stored energy at an endpoint, an imposed load and a fixed endpoint are physically different. A field's action can contain an interior density and separate surface or endpoint terms.

When reducing coordinates, retain how the discarded quantities or reactions can be recovered if needed. If the reduction loses a physical effect important to the question, return to PHY.5; MMP.9 handles the mathematical reduction once its physical premises are chosen.

### PHY.7:4.3 - State what may vary and what must remain fixed {#state-what-may-vary-and-what-must-remain-fixed}

Specify the interval, endpoint conditions, constraints and regularity used in the comparison. For the ordinary fixed-endpoint principle, take `q_epsilon=q+epsilon*eta`, with `eta(t0)=eta(t1)=0`. A position constraint requires a family that preserves that constraint, or a justified multiplier formulation. MATH.10 distinguishes a finite admissible family from a tangent calculation valid only to first order.

The endpoint values used to derive an equation need not be known future observations. Fixing them in the variation removes its endpoint contribution. After deriving the local evolution equation, an initial-value use supplies compatible initial position and velocity; it does not add a guessed final position as another condition.

Distinguish position constraints from restrictions on velocity that cannot be integrated into position constraints. For such a restriction, varying entire constrained histories and requiring zero work of ideal reactions on selected instantaneous virtual displacements can give different equations. A *virtual displacement* here is a comparison of configurations at one fixed time used to state that reaction condition. Obtain the reaction or allowed-variation rule from the physical constraint model before using either construction.

For example, an ideal reaction model for `A(q,t)*qdot+b(q,t)=0` may prescribe zero reaction work on displacements satisfying `A*delta_q=0`. Generalized forces Q are defined by their virtual work, `delta W=Q dot delta_q`. The Lagrange-d'Alembert equations then have the form `d/dt(L_qdot)-L_q=Q+A^T*lambda`, together with the velocity constraint; here Q contains the other forces and `lambda` determines the reactions. This result uses the ideal-reaction premise. Simply putting the velocity constraint into an action with a multiplier is a different construction and need not reproduce it. Use PHY.6 when the balance and reaction description is the sufficient route.

### PHY.7:4.4 - Derive the interior and boundary conditions together {#derive-the-interior-and-boundary-conditions-together}

Apply MATH.10 to the allowed family. Vary the complete action, including dependent quantities and boundary terms. For the smooth finite-dimensional form above, integration by parts gives

`delta S = [L_qdot dot eta] at t0,t1 + integral (L_q-d/dt(L_qdot)) dot eta dt`.

With fixed endpoints and otherwise arbitrary interior variations, stationarity gives `d/dt(L_qdot)-L_q=0`. With restricted variations, derive the condition supported by that restricted family. Retain force terms when the selected principle includes their virtual work.

For a field, perform the corresponding integration in space as well as time. First identify the boundary terms, then decide which vanish because the boundary value is prescribed and which produce a condition because its variation is free. An endpoint force or boundary energy can change the latter condition without changing the interior equation.

Differentiate symbolically or computationally when helpful, but retain the variables held fixed and the substitution rules. A result from varying only part of the action answers that smaller calculation. It does not justify omitting a physical term.

Stationarity alone does not establish a minimum. Use the stronger comparison only when required and supported. MATH.10 gives both a minimizing free-particle case and a stationary oscillator history with changes of either sign in the action.

### PHY.7:4.5 - Recover the physical consequence and preparation {#recover-the-physical-consequence-and-preparation}

Interpret the equations in the original physical quantities. Supply the independent initial, boundary and driving conditions needed for the intended use. Check their compatibility with constraints. An equation of motion can be the sufficient first result; obtaining a trajectory or a peak can require the subsequent computation in C.29.2.

Derive a conservation claim from the applicable symmetry and its conditions. For the ordinary unconstrained Lagrangian with no additional generalized force, absence of a coordinate from L gives a constant corresponding `L_qdot`. Absence of explicit time dependence gives a constant `qdot dot L_qdot-L`. Interpret these expressions physically; a velocity-dependent interaction can make a canonical momentum differ from mass times velocity. MATH.13 supplies the broader symmetry-to-consequence reasoning and PHY.4 supplies the physical grounds for the symmetry.

Use a discriminating comparison when it can change the result's use. A force balance can reveal a missing coupling; boundary work can reveal an omitted load; a change of coordinates can expose a missing velocity term. Agreement establishes that comparison under its premises. It does not independently validate the physical principle.

### PHY.7:4.6 - Return through the premise that changed {#return-through-the-premise-that-changed}

When an interaction changes, revise its action term or force contribution. When a support or boundary changes, revise the histories, velocity mapping and allowed variations before reusing the equations. When a coordinate description changes, transform the whole expression while keeping the physical history recoverable.

Equivalent expressions can describe the same motion. In the ordinary fixed-endpoint principle, adding `dF(q,t)/dt` changes the action only by endpoint values, so it preserves the interior equations. A use with different endpoint freedoms must also carry the changed boundary term. Distinguish this redescription from introducing another physical interaction.

If a computed consequence fails, locate whether the fault is the physical principle, admissible comparison, mathematical derivation or obtaining procedure. B.5.MPC.R provides the combined return. Seek additional physical evidence only where its possible result could alter the decision or action; a useful conditional derivation can already be used with its stated limits.

## PHY.7:7 - Conformance Checklist {#conformance-checklist}

- The selected physical theory or stated hypothesis supplies the principle and its range.
- Coordinates or fields recover the needed physical quantities, including time-dependent mappings.
- The action includes consequential interactions and boundary contributions.
- Allowed variations and constraints follow the selected physical principle; endpoint restrictions are explicit.
- Interior, force and boundary terms produce the conditions actually used.
- The interpreted result retains compatible preparation and the reach of its stationarity or conservation claim.
- A changed interaction, constraint or representation returns through its affected contribution; further inquiry serves a consequential question.

## PHY.7:9 - Consequences {#consequences}

A useful physical principle can organize several coupled equations and expose what changes when coordinates, constraints or boundaries change. The calculation can be shared with a mathematical specialist or a symbolic tool while the physical premises remain inspectable.

The compact formulation does not remove the need for physical knowledge. Constructing a justified action can be harder than writing a balance. An equation derived from it may still require substantial work to solve or to connect to observation. Stop at the consequence sufficient for the current work and retain unresolved physical choices in any conditional use.

## PHY.7:12 - Relations {#relations}

- **MATH.10:** constructs admissible variations and establishes the reach of the resulting condition.
- **PHY.4, PHY.5 and B.5.TU:** supply physical symmetry grounds, retained detail and use of a theory in a case.
- **PHY.6 and C.29.BB:** provide balance and response constructions for an alternative derivation or a discriminating comparison.
- **MATH.13:** derives a mathematical consequence from symmetry; this method supplies the physical action and its admissible symmetry.
- **MMP.9, MMP.10 and C.29.2:** reduce or formulate the resulting mathematical problem and obtain the needed consequence.
- **B.5.MPC:** connects the mathematical result and its conditions to the physical question.
- **B.5.MPC.R:** revises a failed physical, mathematical or computational contribution and its affected uses.
- **C.11.DUA:** selects further inquiry when resolving the uncertainty can improve the work enough to justify its cost.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): spec://ai.lev/fpf-think-math/contract/MATH-10#root for mathematical variation; spec://ai.lev/fpf-think-phy/contract/PHY-6#root for the direct balance alternative. @status:spec/done

#source spec://ai.lev/fpf-think-phy/source/PHY-7
