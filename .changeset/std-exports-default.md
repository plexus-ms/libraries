---
"@plexus-ms/std": patch
---

The `exports` map names the compiled entry under `default` instead of `import`, so that a consumer that resolves the package through `require` (a script run with `tsx` in a CommonJS package, for one) finds it. With `import` alone such a consumer failed with `ERR_PACKAGE_PATH_NOT_EXPORTED`. ESM consumers resolve the same file as before.
