---
type: artifact-protocol
status: active
created: 2026-08-14
updated: 2026-08-14
tags: [git, release, readme, reproducibility]
related:
  - "[[REQUIRED_ARTIFACTS]]"
  - "[[../10_change_log/VERSIONING_AND_GIT]]"
  - "[[../08_quality_gates/DATASET_RELEASE_AND_ALIGNMENT_GATE]]"
---
# Git-Ready Research Release

Every research release should be understandable without opening Obsidian first.

## README contract
A repository README should contain:
1. Project Overview
2. Features
3. Tech Stack with roles
4. Architecture diagram
5. Project Structure

## Research-specific additions
- version/release status
- evidence boundary
- known limitations
- link to version history
- no secrets or private credentials
- large raw data excluded from Git

## Release checks
1. Internal Obsidian links resolve.
2. No unexpected orphan notes except intentionally top-level README/navigation files.
3. Historical versions remain immutable.
4. Generated hashes are refreshed.
5. Large datasets, model weights, caches, and temporary media are ignored by Git.
6. Exact external dataset revisions live in manifests, not in README prose only.
