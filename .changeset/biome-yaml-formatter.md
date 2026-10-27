---
"@plexus-ms/config": patch
---

Keep Biome's formatter off YAML and Markdown files.
Biome 2.6 formats both by default: it rewrites `pnpm-lock.yaml`, strips aligned comments in workflows and compose files, and turns the frontmatter of a changeset or a `PLEXUS.md` marker into a heading.
The shared config disables it through an `overrides` entry, which Biome 2.5 understands too, so consumers on either version keep passing.
The `$schema` pin is dropped from the shared config: a consumer's root `biome.json` carries the schema matching its own Biome version, and a pin here only produced version-mismatch notices.
