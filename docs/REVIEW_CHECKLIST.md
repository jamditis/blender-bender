# Review checklist

Use this checklist with the [worker guide](./WORKER_GUIDE.md) and [rights guide](./RIGHTS_AND_REFERENCES.md). Record the output version and SHA-256 being reviewed. Use `pass`, `fail`, `not checked`, or `not applicable` with a reason; leave no ambiguous claim of completion.

## Scope and ownership

- [ ] The issue identifies one building or asset and the exact scope.
- [ ] The owner and current claim comment are linked, with a UTC checkpoint and exact input hashes, repository-relative paths, and public-safe private-asset aliases.
- [ ] No overlapping claim or simultaneous edit to the same `.blend` file is unresolved.
- [ ] Changes stay within the agreed scope. MSU campus fidelity remains the priority, all videos remain paused, and Pine Barrens work is excluded.

## Building identity and references

- [ ] The reviewer inspected the actual reference images and output stills.
- [ ] Visible features and site context support the building identity. Foreground and background buildings are distinguished.
- [ ] Conflicting filenames, captions, alt text, or metadata are resolved or explicitly marked uncertain.
- [ ] Important features are checked against suitable views. A single attractive camera angle does not stand in for whole-building review.
- [ ] Each source is traceable to a public source page or public-safe asset alias, version where relevant, and the exact claim it supports. Any private file mapping stays in the authorized private handoff.
- [ ] Dates and building changes are considered where references show different construction or renovation states.

## Geometry and dimensions

- [ ] Footprint, massing, roof form, height relationships, orientation, and characteristic facade features have been checked where the scope requires them.
- [ ] Important measurements list the source, source units, model units, model value, conversion if any, and comparison result.
- [ ] Coordinate frame, origin, axes, scale, source-to-scene transforms, and alignment with related assets are checked where relevant. Unknown registration is explicitly provisional.
- [ ] An agreed tolerance is recorded where available. Missing tolerances or missing measurements are disclosed.
- [ ] Measured, estimated, and unknown geometry are distinguished. No unsupported precision is claimed.
- [ ] Remaining discrepancies are described and visible in the evidence where practical.

Embedded metadata and good-looking renders can help explain a model, but neither establishes verified geometry.

## Files and dependencies

- [ ] Before editing, the worker checked the private current/version manifest for the canonical shared Google Drive store and verified the actual input bytes against the exact SHA-256 for the intended source version and status.
- [ ] Inputs and outputs have stable public-safe aliases, versions, repository-relative paths where applicable, and SHA-256 hashes computed from the actual files. Exact private paths remain in the private handoff.
- [ ] Dated source and output versions are preserved. The latest candidate is distinguished from the accepted integration baseline; neither file recency nor a new upload is treated as acceptance.
- [ ] The latest working model and required dependencies are maintained in the canonical private Drive store. The stored version and hash were verified, or the upload/verification gap is explicitly marked. A secondary Library delivery or backup is not reported as completing the shared Drive handoff.
- [ ] The delivered model was opened or otherwise checked in the stated software version. If this was not possible, the limit is explicit.
- [ ] Linked models, textures, fonts, add-ons, and other dependencies are listed as relevant. Missing files and untested dependencies are disclosed.
- [ ] The dependency check identifies which references are packed, linked, procedural, or unavailable; it does not treat packed content as rights-cleared.
- [ ] No `.blend` files, ZIP archives, raw LiDAR, heavy textures, or render caches are included in Git.
- [ ] No private storage IDs or links, local machine paths, account emails, credentials, tokens, signed download URLs, or unnecessary personal metadata appear in public commits, issues, pull requests, or review materials.

## Still evidence and rights

- [ ] A readable still contact sheet approved for public release labels the building, output version, view directions, and changes under review.
- [ ] Before/after views, whole-building views, and relevant details are included. Still images were visually inspected after export.
- [ ] Public source pages are linked or cataloged first. Copied reference images, textures, and reproduced materials have recorded permission or a license covering their intended use and any public release. Raw copyrighted reference images are not published.
- [ ] The evidence avoids identifiable people, minors, private spaces, and precise personal metadata. Any unresolved privacy or rights concern blocks that material's use.
- [ ] No video has been generated or submitted as part of this task.

## Review decision and handoff

- [ ] The pull request links the issue, claim comment, evidence, dimension checks, and exact output version.
- [ ] Public evidence links work. Intended reviewers' authorized access to the private Project and canonical Drive inputs is checked separately through private coordination, or explicitly marked unverified. No private links, IDs, or current/version manifest contents are exposed in the public handoff.
- [ ] Known uncertainty, blocked checks, dependencies, and the next action are clearly stated.
- [ ] The decision names the reviewed version and records acceptance, requested changes, or a blocker.
- [ ] Any promotion to the integration baseline has a recorded review decision naming the exact accepted version and SHA-256. The private current/version manifest is updated only to reflect verified file status and that decision; the previous dated baseline is preserved.
- [ ] Ownership is released or transferred through explicit coordination after editing stops; a passed timestamp is not treated as permission to take over.

Approval applies only to the stated change and reviewed version. It does not authorize video work, publication, deployment, spending, new access, or any unverified claim about repository protection settings.
