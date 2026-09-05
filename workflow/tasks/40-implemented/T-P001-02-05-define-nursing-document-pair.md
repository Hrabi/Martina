---
id: T-P001-02-05
parent_plan: P-001
parent_task: T-P001-02
owner: coordinator
created: 2026-09-04
updated: 2026-09-04
depends_on:
  - T-P001-02-04
owned_paths:
  - project-brief.md
  - analysis/vyber-neintervencniho-tematu-dva-mesice.md
  - workflow/tasks/20-prepared/T-P001-02-confirm-topic-feasibility.md
---

# T-P001-02-05 – Vymezit párový audit sesterské dokumentace

## Důvod přímého zahájení

Uživatel upřesnil místní pracovní proces a výzkumný záměr: porovnávat se má sesterská překladová zpráva z akutního oddělení s přijímací sesterskou zprávou a vstupním posouzením na LDN. Lékařská překladová zpráva není předmětem práce.

## Očekávaný výstup

- Přesný pracovní název a jednotka analýzy.
- Jednoznačné zahrnutí pouze sesterské dokumentace.
- Metodické odlišení úplnosti, návaznosti a shody od klinické správnosti.

## Akceptační kritéria

- [x] Oba porovnávané sesterské dokumenty jsou pojmenovány.
- [x] Lékařská překladová zpráva je explicitně mimo rozsah.
- [x] Téma zůstává označeno jako favorit, nikoli schválený protokol.
- [x] Rozdílný záznam není bez dalšího označen za chybu.

## Ověření

- Kontrola shody zadání, rozhodovací analýzy a nadřazeného tasku.

## Handoff

- Zpřesněný pracovní název: „Kontinuita ošetřovatelské péče u geriatrických pacientů při překladu z akutních oddělení na LDN: audit úplnosti a návaznosti sesterské překladové a přijímací dokumentace.“
- Jednotkou analýzy je jeden překlad; datovou dvojicí je sesterská překladová zpráva z akutního oddělení a přijímací sesterská zpráva/vstupní posouzení na LDN.
- Lékařská překladová zpráva je mimo obsahový audit.
- Hodnotí se úplnost, návazné zachycení a případně popisná shoda stabilních údajů. Rozdíl mezi dokumenty se bez dalšího důkazu neoznačuje za chybu ani za nesprávnou práci sestry.
- Změněny byly `project-brief.md`, rozhodovací analýza a nadřazený task.
- Ověření: pracovní název a rozsah jsou mezi soubory shodné, všechny citekey analýzy existují v bibliografii a `git diff --check` nehlásí chybu obsahu.
