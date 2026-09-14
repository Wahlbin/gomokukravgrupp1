# UC-01-starta-nytt-parti

## Aktör
Spelare

## Mål 
Spelaren vill starta ett nytt Gomoku-parti.

## Förutsättning
Spelaren befinner sig i huvudmenyn.

## Huvudflöde
1. Spelaren trycker på "Spela".
2. Systemet visar tillgängliga spellägen.
3. Spelaren väljer önskat spelläge, exempelvis lokalt, online eller mot robot.
4. Om spelaren väljer robot väljer spelaren svårighetsgrad.
5. Systemet skapar ett nytt 15×15-spelbräde.
6. Systemet visar spelbrädet och gör det möjligt för spelaren att göra sitt första drag.

## Alternativt flöde
Om spelaren väljer online och ingen motspelare finns tillgänglig, visar systemet att spelaren väntar på en motspelare.

## Resultat
Ett nytt parti har skapats och spelaren kan börja spela.


## Test Case
## Test Case – UC-01 Starta nytt parti

### TC-01a: Spelaren startar ett lokalt parti (huvudflöde)
Givet att spelaren befinner sig i huvudmenyn
När spelaren trycker på "Spela" och väljer spelläget "lokalt"
Då ska systemet skapa ett nytt 15×15-spelbräde
Och spelaren ska kunna göra sitt första drag

### TC-01b: Spelaren väntar på motspelare online (alternativt flöde)
Givet att spelaren har valt spelläget "online"
När ingen motspelare finns tillgänglig
Då ska systemet visa att spelaren väntar på en motspelare

### TC-01c: GDPR – inget onödigt sparande av personuppgifter
Givet att spelaren startar ett nytt parti, oavsett spelläge
När partiet skapas
Då ska systemet inte begära eller lagra några personuppgifter utöver det som krävs för att partiet ska fungera (t.ex. inget krav på registrering för lokalt/robot-läge)
