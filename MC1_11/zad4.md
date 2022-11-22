```blocks
agent.setItem(STONE, 10, 1)
agent.teleportToPlayer()
agent.turn(LEFT_TURN)
agent.place(DOWN)
agent.move(FORWARD, 1)
for (let index = 0; index < 4; index++) {}
```

## Zadanie czwarte
Pamiętaj aby uważnie czytać polecenia, wrazie problemów kliknij na żarówkę

## Krok 1
To zadanie wymaga zrobienia tego samego co w poprzednim kroku, PAMIĘTAJ że pętla
musi wykonać się 7-razy oraz żeby dać twojemu agentowi przedmioty.
```blocks
agent.setItem(STONE, 10, 1)
for (let index = 0; index < 7; index++) {

}
```
## Krok 2
Spróbuj zrobić program samemu, jeśli nie dajesz rady, zobacz kolejny krok
**PAMIĘTAJ** że agent musi stać na fioletowym bloku i być obrócony w strone lawy!

## Krok 3
Gotowy program powinien wyglądać w ten sposób
```blocks
for (let index = 0; index < 7; index++) {
agent.move(FORWARD,1)
agent.place(DOWN)}
```

## Krok 4
Włącz program i kontynuuj przygode
