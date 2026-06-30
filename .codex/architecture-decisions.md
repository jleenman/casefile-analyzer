# Architecture Decision Records

Iedere belangrijke beslissing krijgt een ADR met context, alternatieven, beslissing, motivatie, gevolgen en revisiedatum.

## ADR-001 - Documentation-first repository

Datum: 2026-06-30

Revisiedatum: 2026-07-30

### Context

Het project moet starten zonder applicatiecode, zodat scope, methodiek, privacy-eisen en bronverwijzingen eerst duidelijk zijn.

### Alternatieven

- Direct een Nuxt/Worker-app scaffolden.
- Eerst alleen een README schrijven.
- Eerst een volledige documentatie- en planningsbasis maken.

### Beslissing

Start met documentatie, schema's, synthetische voorbeelden en workflowbestanden. Voeg nog geen applicatiecode toe.

### Motivatie

Het domein is gevoelig. Vroege code zonder methodiek vergroot risico op oncontroleerbare AI-output, privacyfouten en verkeerde verwachtingen.

### Gevolgen

- Volgende Codex-runs hebben duidelijke context.
- Implementatie start later en kleiner.
- Demo-ontwikkeling wordt afhankelijk van gedocumenteerde acceptatiecriteria.

## ADR-002 - Repository Operating System in `.codex`

Datum: 2026-06-30

Revisiedatum: 2026-07-30

### Context

Toekomstige Codex-sessies mogen niet afhankelijk zijn van eerdere chatcontext. De repository moet zelf de planning en toestand bevatten.

### Alternatieven

- Chatcontext gebruiken als geheugen.
- Issues of externe projectmanagementtools gebruiken.
- Een repository-native `.codex` operating-system gebruiken.

### Beslissing

Gebruik `.codex/` als door Codex beheerde state-laag met project state, backlog, roadmap, next task, human inbox, research queue, ADR's en logs.

### Motivatie

Markdown in de repository is transparant, versieerbaar, open-source vriendelijk en direct leesbaar voor iedere sessie.

### Gevolgen

- Iedere sessie start met `.codex/project-state.md`, `.codex/blocked.md`, `.codex/human-inbox.md` en `.codex/next-task.md`.
- Codex moet aan het einde van elke sessie een nieuwe next task genereren.
- Externe automatisering kan dezelfde workflow uitvoeren.

## ADR-003 - Geen database in eerste MVP-architectuur

Datum: 2026-06-30

Revisiedatum: 2026-08-15

### Context

De MVP moet low-budget en inspecteerbaar blijven.

### Alternatieven

- Relationele database.
- Document database.
- Object storage met JSON/JSONL.

### Beslissing

Gebruik object storage met JSON/JSONL en `status.json` per case.

### Motivatie

Dit verlaagt kosten en maakt analyse-output inspecteerbaar. Voor de eerste demo zijn querymogelijkheden minder belangrijk dan controleerbaarheid.

### Gevolgen

- Querying is beperkt.
- Bestandsstructuur en schema's moeten strikt blijven.
- Later kan een database worden toegevoegd als ADR.
