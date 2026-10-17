# Storage, cost and access

## Canonical shared model store

Google Drive is the canonical shared model store for authorized worker use. Maintain the latest working models and their required dependencies in owner-controlled private Drive storage. Library is secondary delivery or backup; it does not replace the shared Drive source or establish that a Drive handoff is complete.

Keep text, scripts, public-safe catalog records and review decisions in Git. Keep `.blend` files, ZIP packages, source photographs, LiDAR, large textures and renders outside Git. Publish only public-safe asset aliases, version names, byte sizes, SHA-256 hashes and status. Keep private file IDs, share links, machine paths and the private current/version manifest in authorized private storage. Never store credentials, tokens or signed download URLs in the repository or handoff records.

## Check the version before editing

1. Read the private current/version manifest. It must identify each asset's dated versions, exact SHA-256 hashes, private source locations, and status.
2. Identify the source version required by the task. Distinguish the latest candidate from the accepted integration baseline; a task may deliberately use the accepted baseline rather than the newest candidate.
3. Read the intended Drive file and verify the actual bytes against the manifest's exact SHA-256 before editing. A matching filename, date, or Library copy alone is insufficient.
4. If the manifest, file, or hash is missing or inconsistent, stop dependent edits and report the gap using the public-safe asset alias. Resolve the private location or access issue through authorized private coordination.

## Preserve versions and record acceptance

Give each new binary revision a distinguishable dated version, source hash and change log. Preserve source files, previous outputs and previous accepted baselines; do not overwrite the only copy of a dated version.

Keep two statuses clear in the private current/version manifest:

- **Latest candidate:** the most recent verified working output available for review. It may contain unresolved geometry, dependency or integration problems.
- **Accepted integration baseline:** the exact version approved for shared integration after review. Record the acceptance decision and its SHA-256.

Do not promote a candidate merely because it is newer, has been uploaded, or looks better. A promotion requires a recorded review decision for the exact version and hash. Update the private manifest to reflect verified storage status and that decision while retaining the prior dated baseline. A material study or partial building variant does not become the full-campus master through recency.

## Verify storage and access separately

After an authorized Drive upload, check the stored version and exact SHA-256 before reporting it verified. This guide does not assert that any upload has occurred or passed that check. A local save, upload attempt, or Library delivery alone does not establish the shared Drive file's status.

Check each intended worker's authorized access separately through private coordination. Your own successful read, a repository invitation, or the existence of a link does not prove another worker can open the file. Report access as unverified when evidence is missing, and do not change permissions as an implied part of storage work.

## Why no Git LFS at setup

GitHub warns for ordinary Git files over 50 MiB and blocks files over 100 MiB; browser uploads are limited to 25 MiB. GitHub recommends small repositories, ideally below 1 GB and strongly below 5 GB. [Official large-file documentation](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github)

LFS can handle larger files, but changed files are stored as a new full version; collaborator and automation downloads consume the repository owner's bandwidth. GitHub Free and Pro currently include 10 GiB storage and 10 GiB download bandwidth, shared at account level. LFS use beyond included amounts can incur charges or be blocked depending on the account's budget/payment settings. [Official LFS billing](https://docs.github.com/en/billing/concepts/product-billing/git-lfs)

The GitHub calculator currently lists additional LFS storage at $0.07 per GiB-month and outbound transfer at $0.0875 per GiB. These are published rates checked October 17, 2026, not a spending authorization or a forecast. Recheck before choosing LFS. [Official pricing calculator](https://github.com/pricing/calculator)

With frequently changing Blender binaries, source storage plus checksummed manifests is a simpler starting point. No LFS setup, paid service, CI render workflow or billing change was made.

## Separate permissions

- A private personal-account repository has an owner and collaborators; collaborators have write access, not a read-only role. An organization supports finer-grained roles. [GitHub permission documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/repository-access-and-collaboration/permission-levels-for-a-personal-account-repository)
- Project visibility/access is separate from repository access.
- A Drive or Library link does not grant the reader permission to the source file. Verify the intended person's authorized access before a handoff.
- Removing access does not erase local copies already downloaded.
- Access to a private repository is not permission to publish, license, deploy, spend money or contact an outside agent.

## Review enforcement

The repository uses a documented PR-review convention. Do not assume protection is enforced. GitHub documents protected branches for public repositories on Free plans; private repositories require Pro, Team or Enterprise. The setup did not change any protection rule or purchase an upgrade. [Official branch-protection documentation](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches)
