# Funkcje domu: Bloki

## Krok 1
Dodaj ``||functions:funkcja||`` i nazwij ją  **ściany**. 

```blocks
function ściany () {
}
```

## Krok 2
Dodaj polecenie ``||agent:ustaw blok lub item||`` i umieść je w funkcji **ściany**. Ustaw ją na **Deski z drewna akacjowego** z liczbą **64** w gnieździe **1**.

```blocks
function ściany () {
    agent.setItem(PLANKS_ACACIA, 64, 1)
}
```

## Krok 3
Weź pętlę ``||loops:powtórz||``, ustaw ją na **3** razy i przeciągnij do **ściany** ``||functions:funkcja||`` poniżej `` ||agent:ustaw blok lub item||`` blok. Dodaj blok ``||agent:agent przesuń||`` wewnątrz pętli ``||loops:powtórz||`` i ustaw go na **w górę o 1**.

```blocks
function ściany () {
    agent.setItem(PLANKS_ACACIA, 64, 1)
    for (let index = 0; index < 3; index++) {
        agent.move(UP, 1)
    }
}
```

## Krok 4
Dodaj kolejną pętlę ``||loops:powtórz||``, ustaw ją na **4** razy i przeciągnij do pierwszej pętli ``||loops:powtórz||``—pod pierwszą ``| |agent:agent przesuń||`` blok. Dodaj ``||agenta:skręć w prawo||`` do drugiej pętli ``||loops:powtórz||``.

```blocks
function ściany () {
    agent.setItem(PLANKS_ACACIA, 64, 1) 
    for (let index = 0; index < 3; index++) { 
        agent.move(UP, 1) 
        for (let index = 0; index < 4; index++) { 
            agent.turn(RIGHT_TURN) 
        } 
    } 
}) 
```

## Krok 5
Dodaj trzecią pętlę ``||loops:powtórz||``, przeciągnij ją do drugiej pętli ``||loops:powtórz||`` i umieść nad 
``||agent: agent skręć w prawo||`` blok. Ustaw trzecią ``||pętle:powtórz||``pętle powtórz  **4** razy. Dodaj blok ``||agent:agent umieść||`` do najbardziej wewnętrznej pętli ``||loops:powtórz||`` i ustaw ją na **Dół**. Dodaj blok ``||agent:agent przesuń||``, ustaw go na **Do przodu o 1** i przeciągnij go do wewnętrznej pętli ``||loops:powtórz||`` pod ``|| agent:miejsce||`` w dół.

```blocks
function ściany () {
    agent.setItem(PLANKS_ACACIA, 64, 1) 
    for (let index = 0; index < 3; index++) { 
        agent.move(UP, 1) 
        for (let index = 0; index < 4; index++) { 
            for (let index = 0; index < 4; index++) { 
                agent.place(DOWN) 
                agent.move(FORWARD, 1) 
            } 
            agent.turn(RIGHT_TURN) 
        } 
    } 
}) 
```

## Krok 6
Dodaj nową funkcje ``||functions:dach||`` i nazwij go **dach**.

```blocks
function dach () {
	
}
```

## Krok 7
Weź blok ``||agent:Ustaw blok lub item||``, ustaw go na **ceglany slab**, a następnie ustaw licznik na **64** i slot na **1** i przeciągnij go do **dach** ``||funkcje:funkcja||``. Dodaj blok ``||agent:agent przesuń||`` i ustaw go na **góra** by **1**.

```blocks
function dach () {
    agent.setItem(BRICKS_SLAB, 64, 1) 
    agent.move(UP, 1) 
}) 
```

## Krok 8
Dodaj pętlę ``||loops:repeat||`` i przeciągnij ją do **dach** ``||functions:dach||``. Ustaw powtarzanie na **4** razy. Dodaj blok ``||agent:agent przesuń||`` i ustaw go na **cofnij o 4**. Dodaj również kolejny blok ``||agent:agent przesuń||`` i ustaw go na **prawo o 1**.
	
```blocks
function dach () {
    agent.setItem(BRICKS_SLAB, 64, 1) 
    agent.move(UP, 1) 
    for (let index = 0; index < 4; index++) { 
        agent.move(BACK, 4) 
        agent.move(RIGHT, 1) 
    } 
}) 
```

## Krok 9
Dodaj kolejną pętlę ``||loops:Powtórz||``, ustaw ją na powtórzenie **4** razy. Dodaj blok ``||agent:
położyć na dół||``, po którym następuje blok ``||agent:przesuń||``, ustaw go na **Do przodu o 1**. Przeciągnij tę pętlę ``||loops:powtórz||`` do poprzedniej pętli powtarzania — nad blok ``||agent:agent przesuń||`` **cofnij o 4**.

```blocks
function dach () {
    agent.setItem(BRICKS_SLAB, 64, 1) 
    agent.move(UP, 1) 
    for (let index = 0; index < 4; index++) { 
        for (let index = 0; index < 4; index++) { 
            agent.place(DOWN) 
            agent.move(FORWARD, 1) 
        } 
        agent.move(BACK, 4) 
        agent.move(RIGHT, 1) 
    } 
}) 
```

## Krok 10
Przeciągnij polecenie ``||player:Przy poleceniu czatu||`` do obszaru roboczego i nazwij je **dom**. Dodaj ``||functions:function||`` i wywołać zarówno **ściany**, jak i **dach** ``||advanced:functions||``.

## Krok 11

Naciśnij przycisk **Odtwórz**, przejdź do Minecrafta i przetestuj polecenie **dom**.

```blocks
function ściany () {
    agent.setItem(PLANKS_ACACIA, 64, 1)
    for (let index = 0; index < 3; index++) {
        agent.move(UP, 1)
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < 4; index++) {
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
        }
    }
}
function dach () {
    agent.setItem(BRICKS_SLAB, 64, 1)
    agent.move(UP, 1)
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 4; index++) {
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.move(BACK, 4)
        agent.move(RIGHT, 1)
    }
}
player.onChat("dom", function () {
    ściany()
    dach()
})
```

