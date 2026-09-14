# Skapa användarkonto frivilligt

## Aktör
Spelare

## Mål
Spelaren har valet att skapa ett användarkonto

## Förutsättningar
Spelaren ligger i sidans main page

## Huvudflöde
1. Spelaren får en prompt i main page om inloggning/registrering
2. Spelaren väljer ett sätt att registrera konto
3. Spelaren väljer användarnamn och lösenord, kanske email också beroende på registreringsmetod
4. Spelaren har skapat ett konto

## Alternative flöde
- Spelaren klickade på "Continue as guest" och fortsätter utan konto

## Resultat
Spelaren fick alternativen att fortsätta med ett konto eller utan

## Test Case – UC-15 Skapa användarkonto (frivilligt)- given when then
### TC-15a: Spelaren skapar konto (huvudflöde)
Givet att spelaren befinner sig på startsidan och får en prompt om inloggning/registrering
När spelaren väljer att registrera sig med användarnamn, lösenord (och ev. e-post)
Då ska ett konto skapas åt spelaren

### TC-15b: Spelaren fortsätter som gäst (GDPR – frivillighet/dataminimering)
Givet att spelaren får prompten om inloggning/registrering
När spelaren klickar på "Continue as guest"
Då ska spelaren kunna fortsätta utan konto och utan att lämna några personuppgifter

### TC-15c: Valideringsfel vid registrering (alternativt flöde)
Givet att spelaren registrerar ett konto
När spelaren anger ett användarnamn som redan är taget, eller ett lösenord som inte uppfyller kraven
Då ska systemet visa ett tydligt felmeddelande om vad som är fel
Och kontot ska inte skapas förrän giltiga uppgifter angetts.
