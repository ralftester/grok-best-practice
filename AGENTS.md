# AGENTS.md

Unofficial playbook. Grok Build CLI (`grok`), not Grok Bot, not grok.com chat.

English `README.md` is the homepage. Polish is `README.pl.md` — same section order.

## First session

1. `grok inspect` (or `grok inspect --json`).
2. Skill `inspect-and-ship`. Do not edit yet.
3. Install the daily loadout once (`catalog/loadout.md`). Then inspect again.
4. Spawn **one** specialist: `design` · `marketing` · `higgsfield` · `notion`.

Do not dump 292 skills into `.grok/`. Packs install with `npx skills add`. This repo only ships routers + agents.

## Specialists (`.grok/agents/`)

| Agent | When |
|---|---|
| `design` | UI, landing, polish, anti-slop |
| `marketing` | Copy, CRO, SEO, social, launch |
| `higgsfield` | Image/video/ads via Higgsfield CLI or MCP |
| `notion` | Pages, skills library, Notion MCP |

Parent stays orchestrator. One specialist per job unless two domains are truly separate.

## Notion

Prefer Notion MCP for workspace pages. Author skills as Notion pages, then `npx skills add <notion-url>` or `npx skills add notion` so every agent loads the same SKILL.md. That loop is the point: Notion is the shared library, Grok (and Claude/Codex) are the runners.

## Hard rules

- `allowed-tools` in SKILL.md does **not** restrict tools here. Real gates: permissions, sandbox, `/hooks-trust`. Hooks fail-open.
- Plan Mode does not block bash.
- Live Shields for stars. Never invent counts.
- No generated YAML agents, no LifeJiggy `GROK.md`, no secrets, no `.grok/sessions/`.
