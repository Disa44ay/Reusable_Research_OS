---
type: version-brief
status: active
public_release: "Release 02"
historical_basis: "historical v3 (2026-08-12)"
updated: 2026-08-16
tags: [release, history, git, obsidian]
related:
  - "[[README]]"
  - "[[RELEASE_HISTORY]]"
  - "[[ARCHITECTURE]]"
---
# Version Brief — Release 02

## Release identity

**Project:** Reusable Research OS  
**Public release:** Release 02 — Evidence-Driven Candidate Validation  
**Historical basis:** historical v3 (2026-08-12)  
**Previous public release:** Release 01

## Plain-language summary

Release 02 shows the Research OS being used under a real thesis deadline. The system expanded from static workflow documentation into an evidence-orchestration process that records external-AI roles, prompt provenance, memory/persistence boundaries, benchmark-first validation, and Git/versioning practices.

## Previous release summary

Release 01 established the reusable workflow, graph-native knowledge structure, evidence protocol, scoring rules, and stage contracts.

## What changed

1. Added memory and persistence policy.
2. Added AI helper registry and quota-aware external-AI protocol.
3. Added prompt-run provenance so AI outputs can be audited and corrected.
4. Added Git/snapshot versioning guidance.
5. Strengthened benchmark-first validation and fast-deadline decision flow.
6. Added reusable resource-aware thinking around one-time preprocessing and compact model-ready features.

## Why it changed

The football thesis search began using Gemini, Claude, Perplexity and direct dataset inspection in parallel. That exposed the need to preserve not only conclusions but also which assistant produced them, which claims were corrected, and which evidence was primary.

## What we were trying to learn

How to coordinate multiple research assistants without treating any assistant as authoritative, and how to preserve the path from broad discovery to an evidence-backed candidate.

## Current understanding

AI helpers are useful as scoped scouts and reviewers, but final claims must be controlled by primary evidence and explicit correction provenance. The operating system also needs durable research snapshots because conversation context alone is insufficient.

## Remaining uncertainty

The workflow had not yet faced a final hostile novelty review or dataset-release mismatch serious enough to require formal alignment gates.

## Next direction

Run a final adversarial evidence lock on the strongest thesis candidate and formalize dataset-version, alignment, and negative-result gates.

## Historical continuity

This release is a **complete repository snapshot**, not a patch. Earlier notes remain present when they still explain the research journey. The public release numbering groups the original v1-v5 history into meaningful Git milestones without erasing the original version lineage.

## Preservation notes

Release 01 rules remain present. New AI/persistence rules extend them rather than replacing the original evidence and stage-contract system.

For the original v1-v5 lineage, see the project's version-history and migration notes as well as [[RELEASE_HISTORY]].
