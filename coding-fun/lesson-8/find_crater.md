### @codeStart players set @s makecode 0
### @codeStop players set @s makecode 1

### @hideIteration true
### @explicitHints 1


# まわりを しらべよう

## Step 1
エージェントが **したの ブロックを かんちする** あいだ、まえに すすみます。エージェントが **したの ブロックを しらべて** **くうき** を みつけたら、``||player:say||`` コマンドで **クレーター はっけん！** と いいましょう。



```template
player.onChat("crater", function () {
            player.say("クレーター はっけん！")
})
```
```ghost
player.onChat("1", function () {
    while (agent.detect(AgentDetection.Block, DOWN)) {
        agent.move(FORWARD, 1)
    }
    if (agent.inspect(AgentInspection.Block, DOWN) == AIR) {
        player.say("クレーター はっけん！")
    }
})
```
