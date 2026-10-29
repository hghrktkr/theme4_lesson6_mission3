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