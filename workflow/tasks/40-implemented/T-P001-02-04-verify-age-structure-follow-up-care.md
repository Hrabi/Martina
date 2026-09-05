---
id: T-P001-02-04
parent_plan: P-001
parent_task: T-P001-02
owner: coordinator
created: 2026-09-04
updated: 2026-09-04
depends_on:
  - T-P001-02-03
owned_paths:
  - analysis/overeni-vekove-struktury-nasledne-pece.md
  - sources/searches/2026-09-04-vek-pacientu-nasledna-pece.md
  - sources/records/csu2025seniori-nasledna-pece.md
  - sources/records/uzis2024nasledna-open-data.md
  - sources/library.bib
  - sources/evidence-matrix.md
  - project-brief.md
---

# T-P001-02-04 – Ověřit věkovou strukturu následné péče

## Důvod přímého zahájení

Uživatel požádal o ověření procenta pacientů starších 60 let na LDN jako podkladu pro obhajobu věkového kritéria. Jde o ohraničenou rešeršní a výpočetní kontrolu navazující na preferované téma.

## Očekávaný výstup

- Oddělit celostátní následnou/dlouhodobou péči od konkrétní přerovské LDN.
- Vypočítat podíl případů 60+ a 65+ z aktuálních otevřených dat.
- Doporučit obhajitelné věkové kritérium studie.

## Akceptační kritéria

- [x] Výpočet má uveden zdroj, rok, čitatel, jmenovatel a definici populace.
- [x] Je popsán rozdíl mezi věkem 60+ a přísně vyšším než 60 let.
- [x] Výsledek není vydáván za místní údaj Nemocnice Přerov.
- [x] Doporučení rozlišuje statistickou převahu od věcného zdůvodnění geriatrického kritéria.

## Ověření

- Opakovatelný součet z otevřeného CSV ÚZIS a kontrola proti publikovanému shrnutí ČSÚ.

## Handoff

- Otevřená data ÚZIS za rok 2024: v celé následné a dlouhodobé péči ČR bylo 74,23 % hospitalizačních případů ve věku 60+ a 68,23 % ve věku 65+; v Olomouckém kraji podle místa zařízení 71,11 %, respektive 65,37 %.
- Užší přehled ČSÚ pro obor následné péče v roce 2023 uvádí 76,5 tisíce případů 65+ a více než sedminásobek proti skupině 15–64; orientačně jde nejméně o 87,5 % mezi těmito dvěma skupinami.
- Veřejná data neumožňují samostatně vyčíslit přerovskou LDN. Pro lokální ověření je nutný anonymní agregovaný výpis všech překladů a překladů 60+/65+.
- Doporučení: ponechat kritérium 65+, které odpovídá aktuálnímu vymezení seniorů ČSÚ; statistickou převahu doplnit věcným geriatrickým zdůvodněním.
- Výstupy: `analysis/overeni-vekove-struktury-nasledne-pece.md`, rešeršní stopa, dva zdrojové záznamy, bibliografie, evidenční matice a doplnění `project-brief.md`.
- Ověření: všechny dvě citekey existují v bibliografii, závorky BibTeX jsou vyvážené a `git diff --check` nehlásí chybu obsahu.
