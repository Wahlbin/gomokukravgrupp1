# UC-22: Hantera åtkomst under underhåll

## Aktör
Spelare

## Mål
När servern är under underhåll ska spelaren få tydlig information om
det och kunna välja ett alternativ — spela ett lokalt läge, vänta
eller försöka igen — utan att spelet kraschar eller data går förlorad.

## Förutsättningar
Spelaren befinner sig i huvudmenyn eller försöker nå en onlinetjänst
(logga in, starta online-parti)
Servern är under underhåll

## Huvudflöde (planerat underhåll)
1. Spelaren klickar på **Spela** och väljer **Online**.
2. Servern svarar med att den är under underhåll.
3. Systemet visar meddelandet: "Underhåll pågår — online-spel är
   tillgängligt igen [tid]".
4. Systemet erbjuder spelaren att spela **Mot datorn** eller **Lokalt**
   under tiden, eller att vänta.
5. Spelaren väljer ett alternativ och kan antingen spela direkt eller
   försöka igen senare utan att ladda om sidan.

## Alternativa flöden
- Oplanerat avbrott (ingen tid kan visas)
  1. Systemet visar "Tillfälligt problem — försök igen om en stund".
  2. Spelaren kan klicka på **Försök igen** eller välja ett lokalt läge.
- Underhåll börjar under ett pågående online-parti
  1. Systemet varnar spelarna innan nedstängningen (t.ex. 5 minuter).
  2. Partiet hinner avslutas eller pausas.
  3. Tappas uppkopplingen ändå → hanteras enligt UC-11.
- Spelaren försöker logga in under underhåll
  1. Systemet meddelar att inloggning inte är tillgänglig just nu.
  2. Spelaren kan fortsätta som gäst i lokala lägen.

## Resultat
Spelaren får tydlig information om underhållet och ett fungerande
alternativ. Onlinefunktioner är otillgängliga endast under
underhållsfönstret, utan krascher eller dataförlust.
