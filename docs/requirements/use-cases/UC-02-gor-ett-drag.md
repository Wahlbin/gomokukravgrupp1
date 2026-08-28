
```mermaid
flowchart LR
    Spelare((Spelare))

    subgraph GomokuSystem [Gomoku]
        direction TB
        UC1(Placera sten)
        UC2(Validera dragets giltighet)
        UC3(Kontrollera vinst/oavgjort)
        UC4(Byta tur till nästa spelare)
        UC5(Ångra drag)
    end

    %% Spelarens direkta interaktioner
    Spelare --- UC1
    Spelare --- UC5

    %% Saker som måste ske när en sten placeras (Include)
    UC1 -.->|<< include >>| UC2
    UC1 -.->|<< include >>| UC3
    UC1 -.->|<< include >>| UC4

    %% Frivillig händelse (Extend)
    UC5 -.->|<< extend >>| UC1
