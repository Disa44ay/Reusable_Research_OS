---
type: evidence-rule
status: active
created: 2026-08-16
updated: 2026-08-16
tags: [sources, datasets, reconciliation, provenance]
related:
  - "[[EVIDENCE_PROTOCOL]]"
  - "[[../08_quality_gates/DATASET_RELEASE_AND_ALIGNMENT_GATE]]"
---
# Source Reconciliation Rule

When a project landing page, paper, repository documentation, shipped file schema, or dataset mirror disagrees, do not silently choose the most convenient version.

1. Pin the repository and dataset revision used for the experiment.
2. Prefer documentation that governs the actual shipped files for schema and loader behavior.
3. Record conflicts explicitly.
4. Preserve older claims as historical evidence when they explain previous decisions.
5. Treat mirrors as potentially stale unless the project identifies them as canonical.
6. Do not convert a release-specific observation into a timeless dataset claim.

The output of reconciliation is a versioned provenance record, not an attempt to rewrite conflicting history.
