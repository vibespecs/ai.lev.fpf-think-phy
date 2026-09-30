# PHY.6 - Construct Physical Evolution from Balances and Response Laws: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.6:5 - Archetypal Grounding {#archetypal-grounding}

### PHY.6:5.1 - Derive coupled motion and identify where mechanical energy goes {#derive-coupled-motion-and-identify-where-mechanical-energy-goes}

Two bodies move along one line. Their masses are `m1` and `m2`. Displacements `x1` and `x2` are measured from a configuration in which their connecting spring is unstretched, so its extension is `x2-x1`. Velocities are `v1` and `v2`. A spring and a viscous damper act between them; the connector's inertia is neglected in the chosen regime.

The momentum balances need the connecting force. Use the ideal response

`f = k*(x2-x1) + c*(v2-v1)`,

where `k>0` is stiffness and `c>=0` is damping. The force on body 1 is `f`; that on body 2 is `-f`.

**When a response parameter is missing.** Suppose this linear response form is already justified, but its parameters are not yet supplied. A static test with extension `1 m`, zero relative velocity and force `3 N` determines `k=3 N/m`; it leaves c undetermined. At extension `1 m` and relative velocity `-2 m/s`, the choices `c=0` and `c=0.5 N*s/m` predict `3 N` and `2 N`. Both reproduce the static test. A prediction of either body's acceleration therefore remains conditional on c; a supplied value or useful bound can settle a stronger question. A question about total momentum change can already be answered from the external forces, independently of c. The single test does not establish the assumed linear form.

With the response parameters and external forces `u1` and `u2` supplied, the connected evolution is

`x1' = v1;  x2' = v2;  m1*v1' = f+u1;  m2*v2' = -f+u2.`

Adding the momentum balances gives `p' = u1+u2` for `p=m1*v1+m2*v2`. This removes the internal force from the total momentum change while retaining it in the relative motion.

The retained mechanical energy is

`H = (m1*v1^2 + m2*v2^2 + k*(x2-x1)^2)/2.`

Differentiating and substituting the evolution gives

`H' = u1*v1 + u2*v2 - c*(v2-v1)^2.`

For the ideal damper whose lost mechanical energy becomes internal energy `U`, add `U' = c*(v2-v1)^2`. Then `(H+U)'` equals the external mechanical power. Omitting `U` from the motion calculation assumes that its change does not appreciably alter the chosen mechanical response.

Take `m1=1 kg`, `m2=2 kg`, `k=3 N/m`, `c=0.5 N*s/m`, `x1=0 m`, `x2=1 m`, `v1=1 m/s`, `v2=-1 m/s`, and no external force. At that instant, `f=2 N`, the accelerations are `2 m/s^2` and `-1 m/s^2`, total momentum has zero rate of change, and mechanical energy decreases at `2 W`. These are useful initial consequences without computing a full trajectory.

**Changed preparation.** Body 2 is instead held at `x2=1 m` from before the initial instant, so `v2=0`. With the other initial values unchanged, `f=2.5 N`. The support supplies the reaction `u2=f`; body 1 accelerates at `2.5 m/s^2`. The selected pair now exchanges momentum with the support. Keeping the earlier `v2=-1 m/s` together with a fixed-position constraint would describe an inconsistent preparation. Suddenly clamping the moving body would be another physical problem, requiring an account of that transition.

The reusable move is to obtain motion by joining balances to a response and preparation, and to revise the relevant exchange when the connection changes.

### PHY.6:5.2 - Obtain a total without solving its spatial distribution {#obtain-a-total-without-solving-its-spatial-distribution}

Let `c(x,t)` be the concentration of one chemical species in a fixed region. Its prescribed velocity field is `u(x,t)`. Use diffusion coefficient `D>0`, a constant first-order consumption rate `k>=0`, and the flux law

`J = c*u - D*grad(c)`.

The species balance supplies

`partial_t(c) = -div(J) - k*c.`

These equations state the response assumptions: advection, Fickian diffusion and first-order conversion. Their applicability is a physical premise. Impose no flux of this species through the region's boundary, `J dot n = 0`, where `n` is the outward normal.

For the total amount `N(t)=integral_region c(x,t) dx`, integration of the balance gives

`N' = -integral_boundary J dot n dS - k*N = -k*N`,

and therefore `N(t)=N(0)*exp(-k*t)`. The requested total follows from its initial total and the stated boundary and reaction laws. Internal transport need not be solved. Consumption of this species can coexist with conservation of the atoms it transfers into products.

**Changed question.** A local concentration maximum requires the initial spatial distribution and its evolution. The total alone no longer answers. Alternatively, if the reaction rate varies with position, the total rate becomes `-integral_region k(x)*c(x,t) dx`; replacing it by a constant times `N` now needs grounds for that reduction. Return to the spatial distribution or a justified bound when the new use needs it.

This case shows how the intended consequence determines which physical relations must be completed. It also separates a global balance result from a local transport prediction.

### PHY.6:5.3 - Detect an incompatible ideal connection before attempting a transient calculation {#detect-an-incompatible-ideal-connection-before-attempting-a}

Two ideal linear capacitors have positive capacitances `C1` and `C2`. Their lower terminals share a reference conductor; their upper terminals are connected through a resistance `R>0`. The effective description neglects leakage, inductance and radiation. Let `v1` and `v2` be the upper-terminal potentials relative to the common reference, and let current `I` flow from capacitor 1 to capacitor 2.

Charge balances and the resistive response give

`C1*v1' = -I;  C2*v2' = I;  R*I = v1-v2.`

The total upper-plate charge `Q=C1*v1+C2*v2` is constant. The difference `delta=v1-v2` obeys

`delta' = -(1/C1+1/C2)*delta/R`.

Thus the difference decays with time constant `tau=R*C1*C2/(C1+C2)`, and both potentials approach

`v_final = (C1*v1(0)+C2*v2(0))/(C1+C2)`.

For `C1=1 F`, `C2=3 F`, `R=2 ohm`, `v1(0)=8 V` and `v2(0)=0 V`, the settled potential is `2 V`, `tau=1.5 s`, and `I(t)=4*exp(-t/1.5) A`, with time measured in seconds.

Stored electrical energy is `H=(C1*v1^2+C2*v2^2)/2`. Substitution gives `H'=-R*I^2`. Its initial and final values are `32 J` and `8 J`, so `24 J` is converted into other energy, here heat in the ideal resistance. More generally, the energy difference is

`C1*C2*(v1(0)-v2(0))^2/(2*(C1+C2))`.

**Changed connection.** Set `R=0` as an ideal connection from the initial instant. Its constraint `v1=v2` conflicts with the supplied unequal initial potentials. The smooth evolution above cannot simply start from them under that constraint. Recover the interaction that establishes the common potential when its current, duration or energy conversion matters. Resistance, inductance or electromagnetic emission may matter depending on the actual arrangement and interval; the ideal connection alone does not specify them.

If only the settled potential is needed, conserved charge together with the premise that the connected system settles can already supply it. A transient description is needed for a different question, such as peak current. Taking the positive-resistance time constant to zero does not remove the finite energy conversion. This is why changing an idealization can require revisiting both the preparation and the requested consequence.

## PHY.6:6 - Bias-Annotation {#bias-annotation}

The examples use classical descriptions with explicit response laws. Their calculations are convenient for exposing balance, coupling and preparation. A stochastic, quantum or history-dependent response requires its own physical grounds and mathematical representation; the example equations do not supply those grounds.

Component descriptions can also make localized parts seem necessary. An account can instead describe a continuous medium through fields or many interacting constituents through collective variables. Choose the physical participants and the resolution of their description from the question.

## PHY.6:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Misstep exposed by the construction | Consequence | Repair |
| --- | --- | --- |
| Expect conservation to determine every rate | The momentum balance still lacks the connecting force. | Supply and qualify the interaction's response law. |
| Remove internal force from each body because it cancels in the total | The relative motion disappears from the description. | Combine balances for the total while retaining the force in the part equations. |
| Treat mechanical damping as destruction of total energy | The energy account misses heating and possible feedback on the response. | Identify the receiving energy form and retain its dynamics when it affects the answer. |
| Read a total as a spatial prediction | An integrated species amount is used to infer a local concentration peak. | Restore the distribution and the conditions its evolution needs. |
| Impose an ideal connection on incompatible initial values | The capacitor transient is undefined within the chosen smooth account. | Resolve the preparation or represent the establishing interaction. |
| Build a detailed transient before using a sufficient balance | Work grows although the settled value or total is already determined. | Derive the required consequence first and expand only where needed. |

## PHY.6:10 - Architectural Rationale {#architectural-rationale}

Separating balances, response laws and preparation makes their different contributions recoverable. Balances restrict change; response laws add behavior; preparation selects admissible evolution. Combining these relations before imposing a solving order lets the same physical account support different mathematical questions.

The construction uses C.29.BB for common balance reasoning and adds the physical choice of interactions, response grounds and compatible preparation. MMP.10 and C.29.2 handle the subsequent formulation and obtaining of mathematical results. This division permits a return to the missing physical premise without treating every solver difficulty as a computational defect.

Energy-based composition is especially useful when storage, conversion and exchange dominate the question. Direct momentum, species or charge balances can be simpler for another consequence. A physical variational principle offers another way to derive motion when its premises apply. The balance-and-response route is selected here for the difficulty it resolves, without requiring one formalism for every physical account.

## PHY.6:11 - SoTA-Echoing {#sota-echoing}

**How much physical description is needed to obtain a selected consequence?** Adopt the quantity-first construction supplied by C.29.BB and developed in :4.1-.3. For the species total in :5.2, integration of the balance gives `N(t)=N(0)*exp(-k*t)`. Constructing and solving the full spatial evolution gives the same total under the same laws and boundary condition, but additionally needs an initial concentration field and a way to obtain its evolution. If only the total is used, the integrated account preserves the answer with fewer needed inputs and operations. It deliberately gives up the spatial profile. A local-concentration question or a position-dependent reaction rate reopens that choice. A readily available spatial solution can also supply the total.

**How should a reusable physical account be composed?** Retaining simultaneous component relations, as in :4.4-.5, preserves their meaning when the analysis or connection changes. For the positive-resistance capacitor case, eliminating the common current into two explicit evolution equations gives the same response as the retained three relations. Keeping the charge balances and the resistive relation separately makes their different contributions available when the connection changes: the balances survive, while setting R to zero changes the latter into a voltage-equality constraint that also restricts the preparation. This accepts the extra task of solving simultaneous relations when reuse or changing connections makes it worthwhile. For an isolated explicit evolution already suited to the question, use that simpler form. Reopen the choice when a new connection introduces a constraint or a consequential store.

[Van der Schaft, Port-Hamiltonian nonlinear systems](https://arxiv.org/html/2412.19673v1) (2024 preprint, sections 1.1-1.2) supplies a contemporary synthesis of storage, dissipation and power-conserving interconnection, including differential-algebraic descriptions. Adapt its separation of these contributions to the physical assembly in :4.3-.4. Remark 1.3 makes an important limit explicit: replacing mechanical dissipation by an untracked internal-energy increase is conditional on the relevant thermodynamic feedback being absent. Adopt that qualification in the damper case. For the two-body case, direct momentum equations and their energy derivative already show motion and the conversion into heat. A port-Hamiltonian representation gives the same consequences under the same response laws and makes energy-preserving composition explicit. Adapt the storage/interconnection distinction without requiring the reader to construct that formal representation for this small problem. Its additional structure becomes useful when a later question needs systematic composition or passivity properties of several interacting parts. Reopen the chosen account when an omitted store or thermal feedback changes those consequences.

The [Modelica 3.7 equation rules](https://specification.modelica.org/maint/3.7/equations.html), especially section 8.6, distinguish simultaneous relations, initialization equations and numerical guesses. Its [connection rules](https://specification.modelica.org/maint/3.7/connectors-and-connections.html), section 9.2, give explicit equality and signed flow-sum constructions. Adopt these as a worked formal tradition for composable physical descriptions and consistent initialization. The physical reason for a connection and the adequacy of a response remain separate from language conformance. Retaining algebraic constraints avoids inventing a physical direction merely to obtain explicit state-derivative equations.

The current [Dyad component-construction tutorial](https://help.juliahub.com/dyad/stable/tutorials/creating-components.html) demonstrates reusable connector and response relations with separate analyses. Adapt that distinction so a reader can reuse the component relations for several analyses.

The three worked calculations are constructed examples under their stated idealizations, not reports of physical measurements.


## PHY.6:End {#end}
