### Tillståndsdiagram 1: Systemtillstånd under spelets gång.

```
stateDiagram-v2
    [*] --> SpelarensTur : Parti startar

    SpelarensTur --> MotståndarensTur : Giltigt drag (UC-02)
    MotståndarensTur --> SpelarensTur : Giltigt drag (UC-02)

    SpelarensTur --> Slut : Vinstvillkor uppfyllt (UC-06)
    MotståndarensTur --> Slut : Vinstvillkor uppfyllt (UC-06)

    Slut --> [*]
```


### Tillståndsdiagram 2: Systemets tillstånd under ranked flöde.
```
stateDiagram-v2
    [*] --> Matchmaking : Sök rankad match (UC-20)

    Matchmaking --> Pågår : Motståndare hittad
    Matchmaking --> Slut : Ingen motståndare hittad

    Pågår --> Pågår : Drag placeras & valideras (UC-02, IFK-05)
    Pågår --> Avslutat : Fem i rad
    Pågår --> Oavgjort : Brädan full

    Avslutat --> Rankinguppdaterad : Poäng beräknas (IFK-10)
    Rankinguppdaterad --> Slut
    Oavgjort --> Slut

    Slut --> [*]
```

#### Tillståndsdiagram 3: Tillstånd gentemot GDPR

stateDiagram-v2
    [*] --> CookieFörfrågan : Besöker sidan

    CookieFörfrågan --> SamtyckeGivet : Godkänner cookies
    CookieFörfrågan --> SamtyckeNekat : Avböjer cookies

    SamtyckeGivet --> SpelDataSparas : Sparar speldata (IFK-06)
    SamtyckeNekat --> Slut : Ingen data sparas

    SpelDataSparas --> SpelKanÅterupptas : Spel kan återupptas (FK-07)
    SpelKanÅterupptas --> Slut : Session avslutas

    SpelDataSparas --> SamtyckeÅterkallat : Återkallar samtycke (IFK-09)
    SamtyckeÅterkallat --> DataRaderad : Raderar speldata (IFK-07)
    DataRaderad --> Slut

    Slut --> [*]


