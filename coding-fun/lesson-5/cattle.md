### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Ферма

## Шаг 1
Посмотрите на стартовый код и попробуйте его запустить. Этот код позволяет перемещаться  Агенту без подсчета блоков. Посмотрите на путь, по которому должен пройти агент, и убедитесь, что вы закончили последовательность программирования правильными поворотами для агента. Убедитесь, что агент может дотянуться до **золотой пластины**.  

```template
player.onChat("овца", function () {
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})

```
