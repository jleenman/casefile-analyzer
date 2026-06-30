# Architectuur

De beoogde architectuur is low-budget, transparant en geschikt voor een open-source MVP.

## Overzicht

- Frontend: statische Nuxt-app op GitHub Pages.
- Backend: Cloudflare Worker of vergelijkbare serverless functie.
- Opslag: S3/R2 object storage.
- Database: geen database in de eerste versie.
- Dataformaat: JSON en JSONL.
- AI: provider abstractielaag.
- Rapportage: Markdown terugschrijven naar object storage.

## Case-structuur in Object Storage

Voorbeeld:

```text
cases/{caseId}/
  status.json
  uploads/{uploadId}/original
  uploads/{uploadId}/metadata.json
  extracted/{sourceId}.jsonl
  jobs/{jobId}.json
  signals/{jobId}.jsonl
  reports/{reportId}.md
```

## status.json per Case

`status.json` bevat de actuele staat:

- case-id;
- aangemaakte datum;
- uploadstatus;
- extractiestatus;
- analysejobstatus;
- rapportstatus;
- foutmeldingen zonder gevoelige detailinhoud;
- laatste update.

## Analysejobs als Bestanden

Elke analysejob is een JSON-bestand met:

- job-id;
- case-id;
- inputbronnen;
- gekozen taxonomieversie;
- pipeline-stappen;
- status;
- foutmelding;
- outputlocaties.

Dit maakt verwerking inspecteerbaar zonder database.

## AI-provider Abstractielaag

De AI-laag moet:

- chunks ontvangen met bronmetadata;
- alleen gestructureerde output teruggeven;
- confidence en onzekerheid ondersteunen;
- provider-specifieke details isoleren;
- output valideren tegen schema's;
- bevindingen zonder bronverwijzing afwijzen.

## Rapportgeneratie

De rapportgenerator leest:

- case metadata;
- evidence-items;
- signalen;
- patronen;
- onzekerheden.

Output:

- Markdown-rapport in object storage;
- later optioneel PDF;
- bijlage met bronverwijzingen.

## Belangrijkste Architectuurkeuzes

- Geen database verlaagt kosten en complexiteit, maar beperkt querymogelijkheden.
- JSON/JSONL maakt inspectie en versiebeheer eenvoudiger.
- Object storage vraagt strikte aandacht voor toegang, keys en verwijdering.
- Serverless verwerking is geschikt voor demo's, maar grote bestanden kunnen later queueing of batch jobs vereisen.
