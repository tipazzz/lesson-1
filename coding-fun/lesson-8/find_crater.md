зх### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Окружение 

## Шаг 1
Пока  Агент **обнаруживает блок снизу**, он должен двигаться вперед. Если Агент **проверит блок** и найдет **воздух**, то используя команду ``||player:сказать||``, он должен сообщить **Найден кратер!**. 



```template
player.onChat("1", function () {
            player.say("Найден кратер!")
})
```
```ghost
player.onChat("1", function () {
    while (agent.detect(AgentDetection.Block, DOWN)) {
        agent.move(FORWARD, 1)
    }
    if (agent.inspect(AgentInspection.Block, DOWN) == AIR) {
        player.say("Crater found!")
    }
})
```
