---
type: governance-schema
status: active
tags: [knowledge-graph, provenance, reasoning, nodes]
updated: 2026-08-10
related:
  - "[[00_governance/SYSTEM_RULES]]"
  - "[[07_artifacts/REQUIRED_ARTIFACTS]]"
---
# Knowledge Graph Node Schema

The research system must preserve both readable notes and atomic reasoning nodes.

## Why atomic nodes exist
Long notes are useful for humans but hide individual decisions, assumptions, evidence, and constraints. Atomic nodes make later graph traversal and reasoning extraction possible without deleting the readable narrative.

## Required node families
1. `constraint` nodes record a hard limit, preference, resource boundary, deadline, or team-capacity fact.
2. `decision` nodes record what was chosen, why it was chosen, what alternatives were considered, and what could reverse the decision.
3. `source` or `evidence` nodes record a primary source and the exact claims it supports.
4. `candidate-topic` nodes record a research hypothesis, candidate title, expected contribution, required evidence, risks, and rejection conditions.
5. `rejection` or `downgrade` nodes preserve ideas that were investigated but weakened by evidence.
6. `dataset` nodes record access, license, modalities, labels, compute implications, and source status.
7. `concept` nodes connect reusable technical concepts to project-specific candidates.

## Minimum frontmatter for reasoning nodes
Use fields when applicable:

```yaml
type: decision | constraint | source | candidate-topic | rejection | dataset | concept
status: active | verified | hypothesis | rejected | downgraded | superseded | unknown
created: YYYY-MM-DD
updated: YYYY-MM-DD
tags: []
depends_on: []
supported_by: []
related: []
supersedes: []
superseded_by: []
```

## Decision-node body contract
Every important decision should answer:
1. What was decided?
2. Why?
3. Which constraints caused it?
4. Which evidence supports it?
5. Which alternatives were rejected or deferred?
6. What would cause the decision to change?
7. Which downstream nodes depend on it?

## No-loss rule
Atomic nodes supplement existing notes. They do not replace or erase historical narrative. When information changes, link the old and new nodes with `supersedes` or `superseded_by` rather than deleting the old state.
