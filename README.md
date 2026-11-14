# reveal-lab

A hostile benchmark, not a product. Earlier drafts called this `preference-lab`. One
idea, one name; `reveal-lab` is current.

> **Status: placeholder, research programme, starts after Project Tenter.** There is no
> code here yet. This file records the method, the end state and the showpiece.

## Why it exists

To let the central claim die cheaply, before anything is built on top of it. The method
is inherited from Witness Lab: freeze the claims, include hostile controls, and allow
the idea to fail.

**A failure here is publishable.**

## It has two jobs, not one

1. **Does inference improve decisions?** At equal disclosure and interruption budgets,
   does hybrid inference (stated plus revealed, carrying explicit uncertainty) beat both
   stated-only and revealed-only on **endorsed** regret? Endorsed regret is measured
   against what the principal accepts after seeing the outcome, not against predictive
   accuracy.

2. **Does the inference process change the person?** A system can surface options, ask
   questions, and repeat exposure until it manufactures a preference, then cite the
   resulting behaviour as evidence that the preference was there all along. Evidence
   produced after an intervention is evidence **conditioned on that intervention**.

The second job is the harder one and it was missing from the first draft.

## Controls that must be present

    shuffled history        context-free inference
    prompt-only LLM         recent-choice heuristic
    an oracle ceiling       a deliberately biased mediator

## Stressors

Choice-set changes, preference drift, contradictory statements, strategic misreporting,
constrained choice, coercive outside options, and naive source combination.

## Two instruments that must prove themselves first

- **Hidden endorsement.** If the synthetic latent objective is reachable by the learner,
  the benchmark measures itself and proves nothing. It then fails by producing pleasant
  numbers rather than an error, which is the worst way to fail.
- **The steering detector must be two-sided.** It must go red on a deliberately biased
  mediator and green on a neutral one. A detector that only ever fires, or never fires,
  is not a detector. Participant satisfaction is not a steering detector: published work
  found people preferred a facilitated process that measurably shifted outcomes without
  improving participation equality.

## Measures

Predictive calibration, ex-post endorsed regret, false-consent rate, human interruptions,
worst-served participant, privacy disclosure, steering delta, revocation time, and
lock-in caused by the system narrowing future choices.

## The end state

1. **A preregistered benchmark.** The claims, the measures and the analysis are frozen
   and published before any run.
2. **Synthetic principals.** Each principal has a hidden objective that the benchmark
   controls, so endorsed regret can be measured.
3. **The listed controls.** Every control above runs in every round.
4. **A two-sided steering detector.** It goes red on the deliberately biased mediator and
   green on a neutral one, and the benchmark publishes both results.
5. **A leaderboard of LLM mediators.** Each mediator gets the same principals, budgets
   and stressors.

## The showpiece

The leaderboard, plus a chart of the steering delta for each mediator. The chart shows
how far each mediator moves the principals from where they started, next to the biased
control and the neutral control.

## The invariants this programme inherits

These hold across every repository in the set. They are not decoration.

- **Legibility is not consent.** That something can be inferred does not make every use of it legitimate.
- **Inference is not authority.** An agent may believe I prefer X and still have no authority to do X.
- **Coordination does not require surrender.**
- A valid mandate is **necessary** for action. It is **not sufficient** for legitimacy.
- Use CRDTs to converge the record, not to converge the people.

## The type chain

No stage may impersonate the next. Each transition owes a two-sided test: red on the
illegal construction, green on the legal one.

    Fact
      -> PreferenceEvidence
      -> PreferenceHypothesis
      -> Endorsement
      -> Mandate
      -> Commitment
      -> Effect
      -> OutcomeReceipt

## Siblings

| Repository | Role |
|---|---|
| [accord-settlement](https://github.com/velvetmonkey/accord-settlement) | The session guard. Stops allowed actions from combining into a leak. |
| [accord](https://github.com/velvetmonkey/accord) | The protocol. Binding deals without disclosure of preferences. |
| [reveal-lab](https://github.com/velvetmonkey/reveal-lab) | The hostile benchmark for LLM mediators. |
| [seal](https://github.com/velvetmonkey/seal) | The finished authority boundary. One exact effect, one receipt. |

A planned essay, "Who can object?", covers agency law for agents and standing for
parties that a deal leaves out.

Licence: [Apache-2.0](LICENSE).
