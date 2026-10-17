# Modeling and validation helpers

Keep small, reviewable scripts here as they are developed. This scaffold does not run Blender, install packages, launch renders or enable CI.

For each helper, document its purpose, Blender/runtime version, inputs and source hashes, units/coordinate frame, expected outputs, and how to validate the result. Prefer a dry-run mode where possible. Never silently overwrite a baseline, execute untrusted embedded scripts, fetch private data with stored credentials or start paid compute.

A modeling script needs the same evidence and still-review gate as a manual edit. Commit code through a task branch and PR. Put large output files in the existing authorized source-storage workflow and record their hashes in the task.
