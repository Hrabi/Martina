---
id: T-P001-02-02
parent_plan: P-001
parent_task: T-P001-02
owner: coordinator
created: 2026-09-04
updated: 2026-09-04
depends_on:
  - T-P001-02-01
owned_paths:
  - analysis/
  - sources/searches/
  - sources/records/
  - sources/library.bib
  - sources/evidence-matrix.md
  - project-brief.md
  - workflow/tasks/20-prepared/T-P001-02-confirm-topic-feasibility.md
---

# T-P001-02-02 – Znovu posoudit observační témata pro dvouměsíční sběr

## Důvod přímého zahájení

Uživatel upřesnil pevné podmínky: původní digitální téma je opuštěno, sběr u hospitalizovaných geriatrických pacientů může trvat nejvýše dva měsíce a nesmí měnit denní režim oddělení. Jde o dostatečně konkrétní zadání pro rozhodovací analýzu.

## Očekávaný výstup

- Srovnání proveditelných neintervenčních témat v českém nemocničním prostředí.
- Doporučení hlavní a záložní varianty s přesnou otázkou, populací, měřením, analýzou, zátěží a riziky.
- Jasné vyřazení témat, která nelze bezpečně uskutečnit za dva měsíce nebo bez změny provozu.

## Akceptační kritéria

- [x] Varianty respektují maximálně dva měsíce prospektivního sběru a nemění péči.
- [x] Doporučení rozlišuje rutinní data, krátké výzkumné měření a denní kontakt s pacientem.
- [x] U každé hlavní varianty jsou uvedeny výsledek, prediktory, minimální data, zátěž a metodické riziko.
- [x] Aktuálnost a zdrojová základna jsou doloženy současnými zdroji.
- [x] Je uvedeno, co musí schválit nemocnice a etická komise.

## Ověření

- Reprodukovatelná orientační rešerše, návaznost citekey, kontrola metodické proveditelnosti a soukromí.

## Handoff

- Doporučená první varianta: opakované krátké hodnocení subjektivní kvality spánku u pacientů 65+ na interně, chirurgii a LDN.
- Klinicky nejsilnější záloha: funkční pokles během pobytu na akutních odděleních; LDN není vhodná jako prostá kontrolní skupina.
- Varianta nejlépe propojující akutní a následnou péči: audit úplnosti a konzistence ošetřovatelských informací při překladu.
- Intervenční mobilizační protokol a původní digitální téma byly vyřazeny, protože neodpovídají aktuálním podmínkám uživatele.
- Před volbou je nutné získat šest agregovaných provozních údajů uvedených v analýze a předběžné stanovisko nemocnice, etické komise a konzultanta.
- Změněné soubory: `analysis/vyber-neintervencniho-tematu-dva-mesice.md`, `analysis/rozhodovaci-analyza-tematu-2026.md`, `project-brief.md`, `sources/searches/2026-09-04-observacni-temata-dva-mesice.md`, osm záznamů v `sources/records/`, `sources/library.bib`, `sources/evidence-matrix.md` a nadřazený task `T-P001-02`.
- Ověření: všechny citekey z analýzy existují v bibliografii; bibliografie má vyvážené závorky; kontrola osobních e-mailů v nových výstupech byla bez nálezu; `git diff --check` nehlásí chyby obsahu.
