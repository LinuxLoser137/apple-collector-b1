 


/**
 * To Do List:
 * 
 * 1) Set Background (Scene)
 * 
 * 2)Create Sprite **collector (Sprites)
 * 
 * 3)Set the movement for the sprite/collector (Controller)
 * 
 * 4)Make sure the sprite/collector stays on the screen (Sprites)
 * 
 * 5)Create a block of code that will update every 1500ms (Game)
 * 
 * 6)Create another sprite/apple but this sprite/apple will be eaten/overlapped/the food (Sprites)
 * 
 * 7)Set where you want the sprite/apples to spawn (Sprites/Math)
 * 
 * 8)Create a new block of code for what happens when your first sprite/collector overlaps your second sprite/apple (Sprites)
 * 
 * 9)Create a destroy feature for your food sprite when your other sprite overlaps it. (Sprites)
 * 
 * 10)Create a change in the score when the second sprite is eaten **apple (info)
 */
/**
 * <--Starts your score at zero
 */
/**
 * <-- Don't forget to name your asset "collector" (it can be named at the bottom of the screen where you created your sprite.)
 */
/**
 * <-- Controls how the "Collector" moves.
 * 
 * <-- Controls your sprite and tells it not to leave the screen
 */
/**
 * <-- Don't forget to name your asset "apple" (it can be named at the bottom of the screen where you created your sprite.)
 */
/**
 * <-- Spawns the apples in random places
 */
/**
 * <-- Controls what happens when the apple is caught.
 */
// <-- Creates what what happens when the "apple" is overlapped by the "collector".
// 
// <-- Score increases by 1 every time "Collector" overlaps "apple"
sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (player3, food) {
    food.destroy(effects.disintegrate, 200)
    info.changeScoreBy(1)
})
let apple: Sprite = null
// Apple Collector - Beginner 1
scene.setBackgroundColor(7)
let player2 = sprites.create(assets.image`collector`, SpriteKind.Player)
controller.moveSprite(player2, 100, 100)
player2.setFlag(SpriteFlag.StayInScreen, true)
info.setScore(0)
// Spawn apples every 1.5 seconds (NO custom function used)
game.onUpdateInterval(1500, function () {
    apple = sprites.create(assets.image`apple`, SpriteKind.Food)
    apple.setPosition(randint(10, 150), randint(10, 110))
})
