---
'@plexus-ms/lib': patch
'@plexus-ms/cli': patch
---

The refusal of a `plx` behind its newest release names the update as `mise up npm:@plexus-ms/cli` alone: what held a fresh release back was mise's minimum release age, not its cache, so the `mise cache clear` it suggested first was never needed.
