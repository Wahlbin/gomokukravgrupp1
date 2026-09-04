# UC-14: Servervalidering Av Drag

## Aktör
Servern

## Mål
Varje gång en spelare gör ett drag ska servern validera att draget är korrekt, via serversidan, så att spelare inte kan modifiera draget lokalt på sin maskin för att fuska.

## Förutsättningar
- 2 spelare befinner sig i ett spel mot varandra
- Båda spelarna har en fungerande uppkoppling emot servern.
- Båda spelarna är inloggade på ett konto

## Huvudflöde
1. En spelare gör ett drag.
2. Draget skickas till server sidan.
3. Servern validerar att draget är giltigt.
4. Valideringen skickas tillbaka till båda spelarnas klient och spelet fortsätter.

## Alternativa flöden
- Ett drag kan ej valideras eller är ogiltigt
	1. En spelare gör ett ogiltigt drag.
	2. Servern skickar ett meddelande till spelaren som säger "Ogiltigt drag, försök igen"

## Resultat
Spelare kan bara använda drag som är giltiga och många möjligheter att fuska undviks.
