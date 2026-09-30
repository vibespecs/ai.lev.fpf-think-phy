# PHY.1 - Construct Physical Similarity Across Changed Conditions: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.1:5 - Archetypal Grounding {#archetypal-grounding}

The following constructed cases derive conditional comparisons. The physical laws and idealizations used in each case are stated; no apparatus measurements are reported.

### PHY.1:5.1 - Find conflicting requirements before building a smaller flow experiment {#find-conflicting-requirements-before-building-a-smaller-flow}

A team proposes a quarter-size free-surface water experiment to investigate a flow in which inertia, gravity and viscosity may affect the result. The proposed geometry is similar, gravitational acceleration is unchanged, and the same liquid is initially intended. Use an incompressible Newtonian-fluid account. A relevant surface-tension, compressibility or other omitted effect would add a condition to this account.

Let L be characteristic length, U speed, g gravitational acceleration and nu kinematic viscosity. Comparing the acceleration contributions from :4.3 gives the Froude and Reynolds numbers:

~~~text
Fr = U/sqrt(g*L)
Re = U*L/nu.
~~~

Write `L'=lambda*L` for the model length. To preserve Fr at the same g, solve:

~~~text
U'/sqrt(g*lambda*L) = U/sqrt(g*L)
U' = sqrt(lambda)*U.
~~~

The same liquid then gives `Re'/Re=lambda^(3/2)`. For lambda=1/4, the required speed is U/2 and Re'=Re/8. A corresponding transit time L'/U' is one-half of L/U. Those settings preserve the inertia/gravity ratio while changing the viscosity/inertia ratio.

If the desired output needs both ratios reproduced, changing speed alone cannot repair the comparison. At fixed g, solving both conditions requires `nu'=lambda^(3/2)*nu`, which is nu/8 in this case. Selecting a liquid with that viscosity remains a physical-material question, including its other properties. Alternatively, with the same liquid and variable effective gravity, the conditions give `U'=U/lambda` and `g'=g/lambda^3`. At quarter scale those values are `4*U` and `64*g`; the transit time is divided by sixteen. A rotating apparatus proposed to create that acceleration also introduces rotation and spatial variation that may affect the comparison.

The first result is a decision about the experiment. If viscosity is negligible for the intended output throughout the relevant regime, the Froude-scaled experiment may suffice under that approximation. If viscosity changes separation or another needed behavior, retain that dependence and change the arrangement or the method of obtaining the answer. Matching initial and boundary conditions remains part of either construction.

Now change the question from a large-scale surface response to a local viscous effect near a wall. The previous gravity-dominated approximation leaves the new output unsupported. The method returns to the relative contributions and near-wall scale; the old choice of speed remains useful only for the question it answered.

### PHY.1:5.2 - Reproduce one deformation without claiming the whole field {#reproduce-one-deformation-without-claiming-the-whole-field}

Consider a straight uniform bar, fixed at the top, with an axial force F pulling down at the lower end. Let L be length, A cross-sectional area, Y Young's modulus, rho density and g gravity. Use small-strain linear elasticity and uniform material properties. Let x measure height from the bottom. The part below that point contributes weight `rho*A*g*x`, so the tensile force there is `F+rho*A*g*x`. Hooke's law gives local strain:

~~~text
strain(x) = F/(Y*A) + rho*g*x/Y.
~~~

Integrating from 0 to L gives total extension delta and mean strain:

~~~text
delta = F*L/(Y*A) + rho*g*L^2/(2*Y)
delta/L = F/(Y*A) + rho*g*L/(2*Y).
~~~

A geometrically similar bar made of the same material has `L'=lambda*L` and `A'=lambda^2*A`. To reproduce the applied-force contribution to strain, use `F'=lambda^2*F`. Its own weight instead changes by `lambda^3`. At unchanged g, the self-weight contribution to strain changes by lambda. Merely using a smaller copy with the same material does not reproduce the two load contributions together.

Suppose the original bar hangs under its own weight, with F=0, and the question concerns **only total extension relative to length**. An added lower-end force on the smaller bar can match that output. Solve the mean-strain equation for the new force:

~~~text
F' = A'*rho*g*L*(1-lambda)/2.
~~~

At quarter scale, F' is 3/128 of the original bar's weight. Substitution into the smaller bar's mean-strain equation gives `rho*g*L/(2*Y)`, the original value. The comparison therefore reproduces the requested normalized extension within this model.

Now ask for the strain at the lower end. The original unloaded bar has zero strain there; the smaller bar with the added force has `F'/(Y*A')` greater than zero. The output-specific construction cannot answer this new local question. To reproduce the complete strain profile, revisit the distributed loading or the combination `rho*g*L/Y`. The successful first comparison is retained for total extension.

### PHY.1:5.3 - Preserve competing physical time scales {#preserve-competing-physical-time-scales}

A substance diffuses along an interval and is consumed by a first-order reaction. A smaller comparison is proposed using the same diffusivity D and reaction rate k. Let c(x,t) be concentration, with the idealized equation:

~~~text
c_t = D*c_xx - k*c,   0 < x < L.
~~~

Both ends absorb the substance, so c(0,t)=c(L,t)=0. For a simple worked preparation take `c(x,0)=c0*sin(pi*x/L)`. Substitution gives:

~~~text
c(x,t) = c0*sin(pi*x/L)*exp(-(pi^2*D/L^2 + k)*t).
~~~

Use `x=L*xi` and the diffusion time `T=L^2/D`. At scaled time tau=t/T, the equation becomes `partial c/partial tau = partial^2 c/partial xi^2 - Da*c` on 0<xi<1, where `Da=k*L^2/D` compares reaction with diffusion. The midpoint concentration relative to c0 is `exp(-(pi^2+Da)*tau)`.

After L'=L/4 at unchanged D and k, the diffusion time is T/16 but Da becomes Da/16. If the original Da is 1, then at tau=1 the smaller experiment has a midpoint concentration exp(15/16), approximately 2.55, times the original normalized value. At that corresponding time, the smaller experiment has lost less substance to reaction.

To reproduce the dimensionless evolution with the same D, the smaller model would require `k'=16*k`, together with the corresponding initial and boundary conditions. A physical change intended to obtain that rate may change D too; solve using the resulting pair of properties. If the question instead concerns diffusion during an interval when consumption has a negligible effect, derive and use that shorter-time approximation. The reaction can re-enter when the requested duration changes.

## PHY.1:6 - Bias-Annotation {#bias-annotation}

The explicit cases use classical continuum laws and positive scale factors because their derivations are easy to inspect. In a new regime, discreteness, quantum effects or a change in material behavior can invalidate such laws. Recover the applicable account before extending their scaling.

The worked algebra assumes access to the physical laws and a reader able to manipulate them. The prerequisites in :1 help locate a needed contribution. One participant can recover the interaction law while another derives the comparison settings; their shared explanation must preserve what the law describes and which settings the arrangement can supply.

## PHY.1:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Misuse | Repair |
| --- | --- |
| Build a smaller geometric copy and apply one scale factor to every result. | Derive how the contributing forces, rates and preparation change; :5.1 and :5.2 produce different factors for different contributions. |
| Match one familiar number while another relevant effect changes. | Recover the physical terms behind the requested output and solve their conditions together. |
| Treat all mathematically adjustable properties as independent apparatus settings. | Use the properties of an available material or arrangement, including changes induced by the same control. |
| Transfer an entire field from a comparison designed for one total. | Retain the output-specific result and reconstruct the comparison for the newly requested field or location. |
| Drop a small term without following its effect to the output. | Examine the relevant limit, interval and sensitivity; keep a bound or a more detailed account where that term changes the decision. |

## PHY.1:10 - Architectural Rationale {#architectural-rationale}

Physical similarity is constructed from the effects that produce the requested answer. Choosing those effects before solving scale equations makes it possible to explain why a setting matters and to revise the comparison when the question changes. Comparing geometry alone would omit the different scaling of physical contributions. Requiring complete behavioral similarity for every use would exclude cheaper comparisons that preserve one useful result.

The physical and mathematical work remain connected. Physical reasoning supplies the laws, their regime and the realizable changes; mathematical operations expose joint conditions and transfer the consequence. Computation can solve those conditions or examine a mismatch. Their common inference and result-use methods are provided by FPF, while this pattern develops the physical scaling construction.

## PHY.1:11 - SoTA-Echoing {#sota-echoing}

The working question is how to obtain a useful physical result after changing scale or conditions. The selected approach derives and reconciles the relevant physical ratios and preparation, then handles unmatched effects at the output that matters. It combines established similarity reasoning with explicit result-specific transfer and revision.

[Mahajan, The Art of Insight in Science and Engineering (2014), sections 5.2-5.3](https://ocw.mit.edu/courses/res-6-011-the-art-of-insight-in-science-and-engineering-mastering-complexity-fall-2014/3bca850386a3005c22134fa62fb3bad5_MITRES_6-011F14_art_insfin.pdf), provides a methodological anchor: dimensionless dependence can expose omitted physics while leaving an unknown coefficient or function. This changes :4.2-4.3 by making physical selection and the remaining unknown explicit. Its examples supply historical grounding rather than a complete current physics inventory.

[Price's 2024 MIT course](https://live.ocw.mit.edu/courses/res-12-001-topics-in-fluid-dynamics-fall-2024/pages/essay-2-dimensional-analysis-of-models-and-data-sets-similarity-solutions-and-scaling-analysis/) emphasizes selecting a physically useful dimensionless basis and relating coefficients to competing terms. Adopt that choice in :4.3. [NASA's explanation of similarity parameters](https://www1.grc.nasa.gov/beginners-guide-to-aeronautics/similarity-parameters/) makes viscosity and compressibility consequences tangible. The warning is applied to effects relevant to the requested output; differing parameters can still permit a useful limited approximation.

[Li et al. (2021), Spatial and temporal scaled physical modeling of fluid convection using hypergravity](https://arxiv.org/abs/2103.16028), report a way to reconcile gravity and viscosity scaling and identify limitations introduced by the apparatus. Their abstract motivates the changed-gravity alternative in :5.1. That case derives the scale factors from its stated conditions; reproducing the reported experiments requires their full apparatus method.

An alternative to a single matched comparison is reconstructing a result from several scales. [Davey and Ochoa-Cabrero (2023), section 2.2](https://doi.org/10.1007/s10665-023-10296-1), derive finite-similitude combinations under additional assumptions about scale dependence. This keeps the multiple-experiment return in :4.5 available when simple matching fails. Their higher-order construction has its own assumptions; the present method does not supply its full calculus or infer them from several measured points.

The output-specific loading and changed-question cases are this publication's conceptual synthesis. Revisit the selected account when a new regime, source result or failed comparison changes a physical premise, available setting or valid approximation. New material or computation can make a previously infeasible comparison useful.


## PHY.1:End {#end}
