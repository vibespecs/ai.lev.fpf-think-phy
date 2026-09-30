# PHY.4 - Constrain an Unknown Physical Law by Transforming the Situation: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.4:5 - Archetypal Grounding {#archetypal-grounding}

These are constructed physical accounts. They illustrate how physical premises constrain an unknown law and how a changed premise changes the result.

### PHY.4:5.1 - Restrict an unknown resistive force {#restrict-an-unknown-resistive-force}

Seek the instantaneous mean resistive force on a body moving through a homogeneous isotropic medium at a fixed material state, in a classical three-dimensional regime. Assume the body and preparation introduce no preferred direction, relevant memory is negligible, and relative velocity w is the only varying input. These assumptions define the proposed comparison; their adequacy in a particular experiment remains a physical question.

Rotating the entire relevant situation rotates w and the force together. Because there is no further directional input, `F(Qw)=QF(w)` for every spatial rotation Q. For nonzero w, rotations about w rule out a perpendicular force component. Equal-length velocities are related by rotation, so write:

`F(w)=-a(|w|^2)*w` for w different from zero.

At w=0, rotational symmetry gives `F(0)=0`. The coefficient a is an unknown scalar function at the fixed material conditions. Its dimension is mass divided by time. Memoryless passive resistance gives:

`F(w) dot w=-a(|w|^2)*|w|^2 <= 0`,

so `a(s)>=0` for s>0.

The result determines a direction and sign while leaving the speed dependence unresolved. Both `a(s)=a0` and `a(s)=b0*sqrt(s)` with suitable nonnegative dimensional constants satisfy these restrictions. They predict different force magnitudes when speed changes. The comparison alone therefore provides neither a linear nor a quadratic drag law.

For a direction-only question, use the result directly. To predict stopping time, supply further information about a over the speeds involved, or obtain a sufficient bound over the admissible family. MMP.11 keeps that unresolved relation visible instead of inserting a familiar drag coefficient.

### PHY.4:5.2 - Add a physical direction {#add-a-physical-direction}

Now the body is oriented or the environment has an aligned surface. Include its unit direction n in the input. Under a rotation of the complete situation, both w and n change, so the condition becomes:

`F(Qw,Qn)=QF(w,n)`.

A rotation fixing w can now change n. The earlier argument that fixed all inputs while rotating a perpendicular output component is no longer available.

For example, one admissible linear resistive family is:

`F(w,n)=-alpha*w-beta*(n dot w)*n`.

For unit n, its power is `-alpha*|w|^2-beta*(n dot w)^2`. Resolving w into parts parallel and perpendicular to n shows passivity for every w when `alpha>=0` and `alpha+beta>=0`. This is a possible family, not an exhaustive determination of the changed law.

With consistent units, take alpha=1, beta=3, `w=(1,1,0)` and `n=(1,0,0)`. The force is `(-4,-1,0)` and power is -5. The force resists motion while pointing in a direction different from -w. This possibility is excluded by the earlier isotropic account and allowed by the additional physical input.

If n is fixed in the laboratory while only the body motion changes, retain that fixed n in the experiment's account. Rotating the coordinate system changes the components of both quantities; it supplies no premise that removes the material or environmental direction.

### PHY.4:5.3 - Exchange two participants {#exchange-two-participants}

Two identical chambers at the same temperature exchange one kind of particle through a symmetric passage. Let a and b be their current concentrations and let `J(a,b)` be the instantaneous mean transfer rate from the first chamber to the second. Assume the proposed regime needs no additional passage state, and the surroundings introduce no directional bias.

Keep the chamber labels and the positive counting direction fixed, and exchange the concentrations in the two preparations. Because the chambers and passage are symmetric and the surroundings supply no bias, this physical exchange predicts a reversed measured transfer rate:

`J(b,a)=-J(a,b)`.

At equal concentrations, `J(a,a)=0`. A proposed law `J(a,b)=k*(a-b)^2` with k>0 fails the interchange condition: it gives a positive rate in the same counted direction after the preparations are exchanged.

Both `J(a,b)=k1*(a-b)` and `J(a,b)=k3*(a-b)^3` satisfy the interchange condition when their constants have the corresponding units. Symmetry has not chosen between them or determined their coefficients. Directional thermodynamic claims would additionally use the physical driving potentials and the applicable dissipation law.

If the passage stores no particles, the chamber particle numbers satisfy `dN1/dt=-J` and `dN2/dt=J`, preserving their sum. If appreciable particles accumulate in the passage, include its particle number and separate inlet and outlet rates. The earlier two-chamber balance then omits a relevant participant.

This comparison uses exchange and balance rather than rotation. It opens the same kind of result: an admissible law family and the physical condition that would require revising it.

## PHY.4:6 - Bias-Annotation {#bias-annotation}

A familiar formula can conceal a missing physical premise. An elegant symmetry argument can conceal the same omission. Recover the participants, preparation and surroundings before deciding which transformations the situation admits.

A conditional family is useful when its remaining freedom is stated. Supplying an unexplained familiar coefficient would replace an unresolved physical question with apparent precision. Obtain further information only for the consequence that needs it.

## PHY.4:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

**Dropping the surroundings from the transformation.** Rotating a body relative to a fixed material direction can change its response. Transform the complete relevant account and distinguish that experiment from a coordinate change.

**Selecting a magnitude law from direction symmetry.** The linear and quadratic resistance possibilities in :5.1 satisfy the same directional restriction. Carry the unknown scalar function until a further physical contribution constrains it.

**Applying an instantaneous dissipation inequality to an energy-storing interaction.** Recover stored energy and the exchange balance. Temporary return of stored energy changes the instantaneous power without establishing an active energy source.

**Using a balance with an omitted participant.** Accumulation in the passage changes the two-chamber balance in :5.3. Include the storage and its exchanges before computing the chamber changes.

## PHY.4:10 - Architectural Rationale {#architectural-rationale}

The physical construction precedes the mathematical symmetry calculation. MATH.13 can derive what a supplied transformation preserves; the present method supplies and criticizes the physical grounds for choosing that transformation and its inputs.

The unknown relation remains explicit through the work. This supports relational formulations as well as response functions, and allows later symbolic, numerical or learned models to use the same physical restrictions.

Similarity, analogy and performance bounds remain separately usable methods. Their results may settle the physical question directly. When a law is still missing, this method constrains its form and identifies the remaining contribution without requiring a detailed mechanism first.

## PHY.4:11 - SoTA-Echoing {#sota-echoing}

Feynman's [discussion of symmetry in physical laws](https://www.feynmanlectures.caltech.edu/I_52.html), especially §52-2, is a historical methodological anchor for transforming an experiment together with its relevant surroundings. The adopted contribution is the physical construction of the comparison. The particular transformation and its regime are selected from the physical account being used.

Villar and colleagues' [Scalars are universal](https://arxiv.org/html/2106.06610v4), Proposition 4 and Appendix H, provides a contemporary constructive connection between specified symmetry actions, scalar invariants and equivariant response families. Its distinctions between rotation and reflection groups and between different input quantities matter when selecting a model. The paper's mathematical representation results are used under their hypotheses; the present physical method establishes which input and transformation account is appropriate.

When formulating an unfamiliar interaction law, a common alternative is to select a familiar constitutive formula and fit its coefficients. With only the physical premises in :5.1, that choice would insert a speed dependence the premises do not determine. The transformation method in :4.2-:4.4 first establishes the allowed direction and sign, leaving the scalar function open. For a direction-only question, this supplies the needed answer without obtaining a detailed law or fitting its coefficients. For a stopping-time prediction, :4.5 requires further information about that function or a sufficient bound; the restriction alone leaves the prediction unresolved.

An established constitutive account or reliable analogue is preferable when it applies to the intended regime and supplies the needed consequence with less work. The present method then helps inspect its physical assumptions or a proposed change of conditions. Reopen this choice when a new physical input or regime invalidates the comparison, an improved account changes its grounds or offers an easier answer, or the receiving question requires information that the constrained family leaves open.


## PHY.4:End {#end}
