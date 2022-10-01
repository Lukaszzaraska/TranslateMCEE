## Krok 1
Uruchom program 

```template
player.onTravelled(SNEAK, function () {
    if (blocks.testForBlock(GLOWSTONE, pos(0, -14, 0))) {
        blocks.place(kolor, pos(0, -12, 0))
    }
})
player.onItemInteracted(WOODEN_HOE, function () {
    gameplay.title(mobs.target(NEAREST_PLAYER), "Kolor zmieniony na", "czarny")
    kolor = BLACK_CARPET
})
player.onItemInteracted(IRON_SWORD, function () {
    kolor = WHITE_CARPET
    gameplay.title(mobs.target(NEAREST_PLAYER), "Kolor zmieniony na", "biały")
})
player.onItemInteracted(GOLDEN_SWORD, function () {
    kolor = YELLOW_CARPET
    gameplay.title(mobs.target(NEAREST_PLAYER), "Kolor zmieniony na", "żółty")
})
player.onItemInteracted(NETHERITE_SWORD, function () {
    gameplay.title(mobs.target(NEAREST_PLAYER), "Gumka włączona", "")
    kolor = AIR
})
function niebieski () {
    blocks.place(BLUE_CONCRETE, world(-34, 68, -475))
    while (true) {
        loops.pause(200)
        if (Math.round(player.getOrientation()) > 79 && Math.round(player.getOrientation()) < 112) {
            break;
        }
    }
    blocks.place(WHITE_CONCRETE, world(-34, 68, -475))
}
loops.forever(function () {
    loops.pause(1000)
    if (blocks.testForBlock(TRIPWIRE, player.position())) {
        loops.pause(1000)
        gameplay.title(mobs.target(NEAREST_PLAYER), "Kliknij W", "Żeby iść prosto")
        loops.pause(3000)
        gameplay.title(mobs.target(NEAREST_PLAYER), "Kliknij D", "")
        loops.pause(2000)
        gameplay.title(mobs.target(NEAREST_PLAYER), "Żeby iść w prawo", "")
        loops.pause(3000)
        gameplay.title(mobs.target(NEAREST_PLAYER), "Kliknij A", "")
        loops.pause(2000)
        gameplay.title(mobs.target(NEAREST_PLAYER), "Żeby iść w lewo", "")
        loops.pause(3000)
        gameplay.title(mobs.target(NEAREST_PLAYER), "Kliknij S", "")
        loops.pause(2000)
        gameplay.title(mobs.target(NEAREST_PLAYER), "Żeby iść do tyłu", "")
    }
    loops.pause(5000)
})
player.onItemInteracted(WOODEN_SWORD, function () {
    gameplay.title(mobs.target(NEAREST_PLAYER), "Kolor zmieniony na", "czerwony")
    kolor = RED_CARPET
})
function zielony () {
    blocks.place(LIME_CONCRETE, world(-30, 68, -475))
    while (true) {
        loops.pause(200)
        if (Math.round(player.getOrientation()) < -70 && Math.round(player.getOrientation()) > -100) {
            break;
        }
    }
    blocks.place(WHITE_CONCRETE, world(-30, 68, -475))
}
player.onItemInteracted(STONE_SWORD, function () {
    gameplay.title(mobs.target(NEAREST_PLAYER), "Kolor zmieniony na", "niebieski")
    kolor = BLUE_CARPET
})
function wstep () {
    mobs.applyEffect(NIGHT_VISION, mobs.target(NEAREST_PLAYER), 600, 1)
    gameplay.title(mobs.target(LOCAL_PLAYER), "Nakieruj myszką na kolor ", "")
    player.say("Niebieski")
    loops.pause(1000)
    gameplay.title(mobs.target(LOCAL_PLAYER), "niebieski", "")
    niebieski()
    gameplay.title(mobs.target(LOCAL_PLAYER), "Nakieruj myszką na kolor ", "")
    player.say("zielony")
    loops.pause(1000)
    gameplay.title(mobs.target(LOCAL_PLAYER), "zielony", "")
    zielony()
    gameplay.title(mobs.target(LOCAL_PLAYER), "Nakieruj myszką na kolor ", "")
    player.say("czerwony")
    loops.pause(1000)
    gameplay.title(mobs.target(LOCAL_PLAYER), "czerwony", "")
    czerwony()
    gameplay.title(mobs.target(LOCAL_PLAYER), "Nakieruj myszką na kolor ", "")
    player.say("żółty")
    loops.pause(1000)
    gameplay.title(mobs.target(LOCAL_PLAYER), "żółty", "")
    żółty()
    gameplay.title(mobs.target(LOCAL_PLAYER), "Brawo udało się", "")
    loops.pause(1000)
    player.teleport(world(-36, 68, -436))
    mobs.clearEffect(mobs.target(LOCAL_PLAYER))
}
player.onItemInteracted(DIAMOND_SWORD, function () {
    gameplay.title(mobs.target(NEAREST_PLAYER), "Kolor zmieniony na", "zielony")
    kolor = LIME_CARPET
})
function czerwony () {
    blocks.place(RED_CONCRETE, world(-32, 68, -477))
    while (true) {
        loops.pause(200)
        if (Math.round(player.getOrientation()) > 170 && Math.round(player.getOrientation()) < 202) {
            break;
        }
    }
    blocks.place(WHITE_CONCRETE, world(-32, 68, -477))
}
function żółty () {
    blocks.place(YELLOW_CONCRETE, world(-32, 68, -473))
    while (true) {
        loops.pause(200)
        if (Math.round(player.getOrientation()) > 350 && Math.round(player.getOrientation()) < 360 || Math.round(player.getOrientation()) > 0 && Math.round(player.getOrientation()) < 22) {
            break;
        }
    }
    blocks.place(WHITE_CONCRETE, world(-32, 68, -473))
}
let kolor = 0
kolor = RED_CARPET
blocks.place(STONE, world(-30, 76, -416))
while (true) {
    if (blocks.testForBlock(BROWN_CONCRETE, positions.add(
    player.position(),
    pos(0, -1, 0)
    ))) {
        wstep()
        break;
    }
}


```
