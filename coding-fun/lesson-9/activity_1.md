### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Камень 

## Шаг 1
Исправьте этот фрагмент кода. Вот что нужно сделать агенту: **переместиться** влево 4 раза**, **уничтожить вниз**, **переместиться вниз**. Если агент обнаруживает **камень** спереди, он должен сказать "Камень найден!", **Уничтожить вперед** и **собрать всё**. Если камень **не обнаружен**, Агент должен сказать: "Здесь нет камня!". Каждый раз после спуска агент должен **переместиться на 1 блок вверх** на поверхность. Это упражнение нужно повторить **4** раза.





```template
player.onChat("1", function () {
    for (let index = 0; index < 3; index++) {
        agent.move(RIGHT, 4)
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) != STONE) {
            player.say("Камень найден!")
            agent.destroy(FORWARD)
            agent.collectAll()
        } else {
            player.say("Здесь нет камня!")
        }
        agent.move(UP, 1)
    }
})
```
