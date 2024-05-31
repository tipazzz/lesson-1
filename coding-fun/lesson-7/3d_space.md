### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Поиск в трёхмерном пространстве

## Шаг 1
Чтобы решить эту задачу, вам нужно запрограммировать Агента добраться до **золотого блока** и собрать его. Агенту необходимо сделать это сначала на первом уровне, а затем **перейти на 3 уровня вверх** и повторить предыдущую процедуру.  

```template
player.onChat("1", function () {
    for (let index = 0; index < 2; index++) {
        
})
``` 
```ghost
player.onChat("1", function () {
    for (let index = 0; index < 2; index++) {
        while (agent.inspect(AgentInspection.Block, FORWARD) != GOLD_BLOCK) {
            if (!(agent.detect(AgentDetection.Block, FORWARD))) {
                agent.move(FORWARD, 1)
            } else {
                agent.turn(LEFT_TURN)
            }
        }
        agent.destroy(FORWARD)
        agent.collectAll()
        agent.move(UP, 3)
    }
})
```