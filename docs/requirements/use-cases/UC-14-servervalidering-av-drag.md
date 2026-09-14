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
Spelare kan bara använda drag som är giltiga och många möjligheter att fuska kan undvikas.

## Test Case – UC-14 Servervalidering av drag - give when then
### TC-14a: Giltigt drag valideras server-side (huvudflöde)
Givet att två inloggade spelare spelar mot varandra med fungerande uppkoppling till servern
När en spelare gör ett drag
Då ska draget skickas till servern och valideras där innan det gäller
Och valideringsresultatet ska skickas tillbaka till båda klienterna

### TC-14b: Ogiltigt eller manipulerat drag avvisas (alternativt flöde)
Givet att en spelare, eller en manipulerad klient, skickar ett drag som inte är giltigt
När servern validerar draget
Då ska servern avvisa draget och visa meddelandet "Ogiltigt drag, försök igen"
Och draget ska inte registreras i spelets tillstånd.

