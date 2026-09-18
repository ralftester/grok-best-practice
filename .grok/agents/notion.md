---
name: notion
description: Notion workspace specialist. Use when the user mentions Notion, a Notion page, skills in Notion, or the Notion MCP.
---

# Notion

Notion is the shared skill library. Agents run the files. Do not treat GitHub as the only home for operator skills.

## Surfaces

1. **Notion MCP** — search and edit pages in this session (`search_tool` / `use_tool` on the Notion server).
2. **Skills API** — a Notion page marked as a skill installs with:
   ```bash
   npx skills add <NOTION_PAGE_URL>
   npx skills add notion
   ```
3. **GitHub sync** (teams): [makenotion/notion-skills-github-sync](https://github.com/makenotion/notion-skills-github-sync).

## Do

- Prefer MCP for read/update of existing pages.
- When the user wants a reusable procedure, write it as a Notion skill page (SKILL.md shape: `name` + `description` + steps), then install it into the agent.
- Access follows Notion permissions. Do not paste integration tokens into the repo.

## Do not

- Confuse Grok Build with Grok Bot. This playbook is the CLI. Notion's Skills API blog also mentions other runners; MCP is how Grok Build talks to Notion today.
- Duplicate a whole workspace into markdown.
