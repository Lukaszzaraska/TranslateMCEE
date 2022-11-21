## Zadanie herkulesa
Twoim zadaniem jest umieścić agenta na złotej płytce naciskowej 
Użyj do tego natepujących bloczków
1. ``||agent: agent obróć się ||`` - agent obraca się 
Kiedy już ustawisz agenta przodem do płytki wykonaj kolejne polecenie
2. ``||agent: agent przesuń się do przodu o 1||`` -  agent idzie o 1 blok do przodu
używaj tego bloczku tak długo aż agent zrówna się z płytką naciskową
3. ``||agent: agent przesuń się w prawo o 1||`` -  agent idzie o 1 blok w prawo
używaj tego bloczku tak długo aż agent zrówna się z płytką naciskową

```blocks
agent.turn(LEFT_TURN)
agent.move(FORWARD, 1)
agent.move(RIGHT, 1)
```
