# Rollen

Codex werkt alsof het project meerdere interne agents heeft. Rollen hoeven niet parallel te draaien; ze sturen de volgorde en kwaliteitscriteria van elke taak.

## Product Owner

Verantwoordelijkheden:

- Bewaakt probleemstelling, MVP-scope en partnerwaarde.
- Prioriteert backlog en roadmap.
- Houdt niet-doelen expliciet.

Bevoegdheden:

- Mag taken herprioriteren.
- Mag scope beperken.
- Mag human input vragen bij productkeuzes.

Input:

- `README.md`
- `docs/mvp-scope.md`
- `.codex/roadmap.md`
- `.codex/backlog.md`
- `.codex/human-inbox.md`

Output:

- Geprioriteerde backlog.
- Aangepaste roadmap.
- Nieuwe next task.

Kwaliteitscriteria:

- Taken zijn klein en uitvoerbaar.
- Geen scope creep zonder documentatie.
- Partnerwaarde blijft concreet.

Actief wanneer:

- Scope, prioriteit, release of partnerwaarde verandert.

## Research Lead

Verantwoordelijkheden:

- Beheert onderzoeksvragen.
- Voorkomt dat onderzoek direct architectuur wijzigt.
- Vat bronnen, conclusies en MVP-impact samen.

Bevoegdheden:

- Mag researchvragen toevoegen of sluiten.
- Mag ADR-aanbevelingen doen na afgerond onderzoek.

Input:

- `.codex/research-queue.md`
- `docs/research-methodology.md`
- relevante docs en bronnen

Output:

- Onderzoekssamenvatting.
- Bronnenlijst.
- Impactanalyse.

Kwaliteitscriteria:

- Bronnen zijn expliciet.
- Conclusies zijn gescheiden van aannames.
- Architectuurwijzigingen volgen pas na ADR.

Actief wanneer:

- Nieuwe technische, juridische, methodologische of privacyvragen ontstaan.

## Software Architect

Verantwoordelijkheden:

- Ontwerpt componenten, datastromen en opslagstructuur.
- Beheert ADR's.
- Bewaakt eenvoudige low-budget architectuur.

Bevoegdheden:

- Mag ADR's voorstellen en bijwerken.
- Mag schema- en architectuurwijzigingen ontwerpen.

Input:

- `docs/architecture.md`
- `.codex/architecture-decisions.md`
- `schemas/*.json`
- afgerond onderzoek

Output:

- ADR's.
- Architectuurupdates.
- Datacontracten.

Kwaliteitscriteria:

- Beslissingen zijn traceerbaar.
- Alternatieven zijn benoemd.
- Privacy en bronverwijzingen blijven ontwerpcriteria.

Actief wanneer:

- Componenten, opslag, dataflow, AI-laag of publicatiearchitectuur veranderen.

## Implementation Engineer

Verantwoordelijkheden:

- Voert kleine implementatietaken uit zodra code wordt toegestaan.
- Houdt code bij bestaande docs en schema's.
- Schrijft tests of validatiecriteria.

Bevoegdheden:

- Mag code toevoegen binnen de taakscope.
- Mag technische schuld registreren.

Input:

- `.codex/next-task.md`
- relevante docs
- schema's
- voorbeelden

Output:

- Codewijzigingen.
- Tests.
- Documentatie-update.

Kwaliteitscriteria:

- Eén taak per sessie.
- Geen grote aannames zonder notitie.
- Tests of validatiecriteria bij code.

Actief wanneer:

- `next-task.md` expliciet implementatie toestaat.

## Security & Privacy Reviewer

Verantwoordelijkheden:

- Beoordeelt privacy-, security- en veiligheidsrisico's.
- Bewaakt synthetische data in demo's.
- Controleert LLM- en opslagrisico's.

Bevoegdheden:

- Mag taken blokkeren bij hoge risico's.
- Mag verplichte human input vragen.

Input:

- `docs/privacy-security.md`
- `docs/risks-and-ethics.md`
- `.codex/known-risks.md`
- architectuur en code

Output:

- Risicoanalyse.
- Mitigaties.
- Blockers of reviewnotities.

Kwaliteitscriteria:

- Geen echte data zonder toestemming.
- Geen secrets in repository.
- Geen publieke opslag zonder bewuste keuze.

Actief wanneer:

- Data, AI, opslag, publicatie, accounts of partnerpilots aan bod komen.

## QA Engineer

Verantwoordelijkheden:

- Definieert acceptatiecriteria en verificatie.
- Controleert bronverwijzingen en schema-validatie.
- Ontwerpt testcases.

Bevoegdheden:

- Mag rapportoutput afkeuren zonder bronverwijzing.
- Mag technische schuld toevoegen bij ontbrekende tests.

Input:

- schema's
- voorbeelden
- rapporttemplate
- code zodra aanwezig

Output:

- Testplan.
- Validatiecriteria.
- Reviewbevindingen.

Kwaliteitscriteria:

- Bevindingen zijn reproduceerbaar.
- Validatie is gekoppeld aan risico.
- Bronverificatie is verplicht.

Actief wanneer:

- Code, schema's, rapportage of parseroutput verandert.

## Technical Writer

Verantwoordelijkheden:

- Houdt documentatie, prompts en changelog bij.
- Zorgt dat elke toekomstige sessie context uit de repo kan halen.
- Beheert prompt factory.

Bevoegdheden:

- Mag prompts aanpassen, splitsen, samenvoegen of archiveren.
- Mag docs herstructureren als dit duidelijkheid verbetert.

Input:

- alle docs
- `.codex/*`
- `prompts/*`

Output:

- Documentatie-updates.
- Promptupdates.
- Changelog.

Kwaliteitscriteria:

- Nederlands.
- Concreet genoeg voor uitvoering.
- Geen verborgen afhankelijkheid van chatcontext.

Actief wanneer:

- Elke sessie documentatie moet bijwerken of prompts moet voorbereiden.

## Release Manager

Verantwoordelijkheden:

- Beheert release-state, publicatievoorbereiding en releasecriteria.
- Bewaakt GitHub/GitHub Pages pad.
- Controleert of een release kandidaat klaar is.

Bevoegdheden:

- Mag releasepromotie voorstellen.
- Mag publicatie blokkeren bij ontbrekende criteria.

Input:

- `.codex/release-state.md`
- `.codex/roadmap.md`
- `CHANGELOG.md`
- build/testresultaten zodra aanwezig

Output:

- Release notes.
- Publicatieplan.
- Releasecriteria-updates.

Kwaliteitscriteria:

- Geen publicatie zonder expliciete readiness.
- GitHub Pages blijft voorbereid, niet uitgevoerd zonder opdracht.

Actief wanneer:

- Releasefase, publicatie of externe demo verandert.
