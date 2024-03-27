### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Разлученная семья!

## Шаг 1
Запрограммируйте Агента на строительство моста через пропасть во льдах. Убедитесь, что у Агента есть **64** блока **дубовых досок** в инвентаре. 

#### ~ tutorialhint 
Не забывайте использовать **не** в цикле **пока**. Подумайте, где вы хотите, чтобы агент размещал блоки. 


```ghost
player.onChat("семья", function () {
    agent.setItem(PLANKS_OAK, 64, 1)
    agent.move(FORWARD, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
        agent.turn(LEFT_TURN)
    }
})

```
