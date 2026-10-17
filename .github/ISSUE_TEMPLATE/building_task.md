---
name: Building or asset task
about: Define one MSU building or asset change with evidence and a clear handoff.
title: "[Building] <building or asset>: <bounded change>"
labels: ''
assignees: ''
---

## Building or asset

Name one exact building or asset. Include the relevant catalog record or README section.

## Requested result

Describe the change and how a reviewer can tell it is complete.

## Scope and boundaries

- Included:
- Excluded:
- Repository paths expected to change:
- Private model or asset aliases (no storage IDs, links, or machine paths):

MSU campus location fidelity is the priority. All videos are paused; still reviews only. Pine Barrens work is excluded.

## Inputs and evidence

- Stable public reference-page links and the features they support:
- Visual building identity check, including foreground/background distinction:
- Public-safe source asset aliases, versions, and repository-relative paths:
- SHA-256 for each input file, or the exact missing input blocking work:
- Measurements, source units, and any agreed tolerances:
- Coordinate frame, registration, and alignment dependencies:
- Rights or access questions:

Link and catalog public source pages first. Public visibility does not grant reproduction, texture, or publication rights. Keep working binaries and source archives in owner-controlled private storage. This public repository does not grant access to those files or the private Project. Never include private storage IDs or links, local machine paths, account emails, credentials, tokens, signed download URLs, or raw copyrighted images in this issue.

## Dependencies

List related issues, assets, or decisions. Note any other work touching the same `.blend` file.

## Acceptance checks

- [ ] Building identity is supported by inspected visual evidence.
- [ ] Relevant dimensions and major features are checked against named sources.
- [ ] Estimates, unknowns, and missing checks are disclosed.
- [ ] A labeled still contact sheet approved for public release and a dependency check are supplied.
- [ ] Public-safe output aliases, versions, repository-relative paths, and exact SHA-256 hashes are recorded.
- [ ] A pull request links the evidence and includes a clear handoff.

Use `docs/REVIEW_CHECKLIST.md` in this repository for the full review.

## Ownership

Creating this issue does not claim it or assign anyone. Immediately before starting, re-read the issue and its recent comments, then post your own claim using the Claim comment section of `docs/WORKER_GUIDE.md`. Include the owner, exact scope, source hashes, repository-relative paths and private asset aliases, and next checkpoint or expiration in UTC. Re-read after posting to detect conflicts.

Keep one active claim per building or asset. GitHub comments are not an atomic lock. Never edit the same `.blend` file simultaneously, assign another person, or take over on timeout. Coordinate explicitly with the owner or human project lead before a handoff.
