### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Выследить марсоход 

## Шаг 1
Исправьте этот фрагмент кода. Цель заключается в следующем: пока Агент **осматривает блок вперед** и это не **кварц**, ему нужно **двигаться вперед**. Если он **обнаруживает** **золотой блок снизу**, ему нужно **повернуть направо**. Если он обнаружит **блок железа снизу**, ему нужно **повернуть налево**. В конце агент должен сказать: «Найден марсоход!».




```template
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, FORWARD) != BLOCK_OF_QUARTZ) {
            if (agent.inspect(AgentInspection.Block, UP) == GOLD_BLOCK) {
            agent.turn(LEFT_TURN)
        }
            if (agent.inspect(AgentInspection.Block, RIGHT) == IRON_BLOCK) {
            agent.turn(RIGHT_TURN)
        }
        agent.move(FORWARD, 1)
    }
    player.say("Нашёл марсоход!")
})
```
