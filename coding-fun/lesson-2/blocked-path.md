### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# Запрограммируйте Агента двигаться по черепашьим следам и разрушать препятствия!

## Шаг 1
Используйте Агента для **уничтожения ствола дерева**, который находится на пути, с помощью блоков ``||agent: агент: уничтожить вперед||`` и ``||agent:агент: собрать все||``. Попробуйте использовать блок ``||loops:повторить||``, чтобы сделать код более эффективным. Когда закончите, нажмите кнопку **Play**, чтобы скомпилировать код. Не забудьте запустить свой код в Minecraft. 


```ghost
player.onChat("путь", function () {
    for (let index = 0; index < 4; index++) {
        agent.turn(LEFT_TURN)
        agent.move(FORWARD, 1)
        agent.destroy(FORWARD)
        agent.collectAll()
    }
})
```

