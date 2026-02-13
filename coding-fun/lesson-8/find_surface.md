### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# マグマを みつけよう

## Step 1
エージェントを **まえに うごかす** プログラムを つくりましょう。エージェントが **したの ブロックを しらべて** **マグマじゃない** あいだ、エージェントは **したに うごく** ひつようが あります。


```ghost
player.onChat("magma", function () {
    agent.move(FORWARD, 1)
    while (agent.inspect(AgentInspection.Block, DOWN) != MAGMA_BLOCK) {
        agent.move(DOWN, 1)
    }
})
```

