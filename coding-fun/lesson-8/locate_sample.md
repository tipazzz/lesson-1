### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Найдите образец! 

## Step 1
Пока Агент **осматривает блок внизу** и **не** находит **синий лед**, запрограммируйте Агента на **разрушение** и **движение вниз**. Когда агент обнаруживает **синий лед**, он должен **уничтожить** и **собрать** образец. 

```ghost 
player.onChat("1", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != ICE) {
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
    }
    agent.destroy(DOWN)
    agent.collectAll()
    
})
```

