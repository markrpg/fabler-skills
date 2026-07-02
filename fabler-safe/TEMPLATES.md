# Fabler Safe Templates

## Verified With Evidence

```markdown
## Verified With Evidence

- Claim: [Statement.]
  Evidence: [Path and symbol, route, or section.]
  Implication: [What the plan must preserve or change.]
```

## Assumptions Pending Confirmation

```markdown
## Assumptions Pending Confirmation

- Assumption: [Statement.]
  Default plan: [What to do unless corrected.]
  Flip condition: [Evidence or user answer that changes the plan.]
```

## Caller Trace

```markdown
## Caller Trace

- Planned item: [API, method, route, job, or data flow.]
  Production caller: [Path and symbol.]
  Caller behavior: [Validation, defaults, casing, sync, permissions, side effects.]
  Plan delta: [Match, mismatch, or unresolved.]
```

## Verification Contract

```markdown
## Verification

- Check: [Command or review step.]
  Expected output: [Success signal.]
  Failure signal: [What proves the stage failed.]
  Rollback: [How to undo or mitigate.]
  Stop/go: [Decision rule.]
```

## Staged Plan

```markdown
## Preferred Direction
[Decision and why.]

## Rejected Alternative
[Alternative and reason rejected.]

## Stages
1. [Stage name]
   - Files: [Paths.]
   - Change: [What changes.]
   - Evidence: [Supporting caller or architecture evidence.]
   - Verification: [Command/check and expected output.]
   - Rollback: [How to undo safely.]
   - Stop/go: [Decision rule.]

## Next Action
[First concrete action.]
```
