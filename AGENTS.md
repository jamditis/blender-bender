# Collaboration instructions

Read README.md, CONTRIBUTING.md and the current task issue before working. MSU campus fidelity is the priority. All videos are paused, review stills only, and Pine Barrens is excluded.

Claim a precise scope in the issue with identity, source hash, paths and next UTC checkpoint; then re-read for conflicts. This is a human coordination convention, not an atomic lock. Do not edit the same binary concurrently or take over a stale claim without coordination. Do not assign other people or imply they accepted work.

Google Drive is the canonical shared model store for worker use. Keep the latest working models and their required dependencies there, in owner-controlled private storage. Library is secondary delivery or backup, not a replacement for the shared Drive source. Before editing, read the private current/version manifest, identify the source version and its status, and verify the actual input bytes against its exact SHA-256. If the manifest, file, or hash cannot be verified, stop dependent edits and report the gap.

Preserve source files and dated versions. Keep the latest candidate distinct from the accepted integration baseline; a newer timestamp or upload does not promote a model. Record the review decision and exact accepted version/hash before changing the baseline. Keep Blender binaries, ZIPs, raw datasets, heavy textures, render caches and large review images outside Git. Never commit private source links or IDs, machine paths, credentials, tokens or signed download URLs.

Treat storage and access as separate checks. Do not claim a Drive upload or another worker's access is verified without evidence. Keep the private manifest and source-location mapping out of this public repository.

Use a branch and PR per bounded change. Include verified source identity, provenance/rights, dimensions and coordinate checks, before/after stills, missing-dependency checks, output hashes and explicit uncertainty. Unknown geometry stays provisional. Attractive rendering is not evidence of location accuracy.

Use issue #1 for concise progress/handoffs and specific task issues for technical detail. The repository and Project do not grant outside-agent contact, access changes, publishing, deployment or spending permission. Respect separate repository, Project and source-file access.
