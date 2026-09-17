## Sekvensdiagram


#### Sekvensdiagram 1: Placera sten & validera drag
- Berör Funktionella krav: FK-02 (Placera sten), FK-06 (Beräkna vinst), FK-08 (Ogiltiga drag hanteras korrekt)
- Samt Icke-funktionella krav: IFK-05 (drag valideras)
```mermaid
sequenceDiagram
    participant Spelare
    participant Server
    participant Motståndare

    Spelare->>Server: Placerar sten (UC-02)
    Server->>Server: Drag valideras (FK-08 & IFK-05)

    alt Giltigt drag
        Server-->>Motståndare: Uppdaterar bräda
        Server->>Server: Kontrollerar vinstvillkor (FK-06)
    else Ogiltigt drag
        Server-->>Spelare: Felmeddelande
    end
```

#### Sekvensdiagram 2: Bjud in vän
- Följande diagram visar systemts flöde för en spelare att bjuda in en vän(motståndare).
- Diagram berör UC-01(Starta parti), samt UC-04(Bjud in vän).
```mermaid
sequenceDiagram
    participant Spelare
    participant Server
    participant Vän

    Spelare->>Server: Bjuder in vän (UC-04)
    Server-->>Vän: Skickar inbjudan

    alt Vän accepterar
        Vän->>Server: Accepterar inbjudan
        Server->>Server: Skapar parti (UC-01)
        Server-->>Spelare: Parti startat
        Server-->>Vän: Parti startat
    else Vän avböjer
        Vän->>Server: Avböjer inbjudan
        Server-->>Spelare: Inbjudan avböjd
    end
```

