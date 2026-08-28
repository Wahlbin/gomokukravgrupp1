```mermaid
flowchart LR
    Spelare((Spelare))

    subgraph GomokuSystem [Gomoku]
        direction TB
        UC1(Starta nytt parti)
        UC2(Välja motståndare <br> Dator/Spelare)
    end

    Spelare --- UC1
    UC1 -.->|<< include >>| UC2
