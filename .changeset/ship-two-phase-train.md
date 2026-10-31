---
"@plexus-ms/cli": minor
"@plexus-ms/lib": minor
---

`ship` and `propagate` learn the consolidated layout (§ 1.5 PLX): the train repos are `primitives`, the three presets and the compendium, cut in two phases — `primitives` first, whose GitHub release locks its tag and publishes `@plexus-ms/{cli,lib,config}` at the train number, a wait until the registry has them, then the rest. Every train tag gets an immutable GitHub release, read back and refused when mutable. The bookkeeping gains the one-writer pins: the packages' manifests, the plx pin in `mise.toml`, the exact `@plexus-ms/config` pin, workflow refs and the collection source under `plexus-ms/primitives`. Propagation updates each consumer in a scratch clone of its origin and opens one pull request per consumer on `train/<version>`, reused on a re-run; the workspace checkouts are never touched. Against a workspace without `primitives` the verbs fail before any write.
