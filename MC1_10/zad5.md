```blocks
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
    agent.teleportToPlayer()
    for (let index = 0; index < 4; index++) {}

```
## Zadanie 5
Ustaw odpowiednio agenta na bloku emeraldu, używając ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` oraz  ``||agent:przesuń się w przód||``

## Krok 1
Aby wykonać to zadanie musimy policzyć ile kratek agent musi iść do przodu i kiedy się 
obrócić. Zaczynamy od tego że budynek ma 3 piętra. więc kiedy będziemy
umieli przejść jedno piętro później będzie trzeba zrobić to samo 3 razy.
Więc umieszczamy pętle która wykona się tyle razy ile jest pięter
```blocks
for (let index = 0; index < 3; index++) {
  
}

```
## Krok 2
Liczymy długość pierwszej lini która musi pokonać nasz agent, zamknij programowanie
i policz !

## Krok 3
Ma ona długość 11 kratek. Teraz mamy zakręt więc chcemy żeby agent się odrócił w lewo
```blocks 
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
}

```
## Krok 4
Przed nami kolejna prosta, policz jaka jest jej długość

## Krok 5
Jej długość też wynosi 11 kratek i znowu musimy się obrócić

```blocks 
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
}

```
## Krok 6
Kolejna prosta przed nami i podpowiem ci że też ma 11 kratek długości i zakręt
Więc nasz kod wygląda tak
```blocks 
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
}

```
## Krok 7
Jak widzisz 3 razy powtarzamy to samo, może to zrobić w inny sposób, ładniejszy i krótszy 
dodając pętle 
```blocks 
for (let index = 0; index < 3; index++) {
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
    }
}

```
## Krok 8
Ostatni bok został do pokonania, tym razem nie jest to takie proste, policzmy
ile jest kratek do schodków
## Krok 9
Jest ich 6 więc każemy naszemu agentowi o tyle posunąć się do przodu, pomiędzy pętlami !
```blocks 
for (let index = 0; index < 3; index++) {
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
    }
    agent.move(FORWARD, 6)
}

```
## Krok 10
Widzimy teraz schody i że składają się z 3 stopni, dlatego zamiast znowu tworzyć
długi kod składający się z wielu kroków odrazu użyjmy pętli która wykona się 3-razy

```blocks 
for (let index = 0; index < 3; index++) {
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
    }
    agent.move(FORWARD, 6)
    for (let index = 0; index < 3; index++) {
    
    }
}

```
## Krok 11
Do ich pokonania będziemy musieli poruszać się 
1. jeden klocek do góry 
2. jeden klocek do przodu

```blocks 
for (let index = 0; index < 3; index++) {
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
    }
    agent.move(FORWARD, 6)
    for (let index = 0; index < 3; index++) {
    agent.move(UP, 1)
    agent.move(FORWARD, 1)
    }
}

```
## Krok 12
Jako ostatni krok musimy ustawić agenta do pozycji z której zaczynał na początku 
aby to uzyskać, musi iść dwa do przodu i obrócić się w lewo. umieszczamy to poza pętlą
użytej wyżej
```blocks 
for (let index = 0; index < 3; index++) {
for (let index = 0; index < 3; index++) {
    agent.move(FORWARD, 11)
    agent.turn(LEFT_TURN)
    }
    agent.move(FORWARD, 6)
    for (let index = 0; index < 3; index++) {
    agent.move(UP, 1)
    agent.move(FORWARD, 1)
    }
    agent.move(FORWARD, 2)
    agent.turn(LEFT_TURN)
}

```
## Krok 13
Uruchom program

