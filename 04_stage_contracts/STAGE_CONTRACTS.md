---
type: specification
status: active
tags: [stage-contracts, handoff]
updated: 2026-08-09
---
# Stage Contracts

Every pipeline stage must have an input contract, an output artifact, verification requirements, and an exit gate.

## Domain discovery
Input: user or team profile, hard constraints, broad interests.
Output: domain landscape table.
Exit gate: enough candidate domains exist to compare on evidence, compute, datasets, and relevance.

## Dataset discovery
Input: shortlisted domains.
Output: verified dataset table with official links and unknowns.
Exit gate: at least one usable public dataset is confirmed for a viable direction.

## Literature collection
Input: domain and dataset candidates.
Output: bibliography with primary links and status.
Exit gate: foundational and recent literature can be identified without fabricated metadata.

## Literature matrix
Input: exact papers.
Output: one structured extraction per paper and a cross-paper matrix.
Exit gate: important claims are traceable to paper text.

## Gap validation
Input: verified matrix.
Output: gap table with evidence papers, evidence type, feasibility, novelty risk, and unknowns.
Exit gate: candidate gap can be tested and is distinguishable from known methods.

## Topic selection
Input: validated evidence package.
Output: scored candidates, rejection reasons, and one provisional winner.
Exit gate: critical assumptions are verified.

## Architecture and experiments
Input: locked research question.
Output: architecture specification and experiment matrix.
Exit gate: compute, evaluation, baselines, and implementation scope are realistic.

## Implementation and evaluation
Input: approved specs.
Output: code, reproducible runs, metrics, logs, failures, figures, and tables.
Exit gate: claims can be supported by actual experiments.

## Writing and publication
Input: verified citations and experimental results.
Output: manuscript, reviewer checklist, venue checklist, submission package.
Exit gate: no unsupported scientific claim remains knowingly unmarked.
