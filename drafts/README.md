# Markdown wiki rukopisu

`drafts/` je jediný zdroj textu rigorózní práce. Hlavní části mají stabilní očíslované složky a `index.md`; delší kapitoly se dále dělí na podstránky `10-nazev.md`, `20-nazev.md` atd.

- [`_index.md`](_index.md) – čitelný rozcestník wiki
- [`_manuscript.yml`](_manuscript.yml) – závazné pořadí stránek pro export
- [`../workflow/templates/section.md`](../workflow/templates/section.md) – šablona nové podstránky

Pořadí neurčuje pouze název souboru. Každou novou stránku musí koordinátor vložit také do `_manuscript.yml`.

Stav stránky se zapisuje do `draft_status`: `outline`, `draft`, `review` nebo `approved`. Kapitoly se podle stavu nepřesouvají, aby se nerozbíjely wiki odkazy.
