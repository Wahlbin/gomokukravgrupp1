# UC-12: Välj spelregler

## Aktör
Spelaren

## Mål
Spelaren ska kunna välja mellan traditionella och moderniserade regler, så att dem kan spela så som dem är vana vid och föredrar.

## Förutsättningar
- Spelaren befinner sig i starta spel menyn
- Båda spelarna har en fungerande uppkoppling emot servern.

## Huvudflöde
1. Spelaren klickar på "Byt spel regler" knappen i hörnet.
2. En liten meny öppnas där spelaren kan välja sitt föredragna spel läge.
3. Spelaren väljer det spel läge dem föredrar.
4. Spel regel menyn stängs och spel läget byts.

## Alternativa flöden
- Spelaren väljer samma läge som dem redan valt
	1. Spelaren klickar på samma spel regler som dem redan har valt.
	2. Inget händer och regel menyn stängs

## Resultat
Spelarna kan fritt spela utifrån dem spel reglerna som dem föredrar.

## Test Case – UC-12 Välj spelregler - given when then 
### TC-12a: Byt spelregler (huvudflöde)
Givet att spelaren befinner sig i starta-spel-menyn med fungerande uppkoppling
När spelaren klickar "Byt spelregler" och väljer traditionella eller moderniserade regler
Då ska det valda regelläget aktiveras och menyn stängas.

### TC-12b: Välja samma regler igen (alternativt flöde)
Givet att spelaren redan har ett valt regelläge
När spelaren väljer samma regler på nytt
Då ska ingenting ändras förutom att menyn stängs.
