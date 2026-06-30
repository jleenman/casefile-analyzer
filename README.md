# casefile-analyzer

`casefile-analyzer` is een open-source MVP voor het analyseren van omvangrijke communicatie- en documentdossiers. Het project start documentatie- en planningsgericht: deze repository bevat eerst de visie, methodiek, scope, schema's, voorbeelden en toekomstige Codex-prompts. Er is in deze stap nog geen applicatiecode.

GitHub: https://github.com/jleenman/casefile-analyzer

## Probleemstelling

Professionals en betrokkenen krijgen soms grote hoeveelheden materiaal: WhatsApp-exports, transcripties, PDF's, DOCX-bestanden, tekstbestanden en later mogelijk audio/video. De relevante signalen zitten verspreid over duizenden regels, verschillende bestandssoorten en lange tijdlijnen. Handmatige analyse is traag, foutgevoelig en afhankelijk van vooraf weten waarnaar gezocht moet worden.

## Oplossing

De tool moet materiaal structureren, signalen detecteren en bevindingen onderbouwen met controleerbare bronverwijzingen. Denk aan signalen rond dreiging, intimidatie, stalking, dwingende controle, escalatie, isolatie, financiële controle en juridische druk.

De kern is niet "automatisch bewijs verzamelen", maar evidence intelligence: grote hoeveelheden materiaal terugbrengen tot een navolgbaar onderzoeksdossier.

## MVP-doel

De eerste MVP moet aantonen dat het mogelijk is om:

- bestanden te uploaden of lokaal te verwerken;
- inhoud te parsen naar uniforme records;
- bronverwijzingen per fragment te behouden;
- signalen en patronen te markeren;
- een controleerbaar Markdown-rapport te genereren;
- alle AI-output te koppelen aan concrete broninformatie.

## Niet-doelen

- Geen definitief juridisch oordeel.
- Geen vervanging van advocaten, hulpverleners, onderzoekers of rechters.
- Geen productieplatform in de eerste demo.
- Geen gebruikersaccounts in de eerste demo.
- Geen database in de eerste architectuur.
- Geen verwerking van echte gevoelige dossiers in demo's zonder expliciete veiligheidsmaatregelen.

## Globale Architectuur

De beoogde low-budget architectuur:

- statische Nuxt frontend op GitHub Pages;
- Cloudflare Worker of vergelijkbare serverless backend;
- S3/R2 object storage voor cases, uploads, analyses en rapporten;
- JSON/JSONL-bestanden als opslagstructuur;
- `status.json` per case;
- analysejobs als bestanden;
- AI-provider abstractielaag;
- rapporten terugschrijven naar object storage.

## Status

Status: planning/documentation first.

Deze repository bevat eerst de inhoudelijke basis, schema's, voorbeelddata en prompts voor latere Codex-runs. Maak nog geen applicatiecode voordat scope, datacontracten, privacy-eisen en verificatiecriteria expliciet zijn vastgelegd.

Publicatiestatus: publieke GitHub-repository op `main`.

## Open Source

Dit project wordt gepubliceerd onder de MIT-licentie. Zie `LICENSE`.

Bijdragen zijn welkom zodra de projectworkflow en scope duidelijk gevolgd worden. Zie `CONTRIBUTING.md` en `SECURITY.md`.

## Waarschuwing

Deze tool geeft geen juridisch advies en geen definitieve juridische kwalificaties. Uitvoer is bedoeld als onderzoeks- en ordeningshulp. Elke bevinding moet door een mens worden gecontroleerd aan de hand van de bronverwijzingen.
