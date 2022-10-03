
## Zadanie pierwsze
### Krok 1
Ustaw odpowiednio agenta na niebieskiej wełnie używając jeśli trzeba ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` oraz  ``||agent:przesuń się w góre||``
### Krok 2
Agnet musi stanąć na jakiekolwiek płytce naciskowej. Więc agent może iść
do przodu albo w lewo albo w prawo 

### krok 3
Wybierz jeden z tych bloczków<br> ``||agent: agent przesuń do przodu o 3||``<br>
``||agent: agent przesuń w lewo o 3||`` <br> ``||agent: agent przesuń w prawo o 3||``
```blocks
agent.move(FORWARD, 3)
albo
agent.move(RIGHT, 3)
albo
agent.move(LEFT, 3)

```
