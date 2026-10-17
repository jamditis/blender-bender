# Blender Bender

A public coordination workspace for building accurate, evidence-backed New Jersey locations in Blender. The immediate priority is the **Montclair State University campus**. This repository makes it easy for a person or an authorized worker to find the current source, choose a bounded task, and show what changed.

**All video work is paused. Review stills only. Pine Barrens is excluded.** Other locations are future backlog, not active assignments.

## Start here

1. Read the [shared progress ledger](https://github.com/jamditis/blender-bender/issues/1) for current direction and handoffs.
2. Open the [private project board](https://github.com/users/jamditis/projects/37) or the [task index](PROJECT_BOARD.md).
3. Read [how to contribute](CONTRIBUTING.md), obtain the private Google Drive current/version manifest through authorized coordination, and verify the exact downloaded source hash. The public [asset manifest](manifests/source-assets.json) identifies the preserved original snapshot; it is not a live pointer to the newest working model. Check the [reference catalog](references/README.md).
4. Claim one precise scope in its issue before changing a binary. Read the issue again to catch conflicting claims.
5. Submit a branch and pull request with evidence, before/after stills, dependency checks, hashes and remaining uncertainty. Use the [review checklist](docs/REVIEW_CHECKLIST.md).

No one is pre-assigned. A claim is a shared coordination convention, not an atomic file lock. Do not edit the same `.blend` file concurrently.

## What belongs where

| In this repository | In the owner-controlled Google Drive model store |
| --- | --- |
| Blender scripts and small configuration files | `.blend` files and binary working variants |
| Reference catalog, provenance and rights notes | Original photographs, large textures and source archives |
| Source/output hashes and public-safe asset aliases | Raw LiDAR, caches, heavy exports and renders |
| Building issues, decisions, PRs and review notes | Large review-still packages shared through authorized private handoff |

**Google Drive is the canonical shared model store.** Keep the latest working models, their private current/version manifest, dependencies and dated prior versions there. GitHub holds coordination and public-safe evidence records. Library copies are secondary delivery or backup copies, not the shared source of truth.

Before editing, read the current Drive manifest and verify the downloaded file's SHA-256 against its exact version. Preserve a dated version before advancing any current pointer. Record separate pointers/statuses for the latest **candidate** and the **accepted integration version**: a newer upload is not automatic approval or permission to replace the accepted baseline. If a manifest or access check is missing, report that gap rather than guessing from a filename or modification date.

Never commit private storage links or IDs, machine paths, signed download URLs, credentials or access tokens. Upload success and access for another worker are separate checks; do not claim either without evidence.

## Current baseline

The preserved October 16, 2026 Drive snapshot contains 654 extracted files, approximately 538 MB, distributed as four ZIP packages. The October 17 audit opened the main and north scenes in Blender 4.5.14 LTS with script auto-execution disabled. Main contains 4,081 objects; north contains 3,370. Counts describe the inspected files, not completeness or accuracy.

- Canonical source archives remain in owner-controlled private Google Drive storage. Request an authorized handoff to its current/version manifest; no access locators are published here.
- [Verified archive and scene hashes](manifests/source-assets.json)
- [Baseline limitations and building inventory](docs/BASELINE.md)
- [Artifact register](manifests/artifact-register.json)

The older Library campus v19 is stale. The separate Sprague study is a noncanonical material/motion test, not a full-campus master. Main and north include overlapping representations; do not merge them blindly.

## What counts as an improvement

A successful correction has the right building identity, source-to-model dimension checks, consistent units and registration, a preserved baseline, no unexplained missing dependencies, and a readable record of uncertainty. Use plan, section, oblique and eye-level stills when relevant. Better lighting or more detail does not establish geographic accuracy.

Official drawings can support measurements; photographs can support appearance and relative relationships. Neither should silently become a survey claim. Existing embedded metadata is provenance to investigate, not a recovered measurement receipt.

## Repository map

- `PROJECT_BOARD.md`: human-readable task index and status definitions
- `CONTRIBUTING.md` and `docs/WORKER_GUIDE.md`: claims, branches, handoffs and collaboration
- `docs/REVIEW_CHECKLIST.md`: acceptance criteria
- `docs/RIGHTS_AND_REFERENCES.md`: reference, privacy and rights handling
- `docs/BASELINE.md`: inspected source, limits and current building scope
- `docs/STORAGE_AND_ACCESS.md`: Git/Git LFS tradeoffs and separate access boundaries
- `references/`: reviewed reference index, source identity, dates and rights status
- `manifests/`: public-safe asset aliases, hashes and artifact status
- `scripts/`: documented, reviewable modeling/validation helpers as they are added
- `.github/`: task, reference-gap and pull-request templates

## Access and review

The repository is prepared for public collaboration. The Project and working source archives remain private; access to them is separate. Public repository visibility does not invite collaborators, authorize outside agents, grant private-source access, publish model assets, deploy anything or commit spending.

Use pull-request review by agreement. Do not assume branch-protection enforcement is enabled: GitHub offers protection for public repositories on Free plans, but no protection rule or plan change was part of this setup. No open-source license has been selected; third-party reference rights remain source-specific.
