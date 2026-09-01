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
