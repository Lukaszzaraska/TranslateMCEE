### @activities 1
## Zadanie piąte
### Krok 1
Ustaw odpowiednio agenta na niebieskiej wełnie ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` oraz  ``||agent:przesuń się w góre||``

### krok 2
będziemy potrzebować niebieskiego bloczka z zakładki "gracz" o nazwie 
``||player:Przy poleceniu czatu ""||`` uzywamy go 4-razy i nadajemy każdemu inną nazwie
naprzykład --> "w" , "s" , "a" , "d"
```blocks
player.onChat("w", function () {
   
})
player.onChat("s", function () {
    
})
player.onChat("a", function () {
    
})
player.onChat("d", function () {
    
})

```
### krok 4
Jak widzisz nazwy bloczków odpowiadają klawiszą do używanych do sterowania
dlatego musimy teraz odpowiednio dobrać kierunek poruszania do nazwy
```blocks
player.onChat("w", function () {
    agent.move(FORWARD, 5)
})
player.onChat("s", function () {
    agent.move(BACK, 5)
})
player.onChat("a", function () {
    agent.move(LEFT, 5)
})
player.onChat("d", function () {
    agent.move(RIGHT, 5)
})

```
### Krok 5
Uruchom program, następnie włącz czat "t" i wpisuj nazwy stworzonych komend żeby
przejść labirynt
