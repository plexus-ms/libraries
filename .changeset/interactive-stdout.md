---
"@plexus-ms/lib": patch
---

An interactive step's output (copier's, during `ship` and `propagate`) goes to stderr like every other narration; stdout stays the verb's result, so `--json` and pipes are not corrupted.
