# UC-08: Spela lokalt flerspelarläge

## Aktör
Spelare (spelare 1 och spelare 2)

## Mål
Att starta ett parti där två spelare turas om att spela mot varandra på en och samma enhet

## Förutsättningar
- Systemet visar huvudmeny
- Spelarna behöver inte ha registrerat något konto för att spela

## Huvudflöde
- En spelare klickar på "spela"-knappen i huvudmenyn
- Spelaren får välja mellan tre spellägen och väljer lokalt på samma enhet
- Systemet genererar spelrutan
- Systemet tilldelar spelarna pjässtenar
- Den med svarta stenar börjar
- Efter varje godkänt drag markerar systemet den senast lagda stenen visuellt

## Alternativa flöden
1. Avbryt innan spelet hinner starta
- Spelaren ångrar sig under valet av spelläge
- Spelaren navigerar tillbaka till huvudmenyn
- Use caset avslutas

## Resultat
Ett lokalt flerspelarparti är igång och båda spelarna kan turas om att lägga stenar på samma enhet

## Test Case – UC-08 Spela lokalt flerspelarläge - give when then
### TC-08a: Starta lokalt tvåspelarparti (huvudflöde)
Givet att huvudmenyn visas och inget konto krävs
När en spelare väljer spelläget "lokalt på samma enhet"
Då ska systemet generera spelrutan och tilldela båda spelarna pjässtenar, med svart som börjar
Och senast lagda sten ska markeras visuellt efter varje godkänt drag

### TC-08b: Avbryt innan start (alternativt flöde)
Givet att spelaren håller på att välja spelläge
När spelaren ångrar sig och navigerar tillbaka till huvudmenyn
Då ska use caset avslutas utan att något parti startas
