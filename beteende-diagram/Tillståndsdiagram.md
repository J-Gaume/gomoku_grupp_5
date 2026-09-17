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
