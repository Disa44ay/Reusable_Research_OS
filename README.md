---
type: moc
status: active
public_release: "Release 01"
updated: 2026-08-16
tags: [research-os, reusable-pipeline, git-ready, moc]
---
# Reusable Research OS

## 1. Project Overview

Reusable Research OS is a topic-agnostic research workflow for moving from an unfamiliar domain to a verified question, feasible experiment, reproducible evidence trail, and publication-ready artifact. **Release 01: Foundation and Scope Formation** represents the state of that workflow at this historical milestone.

Start with [[VERSION_BRIEF]] for the human-readable history of this release.

## 2. Features

1. Evidence protocol, stage contracts, topic scoring and rejection.
2. Graph-native Obsidian node schema and knowledge-preservation rules.
3. Reusable prompt, artifact, quality-gate and publication workflow.
4. Deadline-aware candidate-title checkpoint.

## 3. Tech Stack

1. **Obsidian Markdown** for graph-native research memory.
2. **Git/GitHub** for diffs, tags, history, and releases.
3. **Primary-source literature** as the final evidence authority.
4. **Python/Jupyter** where validation or experimental tooling is required.
5. **External AI assistants** only in scoped, provenance-tracked roles.

## 4. Architecture

```text
Research Goal --> Discovery --> Evidence Verification --> Candidate Scoring/Rejection --> Stage Exit --> Research Artifacts --> Publication
```

This is a research/knowledge workflow, not a claim of an autonomous software platform. See [[ARCHITECTURE]] and [[01_pipeline/END_TO_END_PIPELINE]].

## 5. Project Structure

The established numbered folders are preserved. Key entry points are:

1. `00_governance/` — research rules and knowledge governance.
2. `01_pipeline/` — end-to-end workflow.
3. `02_evidence/` — evidence and verification rules.
4. `03_ai_roles/` — AI orchestration where present in this release.
5. `04_stage_contracts/` to `09_publication/` — stage exits, scoring, prompts, artifacts, quality gates, and publication.
6. `10_change_log/` and `11_session_history/` — provenance and chronological evolution.

See [[RELEASE_HISTORY]], the project's existing changelog/version history, and [[GRAPH_AUDIT]].
