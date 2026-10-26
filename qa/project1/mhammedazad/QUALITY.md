# MhammedAzad - Member 2 / B - editing and deletion

SECJ3343 Project 1, Group TaskFlow; leader Aland Karwan. Due 27 October 2026
(Asia/Baghdad). Software baseline main@5133a6c; authored on bc7b08e, whose src/ and
root README.md are identical to that baseline.

## Identity and ownership

GitHub CLI authentication was verified as MhammedAzad. `gh api user -q .name`
returned no value; `git config user.name` also returned no value, so the requested
GitHub-login fallback is used as FULL_NAME, with safe account/file stem
`mhammedazad`. The repository roster's B placeholder is Lanya; it has not been
changed or treated as evidence of this user's name. Only slot B is authored here.
origin is MhammedAzad/TaskFlow; upstream is aland99/TaskFlow. Branch:
codex/project1-member-b. No collaborator invitation or merge is needed.

## Design inventory and scope

- 41 manual cases: TC-B-001 through TC-B-041; 135 numbered action/result pairs.
- 14 requirements: REQ-B-001 through REQ-B-014, across SRS-B-EDIT,
  SRS-B-CANCEL and SRS-B-DELETE.
- Three child suites: TS-B1 (18), TS-B2 (9), TS-B3 (14), under
  B - MhammedAzad - Editing and deletion.
- 83 designed requirement/case links. Structural coverage is 14/14 (100%);
  every case references at least one defined requirement. This is **design
  coverage**, not verified database coverage or execution coverage.
- Techniques: EP (representative invalid/optional/single-task partitions),
  Decision Table (explicit invalid-title/invalid-description rejection row),
  State Transition (named saved/draft/rejected/closed/removed states), Use Case,
  and Error Guessing (stale targets, duplicate titles, unchanged saves,
  interior mouse events). No numeric boundary sweep is claimed by B.
- Assertions cover README TF-REQ-009–015 and edit persistence only of TF-REQ-018.
  Shared creation, valid enum/date selections and reload are setup/observations
  of edit/delete outcomes. A owns creation/text-boundary/counter behavior;
  C owns enum/date partitions and status/counts; D owns queries; E owns general
  storage recovery, navigation and modal accessibility.
- Each independent case includes exact disposable-profile JSON setup, original
  identities/timestamps, concrete data and exact UI/error text. Timestamp
  assertions use raw ISO values, not the formatted Created label.
- Requirements cite the root README sections and implementing src paths/functions.
  Code-derived dismissal/repeated-operation refinements are explicitly identified.

## Checks actually completed on 27 October 2026 (Asia/Baghdad)

1. Read qa/project1/README.md, root README.md, App updateTask/deleteTask/commit,
   TaskFormModal, ConfirmDeleteModal, Modal, TaskCard, normalizeValues and
   validateTask. Used Aland's module for data structure and quality reference;
   authored B requirements, fixtures, actions and expectations independently.
2. `python3 -I qa/testlink/scripts/validate.py mhammedazad` passed using the
   available Python 3.12.14 interpreter. Recorded in design-validation.json.
   Unique IDs, valid techniques/importance, nonempty action/result steps and
   both directions of the declared mappings were checked.
3. Existing application utility suite: **23 checks passed**. Production build:
   **passed**. These pre-existing checks are supporting verification, not new
   B-authored tests or execution of all 41 manual designs.
4. TaskFlow ran on http://localhost:5173. Chrome 156.0.8078.48 used a new disposable
   profile. Nine grouped automated design-oracle spot checks observed prefill,
   title-edit identity/timestamps/sibling preservation, whole-edit rejection,
   correction/save, four edit dismissal paths, priority reload/reopen persistence,
   exact deletion warning, four deletion dismissal paths, intended-id deletion and
   same-title sibling deletion. Detailed observations and three screenshots are
   under evidence/. These are limited spot checks, not a full manual test run.
   Two initial automation-selector ambiguities were corrected by scoping controls
   to the dialog and selecting the first fixture-ready element; the final run
   completed successfully. Neither issue was an application defect.
5. Reviewed the prefilled edit and deletion confirmation screenshots. The labels,
   control values, buttons and exact warning match the authored expectations.
6. Git, gh, Python 3, Google Chrome and Poppler were located/verified. GitHub CLI
   was downloaded and authenticated by the human. Portable Git supplies Bash;
   OpenSSL TLS was used because Windows Schannel could not acquire credentials
   inside the sandbox. The fork was created with gh repo fork and cloned safely.
   npm's lockfile rewrite and the loader's generated shared header change were
   restored; neither shared tooling nor another member's files are included.

## Physical Windows installation blocker — not completed

Docker Desktop was downloaded from its official distribution and its Authenticode
signature verified. Its per-user installer deployed files but failed on required
Windows registry writes (HKCU Run; access denied). Windows also reports WSL is
not installed. The Docker client exists, but `docker info` cannot connect to the
docker_engine named pipe: there is no running Docker engine. Finishing installation
and WSL enablement needs a human Windows approval/install step outside this sandbox.

Actual requested command attempts:

- `bash qa/testlink/setup.sh`: failed at the macOS `open -a Docker` fallback
  (`open: command not found`) after Docker was unavailable. The script was not edited.
- `python3 -I qa/testlink/scripts/load.py mhammedazad`: failed on its first Docker
  Compose SQL query, exit 125. No local project, B account, cases, requirements,
  plan or build can be claimed as loaded.
- `python3 -I qa/testlink/scripts/report.py mhammedazad`: connection refused at
  localhost:8090. No real TestLink PDFs or XML exports were produced.

Therefore **actual TestLink counts/authorship/coverage, plan/build assignment,
PDF first/middle/last-page review, long-field PDF review and XML export checks
are pending**. No PDF or XML is substituted or fabricated. No TestLink execution
results were recorded. Windows also requires an external runtime compatibility
adapter for report.py's hardcoded macOS Chrome executable/path; the shared script
must remain unchanged.

## Resume and correction procedure

After the human finishes Docker Desktop/WSL setup and Docker reports a running
engine: check 8090 is free (otherwise use one free TESTLINK_PORT consistently),
rerun setup, validate, load, report and audit for mhammedazad only. Adapt the
macOS Chrome launch externally on Windows. Verify actual B authorship, 41 cases,
14 requirements, 3 child suites, 135 steps, 83 active mappings, senior tester role,
Project 1 plan/build and zero claimed manual execution results. Use the existing
audit.py and compare actual active mappings with the declared mapping set.

Open both generated PDFs and both XML exports; render and inspect first/middle/last
PDF pages and all long fixture/step/requirement fields. For corrections, keep stable
case names and IDs and rerun the loader to update/resume, then regenerate and reaudit.
If any old case is renamed/removed, export/back up first and remove only that old B
case within this local B suite; never another tester's data. Record corrections here.

Commit only this member's module and qa/project1/mhammedazad deliverables/evidence.
Update the pull request with real exported PDFs/XML and actual audit counts, and
mark it ready after those checks succeed. Do not merge.

The local environment is preparation only. No lecturer-server project was created,
and no lecturer import or university submission occurred. The lecturer's slides
were not present in this workspace, so their physical review is not claimed; the
existing-project restriction is supplied by the task and repository instructions.
Import eventual exports into the lecturer's EXISTING assigned project, using its
existing roles and verified requirement mappings; do not create another project.
