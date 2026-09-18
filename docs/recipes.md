# Recipes

Step by step. Paste the quoted line. One specialist per recipe.

Situation map: [when-to-use.md](when-to-use.md). Packs: [catalog/library.md](../catalog/library.md).

## 1. First evening

1. `curl -fsSL https://x.ai/cli/install.sh | bash`
2. `cd your-project` then `grok`
3. Type: `Use inspect-and-ship. Do not edit yet.`
4. Wait for Bottom line / Inspect / Change / Residual.
5. If packs are missing: `Install the daily skill packs.` (`loadout`)
6. Inspect again (Grok: `grok inspect`).

Don’t ask for “build the whole app” yet.

## 2. Landing: offer first, look second

1. `Spawn marketing. Write homepage copy. Use product-marketing first. Don’t invent metrics.`
2. When the copy is OK: `Spawn design. Build the landing from this copy. Anti-slop. Desktop and phone.`
3. Exact letters on a graphic: HTML/CSS, not Higgsfield, not `/imagine`.

Marketing does not render the video. Design does not invent the offer.

## 3. Ad video (Higgsfield)

1. `Spawn marketing. One-sentence offer + 15s voiceover. No fake testimonials.`
2. `Spawn higgsfield. Seedance 16:9 ad from that script. Preflight cost before generate.`
3. CLI: `higgsfield auth login` if needed. Don’t commit the token.

Same face every time: train Soul (`higgsfield-soul-id`), then generate with `reference_id`.

## 4. How-to in Notion, run here

1. In Notion: a page with a name, “when to use”, and steps (`SKILL.md` shape).
2. `Spawn notion. Install this page as a skill.` (or yourself: `npx skills add <URL>`)
3. In a new session, tell the agent **when** to pick it, the same way a `description` would.

Notion is the shelf. The agent is the hands. Notion secrets stay out of git.

## 5. Graphic with exact text

1. Not `/imagine`, not Seedance — letters will drift.
2. `Make a self-contained HTML page with this exact headline: "…". Then render PNG.`
3. This playbook’s banner was made that way (`docs/assets/banner.html`).

Leave `/imagine` for a loose picture with no UI copy.

## 6. Slow React / Next

1. Pack: `npx skills add vercel-labs/agent-skills --skill vercel-react-best-practices`
2. `Apply vercel-react-best-practices to this page. Don’t rewrite the whole app.`
3. Inspect so you know the skill actually loaded.

## 7. PDF or Word

1. `npx skills add anthropics/skills --skill pdf` (or `docx` / `xlsx` / `pptx`)
2. `Fill this PDF.` / `Edit this .docx. Keep headings.`
3. First run may install Python tooling. That’s expected.

## 8. Typo, no festival

`Fix the typo on line 3 of README.md. No other files.`

No `design`, no Higgsfield, no marketing. Eval #9 in [examples/eval-routing.md](../examples/eval-routing.md).

## A week

| When | What |
|---|---|
| Day 1 | Recipe 1 (inspect) |
| Day 2 | Daily loadout + inspect again |
| Day 3 | One recipe 2–7, **one** specialist |
| Later | `npx skills find …` or [skills.sh](https://skills.sh) — not all of ECC at once |
