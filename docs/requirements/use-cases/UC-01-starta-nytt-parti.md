## UC-01: Starta nytt parti

**Aktör:** Spelare

**Mål:** Spelaren vill starta ett nytt Gomoku-parti.

**Förutsättning:** Spelaren befinner sig i huvudmenyn.

**Huvudflöde:**

1. Spelaren trycker på "Spela".
2. Systemet visar tillgängliga spellägen.
3. Spelaren väljer önskat spelläge, exempelvis lokalt, online eller mot robot.
4. Om spelaren väljer robot väljer spelaren svårighetsgrad.
5. Systemet skapar ett nytt 15×15-spelbräde.
6. Systemet visar spelbrädet och gör det möjligt för spelaren att göra sitt första drag.

**Alternativt flöde:**

Om spelaren väljer online och ingen motspelare finns tillgänglig, visar systemet att spelaren väntar på en motspelare.

**Resultat:** Ett nytt parti har skapats och spelaren kan börja spela.
