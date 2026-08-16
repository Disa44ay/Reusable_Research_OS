# Architecture

## Status
Release 03 adds formal falsification and dataset provenance gates to the documented workflow.

## Research flow

```text
Candidate
→ primary-source review
→ adversarial evidence lock
→ dataset release/schema/alignment gate
→ negative-result contract
→ implementation decision
```

The candidate is allowed to narrow or fail. Rejected claims are preserved as evidence rather than rewritten.

## Main components

1. [[02_evidence/ADVERSARIAL_EVIDENCE_LOCK]]
2. [[08_quality_gates/DATASET_RELEASE_AND_ALIGNMENT_GATE]]
3. [[04_stage_contracts/NEGATIVE_RESULT_CONTRACT]]
4. [[01_pipeline/END_TO_END_PIPELINE]]
