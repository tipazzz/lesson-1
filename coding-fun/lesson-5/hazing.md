### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Растяжка 

## Шаг 1
Агенту нужно установить **растяжку**, чтобы волки не проникли внутрь. Через команду  ''||agent: выдать агенту||'' добавьте в инвентарь агента **Натяжной датчик** и установите количество **64**. Используйте цикл ''||loops: пока делать||'' и поместите в него условие.  

#### ~ tutorialhint
Не забывайте использовать **не** в условии. 

```blocks
player.onChat("растяжка", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
    	
    }
})

``` 
```ghost
player.onChat("растяжка", function () {
    agent.setItem(TRIPWIRE, 64, 1)
    while (!(agent.detect(AgentDetection.Block, FORWARD))) {
        agent.place(DOWN)
        agent.move(FORWARD, 1)
    }
})
```
