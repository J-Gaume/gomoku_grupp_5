```mermaid
flowchart TD
    A([Start]) --> B{Välj typ av parti}
    B -->|Rankad match| C[Sök rankad match - UC-20]
    B -->|Vän| D[Bjud in vän - UC-04]

    C --> E{Motståndare hittas?}
    E -->|Nej| F[Avbryt sökning]
    F --> Z1([Slut])
    E -->|Ja| G[Starta parti - UC-01]

    D --> H{Inbjudan accepteras?}
    H -->|Nej| F
    H -->|Ja| G

    G --> I[Tom spelbräda visas]
    I --> J[Spelarens tur]

    J --> K[Spelare väljer ruta - UC-02]
    K --> L{Giltigt drag? - IFK-05}
    L -->|Nej| M[Visa felmeddelande]
    M --> K
    L -->|Ja| N[Placera sten på brädan]

    N --> O{Fem i rad?}
    O -->|Ja| P[Avsluta parti - UC-03]
    O -->|Nej| Q{Brädan full?}
    Q -->|Ja| R[Oavgjort]
    R --> P
    Q -->|Nej| S[Byt tur till motståndare]
    S --> J

    P --> T{Var det en rankad match?}
    T -->|Ja| U[Uppdatera rankingpoäng - IFK-10]
    T -->|Nej| V[Visa resultat]
    U --> V
    V --> Z2([Slut])
```

### Detta diagram skapades av Claude för att ge läsare uppfattning om båda funktionella krav gällande verksamhetsregler,
### men även tillhörande icke-funktionella krav. Bland annat följande:

- **UC-01** (Starta spel), **UC-02** (Placera sten), **UC-03** (Avsluta parti), **UC-04** (Bjud in vän), **UC-20** (Rankad match)
- **IFK-05** (systemet validerar dragen) som beslutspunkten "Giltigt drag?"
- **IFK-10** (rankingberäkning) som steget efter en rankad match avgörs
