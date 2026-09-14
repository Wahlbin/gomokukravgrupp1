# UC-16: Hantera oavgjort parti

## Aktör
Spelaren

## Mål
Vid oavgjort parti ska båda spelare få en "Oavgjort" skärm och få lika många poäng.

## Förutsättningar
- 2 spelare befinner sig i ett spel mot varandra
- Båda spelarna har en fungerande uppkoppling emot servern.

## Huvudflöde
1. En spelare gör ett drag som leder till att matchen blir oavgjord.
2. Ett fönster poppar upp som förklarar att det blev oavgjort.
3. Båda spelarna får lika många poäng.
4. Spelet avslutas.

## Alternativa flöden
- Ett tekniskt fel uppstår vid resultatleverans
	1. Ett fel gör att endast en av klienterna tar emot meddelandet om oavgjort
	2. Systemet försöker skicka om meddelandet till den andra spelaren
	3. Spelet förblir avslutat för båda oavsett leveransstatus

## Resultat
Båda spelarna känner sig lika belönade och får korrekt information vid oavgjort parti.

## Test Case – UC-16 Hantera oavgjort parti - given when then
### TC-16a: Oavgjort ger lika poäng till båda (huvudflöde)
Givet att två spelare med fungerande serveruppkoppling spelar mot varandra
När ett drag leder till att matchen blir oavgjord
Då ska båda spelarna se en "Oavgjort"-skärm
Och båda spelarna ska få lika många poäng

### TC-16b: En spelare tar emot resultatet men inte den andra (alternativt flöde)
Givet att partiet blir oavgjort
När ett tekniskt fel gör att bara en av spelarnas klienter tar emot "Oavgjort"-meddelandet
Då ska systemet försöka skicka om meddelandet till den andra spelaren
Och ingen av spelarna ska kunna fortsätta göra fler drag efter att partiet avslutats.
