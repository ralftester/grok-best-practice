# When to use what

Plain map. You do not need to know Claude, Codex, or Grok internals.

A **skill** is a short instruction file (`SKILL.md`) the agent reads when the job matches. A **pack** is a bunch of skills you install with one command. An **agent** in this repo is a specialist (`design`, `marketing`, `higgsfield`, `notion`).

Install packs. Do not copy 200 folders into this git repo. After install, Grok, Claude, and Codex can all see the same files.

Full install table: [catalog/library.md](../catalog/library.md). Daily minimum: [catalog/loadout.md](../catalog/loadout.md).

## Five minutes

```bash
curl -fsSL https://x.ai/cli/install.sh | bash
cd your-project
grok
```

In the chat: `Use inspect-and-ship. Do not edit yet.`

That skill looks around, then waits. Next you install packs (below) and pick **one** specialist for the actual job.

## Situations

| I want to… | Use | Say to the agent |
|---|---|---|
| Open this project for the first time | `inspect-and-ship` | `Use inspect-and-ship. Do not edit yet.` |
| Install the usual packs | `loadout` | `Install the daily skill packs.` |
| Make a screen look less generic | agent `design` + impeccable | `Polish this UI. Anti-slop.` |
| Write a landing page / tweet / launch email | agent `marketing` | `Write homepage copy. Use product-marketing first.` |
| Make a product video, ad, or a face that stays consistent | agent `higgsfield` | `Generate a Seedance ad in Higgsfield.` |
| Keep team how-tos in Notion and run them here | agent `notion` | `Turn this into a Notion skill and install it.` |
| Fix a one-line typo | nobody extra | `Fix the typo on line 3 of README.md.` |
| Plan before coding | Superpowers | `Use Superpowers. Do not write code yet.` |
| React / Next.js that is slow | Vercel React skills | `Apply vercel-react-best-practices.` |
| Edit a PDF / Word / Excel / slides | Anthropic document skills | `Fill this PDF.` / `Edit this .docx.` |
| A video *in React* (programmatic) | Remotion | `Use remotion-best-practices.` |
| Postgres / Supabase | supabase/agent-skills | `Review this schema.` |
| Login / sessions | better-auth/skills | `Follow better-auth-best-practices.` |
| Find a pack I do not know | find-skills | `Search skills.sh for X.` |
| A picture with exact UI text | HTML/CSS, not a video model | `Render this as HTML, then PNG.` |
| A quick picture, not an ad | Grok `/imagine` | `/imagine …` |

Grok Build is the terminal agent (`grok`). Grok on grok.com / Grok Bot is a different product. This guide is for the CLI and for the same `SKILL.md` files other agents load.

## Which specialist

| Agent | When | Not when |
|---|---|---|
| `design` | Layout, color, polish, “it looks like every AI site” | Writing the sales offer (that is `marketing`) |
| `marketing` | Words, SEO, CRO, launch plan | Rendering the ad video (that is `higgsfield`) |
| `higgsfield` | Image/video/ads, Soul face, product shoot | Exact letters on a UI screenshot (use HTML) |
| `notion` | Pages and skills that live in the workspace | Dumping the whole workspace into git |

One specialist per job. The main chat stays in charge.

## Notion, simply

1. Write the how-to as a Notion page (skill shape: name, when to use, steps).
2. `npx skills add <that-page-url>` or `npx skills add notion`.
3. Connect Notion MCP so the agent can read/edit pages.

Same skill file then runs in Grok, Claude, or Codex. Notion is the library. The agent is the hands.

## Do not install in one go

- Everything Claude Code (ECC) — hundreds of files. Catalog, not a starter kit.
- The whole Meng To tree — one skill if you named it.
- 67 TypeUI `design-*` styles — pick **one** look.

Search more packs: `npx skills find <words>` (after `find-skills`) or [skills.sh](https://skills.sh).
