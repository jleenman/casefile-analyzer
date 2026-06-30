# Prompt 009 - File Processing

## Doel

Implementeer de eerste lokale parsers voor WhatsApp TXT, TXT, PDF en DOCX.

## Context

Parsing moet bronposities bewaren. Zonder bronpositie is output niet bruikbaar voor rapportage.

## Inputbestanden

- `docs/file-processing-roadmap.md`
- `schemas/evidence-item.schema.json`
- `schemas/message.schema.json`
- `examples/synthetic-whatsapp.txt`
- `examples/synthetic-transcript.txt`

## Outputbestanden

- Parsercode.
- Parsertests.
- Voorbeeld JSON/JSONL-output indien passend.

## Acceptatiecriteria

- Elke record heeft bronbestand en positie.
- WhatsApp multiline berichten worden correct verwerkt.
- Tests gebruiken synthetische data.
- Privacy, bronverwijzingen en controleerbaarheid zijn leidend.
- Eindig met een kleine commit of duidelijke wijzigingssamenvatting.
