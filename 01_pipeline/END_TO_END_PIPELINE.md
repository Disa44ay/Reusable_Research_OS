---
type: pipeline
status: active
tags: [pipeline, research-process]
updated: 2026-08-10
---
# End-to-End Research Pipeline

## Canonical sequence
Domain discovery
→ dataset discovery
→ literature collection
→ literature matrix
→ recurring limitations
→ validated research gaps
→ topic candidates
→ scoring
→ topic lock
→ architecture
→ experiment design
→ implementation
→ controlled experiments
→ error analysis
→ reproducibility audit
→ scientific writing
→ harsh review
→ venue selection
→ submission
→ revision or rebuttal
→ publication tracking

For academic projects, add thesis preparation and defense after the evidence and system are stable.

## Stage 1. Domain discovery
Goal: identify research domains, not prematurely invent thesis topics.

Output should capture trends, publication activity, industry relevance, public datasets, benchmark maturity, code availability, compute demands, multimodal opportunities, and feasibility.

## Stage 2. Dataset discovery
Verify access, license, size, modalities, labels, splits, benchmark papers, baseline code, storage, preprocessing cost, and whether the required modalities are genuinely public.

## Stage 3. Literature collection
Collect foundational and recent papers. Store exact bibliographic metadata and primary links. Do not treat search summaries as paper evidence.

## Stage 4. Literature analysis
Read actual papers and extract structured evidence. Separate direct statements, inference, and missing information.

## Stage 5. Gap validation
A gap is not valid because it sounds plausible. Require evidence from repeated limitations, explicit future work, benchmark weakness, or a clearly unresolved measurable problem.

## Stage 6. Topic generation and scoring
Generate candidate topics only from verified datasets, literature, and validated or explicitly labeled candidate gaps.

## Stage 7. Topic lock
Do not lock while a critical assumption about dataset access, baseline reproducibility, compute, evaluation, or novelty remains unverified.

## Stage 8. Architecture
Design the smallest production-quality architecture that supports the research question and reproducible experimentation.

## Stage 9. Experiment design
Define baseline, proposed method, metrics, ablations, hyperparameters, compute budget, error analysis, expected artifacts, and stop conditions. Never promise numerical improvement.

## Stage 10. Implementation
Implement the approved architecture and experiment specification. Keep research decisions separate from coding convenience.

## Stage 11. Evaluation
Run controlled comparisons, ablations, robustness checks, runtime or compute tracking, and failure analysis. Preserve negative results.

## Stage 12. Writing
Write from verified sources and actual results only. Flag unsupported claims and missing citations.

## Stage 13. Harsh review
Attack novelty, leakage, unfair baselines, weak statistics, missing ablations, missing citations, reproducibility, figures, tables, and exaggerated claims.

## Stage 14. Publication
Select a realistic venue based on scope, evidence, timing, formatting, indexing, and submission rules. Prepare manuscript, supplementary material, code and reproducibility package as appropriate.

## Stage 6A. Candidate falsification
Before ranking a promising candidate, actively search for prior work that already performs the proposed contribution. The goal is to kill weak novelty claims early.

Record one of these outcomes:
1. `SURVIVES` — no direct conflict found yet, but novelty is still a hypothesis.
2. `NARROWED` — related work exists, so the proposed contribution must become more specific.
3. `DOWNGRADED` — the candidate remains possible but is no longer a top choice.
4. `REJECTED` — direct prior work, inaccessible data, compute, evaluation, or implementation constraints make the idea unsuitable.

## Stage 6B. Candidate-title checkpoint
When an institution requires a title before the final topic can be fully locked, create 2 to 3 evidence-backed candidate titles instead of pretending one title is final. Each candidate title must map to a candidate-topic node and list unresolved assumptions. See [[04_stage_contracts/CANDIDATE_TITLE_CHECKPOINT]].

## Update 2026-08-12: Fast deadline validation branch
When a title deadline is imminent, use this compressed evidence path:

1. Candidate boundary definition.
2. Adversarial related-work sweep.
3. Deep verification of the two or three most dangerous papers.
4. Dataset access and label audit.
5. Benchmark design before model design.
6. Novelty decomposition into task, information, method, and benchmark contributions.
7. Minimum baseline and ablation design.
8. Hostile reviewer test.
9. Candidate-title ranking.
10. Proposal lock.

This branch does not lower the evidence standard. It reduces duplicated search.
