# Fable Restricted-Scenario Skills

This repository contains two Cursor skills that help Fable stay useful in restricted or routing-prone coding scenarios.

They are meant for Fable-style architecture planning, migration critique, production-flow verification, and handoff writing when broad repository context, policy-adjacent wording, or ambiguous prompts could otherwise derail the session.

They are not model jailbreaks or classifier bypasses, and they do not prevent routing. Instead, they make planning work more evidence-backed and resilient by keeping requests planning-first, narrowing context, tracing real production callers, separating verified facts from assumptions, and producing durable handoffs if the session moves to another model.

## Variants

### Fabler Safe

Use `fabler-safe` when the work is sensitive, ambiguous, policy-adjacent, or needs more explicit guardrails.

Best for:
- cautious architecture reviews,
- migration planning with stronger boundaries,
- plan critique before implementation,
- handoffs where assumptions must be visible,
- sessions where routing or refusal risk needs careful handling.

### Fabler Risky

Use `fabler-risky` when the task is ordinary engineering work and you want less ceremony. "Risky" means lighter process, not looser policy boundaries.

Best for:
- second-pass migration reviews,
- production caller tracing,
- finding where a plan disagrees with real flows,
- concise architecture critique,
- fast handoffs for another model or developer.

## Install For Cursor

Copy either or both skill folders into your personal Cursor skills directory.

macOS or Linux:

```bash
mkdir -p ~/.cursor/skills
cp -R fabler-safe ~/.cursor/skills/
cp -R fabler-risky ~/.cursor/skills/
```

Windows PowerShell:

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.cursor\skills"
Copy-Item -Recurse fabler-safe "$env:USERPROFILE\.cursor\skills\"
Copy-Item -Recurse fabler-risky "$env:USERPROFILE\.cursor\skills\"
```

Then start a new chat or reload Cursor if the skills list does not refresh.

## Usage

Invoke explicitly:

```text
Use fabler-safe.
```

or:

```text
Use fabler-risky.
```

## Core Idea

The most useful planning move is to verify production behavior, not just target methods. For every API, route, method, job, or data flow a plan intends to replicate or wrap, trace at least one production caller and compare what the caller does against the plan.

Good outputs separate:
- verified facts with evidence,
- assumptions pending confirmation,
- production caller deltas,
- staged implementation steps,
- verification contracts,
- rollback points,
- next action.

## License

MIT. See [LICENSE](LICENSE).
