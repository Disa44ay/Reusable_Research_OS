---
type: prompt-governance
status: active
created: 2026-08-12
updated: 2026-08-12
tags: [prompts, provenance, reproducibility]
related:
  - "[[03_ai_roles/EXTERNAL_AI_HELPER_PROTOCOL]]"
  - "[[02_evidence/EVIDENCE_PROTOCOL]]"
---
# Prompt Run Ledger Protocol

## Required fields for every external AI research run
1. Run ID.
2. Date.
3. Helper and plan tier if relevant.
4. Exact goal.
5. Exact prompt text or a preserved prompt artifact.
6. Status: planned, running, partial, completed, superseded.
7. Raw finding summary.
8. Primary-source verification status.
9. Known errors or hallucinations.
10. Decisions influenced by the run.
11. Follow-up papers that need deep verification.

## Why this exists
A prompt is part of the research process when it changes the search space, evidence matrix, candidate ranking, benchmark, or decision. It must therefore be reproducible and auditable.
