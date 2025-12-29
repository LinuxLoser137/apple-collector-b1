 # Apple collector

## Beginner Game 1

//Create your first sprite (apple)
```blocks
scene.setBackgroundColor(7)
```
## Step 2
Add a background ``||scene:set background color||``
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
```
## Step 3
Set your sprite to player ``||sprites:set mySprite to sprite of kind Player||``
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
```
Add controls to your game.
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
```
//Set the sprite/player to stay in the screen frame
```blocks
let apple = sprites.create(assets.image`collector`, SpriteKind.Food)
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
info.setScore(0)
```
```blocks
//Set the score to zero
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (player3, food) {
    food.destroy(effects.disintegrate, 200)
    info.changeScoreBy(1)
})
```

//Set the score to change by one when Collector overlaps the Apple
```blocks
game.onUpdateInterval(1500, function () {
    let apple = sprites.create(assets.image`apple`, SpriteKind.Food)
    apple.setPosition(randint(10, 150), randint(10, 110))
})
```


