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

