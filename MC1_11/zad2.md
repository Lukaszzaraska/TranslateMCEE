```blocks
agent.teleportToPlayer()
agent.turn(LEFT_TURN)
agent.move(FORWARD, 1)
agent.destroy(FORWARD)
for (let index = 0; index < 4; index++) {}
```

## Zadanie drugie
Pamiętaj aby uważnie czytać polecenia, wrazie problemów kliknij na żarówkę
## Krok 1
Upewnij się że agent stoi na fioletowym bloczku i jest odwrócony w strone muru

## Krok 2
Użyj pętli która wykona się 4 razy --> ``||loops:powtórz 4 razy wykonaj||`` 
```blocks
for (let index = 0; index < 4; index++) {}
```
## Krok 3
Włóż do niej ``||agent: zniszcz do przodu||`` i ``||agent:zniszcz góra||`` oraz dodaj ``||agent:przesuń do przodu o 1||``
```blocks
for (let index = 0; index < 4; index++) {
agent.destroy(FORWARD)
agent.destroy(UP)
agent.move(FORWARD,1)}
```
## krok 4
Włącz program i kontynuuj przygode

