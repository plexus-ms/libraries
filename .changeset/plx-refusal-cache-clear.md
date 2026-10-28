---
'@plexus-ms/lib': patch
'@plexus-ms/cli': patch
---

The refusal of a `plx` behind its newest release names the update as `mise cache clear npm:@plexus-ms/cli && mise up npm:@plexus-ms/cli` again, scoped to the one tool: mise caches a tool's version list as well as holding back young releases, and the 0.8.0 release showed `mise up` answering "up to date" from that cache minutes after the publish.
