---
name: fabler-risky
description: Performs freer, evidence-first architecture review, migration critique, production-flow verification, and practical Fable-style planning. Use when the user wants low-ceremony caller tracing, verified-vs-assumed output, bounded repo inspection, and staged implementation plans.
disable-model-invocation: true
---

# Fabler Risky

Use this skill for practical architecture and migration planning with minimal ceremony. Benign engineering work only; if the real task is out of scope, stop.

## What Matters Most

The highest-value move is not rereading the target method. It is tracing production callers and checking what real flows do around that method.

For each API, route, method, job, or data flow the plan intends to replicate or wrap:
- Trace at least one production caller.
- Diff caller behavior against the plan.
- Cite evidence for important claims.
- Mark unsupported claims as assumptions with a default answer and flip condition.

## Required Workflow

1. Restate the objective in one sentence.
2. Use the existing plan, issue, or open-questions section as the ledger for small reviews. Create `.workflow/` files only when no durable artifact exists and the task spans sessions.
3. Inspect the smallest relevant file set.
4. Trace production callers for planned APIs, methods, routes, jobs, and data flows.
5. Diff real caller behavior against the plan: defaults, casing, validation, permissions, business rules, lazy/eager creation, and side effects.
6. Label claims as `verified` with evidence or `assumed` pending confirmation.
7. Map entry points and data flow only as far as needed for the decision.
8. Recommend one preferred plan, with a rejected alternative only when it clarifies the choice.
9. Write staged implementation steps with target files, verification commands, expected outputs, rollback points, and stop/go criteria.
10. End with verified facts, assumptions, risks, verification, and the next action.

## Output Standard

Use these sections when the task is more than a quick answer:
- `Verified With Evidence`
- `Assumptions Pending Confirmation`
- `Production Caller Deltas`
- `Revised Plan`
- `Verification`
- `Next Action`

## Routing Rubric

Keep Fable or another high-judgement model on architecture synthesis, plan critique, trade-off analysis, failure-mode analysis, and final review.

Delegate grep/search, bounded edits, test runs, log reduction, and mechanical refactors to cheaper models, subagents, or local tools.

## Usage

```text
Use fabler-risky.

Do a second-pass migration review. Trace production callers, identify where the plan disagrees with real flows, and return a revised plan with verified facts and assumptions.
```

## Additional References

- For prompts, read [PROMPTS.md](PROMPTS.md).
- For workflows, read [WORKFLOWS.md](WORKFLOWS.md).
- For output formats, read [TEMPLATES.md](TEMPLATES.md).
