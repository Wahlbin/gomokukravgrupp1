# UC-13: Byta språk i gränssnittet

## Aktör
Spelare

## Mål
Att byta språket som spelet visar

## Förutsättningar
Spelaren befinner sig på spelsidan eller i menyerna

## Huvudflöde
- Spelaren navigerar till inställningen för språk
- Spelaren väljer ett nytt språk från listan över tillgängliga språk
- Systemet uppdaterar omedelbart all text i gränssnittet till det valda språket

## Alternativa flöden
1. Valt språk kan inte laddas
- Systemet misslyckas med att hämta/ladda texterna för det valda språket
- Systemet visar ett felmeddelande till spelaren
- Gränssnittet behåller det tidigare valda språket tills ett nytt, fungerande val görs.

## Resultat
Spelet visar nu och är fullt spelbart i ett annat vald språk

## Test Case – UC-13 Byta språk i gränssnittet - given when then
### TC-13a: Byta språk (huvudflöde)
Givet att spelaren befinner sig på spelsidan eller i menyerna
När spelaren navigerar till språkinställningen och väljer ett nytt språk
Då ska all text i gränssnittet omedelbart uppdateras till det valda språket.

### TC-13b: Valt språk kan inte laddas (alternativt flöde)
Givet att spelaren väljer ett nytt språk i inställningarna
När systemet misslyckas med att ladda texterna för det valda språket
Då ska spelaren få ett felmeddelande
Och gränssnittet ska behålla det tidigare, fungerande språket.
