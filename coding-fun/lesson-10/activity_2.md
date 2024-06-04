### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true 
### @explicitHints 1


# Окрестности 

## Шаг 1
Пока Агент **осмотравивает блок под собой** и обнаруживает **плотным льдом**, он проверяет условие: **если** Агент **обнаруживает блок справа**, он должен **двигаться вперед**. В противном случае он должен **двигаться вправо**. В рамках этого же цикла будем проверять ещё одно условие: **если** Агент **осматривает блок вниз** и это либо **булыжник** **, либо** **гравий**, то ему нужно **уничтожить вниз** и **собрать все**.





```template
player.onChat("1", function () {
    while (0 == 0) {
        if (true) {
        	
        } else {
        	
        }
        if (agent.inspect(AgentInspection.Block, DOWN) == COBBLESTONE ||agent.inspect(AgentInspection.Block, DOWN) == GRAVEL ) {
        	
        }
    }
})
```
```ghost
player.onChat("2", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != PACKED_ICE) {
        if (agent.detect(AgentDetection.Block, RIGHT)) {
            agent.move(FORWARD, 1)
        } else {
            agent.move(RIGHT, 1)
        }
        if (agent.inspect(AgentInspection.Block, DOWN) == COBBLESTONE || agent.inspect(AgentInspection.Block, DOWN) == GRAVEL) {
            agent.destroy(DOWN)
            agent.collectAll()
        }
    }
})
```
