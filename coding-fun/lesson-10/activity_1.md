### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Окрестности 

## Шаг 1
Пока Агент **осмотравивает блок под собой** и обнаруживает **плотный лед**, он проверяет условие: **если** Агент **обнаруживает блок справа**, он должен **двигаться вперед**. В противном случае он должен **двигаться вправо**.




```ghost
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == PACKED_ICE) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.move(FORWARD, 1)
        } else {
            agent.move(RIGHT, 1)
        }
    }
})
```

