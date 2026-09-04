# UC-21: Spela parti helt utan dataspårning

## Aktör
Spelare

## Mål
Spelaren ska kunna spela ett fullvärdigt parti utan att systemet
samlar in, sparar eller skickar vidare någon data om spelaren eller
partiet — ingen inloggning, ingen vinsthistorik, ingen statistik,
ingen spårning.

## Förutsättningar
- Spelaren befinner sig i huvudmenyn
- Spelaren är inte inloggad på ett konto
- Spelaren väljer ett spelläge som inte kräver konto (lokalt
  flerspelarläge eller mot datorn)

## Huvudflöde
1. Spelaren klickar på **Spela** i huvudmenyn.
2. Spelaren väljer att spela utan att logga in (fortsätt som gäst).
3. Spelaren väljer spelläge, t.ex. **Lokalt** eller **Mot datorn**.
4. Systemet startar partiet utan att be om namn, e-post eller lösenord.
5. Spelarna genomför partiet som vanligt — drag, turer, vinst eller oavgjort.
6. Systemet visar resultatet när partiet avslutas.
7. Systemet sparar ingenting: ingen historik, ingen statistik och
   inga personuppgifter. Partiet finns inte kvar efter att spelaren
   lämnar.

## Alternativa flöden
- Spelaren väljer **Online** utan att vara inloggad
  1. Systemet frågar om spelaren vill logga in, skapa konto eller
     fortsätta som gäst.
  2. Spelaren väljer gäst och matchas utan att någon identitet sparas.
- Spelaren ångrar sig innan partiet startar
  1. Spelaren navigerar tillbaka till huvudmenyn.
  2. Use caset avslutas.
- Spelaren vill spara partiet mitt i spelet
  1. Systemet informerar om att gästpartier inte kan sparas och
     hänvisar till att skapa ett konto om hen vill spara historik.

## Resultat
Spelaren har kunnat spela ett fullvärdigt parti utan att lämna
ifrån sig någon data. Inget konto, ingen historik och ingen spårning.
