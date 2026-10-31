# Practical Data + AI engineering portfolio

Started: 23 October 2026.

Build reliable data systems and focused AI tools for recurring operational
problems. Each project should have a clear user, a reproducible failure mode,
meaningful verification, and an explanation of the engineering tradeoffs.

## Project focus

Latest October 31 update: Bhargav returned to the Cue-like Windows assistant.
[CueDesk](https://github.com/VSBhargav5/CueDesk) is the active sprint; StudyFrame,
RoleWeave and SettleTrace are paused. CueDesk retains its upstream attribution.
Screen selection and explicitly reviewed AI questions are in development; real
screen capture, model usefulness and meeting workflows require validation.

| Project | Operational problem | Evidence to build | Status |
| --- | --- | --- | --- |
| [CueDesk](https://github.com/VSBhargav5/CueDesk) | Screen-assisted study and coding on Windows | Reviewed capture, explicit AI request, personally verified usefulness | Active; real screen and provider trial remain |
| [StudyFrame](https://github.com/VSBhargav5/StudyFrame) | Asking for study/coding help on Windows repeatedly requires assembling context | Bounded screenshot crop/restore, deliberate provider send/cancel, reviewed follow-ups, personally verified usefulness | Paused; [v0.2 screenshot focus](https://github.com/VSBhargav5/StudyFrame/pull/4); 70 offline tests; live validation and usefulness gate remain |
| [RoleWeave](https://github.com/VSBhargav5/RoleWeave) | Relating job requirements to defensible career evidence and application decisions | Reviewed claims, exact posting quotes, separate job markets, personally usable workflow | Set aside by user; nine offline tests; full UI and tailoring planned |
| [SettleTrace](https://github.com/VSBhargav5/SettleTrace) | A custom merchant ledger, processor activity, and bank deposits can disagree | Exact-money contracts, source-row evidence, verified export mapping, operator feedback | Paused; [v0.3 mapping and observation evidence merged](https://github.com/VSBhargav5/SettleTrace/pull/3) |
| [PromptGuard](https://github.com/VSBhargav5/PromptGuard) | AI prompt changes can silently break previously working cases | Coverage-aware comparisons, labeled failure examples, repeatable evaluation, external pilot feedback | Reliability sprint completed; [merged work](https://github.com/VSBhargav5/PromptGuard/pull/2) |
| [LMS ETL](https://github.com/VSBhargav5/LMS-ETL-PIPELINE) | Missing, duplicate, or late events can undermine learner scores and reports | Known expected results, idempotent reruns, controlled crash recovery, measured workloads | Next engineering sprint; review the existing architecture audit first |
| [BlastPath](https://github.com/VSBhargav5/BlastPath) | Reviewers need a traceable explanation of downstream Python change impact | Representative fixtures, measured misses and false positives, honest dynamic-import limitations | Later candidate |

Keep one implementation sprint active. Existing DecisionLog, OpenLoop, and Nifty
projects remain available while these priorities are evaluated.

StudyFrame remains an independent Python project. CueDesk is the separate,
GPL-attributed Cue adaptation selected for the current sprint. The current
screen-study path requires deliberate capture preview and explicit send; the
inherited meeting assistant is not yet integrated into that path. No live model
call or personal screen capture was made during implementation. Product demand
and usefulness remain unvalidated.

## First 90 days

This is a sequence of evidence gates. Scope and dates can change when the
engineering or user feedback calls for it.

| Window | Work | Completion evidence |
| --- | --- | --- |
| Days 1-14 | Build CueDesk's focused personal study MVP; SettleTrace remains paused | Selected screenshot preview, explicit provider request/cancel, a real answer checked by the user; real capture and provider trial remain |
| Days 15-28 | Review CueDesk MVP usefulness and switch back to SettleTrace's next evidence gate | Personally observed study workflow; permitted export/operator review for SettleTrace; no false completeness claims |
| Days 29-42 | Review the LMS audit and demonstrate scoring invariants, duplicate-safe reruns, and recovery | Known results, controlled failure and recovery, measured workload and environment |
| Days 43-56 | Choose one narrow product experiment from observed recurring pain | Repeated problem observed independently; at least one person tries a pilot |
| Days 57-70 | Improve the pilot's costly or unreliable step | Observed task completion, measurable improvement, repeatable setup and recovery |
| Days 71-90 | Publish two strong case studies and evaluate a paid pilot if value is demonstrated | Runnable artifacts, defensible tradeoffs, truthful outcomes and observed usage |

If users cannot be reached, prioritize excellent engineering case studies and
keep product demand explicitly unvalidated.

## First principles alongside implementation

- CueDesk: capture consent, preview-to-payload identity, cancellation and provider boundaries.
- StudyFrame: byte snapshots, bounded image decoding, input validation, UI state,
  local preparation versus inference, deliberate transmission and answer quality.
- SettleTrace: integer money, signs, joins, identity, currency boundaries,
  observation windows, fingerprints, and evidence versus inference.
- PromptGuard: set comparisons, changing denominators, observed versus missing
  outcomes, contracts, deterministic checks, and limits of model evaluation.
- LMS: idempotency, event time, checkpoints, consistency, transactions, indexes,
  bounded concurrency, and throughput versus latency.
- BlastPath: graphs, dependency direction, traversal, static-analysis limits,
  false positives, and false negatives.

Start with the invariant and a failing example. Implement a small behavior,
verify it, and explain what it still cannot guarantee.

## Product experiments

These are hypotheses, not validated markets or revenue claims.

- A bookkeeper maintains custom joins across a merchant ledger, processor, and
  bank. Test an offline investigation pack and a custom mapping/setup offer.
  Stripe already offers [payout reconciliation](https://docs.stripe.com/reports/payout-reconciliation);
  a working feature list does not prove a reason to switch or pay.
- A small AI consultancy needs an evidence pack when handing an extraction or
  support workflow to a client. Test a manual evaluation setup before hosting.
- An education provider spends time investigating stale or inconsistent reports.
  Test a focused diagnostic or implementation service before building a platform.
- A Python team struggles to identify affected dependencies and reviewers.
  Establish useful accuracy before proposing a paid CI integration.

Compare each proposal with the user's current workflow and existing tools.
Promptfoo already provides evaluation and CI quality gates; another feature list
does not establish differentiation. See the
[Promptfoo CI documentation](https://www.promptfoo.dev/docs/integrations/ci-cd/).

## Evidence for every featured project

1. A specific user and recurring problem.
2. A fresh-checkout demo with synthetic or appropriately licensed data.
3. A reproducible failure and recovery story.
4. Measured results with commands, workload, environment, and limitations.
5. Clear tradeoffs and known unsupported behavior.
6. A case study based on completed, verified work.

Keep changes and commits coherent. Progress means useful behavior and evidence,
not a target number of contribution squares.

Follow the [build log](build-log.md) for completed work and verification.
