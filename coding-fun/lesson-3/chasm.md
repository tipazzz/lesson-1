### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Великая пропасть!

## Шаг 1
Запрограммируйте Агента на **строительство моста** через пропасть во льду. Используйте блок ``||agent:выдать агенту блок или предмет||``, чтобы обеспечить наличие у Агента необходимых материалов в инвентаре. Выберите **Oak Planks** в качестве строительного материала и **64** для **количества блоков**. Цикл ``||loops:пока||`` будет выполняться пока Агент **не** обнаружит блок под собой, т.е. снизу. Запрограммируйте Агента на размещение дубовых досок **вниз** и перемещение **вперед** для создания моста.    


```template
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 1, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, DOWN))) {
    	
    }
})
```

```ghost
player.onChat("chasm", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})

``` 

