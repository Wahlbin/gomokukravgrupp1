flowchart LR

&#x20;   Player(("Spelare"))

&#x20;   Bot(("Bot / AI"))

&#x20;   System(("Spelsystemet"))



&#x20;   subgraph Gomoku\["Gomoku — sammanställd funktionell översikt"]

&#x20;       direction TB



&#x20;       %% Spelarens handlingar (Identiska med diagram 1)

&#x20;       P\_UC1("Starta nytt spel")

&#x20;       P\_UC2("Gör ett drag")

&#x20;       P\_UC3("Välj spelläge")

&#x20;       P\_UC4("Spela mot datorn")

&#x20;       P\_UC5("Spela flerspelare online")

&#x20;       P\_UC6("Ge upp matchen")

&#x20;       P\_UC7("Starta om matchen")

&#x20;       P\_UC8("Ändra inställningar")

&#x20;       P\_UC9("Logga in")

&#x20;       P\_UC10("Logga ut")

&#x20;       P\_UC11("Godkänna cookies")

&#x20;       P\_UC12("Återkalla cookie-samtycke")



&#x20;       %% Botens handlingar

&#x20;       B\_UC1("Motta brädstatus")

&#x20;       B\_UC2("Beräkna optimalt drag")

&#x20;       B\_UC3("Skicka drag")



&#x20;       %% Systemets handlingar

&#x20;       S\_UC1("Validera drag")

&#x20;       S\_UC2("Uppdatera brädstatus")

&#x20;       S\_UC3("Kontrollera vinstvillkor")

&#x20;       S\_UC4("Hantera spelsession och timer")

&#x20;       S\_UC5("Fastställa resultat")

&#x20;       S\_UC6("Spara matchhistorik")



&#x20;       %% Matchresultat

&#x20;       O\_UC1("Vinna match")

&#x20;       O\_UC2("Förlora match")

&#x20;       O\_UC3("Spela oavgjort")

&#x20;   end



&#x20;   %% Spelarens direkta kopplingar (Identiska med diagram 1)

&#x20;   Player --- P\_UC1

&#x20;   Player --- P\_UC2

&#x20;   Player --- P\_UC6

&#x20;   Player --- P\_UC7

&#x20;   Player --- P\_UC8

&#x20;   Player --- P\_UC9

&#x20;   Player --- P\_UC10

&#x20;   Player --- P\_UC11



&#x20;   %% Botens kopplingar

&#x20;   Bot --- B\_UC1

&#x20;   Bot --- B\_UC2

&#x20;   Bot --- B\_UC3



&#x20;   %% Systemets kopplingar

&#x20;   System --- S\_UC1

&#x20;   System --- S\_UC2

&#x20;   System --- S\_UC3

&#x20;   System --- S\_UC4

&#x20;   System --- S\_UC5



&#x20;   %% Spelarens logiska relationer (Identiska med diagram 1)

&#x20;   P\_UC1 -.->|"inkluderar"| P\_UC3

&#x20;   P\_UC3 -.->|"utökar"| P\_UC4

&#x20;   P\_UC3 -.->|"utökar"| P\_UC5

&#x20;   P\_UC8 -.->|"utökar"| P\_UC12

&#x20;   

&#x20;   %% Botens logiska relationer

&#x20;   B\_UC2 -.->|"inkluderar"| B\_UC1



&#x20;   %% Utförande av drag triggar systemets validering

&#x20;   P\_UC2 -.->|"utlöser"| S\_UC1

&#x20;   B\_UC3 -.->|"utlöser"| S\_UC1



&#x20;   %% Systemets pipeline

&#x20;   S\_UC1 -.->|"inkluderar"| S\_UC2

&#x20;   S\_UC2 -.->|"inkluderar"| S\_UC3

&#x20;   S\_UC3 -.->|"resulterar i"| S\_UC5

&#x20;   P\_UC6 -.->|"resulterar i"| S\_UC5

&#x20;   S\_UC5 -.->|"inkluderar"| S\_UC6



&#x20;   %% Resultat

&#x20;   S\_UC5 -.->|"definierar"| O\_UC1

&#x20;   S\_UC5 -.->|"definierar"| O\_UC2

&#x20;   S\_UC5 -.->|"definierar"| O\_UC3



