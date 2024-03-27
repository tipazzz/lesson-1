### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @flyoutOnly 1
### @explicitHints 1


# Запрограммируйте Агента на передвижение по черепашьим следам!

## Шаг 1
Перемещайте агента по черепашьим следам с помощью блока ``||agent:агент: переместиться вперед||`` к воротам. Когда закончите, нажмите кнопку **Play**, чтобы скомпилировать код. Не забудьте запустить свой код в Minecraft. 

```ghost
player.onChat("путь", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {
    	
 }
```
