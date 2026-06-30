# Known Risks

## Actieve Risico's

| ID | Risico | Kans | Impact | Mitigatie | Eigenaar |
| --- | --- | --- | --- | --- | --- |
| KR-001 | AI-output bevat conclusies zonder bron | Middel | Hoog | Schema's en rapportgenerator moeten bronverwijzingen verplichten | QA Engineer |
| KR-002 | Gebruikers interpreteren output als juridisch advies | Middel | Hoog | Disclaimers, methodiek en rapporttaal blijven expliciet | Product Owner |
| KR-003 | Gevoelige data lekt via opslag of LLM-provider | Laag tot middel | Zeer hoog | Synthetische demo, security review, geen echte data zonder toestemming | Security & Privacy Reviewer |
| KR-004 | Prompt pipeline drijft af van MVP-doel | Middel | Middel | Roadmap en next-task discipline afdwingen | Product Owner |
| KR-005 | Bronverwijzingen zijn te grof voor professionele controle | Middel | Hoog | Parsercriteria en bronverificatie vroeg ontwerpen | QA Engineer |

## Reviewritme

Controleer dit bestand bij iedere sessie die architectuur, dataflow, AI of rapportage wijzigt.
