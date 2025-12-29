
# Apple collector

## Beginner Game 1


## Step 1
Set background ``||Scene: set background color to||``
```blocks
scene.setBackgroundColor(7)
```
## Step 2
Create player 2 ``||Sprites: set mySprite to sprite of kind player||``
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
```
## Step 3
Set your sprite/apple to a player ``||Sprites: set mySprite to sprite of kind player||``
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
```
## Step 4
Add controls to your game ``||set player2 stay in screen on||``
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
```
## Step 5
Set the sprite/player to stay in the screen frame
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
info.setScore(0)
```
## Step 6
Set your sprite/apple to a player ``||Sprites: set mySprite to sprite of kind player||``
```blocks```
let apple = sprites.create(assets.image`apple`, SpriteKind.Player)
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
info.setScore(0)
```
## Step 7
Set the score to zero
```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (player3, food) {
    food.destroy(effects.disintegrate, 200)
    info.changeScoreBy(1)
})
```
## Step 8
```blocks```
let apple = sprites.create(assets.image`apple`, SpriteKind.Player)
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
info.setScore(0)
```
## Step 9
Set the score to change by one when Collector overlaps the Apple
```blocks
game.onUpdateInterval(1500, function () {
    apple = sprites.create(assets.image`apple`, SpriteKind.Food)
    apple.setPosition(randint(10, 150), randint(10, 110))
})
```