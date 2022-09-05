# Agent Fun Functions: Blocks

## Step 1
Otrzymujesz komende ``||player:on chat||`` komenda **marchewka**, w ``||player:on chat||`` komenda **kurczak** w ``||player:on chat||`` i komenda **śnieżka*.

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

## Step 2
Dodaj nowy blok ``||player:on item used||`` i wybierz **Blaze Rod**.  I w ``||player:run chat||`` nazwij to  **marchewka**, w kolejnej komendzie ``||player:run chat||``którą nzawiemy **kurczak**, i  w trzecim bloku``||player:run chat||`` który nazwiemy  **śnieżka**.

```blocks
player.onItemInteracted(BLAZE_ROD, function () {
    player.runChatCommand("marchewka")
    player.runChatCommand("kurczak")
    player.runChatCommand("śnieżka")
})
```

## Step 3

Naciśnij przycisk **Start**, wróć do Minecrafta i wpisz na czacie komendy **marchewka**, **kurczak**, **śnieżka**, aby zobaczyć co się stanie.
