# Onderzoeksmethodiek

De methodiek maakt strikt onderscheid tussen feit, signaal, patroon, interpretatie en juridische conclusie.

## Begrippen

- Feit: een controleerbaar gegeven uit een bron, bijvoorbeeld een berichtregel, datum, afzender of transcriptsegment.
- Signaal: een fragment dat mogelijk relevant is voor een thema, zoals dreiging of stalking.
- Patroon: meerdere signalen die samen een terugkerende gedragslijn of escalatie suggereren.
- Interpretatie: een voorzichtige duiding van feiten en patronen.
- Juridische conclusie: een kwalificatie binnen een juridisch kader. De tool mag dit niet als definitieve waarheid presenteren.

## Signalen Vinden

Signalen kunnen worden gevonden via:

- woordenlijsten en regels;
- tijdlijnanalyse;
- frequentie en herhaling;
- context rond berichten;
- semantische AI-classificatie per chunk;
- vergelijking tussen thema's, bijvoorbeeld dreiging plus isolatie plus juridische druk.

Elke detectie moet minimaal bevatten:

- bronbestand;
- positie in bron, zoals regelnummer, pagina, timestamp of segment-id;
- betrokken afzender of spreker indien beschikbaar;
- datum/tijd indien beschikbaar;
- fragmenttekst of korte samenvatting;
- reden waarom het fragment relevant kan zijn.

## Ruis Uitsluiten

Ruis wordt beperkt door:

- neutrale context mee te nemen;
- citaten niet los van de conversatie te beoordelen;
- uitsluitingscriteria per signaalcategorie te hanteren;
- herhaalde automatische detecties samen te voegen;
- onzekerheid expliciet te markeren;
- menselijke review verplicht te houden.

## AI-output Controleren

AI-output is alleen bruikbaar als:

- alle bevindingen bronverwijzingen hebben;
- het model geen feiten toevoegt die niet in de bron staan;
- onzekerheid zichtbaar is;
- juridische kwalificaties als mogelijke interpretatie worden benoemd, niet als conclusie;
- representatieve bronfragmenten controleerbaar zijn.

## Onzekerheid

Onzekerheid wordt weergegeven met:

- confidence-score of tekstlabel;
- reden voor onzekerheid;
- alternatieve interpretatie;
- ontbrekende context;
- aanbeveling voor menselijke controle.

Voorbeeld: "Mogelijk signaal van intimidatie, confidence: middel. Context ontbreekt omdat eerdere berichten in dezelfde conversatie niet beschikbaar zijn."
