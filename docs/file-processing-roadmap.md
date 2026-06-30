# File Processing Roadmap

## WhatsApp Export

Parsingstrategie: TXT-export parseren op datum, tijd, afzender en berichttekst. ZIP-export behandelen als container met TXT en optionele mediareferenties.

Bronverwijzing: bestandsnaam, regelnummer, datum/tijd, afzender, bericht-id.

Risico's: verschillende datumnotaties, multiline berichten, systeemmeldingen, verwijderde media, exporttaal.

MVP-status: in scope voor v1.

## TXT

Parsingstrategie: regels of alinea's opsplitsen, optioneel timestamps herkennen.

Bronverwijzing: bestandsnaam, regelnummer of tekstoffset.

Risico's: ontbrekende structuur, onbekende spreker, onduidelijke datums.

MVP-status: in scope voor v1.

## PDF

Parsingstrategie: tekstextractie per pagina; OCR later voor gescande PDF's.

Bronverwijzing: bestandsnaam, pagina, tekstblok of regelpositie indien beschikbaar.

Risico's: slechte extractievolgorde, tabellen, scans, kolommen, verborgen tekstlagen.

MVP-status: in scope voor tekst-PDF's; OCR later.

## DOCX

Parsingstrategie: paragrafen, tabellen en metadata uitlezen.

Bronverwijzing: bestandsnaam, paragraafindex, tabelcel indien relevant.

Risico's: opmerkingen, track changes, kop/voetteksten, tabellen.

MVP-status: in scope voor v1.

## Audio

Parsingstrategie: transcriptie met timestamps en sprekerherkenning waar mogelijk.

Bronverwijzing: bestand, starttijd, eindtijd, sprekerlabel, transcriptsegment.

Risico's: transcriptiefouten, sprekerverwisseling, achtergrondgeluid, toestemming.

MVP-status: later.

## Video

Parsingstrategie: audio extraheren voor transcriptie; frames selecteren voor OCR of visuele context.

Bronverwijzing: bestand, timestamp, transcriptsegment, frame-id.

Risico's: hoge kosten, privacygevoelige beelden, onnauwkeurige OCR, contextverlies.

MVP-status: later.

## Afbeeldingen

Parsingstrategie: OCR en metadata-extractie, later object/contextdetectie alleen met strikte beperkingen.

Bronverwijzing: bestand, OCR-blok, bounding box indien beschikbaar.

Risico's: OCR-fouten, gevoelige personen op beeld, metadata-lekken.

MVP-status: later.

## E-mail

Parsingstrategie: `.eml` of `.mbox` parseren naar headers, body, attachments en threadrelaties.

Bronverwijzing: message-id, datum, afzender, ontvanger, subject, attachment-id.

Risico's: replies met geciteerde tekst, forwards, HTML, attachments, BCC/privacy.

MVP-status: later.
