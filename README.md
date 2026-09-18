**Language:** **English** · [Polski](README.pl.md)

<p align="center">
  <img src="docs/assets/banner-1280x640.png" width="800" alt="grok-best-practice" />
</p>

<p align="center">
  <a href="https://github.com/ralftester/grok-best-practice/stargazers"><img src="https://img.shields.io/github/stars/ralftester/grok-best-practice?style=flat&label=%E2%98%85&labelColor=111&color=1d9bf0" alt="Stars" /></a>
  <img src="https://img.shields.io/github/last-commit/ralftester/grok-best-practice" alt="Last commit" />
  <img src="https://img.shields.io/badge/license-CC%20BY%204.0-lightgrey" alt="License" />
  <img src="https://img.shields.io/badge/status-unofficial-lightgrey" alt="Unofficial" />
  <a href="https://x.ai/cli"><img src="https://img.shields.io/badge/Grok_Build-best_practice-1d9bf0" alt="Grok Build" /></a>
  <a href="README.md"><img src="https://img.shields.io/badge/lang-EN-blue" alt="English" /></a>
  <a href="README.pl.md"><img src="https://img.shields.io/badge/lang-PL-red" alt="Polish" /></a>
</p>

# grok-best-practice

**from vibe coding to agentic engineering on Grok Build**

A living course and ecosystem map for xAI’s terminal coding agent. Skills, plugins, hooks, `AGENTS.md`, `grok inspect`, Plan Mode, headless, ACP.

> Independent community playbook. Not affiliated with xAI. **Grok Build ≠ Grok Bot ≠ grok.com chat.**

## How to use

```bash
curl -fsSL https://x.ai/cli/install.sh | bash   # macOS / Linux
# irm https://x.ai/cli/install.ps1 | iex        # Windows PowerShell

cd your-project
grok inspect
grok plugin install superpowers@xai-official --trust
grok
```

In the TUI: `Use inspect-and-ship. Do not edit yet.`

Read this repo as a course. Install one playbook at a time. Do not dump 292 skills into `.grok/`.

## Contents

- [Concepts](#concepts)
- [Grok Build vs Claude Code vs Cursor](#grok-build-vs-claude-code-vs-cursor)
- [Workflows](#workflows)
- [Community](#community)
- [Caveats](#caveats)
- [Tips](#tips)
- [Contributing](#contributing)

## Concepts

| Feature | Location | Notes |
|---------|----------|--------|
| Instructions | `AGENTS.md`, `.grok/rules/` | Also loads `CLAUDE.md` as compat. Deeper path wins. |
| Skills | `.grok/skills/<name>/SKILL.md`, `~/.grok/skills/` | [best-practice/grok-skills.md](best-practice/grok-skills.md) |
| Plugins | `/marketplace`, `grok plugin install …` | [best-practice/grok-plugins.md](best-practice/grok-plugins.md) |
| Hooks | `.grok/hooks/`, `/hooks-trust` | Fail-open. [best-practice/grok-hooks.md](best-practice/grok-hooks.md) |
| Ignore | `.grokignore` | Plus gitignore-skipped instruction files. |
| Inspect | `grok inspect` / `--json` | [best-practice/grok-inspect.md](best-practice/grok-inspect.md) |
| Plan Mode | `/plan`, Shift+Tab | File-edit gate. Bash is not blocked. [plan](best-practice/grok-plan-mode.md) |
| Subagents | `.grok/agents/`, worktrees | [best-practice/grok-agents.md](best-practice/grok-agents.md) |
| Headless | `grok -p` | [best-practice/grok-headless.md](best-practice/grok-headless.md) |
| ACP | `grok agent stdio` | IDE / web UIs attach here. |
| Imagine | `/imagine`, `/imagine-video` | Native. Not a plugin. |
| Memory | `/memory`, `/flush` | GA as of CLI 1.0.34. |
| Demo skill | [inspect-and-ship](.grok/skills/inspect-and-ship/SKILL.md) | First session in this repo. |

<p align="center">
  <img src="docs/assets/compare-strip.png" width="800" alt="Grok Build vs Claude Code vs Cursor" />
</p>

## Grok Build vs Claude Code vs Cursor

Checked 2026-09-17 against [docs.x.ai/build](https://docs.x.ai/build/overview) and public repos. Not a dunk table.

| | **Grok Build** | **Claude Code** | **Cursor** |
|---|---|---|---|
| Form | Rust TUI, open harness | Closed CLI | IDE + agents |
| Model | grok-4.6 + BYO | Anthropic-first | Mixed; Grok Bot is a different product |
| Skills | `SKILL.md`; **`allowed-tools` does not restrict tools** | `SKILL.md`; allowed-tools enforced | Rules / plugins |
| Plan | Edit-gate on the plan file; bash/subagents leak | Plan + permissions | Agent in the editor |
| Inspect | `grok inspect` | No dump | Settings UI |
| IDE | ACP first-class | Own protocol | Native |
| Unique | Inspect, ACP, imagine, X search, BYO | Marketplace size, eval culture | Editor UX, Grok Bot VMs |
| This repo | Yes | Pointers | Pointers; Bot ≠ Build |

**Do not say “drop-in Claude.”** Grok will *read* `.claude/skills`. It will not copy Claude’s security model.

## Workflows

Peer playbooks, live star badges. Grok-shaped install when it exists.

See the full table: [catalog/workflows.md](catalog/workflows.md).

| Playbook | ★ | On Grok |
|---|---|---|
| [Superpowers](https://github.com/obra/superpowers) | [![★](https://img.shields.io/github/stars/obra/superpowers)](https://github.com/obra/superpowers) | `grok plugin install superpowers@xai-official --trust` |
| [Matt Pocock Skills](https://github.com/mattpocock/skills) | [![★](https://img.shields.io/github/stars/mattpocock/skills)](https://github.com/mattpocock/skills) | `npx skills add mattpocock/skills` then `grok inspect` |
| [Addy Osmani agent-skills](https://github.com/addyosmani/agent-skills) | [![★](https://img.shields.io/github/stars/addyosmani/agent-skills)](https://github.com/addyosmani/agent-skills) | `npx skills add addyosmani/agent-skills` |
| [Spec Kit](https://github.com/github/spec-kit) | [![★](https://img.shields.io/github/stars/github/spec-kit)](https://github.com/github/spec-kit) | `uv tool install specify-cli` |
| [anthropics/skills](https://github.com/anthropics/skills) | [![★](https://img.shields.io/github/stars/anthropics/skills)](https://github.com/anthropics/skills) | Compat loader |
| [xai-org/grok-build](https://github.com/xai-org/grok-build) | [![★](https://img.shields.io/github/stars/xai-org/grok-build)](https://github.com/xai-org/grok-build) | Official CLI |

## Community

Only entries that talk to official `grok`. Full list: [catalog/community.md](catalog/community.md).

- [xai-org/grok-build](https://github.com/xai-org/grok-build) — harness.
- [DominikTobureto/awesome-grok-build](https://github.com/DominikTobureto/awesome-grok-build) — starter kit (last push 2026-08-23; credit it, CLI has moved).
- [xintaofei/codeg](https://github.com/xintaofei/codeg) — GUI over ACP.
- [farion1231/cc-switch](https://github.com/farion1231/cc-switch) — multi-CLI switcher.
- [kenryu42/cc-safety-net](https://github.com/kenryu42/cc-safety-net) — PreToolUse guard.
- [superagent-ai/grok-cli](https://github.com/superagent-ai/grok-cli) — **unofficial** API agent. Different binary.

Grok Bot lives in [ZeroPointRepo/awesome-grok-bot](https://github.com/ZeroPointRepo/awesome-grok-bot). Different product.

## Caveats

1. `allowed-tools` in SKILL.md is not a security boundary.
2. Plan Mode does not block bash.
3. Hooks fail-open (crash → tool still runs).
4. Skill `model` / `effort` fields are ignored.
5. Official harness does not take public PRs. Use `/feedback`.
6. LifeJiggy-style YAML/`GROK.md` dumps do not load. Grok workflows are `.rhai`.

## Tips

Sourced. Not “pro tips”.

1. `grok inspect` before you debug a missing skill. ([inspect](best-practice/grok-inspect.md))
2. Trust project hooks with `/hooks-trust`, not by hoping SKILL.md will sandbox you. ([hooks](best-practice/grok-hooks.md))
3. Install Superpowers from the xAI marketplace, then inspect again. ([plugins](best-practice/grok-plugins.md))
4. Headless CI: `grok -p` + `--no-auto-update`. Do not put keys on the argv. ([headless](best-practice/grok-headless.md))
5. One playbook per week. ECC’s 292 skills are a catalog, not a loadout. ([workflows](catalog/workflows.md))
6. Exact on-screen text belongs in HTML/code, not `/imagine`. Native imagine is for pictures.
7. Polish readers: [README.pl.md](README.pl.md). Product names stay English.

## Contributing

[CONTRIBUTING.md](CONTRIBUTING.md). New rows must be Grok Build, sourced, no invented stars.

## License

List and docs: [CC BY 4.0](LICENSE). Unofficial.

If this saved you a setup day, [star the repo](https://github.com/ralftester/grok-best-practice/stargazers). That is the only ranking signal we ask for.

[![Star History Chart](https://api.star-history.com/svg?repos=ralftester/grok-best-practice&type=Date)](https://www.star-history.com/#ralftester/grok-best-practice&Date)
