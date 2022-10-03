### @activities 1
## Zadanie trzecie
### Krok 1
Ustaw odpowiednio agenta na niebieskiej wełnie używając jeśli trzeba ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` oraz  ``||agent:przesuń się w góre||``
### Krok 2
Agnet musi iść 7 kratek do góry a następnie 4 do przodu. Więc bierzemy w bloczki
``||agent: agent przesuń do przodu ||`` z zakładki ``||agent:AGENT||``
### krok 3
zmieniamy pierwszy bloczek na ``||agent: agent przesuń do góry o 7||``
a w drugim zmieniamy tylko n odległość na 4
```blocks

    agent.move(UP, 7)
    agent.move(FORWARD, 4)

```
### krok 4
A to wkładamy do niebieskiego bloczku ``||player:Przy poleceniu czatu "jump"||``
```blocks
player.onChat("jump", function () {
    agent.move(UP, 7)
    agent.move(FORWARD, 4)
})

```
### Krok 4
Uruchom program
