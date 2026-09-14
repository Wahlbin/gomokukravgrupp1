# UC-04: Starta spel mot dator

## Aktör
Spelare


## Mål
Att starta ett nytt parti mot en dator som motståndare i enspelarläge


## Förutsättningar
- Spelaren befinner sig i huvudmeny
- Spelaren behöver inte vara inloggad eller ha ett registrerat konto för att kunna spela fullt ut


## Huvudflöde
- Spelaren klickar på "spela"-knappen i huvudmeny
- Systemet ger spelaren möjlighet att välja spellägena: mot en robot, online eller lokalt på samma enhet
- Spelaren väljer enspelarläge (mot en robot)
- Systemet erbjuder alternativ för svårighetsgraderna "lätt", "mellan" och "svår"
- Spelaren klickar på den svårighetsgrad hen vill ha
- Systemet genererar spelruta på 15x15 linjer
- Systemet tilldelar sidorna färgerna svart och vitt
- Spelet startar och systemet tillämpar regeln att svart kör först

## Alternativa flöden
1. Avbryt innan start: Spelaren väljer att gå tillbaka till huvudmenyn innan svårighetsgrad har valts. Use caset avslutas

## Resultat
Ett nytt parti mot dator startas, spelbrädet visas och är redo för det första draget

## Test Case – UC-04 Starta spel mot dator - given when then

### TC-04a: Starta parti mot dator (huvudflöde)
Givet att spelaren befinner sig i huvudmenyn, utan krav på inloggning eller konto
När spelaren klickar på "Spela", väljer enspelarläge (mot en robot) och väljer en svårighetsgrad ("lätt", "mellan" eller "svår")
Då ska systemet generera ett spelbräde på 15×15 linjer, tilldela sidorna färgerna svart och vitt
Och partiet ska starta med regeln att svart kör först

### TC-04b: Avbryt innan start (alternativt flöde)
Givet att spelaren har valt enspelarläge men ännu inte valt svårighetsgrad
När spelaren väljer att gå tillbaka till huvudmenyn
Då ska use caset avslutas utan att något parti startas
