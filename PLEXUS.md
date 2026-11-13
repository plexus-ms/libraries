---
plexus: 0.120.0
modules: [PLX-Repo, PLX-JS, PLX-Delivery, PLX-Updates]
---

- The `@plexus-ms/*` libraries: tenant-neutral methodology for the web/Node/TypeScript world on its own semver, versioned by changesets and published through trusted publishing (§ 5 PLX-Delivery); `plx` and `@plexus-ms/lib` live in `tooling` and carry the Plexus version (§ 1.5 PLX).
  The libraries do not carry the Plexus version (§ 1.5 PLX): `plexus` above is the version this repo's arrangement was last brought up to, not a version of the libraries.
- A consumer of `template-repo-turbo` with `publishes_packages`, like a tenant's web repo: the arrangement arrives by the pull request that takes a Plexus version and is not hand-maintained.
- `@plexus-ms/config` is a workspace package here, not a catalog entry (Maintaining, PLX-JS): this repo is where it comes from, so the root manifest says `workspace:*` where the template says `catalog:plexus`.
