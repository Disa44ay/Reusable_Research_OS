# Historical README Before Public-Release Reconstruction

This file preserves the README text that existed in the historical snapshot used as the basis for this public release. It is retained for provenance. The repository-root README was rewritten only for clearer Git onboarding.

---

---
type: moc
status: active
version: v4
updated: 2026-08-14
tags: [research-os, reusable-pipeline, git-ready, moc]
---
# Reusable Research OS

## 1. Project Overview
Reusable Research OS is a topic-agnostic research workflow for moving from an unfamiliar research area to a defensible problem, verified evidence base, benchmark, implementation, experiments, academic writing, and publication preparation. It is designed to preserve the full reasoning trail instead of only the final topic.

The active thesis-specific evidence is intentionally stored in a separate vault. This repository contains reusable process, governance, evidence, AI-orchestration, quality-gate, and publication patterns.

## 2. Features
1. Evidence states that separate verified facts, hypotheses, rejected claims, and unresolved risks.
2. Atomic Obsidian nodes for decisions, sources, constraints, AI research runs, and quality gates.
3. Adversarial novelty verification before architecture design.
4. Dataset release, schema, alignment, and provenance gates.
5. AI-helper orchestration with prompt-run provenance and correction tracking.
6. Negative-result-safe experiment design.
7. Git/version snapshot rules that preserve historical research reasoning.
8. Publication and artifact checklists.

## 3. Tech Stack
1. **Obsidian Markdown**: human-readable knowledge graph and backlinks.
2. **Git**: line-level history, tags, and release provenance.
3. **Python/Jupyter**: data audits, benchmark construction, and reproducibility scripts when a project reaches implementation.
4. **External research assistants**: used as scouts or reviewers, never as unverified evidence sources.
5. **Primary-source literature**: final authority for scientific claims.

## 4. Architecture
```mermaid
flowchart LR
    A[Research Question] --> B[Evidence Discovery]
    B --> C[Primary Source Verification]
    C --> D[Adversarial Evidence Lock]
    D --> E[Dataset and Benchmark Gate]
    E --> F[Baselines and Experiments]
    F --> G[Implementation]
    G --> H[Scientific Analysis]
    H --> I[Writing and Publication]
    D --> J[Reject or Narrow]
    E --> J
    F --> J
```

Start with [[00_governance/SYSTEM_RULES]], then [[01_pipeline/END_TO_END_PIPELINE]], [[02_evidence/EVIDENCE_PROTOCOL]], and [[02_evidence/ADVERSARIAL_EVIDENCE_LOCK]].

## 5. Project Structure
```text
Reusable_Research_OS/
├── 00_governance/      # system rules, node schema, persistence policy
├── 01_pipeline/        # end-to-end research workflow
├── 02_evidence/        # evidence protocol and adversarial evidence lock
├── 03_ai_roles/        # AI orchestration and helper registry
├── 04_stage_contracts/ # stage exit criteria and negative-result contract
├── 05_scoring/         # topic scoring, rejection, and narrowing
├── 06_prompts/         # reusable prompts and prompt-run ledger rules
├── 07_artifacts/       # required research artifacts
├── 08_quality_gates/   # evidence, dataset, and implementation gates
├── 09_publication/     # publication workflow
├── 10_change_log/      # changelog, version history, Git policy
├── 11_session_history/ # chronological research-system evolution
└── README.md
```

## Version
This is **v4**. It extends v3 with the adversarial evidence-lock protocol, dataset release/alignment gate, and negative-result contract derived from the thesis validation sprint. See [[10_change_log/VERSION_HISTORY]] and [[10_change_log/CHANGELOG]].


Graph integrity record: [[GRAPH_AUDIT]].


## Additional Navigation
- [[11_session_history/SESSION_LOG]]
- [[06_prompts/REUSABLE_PROMPT_LIBRARY]]
- [[09_publication/PUBLICATION_PIPELINE]]
- [[10_change_log/MIGRATION_MANIFEST]]
