## Zadanie 7
Ustaw odpowiednio agenta bloku emeraldu, używając ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` oraz  ``||agent:przesuń się w przód||``

## Krok 1
Żeby wykonać to zadanie musisz użyć bloczków logiki które poznasz na kolejnych 
zajęciach. Podpowiem ci kawałek kodu a ty spróbuj dokończyć sam ;)
Włóż co ma się stac kiedy agent napotka przedsoba blok złota a co kiedy ma powietrze przed sobą 
```blocks
while (true) {
    if (agent.detect(AgentDetection.Block, FORWARD)) {
         "Tutaj włóż jeden odpowiedni bloczek" Tutaj agent ma blok złota przed sobą
    } else {
       "Tutaj włóż jeden odpowiedni bloczek" Tutaj agent ma blok powietrza przed sobą
    }
}

```
## Krok 2
Uruchom program kiedy dodasz bloczki
