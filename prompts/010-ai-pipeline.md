# Prompt 010 - AI Pipeline

## Doel

Ontwerp en implementeer een eerste AI-classificatiepipeline op chunks.

## Context

AI mag signalen voorstellen, maar niet zelfstandig juridische conclusies trekken.

## Inputbestanden

- `docs/research-methodology.md`
- `docs/signal-taxonomy.md`
- `schemas/evidence-item.schema.json`
- `schemas/signal.schema.json`

## Outputbestanden

- AI-provider abstractielaag.
- Prompttemplates of classificatie-instructies.
- Validatie voor outputschema.

## Acceptatiecriteria

- Output zonder bronverwijzing wordt afgekeurd.
- Confidence en onzekerheid worden vastgelegd.
- Providerdetails zijn geïsoleerd.
- Privacy, bronverwijzingen en controleerbaarheid zijn leidend.
- Voeg tests of validatiecriteria toe.
- Eindig met een kleine commit of duidelijke wijzigingssamenvatting.
