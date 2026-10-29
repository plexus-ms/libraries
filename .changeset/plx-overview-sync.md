---
'@plexus-ms/lib': minor
'@plexus-ms/cli': minor
---

`plx overview -s`/`--sync` fetches every repo's remotes first (eight at a time) and marks each branch with the commits it is behind (`↓n`) and ahead of (`↑n`) its upstream; a fetch that fails shows as a problem on the repo. Off by default, since the fetches make a quick look slow.
