# Export rukopisu

Tato složka bude obsahovat verzované šablony, citační styl a skripty pro reprodukovatelné sestavení rukopisu. Samotné generované DOCX/PDF patří do ignorované složky `exports/`.

## Zamýšlený tok

1. Načíst pořadí z `drafts/_manuscript.yml`.
2. Ověřit existenci všech stránek a citekey.
3. Složit Markdown v určeném pořadí.
4. Použít potvrzenou univerzitní šablonu a citační styl.
5. Vytvořit pracovní DOCX a PDF do `exports/`.
6. Vykreslit a vizuálně zkontrolovat každou stránku.
7. Zapsat parametry sestavení do exportního logu.

Konkrétní nástrojový řetězec se zvolí až podle finální univerzitní šablony. Zdrojové Markdown soubory se kvůli exportu ručně neduplikují.
