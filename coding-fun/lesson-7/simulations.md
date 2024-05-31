### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Симулятор 

## Шаг 1
Добро пожаловать в Симулятор! Запрограммируйте своего Агента собирать **золотые блоки** и уничтожать препятствия на своем пути.


```template
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (agent.inspect(AgentInspection.Block, LEFT) == GOLD_BLOCK) {
        	
        }
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.turn(LEFT_TURN)
        }
    }
})

```
```ghost
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (agent.inspect(AgentInspection.Block, LEFT) == GOLD_BLOCK) {
            agent.destroy(LEFT)
            agent.collectAll()
        }
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.turn(LEFT_TURN)
        }
        agent.move(FORWARD, 1)
    }
    agent.destroy(FORWARD)
    agent.collectAll()
})
```
