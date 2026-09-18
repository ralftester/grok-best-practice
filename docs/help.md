# Help

Inspect first. Then this list. Don’t add 200 skills “just in case”.

## The skill never fires

1. Is it on disk? Grok: `grok inspect`. Claude/Codex: `skills/` or `.claude/skills` / `.agents/skills`.
2. Does YAML `name` match the folder name?
3. Does `description` say **when** — not **how**? A full procedure in the description often means the body never loads.
4. Name collision? Inspect shows a prefix.
5. Did the session start *after* install? Skills are snapshotted at startup.

Eval: [examples/eval-routing.md](../examples/eval-routing.md).

## `npx skills add` ran, Grok sees nothing

The CLI often writes `.agents/skills/` or `.claude/skills/`. Grok **does** scan those, but:

- run `grok inspect` in **this** project directory,
- or pass `-a` for your harness to `npx skills add`,
- or install again targeting the right agent.

Don’t hand-copy a pack into this playbook’s `skills/` (that folder is only our two skills).

## The agent does too much

Say it: `One specialist only: design.` / `Fix this typo. No other files.`

The main chat stays in charge. Recipe 8.

## Plan Mode, but bash still runs

That’s how Grok is built. Plan gates **edits to the plan file**, not the terminal. A child agent is not a sandbox either. See [best-practice/grok-plan-mode.md](../best-practice/grok-plan-mode.md).

## The hook “should have blocked” and the command ran

On Grok, hooks are fail-open: crash or timeout ≠ stop. Trust them with `/hooks-trust`. `allowed-tools` in SKILL.md does **not** close tools here. On Claude Code, `allowed-tools` *is* a gate — don’t mix the two.

## Higgsfield burned credits / wrong picture

- Preflight: `higgsfield model get <id>` and `higgsfield generate cost …` (or MCP `get_cost`).
- Don’t `curl api.higgsfield.ai`.
- Exact UI text → HTML, not generate.
- Train Soul once; prompting with `reference_id` is the second step.

## Notion 401 / empty skill list

- MCP and `npx skills add notion` are two doors. Both need your login, not a secret in git.
- You only see pages the connection can read.
- Grok Build ≠ Grok Bot. MCP is the CLI path.

## Stars / “trending #1”

This repo only uses live Shields. Don’t type a number. “How many stars does Superpowers have?” = the badge, not a guess (eval #10).

## Too many packs, the session gets dumb

Uninstall what you aren’t using today. The daily set is small on purpose. ECC and the full Meng To tree stay on the shelf, not in startup.
