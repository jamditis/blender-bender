# Storage, cost and access

## Default storage choice

Keep text, scripts, manifests and review decisions in Git. Keep `.blend` files, ZIP packages, source photographs, LiDAR, large textures and renders in existing authorized Drive or Library storage. Publish only an asset alias, filename, byte size, SHA-256 and status. Keep private file IDs and share links in an authorized private handoff. Never store a signed download URL or token.

Each new binary revision should be a named output with a source hash and change log. Do not overwrite the preserved source or pretend a material study is the full-campus master. GitHub is not the only backup.

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
