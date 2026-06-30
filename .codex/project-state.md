# Project State

Laatste update: 2026-06-30

## Project

Naam: `casefile-analyzer`

Doel: open-source MVP voor het analyseren van omvangrijke communicatie- en documentdossiers met controleerbare bronverwijzingen.

GitHub: https://github.com/jleenman/casefile-analyzer

## Huidige fase

Fase: Planning

Status: documentatie- en workflowbasis. Er is nog geen applicatiecode, geen package manager setup en geen Nuxt/Worker-installatie.

## Huidige focus

De repository wordt ingericht als zelforganiserend softwareproject. Iedere toekomstige Codex-sessie moet zonder chatcontext kunnen starten, exact een taak uitvoeren en de volgende taak voorbereiden.

## Harde uitgangspunten

- Geen conclusies zonder bron.
- Geen definitieve juridische kwalificaties.
- Privacy-by-design.
- Synthetische data voor demo's.
- Kleine sessies van ongeveer een uur.
- Iedere sessie eindigt met bijgewerkte `.codex/next-task.md`.

## Belangrijkste documenten

- `README.md`: projectoverzicht.
- `AGENTS.md`: werkinstructies voor Codex.
- `docs/repository-operating-manual.md`: handboek voor autonome sessies.
- `.codex/backlog.md`: Markdown Kanban.
- `.codex/next-task.md`: enige uitvoerbare taak voor de volgende sessie.

## Current State

- Documentation foundation bestaat.
- Eerste JSON Schema's bestaan.
- Synthetische voorbeelden bestaan.
- Repository Operating System is toegevoegd.
- Dagelijkse Codex-automatisering is geconfigureerd in de Codex-app.
- Open-source publicatiebasis is toegevoegd met MIT-licentie, contributing-richtlijnen en security policy.
- Repository is publiek gepubliceerd op GitHub.

## Known Issues

- Er is nog geen applicatiecode of testsetup.
- Automatisering moet stoppen bij verplichte openstaande input in `human-inbox.md`.

## Next Actions

Voer uitsluitend de taak in `.codex/next-task.md` uit.

## Automatisering

Automatisering: `casefile-analyzer-daily-next-task`

Schema: dagelijks om 09:00 lokale tijd.

Runtime: lokaal in de Codex-app, niet cloud-hosted.

Gedrag: stop bij verplichte openstaande input in `.codex/human-inbox.md` of actieve blockers in `.codex/blocked.md`; voer anders uitsluitend `.codex/next-task.md` uit.

Onderbreking: als het systeem of de Codex-app sluit terwijl een taak loopt, kan de run worden afgebroken met gedeeltelijke bestandswijzigingen. De volgende sessie moet starten met git status, `.codex/project-state.md`, `.codex/blocked.md`, `.codex/human-inbox.md` en `.codex/next-task.md`, en moet eerst de half-afgeronde taak stabiliseren voordat nieuw werk wordt gestart.
