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
