# PHY.3 - Derive a Physical Limit from Permitted Transformations: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.3:5 - Archetypal Grounding {#archetypal-grounding}

### PHY.3:5.1 - Bound a proposed engine without designing its mechanism {#bound-a-proposed-engine-without-designing-its-mechanism}

**Question.** A proposed cyclic machine takes 100 J from an ideal reservoir at 600 K and delivers 60 J as work. Its only other interaction is heat rejection to an ideal reservoir at 300 K. The machine returns to its initial state. Can a different mechanism make the proposal possible under these same conditions?

The physical preparation includes both reservoirs, the work store and restoration of the machine. It supplies no fuel, depleted auxiliary store or initially available nonthermal resource. The two temperatures are absolute thermodynamic temperatures. Energy balance gives 40 J rejected to the cold reservoir; that balance alone leaves the proposed output admissible.

Use the classical second-law account for these conditions. Its Clausius restriction excludes a composite process whose only net effect is transfer of heat from the colder reservoir to the hotter one. An admitted reversible reference between these reservoirs has `eta_ref = 1 - 300/600 = 1/2` and can run backward. This is a theoretical reference; no claim of a finite-power reversible laboratory device is needed.

Choose cancellation of the work exchange. A backward reference consuming the proposed 60 J extracts 60 J from the cold reservoir and delivers 120 J to the hot reservoir. The compatible exchanges combine as follows; positive entries increase the named store.

| Store or component | Proposed engine | Backward reference | Net change |
| --- | --- | --- | --- |
| Hot reservoir | -100 J | +120 J | +20 J |
| Cold reservoir | +40 J | -60 J | -20 J |
| Work store | +60 J | -60 J | 0 |
| Both devices | Each completes its cycle | Each completes its cycle | Restored |

The net process transfers 20 J from cold to hot with no other change. It violates the selected restriction. The argument uses only the proposed exchanges and cyclic condition, so changing the candidate's internal mechanism cannot repair it within this class.

For a general positive requested work `W`, the backward reference requires `Q_hot_ref=W/eta_ref`. If `W > eta_ref*Q_hot`, then `Q_hot_ref > Q_hot`; canceling work again produces the prohibited cold-to-hot transfer. Therefore:

~~~text
W <= eta_ref*Q_hot = (1 - T_cold/T_hot)*Q_hot.
For the stated inputs: W <= 50 J.
~~~

The practical result redirects the design question to work below this bound or to a change in the stated resources. It does not supply the design that attains a chosen value, its power or its operating cost.

**Change the allowed physical operation.** Suppose the proposed device may also receive 20 J of external work. A forward reversible reference producing 40 J from 80 J of hot-reservoir heat, together with routing those 20 J through the work store, can supply 60 J gross output. The net work produced is 40 J. The denominator and net exchange must now reflect the actual question; this construction supplies no engine producing 60 J net work from the original 100 J alone. If exactly 100 J must still be taken from the hot reservoir, an admitted additional transfer of 20 J from hot to cold accounts for the remainder. The total cold-reservoir gain is 60 J, and both laws permit the resulting exchanges. The changed resource condition opens a construction rather than altering the earlier bound.

For a microscopic proposal with initial correlations or a nonthermal auxiliary, use the physical account appropriate to those resources. A reservoir-only calculation leaves their contribution out. The source comparison in :11 identifies a current treatment; it does not prescribe the same generalized formula for every macroscopic device.

### PHY.3:5.2 - Test copying across inputs while allowing auxiliary outputs {#test-copying-across-inputs-while-allowing-auxiliary-outputs}

**Question.** Can one device take one input qubit in an unknown pure state and produce two perfect copies on every run? The device can use an auxiliary prepared independently of the input, and its final auxiliary state may depend on that input. Discarding an auxiliary is allowed.

Use the standard quantum description of a deterministic operation. Include the device's environment and any measurement records in the description of the complete process. A fixed mixed auxiliary preparation can be purified by adding a reference system. The total evolution can then be represented by one isometry `V`, which preserves inner products. This includes deterministic operations obtained by interaction and later discarding part of the system; it does not impose that the visible two-qubit map itself be unitary. If both required output copies are pure, their joint output factors from the remaining pure total state.

Choose two distinct nonorthogonal input states `|a>` and `|b>`. Let `|0>` be the blank second qubit and `|e>` the fixed initial auxiliary. Perfect copying would require:

~~~text
V(|a>|0>|e>) = |a>|a>|e_a>
V(|b>|0>|e>) = |b>|b>|e_b>.
~~~

The final auxiliary states are deliberately allowed to differ. Define `s=abs(<a|b>)`, with `0<s<1`, and `r=abs(<e_a|e_b>)`, with `0<=r<=1`. Taking inner-product magnitudes before and after the same isometry gives:

~~~text
s = s*s*r.
Dividing by s>0 gives 1=s*r.
But s*r <= s < 1.
~~~

The requirements are inconsistent. For the concrete pair `|a>=|0>` and `|b>=(|0>+|1>)/sqrt(2)`, `s=1/sqrt(2)` would require `r=sqrt(2)`. That exceeds the allowed overlap of normalized auxiliary states. More unobserved auxiliary output cannot make this deterministic perfect copier possible under the stated account.

This is a physical restriction on one operation across its input family. The mathematical step is preservation of an inner product; the physical work is establishing why the candidate devices admit that common description with the stated preparation. Showing failure of one guessed gate arrangement would leave this broader question unanswered.

**Change the input family.** Restrict it to the computational-basis states `|0>` and `|1>`, with a blank second qubit `|0>`. Controlled-NOT gives `|0>|0> -> |0>|0>` and `|1>|0> -> |1>|1>`. The same arrangement therefore copies every input in that restricted family. A different known orthogonal pair can first be mapped to that basis, copied, and mapped back on both outputs.

**Change the performance instead.** If failed runs may be discarded, the accepted operation is conditioned on an outcome and the all-runs argument no longer directly characterizes its normalized successful output. One must specify the allowed input set, success probability and failure output, then derive their restrictions. Allowing imperfect copies likewise changes the output relation and requires an accuracy question. The present result identifies why either revised problem differs; it supplies no unexamined claim that a desired success rate or accuracy is achievable.

## PHY.3:6 - Bias-Annotation {#bias-annotation}

The method corrects two live errors: treating one device's failure as a prohibition on every mechanism, and applying a quoted prohibition after its resource or input conditions have changed. Its own principal risk is selecting a convenient physical description that omits an allowed device or contribution. Keep the coverage argument next to the conclusion and use a changed-condition return to expose what the result actually depends on.

The worked proofs assume established classical thermodynamics and standard quantum operations in their stated regimes. Their conditional strength should remain visible when a research question concerns the adequacy of those theories themselves. A formal contradiction identifies incompatible premises; it does not choose by itself which empirical premise to revise.

## PHY.3:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Failure in use | Repair |
| --- | --- | --- |
| A limit quoted without its physical preparation | A bound derived for two reservoirs is applied to a device consuming an additional resource. | Recover the complete transformation and derive the applicable restriction. |
| An algebraic inverse treated as an available apparatus | The comparison depends on a reverse process whose required preparation or control was never admitted. | Establish the physical reference operation before using its cancellation. |
| Failure of one construction promoted to impossibility | Another permitted coupling or auxiliary lies outside the calculation. | Give a covering physical description or restrict the conclusion to the analyzed class. |
| Input-specific devices hidden inside one-device wording | A calculation selects a separate operation after knowing each supposedly unknown input. | Hold the common device and allowed information fixed across the input comparison. |
| Reset or ancillary change omitted | Apparent cyclic performance consumes a stored resource or accumulates a consequential change. | Include that state change and the reset required by the actual repeatability condition. |

## PHY.3:10 - Architectural Rationale {#architectural-rationale}

The complete transformation is the shared object of the two comparison constructions. It makes hidden resources and restoration conditions available to reasoning, while leaving the internal mechanism open. Reference cancellation reduces a proposal to a constrained composite effect. Input comparison constrains what one operation can do across alternatives. These differences explain the choice in :4.3; neither construction is a compulsory stage of the other.

The physical premise gives the mathematical operation its bearing on a device. A conserved sum or preserved inner product can be studied mathematically without that interpretation. Conversely, knowing the name of a physical principle does not yet specify the permitted exchanges, preparation or input family. The method supplies this physical construction and uses the existing mathematical and common inquiry methods for their contributions.

An ideal reference helps bound real proposals when its admitted operations and the coverage relation are explicit. It serves a different purpose from a realistic simulation of one device. Both kinds of account can remain useful in the same inquiry: the bound directs construction, and the constructed mechanism reveals further practical restrictions. The explanation of a failed proposal can also generate the next problem by identifying a consequential change of premise.

## PHY.3:11 - SoTA-Echoing {#sota-echoing}

**Reversible-reference comparison.** [David Tong, Statistical Physics, §4.3.1-4.3.2](https://davidtong.org/pdfs/teaching/statistical-physics/statphys4.pdf) gives the established Carnot comparison and the thermodynamic temperature ratio. It is a historical methodological anchor for composing processes and canceling exchanges. The pattern uses the construction beyond a particular working substance.

**Input comparison with auxiliaries.** [Peter Shor, Quantum Computation, lecture 5](https://math.mit.edu/~shor/18.435/oldlectures/lecture5.html) presents the no-cloning comparison and explicitly includes an input-dependent ancillary output. The present worked case spells out the total-process interpretation, overlap bound and changed-input return. The classical thermal and quantum arguments exemplify different physical restrictions and different comparison operations.

**Resource conditions in current thermodynamics.** [Aguilar and Lutz, Correlated quantum machines beyond the standard second law, version 2 (2025)](https://arxiv.org/html/2409.07899v2) analyzes initial correlations, nonthermal resources, interaction energy and changes remaining after a driving cycle. These contributions explain why a reservoir-only efficiency claim can need a different account. Its microscopic assumptions determine where its generalized expressions can be used.

**One occurrence and repeatable performance.** [Marletto, Deutsch and Vedral, Tests of constructor theory (2026), §1.4 and §3.2](https://arxiv.org/html/2606.07352v1) develops the distinction between an allowed evolution and a device able to repeat a specified transformation, including the difference between reversing dynamics and supplying a reusable inverse operation. The pattern adopts that problem distinction. The article's new constructor-theoretic principles are research proposals with their own tests; they are unnecessary premises for the two established arguments above.

The synthesis selects operations for constructing a physical limitation and reopening it under changed conditions. It does not require one universal physical resource theory. A new account of the permitted operations, an omitted resource or a changed performance condition is a reason to revisit the affected argument and its source premises.


## PHY.3:End {#end}
