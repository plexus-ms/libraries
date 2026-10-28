---
'@plexus-ms/cli': minor
'@plexus-ms/lib': minor
---

`plx changeset`: the changeset a dependency bump owes. On an update bot's branch it diffs every workspace package's `dependencies`, `optionalDependencies` and `peerDependencies` against the merge base, catalog entries included, and writes one deterministic `.changeset/bot-<branch>.md`: a patch per package whose runtime dependencies moved, a major when a peer range did; devDependencies, private and ignored packages owe nothing, and a stale file from an earlier run is removed. In lib: `readChangeset`, the pure `planChangeset`, `parseCatalogs` and `workspaceGlobs`.

The cli now declares what it inlines, `@plexus-ms/lib`, `commander` and `@inquirer/prompts`, as dependencies rather than devDependencies: a release of theirs has to release the cli that carries them, which changesets and `plx changeset` do for a declared dependency, and the redundant install is small. The published 0.3.0 bundle had missed lib 0.3.1's fix that keeps stdout clean during interactive steps; this release carries it.
