# Build log

Entries distinguish shipped code, verification, limitations, and planned work.

## 14 November 2026 — visual application studio and PDF cover letters

[Studio PR #30](https://github.com/VSBhargav5/RoleWeave/pull/30),
[frozen document contracts](https://github.com/VSBhargav5/RoleWeave/commit/44c1d4a63f38ca3766194654c3855080cd188f91),
[Windows recovery paths](https://github.com/VSBhargav5/RoleWeave/commit/b3c7cfa65cdcd57d323502dcb1c4dadbbca19585),
[browser studio](https://github.com/VSBhargav5/RoleWeave/commit/70942b4558193b77288be5c9717229e042289847),
[release evidence](https://github.com/VSBhargav5/RoleWeave/commit/372574697e2ae1a8fffce16a6d9317b6a9361d1b).

The two-pane browser studio selects a resume theme and orders reviewed facts
within fixed sections. Its HTML layout preview is read-only; exact preview PDF
bytes can be downloaded before freezing. Changing layout/order/label invalidates
review, and the server checks the preview fingerprint before saving. New letters
freeze PDF bytes and join the matching resume in a recipient-only two-PDF kit.
TXT remains available; old document/dossier/backup versions remain compatible.
Windows recovery now handles deep paths without changing system settings.

PR #30 is merged; all six PR checks passed, covering Windows/Linux 3.11/3.12,
source and actual packaged browser workflows, installed runtime and installer lifecycle.
331 offline native Windows tests, actual packaged browser workflow and frozen
TLS/parser/recovery/studio checks passed. Three resume PDFs and a cover letter
were rendered and visually inspected; prior executable-created documents replay.
Visual QA caught an unstyled preview under the restrictive content policy; a
scoped local stylesheet corrected it without relaxing that policy. Browser QA
also found the deep-path issue and verifies fact ordering and stale preview.

[Current guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/application-studio.md)
and [gap review](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/research-and-plan.md)
separate this work from Dossier parity. Browser AI drafting/chat, scheduled
search agent, Gmail/broad sync and universal employer controls remain missing;
manual uploads/screening/final submission and real acceptance remain explicit.
No live model call, personal transmission or application was performed. Unsigned
controlled beta; no hiring, usefulness or production reliability claim.

## 14 November 2026 — start from an existing resume and recover the workspace

[Workflow PR #29](https://github.com/VSBhargav5/RoleWeave/pull/29),
[local parser](https://github.com/VSBhargav5/RoleWeave/commit/14a479639d6f01dd40d336b6756064d624c754ab),
[reviewed import and recovery](https://github.com/VSBhargav5/RoleWeave/commit/19f0318d6b7675c159c26e7806e83b47155f5602),
[packaged workflow](https://github.com/VSBhargav5/RoleWeave/commit/b0a2e69265c4934f8dbeb10d0cb5e054a551dc5d),
[dependency consistency](https://github.com/VSBhargav5/RoleWeave/commit/3d4de8e9dbbf0b58a133420fb80c3f2592d2cd44).

Career profile imports selectable-text PDF, DOCX or UTF-8 TXT locally in a
bounded child process. Users review actual excerpts, select sections, confirm
and explicitly save their profile draft. Original bytes and fingerprints remain
local; no identity, qualification or employment claim is inferred. No OCR or
layout reproduction is promised.

Recovery ZIPs include the shelf and all managed web letters, recipient files,
original imports and retained provider responses. Preview validates paths, sizes,
hashes and the database before confirmed, staged recovery into a new workspace.
The active one is preserved. Completed copies reopen from Settings. Bundles are
unencrypted and bounded at 64 MiB/1,000 managed files; external exports, other
workspaces, credentials and unsaved drafts are excluded. Windows paths at the
legacy length boundary are refused before persistent output.

All 325 offline Windows tests and all six PR CI checks passed, including the
Windows/Linux matrix, packaged browser journey, installed runtime and installer
lifecycle data preservation. PR #29 is merged with its exact tested tree.
The actual v0.19 Windows executable passes the frozen PDF-worker/recovery/TLS
self-test and complete synthetic Chromium application journey. Final packaged
QA caught the deep-path failure; CI initially caught a duplicate PDF dependency
pin. Both were corrected before merge. Synthetic checks do not establish real
helper installation, arbitrary employer controls, personal acceptance, signing
or optional live AI/Google compatibility. Submission, uploads and screening
answers stay with the user. No personal transmission or application was made.
[First-use guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/using-roleweave.md).

## 13 November 2026 — recover from hidden background servers

[Startup recovery PR #28](https://github.com/VSBhargav5/RoleWeave/pull/28),
[implementation](https://github.com/VSBhargav5/RoleWeave/commit/54faa8678ae69450f4b2d4232aa4adada8e9acbc).

The user could not find the old app to close: its browser tab was gone but its
v0.17 server still owned8765, blocking the corrected executable. Read-only health
inspection confirmed this. Immediate recovery opened corrected0.18.1 on a free
port without closing another process or resetting the workspace.

v0.18.2 normal launch checks a bounded loopback range for the exact current
version/workspace, reopens a match or binds a free port. Different versions,
workspaces and unrelated servers stay untouched. Occupancy/bind races fall back
safely; Windows can time out before reporting refused loopback connections, so
binding supplies the authoritative occupancy check. Non-port failures still fail
explicitly. No process termination or CLI flag is needed for ordinary launch.

311 offline Windows tests and the full synthetic Chromium workflow pass. The
actual packaged preferred-port startup was tested while the hidden v0.17 server
remained: a second launch reused the matching host, and the packaged browser
London search returnedHTTP200/20accepted/0excluded using an empty isolated DB.
The complete ZIP and versioned app copy are ready; the old locked folder stays
preserved. The previous TLS asset fix and privacy/consent boundaries remain.
Personal acceptance, real installed-helper/employer compatibility, signing and
optional live integrations remain separate unverified gates. No personal data
was transmitted externally and no application was submitted.
All6PR CI43422969675 checks passed, including browser, Windows/Linux3.11/3.12,
portable/installed runtime and installer lifecycle checks.

## 13 November 2026 — fix the actual packaged first search

[Search fix PR #27](https://github.com/VSBhargav5/RoleWeave/pull/27),
[implementation](https://github.com/VSBhargav5/RoleWeave/commit/b2ec8d36f98607174a8fb3d040f8922b1723d165).

The user reported failure on their initial search. Reproduced v0.18 packaged
HTTP400 while source returned20results. The build Python's SSLContext expected a
runtime policy sidecar omitted from the local Windows package, raising before
any HTTPS request. Earlier source live checks and mocked browser tests had not
verified this real packaged path. Those checks did not establish live packaged
search functionality.

v0.18.1 retains the runtime SSL policy asset beside frozen ssl.py without weakening
certificate/hostname verification or changing global trust settings. HTTPS setup
errors are actionable and sanitized; loading/errors remain visible inline. The
frozen offline web smoke now initializes a verified TLS context. Optional public
CLI and browser checks exercise the actual installed executable, not source.

306 offline Windows tests and synthetic browser regressions pass. The corrected
packaged CLI, local HTTP route and actual browser form returned HTTP200 with20
accepted/0excluded public results for data engineer/london; screenshot inspected
using an empty isolated database. Frozen smoke reports verified_https_context=true.
No personal saved jobs, credentials, paid calls, account links or applications
used. Corrected ZIP/versioned app copy are ready; the open old folder was preserved.
The old host must be quit before opening v0.18.1. Real employer submission and
installed-helper acceptance remain unverified.
All6PR CI43419724546 jobs passed, including frozen TLS initialization, browser,
Windows/Linux3.11/3.12 and portable/installer lifecycle checks. PR #27 merged at
8235901663703c4f7b4689dde7ea182ca3246e41, tested tree
7d89ee4ecfc9170e170795878fa8cea20a3f444b matched exactly.

## 13 November 2026 — RoleWeave v0.18 continuing applications

[Workflow PR #26](https://github.com/VSBhargav5/RoleWeave/pull/26),
[saved letters and matching documents](https://github.com/VSBhargav5/RoleWeave/commit/f8f65a4cf7edf52c06eb3fbdf8ee9f7d8ea1d334),
[explicit search pages](https://github.com/VSBhargav5/RoleWeave/commit/095634c63c8dd6167aacdca425ec047c1538c051),
[board filters and reminders](https://github.com/VSBhargav5/RoleWeave/commit/4400b28da444069fd21643e84cf42a925ad1d25e),
[release and practice guide](https://github.com/VSBhargav5/RoleWeave/commit/061283b1d58c436f25b4a066deb33ed063e5675e).

Saved cover letters reopen after restart in Documents and exact-job application
kits. Recipient ZIPs can include a PDF plus a same-job/frozen-profile letter TXT;
private sources/history remain excluded. Corrupt files are reported and preserved.
The catalog is bounded; private web artifacts still need separate preservation
outside shelf backups.

Discovery has explicit Previous/Next20-record pages, validated provider offsets,
retained destination market, scoped result labels and no automatic polling.
Concurrent searches are refused, and failed requests preserve prior results.
Pages can move/repeat as a live source changes; no completeness/closure claim.
A generic public IN/data-engineer offset20 check accepted20records/excluded0.
Applications combines market/text/stage/due filters. Stage/submission forms keep
existing reminders; stale saves refuse, while explicit reload retains drafts and
shows newer tracking, resetting submission confirmation.

304 offline Windows tests pass. Expanded Chromium checks cover letter reopening,
recipient selection, reminder preservation, concurrent tracking refusal/reload,
combined filters and21synthetic records over2pages, alongside earlier document
and7native-contact-fill/no-submit checks. Source/frozen runtime checks and bundled
asset equality pass. The complete v0.18 ZIP and a separate verified Windows copy
are available; promotion into the current app folder was refused because it was
open, preserving that package. Real installed-helper/employer compatibility,
personal acceptance, signing and optional live integrations remain unverified.
No personal data, paid call, account link or actual application was sent.
All6PR CI43414730533 jobs passed, including browser, Windows/Linux3.11/3.12,
portable/installed runtime and installer lifecycle/checksums. PR #26 merged at
955db25a1b5a5f5e9827e7c278a0e412e86ae244; tested/published tree
ba53f048be84117feea2f5a7ae1280b3724eff9b matches exactly.

## 13 November 2026 — RoleWeave browser application workspace

[Workspace and form-helper PR #25](https://github.com/VSBhargav5/RoleWeave/pull/25),
[implementation](https://github.com/VSBhargav5/RoleWeave/commit/d4b16016660697dc943fb9fa7b0664be02fd14d7),
[setup and runnable checks](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/browser-workspace.md).

The default launcher opens a browser-rendered charcoal/lime workspace with CSS
and original SVG rather than another native Tkinter theme. Python/SQLite remain
authoritative and native advanced tools remain accessible. Users search by role,
location, country and remote preference through the personal/non-commercial
FreeHire API, explicitly choose an application market, review evidence, freeze
resumes/letters, download recipient documents and record their own submissions.
One generic public IN search returned20 accepted records with0 exclusions;
provider totals are not verified coverage, relevance or sponsorship evidence.

The original MV3 Chrome/Edge helper uses activeTab and session memory. It loads
only an explicitly prepared contact sheet, previews destination/fields and fills
checked supported empty native contact inputs after consent. It never submits,
uploads, clicks Next, overwrites existing values or answers sensitive questions.
No upstream Dossier source/assets/history were imported.

298 offline native Windows tests pass. Chromium verifies synthetic search/save,
PDF, letter and recipient ZIP downloads, submission tracking, draft guards,
seven actual native input fills, stale-preview refusal and zero submits. Desktop
and900px layouts were checked and screenshots inspected. Source/frozen web assets
and retained native runtime smoke pass; bundled assets match committed source.
All six PR CI checks passed, including browser-workflow, four Python jobs
and Windows portable/installer lifecycle checks. PR #25 is merged at
960ca73d36f94cb511f4b2c47d84c7f8987c0901; tested/published tree
60bf9ccc272d9f9198956c842d7faec75dc6902b matches exactly. Public/production readiness is
not inferred from these checks. Manual helper installation/toolbar permissions,
real ATS compatibility, personal acceptance, signing and optional live accounts
remain unverified. Separate private web artifacts are outside shelf backups.

## 12 November 2026 — RoleWeave v0.16 practical application handoff

[Handoff PR #24](https://github.com/VSBhargav5/RoleWeave/pull/24),
[upload folders](https://github.com/VSBhargav5/RoleWeave/commit/17191da366cb56ce6f5f12b0cc9109df73af093c),
[structured submissions](https://github.com/VSBhargav5/RoleWeave/commit/9abc2fbbdc7ac8a5817a9b2ec9c9dce944169acf),
[release verification](https://github.com/VSBhargav5/RoleWeave/commit/705a39a6437f753051b360230ddea08ebfb29685).

Users can select PDF/TXT/HTML/matching-letter files with checkboxes and save an
upload-ready folder. No format-name typing or ZIP extraction is required.
Only recipient documents are written; private sources/history are excluded.
Existing folders are never reused. The local completion note is published last;
failed exports can leave an incomplete folder without that note and never
claim success. The user can open the saved folder and upload documents manually.
Legacy ZIP export remains available; no automatic upload or applying is added.

Tracking now opens a structured submission form for date, channel, reference,
note and follow-up without a private dossier. A matching dossier remains an
optional evidence link. Older submission notes retain interview/offer/closed
states. Stale forms cannot overwrite newer tracking; explicit reload preserves
submission fields and requires renewed confirmation. Exact duplicates are
refused. A saved observation followed by view failure is reported as saved.

291 native Windows offline tests, final source/frozen self-tests and the updated
fresh-user UI journey pass. That journey exports actual PDF/TXT upload files,
checks private-source exclusion, records a basic structured submission after a
mocked browser handoff and restores history/documents into another shelf; it
creates no ZIP/dossier file. Native minimum-size form controls and cancellation,
partial writes, stale drafts and refresh failures have regressions. Packaged
smoke checks upload-folder generation and the native picker. Tested tree:
`3da6d718ed2e7bc0fccc6b6408ea835164ac040f`.

No personal/employer data, real application/upload, live account or paid model
call was used. Real portal behavior, personal usability and unusual scaling
remain unverified. [Updated first-application guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/first-application.md).

## 12 November 2026 — RoleWeave v0.15 complete manual application journey

[Workflow PR #23](https://github.com/VSBhargav5/RoleWeave/pull/23),
[implementation](https://github.com/VSBhargav5/RoleWeave/commit/aa5670d70a618a9ad4bc3763566cc051f2029eb4).

The owner clarified the goal: a user must be able to complete the application
journey, not accumulate isolated features and tests. A visible Apply workspace
now connects reviewed career profile, exact job evidence, frozen PDF resume,
optional letter/recipient bundle, employer-page handoff and manual tracking.
Actual saved prerequisites are explained. Basic Applied/follow-up tracking needs
no private dossier. Recipient files are emphasized; private archives remain
private. A failed browser launch is reported instead of claiming the page opened.
Opening a page or exporting documents never marks an application Applied.

The fresh-user native UI journey starts from an empty shelf, saves a posting,
creates a reviewed profile, links evidence, freezes/exports a PDF, parses its
text, exports a letter and recipient-only ZIP, exercises a mocked browser
handoff, records explicit Applied/follow-up and restores the records into a
separate shelf. Private source notes are absent from employer-facing files;
no private dossier is written. This verifies the local software journey, not
an actual employer submission, successful hiring outcome or personal usefulness.

276 offline Windows tests, final focused journey checks and source/frozen v0.15
self-tests pass. Tested/published tree: `2fd2ea32e2980f07c657cc644a8a4eb7c8808c12`.
[First-application walkthrough](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/first-application.md)
explains direct PDF upload, extracting recipient ZIPs, manual employer-site
submission and tracking without a dossier. Google/AI stay optional previews;
real portal behavior, unusual scaling and user acceptance remain unverified.

## 12 November 2026 — RoleWeave v0.14 release safety beta

[Release-safety PR #22](https://github.com/VSBhargav5/RoleWeave/pull/22),
[schema compatibility](https://github.com/VSBhargav5/RoleWeave/commit/20e542722fb33485a7c2bbe3df4ce8cfbeac2b08),
[private UI errors](https://github.com/VSBhargav5/RoleWeave/commit/84056f75022b29f53b9bcaa77a0e670f40b8d566),
[release gates](https://github.com/VSBhargav5/RoleWeave/commit/575a56ed44ff7e541c204fe0d3ec051a57d5c0de).

The user requested production readiness. Auditing startup found that table
initialization could touch incompatible files before detecting the problem.
Known legacy declarations are now adopted atomically; foreign/newer/altered
schemas and unexpected objects are refused before DDL. Valid marked shelves
reopen without header rewrites. Regression fixtures prove source-row preservation,
byte-preserving refusals and rollback after a synthetic mid-adoption failure.

Unexpected Tk callbacks show RW-UI-001 without private exception text,
persistence, transmission or automatic retry. The message warns that prior work
may already have committed and asks users to inspect state before repeating it.
Startup errors exit nonzero. This does not claim power-loss recovery.

272 offline native Windows tests and source/frozen v0.14 synthetic self-tests
passed. [PR CI](https://github.com/VSBhargav5/RoleWeave/actions/runs/43151637777)
checks portable and installed behavior and emits same-run SHA256SUMS for the
ZIP/setup artifacts. Checksums detect changed downloads; they are not signing.
The tested/published tree is `6846f518d3bbe9a3f438aa7080b9384145c937bd`.

The owner selected local Windows v1 first. Google/AI stay optional previews
outside local-v1 acceptance. This remains an unsigned controlled beta:
clean-Windows human acceptance, signing/distribution and interrupted-upgrade
confidence remain open; no production, adoption or usefulness claim is made. No real database,
account, credential or paid call was used. See the
[release acceptance and rollback guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/release-acceptance.md).

## 11 November 2026 — RoleWeave v0.13 dark neon workspace

[UI PR #21](https://github.com/VSBhargav5/RoleWeave/pull/21),
[implementation commit](https://github.com/VSBhargav5/RoleWeave/commit/7db924daf0b483d7efdb3456a27554625697035e).

The user requested black/dark colors, gradients, neon accents and better
alignment. The native workspace now uses near-black surfaces, rounded ttk
controls, violet actions, cyan highlights, compact tinted metrics, preferred
Segoe UI Variable Text and original gradient weave artwork. Exact requirement
quotes, linked claims and sources appear as distinct evidence cards. Large
reviews have bounded 20-card pages; explicit copying preserves the full review.
Existing workflow identity, draft guards and native consent controls remain.
No new dependency, backend rewrite or network-loaded asset was introduced.

261 offline Windows tests, eight final design tests and source/frozen v0.13
synthetic self-tests passed. The main synthetic Windows workspace was visually
inspected. Contrast, exact evidence, pagination, explicit copying, disabled
consent controls and minimum-size layouts have regression coverage. The tested
and connector-published tree is `1cc638da08a416b56d079fbcd1811aee8d1d7ba3`.
[PR CI](https://github.com/VSBhargav5/RoleWeave/actions/runs/43004668316)
checks source, portable and installed behavior. Local exe/ZIP refreshed.
Unusual scaling, every native file dialog, personal acceptance and live
Google/AI behavior remain unverified. No personal window/data or live account
was used in this redesign.

## 11 November 2026 — RoleWeave v0.12 Windows workspace refresh

[PR #20 merged](https://github.com/VSBhargav5/RoleWeave/pull/20).
[Workspace implementation](https://github.com/VSBhargav5/RoleWeave/commit/477eed44a58292b1b022c7955cf9fb8f07c82787),
[compact-filter correction](https://github.com/VSBhargav5/RoleWeave/commit/fa1d677884703bfb7272a1d92efb0e3f464042a1).

Dense single-line job rows now show role/company on two lines with a separate
manual-stage column. Rows use immutable review IDs through sorting/filtering;
existing tracking/export/draft guards remain. Filters collapse without losing
values or the opened draft, and a visible summary preserves scope awareness.
Indigo accents, a midnight rail/monogram, pastel metric cards, bordered work
surfaces, clearer primary/secondary actions, stage badges and distinct linked/
open/source typography give the native app a stronger reading hierarchy.

Freshly authorized synthetic previews were visually inspected. Footer wrapping,
native tab borders and taskbar overlap were corrected. A separate minimum-size
check caught the expanded drawer leaving too little list space; the final compact
layout retains visible role rows and posting space at1040x700. No personal window
or data was controlled; full manual interaction/unusual scaling acceptance is
still unverified. No screenshot bodies or private data are published here.

259 final offline native Windows tests, exact final source and frozen runtime
self-tests passed. All five [final PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42991657450)
passed, including portable/installed runtime and installer lifecycle. The final
connector tree matches the tested tree `e45705b02cd6e0f3c28e32904ad01ab88da7a451`.
Local v0.12 exe/ZIP refreshed. No new theme dependency, schema migration, hosted
frontend or provider/account behavior. Google OAuth setup/live trial, AI quality,
provider coverage and personal usefulness remain evidence gates.

[Design guide and runnable verification](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/workspace-design.md).

## 11 November 2026 — RoleWeave v0.11 personal readiness and Google follow-ups

[Readiness PR #18](https://github.com/VSBhargav5/RoleWeave/pull/18) and
[Google Calendar PR #19](https://github.com/VSBhargav5/RoleWeave/pull/19) are merged.
[Readiness release](https://github.com/VSBhargav5/RoleWeave/commit/9105abccb0220f23de324ec0705b6c85297811cd),
[Calendar release](https://github.com/VSBhargav5/RoleWeave/commit/f5a3975a43f0bdc5a821fa50f79f8412632ef601).

The user requested a concrete readiness breakdown and selected Google Calendar
follow-up sync first. Getting started now has readable current-workflow,
readiness and storage tabs. It distinguishes eight implemented/offline-tested
local workflow groups from personal acceptance and optional online gates;
there is no invented overall completion percentage. Reproduced immediate-close
Tk theme errors and cancelled-worker poll callbacks are fixed with regressions.

The Google integration uses browser consent/PKCE/state through Google's
maintained library and only app-created-secondary-calendar scope. Credentials
stay in memory for the window; no config/token file lookup, persistence or
automatic refresh. Windows separates scope consent, deliberate calendar creation,
local-only preview, consented exact-event read and one confirmed create/update.
Generic private reminders are default; company/role is opt-in. Deterministic
base32hex IDs, exact local source/history checks and conditional ETag PATCH guard
duplicates/stale writes. No primary calendar, invitations, automatic deletions,
background/two-way sync, mailbox access or local application-stage mutation.
Cancellation cannot reverse remote processing. OAuth adds pinned dependencies
whose licenses/metadata are included in the portable build.

One unauthenticated bounded GET per documented public board example parsed
Greenhouse19posts and Lever EU6; Lever global was empty. Ashby returned76listed
records but three descriptions around357000characters exceeded the50000-character
posting contract, so the entire feed was refused. Errors now name row/size and
next steps; there is no silent truncation/subset import. Only metadata/hashes
are published, not employer posting bodies. This is limited historical evidence,
not complete provider coverage or current job recommendations.

258 final offline native Windows tests and source/frozen v0.11 runtime checks
passed. All five [readiness PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42961711298)
and [Calendar PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42963395268)
passed, including portable/installed runtime and installer lifecycle. The final
suite had zero prior ThemeChanged/shutdown diagnostics. Tested/published tree:
`9b77b197a8ab75b37a12f570cdb6f8a53582d657`. Local exe/ZIP refreshed; main clean.

No Google account linked, calendar created, event written, paid model call or
personal transmission. Desktop OAuth client setup and a synthetic live Calendar
trial are required. AI quality, calendar-client import, manual UI acceptance,
source coverage and personal usefulness remain unverified. Mailbox/general
account synchronization is not implemented. Separate artifacts remain outside
shelf backups; no new outcome/authenticity/recovery guarantee is claimed.

[Readiness matrix/start here](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/personal-readiness.md),
[Google setup and controlled trial](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/google-calendar.md).

## 11 November 2026 — RoleWeave v0.10.1 private rehearsal and shelf verification

[Rehearsal PR #16](https://github.com/VSBhargav5/RoleWeave/pull/16) and
[read-only audit PR #17](https://github.com/VSBhargav5/RoleWeave/pull/17) are merged.
[Rehearsal release](https://github.com/VSBhargav5/RoleWeave/commit/f46063099aed8ca02e8e14d34c0b8adc69680402),
[audit implementation](https://github.com/VSBhargav5/RoleWeave/commit/87dbb79c4d0bd594d77b3cc3b1ac1836e407e64e).

Selected requirement IDs now anchor private answer/reflection drafts to the exact
frozen review. Windows navigation/reveal preserves drafts; save/reopen preserves
source identity. Re-selecting or restoring unchanged questions cannot manufacture
a timestamp-only version. Private TXT packs contain selected quotes/evidence,
with answer drafts only by explicit choice. An explicitly started local timer
records unverified elapsed seconds. Version comparison requires the same exact
source and shows text/selection changes without assigning a learning score.

SQLite structure can pass while source bytes/references are inconsistent. The
new audit checks every stored review, profile, resume, history sequence and
reference in one bounded read-only snapshot. It rejects shelves above10000 rows
or64MiB field bytes, never repairs/writes, and omits source claims/notes from
optional private ID/check reports. Separate exported files are outside the audit.

245 offline native Windows tests and source/frozen v0.10.1 self-tests passed.
All five [rehearsal CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42959279534)
and all five [audit CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42959858269)
passed, including portable/installed runtime and installer lifecycle. Local
portable exe/ZIP are refreshed. Tested/published tree:
`5aa576ea3a5a40c311aa9ef0a88eb9bffa00b967`. Existing Tk theme shutdown diagnostics
persist despite passing assertions. A disposable test fixture initially retained
a SQLite connection; explicit closure corrected it before the final suite.

No dependency/schema migration or live/personal transmission. Journals/packs are
unencrypted separate files, outside shelf backups. Hashes do not authenticate
claims. Recorded time and draft changes do not verify learning; no application
stage is changed by rehearsal. Audit checks stored PDF contracts rather than
renderer replay and does not guarantee recovery. Manual dialogs/scaling, large-
shelf performance, real-feed compatibility, live AI quality, remote integrations
and personal usefulness remain unverified. Next is a focused user trial and
observed fixes, not an automatic expansion of the feature list.

[Runnable60-90minute practice](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/rehearsal-workflow.md),
[read-only audit verification](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/shelf-audit.md).

## 11 November 2026 — RoleWeave v0.9 selected-source collections

[PR #15 merged](https://github.com/VSBhargav5/RoleWeave/pull/15) ships eight coherent changes.
[Release](https://github.com/VSBhargav5/RoleWeave/commit/ce15b5c1e5f9fdcf567a2d36ad6335c3a0b79eef).
Explicit multi-board Windows review/import keeps source status/times separate.
Private original-byte archives reopen offline with local filters. Comparisons
distinguish failed/unselected sources from observed posting changes. Metadata-only
shortlists carry source fingerprints and partial-coverage counts. Failed-source
retries retain successful response bytes and their original ages.

225 offline native Windows tests/source smoke passed. All five [PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42957173679)
passed, including portable/installed runtime and installer lifecycle. Minimum-size
actions/reading space and cancellation-after-failure regressions pass. Existing Tk
teardown diagnostics persist despite passing assertions. Every connector tree
matches its tested local counterpart; final tree `1a9ee99b6fdb989d39fd4c761864b943937feddc`.

No new dependency/database migration, automatic scan, paid call, personal
transmission, account access or application. Archives are separate private files.
Hashes/time membership do not prove authenticity, completeness or eligibility.
Retried collections mix source ages; real-feed compatibility and manual user
acceptance remain unverified.
[Runnable workflow and60-90minute exercise](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/selected-collections.md).

## 10 November 2026 — RoleWeave employer-watchlist foundation

[PR #14 merged](https://github.com/VSBhargav5/RoleWeave/pull/14) contains four coherent changes.
[Stopping-point package](https://github.com/VSBhargav5/RoleWeave/commit/1c9ccb37e39309f4270eb2fd3da168a8640cea02).
Portable JSON stores checked board choices, explicit market defaults and local
filters. The Windows editor preserves unapplied drafts and opens a selected
discovery board without fetching. A source CLI explicitly fetches1-5 selected
boards with cancellation,16MiB total byte bounds and visible partial failures.

All five [PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42817866841) passed, including portable and installed runtimes.
204 offline Windows tests and source v0.8.1 self-test pass, including minimum-size
layout and offline saved-source reuse. Every connector tree matches the tested
source; final tree `c56be2c9a61949a189bc2bc78bc4a45146705c6f`.
The user wrapped up for today. Multi-board Windows collection preview/import,
collection archives/comparison and live compatibility remain unfinished.
[Exact continuation and guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/employer-watchlists.md).

Watchlist files remain separate from shelf backups. No automatic scanning,
account connection, paid call or actual application was performed. Prior v0.8
delivery features remain; manual user acceptance and usefulness are unverified.

## 10 November 2026 — RoleWeave v0.8 application delivery

[PR #13 merged](https://github.com/VSBhargav5/RoleWeave/pull/13) ships14 coherent changes.
[Release](https://github.com/VSBhargav5/RoleWeave/commit/73cec96dd0affb8e8dad8c24ac72d5cb9cb0ebe7).

Reviewed cover letters copy selected claims exactly and freeze profile/job context.
Private dossiers bind an exact review/resume/optional matching letter and replay
documents without archive extraction. Recipient-only exports exclude private
sources/history. Manual submission receipts and selected local plaintext email
excerpts append observations without sending or inferring hiring stages.
Optimistic revisions reject stale tracking writes; explicit reload preserves
user control over drafts. No database schema migration or new dependency.

194 offline native Windows tests and source smoke passed. All five [PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42815871690)
passed, including portable/installed end-to-end delivery and recovery.
New form minimum-size and tamper/concurrency regressions pass. Existing Tk teardown
diagnostics remain despite passing assertions. Every published tree matches the
tested local counterpart; final tree `d83813dee0c6cf8c993ea13ce5a01f46ab296e61`.

Private letter/dossier/email files are separate from shelf backups; recorded
observations use existing v3 recovery. PDF replay needs the matching deterministic
renderer and can refuse legacy outputs without deleting originals.
No paid calls, personal transmissions, account connection or actual application.
Live accounts/AI, manual dialogs/scaling and personal usefulness remain unverified.
[Workflow and60-90minute practice](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/application-delivery.md).

## 10 November 2026 — RoleWeave v0.7 discovery workspace

[PR #12 merged](https://github.com/VSBhargav5/RoleWeave/pull/12) contains nine coherent changes.
[Release commit](https://github.com/VSBhargav5/RoleWeave/commit/27b3e48f522e7475dc1141ceba4a9374b3594800).

- Public-board transport rejects credentials and POST bodies before dispatch.
- Lever global/EU and listed-only Ashby adapters preserve exact source identity.
- Windows provider/board-URL selection guards against importing stale results.
- Original-byte private archives replay offline and compare observations without closure inference.
- Description/exclusion filtering and observed-result counts run entirely locally.
- V0.7 runnable fixtures and packaged smoke exercise every supported provider.

All five [PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42807456479) passed, including portable and installed runtimes.
156 offline Windows tests and the source self-test passed. The expanded UI initially
collapsed the preview at850x650; actions are consolidated and the existing minimum
layout regression now passes. Every published commit tree matches its tested local
counterpart. Final tree: a1e02328e31b5ce5687f27737adc3d71c0f189d2.

Provider contracts were checked against current official docs. No live new-provider
fetch, paid call, profile transmission or account connection occurred. Real feed
compatibility, manual dialogs/unusual scaling and completeness remain unverified;
Lever responses at1000 posts fail closed. Archives are separate private files,
not part of shelf backups. Integrity does not prove authenticity or eligibility.

[Runnable discovery guide and60-90minute practice](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/discovery-workflow.md)
covers source identity, hidden Ashby listings, local filters, offline replay and why
not_observed cannot be called closed. No learning or usefulness claim is made.

## 10 November 2026 — RoleWeave per-user Windows setup

[PR #11 merged](https://github.com/VSBhargav5/RoleWeave/pull/11) adds an Inno Setup
installer, Start-menu entry and Windows uninstall support. Program files install
separately from the existing user database; no source-shelf migration or automatic
launch happens. The stable application ID supports an in-place reinstall.

139 offline Windows tests passed; existing Tk teardown diagnostics remain.
All five [PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/42799947287) passed.
Windows CI compiles setup and tests isolated installation, reinstall, installed
frozen runtime and uninstall while retaining synthetic data. Manual wizard
acceptance, signing/reputation and interrupted-upgrade recovery remain unverified.
The [installation guide](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/windows-installation.md)
documents backup, source/installed data locations and deliberate restore.

Live AI quality, calendar-client import and remote account integrations still
need their own authorized trials. No paid call, account linking or personal
transmission was performed. Other project sprints remain paused.

## 4 November 2026 — RoleWeave v0.6 daily-use readiness

[PR #10 merged](https://github.com/VSBhargav5/RoleWeave/pull/10) contains 19 coherent authored changes.
[Release commit](https://github.com/VSBhargav5/RoleWeave/commit/cebe184ee40f59722707dda85b333ab893dc2d3d).

- Atomic no-overwrite exports, Unicode/control validation and staged build rollback.
- Opt-in posting search, sort order, explicit source opening and guarded shortcuts.
- Private profile transfer with renewed review, frozen resume TXT and exact-job browsing.
- Read-only backup/storage inspection and filtered spreadsheet-safe CSV/calendar files.
- Related review comparison, exact-evidence rehearsal, fact search and offline AI payload export.

All five [PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/41813795960) passed.
137 offline native Windows tests passed; source and final packaged v0.6 full-workflow
self-tests passed. Tk teardown emitted ThemeChanged diagnostics despite passing tests.
Every connector-published commit tree matches its tested local counterpart; final tree
4729f9a579ceb7050521dffdc80ab74d0ad06702. No provider call or personal transmission.
Hard-link-capable storage is required for atomic exports; unsupported filesystems fail
closed. Build staging retains earlier directories for manual recovery. Manual layout,
calendar-client import, live AI quality and personal usefulness remain unverified.

[Runnable workflow and 60–90 minute practice](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/readiness-workflow.md)
covers a separate synthetic shelf, profile re-review, exact resume identity and backup
inspection. Learning is not marked complete without user practice.

## 4 November 2026 — RoleWeave Windows frontend redesign

[PR #9 merged](https://github.com/VSBhargav5/RoleWeave/pull/9) ·
[Implementation](https://github.com/VSBhargav5/RoleWeave/commit/ee3875a8d70fe07a367a0a9e47268b1b2f2106c9).
[Dialog allocation correction](https://github.com/VSBhargav5/RoleWeave/commit/62f9421428913ac4b53385b467fad30a71126614).
The crowded form becomes a navy navigation rail, pale canvas, white cards, teal
primary actions and Segoe UI typography. Posting, evidence/next steps and editable
details have separate tabs; descriptions get a full reading area and scrollbars.
Titles appear first in the opportunity list, filters explain empty results, and
global cards count saved review snapshots, active due follow-ups and frozen resume
versions. They do not claim unique applications or verified hiring outcomes.
Profile, resume, discovery, AI and tracking dialogs share the native ttk theme.

119 offline native Windows tests passed on Python 3.12.14. Added regressions cover
global counts versus filters, draft-preserving tabs, resume-count refresh and
all current-page actions staying mapped/full-height inside supported window sizes.
An evidence-editor Save action
was initially clipped at650px; its form is compacted and minimum height enforced
at700px, then verified. Source and final packaged full-workflow smoke passed
without provider calls. Packaged main/posting/evidence layouts were visually
checked on synthetic data. A profile footer collapse was caught during visual
review after the initial bounds-only test passed. Fixed shared footer allocation,
split the fact library/editor and strengthened tests across all dialog tabs.
The additional visual check was denied by Windows automation; the corrected
dialog's manual visual acceptance remains unverified. Tested tree:
`6f2e491e150c3ec6ebe98aaf678c7f7cab9c20b6`.
All five [final-head PR checks](https://github.com/VSBhargav5/RoleWeave/actions/runs/41804556610)
and all five [post-merge checks](https://github.com/VSBhargav5/RoleWeave/actions/runs/41805222822)
passed, including the packaged-runtime workflow.

No new runtime dependency, data migration or provider behavior change. Existing
private databases and v1/v2/v3 backups remain supported. Minimum main workspace
1040×700 logical pixels; unusual scaling/small displays and complete native
file-dialog acceptance still need user checks. Live AI, calendar-client import,
personal usefulness, account integrations and installer remain unverified/pending.
The [workspace guide and practice exercise](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/workspace-design.md)
explain navigation and why snapshots cannot be counted as applications sent.

## 4 November 2026 — RoleWeave discovery, AI quote review and calendar files

[PR #8 merged](https://github.com/VSBhargav5/RoleWeave/pull/8) ships six coherent changes:

- [Bounded public Greenhouse adapter and provenance](https://github.com/VSBhargav5/RoleWeave/commit/58ff852eff6d8eef05c5fd7711e4eea0748ce25c).
- [Cancellable Windows discovery, preview and explicit import](https://github.com/VSBhargav5/RoleWeave/commit/ed986004d60a31df8034c9fe77cc500f932ebc96).
- [Consent-bound AI exact-quote contract](https://github.com/VSBhargav5/RoleWeave/commit/f7cf08db2abf97ca0d0f445f87c7ae5b3df68896).
- [Request preview, session key and human quote adoption](https://github.com/VSBhargav5/RoleWeave/commit/3d9779c1a2d16e71ddc1beb8c2fca72402f7e398).
- [Private calendar follow-up export](https://github.com/VSBhargav5/RoleWeave/commit/076fb6a79ab25e897f76716c732883946d2f4cf2).
- [V0.4 portable smoke and explicit-use guide](https://github.com/VSBhargav5/RoleWeave/commit/639dc45a44e1e574c775d38bf6535a92034c964e).

116 offline native Windows tests passed on Python 3.12.14. Source and final
packaged executable smoke passed synthetic discovery → AI quote review →
HTML/PDF → calendar → v3 recovery without provider calls. Tested tree:
`f2b39ec621a37a97ae8e5fb1e63617a81bb81467`. Every published commit tree matches
its local counterpart. A Tk teardown diagnostic in an earlier run was addressed
by draining pending idle events in the new UI tests; final suite passed cleanly.
All five [PR CI jobs](https://github.com/VSBhargav5/RoleWeave/actions/runs/41792981922)
passed, including the packaged executable smoke. Local main is clean and
synchronized with the merge. Packaged main/discovery layout was visually checked;
AI review was exercised with native offline UI tests, not a live provider call.
All five [post-merge main checks](https://github.com/VSBhargav5/RoleWeave/actions/runs/41793294960) also passed.

One separate public GET through the source adapter observed 20 Greenhouse vacancy
posts at 2026-11-04T07:24:53Z, response SHA256
`be3b408ec52ffc2732c413abbff0792b0197812fc7e4c0c4fabe83e5fd73eed4`.
No profile/candidate data was sent. This establishes that response only, not all
boards or current vacancy availability. A sandbox network attempt failed before
the authorized network check succeeded.

Discovery imports selected posts into a manually chosen market. It never infers
eligibility, closes missing jobs or replaces earlier evidence. AI only receives
the explicitly previewed posting after per-request consent and session-key entry;
exact quotes still require relevance review before entering an unsaved draft.
No paid/live AI request was made; account access and model quality are unverified.
Cancel/store=false are not no-charge/zero-retention guarantees. Calendar files
include title/company, date and saved-review/history identity, excluding notes and
resumes. They require user import; no account linking, invitations or remote event
changes. Calendar-client acceptance, manual dialog coverage and personal usefulness
remain unverified. The portable build remains unsigned; no new runtime packages.

See the [connected workflow and focused exercise](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/connected-workflow.md).

## 4 November 2026 — RoleWeave local profile-to-resume release

[PR #7 merged](https://github.com/VSBhargav5/RoleWeave/pull/7) ships eight coherent changes:

- [Immutable reusable career profiles](https://github.com/VSBhargav5/RoleWeave/commit/6b487f9e5444f42093a33c06c36b5fdfab07f1f4).
- [Reviewed resume selection and safe HTML/PDF output](https://github.com/VSBhargav5/RoleWeave/commit/e507b54a0cbccd732b75ff84a605ef734ed2dfaf).
- [V3 profile/resume backup with v1/v2 compatibility](https://github.com/VSBhargav5/RoleWeave/commit/d709b6fd57247784a9bc4a6d3da12313e5b5e8d6).
- [Windows profile editor and deliberate fact reuse](https://github.com/VSBhargav5/RoleWeave/commit/10c755863a89115f1d2e5ac49d560f7de495111e).
- [Windows resume preview, approval, versioning and export](https://github.com/VSBhargav5/RoleWeave/commit/11eb9a402f9d7012f9d014ca6222daa64a4333b5).
- [Separate synthetic practice workspace and runtime self-test](https://github.com/VSBhargav5/RoleWeave/commit/b96c0ff3d17dbd224378565cbc620cdc8315d42a).
- [Portable Windows packaging, setup and CI](https://github.com/VSBhargav5/RoleWeave/commit/498a05bfa53e479a1e7938ae25783c3f90ab5fad).
- [Start guide and focused recovery exercise](https://github.com/VSBhargav5/RoleWeave/commit/03868d09607a64460ba045f4a0c1388db8eced4c).

92 native Windows tests passed on Python 3.12.14. All four OS/Python test jobs
and the portable-build/runtime job passed in [PR CI](https://github.com/VSBhargav5/RoleWeave/actions/runs/41773381960).
[Post-merge main CI also passed](https://github.com/VSBhargav5/RoleWeave/actions/runs/41773520315).
Every published commit tree matches its local snapshot; merged/tested tree:
`5b0408d258750ca45e21f6da77f28149516f82b9`. The final local executable passed
synthetic profile, frozen document export and full recovery smoke. A PDF was
rendered and visually checked; extracted text preserves selected claims.

Direct Windows UI checks covered profile display, claim selection, preview,
approval and saving a resume version. Native Save dialog completion could not be
automated reliably and remains a manual acceptance item. Initial local test runs
hit sandbox temp permissions and a missing test dependency; both were resolved
before the final green run.

Profile corrections never rewrite old resume bytes. No claim is invented or
rewritten, and unreviewed facts cannot be selected. V3 backups preserve source
profiles and exact documents privately; older backups remain readable. Data and
exports are unencrypted. The unsigned portable build requires its whole folder;
it is not an installer. Unsupported PDF glyphs require HTML/browser printing.
Personal usefulness, ATS behavior and real outcomes remain unverified. Live
discovery, AI assistance, external integrations and submissions are not shipped.
No personal data or paid calls were used.

Try the [resume version/recovery exercise](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/resume-first-principles.md)
in a separate synthetic workspace. Practice is not marked complete by the build.

## 3 November 2026 — RoleWeave manual application workflow

[PR #6 merged](https://github.com/VSBhargav5/RoleWeave/pull/6) ships six tested changes:

- [Manual stage, note and follow-up history](https://github.com/VSBhargav5/RoleWeave/commit/3d1e6f4bd72144d7463622f2f156ef918d6ac01e).
- [Backup v2 history preservation and v1 compatibility](https://github.com/VSBhargav5/RoleWeave/commit/9b0e19094d371167699b762d0ad3dbfb81f4d7bb).
- [Combined market, stage, Unicode search and due-date filters](https://github.com/VSBhargav5/RoleWeave/commit/4be417caa079aa94be544cd6936673896d51160c).
- [Windows application tracker](https://github.com/VSBhargav5/RoleWeave/commit/d5520c625e8958b4891f1eed7ad033f07728e7d2).
- [Private text preparation packs](https://github.com/VSBhargav5/RoleWeave/commit/74815d82e8440ab34669d33dc5368dd557e8d4f1).
- [Unsaved-draft guards and focused learning exercise](https://github.com/VSBhargav5/RoleWeave/commit/7b41b5cf3a426b32333d5092e7c4fb2a26d9caa2).

66 Windows tests passed and all four Python3.11/3.12 Windows/Linux PR CI jobs
passed. Linux skips native Windows UI checks. Tested and merged tree:
`6c0c09e1324a00efe4acc19d76a8441a468acb1d`. Every published commit tree matches
its tested local counterpart. One draft-guard test initially failed because an
assertion was placed in the wrong test; it was corrected before final checks.

Tracking is a manual observation tied to an exact saved review; later evidence
revisions do not inherit applied status. V2 backups preserve history; v1 restores
do not erase it, and divergent histories fail atomically. Preparation packs copy
only selected reviewed claims and keep open questions; they are not resumes or
submissions. Follow-ups use local calendar dates in the app, without background
notifications. Drafts remain unsaved until explicitly saved/recorded.

No personal data, network/provider calls or dependencies added. Shared career
profiles, resume/PDF output, permitted live discovery, AI assistance, integrations
and installer remain pending. Manual dialog/layout use and personal usefulness
remain unverified. Try the [synthetic workflow exercise](https://github.com/VSBhargav5/RoleWeave/blob/main/docs/application-first-principles.md).

## 3 November 2026 — RoleWeave fact corrections

[PR #5 merged](https://github.com/VSBhargav5/RoleWeave/pull/5) ·
[Implementation](https://github.com/VSBhargav5/RoleWeave/commit/1e2279153fd92da1b205b94226bdcff4da0ccb53).
Load and correct an existing fact in the evidence editor. Loading clears the
review checkbox. Changed claim/source or revoked review clears every old
requirement link; unchanged reviewed facts keep links. Referenced facts cannot
be removed until unlinked. Saving creates a new snapshot and preserves originals.
37 Windows tests pass, including five cross-platform fact-change tests and two
native UI correction/removal checks. All four Windows/Linux Python3.11/3.12 CI
jobs passed (Linux skips native UI). Tested/merged tree:
`d3fda70dfe81d281d41bc9687163121e58f4189f`.
No new dependencies, personal data or AI calls. Manual layout/dialog interaction,
personal usefulness and resume tailoring remain unverified or pending. Reviewed
flags and links remain human assertions, not proof of qualification.

## 3 November 2026 — RoleWeave full backup and restore

[PR #4 merged](https://github.com/VSBhargav5/RoleWeave/pull/4) ·
[Implementation](https://github.com/VSBhargav5/RoleWeave/commit/d81e9d622b79f09fc7a0ca277074bdf6b84d58f5).
Full-shelf backup now includes job metadata, separate markets, capture timestamps
and original review bytes. Restore validates records, skips duplicates, and rolls
back all inserts on an ID conflict. Backups refuse existing filenames; JSON files
are bounded to 64 MiB and original reviews to 1 MiB each.
30 Windows tests pass, including eight recovery tests and native UI wiring.
All four Python3.11/3.12 Windows/Linux CI jobs passed (Linux skips native UI).
Tested/merged tree: `63b18260bc99ed4c66e76066027ca99b5a2f6a31`.
Synthetic recovery into a fresh shelf and repeat restore were verified. Personal
recovery and manual dialogs remain unverified. Backup files are unencrypted;
source fingerprints do not authenticate metadata. A failed write may leave a
partial backup file, which must be discarded and retried under a new filename.

## 3 November 2026 — RoleWeave evidence editor

[PR #3 merged](https://github.com/VSBhargav5/RoleWeave/pull/3) ·
[Implementation](https://github.com/VSBhargav5/RoleWeave/commit/07ea559c3e2626550e7434c8039df36602162676).
The Windows app now edits exact requirement quotes, adds human-reviewed claims
with source provenance, and links selected facts to requirements. Invalid quotes
and unreviewed links fail validation. Pending form edits block saving rather
than disappearing; saving appends a new snapshot and keeps originals intact.
22 Windows tests pass, including four new native editor regressions; all four
Python3.11/3.12 Windows/Linux CI jobs passed (Linux skips native UI tests).
Tested/merged tree: `6d9dd7ccdb4277e005fa60126b2188bc426ebb08`.
Existing fact revision/removal and resume tailoring remain pending. Links and
reviewed flags are human assertions, not proof of qualification or eligibility.
No AI calls, personal data or new dependencies. Manual layout/dialog interaction
and personal usefulness remain unverified.

## 3 November 2026 — RoleWeave local job shelf

[PR #2 merged](https://github.com/VSBhargav5/RoleWeave/pull/2) ·
[Implementation](https://github.com/VSBhargav5/RoleWeave/commit/636953482f738fca194c8e1639e0e3bbb6bb23e8).
Save and reopen manually selected postings in a local Tkinter/SQLite app, filter
India/remote and relocation separately, import existing evidence reviews and
export their exact original JSON without overwriting files. Changed source hashes
fail on reopen. Edits append a new posting without inheriting old evidence links.
18 local Windows tests passed, including native UI save/reopen/filter/import;
all four Windows/Linux Python 3.11/3.12 CI jobs passed (Linux skips native UI).
An initial test run found unclosed SQLite connections; explicit closure resolved
Windows file locks. Tested/merged tree: `ceefd097e3e2487fb3eaa6de2f1d5c5f8280bf70`.
No new dependencies, AI calls, personal data, scraping or submissions. Export
excludes job metadata; full backup/restore, evidence editing, desktop launcher
interaction and personal usefulness remain unverified or pending.

## 31 October 2026 — CueDesk screen-assisted study

[PR #2 merged](https://github.com/VSBhargav5/CueDesk/pull/2) ·
[Implementation](https://github.com/VSBhargav5/CueDesk/commit/9b89ef97730b715b9a0eb078ea4ee425e194c288).
The Cue-derived Windows launcher now lists screens/windows, previews a selected
still, and sends the reviewed image and question to OpenAI after explicit consent.
It supports session-only key entry, cancellation, pinning and a local launcher.
306 offline tests and the synthetic Windows Electron smoke passed; all four PR
CI jobs passed. The tested and merged tree is `f140108eb8c3f1979f4124105b35eb1839f0857c`.
Real screen selection, a live provider response and meeting features remain
unverified; no personal screen or paid call was used. Calls may incur charges.

## 31 October 2026 — StudyFrame v0.2 screenshot focus and installed-build repair

[PR #4 merged](https://github.com/VSBhargav5/StudyFrame/pull/4) ·
[Implementation](https://github.com/VSBhargav5/StudyFrame/commit/3e6ab087e6fe661250be0e263b9c72abe888a1e6).
Drag a crop or use pixel controls to select the relevant part of a saved image.
The resulting preview and request contain a fresh selected-pixel PNG without
source metadata. Restore original returns the exact original byte snapshot.
Crop/restore reset request/consent/follow-up state; cancel preserves prior state.
No original file overwrite, screen capture or automatic send.

Investigation found the installed v0.1.0 wheel still lacked AI send/follow-ups
despite upgraded source. Refreshed the local installation to v0.2.0, added a
visible version and Launch-StudyFrame.cmd, and added CI checks for installed
imports outside the source directory. This prevents testing only current source
while a previously installed entry point remains stale.

70 tests cover native Windows Qt, 11 new crop pixel,
metadata, coordinate, payload, cancellation and restore checks. Synthetic crop
editor/result rendered and inspected. Installed imports outside the project
report v0.2.0 and expose AI, follow-up and crop actions. Tested/published tree:
`c2b0a0dccb4e13689e79115f68ac4dc07de1df41`.
Linux Python 3.11 CI twice passed all assertions then crashed during native Qt
interpreter shutdown with 6.12.0. Explicit disposal alone did not resolve it;
the release pins official PySide6 Essentials/Shiboken 6.11.3 and adds a native
raster-call exit check. Both failed runs remain in PR history. Exact native root
cause was not independently proved.
All four final PR jobs passed on Python 3.11/3.12 Windows/Linux, including
installed-package imports and synthetic crop rendering. The installed local
build also passed all 70 tests from outside the source folder, with no broken
dependency requirements.

No paid calls or personal images used. Crop encoding/decoding are synchronous and
unbenchmarked; live account access/model quality, manual Windows interaction and
installer remain unverified. Next focused practice: crop a synthetic code block,
predict pixel bounds and compare crop/original hashes after restore.

## 31 October 2026 — StudyFrame guided study and follow-ups

The user returned the active sprint to StudyFrame and put RoleWeave aside.
[StudyFrame PR #3](https://github.com/VSBhargav5/StudyFrame/pull/3) introduces
Question, Review and send, and Answer tabs; explicit answer copying; and a
reviewed follow-up that includes only the immediately prior question and answer.
Current notes/image are included again; source edits, new question and clear
discard selected prior context. Each send requires a new review/consent.
Merged after all four PR CI jobs passed on Python 3.11/3.12 Windows/Linux.
Merge: `29209b86df915ee9a5f0f6d336c9dd8c584eb56c`.

Previous exchanges are bounded to a 4,000-character question and 12,000-character
answer; oversized answers stay readable/copyable but cannot start a follow-up.
Earlier turns are omitted and answers remain unverified reference material.
Final review fixed clearing the retained sent-question field.

58 offline tests pass locally with offscreen and native Windows Qt. The actual
Windows layout was rendered and inspected. Tested/published final tree:
`e5fbb86b949f0b9e0f0769424dcfdd2a73a414f1`.
[UI change](https://github.com/VSBhargav5/StudyFrame/commit/c64223d626c7568ccb9a49f253f368c71755115f) ·
[Follow-ups](https://github.com/VSBhargav5/StudyFrame/commit/6581f7f8ae275b5564a4542a6b1cd26718227bb1) ·
[Clear correction](https://github.com/VSBhargav5/StudyFrame/commit/2a6583624253e33632484dee4678b3ec15d99d91).

No paid calls, personal image transmission or live model-quality evaluation were
performed. Manual Windows dialog/physical clipboard and installer remain open.
Next learning: predict what the second/third follow-up sends, inspect the exact
preview and payload test, and explain bounded context versus full conversation.
An authorized synthetic live trial and personally checked answer remain the MVP
evidence gate. RoleWeave and SettleTrace remain set aside.

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
