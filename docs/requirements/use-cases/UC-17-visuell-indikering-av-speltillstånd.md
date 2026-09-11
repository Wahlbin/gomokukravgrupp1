# UC-17-visuell-indikering-av-speltillstånd

## Aktör
Spelare

## Mål
Spelaren förstår vems tur det är i spelet

## Förusättningar
Spelaren är i spelet

## Huvudflöde
1. Spelaren är i spelet mot en motståndare
2. Båda spelarna spelar sin tur
3. Längst nere på skärmen så står det om det är din tur eller motståndarens tur
4. Det står även vilken färg har turen, och vilken färg spelaren är


## Resultat
Spelaren får en tydlig indikering på vems tur det är att spela


## Test Case – UC-17 Visuell indikering av speltillstånd - given when then
### TC-17a: Turindikering visas korrekt (huvudflöde)
Givet att spelaren är i ett pågående parti mot en motståndare
När det är någons tur att göra ett drag
Då ska det längst ner på skärmen tydligt stå om det är spelarens eller motståndarens tur
Och vilken färg som har turen och vilken färg spelaren själv spelar med

### TC-17b: Indikeringen uppdateras inte i tid (alternativt flöde)
Givet att ett drag precis har registrerats och turen ska växla
När det uppstår fördröjning i kommunikationen mellan klient och server
Då ska gränssnittet inte visa fel spelare som "aktiv" längre än nödvändigt
Och indikeringen ska uppdateras så snart korrekt tillstånd tagits emot.
