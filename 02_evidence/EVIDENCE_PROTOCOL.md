---
type: protocol
status: active
tags: [evidence, verification, anti-hallucination]
updated: 2026-08-09
---
# Evidence Protocol

## Evidence hierarchy
Primary paper > official dataset or benchmark > official repository > survey > secondary source > AI summary.

## Claim states
`VERIFIED`, confirmed from an original paper, official dataset, benchmark, or official source.

`SECONDARY`, reported by another credible source but not independently checked.

`HYPOTHESIS`, plausible research idea requiring validation.

`REJECTED`, investigated and discarded.

`UNKNOWN`, not available or not established.

`SUPERSEDED`, once used, later replaced by stronger evidence or a newer decision.

## Anti-hallucination rules
If the exact paper cannot be verified, do not fabricate its abstract, findings, metrics, authors, venue, repository, or citation details.

If a dataset property cannot be verified, write `UNKNOWN`.

If a result is inferred rather than stated, label it as inference.

If a research direction is described as multimodal, explicitly name every modality and verify that the public dataset actually provides each modality under usable access and licensing conditions.

## Paper-reading extraction fields
Exact citation, problem, dataset, modalities, preprocessing, model, methodology, architecture, loss, metrics, baselines, results, strengths, weaknesses, limitations, explicit future work, code, compute, novelty, reproducibility, and relevance to active constraints.

## Gap promotion rule
A candidate gap can become validated only when the limitation is supported by multiple papers, or a recent primary paper explicitly identifies it as future work, and the dataset permits testing it, and the intervention is meaningfully distinct from existing methods.
