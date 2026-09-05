# Pokyny pro Codex

## Kontext a cíl projektu

Tento repozitář slouží k přípravě rigorózní práce v oblasti ošetřovatelství. Výchozím jazykem komunikace, plánů a rukopisu je čeština, pokud uživatel neurčí jinak. Cílem je vytvořit odborně správný, dohledatelný a bezpečně exportovatelný rukopis, nikoli pouze souvislý text bez evidence původu.

Informace získané z projektových chatů nebo soukromých zpráv převáděj do repozitáře jen jako nezbytné anonymizované požadavky, rozhodnutí nebo úkoly. Původní soukromý obsah do sledovaných souborů nekopíruj.

## Zdroje pravdy a řešení rozporů

- `AGENTS.md` je zdrojem pravdy pro pracovní postup, bezpečnost, soukromí a koordinaci agentů.
- `project-brief.md` je zdrojem pravdy pro aktuálně schválené téma, cíle, výzkumné otázky, metodiku, citační normu a zásadní rozhodnutí.
- `requirements/` obsahuje anonymizované institucionální a exportní požadavky. Časově proměnlivé údaje vždy opatři datem kontroly a zdrojem.
- Umístění plánu nebo tasku ve stavové složce `workflow/` je jediným zdrojem pravdy pro jeho stav. Stav neduplikuj ve frontmatteru.
- `sources/records/` je zdrojem pravdy pro jednotlivé bibliografické a evidenční záznamy; `sources/library.bib` je koordinovaný souhrn.
- `drafts/` je jediným zdrojem rukopisu. DOCX a PDF jsou odvozené exporty a ručně se neupravují.
- `drafts/_manuscript.yml` je jediným zdrojem pořadí stránek při exportu.
- Při rozporu mezi soubory nerozhoduj odhadem. Zapiš rozpor do příslušného tasku, označ konkrétní blocker a vyžádej rozhodnutí uživatele, pokud mění odborný nebo formální směr práce.

## Povinná kontrola před rozsáhlejším psaním

Než začne rozsáhlejší rešerše, návrh protokolu nebo psaní kapitol, ověř v `project-brief.md`:

- administrativní možnost pokračovat v rigorózním řízení a relevantní termíny;
- schválený český a anglický název nebo výslovně označený pracovní název;
- hlavní výzkumnou otázku, cíle a cílovou populaci;
- zvolený a zdůvodněný výzkumný design;
- přístup k pracovišti, respondentům nebo datům;
- etické, právní a datové požadavky;
- citační normu a aktuální formální požadavky instituce.

Není-li některý bod potvrzen, lze připravovat varianty a podklady, ale nesmí být prezentovány jako schválené rozhodnutí.

## Implementační plány

Plány ukládej do `workflow/plans/` jako složky `P-NNN-strucny-slug/` se souborem `plan.md`.

- `10-preparing/` – plán se připravuje; chybí rozhodnutí, rozpad na tasky nebo kritéria.
- `20-ready/` – plán je kompletní, zkontrolovaný a uživatelem schválený, pokud mění téma, metodiku nebo formální směr.
- `30-active/` – alespoň jeden podřízený task probíhá.
- `40-completed/` – všechny povinné tasky jsou v `40-implemented/` a proběhla integrační kontrola.

Každý plán musí obsahovat cíl, rozsah a non-goals, vstupy, rozhodnutí a předpoklady, závislosti, rizika, seznam ID tasků a podtasků, cílové výstupy, akceptační kritéria a způsob ověření.

## Životní cyklus tasků

Task ukládej jako `T-PNNN-NN-strucny-slug.md`; podtask jako `T-PNNN-NN-NN-strucny-slug.md`. Používej tyto stavové složky:

- `10-preparation/` – nápad nebo neúplné zadání; chybí část rozsahu, vstupů nebo kritérií.
- `20-prepared/` – zadání, výstup a kritéria jsou popsány, ale zbývá schválení, rozhodnutí nebo závislost.
- `30-ready-to-implement/` – všechny vstupy, cílové soubory, závislosti a oprávnění jsou ověřeny; task lze bezpečně převzít.
- `35-in-progress/` – task má právě jednoho vlastníka a práce probíhá.
- `40-implemented/` – výstup existuje, byla splněna akceptační kritéria a proběhly odborné, citační, návaznostní a bezpečnostní kontroly uvedené v tasku.
- `90-blocked/` – výjimečná provozní fronta; task musí uvádět konkrétní blocker, dosavadní zjištění a podmínku odblokování.

Hlavní požadovaný tok je `preparation → prepared → ready-to-implement → in-progress → implemented`. Stav `prepared` neznamená, že lze task realizovat; to znamená až `ready-to-implement`. Stavy nepřeskakuj bez zaznamenaného důvodu. Při znovuotevření vrať task do nejbližšího odpovídajícího stavu.

Task musí obsahovat `id`, `parent_plan`, volitelně `parent_task`, vlastníka, závislosti, přidělené cesty, očekávané výstupy, akceptační kritéria, ověřovací postup, použité zdroje a handoff. Přesuny mezi stavovými složkami provádí koordinující agent.

## Paralelní agenti a vlastnictví souborů

- Jeden agent je koordinátor: rozděluje plán, kontroluje závislosti, přiděluje tasky, integruje výsledky a mění stavové složky.
- Paralelně spouštěj pouze nezávislé tasky s nepřekrývajícími se cílovými soubory.
- Jeden task a jeden cílový soubor smí mít v daný okamžik právě jednoho zapisujícího agenta.
- Před editací agent vytvoří claim v `workflow/claims/`, uvede ID tasku, vlastníka a přidělené cesty a ověří, že neexistuje kolidující claim.
- Pracovní agent mění pouze svůj task a přidělené cesty. Změnu mimo ně předá koordinátorovi.
- `AGENTS.md`, `project-brief.md`, `drafts/_manuscript.yml`, centrální indexy, `sources/library.bib` a `sources/evidence-matrix.md` při paralelní práci upravuje pouze koordinátor.
- Pracovní agent nepřesouvá task mezi stavy a sám jej neoznačuje jako dokončený.
- Handoff každého agenta uvede změněné soubory, použité zdroje, provedené ověření a otevřené body.
- Agentům předávej ze soukromých zpráv pouze minimální anonymizovaný kontext potřebný pro jejich task.
- Paralelní práce neopravňuje žádného agenta ke commitu, pushi, odeslání zprávy, zveřejnění ani sdílení dat.

## Markdown wiki rukopisu

- Každá hlavní část má stabilní složku v `drafts/` a soubor `index.md`; samostatné sekce zapisuj jako očíslované Markdown podstránky.
- `_index.md` v kořeni rukopisu funguje jako čitelný rozcestník. Exportní pořadí řídí `_manuscript.yml`.
- Cesty a názvy souborů používej v ASCII `kebab-case`; text a nadpisy piš česky.
- Každá stránka rukopisu obsahuje frontmatter alespoň s `id`, `title`, `parent`, `order`, `draft_status`, `source_ids` a `last_reviewed`.
- `draft_status` používá hodnoty `outline`, `draft`, `review` nebo `approved`. Tento stav se nemění přesunem souboru.
- Po vytvoření neměň ID stránky. Při přesunu nebo přejmenování oprav odkazy i exportní manifest.
- `index.md` shrnuje obsah a odkazuje na podstránky; neduplikuje jejich celý text.
- Odborné tvrzení musí mít dohledatelnou citaci. Neověřená místa označ `<!-- TODO[CITE]: co ověřit -->`; nikdy nevytvářej provizorní nebo smyšlenou citaci.
- Citace v Markdownu zapisuj jednotnými citekey, například `[@novak2024]`. Výslednou podobu určuje exportní citační styl.
- V textu jasně odliš fakta ze zdrojů, vlastní syntézu, interpretaci a pracovní hypotézu.

## Odborná práce a evidence zdrojů

- Nevymýšlej zdroje, citace, DOI, PMID, NCT ani výsledky studií.
- Preferuj recenzované studie, systematické přehledy, doporučené postupy a autoritativní zdravotnické instituce. PubMed a ClinicalTrials.gov používej jako vyhledávací a ověřovací zdroje, nikoli jako náhradu kritického hodnocení.
- Každou rešerši ulož do `sources/searches/` včetně databáze, přesného dotazu, filtrů, data hledání a počtu výsledků.
- Pro každý zařazený zdroj vytvoř právě jeden záznam v `sources/records/`; duplicity kontroluj podle DOI, PMID, ISBN nebo stabilní URL.
- Záznam zdroje obsahuje úplnou citaci, identifikátory, typ dokumentu a studie, databázi a datum kontroly, dostupnost plného textu, populaci a vzorek, výsledky, omezení, riziko zkreslení nebo kvalitu a vztah k výzkumné otázce.
- U číselných výsledků zaznamenej stránku, tabulku nebo jinou přesnou lokaci v originálu.
- Pokud byl dostupný jen abstrakt, označ záznam `abstract-only` a netvrď podrobnosti vyžadující plný text.
- Preprint neoznačuj jako recenzovanou studii. Primární studie, přehled, guideline a konsenzus eviduj jako odlišné typy důkazů.
- Plné texty ukládej jen při oprávněném přístupu a v souladu s licencí; automaticky je nezařazuj do Gitu.

## Soukromí a citlivá data

- Všechny sledované soubory považuj za veřejné bez ohledu na aktuální viditelnost GitHub repozitáře.
- Do Gitu nikdy neukládej celé e-maily nebo soukromé zprávy, adresy, kontakty, přihlašovací údaje, zdravotní dokumentaci, surové dotazníky, přepisy rozhovorů, převodní klíče ani identifikovatelné údaje pacientů či účastníků.
- Citlivé pracovní podklady patří pouze do ignorované složky `private/` a jen na výslovný pokyn uživatele. Pseudonymizovaná data jsou stále citlivá.
- Outlook používej jen na výslovný pokyn. Načítej pouze rozsah nutný pro konkrétní úkol.
- E-maily neposílej, nepřeposílej, nemaž ani neměň bez výslovného zadání uživatele.
- Umístění v `private/` samo o sobě neopravňuje obsah odeslat, sdílet nebo předat externímu nástroji.
- Před dokončením zkontroluj všechny nové sledované soubory a Git diff na osobní, zdravotní, přístupové a kontaktní údaje.

## Export a formální kontrola

- Exportní konfiguraci, šablony a skripty ukládej do `export/`; generované DOCX a PDF do ignorované složky `exports/`.
- Univerzitní šablonu nepřepisuj. Pracuj s kopií a eviduj původ, verzi a datum ověření požadavků.
- Finální export vytvoř až po potvrzení aktuálních požadavků instituce. Pracovní export viditelně označ jako koncept.
- U každého exportu eviduj použitý manifest, citační styl, šablonu, datum a reprodukovatelný příkaz nebo postup.
- Před finálním předáním vizuálně ověř každou stránku a zkontroluj pořadí, nadpisy, číslování, křížové odkazy, tabulky, obrázky, citekey, bibliografii, rozsah, TODO značky a anonymizaci.

## GitHub a dokončení práce

- Primární vzdálený repozitář je `Hrabi/Martina`.
- Neměň viditelnost repozitáře, přístupová práva ani sdílení bez výslovného souhlasu.
- Commit nebo push prováděj pouze na výslovný pokyn uživatele.
- Hotovo znamená, že požadovaný výstup existuje, odkazy a manifesty jsou aktuální, akceptační kritéria byla ověřena, nezůstaly skryté odborné nebo citační domněnky a nebyla porušena ochrana dat.
