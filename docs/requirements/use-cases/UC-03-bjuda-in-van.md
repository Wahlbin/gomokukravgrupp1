# UC-03: Bjuda in vän

## Aktör
Spelare

## Mål
Att kunna skicka en inbjudan till en annan person och koppla ihop båda spelarna i samma spelpart

## Förutsättningar
- Spelaren befinner sig i spelets huvudmeny eller i en väntelobby
- Systemet har en fungerande nätverkskoppling eller serveranslutning
- (Frivilligt) spelaren är inloggad på sitt konto

## Huvudflöde
- Spelaren klickar på knappen bjud in vän (eller motsvarande alternativ)
- Systemet genererar en unik inbjudningslänk (alternativ öppnar upp en lista över vänner i spelet)
- Spelaren delar länken med sin vän via valfri app eller väljer att skicka inbjudan direkt till en specifik användare i vänlistan
- Vännen tar emot inbjudan och klickar på acceptera (eller trycker på länken)
- Systemet validerar inbjudan och ansluter vännen till spelarens spel/lobby
- Systemet bekräftar visuellt för både spelarna att de nu är i samma parti

## Alternativa flöden
1. Vännen avböjer inbjudan:
- Vännen klickar på neka istället för acceptera
- Systemet skickar en notis om att inbjudan nekades till den som bjöd in
- Use caset avslutas utan att ett spel startas

2. Inbjudan löper ut:
- Vännen svarar inte inom en förutbestämd tid
- Systemet ogiltigförklarar inbjudan och meddelar spelaren att tiden gick ut
- Use caset avsultas

3. Länken är ogiltigt eller partiet är redan fullt:
- Vännen klickar på en gammal länk eller försöker ansluta sig till ett spel som redan startat eller avslutat
- Systemet visar felmeddelande för vännen
- Use caset avslutas

## Resultat
Spelaren och vännen är sammankopplade i gemensam lobby eller har startat ett nytt parti Gomoku.

## Test Case – UC-03 Bjuda in vän - given when then

### TC-03a: Vän bjuds in och ansluter (huvudflöde)
Givet att spelaren befinner sig i huvudmenyn eller en väntelobby med fungerande serveranslutning
När spelaren klickar på "Bjud in vän" och delar den genererade länken/inbjudan, och vännen accepterar den
Då ska systemet validera och ansluta vännen till spelarens parti
Och systemet ska bekräfta visuellt för båda spelarna att de är i samma parti

### TC-03b: Vännen avböjer inbjudan (alternativt flöde 1)
Givet att en inbjudan har skickats till en vän
När vännen klickar på "neka" istället för "acceptera"
Då ska systemet meddela spelaren att inbjudan avböjdes

### TC-03c: Inbjudan löper ut (alternativt flöde 2)
Givet att en inbjudan har skickats
När vännen inte svarar inom den förutbestämda tidsgränsen
Då ska systemet ogiltigförklara inbjudan automatiskt

### TC-03d: Ogiltig eller för gammal länk (alternativt flöde 3)
Givet att en inbjudningslänk finns
När någon klickar på en länk som redan använts, är för gammal, eller leder till ett parti som redan startat/är fullt
Då ska systemet visa ett tydligt felmeddelande och neka anslutning

### TC-03e: Integritet – ingen inloggning krävs för att bjuda in (kopplat till GDPR/anonymt spelande)
Givet att inloggning är frivilligt enligt kraven
När en spelare bjuder in en vän via länk utan att vara inloggad på ett konto
Då ska inbjudan ändå fungera
Och systemet ska inte kräva eller lagra personuppgifter utöver vad som krävs för att koppla ihop de två spelarna i partiet
