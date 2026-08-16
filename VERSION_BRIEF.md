---
type: version-brief
status: active
public_release: "Release 03"
historical_basis: "historical v4 (2026-08-14)"
updated: 2026-08-16
tags: [release, history, git, obsidian]
related:
  - "[[README]]"
  - "[[RELEASE_HISTORY]]"
  - "[[ARCHITECTURE]]"
---
# Version Brief — Release 03

## Release identity

**Project:** Reusable Research OS  
**Public release:** Release 03 — Scientific Lock and Re-verification  
**Historical basis:** historical v4 (2026-08-14)  
**Previous public release:** Release 02

## Plain-language summary

Release 03 is the scientific-falsification stage. The Research OS now requires a candidate to survive adversarial evidence review, dataset release/alignment checks, and a negative-result-safe experiment contract before it is treated as implementation-ready.

## Previous release summary

Release 02 added AI provenance, persistence, Git history, and benchmark-first validation while the thesis candidate was being narrowed.

## What changed

1. Added an adversarial evidence-lock procedure.
2. Added a dataset release, schema, correction, and alignment gate.
3. Added a negative-result contract so a thesis remains scientifically interpretable even when the proposed method does not improve the baseline.
4. Converted the README into a Git-facing project entry point.
5. Recorded graph-integrity evidence for the release.

## Why it changed

Primary-source re-verification found that some earlier claims were too broad, some dataset assumptions were release-specific, and the proposed method could not rely on novelty from graph reasoning alone. The workflow therefore needed formal falsification and data-provenance gates.

## What we were trying to learn

A defensible research question can survive even when method novelty is downgraded, provided the experiment is designed to distinguish the information contribution from the modeling contribution.

## Current understanding

The strongest research workflow is not one that protects an idea. It is one that records where the idea weakens, narrows the claim, and still produces an interpretable experiment.

## Remaining uncertainty

The system had not yet translated those gates into a resource-budgeted, large-file execution plan.

## Next direction

Convert the scientific lock into an executable pipeline with large-data compression, pre-paid-compute feasibility testing, and release-ready documentation.

## Historical continuity

This release is a **complete repository snapshot**, not a patch. Earlier notes remain present when they still explain the research journey. The public release numbering groups the original v1-v5 history into meaningful Git milestones without erasing the original version lineage.

## Preservation notes

All earlier evidence/scoring rules remain. The new gates are additions motivated by real corrections in the thesis project.

For the original v1-v5 lineage, see the project's version-history and migration notes as well as [[RELEASE_HISTORY]].
