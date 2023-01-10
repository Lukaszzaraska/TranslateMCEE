```blocks
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
    agent.destroy(FORWARD)
    agent.teleportToPlayer()
    for (let index = 0; index < 4; index++) {}

```
## Zadanie 3
Ustaw odpowiednio agenta na bloku emeraldu, używając ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` oraz  ``||agent:przesuń się do przodu||``

## Krok 1
Pętla ma się wykonać 11 razy a po jej wykonaniu
ma sie agent przesunąć o jeden do przodu. Dlatego blok ``||agent:przesuń do przodu o 1||``
włożymy po pętli wtedy wykona się tylko jeden raz
```blocks
for (let index = 0; index < 11; index++) {
  
}
agent.move(FORWARD, 1)
```
## Krok 2
zajmijmy się teraz uzupełnieniem pętli, musimy wykonać następujące rzeczy
1. Agent zniszcz przed sobą 
2. Agent idź do przodu o 1

```blocks
for (let index = 0; index < 11; index++) {
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
}
agent.move(FORWARD, 1)
```
## Krok 3
Zanim uruchomisz program upewnij się że porozmawiałeś z pomocnikiem i kliknąłeś
"Do dzieła" bez tego program może nie zadziałać.

## Krok 4
Uruchom program
