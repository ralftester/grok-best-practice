---
name: inspect-and-ship
description: >
  First pass on a Grok Build repo: grok inspect, smallest safe change, plan
  caveats, then ship. Use when starting a project, onboarding, or the user
  says inspect, health check, smallest PR, or how do I start with grok.
when-to-use: >
  Unfamiliar repo, first session, "what should I do first", setup, inspect,
  smallest PR, ship a tiny change.
---

# Inspect and ship

Grok-native first session. Not a Claude Code clone.

## Do this in order

1. Run `grok inspect` (and `grok inspect --json` if you need machine output).
   Read: config sources, instruction files, skills (including collisions),
   plugins, hooks, MCP, sandbox.
2. Read `AGENTS.md`, `.grokignore`, and the smallest README that names commands.
3. If the change is risky or multi-file, enter Plan Mode (`/plan` or Shift+Tab).
   **Caveat:** Plan Mode gates *file edits on the plan*. Bash and child
   subagents are not the same gate. Do not treat `/plan` as a sandbox.
4. Propose **one** smallest PR. Wait for the human.
5. Implement only that. Run the repo's real test/lint command if it exists.
   Do not invent a test runner.
6. Summarize: what `inspect` showed, what changed, what is still unverified.

## Guardrails

- `allowed-tools` in SKILL.md does not grant or restrict tools here.
  Real gates: permission rules, sandbox, and hooks (`/hooks-trust`).
- Hooks fail-open: a crash or timeout does not block the tool.
- Skill body stays short. Point at `best-practice/` in this repo instead of
  pasting a textbook.
- Never commit secrets, `.grok/sessions/`, or generated junk.

## Output

```
Bottom line: <one sentence>
Inspect: <skills / hooks / collisions>
Plan: <used / skipped, and why>
Change: <files>
Verified: <command or "none found">
Residual: <risks>
```
