# UC-11: Hantera tappad uppkoppling

## Aktör
Spel servern

## Mål
Att om en spelare tappar uppkoppling, ska spel servern försöka återuppta den eller veta hur den ska hantera om det inte går.

## Förutsättningar
- Spelare befinner sig i ett pågående multiplayer spel.
- Båda spelarna har en fungerande uppkoppling emot servern.

## Huvudflöde
1. Minst en spelare tappar sin uppkoppling.
2. Servern meddelar motståndaren att den andra spelaren väntar på att återuppta uppkopplingen, och pausar spelet.
3. Servern påbörjar väntar 30 sekunder på att uppkopplingen ska återupptas.
4. Uppkopplingen återupptas och spelet får då fortsätta.

## Alternativa flöden
- Spelaren kan inte återuppta anslutningen
	1. Servern misslyckas att nå spelaren och återuppta anslutningen.
	2. Spelaren får ett meddelande att dem kopplats ifrån
	3. Motståndaren får ett meddelande om att den andra spelaren tappat anslutningen
	4. Spelet avbryts.

## Resultat
Servern vet hur den ska hantera tappad anslutning och lämnar rum för att låta spelare återansluta när det går.

## Test Case – UC-11 Hantera tappad uppkoppling - given when then
### TC-11a: Tillfälligt tappad anslutning återupptas (huvudflöde)
Givet att två spelare är i ett pågående multiplayer-parti med fungerande uppkoppling
När en spelare tappar sin uppkoppling
Då ska servern pausa spelet, meddela motståndaren, och vänta i 30 sekunder på återanslutning
Och om spelaren återansluter inom tidsgränsen ska spelet fortsätta

### TC-11b: Återanslutning misslyckas (alternativt flöde)
Givet att servern väntar på att en frånkopplad spelare ska återansluta
När spelaren inte återansluter inom 30 sekunder
Då ska båda spelarna meddelas om frånkopplingen
Och spelet ska avbrytas.
