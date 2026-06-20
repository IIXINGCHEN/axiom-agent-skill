# axiom

Winner: `Current`

- current tokens: `66`
- winner tokens: `66`

## Winner

Use when the user says axiom / axiomOS / 用 axiom 视角, or asks for production-grade engineering: architecture review, complex feature design, code review, bug diagnosis, security assessment. Do not use for prototypes, MVP validation, one-off scripts, exploratory ML.

## Candidate Ranking

| Candidate | Tokens | Dev FP | Dev FN | Dev Near | Holdout FP | Holdout FN |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| `Current` | 66 | 0 | 0 | 1.0 | 0 | 0 |
| `Minimal` | 56 | 0 | 1 | 1.0 | 0 | 0 |
| `Guardrail` | 68 | 0 | 1 | 1.0 | 0 | 0 |
| `Balanced` | 74 | 0 | 1 | 1.0 | 0 | 0 |
| `Boundary` | 90 | 0 | 1 | 1.0 | 0 | 0 |
| `Artifact Aware` | 101 | 0 | 1 | 1.0 | 0 | 0 |

## Acceptance Gates

| Gate | Winner FP | Winner FN | Current FP | Current FN | Baseline FP | Baseline FN |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Holdout | 0 | 0 | 0 | 0 | - | - |
| Blind Holdout | 0 | 0 | 0 | 0 | - | - |
| Judge Blind Holdout | 0 | 2 | 0 | 2 | - | - |
| Adversarial Holdout | 0 | 0 | 0 | 0 | - | - |

## Calibration

| Gate | Winner Gap | Winner Risk | Winner Boundary Rate | Current Gap | Baseline Gap |
| --- | ---: | --- | ---: | ---: | ---: |
| Holdout | 0.506 | healthy | 0.0 | 0.506 | - |
| Blind Holdout | 0.506 | healthy | 0.0 | 0.506 | - |
| Adversarial Holdout | 0.489 | healthy | 0.0 | 0.489 | - |

## Judge Blind Summary

| Gate | Winner Agreement | Winner Mean Confidence | Current Agreement | Baseline Agreement |
| --- | ---: | ---: | ---: | ---: |
| Judge Blind Holdout | 0.667 | 0.643 | 0.667 | - |

## Family Health

| Gate | Winner Clean Families | Winner Weakest Family | Current Clean Families | Baseline Clean Families |
| --- | --- | --- | --- | --- |
| Holdout | 6/6 | trivial (0 errors) | 6/6 | -/- |
| Blind Holdout | 6/6 | root_cause (0 errors) | 6/6 | -/- |
| Judge Blind Holdout | 4/6 | root_cause (1 errors) | 4/6 | -/- |
| Adversarial Holdout | 5/5 | routes_to_thinking_skills (0 errors) | 5/5 | -/- |

## Selection Logic

Ordered by:
- fewest false positives
- fewest false negatives
- highest near-neighbor pass rate
- highest negative pass rate
- highest precision
- highest recall
- shortest description
