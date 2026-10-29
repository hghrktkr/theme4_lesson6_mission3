# 階段を作ろう！

```blocks

let 開始位置: Position = null
function 階段を作る (開始位置: Position) {
    blocks.fill(
    GLASS,
    positions.add(
    開始位置,
    pos(-2, 0, 0)
    ),
    positions.add(
    開始位置,
    pos(2, 3, 0)
    ),
    FillOperation.Replace
    )
    blocks.fill(
    AIR,
    positions.add(
    開始位置,
    pos(-1, 0, 0)
    ),
    positions.add(
    開始位置,
    pos(1, 2, 0)
    ),
    FillOperation.Replace
    )
}
player.onChat("run", function () {
    開始位置 = positions.add(
    player.position(),
    pos(0, 0, 5)
    )
    while (blocks.testForBlock(WATER, 開始位置)) {
        階段を作る(開始位置)
        開始位置 = positions.add(
        開始位置,
        pos(0, 1, 1)
        )
    }
})


```

```template

let 開始位置: Position = null
function トンネルを作る (開始位置: Position) {
}
player.onChat("run", function () {
    開始位置 = positions.add(
    player.position(),
    pos(0, 0, 5)
    )
})

```


## 地上へ続く階段をならべよう！ @unplugged
<p>関数を使って、地上へつづく階段を作ろう！</p>
<n></n>
<img style="display: block; margin: auto;" height="50%" width="50%" src="https://vcode-esia.com/images_for_world_data/Basic/Theme4/Lesson6/L6_complete3.gif">



## 目標(もくひょう)
<p>今回は、**いちから自分で考えてプログラミングしよう！**</p>
<p>・**ガラス**でできた階段を作ろう！</p>
<p>①変数``||variables.開始位置||``には、ブロックを並べ始める場所の座標が入っている</p>
<p>②関数``||functions.階段を作る||``の中に、下のような形にガラスを並べるようにプログラミングする</p>
<p>②階段の長さはわからないので、``||functions.階段を作る||``を``||variables.開始位置||``の場所に**水がなくなるまでくりかえし**呼び出して、地上までの階段にする</p>
<p>さっきまでとは、**階段を作る方向がちがう**ので注意しよう！</p>
<br></br>
<img width="100%" src="https://vcode-esia.com/images_for_world_data/Basic/Theme4/Lesson6/L6_front_view3.png">



## プログラミングのヒント
<p>下のヒントを参考にしてみよう！</p>
<p>今回は、トンネルを作る長さが分からないので、``||variables.開始位置||``が**水**の間はトンネルを作るようにします。</p>
<p>``||loops.もし～ならくりかえし||``と、``||blocks.～が(~0, ~0, ~0)に存在する||``、``||variables.開始位置||``を組み合わせましょう！</p>
<p>階段の形になるよう、``||variables.開始位置||``を**南と上に動かす**ことをわすれないようにしましょう！</p>
<br></br>
<p>むずかしいときは、**Theme3 Lesson8**を復習してみよう！</p>



## 実行しよう！
<p>プログラミングができあがったら、▶ボタンを押(お)して実行しよう</p>
<br></br>
<img height="50%" width="50%" src="https://vcode-esia.com/images_for_world_data/school/1st/execute.gif">
<br></br>
<p>ゲーム画面にもどったら、思った通りにプログラムが動くか試してみよう！</p>
<p>うまくいかなかったときは、どこが良くなかったのか、自分のプログラムを見なおして何度でもちょうせんしてみよう</p>
<br></br>
<img width="100%" src="https://vcode-esia.com/images_for_world_data/Basic/Theme4/Lesson6/L6_complete3.gif">
<br></br>
<p>できあがったのを確認したら、**村人に話しかけよう**</p>

```blocks

let 開始位置: Position = null
function 階段を作る (開始位置: Position) {
    blocks.fill(
    GLASS,
    positions.add(
    開始位置,
    pos(-2, 0, 0)
    ),
    positions.add(
    開始位置,
    pos(2, 3, 0)
    ),
    FillOperation.Replace
    )
    blocks.fill(
    AIR,
    positions.add(
    開始位置,
    pos(-1, 0, 0)
    ),
    positions.add(
    開始位置,
    pos(1, 2, 0)
    ),
    FillOperation.Replace
    )
}
player.onChat("run", function () {
    開始位置 = positions.add(
    player.position(),
    pos(0, 0, 5)
    )
    while (blocks.testForBlock(WATER, 開始位置)) {
        階段を作る(開始位置)
        開始位置 = positions.add(
        開始位置,
        pos(0, 1, 1)
        )
    }
})

```
