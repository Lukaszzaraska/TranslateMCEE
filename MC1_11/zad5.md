
```blocks
blocks.place(GRASS, pos(0, 0, 0))
world(0, 0, 0)
agent.setItem(STONE, 10, 1)
agent.teleportToPlayer()
agent.turn(LEFT_TURN)
agent.place(DOWN)
agent.move(FORWARD, 1)
for (let index = 0; index < 4; index++) {}

```
## Zadanie piąte
Pamiętaj aby uważnie czytać polecenia, wrazie problemów kliknij na żarówkę
## Krok 1
Żeby przejść dalej musimy zatkać dziury z kótrych leje się lawa, nasze sondy podały nam ich koordynaty
o to one (11,68,8-4) (11,65,-79) (11,65,-80)
## Krok 2 
Musimy postawić tam blok żeby je zatkać, użyjemy do tego ``||blocks: umieść kamień w (0,0,0)||`` oraz koordynatów bezzwględnych 
``||position: world(0, 0, 0)||``

```blocks
blocks.place(GRASS, world(0, 0, 0))
```
## Krok 3 
Tworzymy kod i wpisujemy poprawne koordynaty *(11,68,8-4) (11,65,-79) (11,65,-80)*
```blocks
blocks.place(STONE, world(0, 0, 0))
blocks.place(STONE, world(0, 0, 0))
blocks.place(STONE, world(0, 0, 0))
```

## Krok 4
Włącz program 

## Krok 5 
Teraz musimy zbudować most, technika dowolna, możesz użyć agenta albo bloczka wypełnij
```blocks
blocks.fill(
GRASS,
pos(0, 0, 0),
pos(0, 0, 0),
FillOperation.Replace
)
```
