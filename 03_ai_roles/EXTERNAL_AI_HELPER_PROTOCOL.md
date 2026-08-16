---
type: protocol
status: active
created: 2026-08-12
updated: 2026-08-12
tags: [ai, parallel-research, verification]
related:
  - "[[03_ai_roles/AI_HELPER_REGISTRY]]"
  - "[[02_evidence/EVIDENCE_PROTOCOL]]"
  - "[[06_prompts/PROMPT_RUN_LEDGER_PROTOCOL]]"
---
# External AI Helper Protocol

## Objective
Parallelize research without turning AI agreement into evidence.

## Workflow
1. Define one precise uncertainty to reduce.
2. Assign a helper based on [[03_ai_roles/AI_HELPER_REGISTRY]].
3. Save the exact prompt with a run ID such as PR-001.
4. Save the helper used and completion status.
5. Extract claims, cited papers, datasets, and proposed gaps.
6. Mark every claim as VERIFIED, SECONDARY, INFERENCE, UNKNOWN, or REJECTED.
7. Re-check load-bearing claims against primary papers or official repositories.
8. Record corrections as separate linked facts rather than silently editing history.
9. Only verified findings may influence final novelty claims, benchmark definitions, or title lock.

## Adversarial rule
At least one research run for a candidate should try to kill the idea rather than support it.

## Quota rule
Do not spend scarce deep-reading quota on broad discovery. Use broad tools first, then narrow reviewers for the most dangerous papers.
