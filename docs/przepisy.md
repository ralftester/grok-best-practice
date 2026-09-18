# Przepisy

Krok po kroku. Wklejasz zdanie w cudzysłowie. Jeden specjalista na przepis.

Mapa sytuacji: [kiedy-czego-uzyc.md](kiedy-czego-uzyc.md). Paczki: [catalog/library.md](../catalog/library.md).

## 1. Pierwszy wieczór

1. `curl -fsSL https://x.ai/cli/install.sh | bash`
2. `cd twoj-projekt` potem `grok`
3. Napisz: `Use inspect-and-ship. Do not edit yet.`
4. Poczekaj na blok Bottom line / Inspect / Change / Residual.
5. Jak brakuje paczek: `Install the daily skill packs.` (skill `loadout`)
6. Znowu inspect (Grok: `grok inspect`).

Nie proś jeszcze o „zrób całą apkę”.

## 2. Landing: najpierw oferta, potem wygląd

1. `Spawn marketing. Write homepage copy. Use product-marketing first. Don’t invent metrics.`
2. Jak tekst jest OK: `Spawn design. Build the landing from this copy. Anti-slop. Desktop and phone.`
3. Dokładny napis na grafice: HTML/CSS, nie Higgsfield i nie `/imagine`.

Marketing nie renderuje filmu. Design nie wymyśla oferty.

## 3. Reklama wideo (Higgsfield)

1. `Spawn marketing. One-sentence offer + 15s voiceover. No fake testimonials.`
2. `Spawn higgsfield. Seedance 16:9 ad from that script. Preflight cost before generate.`
3. CLI: `higgsfield auth login` jeśli jeszcze nie. Nie wklejaj tokenu do repo.

Twarz „zawsze ta sama”: najpierw Soul (`higgsfield-soul-id`), potem generate z `reference_id`.

## 4. Instrukcja w Notion, odpalana tutaj

1. W Notion: strona z nazwą, „kiedy używać”, krokami (kształt `SKILL.md`).
2. `Spawn notion. Install this page as a skill.` (albo sam: `npx skills add <URL>`)
3. W nowej sesji: powiedz agentowi **kiedy** ma tę instrukcję wziąć, tak jak w `description`.

Notion = szafka. Agent = ręce. Hasła Notion nie idą do gita.

## 5. Grafika z dokładnym tekstem

1. Nie `/imagine` i nie Seedance — litery rozjadą się.
2. `Make a self-contained HTML page with this exact headline: "…". Then render PNG.`
3. W tym playbooku tak powstał baner (`docs/assets/banner.html`).

`/imagine` zostaw na luźny obrazek bez UI-copy.

## 6. Wolny React / Next

1. Paczka: `npx skills add vercel-labs/agent-skills --skill vercel-react-best-practices`
2. `Apply vercel-react-best-practices to this page. Don’t rewrite the whole app.`
3. Inspect, czy skill w ogóle wpadł na listę.

## 7. PDF albo Word

1. `npx skills add anthropics/skills --skill pdf` (albo `docx` / `xlsx` / `pptx`)
2. `Fill this PDF.` / `Edit this .docx. Keep headings.`
3. Na pierwszym razie skill może doinstalować swoje narzędzia Pythona — to normalne.

## 8. Literówka, bez festiwalu

`Fix the typo on line 3 of README.md. No other files.`

Bez `design`, bez Higgsfield, bez marketingu. Eval #9 w [examples/eval-routing.md](../examples/eval-routing.md).

## Kolejność na tydzień

| Kiedy | Co |
|---|---|
| Dzień 1 | Przepis 1 (inspect) |
| Dzień 2 | Daily loadout + znowu inspect |
| Dzień 3 | Jeden przepis 2–7, **jeden** specjalista |
| Później | `npx skills find …` albo [skills.sh](https://skills.sh) — nie ECC na raz |
