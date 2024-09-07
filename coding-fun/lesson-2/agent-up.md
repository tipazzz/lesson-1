# coding-fun/lesson-2/agent-up
### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# Запрограммируйте агента на переход на золотую пластину!

## Step 1
Используйте команды ``||player:при команде чата||`` and  ``||agent:агент:переместиться вперед||`` чтобы запрограммировать Агента на движение к золотой пластине. Вы можете запрограммировать агента на перемещение **вверх**. Когда закончите, нажмите кнопку **Play** для компиляции кода. Перейдите в Minecraft, чтобы запустить свой код в игре.



```ghost
player.onChat("up", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})

```  
