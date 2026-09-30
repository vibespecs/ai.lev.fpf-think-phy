# PHY.10 - Construct a Physical Test That Separates Rival Accounts: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *Physical Thinking DPF* (22 September 2026), `Foundational Thinking DPF Suite/PHYSICAL-THINKING-DPF.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## PHY.10:5 - Archetypal Grounding {#archetypal-grounding}

### PHY.10:5.1 - Change speed to separate two drag accounts {#change-speed-to-separate-two-drag-accounts}

A specimen moves through the same fluid at an imposed positive speed v. In the proposed operating range, account L takes the opposing force magnitude to be `F=b v`; account Q takes it to be `F=c v²`. The coefficients are positive and constant under their respective accounts.

At v=1 m/s, an earlier calibrated force comparison places the true drag between 0.95 and 1.05 N. Thus L permits b between 0.95 and 1.05 N·s/m, while Q permits c between 0.95 and 1.05 N·s²/m². Both explain that observation.

A repeat at the same speed leaves this disagreement intact. Instead impose v=2 m/s while retaining specimen geometry and the fluid conditions on which the coefficients depend. L predicts a force between 1.9 and 2.1 N; Q predicts between 3.8 and 4.2 N. With an additional bounded force-readout error of ±0.1 N, the possible indications lie in [1.8,2.2] N and [3.7,4.3] N. They are disjoint.

The drive and readout must sustain that comparison. Under Q the required mechanical power can reach 8.4 W, since P=Fv. A 5 W drive cannot establish the proposed steady speed for every admitted Q response. A 10 W drive at that speed can meet this particular power demand, while its other operating limits remain relevant.

Suppose the comparison returns 2.05 N. It is compatible with L and incompatible with Q under the stated ranges and conditions. A return of 2.9 N instead disagrees with both. It prompts examination of the retained physical regime, parameter constraints and readout; it does not justify selecting whichever nominal curve is closer.

Heating or a geometry change can make a coefficient vary between runs. If that effect can span the separation, the test no longer has the same interpretation. Restore the shared condition, include the changed dependence or choose another contrast. Increasing speed without this return can defeat the very accounts being compared.

### PHY.10:5.2 - Change a drive that makes storage and conduction coincide {#change-a-drive-that-makes-storage-and-conduction-coincide}

A two-terminal element is driven with `V(t)=V_0 exp(t/tau)`. One proposed account is an ideal resistor, `I=G V`. Another is an ideal capacitor, `I=C dV/dt`, prepared with charge C V_0 at the start of the recorded ramp.

Since `dV/dt=V/tau`, choosing C=G tau makes the complete current traces identical during this ramp. More accurate recording of that same drive cannot distinguish the accounts.

Use V_0=1 V, tau=2 s, G=1 mS and C=2 mF. Stop increasing the voltage when it reaches 2 V and hold it there. After the drive and readout have settled, the resistor predicts 2 mA and the ideal capacitor predicts zero current. The change removed dV/dt while retaining V.

The waiting interval must be interpreted physically. A source with finite output resistance and a detector with finite response can create a transient after the change. Include it or choose a readout time after its consequential effect. The ideal predictions also exclude a significant leakage path.

Now suppose the held-voltage current is 0.6 mA, while the earlier ramp still has I/V=1 mS. The ideal pair is inadequate for these records. A parallel conductance and capacitance give

`I=G V+C dV/dt`.

The hold gives G=0.3 mS. Substitution into the ramp relation `G+C/tau=1 mS` gives C=1.4 mF. The test has opened a physically different account in which conduction and storage coexist. These two records determine its two parameters under the stated idealization; they do not establish that this account suffices at every frequency or voltage.

The resulting distinction changes use. A continuously held voltage dissipates power through the conductance, while the capacitance stores charge and supplies a transient response. Subsequent pulse or frequency use can therefore ask a question that the original exponential ramp could not resolve.

### PHY.10:5.3 - Refocus a hidden physical difference {#refocus-a-hidden-physical-difference}

A prepared ensemble has a transverse phase signal. Consider two idealized accounts of its free decay. In account S, each member has a fixed frequency offset delta, drawn from the Lorentzian density

`p(delta)=Gamma/[pi (delta²+Gamma²)]`, with Gamma>0.

Each phase advances by delta t. Averaging over the ensemble gives `M_S(t)=exp(-Gamma t)` for t≥0. The individual offsets remain fixed even though the mean signal decays.

In account D, the phase instead has independent Gaussian increments with variance `2 Gamma dt` over an interval dt. This Markov dephasing gives the same free signal, `M_D(t)=exp(-Gamma t)`. The two accounts agree on this free-decay observation.

Apply a refocusing rotation at time tau and read the signal at 2 tau. In the ideal pulse comparison, the sign of phase accumulation is reversed for the second interval. Under S, each accumulated phase becomes `delta tau-delta tau=0`; the ensemble signal returns to 1. Under D, the two intervals have independent phase increments. Subtracting them leaves variance `4 Gamma tau`, so the signal remains `exp(-2 Gamma tau)`.

For Gamma=10 s⁻¹ and tau=0.1 s, the predicted refocused signals are 1 and approximately 0.135. The intervention exposes a difference hidden by the equal free decays.

A physical pulse has finite duration, range and accuracy. Its response over the occupied frequency range, other relaxation during the sequence and readout error must be included where they can change this separation. For illustration, if their combined effect on each predicted normalized signal is bounded by 0.05, the predicted indication intervals around 1 and 0.135 remain disjoint. This bound is a condition of that proposed implementation, not supplied by the ideal calculation.

If the pulse cannot refocus a consequential part of the ensemble, a small return can have that cause as well as irreversible dephasing. Change the pulse or reference comparison, retain its bounded effect, or leave the interpretation conditional. A partial echo can also motivate an account with both static variation and changing noise. The performed comparison then guides which hidden dynamics to retain.

## PHY.10:6 - Bias-Annotation {#bias-annotation}

The cases use controlled laboratory comparisons and idealized response laws. Astronomical, geological and other field questions can require naturally available contrasts whose backgrounds cannot be independently fixed. The relevant physical premises must then support the observational comparison.

A finite candidate set can exclude a useful account before the test begins. A result inconsistent with every candidate, or a new physical dependence exposed by the experiment, can justify developing the set. It need not become a competition among the original labels.

## PHY.10:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | What fails | Repair |
| --- | --- | --- |
| Better data from an uninformative drive | The resistor and capacitor retain identical ramp traces. | Change the physical input that made the laws coincide. |
| Nominal curves treated as complete accounts | Adjustable coefficients make the predicted response families overlap. | Compare the responses allowed by the admitted parameter information. |
| Increase the drive until the curves separate | A new physical regime defeats the retained laws or apparatus. | Derive the changed interactions and check attainable preparation. |
| Distinct states, identical indications | The detector erases the predicted difference. | Change the measuring interaction or readout. |
| Nearest curve must win | A response outside both admitted ranges is forced into the original pair. | Locate the failed premise and develop another account when needed. |
| A failed echo proves irreversible loss | Control error or an unaddressed frequency range can suppress the return. | Include or distinguish the consequential pulse and readout effects. |

## PHY.10:10 - Architectural Rationale {#architectural-rationale}

B.5.TC compares how theoretical accounts answer a working question. This method develops a physical consequence of that comparison: how a preparation or interaction can expose the disputed dependence. PHY.9 supplies an observable readout; the statistical or mathematical design uses that physically realizable relation.

Equal unperturbed responses can conceal different retained state. Changing a drive or reversing an interaction therefore supplies more than another sample of the old observation. It asks the accounts how the physical system responds to a different operation. That response can also reveal how the system might be controlled or used.

The test retains the apparatus and preparation because they participate in the consequence being compared. This makes an unsuccessful comparison informative: a return can change the subject account, the experimental construction or their mathematical description, according to which premise failed.

## PHY.10:11 - SoTA-Echoing {#sota-echoing}

[Huan, Jagalur and Marzouk, *Optimal experimental design: Formulations and computations*](https://arxiv.org/abs/2407.16212), Acta Numerica (2024), with corrections and clarifications in the 2026 author revision, distinguishes design for parameter information, prediction and model discrimination. Its sections 2.2 and 6.1 retain uncertain influences and the possibility of model misspecification. These distinctions enter :4.1 and :4.4-.5. A design based on a supplied model set does not establish that the set contains an adequate account.

For the drag comparison, the disjoint force ranges give a sufficient design without a numerical optimizer. When feasible inputs are numerous and predicted records are uncertain, an experimental-design method can compare their expected contribution. Its advantage depends on a useful objective and credible response models. The cost of constructing and evaluating that optimization matters alongside the cost of the experiment.

[Vezvaee et al., *Fourier transform noise spectroscopy*](https://www.nature.com/articles/s41534-024-00841-w), npj Quantum Information (2024), develops noise reconstruction from free-induction and spin-echo measurements. The adopted physical contribution is changing how a prepared probe couples to temporal structure. The paper's spectral reconstruction relies on its pure-dephasing and stationary Gaussian-noise setting; those assumptions are not imposed on the Lorentzian static-offset construction in :5.3.

For a noise question within that setting, the paper compares reconstruction from simple sequences with methods requiring many pulses. It also exposes different limitations: finite pulse timing, a restricted accessible frequency range and sensitivity of time derivatives to measurement error. Choosing more elaborate control is therefore not a general improvement. The simpler sequence can be sufficient for the needed distinction, while a different noise or control question calls for another method.

The three numerical cases are constructed comparisons under stated physical laws. Their purpose is to exhibit the changed preparation, response and interpretation; they are not reports of performed experiments. New physical effects or apparatus limits change the corresponding case premises.


## PHY.10:End {#end}
