## Krok 1
Uruchom program 

```template
player.onChat("s", function (num1) {
    for (let index = 0; index < num1; index++) {
        if (agent.inspect(AgentInspection.Block, DOWN) == 236) {
            loops.pause(100)
            agent.setAssist(PLACE_ON_MOVE, true)
            agent.move(BACK, 1)
        }
    }
})
player.onChat("a", function (num1) {
    for (let index = 0; index < num1; index++) {
        if (agent.inspect(AgentInspection.Block, DOWN) == 236) {
            loops.pause(100)
            agent.setAssist(PLACE_ON_MOVE, true)
            agent.move(LEFT, 1)
        }
    }
})
player.onChat("w", function (num1) {
    for (let index = 0; index < num1; index++) {
        if (agent.inspect(AgentInspection.Block, DOWN) == 236) {
            loops.pause(100)
            agent.setAssist(PLACE_ON_MOVE, true)
            agent.move(FORWARD, 1)
        }
    }
})
player.onChat("d", function (num1) {
    for (let index = 0; index < num1; index++) {
        if (agent.inspect(AgentInspection.Block, DOWN) == 236) {
            loops.pause(100)
            agent.setAssist(PLACE_ON_MOVE, true)
            agent.move(RIGHT, 1)
        }
    }
})
agent.setItem(STONE, 1, 1)
agent.setSlot(1)

```
