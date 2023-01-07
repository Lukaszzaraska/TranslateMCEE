## Zadanie 1
Ustaw odpowiednio agenta na bloku emeraldu, używając ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` oraz  ``||agent:przesuń się w przód||``
## Krok 1
Pętla to specjalny bloczek która pozwala nam powtarzać daną czynność wielokrotnie
Są różne rodzaje pętli ale wszystkie mają taki sam kolor ---> ``||loops:Jakaś pętla||``

## krok 2
Do kilku następnych zadań będziemy potrzebować pętli 
``||loops:powtórz "Liczba" razy wykonaj||`` w miejscu 'liczba' będziemy
wpisywać liczbe ile razy ma się powtórzyc kod wewnątrz niej
```blocks
for (let index = 0; index < 4; index++) {
    
}
```
## krok 3
Zgodnie z poleceniem nasza pętla ma się wykonać 4 razy, dodajemy ją 
a następnie do jej wnętrza wkładamy odpowiednie bloczki zgodne z poleceniem
1. Agent idź do przodu o 1
2. Agent idź do góry o 1
3. Agent idź do przodu o 1
4. Agent obróć się w lewo
```blocks
for (let index = 0; index < 4; index++) {
    agent.move(FORWARD, 1)
    agent.move(UP, 1)
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
}

```
## Krok 4
Uruchom program
