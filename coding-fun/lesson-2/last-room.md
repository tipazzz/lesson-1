### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# Запрограммируйте агента на переход на золотую пластину!

## Шаг 1
Запрограммируйте агента так, чтобы он добрался до золотой пластины. Вам нужно оставаться на своей золотой пластине, в то время как агенту нужно оставаться на другой. Когда закончите, нажмите кнопку **Play** для компиляции кода. Перейдите в Minecraft, чтобы запустить свой код.


```ghost
player.onChat("last", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
```  
