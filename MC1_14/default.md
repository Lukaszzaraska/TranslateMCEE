```blocks
blocks.fill(
GRASS,
pos(0, 0, 0),
pos(0, 0, 0),
FillOperation.Replace
)
    
player.onTravelled(WALK, function () {
    mobs.spawn(OCELOT, pos(0, 0, 0))
})
player.onChat("zoo", function () {
    for (let index = 0; index < 20; index++) {
        mobs.spawn(CHICKEN, pos(0, 0, 0))
    }
})
```
```template
.

```
## Zadanie pierwsze
Naszym zadaniem się sprawić aby w zoo pojawiły się zwierzęta, zrobimy to na dwa sposoby
## Krok 1
Pierwszy z nich to pojawienie się zwierząt na komende

## krok 2
Nazywamy naszą komende "zoo" 
```blocks
player.onChat("zoo", function () {
    
})
```
## krok 3
Dodajemy pętle i wpisujemy ile chcemy stworzyć zwierząt
<br>Uwaga! nie dajemy liczby większej niż 50
```blocks
player.onChat("zoo", function () {
    for (let index = 0; index < 20; index++) {
     
    }
})
```
## krok 4
Na koniec Dodajemy do pętli bloczek ``||mobs:zespawnuj "zwierze" w ~0 ~0 ~0||``
```blocks
player.onChat("zoo", function () {
    for (let index = 0; index < 20; index++) {
        mobs.spawn(CHICKEN, pos(0, 0, 0))
    }
})
```
## Zadanie drugie
Sposób drugi to program powodujący tworzenie sie zwierząt podczas chodzenia
## Krok 2
Zaczynamy od stworzenia wyzwalacza czyli bloczka który będzie uruchamiac komende
Wygląda on tak -->
```blocks
player.onTravelled(WALK, function () {
   
})
```
##Krok 3
Dodajemy do środka znowu bloczek spawnujący zwierzęta ``||mobs:zespawnuj "zwierze" w ~0 ~0 ~0||``
<br> I gotowe, zwierzęta będą pojawiać sie pod naszymi nogami
```blocks
player.onTravelled(WALK, function () {
   mobs.spawn(CHICKEN, pos(0, 0, 0))
})
```

