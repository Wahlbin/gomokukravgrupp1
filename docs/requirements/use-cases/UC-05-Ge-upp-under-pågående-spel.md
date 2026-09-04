# UC-05: Ge upp under pågående spel

## Aktör
Spelare

## Mål
Att det ska gå att ge upp under ett pågående spel för att avbryta.

## Förutsättningar
- Spelaren befinner sig i ett spel mot en annan spelare eller en bot.
- Systemet har en fungerande nätverkskoppling eller serveranslutning
- (Frivilligt) spelaren är inloggad på sitt konto

## Huvudflöde
1. Spelaren klickar på "Ge upp" knappen, under ett pågående spel.
2. En ruta poppar upp som frågar "Vill du verkligen ge upp?"
3. Spelaren får alternativen "Ja" och "Nej"
4. Spelaren klickar på "Ja", vilket avslutar spelet
5. Ett meddelande poppar upp för spelaren som säger "Du gav upp" samtidigt som ett meddelande poppar upp för motståndaren där det står "Motståndaren gav upp"

## Alternativa flöden
- Spelaren klickar "Nej" när dem får frågan om dem vill ge upp.
	1. Spelet fortsätter som innan

## Resultat
Spelaren kan fritt avsluta ett pågående spel när dem vill, genom att ge upp, vilket avslutar spelet.
