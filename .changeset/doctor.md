---
"@plexus-ms/lib": minor
"@plexus-ms/cli": minor
---

Add `plx doctor [dir]`, the staleness check of § 13.4 PLX that replaces the toolbox's `staleness.sh`: every marker under a directory is checked against the compendium's modules for requirements that changed since and dependencies not declared where § 1.4 says they are satisfied. In lib: `readCatalog` and `parseModule` for module pages, the pure `diagnose`, and a `git: false` scan option.
