```blocks
agent.setItem(STONE, 10, 1)
agent.teleportToPlayer()
agent.turn(LEFT_TURN)
agent.place(DOWN)
agent.move(FORWARD, 1)
agent.destroy(FORWARD)
for (let index = 0; index < 4; index++) {}
```

## Zadanie pierwsze 
Pamiętaj aby uważnie czytać polecenia, wrazie problemów kliknij na żarówkę
## Krok 1
Sprawdź czy agent stoi na fioletowym bloczku, **jeśli nie** to stań na tym bloczku i teleportuj 
agenta do gracza ``||agent.agent teleportuj do gracza||``
```blocks
agent.teleportToPlayer()
```
## Krok 2
Sprawdź czy agent jest zwrócony przodem do środka planszy, **jeśli nie** to używając
bloczku obrotu ``||agent.agent obróć się ||`` ustaw go odpowiednio
```blocks
agent.turn(LEFT_TURN)
agent.turn(LEFT_TURN)
```
## Krok 3
Następnie wykonaj 2 kroki do przodu ``||agent.przesuń do przodu 2||``
```blocks
agent.move(FORWARD, 2)
```

## krok 4
Następnie daj przedmiot i ustaw aktywny slot używając bloczku 
``||agent. Umieść blok lub przedmiot (BLOK) w liczbie (LICZBA) w gnieździe (NUMER) ||``
Wybierz dowolny blok i ustwa jego ilość na 10, numeru gniazda nie zmieniaj !
```blocks
agent.setItem(STONE, 10, 1)
```
## Krok 5
Nasz agent potrzebuje zbudować wieże o wysokości 10 kratek użyjemy w tym celu 
pętli ``||loops.powtórz (ILE) razy wykonaj||``
```blocks
for (let index = 0; index < 10; index++) {}
```
## Krok 6
Do pętli włóż ``||agent.przesuń do góry o 1||`` i ``||agent.umieść dół||``

```blocks
for (let index = 0; index < 4; index++) {
agent.move(UP, 1)
agent.place(DOWN)
}
```
## Krok 7
Cały program powinien wyglądać w ten sposób, **zakładając że agent stoi już na środku
planszy i jest odpowiednio odwrócony** ---> Kliknij w **żarówkę**
```blocks
agent.setItem(STONE, 10, 1)
for (let index = 0; index < 4; index++) {
agent.move(UP, 1)
agent.place(DOWN)
}
```
## krok 8
Włącz program i kontynuuj przygode

