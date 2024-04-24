### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Бамбуковая изгородь

## Шаг 1
Перед вами стартовый код, который мы подготовили для вас.  Попробуйте сначала запустить его. Конечная цель состоит в том, чтобы посадить бамбук вдоль **4** сторон участка панды. 

```template
player.onChat("бамбук", function () {
    agent.setItem(BAMBOO, 64, 1)
    for (let index = 0; index < 16; index++) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
    agent.turn(LEFT_TURN)
})
```
