# Funktionella krav

## 00-Spelmekanik och regler
----------------------------

-Systemet ska kunna känna igen och hantera när en spelare vinner, förlorar eller när det blir oavgjort.
-Systemet ska tilldela de två sidorna färgerna Svart och vit
-Systemet ska automatiskt utvärdera brädet efter varje enskilt drag för att kontrollera vinst- och oavgjort-villkor.
-Systemet ska identifiera och utropa vinst när en spelare uppnår fem stenar i rad (horisontellt, vertikalt eller diagonalt).
-Systemet ska identifiera och deklarera oavgjort (draw) om alla skärningspunkter fylls utan att ett vinstvillkor uppfylls.
-Spelet ska generera en spelruta som är 15x15 linjer.
-Spelet ska tillåta och kräva att pjäserna placeras på linjernas skärningspunkt, inte inuti rutorna.
-Systemet ska validera drag och endast tillåta placering av en sten på en tom och ledig skärningspunkt.
-Systemet ska tillämpa regeln att spelaren med svarta stenar alltid gör det första draget i ett nytt parti.
-Systemet ska registrera ett giltigt drag och omedelbart lämna över turen till den andra spelaren.
-Systemet ska spärra brädet och förhindra ytterligare drag så fort ett parti har avslutats.

----------------------------


## 01-Spellägen och meny
------------------------

-Menyn ska innehåla en "spela"-knapp samt ge användaren möjlighet att välja mellan tre spellägen = mot en robot, online eller lokalt ("verkligheten") på samma enhet.
-När man spelar mot datorn ska systemet erbjuda klickbara alternativ för svårighetsgraderna = "Lätt", "mellan" och "svår".
-Systemet ska tillhandahålla en huvudmeny där användaren kan välja att starta ett nytt parti.
-Systemet ska erbjuda ett "Lokalt Flerspelarläge" (Hotseat) där två spelare turas om att lägga stenar på samma enhet.
-Systemet ska erbjuda ett "Enspelarläge" (Single player) där användaren spelar mot en datorstyrd motståndare.
-Systemet ska erbjuda ett "Nätverksläge" (Multiplayer online) där två användare kan spela mot varandra från olika enheter.
-Systemet ska erbjuda en funktion under pågående spel för att ge upp (Resign) och ge vinsten till motståndaren.
-Systemet ska ha en menyfunktion för att avbryta ett pågående parti och återgå till huvudmenyn.
-Systemet ska ha en funktion för att snabbt starta om (Restart) ett pågående eller avslutat parti.

------------------------------------------


## 02-Användarfunktioner och inställningar
------------------------------------------

-Systemet ska via gränssnittet visuellt och tydligt indikera vems tur det är att spela.
-Systemet ska visuellt markera den senast lagda stenen (t.ex. med en liten prick på stenen) för att ge spelarna en tydlig överblick över senaste händelsen.
-Systemet ska, när vinst uppnås, visuellt framhäva den vinnande raden av stenar (genom animation eller markering).
-Systemet ska ha inställningar för att slå på och av ljud för stenplacering och vinstfanfar.
-Systemet ska tillåta användare att starta och spela spelet fullt ut utan att behöva regristera ett konto.
-Systemet ska inte spara vinsthistorik, statistik eller ha någon form av tracking.

------------------------------------------
