### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Железо

## Step 1
Пока Агент **проверяет блок снизу**, и этот блок не является **железной рудой**, он должен **двигаться вперед**. Если Агент **обнаруживает блок перед собой**, то он должен **уничтожить вперед**. Когда Агент найдет железо, запрограммируйте его на его **сбор**. Обратите внимание, что для того, чтобы собрать блок, Агент должен сначала уничтожить его. 

```ghost
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != IRON_ORE) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
    }
    player.say("Found the iron ore!")
    agent.destroy(DOWN)
    agent.collectAll()
})
```
