# Exportní profil – pracovní verze

Stav: **není finální šablona**  
Poslední kontrola podkladů: **2026-09-04**

## Zdroje exportu

- pořadí: `drafts/_manuscript.yml`
- text: Markdown stránky v `drafts/`
- bibliografie: `sources/library.bib`
- výstup: `exports/`

## Mapování stylů

| Markdown | Cílový styl | Pracovní pravidlo |
|---|---|---|
| `#` hlavní část | Nadpis 1 | nová strana, zahrnout do obsahu |
| `##` podkapitola | Nadpis 2 | číslovat podle finální šablony |
| `###` podsekce | Nadpis 3 | používat střídmě |
| běžný odstavec | Základní text | Times New Roman 12 pt, řádkování 1,5, do bloku |
| tabulka | Popisek tabulky | pořadové číslo, název a odkaz v textu |
| obrázek/graf | Popisek obrázku | pořadové číslo, název, zdroj a odkaz v textu |
| `[@citekey]` | citace autor–datum | vykreslit podle potvrzeného stylu ČSN ISO 690:2022 |

## Rozvržení stránky

- levý okraj 4 cm;
- horní, pravý a dolní okraj 2,5 cm;
- záhlaví a zápatí 1,25 cm;
- hlavní kapitoly na nové straně;
- viditelné číslování stran od Úvodu, s kontrolou započtení předchozích stran podle šablony.

## Před finálním exportem

- [ ] Znovu ověřit aktuální předpisy a závaznou šablonu.
- [ ] Potvrdit titulní listy, prohlášení, abstrakty a povinné seznamy.
- [ ] Zkontrolovat všechny citekey a úplnost bibliografie.
- [ ] Odstranit nebo vyřešit všechny TODO značky.
- [ ] Zkontrolovat rozsah textu a poměr teoretické a praktické části.
- [ ] Ověřit tabulky, obrázky, přílohy a křížové odkazy.
- [ ] Projít vizuálně každou stránku DOCX i PDF.
- [ ] Ověřit, že finální soubory neobsahují skryté komentáře, revize ani citlivá metadata.
