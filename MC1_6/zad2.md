### @activities 1
## Zadanie drugie
### Krok 1
Ustaw odpowiednio agenta na niebieskiej wełnie używając jeśli trzeba ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` oraz  ``||agent:przesuń się w góre||``
### Krok 2
Agnet musi iść o 3 kratki do przodu a następnie 2 w lewo. Więc bierzemy w bloczki
``||agent: agent przesuń do przodu ||`` z zakładki ``||agent:AGENT||``
### krok 3
Następnie w drugi z bloczków zmieniamy żeby szedł w prawo 
```blocks
agent.move(FORWARD, 3)
agent.move(RIGHT, 2)

```
