# Ověření věku pacientů následné a dlouhodobé péče

- Datum hledání a výpočtu: 2026-09-04
- Účel: ověřit tvrzení, že na LDN převažují pacienti vyššího věku, a posoudit hranici 60+ versus 65+.
- Zdroje: web ČSÚ, Národní zdravotnický informační portál/ÚZIS, veřejný web Nemocnice AGEL Přerov.
- Charakter: cílená statistická kontrola, nikoli systematická rešerše.

## Vyhledávací dotazy

```text
site:uzis.cz LDN věk pacientů 60 65 následná lůžková péče statistika věkové skupiny
site:nzip.cz léčebny dlouhodobě nemocných věk pacientů statistika
site:nemocniceprerov.agel.cz výroční zpráva LDN Přerov pacienti věk
site:csu.gov.cz hospitalizovaní léčebny dlouhodobě nemocných věk 60
"léčebny dlouhodobě nemocných" "průměrný věk" hospitalizovaných 2023
"léčebnách dlouhodobě nemocných" "65" hospitalizovaných procent
```

## Použité zdroje

1. ČSÚ: *Lůžková zdravotnická zařízení*, zveřejněno 20. 3. 2025, data za rok 2023.
2. ÚZIS/NZIP: *Charakteristika hospitalizačních případů následné a dlouhodobé péče*, aktualizace 6. 11. 2025, data 2010–2024.
3. Nemocnice AGEL Přerov: veřejný popis LDN, kontrola 4. 9. 2026; stránka neobsahuje věková data.

## Reprodukovatelný výpočet z dat ÚZIS

- Distribuce CSV: `https://data.mzcr.cz/data/distribuce/391/Otevrena-data-NR-04-39-hospitalizacni-pripady-nasledna-pece.csv`
- Filtr: `rok = 2024`.
- Čitatel: součet `pocet_hosp` pro pětileté věkové kategorie s dolní hranicí nejméně 60, respektive 65 let.
- Jmenovatel: součet `pocet_hosp` přes všechny věkové kategorie; věk byl znám u všech započtených případů.
- Olomoucký kraj: `kraj_ICZ = CZ071`.

Výsledek:

| Rozsah | Celkem | 60+ | % 60+ | 65+ | % 65+ |
|---|---:|---:|---:|---:|---:|
| ČR | 177 386 | 131 680 | 74,23 | 121 031 | 68,23 |
| Olomoucký kraj podle místa zařízení | 11 285 | 8 025 | 71,11 | 7 377 | 65,37 |

Kontrolní výpočet podle ošetřovacích dnů na standardních lůžkách v celé ČR: 71,78 % dnů připadalo na skupinu 60+ a 66,11 % na skupinu 65+.

## Omezení

- Otevřená data ÚZIS zahrnují širší následnou a dlouhodobou péči, nikoli jen LDN.
- Veřejný geografický detail neumožňuje určit samostatně Nemocnici Přerov.
- Pětiletá skupina 60–64 neumožňuje oddělit přesně věk 60 od věku 61–64.
- Publikované tvrzení ČSÚ o sedminásobném rozdílu umožňuje pouze orientační přepočet podílu 65+.

