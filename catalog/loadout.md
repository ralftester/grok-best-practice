# Daily loadout

Install these packs. Stars are live Shields. Checked 2026-09-18.

This repo does **not** vendor the pack bodies. Agents load them from the skill dirs `npx skills` writes.

## Install once

```bash
grok plugin install superpowers@xai-official --trust

npx skills add pbakaus/impeccable
npx skills add nextlevelbuilder/ui-ux-pro-max-skill
npx skills add vercel-labs/agent-skills --skill web-design-guidelines
npx skills add anthropics/skills --skill frontend-design

npx skills add coreyhaines31/marketingskills

npx skills add higgsfield-ai/skills

npx skills add notion
```

Then:

```bash
grok inspect
```

MCP (already used with this playbook):

- Notion: `https://mcp.notion.com/mcp`
- Higgsfield: `https://mcp.higgsfield.ai/mcp`

Do not put tokens in the repo. Auth is local.

## Packs

| Job | Pack | ★ | Install |
|---|---|---|---|
| Methodology | [obra/superpowers](https://github.com/obra/superpowers) | [![★](https://img.shields.io/github/stars/obra/superpowers)](https://github.com/obra/superpowers) | `grok plugin install superpowers@xai-official --trust` |
| UI polish | [pbakaus/impeccable](https://github.com/pbakaus/impeccable) | [![★](https://img.shields.io/github/stars/pbakaus/impeccable)](https://github.com/pbakaus/impeccable) | `npx skills add pbakaus/impeccable` |
| UI intelligence | [ui-ux-pro-max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | [![★](https://img.shields.io/github/stars/nextlevelbuilder/ui-ux-pro-max-skill)](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | `npx skills add nextlevelbuilder/ui-ux-pro-max-skill` |
| UI review | [vercel-labs/agent-skills](https://github.com/vercel-labs/agent-skills) | [![★](https://img.shields.io/github/stars/vercel-labs/agent-skills)](https://github.com/vercel-labs/agent-skills) | `--skill web-design-guidelines` |
| Frontend craft | [anthropics/skills](https://github.com/anthropics/skills) | [![★](https://img.shields.io/github/stars/anthropics/skills)](https://github.com/anthropics/skills) | `--skill frontend-design` |
| Marketing | [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) | [![★](https://img.shields.io/github/stars/coreyhaines31/marketingskills)](https://github.com/coreyhaines31/marketingskills) | `npx skills add coreyhaines31/marketingskills` |
| Image / video / ads | [higgsfield-ai/skills](https://github.com/higgsfield-ai/skills) | [![★](https://img.shields.io/github/stars/higgsfield-ai/skills)](https://github.com/higgsfield-ai/skills) | `npx skills add higgsfield-ai/skills` |
| Notion library | [Notion Skills API](https://developers.notion.com/guides/agent-skills/overview) | — | `npx skills add notion` |
| Notion → git | [makenotion/notion-skills-github-sync](https://github.com/makenotion/notion-skills-github-sync) | [![★](https://img.shields.io/github/stars/makenotion/notion-skills-github-sync)](https://github.com/makenotion/notion-skills-github-sync) | team sync, optional |

## Higgsfield skills (from upstream README, v0.12)

`higgsfield-generate` · `higgsfield-soul-id` · `higgsfield-product-photoshoot` · `higgsfield-brandkit` · `higgsfield-marketplace-cards` · `higgsfield-websites` · `higgsfield-video-explainer` · `higgsfield-youtube-thumbnail` · `higgsfield-game-generation`

CLI: `curl -fsSL https://raw.githubusercontent.com/higgsfield-ai/cli/main/install.sh | sh` then `higgsfield auth login`.

## Marketing — start small

`product-marketing` first, then one of `copywriting` · `cro` · `seo-audit` · `social` · `launch` · `ad-creative`. The pack has many more; do not load them all.

## Skip unless named

- Full [MengTo/Skills](https://github.com/MengTo/Skills) tree — one skill if the user named it.
- 67 TypeUI `design-*` slugs — one style if named.
- ECC 292 — catalog, not a loadout.

## Agents in this repo

`.grok/agents/design.md` · `marketing.md` · `higgsfield.md` · `notion.md`
