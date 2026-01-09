# Apple collector

## Beginner Game 1 @unplugged
This is a game for beginners 

## Step 2
Add a background ``||scene:set background color||``
```blocks
scene.setBackgroundColor(7)
```
## Step 3
Set your sprite to player ``||sprites:set mySprite to sprite of kind Player||``
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
```
## Step 4
Add controls to your game. ``||Controller: moveSprite(player2, 100, 100)||``
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
```
## Step 5
Set the sprite/player to stay in the screen frame ``||Sprites:setFlag(SpriteFlag.StayInScreen, true)||``
```blocks
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
```
## Step 6
Create a sprite called apple. ``||sprites:create(assets.image`collector`, SpriteKind.Food)||``
```blocks
let apple = sprites.create(assets.image`collector`, SpriteKind.Food)
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
```
## Step 7
Set score to zero ``||Info:setScore(0)||``
```blocks
let apple = sprites.create(assets.image`collector`, SpriteKind.Food)
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
info.setScore(0)
```
## Step 8
Set blocks to destroy food and increase the score ``||sprites:onOverlap(SpriteKind.Player, SpriteKind.Food)||``
``||sprites:destroy(effects.disintegrate, 200)||``
``||info:changeScoreBy(1)||``
```blocks
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (player3, food) {
    food.destroy(effects.disintegrate, 200)
    info.changeScoreBy(1)
})
```
## Step 9
Set an interval function. The apples need to regenerate and appear in a random position ``||game:onUpdateInterval(1500)||``
``||sprites:create(assets.image`apple`, SpriteKind.Food)||``
``||sprites:setPosition(randint(10, 150), randint(10, 110))||``
})
```blocks
game.onUpdateInterval(1500, function () {
    let apple = sprites.create(assets.image`apple`, SpriteKind.Food)
    apple.setPosition(randint(10, 150), randint(10, 110))
})
```


