# Udstillingslys

En lille webapp til at beregne lys i et udstillingsmiljø. Åbn `index.html` direkte i en browser – der er ingen build-trin eller afhængigheder.

## Beregninger

- **Spot på værk** – belysningsstyrke (lux) på midten af et værk på væggen ud fra skinnehøjde, vinkel fra lodret (30°-reglen), lysstyrke i candela (eller anslået fra lumen), spredningsvinkel, dæmpning og antal spots. Viser afstand fra væg, lyskeglens størrelse og et snit af rummet.
- **Lysdosis pr. år** – luxtimer pr. år (lux × timer/dag × dage/år) sammenholdt med CIE 157:2004. Viser maks. lux, timer og udstillingsdage inden for anbefalingen.
- **Rumbelysning** – antal armaturer efter lumenmetoden, N = E·A / (Φ·UF·MF), med rumindeks, forslag til net, afstand mellem armaturer og effekt pr. m².

Genstandens lysfølsomhed vælges øverst og bruges i alle tre beregninger:

| Følsomhed | Maks. lux | Maks. luxtimer/år |
|---|---|---|
| Ufølsom | ingen grænse | ingen grænse |
| Lav | 200 | 600.000 |
| Middel | 50 | 150.000 |
| Høj | 50 | 15.000 |

Indtastninger gemmes lokalt i browseren. Alle tal er overslag – kontrollér med luxmeter på stedet.

# Indretning af rum

`indretning.html` er et planlægningsværktøj til at indrette et udstillingsrum set oppefra. Også her uden build-trin – åbn filen i en browser.

## Elementer

- **Montrer** – vægmontre, fritstående montre, bordmontre og søjlemontre.
- **Vægge og åbninger** – skillevægge, døre/åbninger, vinduer og afspærringer.
- **Lys** – spots (med monteringshøjde, strålevinkel, vinkel fra lodret og sigtehøjde), downlights og lysskinner. Lyskeglen tegnes i planen, og panelet viser hvor langt ude lyset rammer, og hvor stor keglen er.
- **Møbler og værker** – podier/sokler, bænke, tekststandere, skærme og værker på væg.

Elementer flyttes med musen eller piletasterne, drejes med det runde håndtag og ændres i størrelse med de firkantede. Vægmontrer, værker, skærme, døre og vinduer lægger sig op ad nærmeste væg. Alle mål kan også tastes direkte i panelet til højre. Hvert element får en kode (M1, V1, L1 …) og kan have en note om indhold.

Værktøjet markerer elementer der overlapper eller står uden for rummet, og passager der er smallere end den valgte mindste gangbredde (standard 0,9 m). Listen under planen fungerer som stykliste.

## Gem og hent

- **Gem** gemmer rummet under sit navn i browseren; **Gemte rum** viser alle gemte rum med miniature, søgning, åbn og slet.
- **Gem som kopi** laver en variant af et rum, fx til at afprøve en alternativ opstilling.
- Rum kan **eksporteres** som JSON-fil (enkeltvis eller alle) og **importeres** igen – brug det til backup eller til at dele med kolleger.
- Arbejdet gemmes løbende som kladde, så intet går tabt ved genindlæsning. Fortryd/gentag med Ctrl+Z / Ctrl+Y.
- **Udskriv** giver en plantegning med stykliste (kan gemmes som PDF).

# Ophængning af værker

`ophaeng.html` er et værktøj til at planlægge, hvordan værker hænger på én væg, set forfra. Også her uden build-trin – åbn filen i en browser. Alle mål er i millimeter, og højder måles fra gulvet.

## Væg og værker

- **Væg** – bredde, højde, vægfarve og en øjenhøjde-linje (til værkets centrum, standard 1500 mm).
- **Værker** – titel, kunstner, år, yderste mål, ramme, dybde, ophængning (én krog, to kroge eller skinne) og eventuelt et billede. «Fra billeder …» opretter værker direkte ud fra billedfiler.
- **Hindringer** – døre, kontakter og andet, der skal holdes frit. De gælder alle forslag.
- **Forslag** – værkerne er fælles; placeringen gemmes pr. forslag, så flere opstillinger kan sammenlignes. Forslag kan kopieres.

## Placering

Værker trækkes med musen eller fingeren (to fingre zoomer), og piletaster finjusterer (10 mm, Skift 100 mm, Alt 1 mm). De klikker på plads efter vægkanter, gulv, loft, øjenhøjde og andre værkers kanter og midter, og efter et fast mellemrum, hvis det er sat. Gitter kan slås til. Hold Alt nede for at flytte uden hjælp. Under træk vises hjælpelinjer, og for det valgte værk vises afstande til nabo, væg, gulv og loft.

Under tegningen kan flere valgte værker **justeres** (venstre/centrum/højre, top/midte/bund), **fordeles** med lige stor afstand, stilles med **fast mellemrum** eller sættes **på øjenhøjde**.

**Højdemål:** tallene i panelet og i montagelisten kan måles fra gulv til værkets underkant, centrum eller overkant (vælges under «Hjælp ved placering»; standard er underkant).

## Bemærkninger, montageliste og udskrift

- Værktøjet markerer værker, der overlapper, rager ud over væggen eller dækker en hindring.
- **Montageliste** med afstand fra væggens venstre kant og højde fra gulv for underkant, centrum og overkant samt krogenes placering. Kan hentes som CSV.
- **Udskriv** giver en tegning af væggen med montageliste på A3 (kan gemmes som PDF), enten tilpasset siden eller i målestok 1:10, 1:20, 1:25 eller 1:50.

## Gem og hent

Arbejdet gemmes løbende i browseren (billeder skaleres ned til maks. 900 px). Planen kan eksporteres som JSON-fil og importeres igen. Fortryd/gentag med Ctrl+Z / Ctrl+Y. «Indlæs eksempel» viser en færdig væg med to forslag.
