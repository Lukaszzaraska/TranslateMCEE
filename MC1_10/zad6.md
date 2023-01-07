## Zadanie 6
Ustaw odpowiednio agenta przed wełną, używając ``||agent:teleportuj do gracza||`` ,
``||agent:obróć się w ||`` lub  ``||agent:przesuń się w przód||``

## Krok 1
Od pomocnika wiemy że przeszkoda ma 18 kratek długości, dltaego nasza pętla
wykona się tyle samo.
```blocks
for (let index = 0; index < 18; index++) {
  
}

```
## Krok 2
zajmijmy się teraz uzupełnieniem pętli, musimy wykonać następujące rzeczy
1. Agent zniszcz przed sobą 
2. Agent idź do przodu o 1
3. Agent zniszcz nad sobą

```blocks
for (let index = 0; index < 18; index++) {
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
    agent.destroy(UP)
}
```
## Krok 3
Na sam koniec musimy przesunąć agenta o jeden do przodu aby stanął na płytce naciskowej 
i odblokował nam przejście
```blocks
for (let index = 0; index < 18; index++) {
    agent.destroy(FORWARD)
    agent.move(FORWARD, 1)
    agent.destroy(UP)
}
agent.move(FORWARD, 1)
```
## Krok 4
Zanim uruchomisz program upewnij się że porozmawiałeś z pomocnikiem i kliknąłeś
"Do dzieła" bez tego program może nie zadziałać
## Krok 5
Uruchom program
