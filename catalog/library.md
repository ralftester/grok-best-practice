# Skill library (pointers)

What people actually install. Same `SKILL.md` files work in **Grok Build**, Claude Code, Codex, and Cursor after `npx skills add` (Grok also has `grok plugin install` for Superpowers).

We do **not** vendor the trees. Stars are live Shields. Human docs: [docs/README.md](../docs/README.md).

Daily subset: [loadout.md](loadout.md).

## Find a pack

```bash
npx skills add vercel-labs/skills --skill find-skills
npx skills find postgres
```

Directory: [skills.sh](https://skills.sh).

## How you work

| Pack | When | Install | Grok |
|---|---|---|---|
| [obra/superpowers](https://github.com/obra/superpowers) [![★](https://img.shields.io/github/stars/obra/superpowers)](https://github.com/obra/superpowers) | Plan, TDD, debug, “don’t code yet” | `grok plugin install superpowers@xai-official --trust` or `npx skills add obra/superpowers` | Official marketplace |
| [mattpocock/skills](https://github.com/mattpocock/skills) [![★](https://img.shields.io/github/stars/mattpocock/skills)](https://github.com/mattpocock/skills) | Engineering taste, grilling a design | `npx skills add mattpocock/skills` | Then `grok inspect` |
| [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) [![★](https://img.shields.io/github/stars/addyosmani/agent-skills)](https://github.com/addyosmani/agent-skills) | DEFINE → SHIP loop | `npx skills add addyosmani/agent-skills` | Inspect names |
| [github/spec-kit](https://github.com/github/spec-kit) [![★](https://img.shields.io/github/stars/github/spec-kit)](https://github.com/github/spec-kit) | Spec before code | `uv tool install specify-cli` | CLI, not a SKILL.md dump |
| This repo `inspect-and-ship` | First session | already in `skills/` | Per-harness discovery |

## Design and frontend

| Pack | When | Install |
|---|---|---|
| [pbakaus/impeccable](https://github.com/pbakaus/impeccable) [![★](https://img.shields.io/github/stars/pbakaus/impeccable)](https://github.com/pbakaus/impeccable) | Polish / audit / “looks AI-generic” | `npx skills add pbakaus/impeccable` |
| [ui-ux-pro-max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) [![★](https://img.shields.io/github/stars/nextlevelbuilder/ui-ux-pro-max-skill)](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | Styles, palettes, product-type search | `npx skills add nextlevelbuilder/ui-ux-pro-max-skill` |
| [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) [![★](https://img.shields.io/github/stars/vercel-labs/agent-skills)](https://github.com/vercel-labs/agent-skills) | `web-design-guidelines`, `vercel-react-best-practices` | `npx skills add vercel-labs/agent-skills --skill web-design-guidelines` |
| [anthropics/skills](https://github.com/anthropics/skills) `frontend-design` [![★](https://img.shields.io/github/stars/anthropics/skills)](https://github.com/anthropics/skills) | Distinct UI, not a template | `npx skills add anthropics/skills --skill frontend-design` |
| [hueyexe/frontend-agent-skills](https://github.com/hueyexe/frontend-agent-skills) [![★](https://img.shields.io/github/stars/hueyexe/frontend-agent-skills)](https://github.com/hueyexe/frontend-agent-skills) | Forms, nav, errors that don’t feel dumped | `npx skills add hueyexe/frontend-agent-skills` |

Spawn agent `design` in this repo after those packs exist.

## Marketing and Notion

| Pack | When | Install |
|---|---|---|
| [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) [![★](https://img.shields.io/github/stars/coreyhaines31/marketingskills)](https://github.com/coreyhaines31/marketingskills) | Copy, CRO, SEO, social, launch | `npx skills add coreyhaines31/marketingskills` — start with `product-marketing` |
| Notion Skills API | How-tos live in the workspace | `npx skills add notion` + MCP `https://mcp.notion.com/mcp` |
| [makenotion/notion-skills-github-sync](https://github.com/makenotion/notion-skills-github-sync) [![★](https://img.shields.io/github/stars/makenotion/notion-skills-github-sync)](https://github.com/makenotion/notion-skills-github-sync) | Team: Notion → GitHub marketplace | optional sync |

Spawn `marketing` or `notion`.

## Image, video, ads

| Pack | When | Install | Notes |
|---|---|---|---|
| [higgsfield-ai/skills](https://github.com/higgsfield-ai/skills) [![★](https://img.shields.io/github/stars/higgsfield-ai/skills)](https://github.com/higgsfield-ai/skills) | Ads, Soul face, product shoot, Seedance/Kling | `npx skills add higgsfield-ai/skills` | CLI + MCP `https://mcp.higgsfield.ai/mcp`. Spawn `higgsfield`. |
| [remotion-dev/skills](https://github.com/remotion-dev/skills) [![★](https://img.shields.io/github/stars/remotion-dev/skills)](https://github.com/remotion-dev/skills) | Video **as React code** | `npx skills add remotion-dev/skills` | Not a replacement for Higgsfield |
| Grok `/imagine` | Quick still, no pack | built into Grok Build | Exact UI letters → HTML, not Imagine |

Higgsfield skill names (upstream v0.12): `higgsfield-generate` · `higgsfield-soul-id` · `higgsfield-product-photoshoot` · `higgsfield-brandkit` · `higgsfield-marketplace-cards` · `higgsfield-websites` · `higgsfield-video-explainer` · `higgsfield-youtube-thumbnail` · `higgsfield-game-generation`.

## Documents, data, auth, browser

| Pack | When | Install |
|---|---|---|
| anthropics `pdf` `docx` `xlsx` `pptx` | Office files | `npx skills add anthropics/skills --skill pdf` (repeat for `docx` / `xlsx` / `pptx`) |
| [supabase/agent-skills](https://github.com/supabase/agent-skills) [![★](https://img.shields.io/github/stars/supabase/agent-skills)](https://github.com/supabase/agent-skills) | Postgres / Supabase | `npx skills add supabase/agent-skills` |
| [better-auth/skills](https://github.com/better-auth/skills) [![★](https://img.shields.io/github/stars/better-auth/skills)](https://github.com/better-auth/skills) | Auth | `npx skills add better-auth/skills` |
| [vercel-labs/agent-browser](https://github.com/vercel-labs/agent-browser) [![★](https://img.shields.io/github/stars/vercel-labs/agent-browser)](https://github.com/vercel-labs/agent-browser) | Drive a real browser | `npx skills add vercel-labs/agent-browser` |

## Catalogs, not loadouts

| Repo | Why it is listed | Do not |
|---|---|---|
| [affaan-m/ECC](https://github.com/affaan-m/ECC) [![★](https://img.shields.io/github/stars/affaan-m/ECC)](https://github.com/affaan-m/ECC) | Huge Claude library | Dump 292 skills into `.grok/` |
| [MengTo/Skills](https://github.com/MengTo/Skills) [![★](https://img.shields.io/github/stars/MengTo/Skills)](https://github.com/MengTo/Skills) | Motion / Three / UI techniques | Install the whole tree |
| TypeUI `design-*` (67) | Named visual worlds | Install all 67 |
| [shanraisshan/claude-code-best-practice](https://github.com/shanraisshan/claude-code-best-practice) [![★](https://img.shields.io/github/stars/shanraisshan/claude-code-best-practice)](https://github.com/shanraisshan/claude-code-best-practice) | Course shape we borrowed | Treat as Grok docs |

## After any install

Grok Build: `grok inspect`. Claude/Codex: list `skills/` (and `.claude/skills` / `.agents/skills`). Colliding names get messy — inspect beats guessing.
