---
name: loadout
description: >
  Daily skill packs for this playbook: design, marketing, Higgsfield, Notion.
  Use when the user says loadout, install packs, Higgsfield, Notion skills,
  marketing skills, impeccable, or "what should I install".
when-to-use: >
  First setup, missing packs, "install skills", design/marketing/video stack.
---

# Daily loadout

Install **packs**, do not copy trees into this repo. Then run `inspect-and-ship` discovery for **this** harness (Grok: `grok inspect`; Claude/Codex: list `skills/`).

Full table: [catalog/loadout.md](../../catalog/loadout.md).

```bash
# engineering baseline
grok plugin install superpowers@xai-official --trust

# design
npx skills add pbakaus/impeccable
npx skills add nextlevelbuilder/ui-ux-pro-max-skill
npx skills add vercel-labs/agent-skills --skill web-design-guidelines
npx skills add anthropics/skills --skill frontend-design

# marketing
npx skills add coreyhaines31/marketingskills

# Higgsfield (CLI auth is part of setup)
npx skills add higgsfield-ai/skills

# Notion workspace skills (needs Notion login)
npx skills add notion
```

## After install

1. Discovery from `inspect-and-ship` — confirm names, collisions, MCP (Notion, Higgsfield).
2. Spawn one agent: `design` · `marketing` · `higgsfield` · `notion`.
3. If `npx skills` ran inside an agent and only wrote `.agents/skills/`,
   pass `-a` for the host (Grok still scans `.agents/skills/` and `.claude/skills/`).

## Do not

- `npx skills add` the entire Meng To or TypeUI 67-skill trees.
- Commit vendor skill bodies into this playbook.
- Put Notion or Higgsfield tokens in git.
