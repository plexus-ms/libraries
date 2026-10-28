---
'@plexus-ms/lib': minor
'@plexus-ms/cli': minor
---

Add `deploy`, the last ops verb that `ci-cd` carried as bash: render the app's compose file with the image pinned, stage it on the host, pull, migrate, swap, up, poll readiness, roll back on failure. Every command sent to the host is one line of shell over a shared ssh connection, carried in the plan and printed verbatim by `--dry-run`; the heredoc `ssh` step of the plan model is gone with the script it served.
