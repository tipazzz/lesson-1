### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Обезопасьте территорию

## Шаг 1
Запрограммируйте Агента на создание **дубового забора**. Агенту нужно разместить **дубовый забор** справа, разрушить препятствия и двигаться вперед. Забор должен быть длиной **17 блоков**. 

#### ~ tutorialhint
Убедитесь, что Агент размещает справа, а уничтожает перед собой. 

```blocks
player.onChat("забор", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
            }
})
```
```ghost
player.onChat("забор", function () {
    agent.setItem(OAK_FENCE, 64, 1)
    for (let index = 0; index < 17; index++) {
        agent.place(RIGHT)
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
    }
})
``` 

