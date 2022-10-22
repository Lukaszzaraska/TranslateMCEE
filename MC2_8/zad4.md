## Krok 1
Stajemy na fioletowym bloczku

## Krok 2
Wykorzystamy do tego zadania bloczek ``||blocks.wypełnij od do||`` żeby usunąć przeszkode

## Krok 3
Musimy zamienić bloki drewna w powietrze, podpowiedzi znajdziesz na tabliczkach

```blocks
blocks.place(GRASS, pos(0, 0, 0))
```
## Krok 4 

```blocks
blocks.fill(
AIR,
pos(0, 0, 2),
pos(-1, 2, 2),
FillOperation.Replace
)

```
