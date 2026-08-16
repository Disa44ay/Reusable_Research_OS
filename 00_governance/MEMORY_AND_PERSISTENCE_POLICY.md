---
type: governance
status: active
created: 2026-08-12
updated: 2026-08-12
tags: [memory, persistence, provenance, continuity]
related:
  - "[[00_governance/SYSTEM_RULES]]"
  - "[[06_prompts/PROMPT_RUN_LEDGER_PROTOCOL]]"
  - "[[10_change_log/VERSIONING_AND_GIT]]"
---
# Memory and Persistence Policy

## Purpose
Do not rely on conversational memory as the only durable record of research.

## Rules
1. The vault is the authoritative long-term record.
2. Important constraints, decisions, prompts, external AI findings, corrections, evidence states, dataset access links, benchmark definitions, and rejected ideas must be written into graph-linked notes during an explicit vault update.
3. Conversation context may be used as a temporary working buffer between updates.
4. When an external AI output contains an error, preserve the original research run and add a correction or verification node. Do not silently erase the error.
5. Historical versions must remain reconstructable through Git commits, tags, or immutable snapshot archives.
6. A future researcher should be able to answer both "what was decided" and "why was it decided" from linked notes.

## Persistence chain
Conversation or external AI run
→ prompt-run record
→ evidence verification
→ decision or rejection node
→ current-state summary
→ version history.
