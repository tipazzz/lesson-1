### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Бамбуковое убежище

## Шаг 1
Запрограммируйте Агента на посадку **3** блоков бамбука с каждой стороны песчаного участка. Добавьте блок ``||agent: агент: повернуться||``, чтобы убедиться, что Агент может завершить действие. 

#### ~ tutorialhint
Должно быть **2** цикла, один вложенный в другой.
 
```ghost
player.onChat("бамбк", function () {
    for (let index = 0; index < 3; index++) {
        agent.setItem(BAMBOO, 64, 1)
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(RIGHT_TURN)
})
```


