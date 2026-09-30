# PHY.2 - Construct a Physical Analogue from Interactions: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.2:5 - Archetypal Grounding {#archetypal-grounding}

These constructed examples show two uses: obtaining consequences of a known physical account and developing a proposed physical mechanism. The calculations describe idealized sources; they report no apparatus measurements.

### PHY.2:5.1 - Build the missing coupling in a mechanical/electrical analogue {#build-the-missing-coupling-in-a-mechanical-electrical-analogue}

Two bodies move along a line, joined by an ideal spring. Let their masses be m1 and m2, velocities v1 and v2, and the spring extension be d. External forces are f1 and f2; linear drag coefficients b1 and b2 are nonnegative. With spring stiffness k>0, the physical laws are:

~~~text
m1*dv1/dt = f1 - b1*v1 - k*d
m2*dv2/dt = f2 - b2*v2 + k*d
dd/dt = v1 - v2.
~~~

The question is how a deformation transfers motion between the bodies. Two independent electrical elements for the masses would omit that interaction. Choose node voltages to represent velocities, injected currents to represent external forces, and charge-accumulating capacitors for the masses. A conductance from each node to the reference node can represent its drag. The missing coupling needs a state whose rate is proportional to the difference of the two voltages. An inductor connected between the nodes supplies that relation.

Let `s=r*t` be source time, `V_i=a*v_i` the voltages and `I_i=h*f_i` the injected currents, with positive dimensional conversion factors a and h and positive time ratio r. Let J be current through the inductor from node 1 to node 2. Current conservation and the ideal inductor law give:

~~~text
C1*dV1/ds = I1 - G1*V1 - J
C2*dV2/ds = I2 - G2*V2 + J
L*dJ/ds = V1 - V2.
~~~

Substitute the conversions and `J=h*k*d`. All three relations match the mechanical account when:

~~~text
C_i = r*h*m_i/a
G_i = h*b_i/a
L = r*a/(h*k).
~~~

The constructed inductor carries the coupling state. The initial source state must satisfy `V_i(0)=a*v_i(0)` and `J(0)=h*k*d(0)`. For m1=2 kg, m2=1 kg, k=3 N/m, d(0)=1 m, zero velocities and zero applied forces, the first accelerations are -1.5 and +3 metres per second squared. The prepared inductor current produces the corresponding voltage changes. With J(0)=0, the source would instead remain at rest and miss the deformation-driven motion.

The stored mechanical energy is `(m1*v1^2 + m2*v2^2 + k*d^2)/2`. Differentiating gives power `f1*v1 + f2*v2 - b1*v1^2 - b2*v2^2`. The circuit's stored energy is `r*a*h` times the mechanical energy; its supplied and dissipated powers have the compatible factor `a*h`. The correspondence therefore includes storage and transfer under the stated ideal laws.

The first result is a source design and interpreted initial response. Before building it, choose the conversion factors so capacitances, conductances, inductance, voltages and currents lie in the available ranges. Include losses or loading that would alter the requested response.

Now change the target: a controller supplies a force that increases with velocity, producing effective negative damping over a stated range. A nonnegative conductance cannot realize that contribution. The changed physical construction needs an active element and its energy supply, or another means of obtaining the result. The previously constructed passive analogue still answers the original dissipative question.

### PHY.2:5.2 - Construct a mechanism whose short-time consequence differs from diffusion {#construct-a-mechanism-whose-short-time-consequence-differs-from}

A spreading population of moving particles is approximately diffusive over long observations. The target question is whether that approximation can describe the first short interval after a localized release. Consider a proposed mechanism in which motion persists for a while before its direction changes.

Build a simple source in thought: independently driven shuttles on a line move at speed u, reversing direction at random times. The waiting times are independent exponentials with reversal rate lambda. A drive maintains the speed, and a controller supplies the reversals. Treat reversal duration as negligible relative to the intervals being considered. This source combines sustained physical motion with stochastic switching. Using it for the particles proposes a relation between their direction persistence and their observed spreading.

The motion already supplies a useful qualitative consequence. Starting at x=0, a shuttle travels path length `u*t` in elapsed time t; reversals can only reduce its distance from the start. Thus `abs(x(t)) <= u*t`. Reaching a point at distance d requires at least time `d/u`. An ideal diffusion law with positive diffusivity instead assigns positive probability beyond every finite distance at every positive time. These are different predictions even when their long-time spreading agrees. An arrival before `d/u` would contradict the proposed bounded-speed target mechanism under its stated speed and preparation. Whether an earliest-arrival observation would discriminate the mechanisms also depends on its resolution and on the probability predicted for such arrivals. The bound is already a source result; the target correspondence remains a hypothesis.

For a small interval dt, reversal has probability `lambda*dt` to first order. If p_plus and p_minus are the position densities of right-moving and left-moving shuttles, transport and exchange between the two states give:

~~~text
partial_t p_plus  = -u*partial_x p_plus  - lambda*p_plus + lambda*p_minus
partial_t p_minus = +u*partial_x p_minus + lambda*p_plus - lambda*p_minus.
~~~

The total density is `p=p_plus+p_minus` and the flux is `j=u*(p_plus-p_minus)`. Adding and subtracting the equations yields:

~~~text
partial_t p = -partial_x j
partial_t j = -u^2*partial_x p - 2*lambda*j.
~~~

Direction is the additional state that lets the source retain motion between changes. Omitting it too early would erase the short-time effect under investigation.

Release all shuttles at x=0 with equal probabilities of the two directions, on an unbounded line. The mean position stays zero. Multiplying the equations by x and `x^2` and integrating, with vanishing boundary terms, gives for the mean-square displacement M(t):

~~~text
M''(t) + 2*lambda*M'(t) = 2*u^2
M(0) = M'(0) = 0
M(t) = (u^2/lambda)*[t - (1-exp(-2*lambda*t))/(2*lambda)].
~~~

At short times M(t) is approximately `u^2*t^2`: particles mostly retain their direction. At long times its leading growth is `(u^2/lambda)*t`, corresponding to diffusion coefficient `D=u^2/(2*lambda)`. The source thus produces a long-time diffusion law while giving a different short-time consequence. If u and lambda both have numerical value 1 in the chosen units, M(1) is approximately 0.568 square length units, while the leading diffusion expression gives 1.

The first result is a conditional explanation and a candidate change of observation interval. Long-time diffusive behavior alone leaves the proposed persistence mechanism unresolved. A useful return is to compare direction correlation or early spreading when either could distinguish it from a competing mechanism. An existing measurement can suffice. A physical shuttle apparatus adds no value if the derivation already supplies the consequence the work needs.

Now suppose target turns have an appreciable duration, or their occurrence depends on how long the present run has lasted. The source's instantaneous, memoryless reversal rule no longer supplies that target behavior. Construct the missing turn state or waiting-time dependence, recover its physical interpretation, and derive its effect on the requested interval. The previous model remains a limiting construction where those effects are negligible. For a material shuttle implementation, finite acceleration also limits how short an interval it can reproduce.

## PHY.2:6 - Bias-Annotation {#bias-annotation}

The worked cases use classical interaction laws and stochastic switching that can be manipulated through ordinary differential reasoning. Other physical regimes can require different permitted states, transformations and observations. Reuse the construction method with the physical laws of that regime; the elementary sources here supply examples of it.

A familiar source can be easier to imagine than a suitable one. Follow the behavior required by the target question when choosing and revising mechanisms. Collaborators can supply unfamiliar physical contributions. Human mental-model studies motivate part of this approach; applying the method with AI contributors requires checking the construction they actually produce and the prerequisites its users possess.

## PHY.2:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Misuse | Repair |
| --- | --- |
| Give components corresponding names but leave their interaction unbuilt. | Construct the connection's physical law and state, then derive the coupled behavior. |
| Reuse isolated-component behavior after connecting a load that changes it. | Include the loading or derive conditions under which its influence is negligible for the output. |
| Start every source state at zero while the target contains stored deformation or another prepared state. | Map and realize the preparation used by the target question. |
| Treat one reproduced observation as enough to identify the target mechanism. | Derive a consequence on which plausible mechanisms differ, or keep the explanation conditional when that suffices. |
| Change a coefficient past the range an available mechanism can supply. | Reconstruct the physical source, including a required drive or new state, or retain the result in its applicable range. |

## PHY.2:10 - Architectural Rationale {#architectural-rationale}

The operative contribution is constructing physical mechanisms that can work together. Correspondence becomes usable after there is enough source behavior to compare. Preparation, coupling and the means of producing an effect therefore belong inside construction, where they can change the selected source.

The method accommodates both a known target account and development of a target hypothesis. Their first results differ: a derived transfer can answer a target question under its physical premises; a proposed mechanism can reveal a consequence that directs inquiry. This keeps early physical imagination useful while making the strength of its result recoverable.

FPF supplies common first-model reasoning, state construction, correspondence, computation and inquiry choice. Mathematical Thinking and MMP supply the required mathematical operations and formulation methods. The physical contribution here selects interactions, their connections and their attainable behavior. A circuit or a moving-shuttle construction demonstrates that contribution.

## PHY.2:11 - SoTA-Echoing {#sota-echoing}

The working question is how to construct a useful physical source when no ready analogue supplies the required behavior. The approach combines iterative source construction with explicit physical interactions, preparation and result use.

[Nersessian (2025), section 3](https://onlinelibrary.wiley.com/doi/10.1111/tops.12777), examines scientific cases in which the analogy source is itself developed through construction and manipulation. Adopt that contribution in :4.2-4.6: source revision can refine the target problem as well as its candidate solution. Her studies support a human scientific practice; the allocation of work among people and AI here is a methodological extension.

[De Benedetto and Poth (2025, first online 2024), section 3.1](https://doi.org/10.1007/s13164-024-00752-x), reconstruct how combined representational resources can create new inferential possibilities. This supports keeping mechanisms from different sources available during construction. The present pattern develops the physical work of connecting them rather than adopting their full theory of concept learning.

[Hangleiter, Carolan and Thebault, Analog Quantum Simulation (2022), sections 8.3.3-8.4](https://arxiv.org/pdf/2303.00814), distinguish the source apparatus, its mathematical description, the formal target and the physical target. Their analysis changes :4.4-4.5 by locating the premise needed for each inference. The general connection is reused from C.29.1 and C.29.3. Their validation discussion is applied according to the conclusion needed; a conditional hypothesis remains a useful result when a stronger target claim is unresolved.

[Angelani (2016), section 2](https://arxiv.org/pdf/1601.04845), supplies a transparent transport-and-switching construction for the second worked case. His tumble events choose a new direction, whereas lambda here counts actual reversals; the rate convention is stated in the case. [Datta, Beta and Grossmann, version 3 of The random walk of intermittently self-propelled particles](https://arxiv.org/html/2406.15277v3), makes richer run/turn dynamics and waiting-time distributions available. Its section II supports the return when the simple switching assumption fails. The one-dimensional shuttle example is a constructed illustration, not a reproduction of those authors' apparatus or a complete active-matter model.

The dimensional circuit construction and paired changed-condition uses are this publication's synthesis. Revisit a source choice when a new law, available mechanism or observed disagreement changes the correspondence or reveals a useful physical possibility. A new example alone leaves the general method unchanged.


## PHY.2:End {#end}
