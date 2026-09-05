# Workflow plánů a tasků

Tato složka je provozní vrstva projektu. Plány říkají **proč a co** se má udělat; tasky říkají **kdo, kde, s jakými vstupy a jak ověří výsledek**.

## Stavové fronty plánů

| Složka | Význam | Brána pro přesun |
|---|---|---|
| `plans/10-preparing/` | plán je rozpracovaný | doplnit rozsah, rozhodnutí, tasky, rizika a kritéria |
| `plans/20-ready/` | plán je připravený | odborně zásadní volby jsou potvrzené a tasky mají závislosti |
| `plans/30-active/` | plán se provádí | alespoň jeden task je v `35-in-progress/` |
| `plans/40-completed/` | plán je dokončený | všechny povinné tasky jsou `implemented` a celek je zkontrolován |

## Stavové fronty tasků

| Složka | Význam | Brána pro přesun |
|---|---|---|
| `tasks/10-preparation/` | specifikace není úplná | doplnit výstup, vstupy, závislosti a kritéria |
| `tasks/20-prepared/` | task je popsaný, ale čeká | získat chybějící rozhodnutí, schválení nebo závislost |
| `tasks/30-ready-to-implement/` | task lze bezpečně zahájit | všechny vstupy a přidělené cesty jsou ověřené |
| `tasks/35-in-progress/` | právě na něm pracuje jeden vlastník | existuje nekolidující claim a průběžný handoff |
| `tasks/40-implemented/` | výstup je hotový a ověřený | splněna všechna akceptační kritéria a bezpečnostní kontrola |
| `tasks/90-blocked/` | práci zastavil konkrétní blocker | uvést podmínku odblokování; potom vrátit do odpovídajícího stavu |

Stav určuje výhradně cesta souboru. Frontmatter proto pole `status` neobsahuje.

## ID a názvy

- plán: `P-001-strucny-slug/plan.md`
- task: `T-P001-01-strucny-slug.md`
- podtask: `T-P001-01-01-strucny-slug.md`
- claim: `claims/T-P001-01.md`

ID se po vytvoření nemění. V textu odkazuj primárně ID; po přesunu souboru koordinátor aktualizuje potřebné odkazy.

## Postup koordinátora

1. Zkontrolovat `project-brief.md` a relevantní požadavky.
2. Vytvořit nebo aktualizovat plán podle `templates/plan.md`.
3. Rozdělit plán na malé tasky s nepřekrývajícími se `owned_paths`.
4. Přesunout task do `ready-to-implement` až po splnění všech závislostí.
5. Před paralelním spuštěním ověřit, že tasky nemění stejné soubory.
6. Vytvořit claim, určit vlastníka a task přesunout do `in-progress`.
7. Převzít handoff, ověřit výstup a teprve potom task přesunout do `implemented`.
8. Po dokončení všech povinných tasků provést integrační kontrolu plánu.

## Definice připravenosti tasku

Task může být v `ready-to-implement`, jen když:

- má jednoznačný očekávaný výstup;
- má známé vstupy a splněné závislosti;
- uvádí přesné soubory, které může vlastník měnit;
- nevyžaduje neudělené oprávnění nebo nevyřešené rozhodnutí uživatele;
- obsahuje ověřitelná akceptační kritéria;
- lze jej provést bez souběžné editace stejného souboru jiným agentem.

## Definice dokončení tasku

`implemented` znamená, že výstup existuje, akceptační kritéria byla skutečně ověřena, odkazy a navazující indexy jsou aktuální a proběhla kontrola zdrojů, citací, soukromí a citlivých údajů. Pouhé vytvoření textu nestačí.
