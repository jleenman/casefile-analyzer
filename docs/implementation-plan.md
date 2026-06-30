# Implementatieplan

## 1. Documentatie en Schema's

Doel: repository foundation met visie, scope, methodiek, taxonomie, architectuur en JSON Schema's.

Acceptatie: alle docs bestaan, schema's zijn valide JSON en voorbeelden sluiten aan op schema's.

## 2. Synthetische Testdata

Doel: representatieve maar fictieve WhatsApp- en transcriptvoorbeelden.

Acceptatie: geen echte persoonsgegevens; voorbeelden bevatten neutrale tekst en enkele duidelijke signalen.

## 3. Lokale Parser

Doel: CLI of script dat WhatsApp TXT, TXT, PDF en DOCX omzet naar evidence-items.

Acceptatie: output bevat bronverwijzingen; parser heeft tests met synthetische data.

## 4. Rapportgenerator zonder AI

Doel: rapport genereren op basis van handmatig gemarkeerde of regelgebaseerde signalen.

Acceptatie: Markdown-rapport bevat samenvatting, bronnen, tijdlijn en bronfragmenten.

## 5. AI-classificatie op Chunks

Doel: chunks classificeren tegen de signaaltaxonomie.

Acceptatie: AI-output valideert tegen schema; geen signaal zonder bronverwijzing.

## 6. Bronverificatie

Doel: controleren dat elk rapportfragment terug te vinden is in de originele of geëxtraheerde bron.

Acceptatie: rapportgeneratie faalt bij ontbrekende bronverwijzing.

## 7. Nuxt Demo

Doel: statische demo voor upload, case-status en rapportweergave.

Acceptatie: geen gebruikersaccounts; synthetische demo werkt lokaal en statisch waar mogelijk.

## 8. Serverless Opslag/Processing

Doel: Worker en object storage integreren.

Acceptatie: upload, status.json, jobbestand en rapportbestand werken end-to-end met synthetische data.

## 9. Security Review

Doel: privacy- en securityrisico's beoordelen voor pilotgebruik.

Acceptatie: risico's, mitigaties en resterende beperkingen zijn gedocumenteerd.

## 10. Partnerdemo

Doel: gecontroleerde demo voor praktijk- en validatiepartners.

Acceptatie: demo gebruikt uitsluitend synthetische of expliciet vrijgegeven data; feedbackvragen zijn voorbereid.
