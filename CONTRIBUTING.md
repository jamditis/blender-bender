# Contributing to blender-bender

Start with the [README](./README.md), then follow the [worker guide](./docs/WORKER_GUIDE.md).

## Current scope

- Prioritize recognizable, evidence-backed Montclair State University campus locations.
- All video work is paused. Submit still images for review.
- Pine Barrens work is outside this repository's current scope.
- Work on the building or asset named in the issue. Ask before expanding that scope.

## Before editing

1. Read the issue, its latest comments, and related pull requests. Check for an existing claim and dependencies.
2. Verify access separately to the public repository, any private GitHub Project, and owner-controlled private source storage. Public repository access does not grant access to the Project or working binaries.
3. Inspect the actual references. Confirm the intended building visually, including which structures are in the foreground and background. Captions, filenames, alt text, and embedded metadata are leads, not sufficient proof.
4. Confirm the exact source-file versions and their SHA-256 hashes. If an input is missing or cannot be verified, report that gap before editing it.
5. Post your own claim comment using the [worker guide](./docs/WORKER_GUIDE.md#claim-comment). Re-read the issue after posting to catch overlapping claims. GitHub comments do not provide an atomic lock.

Keep one active claim per building or asset. A claim names its owner, exact scope, source hashes, editable paths, and next checkpoint or expiration in UTC. Do not claim work on behalf of another person or assign other people. If a claim appears stale, coordinate with its owner or the human project lead before taking over. A passed timestamp does not release the work.

## Work and storage

- Use a separate branch for each task, tied to its issue. Open a draft pull request when the change is ready for review.
- Never edit the same `.blend` file concurrently. Agree on a handoff or divide work into separate files before work begins.
- Keep `.blend` files, ZIP archives, raw LiDAR, heavy textures, and render caches in owner-controlled private storage. Git holds public-safe catalog records, checksums, scripts, documentation, and small review stills approved for public release.
- Public records use stable asset aliases, versions, SHA-256 hashes, and repository-relative paths. Keep the alias-to-private-file mapping in an owner-controlled private handoff. Never commit private storage IDs or links, local machine paths, account emails, credentials, tokens, or signed download URLs.
- Check [rights and references](./docs/RIGHTS_AND_REFERENCES.md) before copying images or turning them into textures. A public repository does not grant rights to its source material.

The `.gitignore` file is a safeguard, not a complete content or rights check. Review the actual files being committed. Ignoring a file does not remove a file that Git already tracks.

## Review and handoff

Use the [review checklist](./docs/REVIEW_CHECKLIST.md) and pull request template. Include:

- Issue and claim links, the exact work completed, and remaining questions
- Public-safe input and output asset aliases, versions, repository-relative paths, and SHA-256 hashes
- Building identity evidence, dimension checks against named sources, and coordinate/registration checks
- A still contact sheet approved for public release, with labeled before/after views and permitted reference comparisons
- Dependency and missing-file checks for the delivered model
- Known uncertainty, any estimated geometry, and a clear handoff

Good-looking renders and embedded metadata alone do not verify geometry. A review must distinguish measured dimensions, visual estimates, and unknowns.

Record the review or agreed handoff decision and exact output version before releasing the claim. A pull request does not authorize publication, deployment, spending, new access, or a change to the current video pause. Repository settings and branch protection must be checked directly; these guides do not establish them.
