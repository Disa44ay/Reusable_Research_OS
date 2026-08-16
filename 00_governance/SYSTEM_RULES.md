---
type: governance
status: active
tags: [rules, provenance, no-loss]
updated: 2026-08-10
---
# System Rules

## Rule 1. Two-vault separation
Maintain two distinct knowledge bases.

A. Reusable Research OS, this vault. It stores methods, stage definitions, reusable prompts, evidence rules, AI orchestration, templates, and quality gates.

B. Research Project Vault, a separate vault. It stores the actual research journey from domain exploration through literature, topic decisions, experiments, writing, publication, and defense.

## Rule 2. No knowledge loss
Never delete project knowledge merely because it is outdated, rejected, duplicated, or disproven. Supersede it with status and provenance.

Recommended states are `VERIFIED`, `SECONDARY`, `HYPOTHESIS`, `REJECTED`, `SUPERSEDED`, and `UNKNOWN`.

## Rule 3. Preserve decision history
When a decision changes, retain the old decision, the reason it changed, the date, and the evidence that caused the change.

## Rule 4. Current-chat synchronization
At the end of any substantial research or pipeline-design session, update the relevant vault notes through the latest confirmed state of that session. Do not rely on chat history as the only copy of important knowledge.

## Rule 5. Source-first research
Important research claims must be traceable to primary papers, official dataset pages, official benchmark pages, or official repositories when available.

## Rule 6. Never upgrade certainty by repetition
Multiple AI systems repeating the same unsupported statement does not make it verified.

## Rule 7. Unknown means unknown
If a paper, metric, license, dataset property, baseline detail, code link, or venue cannot be verified, record `UNKNOWN` or `UNVERIFIED`. Do not fill the gap by inference.

## Rule 8. Topic agnosticism
This vault must not silently absorb the active thesis topic. Topic-specific configuration can instantiate the pipeline, but belongs in the project vault.

## Rule 9. Atomic reasoning nodes
Do not bury every important decision or constraint inside a long note. Preserve the narrative, then create or update an atomic node using [[00_governance/NODE_SCHEMA]] so later graph traversal can reconstruct the reasoning chain.

## Rule 10. Explicit synchronization checkpoints
The default durable synchronization point is the end of a substantial session. If the project owner explicitly asks to defer file updates during active discussion, keep a session-change buffer in the conversation and synchronize only when requested or at the agreed session checkpoint. Never claim deferred changes were already written.

## Rule 11. Research compute and deployment are separate constraints
A project may allow paid or temporary research compute while still requiring zero-cost production deployment. Score and document these separately.

## Rule 12. Multimodality must be functional
Do not reward a topic merely for combining modalities. A second modality should address a documented limitation, add measurable information, or enable a clearly defined capability. Decorative multimodality is not a research contribution.

## Update 2026-08-12: AI provenance and persistence
1. Treat [[00_governance/MEMORY_AND_PERSISTENCE_POLICY]] as mandatory for long research journeys.
2. External AI tools are research assistants, not evidence authorities. Follow [[03_ai_roles/EXTERNAL_AI_HELPER_PROTOCOL]].
3. Log prompts and correction history through [[06_prompts/PROMPT_RUN_LEDGER_PROTOCOL]].
4. Design the benchmark before optimizing model architecture when the proposed contribution depends on a derived task.
5. Separate task novelty, information novelty, modeling novelty, and engineering novelty.
