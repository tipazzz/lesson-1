### @hideIteration false 
### @flyoutOnly 1
### @explicitHints 1


# Запрограммируйте Агента на передвижение по черепашьим следам!

## Шаг 1
Перемещайте агента по черепашьим следам с помощью блока ``||agent:агент: переместиться вперед||``. 

#### ~ tutorialhint 
Попробуйте использовать блок ``||loops:повторить||``, чтобы сделать код более эффективным.

## Шаг 2
Когда закончите, нажмите кнопку **Play**, чтобы скомпилировать код. Не забудьте запустить свой код в Minecraft. 

```blocks
player.onChat("run", function () {
    agent.move(FORWARD, 1)
    agent.turn(LEFT_TURN)
})
for (let index = 0; index < 4; index++) {
    	
 }
```
