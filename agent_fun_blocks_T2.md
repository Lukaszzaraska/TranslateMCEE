# Edycja śmiesznych funkcji agenta: Bloki

## Krok 1
Otrzymujesz następujące komendy ``||player:Przy poleceniu gracza||`` **marchewka**, **kurczak** i **śnieżka**.

```template
player.onChat("marchewka", function () {
    agent.setItem(CARROTS, 64, 1)
    for (let index = 0; index < 3; index++) {
        for (let index = 0; index < 5; index++) {
            agent.till(FORWARD)
            agent.move(FORWARD, 1)
            agent.place(DOWN)
        }
        agent.move(BACK, 5)
        agent.move(RIGHT, 2)
    }
})
player.onChat("kurczak", function () {
    for (let index = 0; index < 15; index++) {
        mobs.spawn(CHICKEN, pos(0, 0, 0))
    }
})
player.onChat("śnieżka", function () {
    for (let index = 0; index < 15; index++) {
        mobs.spawn(SNOWBALL_PROJECTILE_MOB, pos(0, 10, 0))
    }
})
```

## Krok 2
Zmień nazwę podanej komendy **marchewka** ``||player:Przy poleceniu gracza||`` na **pochodnie**. Zmień ``||agent:Ustaw blok lub przedmiot||`` na **Pochodnia** przy liczbie **32** w gnieździe **1**.

```blocks
player.onChat("Pochodnie", function () {
    agent.setItem(TORCHES, 32, 1)
})
```

## Krok 3

Zmodyfikuj istniejące pętle ``||loops:Powtórz||``, aby ukończyć 12 cykli sadzenia.

**UWAGA:**: Można to osiągnąć za pomocą pętli (4x3) lub (3x4).

```blocks
player.onChat("Pochodnie", function () {
    agent.setItem(TORCHES, 32, 1)
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 3; index++) {
        	
        }
        agent.move(BACK, 5)
        agent.move(RIGHT, 2)
    }
})
```

## Krok 4
Pobierz nowe polecenie ``||player:Kiedy przedmiot został użyty||`` i wybierz **trójząb**. Dodaj polecenie ``||player:Przy poleceniu gracza||`` o nazwie **pochodnie**. Dodaj kolejne polecenie ``||player:run chat||`` i nazwij je **kurczak**. Dodaj kolejne polecenie ``||player:Przy poleceniu gracza||`` i nazwij je **snowball**.

```blocks
player.onItemInteracted(BLAZE_ROD, function () { 
    player.runChatCommand("torches") 
    player.runChatCommand("chicken") 
    player.runChatCommand("snowball") 
})
```

## Krok 5
Naciśnij przycisk **Graj**, wróć do Minecrafta i wpisz na czacie polecenia **pochodnie**, **kurczak**, **śnieżka**, aby zobaczyć, co się stanie.

## Krok 6

Zmodyfikuj pozostałe podane komendy ``||player:Przy poleceniu gracza||`` **Kurczak** i **Śnieżka**. Możesz wybrać inny efekt dla tego doświadczenia kodowania.

## Krok 7

Naciśnij przycisk **Graj**, wróć do Minecrafta i wpisz na czacie polecenia **Kurczak** i **Śnieżka**, aby zobaczyć, co się stanie.
