# UC-07: Starta om snabbt

## Aktör
Spelare

## Mål
Att använda en funktion för att snabbt starta om ett pågående eller precis avslutat parti

## Förutsättningar
Ett parti är igång eller har precis avslutat (Via vinst, oavgjort eller lämnat)

## Huvudflöde
- Spelaren väljer funktionen för att snabbt starta om i gränssnittet
- Systemet nollställer spelbrädan och rensar bort alla placerade stenar
- Systemet ser till att färgerna svart och vit är tilldelade
- Systemet tillämpar regeln att spelaren med svarta stenar gör första draget

## Alternativa flöden
1. Spelaren väljer att avbryta helt istället för att starta om
- Spelaren använder menyfunktionen för att avbryta det pågående parti
- Systemet återgår till huvudmenyn
- Use caset avslutat

## Resultat
Ett helt nytt parti har startat omedelbart och är redo för det första draget av en av spelarna på den nya partiet
