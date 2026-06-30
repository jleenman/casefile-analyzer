# Prompt 008 - Cloudflare Worker

## Doel

Ontwerp en implementeer een minimale serverless backend voor uploads, status en object storage.

## Context

De backend moet klein blijven en geen database introduceren.

## Inputbestanden

- `docs/architecture.md`
- `docs/privacy-security.md`
- `schemas/case.schema.json`
- `schemas/analysis-job.schema.json`

## Outputbestanden

- Worker-code wanneer expliciet binnen deze prompt uitgevoerd.
- Documentatie over endpoints, storage keys en security.

## Acceptatiecriteria

- Upload en status werken met synthetische data.
- Objecten zijn niet publiek leesbaar.
- `status.json` wordt betrouwbaar bijgewerkt.
- Privacy, bronverwijzingen en controleerbaarheid zijn leidend.
- Voeg tests of validatiecriteria toe.
- Eindig met een kleine commit of duidelijke wijzigingssamenvatting.
