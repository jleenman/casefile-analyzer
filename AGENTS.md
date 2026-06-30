# AGENTS.md

Instructies voor Codex-runs in deze repository.

## Werkstijl

- Start iedere sessie met de verplichte volgorde uit `docs/repository-operating-manual.md`.
- Lees altijd eerst `.codex/project-state.md`, `.codex/blocked.md`, `.codex/human-inbox.md` en `.codex/next-task.md`.
- Voer per sessie precies één logische taak uit: de taak in `.codex/next-task.md`.
- Werk in kleine incrementele stappen.
- Maak geen grote aannames zonder ze expliciet te documenteren.
- Geef bij elke taak een korte samenvatting van wijzigingen.
- Houd wijzigingen beperkt tot de gevraagde scope.
- Update documentatie wanneer architectuur, scope, schema's of privacykeuzes veranderen.
- Voeg geen applicatiecode toe in documentatie-only stappen.

## Privacy en veiligheid

- Privacy en security zijn harde eisen, geen latere optimalisaties.
- Behandel alle voorbeelden als potentieel gevoelig, ook wanneer ze synthetisch zijn.
- Gebruik geen echte namen, echte dossiers of echte persoonsgegevens in demo- of testdata.
- Documenteer opslag-, verwijder- en toegangsrisico's zodra code wordt toegevoegd.
- Gebruik geen AI-provider of externe API met echte dossierdata zonder expliciete toestemming en veiligheidsanalyse.

## Bronverwijzingen en controleerbaarheid

- Alle AI-uitvoer moet bronverwijzingen ondersteunen.
- Geen conclusies zonder bron.
- Elke bevinding moet herleidbaar zijn naar bestand, regelnummer, timestamp, afzender, datum of transcriptsegment.
- Maak onderscheid tussen feit, signaal, patroon, interpretatie en juridische conclusie.
- Presenteer juridische kwalificaties nooit als definitieve waarheid.

## Validatie

- Schrijf tests of validatiecriteria zodra code wordt toegevoegd.
- Valideer schema's voordat ze als contract worden gebruikt.
- Voeg voorbeeldinput en verwachte output toe voor parsers en rapportgeneratoren.
- Controleer dat rapporten geen bevindingen bevatten zonder bronfragment.

## Documentatie

- Houd documentatie in het Nederlands.
- Houd docs concreet genoeg voor een volgende Codex-run.
- Noteer tijdelijke aannames expliciet.
- Splits current state, known issues en next actions wanneer operationele notities worden toegevoegd.
- Werk `CHANGELOG.md`, `.codex/backlog.md`, `.codex/roadmap.md`, `.codex/daily-log.md` en `.codex/next-task.md` bij aan het einde van iedere sessie.

## Zelforganisatie

- `.codex/` is de door Codex beheerde operating-system-laag van het project.
- `prompts/` is de door Codex beheerde prompt factory.
- Gebruik `.codex/human-inbox.md` als enige plek voor verplichte menselijke input.
- Onderzoeksvragen gaan eerst naar `.codex/research-queue.md` en wijzigen niet direct architectuur.
- Belangrijke beslissingen krijgen een ADR in `.codex/architecture-decisions.md`.
