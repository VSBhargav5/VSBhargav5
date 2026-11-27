# Practical Data + AI engineering portfolio

Started: 23 October 2026.

Build reliable data systems and focused AI tools for recurring operational
problems. Each project should have a clear user, a reproducible failure mode,
meaningful verification, and an explanation of the engineering tradeoffs.

## Project focus

Latest 27 November: **RoleWeave is active**, superseding the earlier StudyFrame
focus below. [v0.51.1 PR #49](https://github.com/VSBhargav5/RoleWeave/pull/49)
ships reviewed reusable answers with recovery, embedded application frames,
section tailoring, batch rehearsal and saved-search continuation. Both six-job
CI runs passed; main matches tested tree ecf7bdc2c35682324a88570412b87c0e6ac63381.
Next work should follow observed user needs and manual acceptance. Real employer
forms, live model quality and account integrations remain evidence gates.
StudyFrame v0.13 is preserved and paused; do not repeat its shipped glass/OCR work.

Latest24November: [StudyFrame v0.13 clear glass and ready model distributions](https://github.com/VSBhargav5/StudyFrame/pull/18)
adds much stronger canvas transparency with saved0–90tint and explicit presets.
Interior shadow no longer hides zero transparency; controls retain local backing.
Both small speech models now ship through verified build-time asset setup instead
of manual folder setup.180 native Windows tests, native corner/exclusion fixtures
and nine local frozen checks passed. Personal accuracy/timing,401 and unsigned
installer manual acceptance remain evidence gates, not claimed complete.

Latest24November: [StudyFrame v0.12 reviewed local screen-text workflow](https://github.com/VSBhargav5/StudyFrame/pull/17)
adds keyless local capture/OCR, editable review and consented text-only asks with
no old image/audio/notes.173 native Windows tests passed, including actual CPU OCR
with networking forbidden. Verified local models, bounded disposable worker,
telemetry-disabled sessions and honest auth badges address observed gaps. Personal
OCR/speech accuracy, provider timing,401 diagnosis and manual installer acceptance
remain open; no overall completion percentage or production acceptance claim.
[Core paths and acceptance](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/mvp.md).

Latest 19 November: [StudyFrame v0.11 session/capture/speech changes](https://github.com/VSBhargav5/StudyFrame/pull/16)
follows reports of lost session key, slower vision and poor accent recognition.
165 offline Windows tests pass. Provider-isolated in-memory keys and reset clarity
are defensive; exact key loss is not reproduced. Balanced captures reduce pixels
with original restoration, without claiming measured vision speed. An installed
Indian-English model offers an offline comparison; personal accuracy is unverified.

Latest 19 November: [StudyFrame v0.10 streaming/glass workflow](https://github.com/VSBhargav5/StudyFrame/pull/15)
follows user-confirmed correct synthetic text/screen answers and a separate timeout.
Quick mode and explicit length precedence address unwanted long lessons. Streamed
text, partial/completed distinction and session-only first-text/total timings
remove wait-for-whole-answer display behavior without promising upstream speed.
Capture/Voice share the header, glass tint is lighter with tested contrast, and
key-ready clears stale feedback without authenticating. 160 offline native Windows
tests passed. Live streaming acceptance remains unverified; no agent inference call.

Latest 19 November: [StudyFrame v0.9.2 free-usage diagnostics](https://github.com/VSBhargav5/StudyFrame/pull/14)
is merged with all five PR checks passed; it
follows the [v0.9.1 visibility fix](https://github.com/VSBhargav5/StudyFrame/pull/13).
The user-run trial now shows HTTP429; no answer is verified yet. Explicit metadata-only
usage counters, safe status/retry guidance and eligible free-provider failover help
investigate limits while retaining zero-price/privacy constraints and no client retries.
152 offline Windows tests and eight frozen runtime checks passed. The user confirmed49of50 daily requests remaining through the new metadata UI;
model success is still unverified. The agent has not accessed the key.
[Diagnostics and acceptance](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/windows-release.md#http429-and-free-usage).

Earlier 19 November: [StudyFrame v0.9 Windows MVP](https://github.com/VSBhargav5/StudyFrame/pull/12)
is merged. Visible model setup, prepared/reusable audio recognizer, exact named
microphone/playback selection, on-screen window fit and unsigned per-user installer.
142 native Windows offline tests and all five PR checks passed, including installed
runtime, active-session guard, reinstall and config-preserving uninstall in CI.
User's missing-opening-words report drove the Prepare → Ready → Listen → Listening
now flow; physical retest and actual microphone accuracy remain pending. OpenRouter
free trial is explicitly deferred until the user obtains and enters their own key.
No personal audio/model call. Local model and portable available; CI installer omits
weights. Signing, interrupted-upgrade recovery and personal acceptance remain gates.
[Defined scope and acceptance](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/mvp.md).

Earlier 18 November: [StudyFrame v0.8.1 PR #11](https://github.com/VSBhargav5/StudyFrame/pull/11)
corrects low-contrast glass found in the user’s light-desktop photos. Stronger dark
material, reduced glow and brighter/larger secondary text preserve native frost.
131 offline Windows tests and all five PR checks, including portable runtime, passed; actual
native light/dark previews retain 36/36 corner pixels and hidden-baseline exclusion.
The rebuilt standalone runtime and 341 manifest hashes verified. This addresses
an observed issue, not a new speculative feature. Personal acceptance/live AI/mic
quality and signed distribution remain gates. [Reproduce it](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/native-capsule.md).

Earlier 18 November release: [StudyFrame v0.8 PR #10](https://github.com/VSBhargav5/StudyFrame/pull/10)
is merged. True compositor-clipped Windows 11 frost replaces the square Acrylic
halo. Physical bounds/input shape, pinning, capture/minimize/close lifecycle and
both-layer exclusion read-back are covered; unsupported hosts retain Qt fallback.
130 offline native Windows tests and five PR checks passed. The frozen runtime
loads the compositor; 341 manifest hashes and ZIP integrity verified. Guarded
synthetic exclusion matches the hidden-overlay baseline, with 36/36 corners
unchanged. [Contracts and focused practice](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/native-capsule.md).
No background screenshot loop or personal transmission. Native system policy can
change appearance; microphone/live AI quality, other devices/recorders, personal
acceptance and signed installation remain gates. Use the complete unsigned
portable folder; enter a key only in the app for an explicit synthetic trial.
Only StudyFrame is active. No overall long-term feature-completion claim.

Earlier 18 November release: [StudyFrame v0.7.1 PR #9](https://github.com/VSBhargav5/StudyFrame/pull/9)
is merged. Standalone Windows EXE/ZIP, non-secret setup persistence, input signal
meter, silent-source guidance and correct frozen worker pipes. An authorized
public-sample default-playback trial found a native-DLL startup deadlock; the
nonblocking-pipe fix passed its hardware retest after unmuting. No captured audio
was saved or uploaded. Local package includes the trusted small English model;
CI leaves weight selection explicit.124 native Windows offline tests and all five
PR checks passed, including portable build/runtime. [Build artifacts](https://github.com/VSBhargav5/StudyFrame/actions/runs/44254832063).
[First use and remaining acceptance](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/windows-release.md).
Unsigned portable software; microphone quality, other devices, live AI and personal
acceptance remained gates; v0.8 above subsequently addresses native frost. StudyFrame
is the only active implementation, not a claim that every long-term feature is done.

Earlier 18 November follow-up: [StudyFrame v0.6 PR #8](https://github.com/VSBhargav5/StudyFrame/pull/8)
is merged. Explicit local microphone/default-playback speech, 30-second clips,
Stop/Discard, editable transcript and a separate text-only model send; no audio or
old screenshot/notes accompany it. Optional local Vosk/SoundCard model setup, not
a cloud transcription key. The rectangular Acrylic backdrop was removed after
pixel checks disproved correct clipping; 36/36 outer-corner pixels now stay equal
to the sharp background. Fully frosted native blur remains unresolved. Windows
capture exclusion remains independently checked and on by default.
115 offline native Windows tests/all four PR checks passed; local public-sample
recognition ran with later-digit errors disclosed. Physical devices, live AI
quality and personal usefulness remain unverified. [Setup and tradeoff](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/speech.md).

Earlier 18 November: [StudyFrame v0.5 native glass capsule PR #7](https://github.com/VSBhargav5/StudyFrame/pull/7)
is merged. Small 360 × 90 logical-pixel startup capsule, expandable answers,
rounded native shape and guarded Acrylic compatibility effect. Windows capture
exclusion is on by default with explicit read-back status and lifecycle reapply.
Actual blur and visible/excluded/restored synthetic capture were checked on build
26300; 106 offline native Windows tests and all four PR checks passed. Installed
v0.5 verified outside checkout. [Reproduction and tradeoff](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/native-capsule.md).
Acrylic uses an undocumented compatibility export with fallback; this capture
check does not establish support for every recorder. Live model quality, unusual
scaling and personal usefulness remain unverified. Only StudyFrame is active.

Earlier 17 November: [StudyFrame v0.4 glass companion PR #6](https://github.com/VSBhargav5/StudyFrame/pull/6)
is merged. Compact translucent/gradient overlay, question and answer together,
draggable/resizable frame, connection/preview drawers and reversible small bar.
Capture & ask explicitly sends one freshly captured screen to the shown provider;
preview/crop/approve/send stays optional and separate. Failed or cancelled captures
never send stale images. No recording/process concealment or native-blur claim.
98offline tests/all four PR checks passed, synthetic answer/settings/bar inspected,
narrow overflow and key-field scroll corrected. Installed0.4 refreshed and verified.
[Guide and practice](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/glass-overlay.md).

StudyFrame remains the one active implementation; RoleWeave is paused as a local
MVP. Next is an authorized real-screen/synthetic live answer trial and observed
fixes; physical capture/compositor/scaling, live routing/quality and personal
usefulness remain unverified. No personal image/live/paid call/key access exercised.
Click-triggered stills are not completed continuous watching. No churn for counts.

Earlier explicit focus switch17November: **StudyFrame is active; RoleWeave is paused
as a local MVP.** CueDesk remains a reference; one original Python assistant is
being developed. [v0.3 PR #5](https://github.com/VSBhargav5/StudyFrame/pull/5) merged:
selected-display still capture, physical-pixel crop/review, timestamp, pinning,
Explain default and a fixed reviewed free OpenRouter route. No paid fallback or
automatic upload.85offline tests/all four PR checks passed; installed local0.3
verified outside checkout. No personal capture, live model call or key/account
access. [Workflow](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/screen-assistant.md).

Next evidence gate: a permitted synthetic real-screen/API trial, then bounded
started/stopped watching and additional direct/local adapters. Still capture is
not continuous video. Free quotas and privacy policies constrain cloud usage;
[official provider/key research](https://github.com/VSBhargav5/StudyFrame/blob/main/docs/free-vision-options.md)
is documented. Live quality, physical capture behavior, installer and user learning
remain unverified. Do not resume RoleWeave merely to add features/counts.

Earlier RoleWeave release evidence17November: [v0.37 document languages PR #48](https://github.com/VSBhargav5/RoleWeave/pull/48)
is merged after all six PR checks passed. It adds fixed labels, structured dates,
letter scaffold and metadata across seven
languages/nine choices. Human-authored content stays exact, preview consent binds
locale, saved selections show it, and frozen exports/recovery retain original bytes.
512offline tests:421passed/91archived-native skips, five Node checks and final
source/actual Windows package/frozen journeys passed. Synthetic German/French
PDF layouts inspected. No full21-language/content/app translation, language-quality
acceptance or personal acceptance claim. [Guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/document-localization.md).
Current checklist: **17implemented/4partial/4missing**. Localization is partial;
Gmail, inbox/AI replies, MCP and remote hosting/auth are still missing. Choose a
useful next workflow without assuming account access or personal transmission.

Earlier on 17 November: [v0.36 startup notices PR #46](https://github.com/VSBhargav5/RoleWeave/pull/46)
is merged. Keyless explicit HN jobs observations feed local filtering, checked
employer/market imports, exact source receipts and managed recovery. One public
sample accepted ten notices from a 31-entry index; no profile/query transmission
or employer-page fetch. This is HN-listed startup notices, not the full YC directory,
Who is hiring threads or verified eligibility. 503 offline tests: 412 passed /
91 archived-native skips; final source/Windows portable/frozen journeys and all six
PR checks passed. [Guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/startup-discovery.md).
[Merged v0.36.1 correction PR #47](https://github.com/VSBhargav5/RoleWeave/pull/47) fixes a
reproduced older-page response resurrecting a closed source. A controlled held-read
regression and ten actual Windows package close/replay cycles pass. All six patch PR
and six post-merge checks passed. The original
feature post-merge Windows browser job failed; its exact pointer-failure cause is
not independently established. No retry was used to hide that result.
Current scoped checklist: **17 implemented / 3 partial / 5 missing**. Missing:
connected Gmail, inbox/AI responses, MCP, remote hosting/authentication and document
localization. Existing permission/account/live-quality gates remain; no overall
personal or production acceptance claim.

Earlier on 17 November: [v0.35 automatic recovery PR #45](https://github.com/VSBhargav5/RoleWeave/pull/45)
is merged. Opt-in local-host nightly snapshots/catch-up, verified seven-file
retention, exact ZIP download and separate restore protect the managed application
workspace. Off by default; restored policies require renewed consent. Same-device,
unencrypted, no OS task/cloud backup or operation while the host is closed.
489 offline tests: 398 passed / 91 archived-native skips; source/actual Windows
portable/frozen journeys and all six PR checks passed. Overnight/sleep/power-loss
and personal acceptance remain unverified. [Guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/automatic-backups.md).
At v0.35: **16 implemented / 3 partial / 6 missing**; the startup milestone above supersedes that missing count. Remaining
priorities include scored/scheduled discovery and browser/broader Calendar; external
accounts, provider compatibility and live quality retain separate consent/evidence
gates. One previously missing area is now implemented, not overall production readiness.

Earlier on 17 November: [v0.34 PR #44](https://github.com/VSBhargav5/RoleWeave/pull/44)
adds optional experimental JSearch discovery: explicit public-query review,
one-request credentials/consent, cursor pages, original-byte evidence and managed
recovery. Final source/Windows portable flows pass, including a real stale-board
refresh correction with a forced delayed-response regression. 473 local tests:
382 passed / 91 retired-native skips. All six PR checks passed; one Windows package
check needed a targeted retry after an isolated localhost connection failure.
Live response compatibility and usefulness remain unverified; FreeHire stays the
default and named saved searches still use FreeHire. [Workflow and limits](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/jsearch-discovery.md).

Earlier on 17 November: [reviewed assessment v0.33 PR #43](https://github.com/VSBhargav5/RoleWeave/pull/43)
is merged after completing the preserved candidate's final source/Windows portable/
frozen checks. The workflow links selected facts to exact requirement quotes, human
corrections and uncalibrated advisory opinions. Comparable-source/model ranking,
separate market filters, per-job history and exact-request recovery are implemented.
No eligibility/hiring-probability or production/personal acceptance claim.

[Structured career sections v0.31 PR #41](https://github.com/VSBhargav5/RoleWeave/pull/41)
and [retained conversations v0.32 PR #42](https://github.com/VSBhargav5/RoleWeave/pull/42)
shipped on 16 November. Typed evidence survives review/documents/recovery. Opt-in local
conversation turns retain original requests/proposals and reopen without another
model call. A real CI tracking race was fixed with frozen dialog revisions and a
deterministic browser regression. All six release PR checks passed for each release.
Current source/final portable flows use synthetic data; no native GUI tests run on
the user's laptop. Last full local suite: 461 tests, 370 passed / 91 native skips, with 24 final
assessment/provider and 5 Node checks plus actual browser/frozen verification.

[Current capability checklist](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/dossier-parity.md):
At v0.34: 15 implemented / 3 partial / 7 missing. Three of six requested partial areas closed. The v0.35 recovery milestone above supersedes that missing count. Next:
permitted JSearch compatibility validation, additional aggregate sources, scheduled/scored discovery and browser/
broader Calendar, followed by the seven still-missing areas. Actual account setup,
permitted live trials, personal acceptance and observed quality remain separate gates.
Use public/synthetic data; no paid calls, secrets from files/env, personal/employer
transmission, accounts, deployment or applications without required authorization.
[Assessment practice](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/job-assessment.md)
compares quoted-row coverage with advisory opinion; practice is not presumed complete.

Earlier milestones below are historical; completed work supersedes their next-step notes.

Latest v0.28 [theme builder PR #38](https://github.com/VSBhargav5/RoleWeave/pull/38)
is merged: bounded document styling and portable JSON sharing preserve exact old
preset rendering and new frozen source provenance.321local tests passed/91native
skips; actual final package browser/runtime and all six PR checks passed. Six
rendered synthetic PDF pages inspected; personal/ATS acceptance unverified.
The12implemented/6partial/7missing matrix is capability scope, not a readiness
percentage. Remaining rich profile, browser employer boards, assessment, refinement
chat/undo, Calendar and scheduled-agent work is pending. User requested a break;
resume deliberately from verified main, with no new feature work during the break.

Latest November16: [provider PR #36](https://github.com/VSBhargav5/RoleWeave/pull/36)
and [insights PR #37](https://github.com/VSBhargav5/RoleWeave/pull/37) are merged.
Non-secret provider/model selection (OpenAI/Anthropic/Mistral and numeric-loopback
Ollama/LMStudio) preserves exact reviewed destinations and per-send consent. A new
read-only Insights page shows current/ever-recorded stages,12UTC weeks and a
market-filtered follow-up calendar, with review-level rather than outcome claims.
313passing local tests/91native skips; actual source/portable journeys/runtime and
all six PR/post-merge checks passed. Live model compatibility/quality/accounts and
personal acceptance remain unverified. Broad partial-completion remains active;
custom theme builder next, followed by remaining current matrix areas. No deployment,
account linking, automatic application, model start/download or paid call performed.

Latest November 16 milestone: [v0.25 PR #35](https://github.com/VSBhargav5/RoleWeave/pull/35)
ships saved manual discovery queries, explicit first-page runs, a persisted review
queue, exact source recovery and Markdown import. Three active named searches,
local rolling attempt budget, stale guards, interrupt/late-result ownership and
whole-run capacity rollback preserve decisions. Changed location/work-mode/content
requires new review. Explicit application imports are idempotent, never submissions.
[Saved discovery guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/saved-discovery.md).

381local tests discovered:290passed/91native archive skips. Actual source and
packaged synthetic browser journeys and all six PR checks passed; live saved-run
compatibility/coverage and personal acceptance remain unverified. Scoped parity
9implemented/9partial/7missing: Markdown closes the import-format gap; named manual
queue makes the agent area partial, not full scheduled/scored agent parity.
The user's request to finish partials remains active: provider/model settings next,
then other documented partials. FreeHire current terms restrict unpaid reads to
personal/noncommercial use; public offering requires its plan. No paid plan/live
provider request, source scraping, account linking or application sending performed.

Latest November 16 comparison/email: [v0.24 PR #34](https://github.com/VSBhargav5/RoleWeave/pull/34)
adds a local sender/recipient/message composer with exact matching frozen PDFs,
renewed preview/confirmation, immutable save/reopen, EML download and managed
recovery. It sends nothing and does not alter application history. Actual source
and packaged synthetic browser journeys,271 local passing tests/91 native skips,
and all six PR release checks passed. Physical mail-client/clipboard acceptance,
real accounts and personal usefulness remain unverified.

[Pinned 25-area Dossier checklist](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/dossier-parity.md):
8 implemented,9 partial,8 missing after v0.24; baseline v0.23 was7/9/9. These
are stated local capability areas, not effort percentages or production acceptance.
Next: saved discovery searches with deliberate run/review queue, then broader
AI providers. Gmail/inbox, startup discovery, nightly backups, MCP, remote hosting/
password access and localized document labels/dates remain missing. Rich profile,
themes, discovery/scoring/chat/Calendar/analytics remain partial. The README's
claims were rechecked against Dossier c79562e; no upstream app benchmark or code copy.
[Email guide and limits](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/application-email.md).

Latest November 16 migration: [v0.23 PR #33](https://github.com/VSBhargav5/RoleWeave/pull/33)
adds private interview rehearsal inside the single browser interface: selected
source questions, linked evidence reveal, bounded answers/reflections, confirmed
immutable versions, reopen and original JSON download. Managed recovery verifies
both journal integrity and full saved-review identity. 263 local tests passed,
91 archived native skips; all six PR CI jobs and actual packaged synthetic browser
checks passed. No generated answers, timer, grading or learning-completion claim.
[Rehearsal workflow and limits](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/browser-rehearsal.md).
Older journal import/comparison/text packs and other native-only screens remain
pending browser migration, alongside broader Dossier parity and personal acceptance.


Latest November 14 interface repair: [v0.22 PR #32](https://github.com/VSBhargav5/RoleWeave/pull/32)
retires the native-tools fallback, redirects historical --legacy launches to the
browser and fixes the repository launcher to choose the current versioned build.
Default local tests no longer open archived native windows; CI explicitly retains
that regression coverage. 255 local tests passed, 91 archived native skips;
all six PR CI jobs and actual packaged synthetic browser checks passed. Stored
data is preserved. Native-only board management, Calendar setup, audit and
rehearsal need browser migration before being offered again.
[One interface and workspace paths](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/single-interface.md).

Latest November 14 AI/UI iteration: [v0.21 PR #31](https://github.com/VSBhargav5/RoleWeave/pull/31)
adds reviewed browser proposals and explicit revisions, persistent per-job drafts,
master-profile preservation and matching PDF/letter handoff. The previous missing
browser-tailoring item is now implemented and offline tested. Compact onboarding,
aligned spacing and one-click offline practice address UI/entrypoint friction.
342 Windows tests and actual packaged synthetic checks pass. Source references
are not factual verification; real model quality/account access is unverified.
[Current workflow / limits](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/ai-tailoring.md).
Multiple providers/full chat, scheduled discovery, Gmail/general sync, universal
employer controls and production acceptance remain future scope. No live calls,
personal data transmission or automatic applications are claimed.

Latest November 14 studio: [v0.20 PR #30](https://github.com/VSBhargav5/RoleWeave/pull/30)
adds visual resume preparation, three themes, ordered facts and frozen PDF letters
in recipient kits. The actual Windows package and 331 offline tests exercise the
workflow. Deep Windows recovery paths are supported. Next implementation priority
is source-bound browser AI tailoring/refinement with deliberate payload/provider
consent; existing native quote proposals are not equivalent. Scheduled discovery,
Gmail/general sync, broader form controls and real acceptance remain separate gaps.
[Current scope and guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/application-studio.md).

Latest November 14: [v0.19 PR #29](https://github.com/VSBhargav5/RoleWeave/pull/29)
adds reviewed existing-resume import and complete managed-web-workspace recovery,
with a guided first application path. The actual Windows package, rather than
only source/mocks, is exercised through import, profile save, documents, contact
filling, manual tracking and separate recovery. Current scope and limits:
[first-use guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/using-roleweave.md).
The import/recovery items described as possible work in older entries below
are now implemented. Real helper/employer acceptance, signing and optional live
account/model checks remain separate; no production or hiring outcome is claimed.

Latest November13 startup correction: [v0.18.2 PR #28](https://github.com/VSBhargav5/RoleWeave/pull/28)
removes the need to find a hidden old server before opening the app. Current
matching hosts are reused; older/unrelated processes are preserved and occupied
ports recover automatically.311 offline tests and real packaged normal/repeat
startup plus public search are verified. User acceptance and actual employer/helper
compatibility remain open; do not infer them from these checks.

Latest November13 correction: [v0.18.1 PR #27](https://github.com/VSBhargav5/RoleWeave/pull/27)
fixes a real packaged first-search failure that source/mocked checks missed.
A missing runtime SSL policy asset is now retained without bypassing TLS checks.
306 offline tests, frozen TLS initialization and the actual packaged browser
search path are verified;20public London results observed from an isolated empty
workspace. Prior v0.17/v0.18 local builds should be replaced with the corrected
complete package. Remaining personal/helper/ATS gates stay open.

Latest November13 continuation: [v0.18 PR #26](https://github.com/VSBhargav5/RoleWeave/pull/26)
closes repeat-use gaps: saved letters reopen and join matching recipient PDFs;
explicit search pages preserve scope/market; application filters and stale-safe
reminders keep the next action visible.304 Windows tests and the expanded
synthetic browser journey pass. Next useful gates remain a permitted real first
application/helper acceptance trial and observed fixes. Existing-resume import,
richer supported form controls and complete web-artifact recovery are possible
next workflow work, not shipped claims.

Latest November13 workflow: [v0.17 PR #25](https://github.com/VSBhargav5/RoleWeave/pull/25)
replaces the default presentation with a browser-rendered CSS/SVG workspace while
preserving Python/SQLite and native advanced tools. Search by role/location no
longer needs a board URL. The original Chrome/Edge helper reviews and fills
supported empty contact inputs; uploads, screening answers and final submission
remain manual.298 offline Windows tests, a synthetic Chromium application
journey, seven native input fills and source/frozen runtime checks pass. Next:
permitted helper installation and a real first-application acceptance trial,
followed by observed compatibility fixes. No universal ATS/production claim.

Latest November12 handoff update: [v0.16 PR #24](https://github.com/VSBhargav5/RoleWeave/pull/24)
adds direct upload folders with checkbox document selection and structured
submission date/channel/reference/follow-up without a dossier. Later stages and
newer tracking are protected.291 native Windows tests and source/frozen smoke
pass; the complete synthetic journey uses actual files without ZIP extraction.
Next is permitted personal application use and observed friction fixes. Employer
submission remains manual; Google/AI are optional previews outside local v1.

Latest November12 user-goal update: [v0.15 Apply workspace PR #23](https://github.com/VSBhargav5/RoleWeave/pull/23)
connects the entire manual application journey: save job, review profile/evidence,
prepare PDF/letter, export recipient files, open employer page and record the
submission/follow-up. A fresh synthetic UI journey verifies these steps and
backup restore without requiring a private dossier.276 Windows tests pass;
actual employer submission remains the user's manual action. Next is a permitted
personal first-application trial and observed friction fixes. Google/AI remain
optional previews outside local v1; no real submission or outcome is claimed.

Latest November12 update: [v0.14 release-safety PR #22](https://github.com/VSBhargav5/RoleWeave/pull/22)
adds atomic known-legacy schema adoption, incompatible-file refusal, private UI
error reporting, startup failure exit codes and download checksums.272 offline
Windows tests and source/frozen checks pass. The current deliverable is a
controlled beta. The owner chose local Windows v1 first: clean-Windows human
acceptance, signing/distribution and interrupted-upgrade validation remain
tracked. Google/AI are optional previews, outside local-v1 acceptance.
See the [release acceptance guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/release-acceptance.md).

Latest November11 update: [v0.13 dark workspace PR #21](https://github.com/VSBhargav5/RoleWeave/pull/21)
adds near-black surfaces, violet/cyan accents, gradient weave artwork, rounded
native controls and exact evidence cards.261 offline Windows tests, eight final
design tests and source/frozen synthetic checks pass. Main synthetic visuals
were inspected; unusual scaling/full manual acceptance remain open.
The [v0.11 Google follow-up integration](https://github.com/VSBhargav5/RoleWeave/pull/19)
remains implemented/offline tested, with no live account/write trial yet. Next:
user-owned Desktop OAuth setup and a synthetic consent/create/update/conflict
trial, then permitted personal use and observed fixes. AI quality/manual acceptance
remain open; mailbox/general two-way sync stays deferred. No outcomes claimed.

Historical November10 stopping point (completed by v0.9): [v0.8.1 watchlist foundation](https://github.com/VSBhargav5/RoleWeave/pull/14)
adds portable board/filter choices, a guarded Windows editor and explicit bounded
multi-board source CLI.204 offline tests pass. Resume next with multi-board
Windows collection preview/import and collection archives/comparison were the
next steps and are now shipped. Live/user acceptance gates remain.

Latest November10 delivery update: [v0.8 PR #13](https://github.com/VSBhargav5/RoleWeave/pull/13)
ships reviewed letters, exact private dossiers/recipient-only exports, manual
submission and local email excerpts, plus stale-history protection.194 offline
tests and source/portable/installed CI pass. Saved employer-board reuse is next;
live accounts/AI and user acceptance remain gated.

Latest November10 discovery update: [v0.7 PR #12](https://github.com/VSBhargav5/RoleWeave/pull/12)
adds Lever global/EU and Ashby alongside Greenhouse, local filters, board-URL
resolution and private byte-verified observation replay/comparison. 156 offline
Windows tests and source smoke pass. Live new-provider compatibility and manual
acceptance remain unverified; no complete-board or eligibility inference.

Latest November 10 update: [Windows setup PR #11](https://github.com/VSBhargav5/RoleWeave/pull/11)
adds per-user installation, Start-menu access and uninstall with data retained.
139 offline Windows tests pass. Signing, manual wizard acceptance, interrupted
upgrades, live AI and calendar-client use remain evidence gates.

Latest November 4 update: RoleWeave remains active; CueDesk, StudyFrame and
SettleTrace are paused. [v0.6 readiness sprint](https://github.com/VSBhargav5/RoleWeave/pull/10)
adds profile transfer with fresh human review, exact-job resume browsing and TXT,
filtered CSV/calendar export, backup inspection, read-only storage checks,
related-review comparison and evidence rehearsal. Safer exports publish complete
files without overwrite; staged Windows builds preserve the previous package.
137 offline native Windows tests and source/frozen self-tests passed. Manual
acceptance, authorized live AI and calendar-client import remain evidence gates.
No hiring outcomes, time savings or personal usefulness are claimed.

| Project | Operational problem | Evidence to build | Status |
| --- | --- | --- | --- |
| [CueDesk](https://github.com/VSBhargav5/CueDesk) | Screen-assisted study and coding on Windows | Reviewed capture, explicit AI request, personally verified usefulness | Paused; real screen and provider trial remain |
| [StudyFrame](https://github.com/VSBhargav5/StudyFrame) | Asking for study/coding help on Windows repeatedly requires assembling context | Bounded screenshot crop/restore, deliberate provider send/cancel, reviewed follow-ups, personally verified usefulness | Active; [v0.7.1 portable](https://github.com/VSBhargav5/StudyFrame/pull/9); 124 offline tests, frozen runtime and default-playback sample verified; microphone/live AI and frosted blur remain open |
| [RoleWeave](https://github.com/VSBhargav5/RoleWeave) | Relating job requirements to defensible career evidence and application decisions | Reviewed claims, exact posting quotes, separate job markets, personally usable workflow | Paused as a local MVP; browser discovery/application preparation and recovery remain shipped; live AI/personal acceptance next |
| [SettleTrace](https://github.com/VSBhargav5/SettleTrace) | A custom merchant ledger, processor activity, and bank deposits can disagree | Exact-money contracts, source-row evidence, verified export mapping, operator feedback | Paused; [v0.3 mapping and observation evidence merged](https://github.com/VSBhargav5/SettleTrace/pull/3) |
| [PromptGuard](https://github.com/VSBhargav5/PromptGuard) | AI prompt changes can silently break previously working cases | Coverage-aware comparisons, labeled failure examples, repeatable evaluation, external pilot feedback | Reliability sprint completed; [merged work](https://github.com/VSBhargav5/PromptGuard/pull/2) |
| [LMS ETL](https://github.com/VSBhargav5/LMS-ETL-PIPELINE) | Missing, duplicate, or late events can undermine learner scores and reports | Known expected results, idempotent reruns, controlled crash recovery, measured workloads | Next engineering sprint; review the existing architecture audit first |
| [BlastPath](https://github.com/VSBhargav5/BlastPath) | Reviewers need a traceable explanation of downstream Python change impact | Representative fixtures, measured misses and false positives, honest dynamic-import limitations | Later candidate |

Keep one implementation sprint active. Existing DecisionLog, OpenLoop, and Nifty
projects remain available while these priorities are evaluated.

StudyFrame remains an independent Python project. CueDesk is the separate,
GPL-attributed Cue adaptation preserved as a reference. StudyFrame Capture & ask
explicitly authorizes one fresh still send; optional preview/crop remains local
until separately approved. Continuous watching and meeting audio are not built. No live model
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
