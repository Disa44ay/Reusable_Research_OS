---
type: correction-note
status: resolved
verified: 2026-09-10
---

# V01 Context File Anomaly — Root Cause and Correction

## The anomaly (as originally flagged)

`Reusable_Research_OS_V01_Context.txt`'s embedded `VERSION_BRIEF.md`
extract was byte-identical to `Reusable_Research_OS_V04_Context.txt`'s,
both showing `public_release: "Release 04"`, despite the file being
labeled Release 01.

## Root cause (confirmed)

The local working folder `Reusable_Research_OS/Release_01/Reusable_Research_OS/`
is a live Git checkout, not a static per-release snapshot. At the time
the context extraction ran, it was sitting at HEAD (the Release 04
state) regardless of the folder's Release-01 name. Same mechanism as
the identical issue found in the companion Thesis Research Project.

## Correct Release 01 content (recovered via `git show 8b9eb4c:VERSION_BRIEF.md`)

```
public_release: "Release 01"
historical_basis: "historical v1-v2 period, endpoint v2 (2026-08-10)"
```

Previous public release: None. The recovered file's title is "Version
Brief - Release 01"; it summarizes the original vault split and
reorganization into a graph-native Obsidian workflow.

## What this means for this repository

Nothing in Release 04 or Release 05 was built on the corrupted V01
extract. This anomaly affected only the standalone
`Reusable_Research_OS_V01_Context.txt` reference file, not any release
package. Documented here so it doesn't need rediscovering, and as a
process note: future context-file regeneration from local Git history
should pin the exact commit per release rather than reading whatever a
live checkout happens to be at.

------------------------------------------------------------------------
