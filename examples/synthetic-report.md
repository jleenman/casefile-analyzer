# Synthetisch Voorbeeldrapport

Waarschuwing: dit rapport is fictief en geen juridisch advies. Het toont alleen hoe bronverwijzingen en controleerbare signalen eruit kunnen zien.

## Samenvatting

In de synthetische WhatsApp-export en transcriptie staan enkele mogelijke signalen van druk, dreiging, ongewenst contact en isolatie. De analyse is beperkt tot de aangeleverde voorbeeldbestanden.

## Scope en Beperkingen

Onderzochte bronnen:

| Bron-id | Bestand | Type | Beperking |
| --- | --- | --- | --- |
| SRC-001 | `examples/synthetic-whatsapp.txt` | WhatsApp TXT | Fictieve korte selectie |
| SRC-002 | `examples/synthetic-transcript.txt` | Transcript | Geen audio beschikbaar |

## Methode

Fragmenten zijn handmatig gemarkeerd aan de hand van de eerste signaaltaxonomie. Elk signaal verwijst naar bestand en regel of timestamp.

## Tijdlijn

| Datum/tijd | Gebeurtenis | Bron |
| --- | --- | --- |
| 12-05-2026 20:03 | Mogelijke dreiging met onaangekondigd langskomen | SRC-001 regel 6 |
| 13-05-2026 08:03 | Mogelijk isolatiesignaal: niet met anderen praten | SRC-001 regel 9 |
| 15-05-2026 22:32 | Mogelijke dreiging na herhaald bellen | SRC-001 regel 15 |
| 00:00:22 | Mogelijke juridische/sociale druk bij betrekken van anderen | SRC-002 timestamp 00:00:22 |

## Belangrijkste Signalen

### Dreiging

- Score: 4
- Confidence: middel
- Bron: `examples/synthetic-whatsapp.txt`, regel 6
- Fragment: "Als je mij blijft negeren kom ik straks langs."
- Toelichting: de uiting koppelt niet reageren aan onaangekondigd langskomen. Menselijke review moet context en veiligheidsrisico beoordelen.

### Isolatie

- Score: 3
- Confidence: middel
- Bron: `examples/synthetic-whatsapp.txt`, regel 9
- Fragment: "En praat niet met anderen hierover."
- Toelichting: mogelijk signaal van beperken van steun of externe bespreking.

### Juridische of sociale druk

- Score: 3
- Confidence: laag tot middel
- Bron: `examples/synthetic-transcript.txt`, timestamp 00:00:22
- Fragment: "Als jij anderen erbij haalt, wordt het voor jou vervelend."
- Toelichting: de consequentie is niet concreet, maar de voorwaardelijke druk is relevant.

## Onzekerheden

- De voorbeelden zijn kort en synthetisch.
- Er is geen volledige conversatiecontext.
- Er is geen audio voor transcriptcontrole.
- Geen juridische conclusie kan uit deze voorbeelden worden getrokken.

## Bijlage met Bronverwijzingen

| Signaal-id | Categorie | Bron | Positie |
| --- | --- | --- | --- |
| SIG-001 | Dreiging | `examples/synthetic-whatsapp.txt` | regel 6 |
| SIG-002 | Isolatie | `examples/synthetic-whatsapp.txt` | regel 9 |
| SIG-003 | Dreiging | `examples/synthetic-whatsapp.txt` | regel 15 |
| SIG-004 | Juridische/sociale druk | `examples/synthetic-transcript.txt` | 00:00:22 |
