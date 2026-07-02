# Fabler Risky Workflows

## Caller Delta Workflow

1. List the plan's depended-on APIs, routes, methods, jobs, and data flows.
2. Find one real production caller for each important item.
3. Read the caller's setup, call, and follow-up behavior.
4. Record deltas:
   - casing and normalization,
   - defaults,
   - validation,
   - permission or license checks,
   - lazy versus eager creation,
   - sync or re-fetch behavior,
   - other side effects.
5. Convert each delta into a plan change, an explicit rejection, or an assumption.

## Fast Review Workflow

1. Restate objective.
2. Use the current plan as the ledger.
3. Search narrowly.
4. Verify claims with file evidence.
5. Mark unsupported claims as assumptions.
6. Return one revised plan with verification and rollback.

## Architecture Workflow

1. Map only the entry points and data flow needed for the decision.
2. Identify invariants and blast-radius risks.
3. Prefer the smallest staged plan that preserves verified behavior.
4. Stop when further repository reading is unlikely to change the decision.

## Handoff Workflow

1. Summarize the decision.
2. List verified facts.
3. List assumptions with default answers and flip conditions.
4. List caller deltas.
5. Give staged steps, verification, rollback, and next action.
