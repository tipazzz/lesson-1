### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Куриный переворот

## Шаг 1
Агенту необходимо разместить **2** слоя по **9** блоков **железной решетки**. У нас есть  **4** стороны, которые должны иметь **железную решетку**. Не забывайте использовать ``||agent: агент: переместиться вверх||`` для постройки второго слоя.

#### ~ tutorialhint
В конце у вас будет **3** команды ``||loops: повторить|``, вложенные друг в друга. Убедитесь, что у Агента в инвентаре более 64 блоков!

```ghost
player.onChat("курица", function () {
    for (let index = 0; index < 2; index++) {
        agent.setItem(IRON_BARS, 1, 1)
        for (let index = 0; index < 4; index++) {
            for (let index = 0; index < 9; index++) {
                agent.place(DOWN)
                agent.move(FORWARD, 1)
            }
            agent.turn(RIGHT_TURN)
        }
        agent.move(UP, 1)
    }
})
```