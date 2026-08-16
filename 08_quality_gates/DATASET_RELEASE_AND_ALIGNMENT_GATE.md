---
type: quality-gate
status: active
created: 2026-08-14
updated: 2026-08-14
tags: [dataset, versioning, alignment, reproducibility]
related:
  - "[[QUALITY_GATES]]"
  - "[[../02_evidence/ADVERSARIAL_EVIDENCE_LOCK]]"
  - "[[../07_artifacts/REQUIRED_ARTIFACTS]]"
---
# Dataset Release and Alignment Gate

Large research datasets may have multiple mirrors, evolving schemas, corrections, or documentation drift. A dataset name alone is not enough provenance.

## Gate sequence
1. Pin the canonical distribution source and exact revision when possible.
2. Record hashes or immutable identifiers for downloaded files.
3. Compare the actual shipped schema with documentation before writing parsers.
4. Use project-provided loaders when timestamp semantics are known to be inconsistent.
5. Validate event-to-frame alignment against every modality used by the model.
6. Maintain an exclusions or quarantine ledger. Never silently delete suspicious records.
7. Resolve documented match-level correction issues before constructing folds.
8. Freeze class policy and folds before model training.

## Required artifacts
- dataset_manifest.json
- corrections.json
- exclusions.json
- alignment_report.json
- class_distribution.json
- folds.json

These artifacts become part of the reproducibility package described in [[../07_artifacts/REQUIRED_ARTIFACTS]].
