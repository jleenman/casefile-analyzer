# Prompt 006 - Architectuurontwerp

## Doel

Werk de low-budget architectuur uit tot concrete componenten, opslagpaden en datastromen.

## Context

Beoogd: statische Nuxt frontend, Cloudflare Worker, S3/R2 object storage, geen database, JSON/JSONL.

## Inputbestanden

- `docs/architecture.md`
- `docs/privacy-security.md`
- `schemas/*.json`

## Outputbestanden

- Bijgewerkte `docs/architecture.md`
- Eventueel schema-aanpassingen wanneer datacontracten ontbreken.

## Acceptatiecriteria

- Componenten, opslagstructuur en jobflow zijn concreet.
- Geen database wordt als bewuste MVP-keuze onderbouwd.
- Object storage-risico's zijn benoemd.
- Privacy, bronverwijzingen en controleerbaarheid zijn leidend.
- Eindig met een kleine commit of duidelijke wijzigingssamenvatting.
