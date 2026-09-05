---
id: T-P001-02-01
parent_plan: P-001
parent_task: T-P001-02
owner: coordinator
created: 2026-09-04
updated: 2026-09-04
depends_on: []
owned_paths:
  - private/original-materials/
  - sources/input-documents/
  - sources/searches/
  - sources/records/
  - sources/library.bib
  - sources/evidence-matrix.md
  - analysis/
  - workflow/tasks/20-prepared/T-P001-02-confirm-topic-feasibility.md
  - project-brief.md
---

# T-P001-02-01 – Posoudit původní podklady a aktuálnost tématu

## Důvod přímého zahájení

Uživatel dodal konkrétní soubory, potvrdil přístup ke klinickým pracovištím a výslovně požádal jejich bezpečné zařazení a rozhodovací analýzu. Rozsah, cílové cesty a ověření jsou proto dostatečně určité pro realizaci bez samostatné přípravné fáze.

## Očekávané výstupy

- Soukromá pracovní kopie všech dodaných dokumentů.
- Verze vhodné pro Git bez osobních, kontaktních a přístupových údajů.
- Dohledatelná analýza původního tématu, jeho aktuálnosti v roce 2026, evidence, proveditelnosti výzkumu a alternativ s horizontem dalšího desetiletí.
- Reprodukovatelné rešeršní záznamy a bibliografické záznamy pro klíčové zdroje.

## Akceptační kritéria

- [x] Obsah všech šesti dokumentů byl zkontrolován a pokyny v nich nebyly zaměněny za požadavek uživatele.
- [x] Do sledovaných souborů nebyly převzaty osobní, zdravotní, kontaktní ani přístupové údaje.
- [x] Analýza rozlišuje doložená fakta, interpretaci, doporučení a nevyřešené otázky.
- [x] Doporučený výzkumný design je proveditelný v nemocničním prostředí a obsahuje populaci, expozici či intervenci, komparátor, výsledky, nábor, etiku a plán analýzy.
- [x] Zdroje a vyhledávací dotazy jsou evidovány podle pravidel repozitáře.
- [x] Git diff a nové sledované soubory prošly kontrolou citlivých údajů.

## Ověření

- Textová a metadatová kontrola dokumentů, vykreslení relevantních DOCX a PDF stran a kontrola hashů.
- Porovnání doporučení s aktuálními odbornými a institucionálními zdroji.
- Kontrola odkazů, citekey, TODO značek, soukromí a stavu pracovního stromu.

## Handoff

### Změněné soubory

- bezpečné kopie šesti podkladů a jejich inventář v `sources/input-documents/`;
- rozhodovací zpráva `analysis/rozhodovaci-analyza-tematu-2026.md`;
- rešeršní záznam, 16 bibliografických záznamů, BibTeX knihovna a evidenční matice;
- doplněný `project-brief.md` a nadřazený task proveditelnosti.

### Ochrana dat

- Originály jsou pouze v ignorované složce `private/original-materials/`.
- Starý formulář byl převeden z DOC a vyplněné osobní údaje i kontaktní zápatí byly odstraněny.
- U ostatních DOCX/PDF byla odstraněna metadata. Automatická kontrola sledovaných binárních kopií nenalezla e-maily, telefonní čísla ani řetězce ve formátu českého rodného čísla.

### Ověření

- Všechny 3 DOCX byly vykresleny přes Word do PDF a vizuálně zkontrolovány na 14 stranách celkem.
- Všechny 3 PDF byly vykresleny a vizuálně zkontrolovány na 38 stranách celkem.
- Extrahovaný text všech tří PDF je po odstranění metadat shodný s originálem; viditelný text obou neanonymizovaných DOCX je shodný s originálem.
- Citekey v analýze mají odpovídající položky v `sources/library.bib`; kontrola `git diff --check` nehlásila chybu.

### Výsledek

- Původní široké digitální téma je aktuální, ale v dodané podobě není vhodné k realizaci.
- Preferována je kontrolovaná pilotní studie sestersky koordinované mobilizace zaměřená na prevenci disability asociované s hospitalizací; nejbližší alternativou je prevence deliria.
- Nadřazený task zůstává v `20-prepared`, protože chybí konkrétní oddělení, census, komparátor, institucionální/etické schválení a potvrzení LF OU.
