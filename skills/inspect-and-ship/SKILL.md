---
name: inspect-and-ship
description: >
  First pass on this repo: harness discovery, smallest safe change, then ship.
  Use when starting, onboarding, or the user says inspect, health check,
  smallest PR, or how do I start.
when-to-use: >
  Unfamiliar repo, first session, "what should I do first", setup, inspect,
  smallest PR, ship a tiny change.
---

# Inspect and ship

## 1. Discovery (this harness only)

| You are | Do |
|---|---|
| Grok Build | `grok inspect` (and `--json` if you need a machine dump). Read skills, hooks, plugins, MCP, collisions. |
| Claude Code | Read `AGENTS.md` (via `CLAUDE.md`). List `skills/` and `.claude/skills/`. Note MCP if present. |
| Codex | Read `AGENTS.md`. List `skills/` and `.agents/skills/`. |
| Cursor / other | Read `AGENTS.md`. List `skills/` and any `.cursor/skills/`. |

Do not run another harness’s inspect command.

## 2. Then

1. Read `catalog/loadout.md` if packs might be missing.
2. If the job is design / marketing / Higgsfield / Notion, spawn **that** agent from `.grok/agents/`. Parent stays orchestrator.
3. Risky or multi-file → plan first. **Grok:** `/plan` gates file edits on the plan; bash and child subagents are not that gate.
4. Propose **one** smallest change. Wait if a human is in the loop.
5. Implement only that. Run the repo’s real test/lint if it exists. Do not invent a runner.

Routing checks: [examples/eval-routing.md](../../examples/eval-routing.md).

## Guardrails

- Do not install every skill pack. Daily set is `catalog/loadout.md`.
- Never commit secrets or session dumps.
- **Grok Build:** `allowed-tools` is not a tool gate. Hooks fail-open.
- **Claude Code:** `allowed-tools` is a tool gate.

## Output

```
Bottom line: <one sentence>
Inspect: <harness; skills; MCP; collisions; agent spawned or none>
Change: <files; verified command or "none found">
Residual: <risks still open>
```
