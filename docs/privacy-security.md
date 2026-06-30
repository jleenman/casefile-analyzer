# Privacy en Security

De tool verwerkt potentieel zeer gevoelige persoonsgegevens. Privacy en veiligheid moeten vanaf het begin leidend zijn.

## Gevoelige Persoonsgegevens

Dossiers kunnen bevatten:

- namen, adressen en telefoonnummers;
- medische of psychologische informatie;
- informatie over relaties en gezin;
- juridische correspondentie;
- locatiegegevens;
- gegevens over geweld, dreiging of misbruik.

## Kinderen

Gegevens over kinderen vragen extra terughoudendheid:

- minimaliseer opslag;
- anonimiseer demo's;
- toon alleen relevante fragmenten;
- vermijd onnodige herpublicatie in rapporten;
- markeer kind-gerelateerde signalen voor menselijke review.

## Encryptie als Doel

Encryptie is een architectuurdoel:

- encryptie in transit;
- encryptie at rest in object storage;
- aparte sleutels per omgeving of tenant zodra accounts bestaan;
- geen secrets in frontendcode;
- veilige secret storage voor serverless functies.

## Minimale Opslag

Bewaar alleen wat nodig is:

- originele upload;
- geëxtraheerde tekst met bronposities;
- analyse-output met bronverwijzingen;
- rapport;
- statusmetadata.

Latere versies moeten bewaartermijnen, export en verwijdering ondersteunen.

## Object Storage Risks

Risico's:

- verkeerd ingestelde publieke buckets;
- voorspelbare object keys;
- langdurige opslag zonder verwijderbeleid;
- onvoldoende scheiding tussen cases;
- metadata-lekken via bestandsnamen.

Mitigaties:

- private buckets;
- onvoorspelbare case-id's;
- signed URLs met korte levensduur;
- minimale metadata;
- logging van toegang tot objecten.

## API/LLM Risico's

Risico's:

- versturen van gevoelige data naar externe providers;
- modelhallucinaties;
- verlies van bronkoppeling;
- opslag of training door derde partijen;
- prompt-injection vanuit dossierinhoud.

Eisen:

- geen trainingsdata zonder expliciete toestemming;
- providerkeuze documenteren;
- prompts moeten bronverwijzingen afdwingen;
- output zonder bronverwijzing wordt afgekeurd;
- echte dossiers alleen verwerken na expliciete veiligheidsafweging.

## Verwijderfunctie

Een verwijderfunctie is een latere harde eis. Deze moet minimaal:

- originele uploads verwijderen;
- afgeleide JSON/JSONL verwijderen;
- analysejobs verwijderen;
- rapporten verwijderen;
- statusbestanden bijwerken;
- verwijdering controleerbaar loggen zonder gevoelige inhoud te bewaren.

## Veilige Demo

De eerste demo gebruikt uitsluitend synthetische data. Geen echte namen, echte organisaties, echte telefoonnummers of herleidbare situaties.
