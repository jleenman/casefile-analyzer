# Prompt Factory

Deze map is volledig door Codex beheerd. Prompts vormen samen een uitvoerbare ontwikkelpipeline voor autonome sessies.

Codex mag prompts schrijven, aanpassen, verwijderen, opsplitsen, samenvoegen en vervangen wanneer dit de pipeline beter maakt. Registreer wijzigingen in `.codex/prompt-history.md`.

## Verplichte promptvelden

Iedere prompt bevat:

- uniek ID;
- doel;
- context;
- benodigde input;
- verwachte output;
- acceptatiecriteria;
- afhankelijkheden.

## Gebruik

1. Start nooit rechtstreeks vanuit deze map.
2. Lees eerst `.codex/project-state.md`, `.codex/blocked.md`, `.codex/human-inbox.md` en `.codex/next-task.md`.
3. Gebruik een prompt alleen als `next-task.md` daarom vraagt.
4. Voer precies één taak per sessie uit.
5. Werk na afloop `CHANGELOG.md`, `.codex/backlog.md`, `.codex/roadmap.md`, `.codex/prompt-history.md`, `.codex/daily-log.md` en `.codex/next-task.md` bij.

## Leidend principe

Privacy, bronverwijzingen en controleerbaarheid zijn leidend. Geen prompt mag vragen om conclusies zonder bron of definitieve juridische kwalificaties.
