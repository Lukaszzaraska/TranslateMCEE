```blocks
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
    agent.teleportToPlayer()
    for (let index = 0; index < 4; index++) {}
    function onStart(){}

```
## Zadanie 2 
Ustaw odpowiednio agenta na bloku emeraldu, używając ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` oraz  ``||agent:przesuń się do przodu||``

## Krok 1
Tym razem pętla ma się wykonać 3-razy więc znowu dodajemy ją i zmieniamy liczbe
```blocks
for (let index = 0; index < 3; index++) {
  
}

```
## Krok 2
I dodajemy bloczki zgodnie z poleceniem
1. Agent idź do góry o 2
2. Agent idź do przodu o 2
3. Agent idź na dół o 2
4. Agent idź do przodu o 2
```blocks
for (let index = 0; index < 3; index++) {
    agent.move(UP, 2)
    agent.move(FORWARD, 2)
    agent.move(DOWN, 2)
    agent.move(FORWARD, 2)
}
```
## Krok 3
Uruchom program
