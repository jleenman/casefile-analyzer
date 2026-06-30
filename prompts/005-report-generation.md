# Prompt 005 - Rapportgeneratie

## Doel

Ontwerp de eerste rapportgenerator zonder AI en met synthetische input.

## Context

Rapporten moeten controleerbaar zijn en mogen geen bevindingen zonder bron bevatten.

## Inputbestanden

- `docs/report-template.md`
- `schemas/report.schema.json`
- `schemas/signal.schema.json`
- `examples/synthetic-report.md`

## Outputbestanden

- Ontwerpnotities of pseudocode in documentatie.
- Later pas code wanneer dat expliciet wordt gevraagd.

## Acceptatiecriteria

- Rapportstructuur volgt de template.
- Elke bevinding heeft minimaal een bronbestand en regel/timestamp/pagina.
- Onzekerheden zijn zichtbaar.
- Privacy, bronverwijzingen en controleerbaarheid zijn leidend.
- Eindig met een kleine commit of duidelijke wijzigingssamenvatting.
