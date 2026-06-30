# Next Task

ID: CF-003

Titel: Herstructureer prompts tot prompt factory met metadata

Eigenaar: Technical Writer

Rol actief: Technical Writer

Complexiteit: M

Prioriteit: P0

Geschatte sessie: ongeveer 1 uur

## Context

De map `prompts/` bevat eerste promptbestanden. Vanaf nu is deze map volledig door Codex beheerd en moet zij functioneren als uitvoerbare ontwikkelpipeline. Iedere prompt moet een uniek ID, doel, context, benodigde input, verwachte output, acceptatiecriteria en afhankelijkheden bevatten.

## Inputbestanden

- `prompts/README.md`
- `prompts/*.md`
- `.codex/prompt-history.md`
- `.codex/backlog.md`
- `.codex/roadmap.md`
- `docs/repository-operating-manual.md`

## Outputbestanden

- Bijgewerkte `prompts/README.md`
- Bijgewerkte promptbestanden
- Eventueel `prompts/archive/README.md`
- Bijgewerkte `.codex/prompt-history.md`
- Bijgewerkte `.codex/backlog.md`
- Nieuwe `.codex/next-task.md`
- Bijgewerkte `.codex/daily-log.md`
- Bijgewerkte `CHANGELOG.md`

## Acceptatiecriteria

- Iedere prompt heeft expliciete metadata.
- Prompts vormen samen een logische ontwikkelpipeline.
- Geen prompt voert direct werk uit; prompts instrueren toekomstige Codex-runs.
- Privacy, bronverwijzingen en controleerbaarheid zijn leidend.
- Afgeronde of vervangen prompts worden in `prompt-history.md` genoteerd.
- De sessie eindigt met een nieuwe hoogste-prioriteitstaak in `.codex/next-task.md`.

## Stopcondities

Stop en schrijf een vraag in `.codex/human-inbox.md` als een keuze nodig is over publicatie, accounts, API keys of echte partnerdata.
