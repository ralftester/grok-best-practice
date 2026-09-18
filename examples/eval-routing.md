# Routing eval

Ten prompts. Expected skill or agent — not quality theatre.

Run them in a fresh session. After each: which skill/agent did you load? Compare to **Must**.

| # | Prompt | Must | Must not |
|---|---|---|---|
| 1 | `Use inspect-and-ship. Do not edit yet.` | `inspect-and-ship` | `higgsfield`, `marketing` |
| 2 | `What should I do first in this repo?` | `inspect-and-ship` | generating video |
| 3 | `Install the daily skill packs.` | `loadout` | cloning Meng To / ECC |
| 4 | `Polish this landing page UI. Anti-slop.` | agent `design` | `higgsfield` as primary |
| 5 | `Write homepage copy for this playbook.` | agent `marketing` | `higgsfield` |
| 6 | `Generate a Seedance 16:9 ad video in Higgsfield.` | agent `higgsfield` | `/imagine` as the only path |
| 7 | `Train a Soul ID from these face photos.` | agent `higgsfield` (`higgsfield-soul-id`) | `notion` |
| 8 | `Turn this procedure into a Notion skill and install it.` | agent `notion` | committing a Notion token |
| 9 | `Fix the typo on line 3 of README.md.` | no specialist; tiny edit | `higgsfield`, `marketing`, `design` |
| 10 | `How many GitHub stars does Superpowers have? Live badge only.` | no invented number; Shields already in README | hardcoded star count |

Pass: 10/10 Must, 0 Must-not hits.

Harness: Grok, Claude, and Codex should agree on Must. Discovery still follows `inspect-and-ship` (Grok uses `grok inspect`; the others list `skills/`).
