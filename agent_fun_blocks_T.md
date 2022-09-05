# Agent Śmieszne funkcje: Bloki

## Krok 1
Mamy gotowe 3 komendy ``||player:Przy poleceniu gracza||`` komenda **marchewka**,  ``||player:Przy poleceniu gracza||`` komenda **kurczak**  ``||player:Przy poleceniu gracza||`` i komenda **śnieżka**.

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
Dodaj nowy blok ``||player:Kiedy przedmiot został użyty||`` i wybierz **Blaze Rod**.  I w ``||player:Przy poleceniu gracza||`` nazwij to  **marchewka**, w kolejnej komendzie ``||player:Przy poleceniu gracza||``którą nzawiemy **kurczak**, i  w trzecim bloku``||player:Przy poleceniu gracza||`` który nazwiemy  **śnieżka**.

```blocks
player.onItemInteracted(BLAZE_ROD, function () {
    player.runChatCommand("marchewka")
    player.runChatCommand("kurczak")
    player.runChatCommand("śnieżka")
})
```

## Step 3

Naciśnij przycisk **Start**, wróć do Minecrafta i wpisz na czacie komendy **marchewka**, **kurczak**, **śnieżka**, aby zobaczyć co się stanie.
