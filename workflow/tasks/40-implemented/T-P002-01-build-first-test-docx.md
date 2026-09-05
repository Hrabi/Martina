---
id: T-P002-01
parent_plan: P-002
parent_task: null
owner: coordinator
created: 2026-09-04
updated: 2026-09-04
depends_on: []
owned_paths:
  - export/build-test-docx.py
  - export/logs/2026-09-04-first-test-docx.md
  - exports/rigorozni-prace-testovaci-export.docx
target_outputs:
  - exports/rigorozni-prace-testovaci-export.docx
---

# T-P002-01 – Sestavit první testovací DOCX

## Očekávaný výstup

Pracovní Word dokument vytvořený z aktuální osnovy rukopisu v pořadí manifestu, se základním formátováním podle dodaného vzoru LF OU a s reprodukovatelným sestavením.

## Vstupy

- Zdroj pravdy: `drafts/_manuscript.yml`, stránky v `drafts/`, `requirements/export-profile.md`.
- Potřebné rozhodnutí nebo oprávnění: uživatel výslovně požádal o první testovací export.
- Stavový přechod: task byl založen přímo jako `in-progress`, protože šlo o bezprostředně převzatý, přesně vymezený uživatelský požadavek bez nevyřešené závislosti.

## Kroky

1. Zkontrolovat dodaný vzor a aktuální rukopis.
2. Vytvořit exportní skript a pracovní DOCX.
3. Vykreslit všechny stránky a provést vizuální kontrolu.
4. Provést strukturální, metadatovou a bezpečnostní kontrolu.
5. Zapsat exportní log a předat DOCX.

## Akceptační kritéria

- [x] Výstup existuje na očekávaném místě.
- [x] Pořadí částí odpovídá `drafts/_manuscript.yml`.
- [x] Dokument je zřetelně označen jako pracovní testovací export.
- [x] Neověřené údaje nejsou doplněny odhadem.
- [x] Všechny stránky byly vykresleny a vizuálně zkontrolovány.
- [x] Sledované soubory neobsahují citlivé údaje.

## Ověření

- Kontrola nebo příkaz: `render_docx.py`, `section_audit.py`, `heading_audit.py`, kontrola ZIP/OOXML a Git diff.
- Očekávaný výsledek: bez ořezu, překryvů, chybějících glyfů a neočekávaného číslování; žádná osobní metadata.

## Použité zdroje a evidence

- Dodaný vzor LF OU `rigorozni-prace-doporucena-uprava-2023.pdf`.
- `requirements/export-profile.md`.

## Blocker

- `none`; neověřené finální údaje budou v testovacím exportu výslovně označeny.

## Handoff

- Změněné soubory: `export/build-test-docx.py`, `export/logs/2026-09-04-first-test-docx.md`, `exports/rigorozni-prace-testovaci-export.docx`.
- Provedené ověření: render 15 stran, kontrola všech PNG, audit sekcí, nadpisů a polí, kontrola ZIP/OOXML, metadat a citlivých řetězců.
- Otevřené body: finální titulní údaje, aktualizovaný obsah po rozšíření rukopisu a potvrzená závazná Word šablona.
