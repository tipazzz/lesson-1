### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Спираль

## Шаг 1
Пока агент **осматривает блок вперед**, а блок **не** является **золотым блоком**, агенту необходимо **продвигаться вперед**. Если Агент **не** обнаруживает блок вперед, Агенту также необходимо двигаться вперед, в противном случае ему необходимо **повернуть налево**. Когда Агент достигает **золотого блока**, ему необходимо **уничтожить** его и **собрать**.


```ghost
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
        if (!(agent.detect(AgentDetection.Block, FORWARD))) {
            agent.move(FORWARD, 1)
        } else {
            agent.turn(LEFT_TURN)
        }
    }
    agent.destroy(FORWARD)
    agent.collectAll()
})
```
