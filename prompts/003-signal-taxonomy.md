# Prompt 003 - Signaaltaxonomie

## Doel

Maak de signaaltaxonomie geschikt voor eerste regelgebaseerde en AI-ondersteunde classificatie.

## Context

Taxonomie moet bruikbaar zijn zonder juridische eindconclusies te trekken.

## Inputbestanden

- `docs/signal-taxonomy.md`
- `schemas/signal.schema.json`
- `examples/synthetic-whatsapp.txt`
- `examples/synthetic-transcript.txt`

## Outputbestanden

- Bijgewerkte `docs/signal-taxonomy.md`
- Eventueel bijgewerkte `schemas/signal.schema.json`

## Acceptatiecriteria

- Elke categorie heeft definitie, voorbeelden, uitsluitingen, ernstscore en vereiste broninformatie.
- Categorieën zijn concreet genoeg voor annotatie.
- Geen conclusie zonder bronverwijzing.
- Privacy, bronverwijzingen en controleerbaarheid zijn leidend.
- Eindig met een kleine commit of duidelijke wijzigingssamenvatting.
