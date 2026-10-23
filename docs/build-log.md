# Build log

Entries distinguish shipped code, verification, limitations, and planned work.

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
