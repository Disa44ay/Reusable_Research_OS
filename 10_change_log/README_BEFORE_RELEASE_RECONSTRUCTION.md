# Historical README Before Public-Release Reconstruction

This file preserves the README text that existed in the historical snapshot used as the basis for this public release. It is retained for provenance. The repository-root README was rewritten only for clearer Git onboarding.

---

---
type: moc
status: active
tags: [research-os, reusable-pipeline, moc]
updated: 2026-08-10
---
# Reusable Research OS

This vault contains the reusable research system. It must remain topic-agnostic.

Its job is to let an AI or human start from a brand-new research area and move through evidence discovery, dataset validation, literature review, gap validation, topic selection, architecture, experiments, implementation, scientific writing, review, and publication preparation without inventing evidence.

## Boundary rule
Topic-specific findings, papers, datasets, candidate gaps, experimental results, thesis decisions, and defense material belong in the separate research-project vault, not here.

## Read order
1. [[00_governance/SYSTEM_RULES]]
2. [[01_pipeline/END_TO_END_PIPELINE]]
3. [[02_evidence/EVIDENCE_PROTOCOL]]
4. [[03_ai_roles/AI_ORCHESTRATION]]
5. [[04_stage_contracts/STAGE_CONTRACTS]]
6. [[05_scoring/TOPIC_SCORING_AND_REJECTION]]
7. [[06_prompts/REUSABLE_PROMPT_LIBRARY]]
8. [[07_artifacts/REQUIRED_ARTIFACTS]]
9. [[08_quality_gates/QUALITY_GATES]]
10. [[09_publication/PUBLICATION_PIPELINE]]
11. [[10_change_log/CHANGELOG]]
12. [[11_session_history/SESSION_LOG]]

## Current system status
Version: 0.1 migrated from the original thesis knowledge base.

The original mixed knowledge base has been separated into this reusable system vault and a thesis-specific research vault. Nothing from the source files was intentionally deleted. See [[10_change_log/MIGRATION_MANIFEST]].

## Graph and reasoning extraction
Important constraints, decisions, sources, candidates, and rejections should be represented as atomic nodes in addition to readable narrative notes. Follow [[00_governance/NODE_SCHEMA]].
