# Worker guide

This guide covers one building or asset from intake through handoff. Read the [README](../README.md) and [contributing guide](../CONTRIBUTING.md) first.

The priority is MSU campus location fidelity. All video work is paused; review uses stills only. Pine Barrens work is out of scope.

## 1. Read the task and inspect the inputs

- Read the issue and all recent comments immediately before claiming work. Check linked pull requests, related assets, and the current owner.
- Identify the exact building, the part being changed, and what is outside the task.
- Open the actual reference images. Confirm the intended building from visible features and its surroundings. Separate foreground subjects from background buildings. Resolve conflicting labels before relying on them.
- Record each input's public-safe asset alias, version, and SHA-256 hash. Keep its private storage identity and exact working path in an owner-controlled private handoff. Hash the actual bytes you will use. A filename alone does not identify a version.
- Check access to the repository, private Project, and private source storage independently. The public repository grants no access to the others. If an input is inaccessible, report its public-safe asset alias and continue only work that does not depend on it.

Use the [reference guide](./RIGHTS_AND_REFERENCES.md) for source records and permissions. Never put private storage IDs or links, local machine paths, account emails, credentials, tokens, or signed download URLs in public issues, pull requests, or commits. Keep private access details in owner-controlled private coordination; never share credentials or signed download URLs as a handoff.

## 2. Claim the work

Keep one active claim per building or asset. Post a comment under your own identity before changing files. For a multi-building task, split the work into separate issues or explicitly separated asset claims.

### Claim comment

Copy this into the issue and replace every placeholder:

```text
Claim: proposed / active / blocked / ready for review / released
Owner: <your public-safe worker identity and authorized GitHub handle>
Building or asset: <one exact building or asset>
Scope: <specific geometry, references, or files being changed>
Out of scope: <nearby or related work excluded from this claim>
Task branch: <branch name>
Source files and versions: <public-safe asset aliases and version identifiers>
Source SHA-256: <one full hash per input, mapped to its file/version>
Editable paths: <exact repository-relative paths and private asset aliases; no private paths>
Dependencies: <issues, assets, or decisions needed; otherwise none>
Next checkpoint or expiration: <YYYY-MM-DDTHH:MM:SSZ>
Handoff contact: <public-safe owner or project-lead handle; no account email>
```

The public asset alias must map unambiguously to the exact private file in the owner-controlled handoff record. Share that mapping only through authorized private coordination.

Use UTC with a `Z` suffix. An expiration is a request to check the claim's status, not permission for someone else to take the work. If the source file is unavailable or its hash is unknown, mark the claim blocked and explain the missing input; do not present an unverified hash as complete.

Re-read the issue immediately after posting. GitHub comments are not an atomic lock: two workers can post at nearly the same time. If claims overlap, stop the overlapping work and coordinate with the other owner or the human project lead. Do not resolve a conflict by editing first.

Do not assign another person or take over because a checkpoint passed. A handoff needs explicit coordination and an agreed source version. Record that agreement in the issue before the next owner edits.

## 3. Make a bounded change

- Use one branch per task. Include the issue number and a short description in its name where practical.
- Work only within the claimed scope. Post an updated scope and coordinate any overlap before widening it.
- Never edit the same `.blend` file simultaneously with another worker. Separate files can be worked on in parallel only when their boundaries and integration owner are agreed.
- Keep `.blend` files, archives, raw LiDAR, heavy textures, and caches in owner-controlled private storage. Update only public-safe catalog aliases, versions, and checksums in Git.
- Preserve the source version. Give a changed output a distinguishable version and record its SHA-256 hash; do not silently replace the input another worker is using.
- Record modeling software versions and linked dependencies needed to open the output. Flag missing tools or add-ons without installing or buying them as an implied part of the task.

For each important dimension, record the source, source units, model units, model value, any conversion, and the result of the comparison. Use an agreed tolerance where one exists. If no tolerance or trustworthy measurement exists, state that clearly and ask for the review decision needed. Do not present a guessed dimension as surveyed or measured.

Record the coordinate frame, origin, axes, scale, and any source-to-scene transform needed to place the asset. Check alignment with related assets before integration. If registration is unknown, mark it provisional and avoid a claim of geographic accuracy.

Prioritize the building's silhouette, massing, roof form, height relationships, footprint, and characteristic facade features. Cosmetic work should not hide unresolved identity or geometry questions.

## 4. Prepare still evidence

Create a compact, labeled contact sheet approved for public release, showing the changed asset from useful still views. Include the building name, output version, view direction, and the feature being checked. Show before/after views, the whole building, and details affected by the task. Include copied reference comparisons only where public reproduction is permitted. Otherwise link a public source page and identify the relevant view or feature. Never publish raw copyrighted reference images or a private source link.

Inspect the actual exported images at a readable size. Check framing, scale, orientation, missing materials, and whether the evidence supports the claimed result. Neither a polished render nor a metadata field establishes geometry accuracy.

Do not render, assemble, or submit video while the pause remains in place.

## 5. Open a draft pull request and hand off

Use the pull request template and [review checklist](./REVIEW_CHECKLIST.md). Link the issue and claim comment. Include exact input/output versions and hashes, dimension results, still evidence, dependency checks, uncertainty, and the next action needed.

Check public evidence links and confirm authorized reviewers can access any private inputs through the separate private handoff. If access is missing, report the blocker without exposing the private link; do not grant permissions or promise access on someone else's behalf. Repository, Project, and source-storage permissions are separate.

At each checkpoint, post a brief issue update with what changed, the current output version, any blocker, and the next UTC checkpoint. When handing off, record:

- The accepted or review-ready output's public-safe alias, version, repository-relative path where relevant, and SHA-256
- The matching branch/commit and pull request
- Checks completed, checks blocked, and known uncertainty
- Whether the `.blend` file identified by its asset alias is still being edited
- The next owner only after they have agreed, plus the next action

Release the claim after the agreed review or handoff is recorded and editing has stopped. A timeout alone never transfers ownership. Merge, publication, deployment, access changes, and spending remain separate decisions.
