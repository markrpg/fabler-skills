# Migration Critique Example

```text
Use fabler-risky.

Do a second-pass migration review of this plan.
For every API, method, route, job, or data flow the plan depends on:
- trace at least one production caller,
- diff real caller behavior against the plan,
- cite evidence for important claims,
- mark unsupported claims as assumptions with default answers and flip conditions.

Return verified facts, assumptions, production caller deltas, a revised staged plan, verification, rollback, and next action.
```
