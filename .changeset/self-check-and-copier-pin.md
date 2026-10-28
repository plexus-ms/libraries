---
'@plexus-ms/lib': minor
'@plexus-ms/cli': minor
---

`ship` and `propagate` refuse to run behind the newest `@plexus-ms/cli` on the registry (asked with `npm view`; an unreachable registry only warns), and propagation runs copier through `mise exec copier@<version>` at the version plx pins (`COPIER_VERSION`, 9.19.1), so the copier a consumer is updated with travels with plx instead of depending on the operator's PATH.
