---
"@plexus-ms/lib": minor
"@plexus-ms/cli": minor
---

`plx ship`, `plx propagate` and `plx requirements`: the release train and the compendium's requirements check move from bash into plx.

- `ship` tags every train repo identically after writing the train bookkeeping (galaxy version, the preset's collection pin, workflow refs, the map's version and timestamp, `changed` on every standard module whose requirements moved), then propagates.
- `propagate` copier-updates every consumer in the workspace on its expected branch, syncs markers, refreshes lockfiles and pins the consumers' ci-cd workflow refs; `-n` previews in scratch clones.
- `requirements` lints the standard's map and module pages and extracts a module's requirement lines, replacing the compendium's `requirements.sh`.
- lib: `Context.stage` performs a step on scratch state in every mode; `run` steps can be `interactive`; line-based frontmatter edits; the train, consumer and bookkeeping readers behind the verbs.
- `plx` exits 2 on a mistake in the arguments.
