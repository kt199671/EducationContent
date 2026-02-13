### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# サンプルを みつけよう！

## Step 1
エージェントが **したの ブロックを しらべて** **あおい こおり** を **みつけない** あいだ、**こわして** **したに うごく** プログラムを つくりましょう。エージェントが **あおい こおり** を みつけたら、**したを こわして** サンプルを **あつめ** ましょう。

```ghost
player.onChat("ice", function () {
    while (agent.inspect(AgentInspection.Block, DOWN) != ICE) {
        agent.destroy(DOWN)
        agent.move(DOWN, 1)
    }
    agent.destroy(DOWN)
    agent.collectAll()

})
```


