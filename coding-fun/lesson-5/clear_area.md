### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Очистите заросли!

## Шаг 1
Агенту необходимо уничтожить **8** блоков зарослей, двигаясь **вперед**. Есть **16** рядов зарослей, которые Агенту нужно уничтожить. Агенту необходимо ``||agent:агент: уничтожить вперёд||`` and ``||agent:агент: переместиться вперёд||`` **8** раз. 
#### ~ tutorialhint 
```blocks
player.onChat("foliage", function () {
    for (let index = 0; index < 8; index++) {
        for (let index = 0; index < 8; index++) {
        	
        }
{
        for (let index = 0; index < 8; index++) {
        	
        }

    }
})

```

```ghost
player.onChat("заросли", function () {
    for (let index = 0; index < 8; index++) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        for (let index = 0; index < 2; index++) {
            agent.move(FORWARD, 1)
            agent.turn(RIGHT_TURN)
        }
    }
})
```
