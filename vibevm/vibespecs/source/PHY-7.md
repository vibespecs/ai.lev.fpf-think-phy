# PHY.7 - Obtain Motion from a Physical Variational Principle: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.7:5 - Archetypal Grounding {#archetypal-grounding}

### PHY.7:5.1 - Represent a constraint, then move its support {#represent-a-constraint-then-move-its-support}

A point mass m moves in a vertical plane on an ideal rigid, massless rod of length l. Its frictionless pivot is initially fixed. Gravity is uniform with acceleration g. Let theta be the angle from the downward vertical; relative to the pivot,

`x=l*sin(theta);  y=-l*cos(theta)`.

The rod constraint is built into this configuration. For its ideal reaction, virtual motion along the circle has no radial displacement and the reaction does no virtual work. Kinetic energy is `T=m*l^2*theta_dot^2/2`, and potential energy is `V=-m*g*l*cos(theta)`. Thus

`L=m*l^2*theta_dot^2/2+m*g*l*cos(theta)`.

Varying theta with fixed temporal endpoints gives

`m*l^2*theta_ddot+m*g*l*sin(theta)=0`.

For `l=1 m`, `g=10 m/s^2` and initial `theta=pi/6`, the angular acceleration is `-5 rad/s^2`. The radial reaction need not be solved to obtain that consequence. It can be recovered from the physical acceleration if a later question concerns the rod load.

**Changed support.** Prescribe a horizontal pivot position X(t). The physical position becomes `x=X(t)+l*sin(theta)` while y is unchanged. Differentiating the complete position gives

`T=m*(X_dot^2+2*X_dot*l*cos(theta)*theta_dot+l^2*theta_dot^2)/2`.

Keeping the same gravitational potential and varying theta gives

`m*l^2*theta_ddot+m*l*X_ddot*cos(theta)+m*g*l*sin(theta)=0`.

With pivot acceleration `X_ddot=2 m/s^2` at the same angle, the angular acceleration is about `-6.732 rad/s^2`. Omitting the pivot term from the velocity would preserve the old answer while losing a real forcing. The pivot's prescribed motion may do work, so the fixed-pivot mechanical-energy conservation claim does not automatically transfer.

**Changed interaction.** For the fixed pivot, add an established damping torque `Q=-b*theta_dot`, with `b>=0`. The virtual-work equation gives `m*l^2*theta_ddot+b*theta_dot+m*g*l*sin(theta)=0`. The mechanical energy has derivative `-b*theta_dot^2`. Appending this dissipative torque to a conservative scalar potential would require a different physical account. PHY.6 supplies the corresponding balance and receiving energy form; a more elaborate dissipative action is useful only when the intended work needs it.

The general move is to construct the allowed configuration and its velocities, derive the consequence, and rebuild only the affected contribution when the support or interaction changes.

### PHY.7:5.2 - Recover an interaction that energy alone would miss {#recover-an-interaction-that-energy-alone-would-miss}

A nonrelativistic particle with mass m and charge e moves in the xy plane in a prescribed uniform magnetic field B perpendicular to it. Electric fields, radiation reaction and the particle's alteration of the source field are neglected. The electromagnetic coupling is the physical premise; the field does no mechanical work but changes the direction of motion.

Choose a vector potential `A=(-B*y/2,B*x/2,0)`, whose curl is the specified magnetic field. With zero electric scalar potential, the physical Lagrangian is

`L=m*(x_dot^2+y_dot^2)/2 + e*B*(x*y_dot-y*x_dot)/2`.

Its derivatives give

`d/dt(L_xdot)=m*x_ddot-e*B*y_dot/2;  L_x=e*B*y_dot/2`,

and the corresponding y expressions. The Euler-Lagrange equations are therefore

`m*x_ddot=e*B*y_dot;  m*y_ddot=-e*B*x_dot`.

For `e*B/m=2 per second`, initial `x_dot=3 m/s` and `y_dot=0`, the initial acceleration is `(0,-6) m/s^2`. Substitution into the kinetic-energy derivative gives zero. Conservation of kinetic energy alone would also allow straight uniform motion; it does not determine the magnetic turning. Using only T with zero scalar potential would miss the interaction.

**Changed representation.** Let `chi=B*x*y/2` and use `A_new=A+grad(chi)=(0,B*x,0)`. The new Lagrangian is `L_new=m*(x_dot^2+y_dot^2)/2+e*B*x*y_dot`. Its difference from L is `e*d(chi)/dt`, so the fixed-endpoint equations are unchanged. The canonical momenta `L_xdot` and `L_ydot` do change; the physical velocity and magnetic field do not. Comparing those canonical expressions as though they were two observed mechanical momenta would invent a physical discrepancy.

The action's stationary paths depend on the physical interaction; equivalent gauge descriptions preserve them under the stated endpoint rule.

### PHY.7:5.3 - Derive an interior law and change the endpoint condition {#derive-an-interior-law-and-change-the-endpoint-condition}

A taut string has uniform tension T and mass per unit length mu. Its transverse displacement u(x,t) is small enough that slopes can be treated to leading order; changes of tension and longitudinal motion are neglected. The kinetic energy per length is `mu*u_t^2/2`. Expanding the extra length to second order in slope gives the stored elastic contribution `T*u_x^2/2`. For length l, use

`S[u]=integral over time and 0<=x<=l of (mu*u_t^2-T*u_x^2)/2 dx dt`.

Take variations eta that vanish at the two temporal endpoints. Integration by parts gives the interior coefficient `-mu*u_tt+T*u_xx` and the spatial boundary contribution

`integral over time of [-T*u_x*eta] at x=0,l dt`.

Thus the interior equation is `mu*u_tt=T*u_xx`. At a fixed endpoint, eta is zero. At an unloaded endpoint free to move transversely in this model, eta is arbitrary and the corresponding slope must be zero.

For `mu=0.01 kg/m`, `T=100 N` and `l=1 m`, wave speed is `sqrt(T/mu)=100 m/s`. Two fixed endpoints admit the lowest nonzero spatial mode `sin(pi*x/l)`, giving frequency `50 Hz`. Keep the left endpoint fixed and free the right endpoint transversely while maintaining its axial tension; the lowest mode becomes `sin(pi*x/(2*l))` and its frequency is `25 Hz`. The interior equation did not change. Reusing the fixed-end spectrum would miss the changed boundary.

**Loaded endpoint.** Attach a massless transverse spring of stiffness kappa at x=l. Add `-integral kappa*u(l,t)^2/2 dt` to the action. With the right endpoint variation free, its coefficient gives `T*u_x(l,t)+kappa*u(l,t)=0`. The spring changes the boundary condition through its stored energy. If an endpoint mass is consequential, its kinetic term must be included too; the massless condition would no longer supply that boundary's dynamics.

Retain the boundary contribution until the physical freedom or load determines its use.

## PHY.7:6 - Bias-Annotation {#bias-annotation}

The examples make smooth classical stationarity easy to inspect. Quantum or probabilistic descriptions can connect an action to observations through a different rule; the fixed-history calculation here does not supply that rule. Use the principle and interpretation of the relevant physical theory.

Compact energy expressions can also hide how a constraint is maintained. The ideal rod, imposed pivot motion and massless endpoint spring each exclude physical detail. Restore that detail when reaction, compliance or a transient changes the requested consequence.

## PHY.7:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Misstep | Consequence | Repair |
| --- | --- | --- |
| Use T-V without recovering the interaction | The magnetic force disappears although kinetic energy is constant. | Supply the coupling from the physical theory and vary the complete Lagrangian. |
| Differentiate coordinates while omitting their moving reference | The prescribed pivot acceleration is absent from the motion. | Differentiate the complete position map, including its explicit time dependence. |
| Discard a boundary term before deciding what is fixed | A loaded or free endpoint receives the wrong condition. | Retain the term until the boundary freedom and physical contribution are specified. |
| Use one constraint rule for every velocity restriction | Different variational constructions are treated as the same physical model. | Recover the constraint's reaction or admissible-variation premise. |
| Read stationary as minimum | A saddle history receives an unsupported optimality claim. | Use the first-variation result at its established scope and perform the stronger comparison when needed. |
| Read a changed canonical expression as changed motion | Gauge-related descriptions appear to disagree physically. | Recover the physical quantities and the endpoint term preserved by the transformation. |

## PHY.7:10 - Architectural Rationale {#architectural-rationale}

The action, allowed comparison and physical interpretation carry different information. Keeping them together prevents the mathematical operation of variation from silently choosing a physical theory. Keeping them distinct allows a return to the part that changed.

MATH.10 supplies the common variational argument. PHY.7 adds the physical choice of principle, interactions, constraint model and preparation. PHY.6 offers the alternative construction from balances and response laws. MMP and the computational patterns receive the resulting equations and conditions when the intended consequence needs further formulation or calculation.

## PHY.7:11 - SoTA-Echoing {#sota-echoing}

**When does an action formulation repay its cost?** For the ideal rod in :5.1, both the angular-action calculation and a tangential projection of Newton's force balance obtain the angular acceleration without solving the radial reaction. Both retain the rod constraint as a physical premise. If the rod load is the requested result, the balance or a reaction reconstruction is needed. For :5.3, both local force balance and field variation give the wave equation; retaining the action's endpoint term also makes the changed spring contribution available. Select that organization when repeated constraint or boundary changes make it useful. Use the simpler sufficient balance for an isolated question. These comparisons are constructed uses, not measurements of universal efficiency.

[Sussman and Wisdom, Structure and Interpretation of Classical Mechanics, second edition, chapter 1](https://mitp-content-server.mit.edu/books/content/sectbyfn/books_pres_0/9579/sicm_edition_2.zip/chapter001.html), is the established source for treating coordinate choice, physical action and variation as a connected construction. Adopt that connection in :4.1-.4. Sections 1.6 and 1.10 limit the automatic use of T-V and of coordinate-constraint arguments. In particular, section 1.10.3 distinguishes stationarity over constrained histories from the ideal-reaction rule for nonintegrable velocity constraints. The resulting instruction is to recover the physical constraint model before choosing the variation. Reopen that choice when the way a constraint is maintained changes a predicted reaction or motion.

[Gaset, Lainz, Mas and Rivas, The Herglotz variational principle for dissipative field theories](https://arxiv.org/abs/2211.17058) (2022 preprint, published 2024), develops two formulations of dissipative field variation. Its section 5.2 gives a mathematical case where they have different solutions; the conclusions identify a condition under which the approaches agree. Adapt the methodological consequence: naming a variational principle is insufficient without its variation rule and conditions. The example establishes formal non-equivalence; it does not select the physical adequacy of either account for an apparatus. An action-based treatment of a new dissipative interaction reopens that choice.

[Galley, Tsang and Stein, The principle of stationary nonconservative action for classical mechanics and field theories](https://arxiv.org/abs/1412.3082) (2014), supplies a distinct route using doubled variables and an initial-value construction. Its opening eliminated-oscillator example shows why eliminating an environment inside the usual endpoint action can lose the intended causal response. For the supplied damping torque in :5.1, the force or virtual-work equation already gives the desired motion with less apparatus. The extended-action route becomes relevant when the work needs elimination within an action or a variational treatment of nonconservative coupling. Retain that choice rather than silently absorbing every loss into an ordinary potential.

The worked calculations are constructed consequences of their stated classical descriptions.


## PHY.7:End {#end}
