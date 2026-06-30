# Prompt 004 - Data Schemas

## Doel

Valideer en verfijn de JSON Schema's voor cases, evidence-items, messages, signals, analysis jobs en reports.

## Context

Schema's vormen het contract tussen parsers, analysepipeline en rapportgenerator.

## Inputbestanden

- `schemas/case.schema.json`
- `schemas/evidence-item.schema.json`
- `schemas/message.schema.json`
- `schemas/signal.schema.json`
- `schemas/analysis-job.schema.json`
- `schemas/report.schema.json`
- `docs/architecture.md`

## Outputbestanden

- Bijgewerkte schema's.
- Eventueel korte toelichting in `docs/architecture.md`.

## Acceptatiecriteria

- Alle schema's zijn geldige JSON Schema drafts.
- Bronverwijzingen zijn verplicht waar bevindingen worden vastgelegd.
- Schema's blijven klein maar bruikbaar.
- Privacy, bronverwijzingen en controleerbaarheid zijn leidend.
- Eindig met een kleine commit of duidelijke wijzigingssamenvatting.
