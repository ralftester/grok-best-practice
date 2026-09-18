# Słownik

Krótko. Jak ktoś z ekipy tłumaczy nowej osobie.

| Słowo | Co to jest | Po co |
|---|---|---|
| **Grok Build** | Program `grok` w terminalu. Agent, który czyta pliki i może je zmieniać. | Kod, docs, skille. **Nie** czat na grok.com. |
| **Grok Bot** | Inny produkt (chmura / maszyna w przeglądarce). | Świadomie go tu nie uczymy. |
| **Agent** | Model z narzędziami (czyta, pisze, odpala komendy). | Żeby nie klepać samego czatu. |
| **Harness** | Program, w którym ten agent siedzi: Grok Build, Claude Code, Codex, Cursor. | Ten sam `SKILL.md` może iść w kilka harnessów. |
| **Skill** | Folder z plikiem `SKILL.md`: *co robię* i *kiedy mnie brać*. | Powtarzalna instrukcja, bez wklejania za każdym razem. |
| **Paczka** | Wiele skilli z jednego repo. | `npx skills add owner/repo` — jedna komenda. |
| **Loadout** | Mały zestaw paczek na co dzień, nie całe internet. | [catalog/loadout.md](../catalog/loadout.md) |
| **Specjalista** | Agent w tym repo: `design`, `marketing`, `higgsfield`, `notion`. | Jedna robota, jeden typ. Główny czat zostaje szefem. |
| **AGENTS.md** | Kontrakt dla *każdego* agenta w tym repo. | Claude czyta to samo przez `CLAUDE.md` (alias). |
| **Inspect** | Rozglądanie się: jakie skille, hooki, MCP, kolizje nazw. | Grok: `grok inspect`. Inni: lista `skills/`. |
| **Plan Mode** | Na Grok: najpierw plan, edycja plików za bramką. | Bash i dziecko-agent **nie** są tą samą bramką. |
| **Hook** | Skrypt przy narzędziu (np. zanim poleci niebezpieczna komenda). | Na Grok hooki są *fail-open*: crash ≠ stop. |
| **MCP** | Wtyczka do obcego serwisu (Notion, Higgsfield) w tej samej sesji. | Agent woła narzędzia, nie wklejasz haseł do gita. |
| **Notion (tu)** | Szafka na skille zespołu. | Piszesz stronę → `npx skills add <url>` → agent ją ładuje. |
| **Higgsfield** | Obraz, wideo, ads, twarz Soul. | Prompt w agencie, job na CLI/MCP. Nie `curl` do ich API. |
| **`npx skills add`** | Instalator skilli ze [skills.sh](https://skills.sh) / GitHuba. | Wpisuje pliki tam, gdzie harness je widzi. |
| **Kolizja nazw** | Dwa skille nazywają się tak samo. | Grok dokleja prefiks. Najpierw inspect, nie zgadywanie. |

Nie myl **paczki** (cudze instrukcje) z **tym git repo** (mapa + dwa nasze skille). Cudzych drzew tu nie kopiujemy.
