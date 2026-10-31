# Build log

Entries distinguish shipped code, verification, limitations, and planned work.

## 31 October 2026 — RoleWeave research and first evidence review

The user requested a personal job-search tool inspired by Dossier and Jobleft,
and chose India/remote-from-India plus international relocation as separate
markets. Created [RoleWeave](https://github.com/VSBhargav5/RoleWeave), an original
Python repository with no upstream code/assets/history imported.
[Foundation PR](https://github.com/VSBhargav5/RoleWeave/pull/1) ·
[Implementation](https://github.com/VSBhargav5/RoleWeave/commit/d1a89b66676f2074efda1f2ece9e7ab89aa0d716) ·
[Research and plan](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/research-and-plan.md).

Reviewed upstream documentation for Dossier, Jobleft, JobOps, Resume Matcher and
Reactive Resume, plus Dossier fact-check/scoring source and Jobleft matching
integration/acceptance outcomes. Upstream claims were not independently tested.

First usable artifact: a standard-library Python CLI validates exact job quotes,
career-fact references and review flags, preserving unresolved requirements and
separate market labels. Input and posting hashes identify the reviewed data.
Nine local tests and a synthetic CLI run pass. Tested/published tree:
`a11fff76c1d451e8bfa6005a233bae58d2dfd61a`.
PR #1 is merged after all Windows/Linux Python 3.11/3.12 checks passed for both
branch and PR runs. Merge: `810e4481d7d764e126102787993ffcca75056d78`.

A selected fact is a human assertion, not verified truth, relevance or eligibility.
No ATS/hiring score, AI, discovery, tailoring, database, desktop UI or application
submission is implemented. Next: SQLite persistence and a small Windows review
interface. StudyFrame is held at its live-validation gate; SettleTrace stays paused.

## 29 October 2026 — StudyFrame deliberate AI study workflow

[PR #2 merged](https://github.com/VSBhargav5/StudyFrame/pull/2) ·
[Implementation](https://github.com/VSBhargav5/StudyFrame/commit/07cdb3f9dd7fc3770d92ecb95e4391d0daaf994a).

Added explicit OpenAI text/image requests, a masked session-only key field,
per-request review, asynchronous waiting, cancel, a 60-second deadline and bounded
response parsing. Original image snapshots are sent only after review. No
automatic retry, redirects, chat history or code execution. Failure preserves
inputs; stale replies cannot finish a later request. Cancellation cannot reverse
remote processing or charges. Entire image files include metadata.

49 tests pass locally, including native Windows widgets and 14 new offline
provider/UI regressions. All four PR CI jobs passed on Windows/Linux with Python
3.11/3.12. Synthetic native rendering was inspected. Tested/published tree:
`64de4530826174e2ec478a3d36ab4f0299f2ca31`.

No live API calls, paid tests or personal screenshot uploads were made. Mock
tests do not establish account access or answer quality. Next is an authorized
synthetic trial and personally verified study answer; SettleTrace stays paused.
[Practice exercise](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/ai-workflow.md).

## 29 October 2026 — StudyFrame original Python foundation

**Status:** [Merged into main](https://github.com/VSBhargav5/StudyFrame/pull/1).
[Implementation](https://github.com/VSBhargav5/StudyFrame/commit/c56659364b2593eb485d65673b0d2e040f6c7b1e) ·
[CI context fix](https://github.com/VSBhargav5/StudyFrame/commit/3437a5871c3735b6ce3b8e6d3740edb732bb8ef8) ·
[CI YAML fix](https://github.com/VSBhargav5/StudyFrame/commit/84059dee0b97bca5f7a156114ef2230215955084) ·
[Merge](https://github.com/VSBhargav5/StudyFrame/commit/5317f11bc5ba4936c4c83ac462c15f2c044dd576).

Bhargav changed direction to a new Python repository and a new name. StudyFrame
has original source and independent history; no Cue/CueDesk source, assets,
tests or Git history were imported. Cue is acknowledged as product inspiration.
CueDesk remains a separate historical fork. SettleTrace stays paused at v0.3.

Python 3.11+ and PySide6 Essentials 6.12.0 provide a local Windows study panel:
select a saved PNG/JPEG, inspect it, add code and a question, and prepare a
hint/explanation/debugging request. Image reads are bounded and decoded from the
same byte snapshot. JPEG orientation is applied. Pasted Python indentation is
preserved. Input edits invalidate the request; cancelled/failed replacement keeps
the prior image. Copy transfers text only; image interpretation is not connected.

Verification:

- 35 original tests passed locally, including native Windows Qt widget checks.
  Automated picker/clipboard checks use stubs and synthetic files.
- Python package build/install passed; the real native-rendered synthetic demo
  was visually inspected. Windows offscreen rendering had no fonts, so the demo
  selects native Windows rendering and rejects a fontless environment.
- [All four PR CI jobs passed](https://github.com/VSBhargav5/StudyFrame/actions/runs/40817801926)
  on Python 3.11/3.12 Windows/Linux, including package installation and demo render.
  Two initial workflow validation failures were corrected before merge.
- Final published and tested Git trees match:
  `ff25d5cf2ded47adf06f7cb36b65cd8a603bd7fd`.

[Run it](https://github.com/VSBhargav5/StudyFrame#run-on-windows) ·
[First-principles exercise](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/first-principles.md) ·
[MVP gates](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/mvp.md).

This is an offline foundation, not a finished AI MVP. No model call, OCR,
screen/audio capture, personal data upload or execution occurs. Manual native
file-dialog and physical clipboard integration remain unverified; synchronous
image decoding is not benchmarked. No installer, adoption, model quality,
learning completion, revenue or time-savings claim is made. Next: one reviewed
provider with an explicit payload preview, send/cancel and useful errors.

## 29 October 2026 — CueDesk personal Windows study foundation

Historical experiment: later the same day, StudyFrame became the active project
at the user's request. This record preserves what the CueDesk fork shipped.

**Status:** [Merged into main](https://github.com/VSBhargav5/CueDesk/pull/1).
[Implementation commit](https://github.com/VSBhargav5/CueDesk/commit/0d4f0b38e15db17bf2a5319432c193ac84eb2049) ·
[Merge commit](https://github.com/VSBhargav5/CueDesk/commit/86c1a4bb36e5fee23ea08ddb585ff523aa86b0c0).

Requested on October 27 and published on October 29 with actual timestamps.
Bhargav chose adapting Cue, with screen-based study/coding first and meetings
later. SettleTrace is paused at v0.3 until a usable CueDesk MVP and review.

CueDesk is a fork of [Blueturboguy07/cue](https://github.com/Blueturboguy07/cue),
pinned initially at `18f388712633bc37694450c55c4958fce63f8392` (v0.2.5).
Upstream history, GPL license, and attribution are retained. Cue already supports
Windows; inherited features are not original CueDesk work.

The new default study entry prepares validated hint/explain/debug requests from
typed question/context, previews/copies them locally, and invalidates stale
context. It has a sandboxed renderer and narrow IPC bridge. It does not infer an
answer, capture screenshots/audio, read upstream credentials/history, or call a
provider. The executable-disguising install hook and inherited agent/release
workflows were removed. Electron is pinned to 45.0.0.

Verification:

- 301 offline Node tests passed locally, including ten new request-contract tests.
  Most repository tests are inherited; this is not a claim of 301 new tests.
- A reproducible Electron smoke exercised the actual renderer/preload/IPC with
  synthetic text: preview, stubbed clipboard copy, stale-context invalidation,
  session clear, and no renderer Node access. Only this app's synthetic rendered
  panel was captured. Physical clipboard integration and an interactive foreground
  launch remain unverified.
- [All four post-merge CI jobs passed](https://github.com/VSBhargav5/CueDesk/actions/runs/40814844679)
  on Windows/Linux with Node 22/24; Windows/Node 24 also ran the native smoke.
- Fork Actions were disabled during bootstrap so inherited publishing/agent
  workflows could first be removed from main. Local checks passed before merge;
  the reviewed replacement read-only CI was then enabled and dispatched on main.
  No branch protection or required human review was bypassed.
- Published and tested trees match: `023c306987f00df4ceb517a8db75bdf22a0c99bb`.

[Setup and source map](https://github.com/VSBhargav5/CueDesk#readme) ·
[MVP gates and 60–90 minute exercise](https://github.com/VSBhargav5/CueDesk/blob/main/docs/CUEDESK-MVP.md) ·
[Origin and modification boundaries](https://github.com/VSBhargav5/CueDesk/blob/main/docs/CUEDESK-ORIGIN.md).

Next: explicit screenshot selection/preview, then one reviewed provider path with
send/cancel/errors; audio follows separately. The AI MVP, signed installer,
personally observed usefulness, answer quality, performance, revenue, and learning
completion are not established. No paid model calls or personal capture occurred.

This is one authored implementation commit, not the inherited fork history.
GitHub [does not count fork commits in the contribution graph](https://docs.github.com/en/account-and-profile/how-tos/contribution-settings/troubleshooting-missing-contributions#commit-was-made-in-a-fork);
the project evidence is reviewable in its own default-branch history.

## 26 October 2026 — SettleTrace v0.3 mapping and observation evidence

**Status:** [Merged into main](https://github.com/VSBhargav5/SettleTrace/pull/3).
[Merge commit](https://github.com/VSBhargav5/SettleTrace/commit/8868da356660c9d833c8b71f0eb1f84a8ff169e8).
This additional iteration was requested after v0.2 shipped on the same day.
Publication uses actual October 26 timestamps; no earlier daily target is claimed.

A matching net total does not explain the bank attribution or which exports were
selected. The operator can now prepare an explicit one-to-one bank mapping,
retain both original byte fingerprints and physical row evidence, replay the
mapping, and attach hash-bound UTC selection declarations to a report.
Sales capture, estimated automatic payout arrival, and bank posting are distinct
events. Declarations do not filter rows or establish complete coverage.

| # | Complete change |
| --- | --- |
| 1 | [Define hash-bound UTC observation declarations without completeness claims](https://github.com/VSBhargav5/SettleTrace/commit/7ff4deab8a922aae3572541c5eec587104066331) |
| 2 | [Map every bank record through explicit one-to-one payout evidence](https://github.com/VSBhargav5/SettleTrace/commit/a25cfdd25a56ee30ff632e40b503776fc12c95f9) |
| 3 | [Export canonical bank records with two-source row and byte audits](https://github.com/VSBhargav5/SettleTrace/commit/bb2930373f28d4130f0e86d9fb3db3773aadaa46) |
| 4 | [Carry observation declarations through reports verification and comparisons](https://github.com/VSBhargav5/SettleTrace/commit/e125cc962ae775753b1cf00e7a9933566f55d084) |
| 5 | [Replay bank mapping packs against original bytes and physical row evidence](https://github.com/VSBhargav5/SettleTrace/commit/7434b92b49c651635c82b83937f636eafcd1ed60) |
| 6 | [Bind verified declaration content and reject unsafe window payloads](https://github.com/VSBhargav5/SettleTrace/commit/46db77f5905d1dae3071168b79bda783595666dd) |
| 7 | [Ship v0.3 with portable mapping fixtures CI and an observation exercise](https://github.com/VSBhargav5/SettleTrace/commit/c6a63ba06cf0b209ab4d9b83e1a780b49ec11729) |

Verification:

- 210 local offline tests: 207 passed, three Windows symlink-capability skips.
- [All four PR CI jobs passed](https://github.com/VSBhargav5/SettleTrace/actions/runs/40318692617)
  on Python 3.11/3.12 across Windows and Linux, including installed CLI workflows.
- The clean synthetic mapping yields USD 76.50 and verifies original mapping,
  bank, sales, processor, and declaration bytes through the respective commands.
- The one-cent exercise first rejects a stale bank fingerprint without a report,
  then produces an explicit +1 minor-unit payout mismatch after a new declaration.
- Independent review found malformed Unicode labels and substituted embedded
  declaration content. Both were fixed with regression tests before publication.
- Every published snapshot matches its local tree. Final tree:
  `25edfa38975e8f72b25ede6d532563878a9035ea`.

[Contract and commands](https://github.com/VSBhargav5/SettleTrace/blob/main/docs/observation-contract.md) ·
[60–90 minute exercise](https://github.com/VSBhargav5/SettleTrace/blob/main/docs/observation-first-principles.md).

Limits: a mapping replay proves the stated join, not that attribution is true.
Dates and account scope are operator declarations; row timestamps, completeness,
real-account export validation, production performance, customer demand, revenue,
and learner practice remain unverified. FX, splits, and aggregates remain unsupported.
The next evidence gate is a permitted real-account import and operator review;
stronger completeness claims need event-time and coverage evidence.

## 26 October 2026 — SettleTrace v0.2 import and evidence workflow

**Status:** [Merged into main](https://github.com/VSBhargav5/SettleTrace/pull/2).
[Merge commit](https://github.com/VSBhargav5/SettleTrace/commit/73d77a15ad94fef0a8954b40d6eb5166b9ce61c6).
Work began on October 24 and was published on October 26 with actual GitHub
timestamps. The earlier day's target is not claimed as met by this later publication.

The operator can now ingest the documented Stripe `payout_reconciliation.itemized.7`
subset directly, validate contracts before writing files, export canonical
activity with an original-row audit, verify report/source fingerprints, and
compare observed exceptions between verified bundles. The HTML/JSON payout
ledger exposes matching, mismatched, mixed-currency, and unobserved payout sides.

Amounts convert exactly from major-unit decimal strings; original `charge_id`
supplies payment identity. Charges, refunds, and debit disputes are supported;
standalone fees, reversals, and other unsupported categories abort the import.
Fees attached to supported rows retain their signs. The adapter never silently
removes unsupported records or substitutes unrelated identifiers.

### Verification and limits

- 156 local tests: 155 passed and one Windows symlink-capability test skipped.
- [All four PR CI jobs passed](https://github.com/VSBhargav5/SettleTrace/actions/runs/40267368286):
  Python 3.11/3.12 on Windows/Linux, including installation outside the source
  tree and documented validate/reconcile/normalize/verify/compare workflows.
- [Post-merge CI passed](https://github.com/VSBhargav5/SettleTrace/actions/runs/40267485248).
- Synthetic dot/comma fixtures yield identical USD 76.50 results. The payout
  ledger and expanded source rows were inspected in a browser.
- Every published snapshot tree matches its local counterpart. Final main tree:
  `527b49aeb27832a2c8778a99e185152366d0c613`.
- Independent review caught multiline canonical audit-row drift, numeric
  serialization limits, excessive capture limits, and nested-JSON error handling.
  Regression coverage accompanies the fixes.
- The first CI run exposed a Python 3.12 parser-depth assumption in a test.
  The final test requires clean rejection regardless of the rejection stage.
- Sandbox file-rename restrictions require normal Windows permissions for local
  completion-marker tests; assertions were retained.

The input capture default is 16 MiB per file, configurable through 256 MiB.
Individual amounts support at most 128 minor-unit digits without rounding.
These are explicit bounds, not measured large-file performance guarantees.
Verification establishes recorded bytes and structure, not authenticity,
complete exports, a consistent date window, or correct bank attribution.

No real Stripe-account export, FX/split-deposit support, automatic bank mapping,
production performance, user adoption, revenue, or completed learning is claimed.
Next: an observation-window and bank-mapping contract, then an operator workflow
comparison if suitable data and authorization are available.

[The focused 60–90 minute session](https://github.com/VSBhargav5/SettleTrace/blob/main/docs/import-first-principles.md)
covers exact units, original-charge identity, source evidence, and what a
fingerprint cannot prove.

### Published implementation commits

The PR preserves 19 authored commits; its merge is counted separately.

| # | Commit |
| --- | --- |
| 1 | [Convert financial CSV decimals to exact integer minor units](https://github.com/VSBhargav5/SettleTrace/commit/ad11379ea470ac7c9d0619f4c06ff2c40797208b) |
| 2 | [Import versioned Stripe charge CSVs with explicit source identities](https://github.com/VSBhargav5/SettleTrace/commit/07f7417bb3a3c86fccc0c557ffebfeec745e7ff0) |
| 3 | [Trace imported refunds and debit disputes to their original charges](https://github.com/VSBhargav5/SettleTrace/commit/b726d5089ec05918f4b531f481310b981be5fb38) |
| 4 | [Expose per-payout balances and contributing source evidence](https://github.com/VSBhargav5/SettleTrace/commit/7379c4acbd704d74d8ed0f952c5de17984b81cfa) |
| 5 | [Parse explicitly selected comma-decimal report amounts without guessing](https://github.com/VSBhargav5/SettleTrace/commit/0371538bf525c5f6dce101f37086315ee4fb0e7b) |
| 6 | [Reconcile Stripe exports directly and record the selected import contract](https://github.com/VSBhargav5/SettleTrace/commit/c71cf63893cfa1164b14c5f86e224ffbf3febe2e) |
| 7 | [Reject known FX and Connect account ambiguities in raw imports](https://github.com/VSBhargav5/SettleTrace/commit/08e1970b26487d7e98842d13017eea20b969c2c4) |
| 8 | [Validate reconciliation input contracts without creating output files](https://github.com/VSBhargav5/SettleTrace/commit/5d5be499e3389bae8d6b9b4eb171a8604ef21de4) |
| 9 | [Export normalized processor records with a raw-source audit trail](https://github.com/VSBhargav5/SettleTrace/commit/47946a3d61d07697e8c8aef9b421159d572ec095) |
| 10 | [Make CI exit severity explicit while preserving review findings](https://github.com/VSBhargav5/SettleTrace/commit/b484b591d0f0944987f22e51a4bbd790ac27460e) |
| 11 | [Bound input capture before parsing while hashing the same bytes](https://github.com/VSBhargav5/SettleTrace/commit/7ba0787d6e0001fce7772d0b2fe65562f55cca09) |
| 12 | [Verify completed report bundles before trusting their recorded evidence](https://github.com/VSBhargav5/SettleTrace/commit/f92b5a67ab70523a05d4105d00f7f19fa7bc2d21) |
| 13 | [Reject impractical capture limits before Python file reads overflow](https://github.com/VSBhargav5/SettleTrace/commit/950095a7ad3048ee24a4a83bba55e6a120448c9c) |
| 14 | [Check original source content against report fingerprints](https://github.com/VSBhargav5/SettleTrace/commit/045d3431dfbf07443d2026168b566156539493a9) |
| 15 | [Compare verified exception packs without treating absence as resolution](https://github.com/VSBhargav5/SettleTrace/commit/25b22c873cf96b1d64f9aa2a6a42b114c2a07805) |
| 16 | [Ship reproducible Stripe import workflows and the v0.2 learning exercise](https://github.com/VSBhargav5/SettleTrace/commit/2208544107f646c731fcf35c6ae5b128ab9dfdd2) |
| 17 | [Keep normalization audit rows accurate for multiline identifiers](https://github.com/VSBhargav5/SettleTrace/commit/610e9009731ccb37e4087855d646d038cc56f2aa) |
| 18 | [Reject amounts beyond the portable serialization contract cleanly](https://github.com/VSBhargav5/SettleTrace/commit/5c98273401d5c767651f5b6f1ba366b8119b680b) |
| 19 | [Check malformed JSON rejection across Python parser versions](https://github.com/VSBhargav5/SettleTrace/commit/36a3eb25326b4a67780be9a2b0a32e70eda3c071) |

## 23 October 2026 — SettleTrace initial reconciliation engine

**Status:** [Merged into main](https://github.com/VSBhargav5/SettleTrace/pull/1).
[Implementation commit](https://github.com/VSBhargav5/SettleTrace/commit/c204987f07395c2b9fa6d2488d881b0760c36047).

A proposed merchant/bookkeeper workflow: investigate differences between a
custom captured-payment ledger, processor activity, and explicitly mapped bank
deposits. The offline CLI validates three canonical CSVs and produces HTML, JSON,
findings CSV, and a SHA-256 manifest. Amount mismatches include expected,
observed, and signed difference with source identifiers and physical CSV lines.

The clean synthetic example follows USD 100.00 through a USD 20.00 refund and
USD 3.50 of fees to a USD 76.50 deposit. The exception example yields four
findings, including a USD 1.00 charge difference and USD 0.50 payout difference.

Verification:

- 79 offline tests passed locally on Python 3.11 with normal Windows permissions.
- [All four PR CI jobs passed](https://github.com/VSBhargav5/SettleTrace/actions/runs/39932967700):
  Python 3.11/3.12 on Linux and Windows, including distribution installation,
  installed-command execution outside the source tree, and a generated report.
- [Post-merge CI passed](https://github.com/VSBhargav5/SettleTrace/actions/runs/39933117896).
- Published main exactly matches the tested tree; the local checkout is clean
  and synchronized. Both synthetic CLI outcomes were checked, and HTML was
  inspected in a browser.
- Independent review caught empty-input success, duplicate sale IDs, ambiguous
  source filenames, input fingerprint races, and partial manifest publication.
  These were fixed with regression coverage before merging.
- The sandbox blocks file renames; unchanged tests pass with normal Windows
  permissions. A first package check lacked the local wheel build command;
  isolated installation with the declared build dependencies succeeded.

[The first-principles session](https://github.com/VSBhargav5/SettleTrace/blob/main/docs/first-principles.md)
starts with integer minor units, signed refunds/fees, and payout sums. It is a
60–90 minute exercise to practice, not a claim of completed learning.

This version accepts canonical data only. Raw Stripe exports, automatic bank
mapping, dates/completeness, FX, split captures/deposits, and large-file
performance are outside the demonstrated scope. Missing observations are review
items, not proof of missing cash. Fingerprints identify parsed bytes, not their
authenticity or completeness. No real customer data, adoption, revenue, or
measured time saving is claimed. The next milestone is a verified export adapter.

## 23 October 2026 — PromptGuard reliability boundaries

**Status:** [Merged into main](https://github.com/VSBhargav5/PromptGuard/pull/2).
[Merge commit](https://github.com/VSBhargav5/PromptGuard/commit/f5382c3efa3405745332969722426b2bbd178a97).

The sprint addresses failures around configuration, selected cases, saved
evidence, comparison scope, and report serialization. Fourteen logical commits
keep each complete behavior with its regression coverage, followed by CI and
learning documentation.

| # | Shipped commit |
| --- | --- |
| 1 | [Reject impossible expectation thresholds and length ranges](https://github.com/VSBhargav5/PromptGuard/commit/12ebf98c1f8f8ebd0ea82dd9f25336ad35a2d60e) |
| 2 | [Enforce unique nonblank case IDs for every suite entry point](https://github.com/VSBhargav5/PromptGuard/commit/bce7d7e6d64b0cd642a6ca3f620239862180f0a4) |
| 3 | [Validate expectation regex syntax before model execution](https://github.com/VSBhargav5/PromptGuard/commit/10be43b29cb9634f00873f3305f1426746e82eea) |
| 4 | [Prevent empty case filters from running the whole suite](https://github.com/VSBhargav5/PromptGuard/commit/255190fe99ae3cb417416bbf8819e90ee3195795) |
| 5 | [Keep run ID reads and writes inside the run store](https://github.com/VSBhargav5/PromptGuard/commit/fc3543009d7fb80804db881bf3169a5e42fd7e0b) |
| 6 | [Reject ambiguous run prefixes with actionable CLI errors](https://github.com/VSBhargav5/PromptGuard/commit/47942a7c47f449516ccf7036f835c7c88922c7e5) |
| 7 | [Save run history atomically without truncating existing results](https://github.com/VSBhargav5/PromptGuard/commit/35912e210cc7b79c516943fc9a9963f95465b5ae) |
| 8 | [Skip malformed run history when listing saved results](https://github.com/VSBhargav5/PromptGuard/commit/3207ac8a5c1e898bcfa4a85c52419be46522692b) |
| 9 | [Reject comparisons between unrelated evaluation suites](https://github.com/VSBhargav5/PromptGuard/commit/c5e99d1809d6b061596443e7aa1048b1c41a95eb) |
| 10 | [Resolve baseline requirements before starting model work](https://github.com/VSBhargav5/PromptGuard/commit/813bba38033fad90f3c667eeda7ec0ca162a3432) |
| 11 | [Reject NaN and Infinity in JSON output validation](https://github.com/VSBhargav5/PromptGuard/commit/6cf366a8863b4d75e6af9e3e0548e9518428ff58) |
| 12 | [Preserve model-output characters safely in JUnit XML reports](https://github.com/VSBhargav5/PromptGuard/commit/d334e5765839f0bed496e049293ffa0c3ea9f2f3) |
| 13 | [Run offline reliability checks on both Windows and Linux](https://github.com/VSBhargav5/PromptGuard/commit/8399427e5bc0ee628d32e71a00d5cb695c0776ba) |
| 14 | [Document reliability contracts and an offline learning exercise](https://github.com/VSBhargav5/PromptGuard/commit/e9cbde073afe3eaaed5c4be070713a067dbeecf9) |

### Verification

- 110 offline tests passed locally on Python 3.11 with normal Windows permissions.
- [All four CI jobs passed](https://github.com/VSBhargav5/PromptGuard/actions/runs/39912866319):
  Python 3.11/3.12 on Linux and Windows.
- Both existing example suites validate without model calls.
- The published branch and merged main tree exactly match the tested local tree.
- The initial sandbox denied atomic file replacement. Tests were rerun with
  normal Windows permissions; the relevant assertions were retained.
- A JUnit round-trip test exposed whitespace loss in the former serializer path;
  the final implementation preserves normal Unicode, XML metacharacters, and
  attribute whitespace while visibly escaping illegal XML characters.

### First principles and limits

[The walkthrough](https://github.com/VSBhargav5/PromptGuard/blob/main/docs/reliability-boundaries.md)
starts with the difference between an absent filter and an explicit empty set.
A failed-case intersection that selects nothing must not trigger the whole suite.

These are tool-reliability checks. No live model calls, model-quality evaluation,
user adoption, revenue, or performance benchmarks are claimed. Transport timeout
behavior and complete case-definition equivalence remain outside this sprint.
Atomic replacement does not provide concurrent-writer conflict detection or a
power-loss durability guarantee. Manually assigned run IDs must use the documented
alphabet; generated UUIDs remain compatible.

## 23 October 2026 — PromptGuard evaluation coverage gate

**Status:** [Merged into main](https://github.com/VSBhargav5/PromptGuard/pull/1).
[Implementation commit](https://github.com/VSBhargav5/PromptGuard/commit/87498f57a565eeeed45df9895eaa13cf8c4c308f).

### Problem

A comparison could report "No pass/fail changes" while baseline cases disappeared
from the new run. Going from eight out of ten passing to eight out of eight
passing does not establish an improvement if two difficult cases were excluded.
These numbers illustrate the failure mode; they are not a measured model result.

### Change

- Show added and removed case IDs in comparison Markdown with observed status.
- Qualify unchanged outcomes to shared cases and identify disjoint runs.
- Add optional `--fail-on-removed` coverage enforcement to `compare` and
  `run --baseline`.
- Fail strict mode when a baseline cannot be found.
- Preserve ordinary subset comparison behavior.
- Fix an existing Python 3.11 CLI syntax incompatibility and cover 3.11/3.12 in CI.

### Verification

- 42 tests passed locally on Python 3.11.
- [GitHub Actions passed on Python 3.11 and 3.12](https://github.com/VSBhargav5/PromptGuard/actions/runs/39906822918).
- CLI regression tests cover removed passing/failing cases, disjoint sets,
  missing baselines, report output, and exit codes.
- Model execution is replaced in the relevant CLI tests; they run offline.
- Optional live evaluation was skipped. No live model-quality claim is made.

[Read the first-principles walkthrough](https://github.com/VSBhargav5/PromptGuard/blob/main/docs/coverage-gates.md).

### Limits and next work

Matching case IDs does not establish that inputs, assertions, or scoring rules
are unchanged. Preserve case-definition evidence before making stronger
comparability claims. User demand, pilot value, and monetization remain
unvalidated.

The LMS reliability sprint and BlastPath accuracy work are planned; they are not
claimed as completed changes in this entry.
