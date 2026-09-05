---
id: P-002
title: Vytvořit první testovací export rukopisu do Wordu
owner: coordinator
created: 2026-09-04
updated: 2026-09-04
depends_on: []
target_outputs:
  - export/build-test-docx.py
  - export/logs/2026-09-04-first-test-docx.md
  - exports/rigorozni-prace-testovaci-export.docx
---

# P-002 – Vytvořit první testovací export rukopisu do Wordu

## Cíl

Vytvořit reprodukovatelný pracovní DOCX z kanonického pořadí v `drafts/_manuscript.yml` a ověřit, že odpovídá základním formálním pravidlům dodaného vzoru LF OU.

## Rozsah

- Zahrnuto: český a anglický titulní list, abstrakty, pracovní prohlášení, obsah, aktuální osnovové stránky rukopisu, číslování stran a vizuální kontrola.
- Nezahrnuto: doplňování neověřených osobních údajů, schváleného názvu, odborného textu, citací nebo finálního univerzitního exportu.

## Vstupy a zdroje pravdy

- `drafts/_manuscript.yml`
- stránky v `drafts/`
- `requirements/export-profile.md`
- `requirements/institutional.md`
- `sources/input-documents/rigorozni-prace-doporucena-uprava-2023.pdf`

## Rozhodnutí a předpoklady

- Výstup bude viditelně označen jako testovací pracovní koncept.
- Použije se A4, Times New Roman 12 pt, řádkování 1,5, levý okraj 4 cm a ostatní okraje 2,5 cm.
- Pracovní český název bude převzat z `project-brief.md`; anglický název, autor a konzultant zůstanou výslovně nepotvrzené.
- Plán byl založen přímo jako aktivní, protože jde o výslovně vyžádaný, omezený testovací export bez změny odborného nebo formálního směru.

## Závislosti a rizika

- Finální šablona a povinné osobní údaje nejsou potvrzeny; výstup proto nesmí být prezentován jako finální.
- V rukopisu jsou zatím pouze osnovové poznámky, nikoli hotové kapitoly.

## Tasky a podtasky

- `T-P002-01` – sestavit a vizuálně ověřit první testovací DOCX.

## Akceptační kritéria plánu

- [x] DOCX je vytvořen v `exports/` a lze jej otevřít.
- [x] Pořadí částí odpovídá exportnímu manifestu.
- [x] Základní rozvržení odpovídá dodanému vzoru a pracovnímu exportnímu profilu.
- [x] Každá vykreslená stránka je vizuálně zkontrolována.
- [x] Exportní log uvádí vstupy, postup, kontroly a známá omezení.
- [x] Git diff neobsahuje osobní, zdravotní, přístupové ani kontaktní údaje.

## Ověření a handoff

- Provedené kontroly: render DOCX do 15 PNG, kontrola všech stran, audit sekcí, nadpisů a polí, kontrola metadat, ZIP/OOXML a citlivých řetězců.
- Výsledek: pracovní DOCX byl vytvořen a prošel integrační a vizuální kontrolou.
- Otevřené body: finální název, anglický název, autor, konzultant, dynamický obsah pro rozšířený rukopis a závazná verze univerzitní Word šablony.
