# PHY.5 - Choose an Effective Physical Description by Scales and Couplings: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.5:5 - Archetypal Grounding {#archetypal-grounding}

### PHY.5:5.1 - Keep a motor's torque while eliminating fast current dynamics {#keep-a-motor-s-torque-while-eliminating-fast-current-dynamics}

Consider an ideal linear motor over a range in which resistance R, inductance L, inertia J, damping b and conversion constant k are positive and constant. In consistent SI units, use the same k for torque per current and back voltage per angular speed:

`L*i' = V - R*i - k*omega`

`J*omega' = k*i - b*omega`

The electrical and mechanical balances describe the assumed device, including its load in J and b. Saturation, variable load or a different drive would require the corresponding physical relations.

Suppose the work needs the slow speed response. The electrical relaxation time is `tau=L/R`. The current toward which the electrical part relaxes is `q(t)=(V(t)-k*omega(t))/R`. Replacing i by q gives

`J*omega' = (k/R)*V - (b+k^2/R)*omega.`

The eliminated current still supplies driving torque and additional damping. The slow response time of this candidate is `J/(b+k^2/R)`. Compare tau with that time and the drive's variation time.

To examine the neglected response, set `e=i-q`. The full electrical equation gives `tau*e'=-e-tau*q'`. If `|q'|<=K` on the interval, integration yields

`|e(t)| <= |e(0)|*exp(-t/tau) + tau*K*(1-exp(-t/tau)).`

The bound on q' can come from `|q'|<=(|V'|+k*|omega'|)/R` and the allowed drive and acceleration, using the full physical account where needed. A bound inferred only by assuming the proposed approximation would leave that assumption unresolved.

For example, let R=2 ohms, L=0.02 henry, k=0.1 in the stated SI convention, J=0.02 kg m² and b=0.01 N m s per radian. Then tau=0.01 s and the candidate slow time is about 1.33 s. With `|e(0)|<=0.5` ampere and K=1 ampere per second, the current departure at 0.05 s is at most 0.01331 ampere, giving a torque departure at that instant of at most 0.001331 N m relative to kq.

The slow speed error is a different output. With the same initial speed and drive, let delta be full speed minus reduced speed. It satisfies

`J*delta' + (b+k^2/R)*delta = k*e.`

Let `B(s)` denote the current-departure bound above. Since the initial speed difference is zero and the response kernel is positive, integration gives

`|delta(t)| <= (k/J)*integral_0^t exp(-(b+k^2/R)*(t-s)/J)*B(s) ds.`

For the stated values, this speed-departure bound at 0.05 s is about 0.026064 rad/s, hence less than 0.02607 rad/s. An allowed error of 0.03 rad/s therefore permits the reduced calculation for that speed reading. The integral carries the earlier transient into the answer; the small current departure at the final instant alone would not give this bound.

**Changed work.** If the next question concerns torque immediately after switching, the bound includes the initial current departure. Use the electrical transient. If the drive varies on the electrical relaxation time, recompute its departure instead of extending the slow-drive approximation. These returns change which physical response is retained.

### PHY.5:5.2 - Decide when a chain can be treated as a continuous medium {#decide-when-a-chain-can-be-treated-as-a-continuous-medium}

Consider an infinite ideal one-dimensional chain with identical masses m, spacing a and linear springs of stiffness kappa. Each mass moves a small distance u_j from its reference position. The balance is

`m*u_j'' = kappa*(u_(j+1)-2*u_j+u_(j-1)).`

For waves with wavenumber q in `0<q*a<pi`, substitution of a sinusoidal wave gives

`omega^2 = (4*kappa/m)*sin^2(q*a/2).`

For wavelengths long compared with a, expanding the neighboring displacements gives the continuum equation `u_tt=c^2*u_xx` with `c=a*sqrt(kappa/m)`. It predicts both phase and group speed c. The chain's phase speed divided by c is `sin(q*a/2)/(q*a/2)`; its group speed divided by c is `cos(q*a/2)`. Expanding those ratios gives `v_phase/c = 1-(q*a)^2/24+O((q*a)^4)` and `v_group/c = 1-(q*a)^2/8+O((q*a)^4)`, exposing their different first corrections.

At q*a=0.2 these ratios are about 0.99833 and 0.99500. A half-percent allowance for these speeds accommodates this ideal comparison, subject to the question's waveform and other physical premises. The group-speed difference is already larger than the phase-speed difference.

**Changed work.** A disturbance containing wavelengths near the shortest traveling waves of the chain probes q*a near pi. The chain's group speed tends to zero, while the continuum account keeps c. A question about that disturbance's propagation requires retaining the discrete dispersion or an adequate extension. Making the computation of the uncorrected continuum equation more accurate cannot recover the omitted physical dependence.

This case concerns an ideal linear chain. It demonstrates choosing spatial resolution from the wave that matters. It supplies no claim that every material, boundary or large deformation obeys the same chain law.

### PHY.5:5.3 - Retain fluctuations after fast velocity has relaxed {#retain-fluctuations-after-fast-velocity-has-relaxed}

For a one-dimensional Brownian particle in a uniform equilibrium bath, take mass m, drag coefficient gamma and temperature T, with no applied force. The underdamped account has position x, velocity v and thermal forcing. Let `tau=m/gamma` and `D=k_B*T/gamma`. With an initially equilibrated velocity, its velocity covariance is `(k_B*T/m)*exp(-|t-s|/tau)`.

Integrating that covariance over the two times gives

`E[(x(t)-x(0))^2] = 2*D*(t-tau*(1-exp(-t/tau))).`

At times large compared with tau, the overdamped diffusion description gives `2*D*t`. Its omitted contribution to this mean-square displacement is bounded by `2*D*tau`. This calculation states which long-time consequence the reduction preserves.

Setting the mean velocity to zero and deleting the forcing instead gives no displacement spread. The unresolved bath continues to transfer random impulses after the velocity's preparation has relaxed. For the displacement distribution, retain their diffusion effect.

**Changed work.** Change the bath to a spatially varying temperature and ask about entropy production. The uniform-bath calculation no longer answers the question. Celani and coauthors show a further distinction: under their smooth-temperature and small-inertia conditions, the overdamped position process has the appropriate limit, while the mean rate of entropy production retains an additional positive contribution absent from the naive overdamped expression. Return to the thermodynamic observable and its limiting calculation. Position accuracy alone cannot decide that use. Their [2012 paper](https://arxiv.org/html/1206.1742v2) states the preparation and the contribution.

## PHY.5:6 - Bias-Annotation {#bias-annotation}

The worked calculations emphasize classical continuous-time descriptions with explicit laws. The method also applies to choosing physical states and interactions when only a constrained response or statistical account is available. In such cases the first result can be a qualified regime choice or a discriminating physical question.

Time-scale separation is especially convenient and can dominate the choice too early. The spatial chain and changed thermodynamic observable show other reasons to retain a contribution. Quantum coherence, rare transitions and collective behavior require their own physical grounds; the classical examples do not decide them.

## PHY.5:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Misstep exposed by the construction | Consequence | Repair |
| --- | --- | --- |
| Delete a fast part and its coupling together | The motor loses the torque and damping supplied by its adjusting current. | Substitute the part's response into the retained interaction. |
| Apply the settled response at every instant | The initial current and switching response disappear. | Carry the transient and propagate its effect into the requested output. |
| Match one propagation speed and assume the other matches | A continuum approximation can misstate the arrival of a wave packet. | Compare the dispersion and the output the disturbance uses. |
| Replace unresolved motion by its mean | The Brownian particle loses its displacement spread. | Retain the fluctuation contribution when the question uses that distribution. |
| Use a successful position reduction for a thermodynamic observable | A limiting position process can omit entropy production. | Reduce the observable and its physical exchanges with the dynamics. |

## PHY.5:10 - Architectural Rationale {#architectural-rationale}

This method organizes the choice by physical consequence and coupling. Comparing parameter sizes alone would miss how an omitted process enters the result. Starting from the most detailed available theory can impose work that the question does not need.

Effective-theory construction supplies a useful way to retain selected influences and improve an approximation systematically. Projection and coarse-graining show why unresolved motion can remain as memory and fluctuations. The observable-specific limit shows why their adequacy is judged at the receiving physical result.

MMP.9 owns the mathematical elimination; PHY.1 uses an effective account to compare changed physical arrangements; PHY.2 uses it when constructing an analogue. The contribution here is choosing and revising the physical resolution and remaining influence of unresolved processes. The motor, chain and Brownian particle demonstrate that contribution in different comparisons.

## PHY.5:11 - SoTA-Echoing {#sota-echoing}

[Stewart's introduction to effective field theory](https://ocw.mit.edu/courses/8-851-effective-field-theory-spring-2013/e4ebfd74257683c3efa47b240196c505_WB8r7CU7clk.pdf) (MIT, 2013, lecture transcript pp. 2-4) is a historical teaching source for selecting relevant degrees of freedom, scales and an improvable leading description. This pattern adapts that construction beyond its quantum-field setting. It retains the need to identify an expansion and its range; improvement by further terms remains conditional on that expansion being useful.

[Dalton and coauthors, Memory and Friction: From the Nanoscale to the Macroscale](https://doi.org/10.1146/annurev-physchem-082423-031037) (2025; [accessible manuscript, section 3](https://arxiv.org/html/2410.22588v1)) supplies the contemporary account of retained observables, memory-dependent friction and simulation through auxiliary variables. Adopt the distinction between eliminating explicit variables and discarding their influence. An instantaneous response saves computation when its conditions hold; resolved memory preserves effects that such a response misses. The review's stated projection, equilibrium and preparation conditions govern its particular equations.

[Celani, Bo, Eichhorn and Aurell](https://arxiv.org/abs/1206.1742) (2012) provide the observable-specific counterexample used in :5.3. Adopt the comparison of the physical result before and after the limit. Their thermal-gradient result qualifies an otherwise successful position reduction; it does not rule out overdamped modeling for the position questions it answers.

The synthesis combines controlled omission, retained coupling and use-specific comparison. It favors the least costly description that supplies the needed consequence under the established physical conditions. Memory kernels, white-noise diffusion and a fully resolved model are alternative constructions with different requirements, selected by the question.


## PHY.5:End {#end}
