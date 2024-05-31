### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Доберитесь до магмы

## Шаг 1
Запрограммируйте Агента на **движение вперед**. Пока Агент **проверяет** блок **вниз** и это **не магма**, Агент должен **двигаться вниз**. 


```ghost
player.onChat("1", function () {
    agent.move(FORWARD, 1)
    while (agent.inspect(AgentInspection.Block, DOWN) != MAGMA_BLOCK) {
        agent.move(DOWN, 1)
    }
})
```
