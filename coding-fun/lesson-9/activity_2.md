### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Глубокий камень 

## Шаг 1
Исправьте этот фрагмент кода. Цель агента заключается в том, чтобы углубиться в поверхность, пока он не наткнется на **золотой** блок слева**. По пути вниз Агент определит, находится ли перед ним **Камень**, и заберет его.

```template
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, LEFT) == AIR) {
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
            if (agent.inspect(AgentInspection.Block, FORWARD) != GRASS) {
                player.say("Нашел камень!")
                agent.destroy(FORWARD)
                agent.collectAll()
        }
    }
})
```
