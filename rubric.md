# Project-review rubric

Use this rubric for coaching. It is not a model-quality benchmark, hiring assessment or certification. Score only the work shown, and record the observation behind each score.

| Criterion | 0: Missing | 1: Developing | 2: Clear and testable |
| --- | --- | --- | --- |
| User task | Only a tool or feature is named | User is named but success is vague | Concrete user, task and observable result |
| Evidence | No source of truth | Source identified; missing-data behavior unclear | Source, ambiguity and unknowns handled explicitly |
| Tool choice | No explanation | Plausible choice with limited reasoning | Choice and an alternative explained with a tradeoff |
| State and review | Consequential actions undefined | Review mentioned but ownership unclear | Reads, writes, reviewer and repeat/stale behavior specified |
| Failure recovery | Happy path only | Error displayed but work preservation unclear | Failed dependency and recovery have an observable outcome |
| Communication | Colleague cannot repeat the design | Main idea clear; limitation missing | Colleague can explain the task, verification and limitation |

A total can summarize one review, but do not use an arbitrary passing threshold. First resolve any missing evidence or unsafe state-change reasoning. Record:

```text
Observed strength:
Specific gap:
Evidence from the design or demonstration:
One revision to make now:
How we will verify the revision:
```

For a later review, compare the actual revision and evidence rather than only the score.
