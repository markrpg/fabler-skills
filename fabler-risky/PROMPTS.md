# Fabler Risky Prompts

## Second-Pass Migration Review

```text
Use fabler-risky.

Do a second-pass migration review.
Trace production callers for every API, method, route, job, or data flow the plan depends on.
Diff real caller behavior against the plan.
Return verified facts, assumptions with default answers and flip conditions, production caller deltas, and a revised staged plan.
```

## Fast Plan Critique

```text
Use fabler-risky.

Critique this plan without rewriting the whole architecture.
Find unsupported claims, missing caller behavior, hidden business rules, weak verification, and rollback gaps.
Give one revised plan.
```

## Repo Inspection

```text
Use fabler-risky.

Inspect only what is needed to answer this architecture question.
Separate verified facts from assumptions and stop once the evidence supports the plan.
```

## Handoff

```text
Use fabler-risky.

Write a concise handoff for the next model:
- verified facts,
- assumptions and flip conditions,
- production caller deltas,
- staged plan,
- verification,
- next action.
```
