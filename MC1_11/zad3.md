```blocks
agent.setItem(STONE, 10, 1)
agent.teleportToPlayer()
agent.turn(LEFT_TURN)
agent.place(DOWN)
agent.move(FORWARD, 1)
for (let index = 0; index < 4; index++) {}
```

## Zadanie trzecie
Pamiętaj aby uważnie czytać polecenia, wrazie problemów kliknij na żarówkę
## Krok 1
Upewnij się że agent stoi na fioletowym bloczku i jest odwrócony w strone drugiej wieży **jeśli nie** to odwróć go odpowiednio

## Krok 2
Użyj tej samej pętli co wcześniej, zmień tylko ilość powtórzeń na 5
``||loops.powtórz (ILE) razy wykonaj||``

```blocks
for (let index = 0; index < 5; index++) {}
```
## Krok 3
Przed petlą dodaj ``||agent. Umieść blok lub przedmiot (BLOK) w liczbie (LICZBA) w gnieździe (NUMER) ||``

```blocks
agent.setItem(STONE, 10, 1)
for (let index = 0; index < 5; index++) {}
```
## Krok 4
Do pętli włóż ``||agent: przesuń się do przodu o 1||`` a nastepnie
``||agent:umieść dół)||``

```blocks
agent.setItem(STONE, 10, 1)
for (let index = 0; index < 5; index++) {
agent.move(FORWARD,1)
agent.place(DOWN)}
```
