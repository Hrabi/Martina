# Rigorózní práce v ošetřovatelství

Pracovní prostor pro přípravu rigorózní práce: od potvrzení zadání přes rešerši, metodiku a rukopis až po kontrolovaný export do univerzitního formátu.

## Hlavní rozcestník

- [`project-brief.md`](project-brief.md) – schválené zadání, pracovní téma, rozhodnutí a otevřené otázky
- [`requirements/`](requirements/) – anonymizované institucionální a exportní požadavky
- [`workflow/`](workflow/) – implementační plány, tasky, stavové fronty a šablony
- [`drafts/`](drafts/) – Markdown wiki rukopisu a pořadí exportu
- [`sources/`](sources/) – rešerše, záznamy zdrojů, evidence a bibliografie
- [`export/`](export/) – exportní konfigurace, šablony a reprodukovatelný postup
- `exports/` – lokální generované DOCX/PDF; složka je ignorována Gitem
- `private/` – citlivé podklady pouze lokálně; složka je ignorována Gitem
- [`AGENTS.md`](AGENTS.md) – závazná pravidla pro práci Codexu a paralelních agentů

## Pracovní princip

1. Potvrdit zadání a rozhodnutí v `project-brief.md`.
2. Připravit plán a tasky ve `workflow/`.
3. Zpracovat a ověřit zdroje v `sources/`.
4. Psát jednotlivé sekce jako stabilní Markdown podstránky v `drafts/`.
5. Integrovat a kontrolovat rukopis podle `drafts/_manuscript.yml`.
6. Generovat DOCX/PDF do `exports/`; zdrojový Markdown zůstává kanonický.

Obsah sledovaný Gitem je nutné považovat za veřejný. Soukromé zprávy, kontakty, zdravotní údaje a surová výzkumná data se do repozitáře neukládají.
