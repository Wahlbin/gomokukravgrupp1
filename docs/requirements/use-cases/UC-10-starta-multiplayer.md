# UC-10: starta multiplayer

## Aktör
Spelare

## Mål
Att det ska gå att spela multiplayer

## Förutsättningar
- Spelaren befinner sig i spelets huvudmeny eller i en väntelobby
- Systemet har en fungerande nätverkskoppling eller serveranslutning
- (Inte frivilligt) Spelaren är inloggad på sitt konto

## Huvudflöde
1. Spelaren öppnar huvudmenyn.
2. Spelaren klickar på "Nytt spel".
3. Spelaren blir satt i en vänte lobby.
4. Spelaren kopplas upp mot spel servrarna och matchas med en annan spelare
5. Multiplayer spelet startas.

## Alternativa flöden
- Spelaren avbryter spel sökandet
	1. Spelaren klickar på "Avbryt" i vänte lobbyn
	2. Vänte lobbyn stängs och spelaren disconnectas

## Resultat
Spelaren kan koppla upp sig mot spelets servrar och matcha med andra spelare för att spela multiplayer.

## Test Case – UC-10 Starta multiplayer - given when then
### TC-10a: Matchas mot annan spelare (huvudflöde)
Givet att spelaren är inloggad och har fungerande serveranslutning
När spelaren klickar "Nytt spel" och matchas i väntelobbyn
Då ska ett multiplayer-parti startas mellan de två spelarna

### TC-10b: Avbryt sökning (alternativt flöde)
Givet att spelaren väntar i lobbyn på en motspelare
När spelaren klickar på "Avbryt"
Då ska väntelobbyn stängas och spelaren kopplas från sökningen
