# Build log

Entries distinguish shipped code, verification, limitations, and planned work.

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
