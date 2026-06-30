# Repository Operating Manual

Dit document beschrijft hoe toekomstige Codex-sessies zelfstandig moeten functioneren. Het is de primaire handleiding voor het zelforganiserende project `casefile-analyzer`.

## Basisprincipe

De repository is de bron van waarheid. Een Codex-sessie mag nooit afhankelijk zijn van eerdere chatcontext. Alle relevante context, planning, blockers en volgende acties moeten in bestanden staan.

## Verplichte Startvolgorde

Iedere toekomstige Codex-run volgt exact deze volgorde:

1. Lees `.codex/project-state.md`.
2. Lees `.codex/blocked.md`.
3. Lees `.codex/human-inbox.md`.
4. Lees `.codex/next-task.md`.
5. Voer uitsluitend de taak uit die in `next-task.md` staat.
6. Werk alle relevante documentatie bij.
7. Werk `.codex/backlog.md` en `.codex/roadmap.md` bij.
8. Werk `CHANGELOG.md` bij.
9. Genereer automatisch een nieuwe `.codex/next-task.md`.
10. Maak indien nodig nieuwe prompts.
11. Archiveer afgeronde of vervangen prompts via `.codex/prompt-history.md`.
12. Voeg een korte samenvatting toe aan `.codex/daily-log.md`.

## Stopregels

Stop de uitvoerende taak wanneer:

- `.codex/blocked.md` een actief blokkerend item bevat;
- `.codex/human-inbox.md` openstaande verplichte input bevat;
- de taak echte persoonsgegevens, API keys, accounts of partnerdata vereist;
- de taak een definitieve juridische kwalificatie vraagt;
- bronverwijzingen niet kunnen worden behouden.

Schrijf in dat geval een concrete vraag in `human-inbox.md` met prioriteit, reden, deadline, impact en wat Codex daarna kan doen.

## Eén Sessie, Eén Taak

Elke sessie vertegenwoordigt ongeveer één uur werk. Kies geen extra implementatiewerk buiten `next-task.md`, ook niet als het logisch lijkt. Nieuwe ideeën gaan naar backlog, research queue, technical debt of known risks.

## Rollenworkflow

Gebruik `.codex/roles.md` om te bepalen welke rol actief is. De rol in `next-task.md` is leidend. Andere rollen mogen reviewcriteria leveren, maar nemen de sessie niet over.

Standaardvolgorde bij twijfel:

1. Product Owner bepaalt prioriteit en scope.
2. Research Lead onderzoekt open vragen.
3. Software Architect legt ontwerpbeslissingen vast.
4. Implementation Engineer implementeert alleen wanneer toegestaan.
5. QA Engineer valideert output.
6. Security & Privacy Reviewer controleert risico's.
7. Technical Writer werkt docs, prompts en changelog bij.
8. Release Manager bewaakt releasecriteria.

## Prompt Factory

`prompts/` is door Codex beheerd. Iedere prompt moet bevatten:

- uniek ID;
- doel;
- context;
- benodigde input;
- verwachte output;
- acceptatiecriteria;
- afhankelijkheden.

Prompts vormen samen een uitvoerbare ontwikkelpipeline. Codex mag prompts aanpassen, vervangen, opsplitsen, samenvoegen of archiveren als dit de pipeline verbetert. Registreer wijzigingen in `.codex/prompt-history.md`.

## Research Workflow

Onderzoek begint altijd in `.codex/research-queue.md`. Onderzoek mag niet direct architectuur wijzigen.

Na afronding moet Codex vastleggen:

- samenvatting;
- bronnen;
- conclusies;
- impact op MVP;
- aanbevolen ADR indien relevant.

Pas daarna mag een architecture decision record worden aangepast of toegevoegd.

## ADR Workflow

Belangrijke beslissingen worden vastgelegd in `.codex/architecture-decisions.md` met:

- context;
- alternatieven;
- beslissing;
- motivatie;
- gevolgen;
- revisiedatum.

Geen grote architectuurwijziging zonder ADR.

## Kanban Workflow

`.codex/backlog.md` is het Markdown Kanban-bord met kolommen:

- To Do
- Ready
- In Progress
- Review
- Blocked
- Done

Iedere taak heeft:

- uniek nummer;
- rol;
- complexiteit;
- prioriteit;
- afhankelijkheden;
- status;
- eigenaar.

Aan het einde van elke sessie verplaatst Codex de huidige taak naar Review of Done en kiest de hoogste-prioriteitstaak die niet geblokkeerd is als nieuwe `next-task.md`.

## Human Inbox

`.codex/human-inbox.md` is het enige communicatiepunt voor menselijke input.

Iedere vraag bevat:

- prioriteit;
- reden;
- deadline;
- impact;
- wat Codex daarna kan doen.

Na verwerking archiveert Codex de vraag in hetzelfde bestand.

## Release Workflow

Release-informatie staat in `.codex/release-state.md` en `.codex/roadmap.md`.

Releasefasen:

1. Planning
2. Prototype
3. MVP
4. Pilot
5. Public Beta
6. Stable

Een release mag pas promoveren wanneer de acceptatiecriteria in `release-state.md` zijn gehaald.

## Automatisering

Deze Codex-omgeving ondersteunt dagelijkse automatisering. De automatisering `casefile-analyzer-daily-next-task` is geconfigureerd voor dagelijks 09:00 lokale tijd.

De huidige automatisering draait lokaal in de Codex-app. In deze omgeving is geen cloud execution target beschikbaar gesteld voor deze repository. Als de lokale machine of Codex-app niet actief is rond het geplande moment, kan de taak niet gegarandeerd exact om 09:00 starten. Als de omgeving wordt afgesloten terwijl een taak loopt, moet de run als mogelijk onderbroken worden beschouwd.

De automatisering moet:

- dagelijks om 09:00 lokale tijd starten;
- werken in deze repository;
- eerst `project-state.md`, `blocked.md`, `human-inbox.md` en `next-task.md` lezen;
- stoppen wanneer verplichte human input openstaat;
- uitsluitend `next-task.md` uitvoeren;
- na afloop een nieuwe `next-task.md` genereren;
- docs, backlog, roadmap, changelog, prompt history en daily log bijwerken.

### Onderbrekingsherstel

Wanneer een geautomatiseerde of handmatige sessie wordt onderbroken:

1. Start de volgende sessie met `git status`.
2. Lees de verplichte `.codex` startbestanden.
3. Controleer of `.codex/next-task.md` nog overeenkomt met de gedeeltelijke wijzigingen.
4. Rond eerst de half-afgeronde taak af of zet een blocker in `.codex/blocked.md`.
5. Start geen nieuwe taak voordat de repository weer consistent is.

Als automatisering later opnieuw moet worden ingesteld, gebruik dezelfde promptlogica en werkdirectory. Voor cloud-uitvoering moet eerst expliciet worden vastgesteld welke Codex-host of CI-runner toegang heeft tot de repository en hoe secrets, filesystem en write-permissies veilig geregeld zijn.

## Publicatievoorbereiding

De repository moet later automatisch publiceerbaar worden naar:

- GitHub;
- GitHub Pages.

Voer publicatie niet uit zonder expliciete taak en zonder releasecriteria. Publicatievoorbereiding hoort bij de Release Manager.

## Dagelijkse Afsluiting

Elke sessie eindigt met:

- korte wijzigingssamenvatting;
- bijgewerkte changelog;
- bijgewerkte daily log;
- nieuwe next task;
- open blockers of human input indien nodig.
