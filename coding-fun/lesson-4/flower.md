### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# Сделайте территорию красивой!

## Шаг 1
Вам нужно посадить **14 одуванчиков** вдоль **4** сторон укрытия. Агент может посадить **14** одуванчиков на одну сторону. 

#### ~ tutorialhint 
Не забудьте изменить количество в блоке ``||agent: выдать агенту блок или предмет ||``. 


```ghost
player.onChat("цветы", function () {
    for (let index = 0; index < 4; index++) {
        for (let index = 0; index < 14; index++) {
            agent.setItem(YELLOW_FLOWER, 64, 1)
            agent.place(DOWN)
            agent.move(FORWARD, 1)
        }
        agent.turn(RIGHT_TURN)
    }
})

```
