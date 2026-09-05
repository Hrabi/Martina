# Záznam prvního testovacího exportu do Wordu

- Datum: 2026-09-04
- Verze zdrojů: commit `b02d082` a aktuální necommitované změny pracovního stromu
- Manifest: `drafts/_manuscript.yml`, verze 1
- Použitý vzor: `sources/input-documents/rigorozni-prace-doporucena-uprava-2023.pdf`, zkontrolováno 2026-09-04
- Doplňující profil: `requirements/export-profile.md`, pracovní verze z 2026-09-04
- Citační styl: ČSN ISO 690:2022, autor-datum; v aktuálním osnovovém rukopisu nejsou použity citekey, bibliografie proto nebyla vygenerována
- Sestavení: `python export/build-test-docx.py --output tmp/word-export/rigorozni-prace-testovaci-export-pre-scrub.docx`
- Odstranění metadat: `privacy_scrub.py` z dokumentového runtime do `exports/rigorozni-prace-testovaci-export.docx`
- Vytvořený DOCX: `exports/rigorozni-prace-testovaci-export.docx`
- Vytvořený PDF: žádný výstupní PDF; dočasný PDF vznikl pouze při vizuální kontrole
- SHA-256 DOCX: `7F6B4D95391740A8E98773DFAFCFD1CCC3D6FE65D0447B2937831FA0B6C8CD68`

## Parametry sestavení

- Formát A4 na výšku.
- Okraje: levý 4 cm, horní, pravý a dolní 2,5 cm.
- Záhlaví a zápatí 1,25 cm.
- Times New Roman 12 pt, řádkování 1,5 a zarovnání běžného textu do bloku.
- Hlavní nadpisy 14 pt, tučně, verzálkami; každá hlavní část začíná na nové straně.
- Přední část má šest stran bez viditelného čísla; Úvod začíná viditelným číslem 7.
- Výstup má 15 stran a je v záhlaví označen jako pracovní testovací koncept.

## Automatické kontroly

- ZIP/OOXML balíček je čitelný bez CRC chyby.
- Dokument má dvě sekce se shodným formátem A4 a požadovanými okraji.
- První sekce nemá číslo strany; druhá sekce obsahuje pole `PAGE` a začíná číslem 7.
- Nalezeno 13 odstavců stylu `Heading 1`; všechny nadpisy používají Times New Roman.
- Osobní metadata `creator` a `lastModifiedBy` jsou prázdná.
- Kontrola obsahu nenašla e-mailové adresy, lokální uživatelskou cestu, testovací jména z univerzitního vzoru ani značku `TODO[CITE]`.

## Vizuální kontrola

- Balíčkový `render_docx.py` byl spuštěn nad finálním DOCX; protože v prostředí není LibreOffice, převod DOCX na dočasný PDF provedla lokální instalace Microsoft Word přes task-local kompatibilní převodník.
- Všech 15 PNG stran bylo zkontrolováno v plném rozlišení.
- Nebyl zjištěn ořez textu, překryv objektů, chybějící glyf, poškozené tabulky, nesprávný zlom stránky ani vadné záhlaví či zápatí.
- Po první iteraci byla odstraněna barevná linka zděděná ze stylu `Title`, nadpisy byly sjednoceny na Times New Roman a titulní údaje byly zarovnány blíže dodanému vzoru; následoval nový render a kontrola všech stran.

## Otevřené body

- Jde o testovací export osnovy, nikoli o finální rukopis.
- Český název je pouze pracovní; anglický název, autor a konzultant nejsou potvrzeni.
- Obsah je pro tento patnáctistránkový snímek statický a musí se při růstu rukopisu nahradit aktualizovaným obsahem.
- Před finálním exportem je nutné znovu potvrdit aktuální institucionální požadavky a závaznou Word šablonu, pokud ji LF OU poskytne.
