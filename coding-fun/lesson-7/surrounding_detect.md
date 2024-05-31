### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Окружение 

## Шаг 1
Пока Агент **осматривает блок вниз**, а блок представляет собой **булыжник**, Агенту необходимо **двигаться вперед**. Если Агент **не** обнаруживает блок впереди, Агенту необходимо **двигаться вперед**, в противном случае ему необходимо **повернуть налево**.

```template
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
        
    }
})
```

```ghost
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) == STONE) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
})
```

