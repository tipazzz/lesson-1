### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Найди детеныша!

## Шаг 1
Запрограммируйте агента на прокладку пути, не зная, какой длины этот путь, используя блоки``||loops:пока||`` и ``||agent:агент: обнаружить вперед||``. Агенту необходимо добавить также блоки ``||agent:агент: уничтожить вперед||``, чтобы вы могли пройти по снегу! Когда закончите, нажмите кнопку **Play**, чтобы скомпилировать код. Не забудьте запустить свой код в Minecraft. 

#### ~ tutorialhint 
Не забудьте добавить блок ``||agent:агент: переместиться вперед||``.

```template
player.onChat("детеныш", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
    	
    }
})
```

```ghost
player.onChat("детеныш", function () {
    while (agent.detect(AgentDetection.Block, FORWARD)) {
        agent.destroy(FORWARD)
        agent.move(FORWARD, 1)
        agent.destroy(UP)
    }
})

```
