# Fabler Safe Workflows

## Caller-Trace Review

1. Extract the plan's APIs, methods, routes, jobs, and data flows.
2. For each item, find at least one real production caller.
3. Read what the caller does before and after the call.
4. Compare caller behavior to the plan:
   - parameter casing and normalization,
   - defaults and fallback values,
   - validation and license/business checks,
   - permission and role checks,
   - lazy versus eager creation,
   - side effects such as sync, cache updates, audit writes, or notifications.
5. Record every mismatch as either a finding or an assumption.
6. Revise the plan to preserve verified production behavior or explicitly reject it with a reason.

## Plan Critique

1. Restate the plan objective.
2. Use the existing plan as the ledger for bounded reviews.
3. Mark each important claim as verified or assumed.
4. Identify hidden dependencies, migration order issues, rollback gaps, and unverifiable steps.
5. Return one revised plan, not a menu of unrelated options.

## Architecture Inspection

1. Identify entry points, persistence, external interfaces, and core invariants.
2. Search narrowly before reading files.
3. Stop exploration when the evidence supports the decision.
4. Produce a compact architecture map and staged plan.

## After-Action

Run this after a refusal, reroute, failed verification, or major plan correction:

1. What was the objective?
2. Which claim was wrong, unsupported, or ambiguously phrased?
3. What production caller or evidence changed the plan?
4. What assumption needs confirmation?
5. What should the next agent do first?

## Verification Rules

Every implementation stage should include:
- Command or check to run.
- Expected successful output.
- Failure signal.
- Rollback or mitigation.
- Stop/go decision.

Verification must be able to fail. Do not use "review manually" as the only check unless the task is purely documentary.
