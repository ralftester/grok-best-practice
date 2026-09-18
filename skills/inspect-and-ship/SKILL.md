---
name: inspect-and-ship
description: >
  First pass on this repo: inspect, smallest safe change, then ship.
  Use when starting, onboarding, or the user says inspect, health check,
  smallest PR, or how do I start.
when-to-use: >
  Unfamiliar repo, first session, "what should I do first", setup, inspect,
  smallest PR, ship a tiny change.
---

# Inspect and ship

## Order

1. Discovery: `grok inspect` (and `--json` if you need a machine dump).
   Read config sources, instruction files, skills (collisions), plugins, hooks, MCP.
2. Read `AGENTS.md` and `catalog/loadout.md`.
3. If the job is design / marketing / Higgsfield / Notion, spawn **that** agent
   from `.grok/agents/`. Parent stays orchestrator.
4. Risky or multi-file → Plan Mode (`/plan`). **Caveat:** it gates file edits
   on the plan. Bash and child subagents are not the same gate.
5. Propose **one** smallest change. Wait if a human is in the loop.
6. Implement only that. Run the repo's real test/lint if it exists.

## Guardrails

- `allowed-tools` in SKILL.md does not grant or restrict tools here.
- Hooks fail-open. Trust them with `/hooks-trust`.
- Do not install every skill pack. Daily loadout is `catalog/loadout.md`.
- Never commit secrets or `.grok/sessions/`.

## Output

```
Bottom line: <one sentence>
Inspect: <skills / hooks / MCP / collisions>
Agent: <none | design | marketing | higgsfield | notion>
Change: <files>
Verified: <command or "none found">
Residual: <risks>
```
