---
type: version-brief
status: active
public_release: "Release 04"
historical_basis: "historical v5 plus verified post-v5 work through 2026-08-16"
updated: 2026-08-16
tags: [release, history, git, obsidian]
related:
  - "[[README]]"
  - "[[RELEASE_HISTORY]]"
  - "[[ARCHITECTURE]]"
---
# Version Brief — Release 04

## Release identity

**Project:** Reusable Research OS  
**Public release:** Release 04 — Execution-Ready Proposal and Feasibility  
**Historical basis:** historical v5 plus verified post-v5 work through 2026-08-16  
**Previous public release:** Release 03

## Plain-language summary

Release 04 is the current execution-ready Research OS. It combines the earlier evidence and falsification workflow with large multimodal-data handling, a feasibility-pilot gate, Git-ready release practices, independent replication checks, source-reconciliation rules, and a clearer separation between readable proposals and detailed citation audits.

## Previous release summary

Release 03 established adversarial evidence locking, dataset release/alignment gates, and negative-result-safe experimentation.

## What changed

1. Added a large multimodal-data pipeline based on streaming raw data once and training from compact feature stores.
2. Added a feasibility-pilot gate before paid accelerator spending.
3. Added Git-ready research-release practices.
4. Added independent-replication validation as a reusable feasibility principle.
5. Added a source-reconciliation rule: when public landing pages and developer/release documentation conflict, pin the revision and privilege the documentation that governs the actual files.
6. Added a concise-proposal plus separate source-audit documentation pattern.
7. Added a reproducible vault-validation script during release reconstruction.

## Why it changed

The thesis moved from planning into a stage where multi-gigabyte JSON, 4K video, dynamic Colab limits, dataset-version differences, and teammate replication had to be handled explicitly. The first long proposal also demonstrated that a complete research log and a readable proposal should not be the same document.

## What we were trying to learn

Feasibility should be demonstrated on a small end-to-end slice before scaling, structural outputs should be independently reproducible, and source verification should remain available without overwhelming the main proposal.

## Current understanding

The reusable system now spans research discovery, evidence control, dataset validation, resource feasibility, controlled experiments, documentation, and Git release management. It remains a documented research operating system with lightweight validation tooling, not an automated autonomous research platform.

## Remaining uncertainty

The feasibility-pilot methodology is defined, but its actual performance and cost are project-specific and must be measured in each application.

## Next direction

Use the pilot gate on the football thesis, record measured outputs, then proceed to controlled full experiments only after the GO/MODIFY/NO-GO decision.

## Historical continuity

This release is a **complete repository snapshot**, not a patch. Earlier notes remain present when they still explain the research journey. The public release numbering groups the original v1-v5 history into meaningful Git milestones without erasing the original version lineage.

## Preservation notes

Historical v1-v5 principles are retained. Release 04 additionally records post-v5 lessons through 2026-08-16 without rewriting earlier stages as if those lessons were known from the beginning.

For the original v1-v5 lineage, see the project's version-history and migration notes as well as [[RELEASE_HISTORY]].
