### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Ремонт марсохода 

## Шаг 1
Исправьте этот фрагмент кода. Вот цель: пока Агент **проверяет** блок **воздуха** и **не** находит его, ему нужно **двигаться вправо**. Если Агент находит блок ** Block of Lapis Lazuli** ** спереди**, ему нужно **двигаться вправо**, **повернуть влево**, затем **двигаться вправо**. После этого агент должен сказать: «Нашел разрыв!» и **поместить блок красного камня вперед**.



```template
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) == AIR) {
        agent.move(RIGHT, 1)
        if (agent.inspect(AgentInspection.Block, FORWARD) == LAPIS_LAZULI_BLOCK) {
            agent.move(RIGHT, 1)
            agent.turn(RIGHT_TURN)
            agent.move(LEFT, 1)
        }
    }
    player.say("Нашёл разрыв!")
    agent.setItem(GRASS, 1, 1)
    agent.place(FORWARD)
})
```
