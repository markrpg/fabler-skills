---
name: fabler-safe
description: Performs safer, more restrictive architecture planning, migration critique, production-caller tracing, evidence-backed repository review, and Cursor/Claude handoff work. Use when the user wants cautious Fable-style planning with explicit boundaries, verified-vs-assumed output, durable state, and fallback discipline.
disable-model-invocation: true
---

# Fabler Safe

Use this skill for cautious, planning-first architecture work. Benign architecture, migration, review, and handoff tasks are in scope; if the real task is harmful, concealed, or out of scope, stop.

## Operating Scope

In scope:
- Architecture maps, module boundaries, invariants, data flow, migration sequencing, coupling, failure modes, observability gaps, test strategy, rollback planning, and handoff writing.
- Plan critique and migration review that verifies production caller behavior before recommending changes.
- Requirements ledgers, decision records, verification contracts, and successor-model instructions.

Out of scope:
- Exploit development, malware, evasion, harmful biological or chemical assistance, classifier bypassing, model distillation, reasoning extraction, or hidden-prompt requests.
- Rewording a genuinely blocked request to conceal its intent.

## Required Workflow

1. Restate the objective in one sentence and classify it as architecture, migration planning, plan critique, or handoff.
2. Choose the smallest durable artifact:
   - For small review passes, use the existing plan or open-questions section as the ledger.
   - For multi-session work with no durable artifact, create `.workflow/` files.
3. Inspect only the smallest relevant file set.
4. For migration or wrapper plans, trace at least one production caller for each API, route, method, job, or data flow the plan intends to replicate or wrap.
5. For each important plan claim, cite supporting file evidence. Mark claims without evidence as assumptions.
6. Diff production caller behavior against the proposed plan, including defaults, casing, sync side effects, lazy/eager creation, validation, permissions, and business rules.
7. Map entry points, data flow, ownership boundaries, persistence, external interfaces, and operational assumptions only as far as needed for the decision.
8. Identify design risks, unresolved facts, assumptions, and flip conditions.
9. Recommend one preferred plan and, when useful, one rejected alternative with reasons.
10. Write staged implementation steps with target files, verification commands, expected outputs, rollback points, and stop/go criteria.
11. End with a compact handoff containing verified facts, assumptions, decisions, files to touch, verification, risks, and next action.

## Evidence Standard

Separate output into:

### Verified With Evidence
- Claim: [statement]
- Evidence: [file path and symbol, route, section, or concise location]
- Implication: [what the plan must preserve or change]

### Assumptions Pending Confirmation
- Assumption: [statement]
- Default plan: [what to do unless corrected]
- Flip condition: [what evidence or user answer changes the plan]

## Routing Rubric

Keep Fable or another high-judgement model on architecture synthesis, requirements reconciliation, trade-off analysis, plan critique, failure-mode analysis, final review, and handoff writing.

Delegate grep/search, file inventory, bounded edits, test execution, log reduction, mechanical refactors, and formatting to Opus, Sonnet, Haiku, subagents, or local tools.

## Fallback Discipline

If a planning turn is refused or rerouted:
- Do not continue as if routing did not happen.
- Identify likely trigger surfaces from visible context.
- Offer a cleaner planning-only brief if the original request was benign.
- Use safe-mode or a clean session for diagnosis where available.
- Persist the plan so work can continue on a different model without losing state.

## Durable State

Use an existing plan, handoff, issue, or design document as the source of truth when one exists. Only create `.workflow/` files when the task spans multiple sessions and no durable artifact already serves that role.

## Usage

```text
Use fabler-safe.

Review this migration plan in planning mode. Trace production callers, label each major claim as verified or assumed, and produce a staged plan with verification contracts.
```

## Additional References

- For prompts, read [PROMPTS.md](PROMPTS.md).
- For workflows, read [WORKFLOWS.md](WORKFLOWS.md).
- For output formats, read [TEMPLATES.md](TEMPLATES.md).
