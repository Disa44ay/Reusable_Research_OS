---
type: stage-contract
status: active
created: 2026-08-14
updated: 2026-08-14
tags: [negative-results, experiment-design, scientific-validity]
related:
  - "[[STAGE_CONTRACTS]]"
  - "[[../05_scoring/TOPIC_SCORING_AND_REJECTION]]"
  - "[[../08_quality_gates/QUALITY_GATES]]"
---
# Negative Result Contract

A thesis topic is safer when its research value does not depend on a guaranteed accuracy improvement.

## Contract
A candidate may advance if:
1. the research question is genuinely unresolved,
2. baselines isolate the question,
3. a negative result would still produce interpretable evidence,
4. failure of the proposed component can be separated from failure of the data pipeline,
5. conclusions are bounded to the evaluated dataset and task.

## Example interpretation pattern
- If simple fusion beats visual-only, the additional modality carries useful information.
- If relational modeling does not beat simple fusion, the modality may help without requiring complex interaction modeling.
- If fusion does not beat visual-only, the result can show that evidence useful for detection does not necessarily transfer to anticipation.

This contract prevents model-first novelty claims and complements [[STAGE_CONTRACTS]].
