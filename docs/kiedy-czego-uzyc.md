# Kiedy czego użyć

Na ludzki język. Nie musisz znać Claude’a, Codexu ani wnętrzności Groka.

Dalej: [słownik](slownik.md) · [przepisy](przepisy.md) · [gdy coś nie gra](gdy-nie-gra.md) · [indeks](README.md)

**Skill** to krótka instrukcja (`SKILL.md`), którą agent czyta, gdy robota do niej pasuje. **Paczka** to zestaw takich instrukcji — instalujesz jedną komendą. **Agent** w tym repo to specjalista: `design`, `marketing`, `higgsfield`, `notion`.

Instalujesz paczki. Nie kopiujesz dwustu folderów do gita. Potem ten sam plik widzi Grok, Claude i Codex.

Pełna tabela: [catalog/library.md](../catalog/library.md). Minimum na co dzień: [catalog/loadout.md](../catalog/loadout.md).

## Pięć minut

```bash
curl -fsSL https://x.ai/cli/install.sh | bash
cd your-project
grok
```

W czacie: `Use inspect-and-ship. Do not edit yet.`

Ten skill najpierw się rozgląda i czeka. Potem instalujesz paczki i bierzesz **jednego** specjalistę do konkretnej roboty.

## Sytuacje

| Chcę… | Bierz | Powiedz agentowi |
|---|---|---|
| Pierwszy raz otworzyć ten projekt | `inspect-and-ship` | `Use inspect-and-ship. Do not edit yet.` |
| Dołożyć zwykły zestaw paczek | `loadout` | `Install the daily skill packs.` |
| Żeby ekran nie wyglądał jak każdy inny AI-site | agent `design` + impeccable | `Polish this UI. Anti-slop.` |
| Tekst na stronę / posta / maila z premiery | agent `marketing` | `Write homepage copy. Use product-marketing first.` |
| Film produktowy, reklamę, twarz która się powtarza | agent `higgsfield` | `Generate a Seedance ad in Higgsfield.` |
| Trzymać instrukcje w Notion i odpalać je tutaj | agent `notion` | `Turn this into a Notion skill and install it.` |
| Poprawić literówkę | nikt extra | `Fix the typo on line 3 of README.md.` |
| Najpierw plan, potem kod | Superpowers | `Use Superpowers. Do not write code yet.` |
| Wolny React / Next.js | skille Vercel React | `Apply vercel-react-best-practices.` |
| PDF / Word / Excel / prezentację | skille dokumentów Anthropic | `Fill this PDF.` / `Edit this .docx.` |
| Wideo **w React** (kodem, klatka po klatce) | Remotion | `Use remotion-best-practices.` |
| Postgres / Supabase | supabase/agent-skills | `Review this schema.` |
| Logowanie / sesje | better-auth/skills | `Follow better-auth-best-practices.` |
| Znaleźć paczkę, której nie znam | find-skills | `Search skills.sh for X.` |
| Obrazek z dokładnym tekstem na UI | HTML/CSS, nie model wideo | `Render this as HTML, then PNG.` |
| Szybki obrazek, nie reklamę | Grok `/imagine` | `/imagine …` |

Grok Build to agent w terminalu (`grok`). Czat na grok.com i Grok Bot to **inny** produkt. Ten plik jest pod CLI i pod te same `SKILL.md`, które ładują też inne agenty.

## Który specjalista

| Agent | Kiedy | Nie wtedy |
|---|---|---|
| `design` | Układ, kolor, polish, „wygląda jak każdy AI-site” | Pisanie oferty (to `marketing`) |
| `marketing` | Słowa, SEO, konwersja, plan premiery | Render filmu reklamowego (to `higgsfield`) |
| `higgsfield` | Obraz/wideo/ads, Soul, zdjęcia produktu | Dokładne litery na screenie UI (zrób HTML) |
| `notion` | Strony i skille w workspace | Zrzut całego Notion do gita |

Jeden specjalista na robotę. Główny czat zostaje szefem.

## Notion, prosto

1. Napisz instrukcję jako stronę w Notion (nazwa, kiedy używać, kroki).
2. `npx skills add <url-tej-strony>` albo `npx skills add notion`.
3. Podłącz Notion MCP, żeby agent mógł czytać i poprawiać strony.

Ten sam skill odpalasz potem w Grok, Claude albo Codex. Notion jest szafką. Agent jest rękami.

## Tego nie wsypuj na raz

- Everything Claude Code (ECC) — setki plików. Katalog, nie zestaw startowy.
- Całe drzewo Meng To — jeden skill, jeśli go nazwałeś.
- 67 stylów TypeUI `design-*` — weź **jeden** wygląd.

Szukanie dalej: `npx skills find <słowa>` (po `find-skills`) albo [skills.sh](https://skills.sh).
