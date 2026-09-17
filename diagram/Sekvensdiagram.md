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

