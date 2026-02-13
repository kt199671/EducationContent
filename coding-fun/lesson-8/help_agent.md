### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# てつ

## Step 1
エージェントが **したの ブロックを しらべて** **てっこうせき** じゃない あいだ、**まえに すすむ** ひつようが あります。エージェントが **まえに ブロックを かんちしたら**、**まえを こわす** ひつようが あります。エージェントが てつを みつけたら、**あつめる** プログラムを つくりましょう。ブロックを あつめるには、まず こわす ひつようが あります。

```ghost
player.onChat("4", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != IRON_ORE) {
        if (agent.detect(AgentDetection.Block, FORWARD)) {
            agent.destroy(FORWARD)
        }
        agent.move(FORWARD, 1)
    }
    player.say("てっこうせき はっけん！")
    agent.destroy(DOWN)
    agent.collectAll()
})
```
