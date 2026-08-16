---
type: protocol
status: active
created: 2026-08-14
updated: 2026-08-14
tags: [evidence, novelty, verification, adversarial-review]
related:
  - "[[EVIDENCE_PROTOCOL]]"
  - "[[../08_quality_gates/QUALITY_GATES]]"
  - "[[../03_ai_roles/EXTERNAL_AI_HELPER_PROTOCOL]]"
---
# Adversarial Evidence Lock

A research direction may advance from literature discovery to architecture only after an explicit evidence-lock pass.

## Required checks
1. Identify the strongest direct prior work, not only papers that support the idea.
2. Separate task novelty, information novelty, method novelty, benchmark novelty, and engineering novelty.
3. Rewrite every novelty statement using the narrowest wording supported by primary sources.
4. Record dangerous claims that must never be made.
5. Verify task definitions, time horizons, metrics, class policies, dataset versions, and licenses from primary sources.
6. Mark unresolved data-quality problems as gates rather than silently cleaning them.
7. Preserve negative-result value. A well-designed experiment may answer a real research question even if the proposed method does not outperform the baseline.

## Evidence statuses
- VERIFIED: supported by a primary source or direct dataset inspection.
- SUPPORTED WITH NARROWER WORDING: core idea is supported but original wording was too broad.
- HYPOTHESIS: plausible design choice requiring experiment.
- UNRESOLVED: implementation or data issue requiring a gate.
- WITHDRAWN: previously used statement should no longer be treated as fact.
- REJECTED: contradicted or strategically discarded.

## Exit condition
Architecture design may begin only when the research gap can be written without first-ever language and still remains worth testing.

See [[../08_quality_gates/QUALITY_GATES]] and [[EVIDENCE_PROTOCOL]].
