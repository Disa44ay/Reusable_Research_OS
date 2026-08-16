---
type: versioning-policy
status: active
created: 2026-08-12
updated: 2026-08-12
tags: [git, versioning, snapshots]
related:
  - "[[00_governance/MEMORY_AND_PERSISTENCE_POLICY]]"
  - "[[10_change_log/CHANGELOG]]"
---
# Versioning and Git

## Recommended repository structure
Keep the actual unzipped vault folders in Git so Markdown diffs remain visible.

1. `Reusable_Research_OS/`
2. `Thesis_Research_Project/`

## Version strategy
1. Use commits for normal research sessions.
2. Use tags for milestones such as `topic-search-v1`, `topic-locked-v1`, `baseline-v1`, and `submission-v1`.
3. Use ZIP archives as immutable backup snapshots, not as the only Git-tracked artifact.
4. Preserve historical snapshots. Never rewrite old versions to make them look cleaner.
5. Ignore volatile Obsidian workspace state when it causes noisy diffs.
6. Keep stable Obsidian configuration only when it improves portability.

## Audit rule
Before publishing a snapshot, run an internal-link check and regenerate integrity hashes.
