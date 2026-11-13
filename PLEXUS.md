---
plexus: 0.120.0
modules: [PLX-Repo, PLX-JS, PLX-Delivery, PLX-Updates]
---

- The `@plexus-ms/*` libraries: tenant-neutral methodology for the web/Node/TypeScript world on its own semver, versioned by changesets and published through trusted publishing (§ 5 PLX-Delivery); `plx` and `@plexus-ms/lib` live in `primitives` and ride the train (§ 1.6 PLX).
  The repo rides outside the train (§ 1.5 PLX): `plexus` above is the train its arrangement was last brought up to, not a version of the libraries.
- A consumer of `preset-repo-web` with `publishes_packages`, like a tenant's web repo: the arrangement arrives by the train's pull request and is not hand-maintained.
- `@plexus-ms/config` is a workspace package here, not a catalog entry (§ 1 PLX-JS): this repo is where it comes from, so the root manifest says `workspace:*` where the template says `catalog:plexus`.
