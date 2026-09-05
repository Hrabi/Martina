# Ověření věkové struktury pacientů následné péče

**Datum kontroly:** 2026-09-04  
**Účel:** posoudit obhajitelnost věkového kritéria 65+ pro audit překladů na LDN  
**Závěr:** celostátní data potvrzují převahu starších pacientů, ale přesné procento pro LDN Nemocnice Přerov musí dodat nemocnice jako agregovaný údaj.

## Hlavní zjištění

Český statistický úřad uvádí pro rok 2023 v oboru následné péče 76,5 tisíce hospitalizačních případů osob ve věku 65 a více let. Tento počet byl více než sedminásobný oproti skupině 15–64 let [@csu2025seniorinasledna]. Z publikovaného poměru vychází orientační podíl osob 65+ přibližně **87,5 %** mezi dvěma porovnávanými věkovými skupinami:

```text
7 / (7 + 1) × 100 = 87,5 %
```

Jde o odhad z formulace „sedminásobně“, nikoli o přesný přepočet z nezkrácených hodnot. Zdroj se týká oboru následné péče v celé České republice, nikoli konkrétní LDN.

Z otevřené datové sady ÚZIS za rok 2024 byl proveden vlastní součet všech hospitalizačních případů následné a dlouhodobé péče [@uzis2024naslednaopendata]:

| Rozsah | Všechny případy | Případy 60+ | Podíl 60+ | Případy 65+ | Podíl 65+ |
|---|---:|---:|---:|---:|---:|
| Česká republika | 177 386 | 131 680 | **74,23 %** | 121 031 | **68,23 %** |
| Olomoucký kraj podle místa zařízení | 11 285 | 8 025 | **71,11 %** | 7 377 | **65,37 %** |

Širší datová sada zahrnuje všechny případy následné a dlouhodobé péče, včetně péče poskytované mladším pacientům, a nerozlišuje samostatně přerovskou LDN. Proto její nižší podíly nejsou v rozporu s užším údajem ČSÚ pro obor následné péče a nelze je vydávat za věkovou strukturu LDN.

## Co znamená „starší 60 let“

Otevřená data používají pětileté věkové skupiny. Lze proto přesně sečíst skupiny **60 let a více**, ale nikoli přísně „více než 60 let“, protože skupina 60–64 zahrnuje i šedesátileté. Pro protokol je nutné psát jednoznačně `věk ≥ 60 let`, nebo `věk ≥ 65 let`.

## Doporučení pro rigorózní práci

Ponechat hranici **65 let a více**. Je metodicky obhajitelnější než 60+ z těchto důvodů:

1. ČSÚ ve své aktuální statistice lůžkové péče vymezuje seniory jako osoby 65+.
2. Stejná hranice umožňuje přímé zasazení místního souboru do českých statistik.
3. Výzkumné téma je určeno oboru ošetřovatelské péče v geriatrii; věkové kritérium je předem definovaným zaměřením, nikoli tvrzením, že na LDN neleží mladší pacienti.

Samotná převaha pacientů 65+ není jediným zdůvodněním. Do protokolu je vhodné doplnit, že vyšší věk souvisí s častější multimorbiditou, funkční závislostí a potřebou přesného předání geriatrických ošetřovatelských informací; tato tvrzení musí být následně doložena odbornými zdroji.

## Co je třeba ověřit lokálně

Nemocnice by měla dodat pouze anonymní agregovaný výpis za posledních 12 měsíců nebo alespoň za dvě srovnatelná dvouměsíční období:

- počet všech překladů na přerovskou LDN;
- počet překladů pacientů ve věku 60+;
- počet překladů pacientů ve věku 65+;
- rozdělení podle výchozího akutního oddělení.

Výpočet místního podílu:

```text
podíl 65+ = počet překladů pacientů ve věku ≥ 65 let / počet všech překladů na LDN × 100
```

Pro plánovanou práci je ještě důležitější absolutní počet překladů 65+ za dva měsíce než samotné procento, protože určí reálně dostupnou velikost výzkumného souboru.

## Omezení

- Veřejné webové stránky Nemocnice AGEL Přerov popisují LDN jako pracoviště následné péče se třemi stanicemi po 30 lůžkách a uvádějí zaměření na geriatrické nemocné, nezveřejňují však věkové rozložení pacientů.
- Celostátní otevřená data nelze kvůli anonymizaci filtrovat na konkrétní zařízení; geografický detail končí krajem.
- Hospitalizační případ není totéž co unikátní pacient ani překlad z konkrétního akutního oddělení.
