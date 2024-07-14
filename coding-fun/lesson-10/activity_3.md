### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Окрестности 

## Шаг 1
Пока Агент **осмотравивает блок под собой** и **не** обнаруживает **плотный лед**, запрограммируйте Агента на поиск, **уничтожение** и **сбор** следующих блоков: **железо**, **золото**, **изумруд** и **алмаз**. Агент должен уничтожить и собрать все блоки с данными ресурсами. Подумайте как это можно сделать.





```ghost
player.onChat("3", function () {
    agent.setItem(STONE, 64, 1)
    while (agent.inspect(AgentInspection.Block, DOWN) != PACKED_ICE) {
        if (agent.inspect(AgentInspection.Block, DOWN) == IRON || agent.inspect(AgentInspection.Block, DOWN) == GOLD) {
            agent.turn(LEFT_TURN)
            agent.destroy(DOWN)
            agent.collectAll()
        }
        if (agent.inspect(AgentInspection.Block, DOWN) == DIAMOND || agent.inspect(AgentInspection.Block, DOWN) == EMERALD) {
            agent.turn(RIGHT_TURN)
            agent.destroy(DOWN)
            agent.collectAll()
        }
        agent.move(FORWARD, 1)
    }
})
```

