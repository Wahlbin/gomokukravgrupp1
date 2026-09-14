# UC-02: Gör ett drag

## Aktör 
Spelare

## Mål
Att kunna placera en spelpjäs (sten) på en ledig korsning på spelbrädaet för att komma närmare en vinst eller för att blocka motståndaren

## Förutsättningar
- Ett spel är startat och pågår
- Det är den aktuella spelarens tur att agera
- Det finns minst en ledig position kvar på spelbrädan

## Huvudflöde
- Spelaren väljer en ledig position på spelbrädan
- Systemet validerar att den valda postitionen är ledig och inom brädets gränser
- Systemet placerar spelarens pjäs på positionen och uppdaterar spelbrädan
- Systemet kontrollerar brädan för att se om draget resulterade i en vinst eller inte
- Systemet kontollerar brädan om draget resulterade i oavgjort
- Turen överlämnas till motståndaren

## Alternativa flöden
1. Spelaren väljer en ogiltig eller redan upptagen postion:
- Systemet vägrar placera pjäsen
- Systemet ger visuell eller ljudmässig feedback om att draget är ogiltigt
- Use caset går tillbaka till steg 1 i huvudflödet (Spelaren får försöka igen)

2. Draget leder till vinst
- Systemet registrerar att spelaren har fått fem i rad
- Systemet tar upp ett vinstmeddelande och markerar de vinnande pjäserna
- Spelet avslutas

3. Draget leder till oavgjort
- Systemet registrerar att spelbrädet är fullt och ingen har fem i rad
- Systemet tar upp ett meddelande om att spelet blev oavgjort
- Spelet avsultas

## Resultat
Ett giltigt drag har registrerat och spelbrädan är uppdaterad. Spelets tillstånd har ändrats till antingen vänta på motståndarens drag eller så har spelet avsultats (vid vinst eller oavgjort)

## Test Case – UC-02 Gör ett drag - given when then

### TC-02a: Giltigt drag placeras (huvudflöde)
Givet att ett spel pågår, det är spelarens tur och minst en position på brädan är ledig
När spelaren väljer en ledig position inom brädets gränser
Då ska systemet placera spelarens pjäs på positionen och uppdatera spelbrädan
Och turen ska överlämnas till motståndaren

### TC-02b: Ogiltigt eller upptaget drag avvisas (alternativt flöde 1)
Givet att ett spel pågår och det är spelarens tur
När spelaren väljer en position som redan är upptagen eller utanför brädets gränser
Då ska systemet vägra placera pjäsen
Och systemet ska ge visuell eller ljudmässig feedback om att draget är ogiltigt
Och spelaren ska få försöka igen

### TC-02c: Draget resulterar i vinst (alternativt flöde 2)
Givet att spelaren gör ett drag som ger fem pjäser i rad
När draget registreras av systemet
Då ska systemet markera de vinnande pjäserna och visa ett vinstmeddelande
Och spelet ska avslutas

### TC-02d: Draget resulterar i oavgjort (alternativt flöde 3)
Givet att spelbrädan blir full utan att någon spelare fått fem i rad
När det sista giltiga draget registreras
Då ska systemet visa ett meddelande om att spelet blev oavgjort
Och spelet ska avslutas

### TC-02e: Serverside-validering (kopplat till icke-funktionellt krav – säkerhet)
Givet att en spelare försöker göra ett drag
När draget skickas till systemet
Då ska draget alltid valideras på serversidan, oavsett vad klienten skickar
Och ett ogiltigt drag ska aldrig kunna registreras enbart baserat på klientens uppgifter.
