---
"@plexus-ms/config": patch
---

Keep Biome's formatter off YAML files.
Biome 2.6 formats YAML by default, which rewrites `pnpm-lock.yaml` and strips aligned comments in workflows and compose files.
The shared config disables it through an `overrides` entry, which Biome 2.5 understands too, so consumers on either version keep passing.
The `$schema` pin is dropped from the shared config: a consumer's root `biome.json` carries the schema matching its own Biome version, and a pin here only produced version-mismatch notices.
