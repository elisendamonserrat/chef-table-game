# Chef's Table Game 
Being a chef is not easy! If you miss an ingredient you migth end up with a completely different dish and some angry customers. Also, you can get cut with kitchen knives. The object of the game is to help Chef Cocô to get all the ingredients he needs on time without being hurt.

## How does it work?
The game screen is a interface where food ingredients and knives will be displayed. Our player, Chef Cocô, can move in all directions and as he is in a hurry, he needs to grab all the ingredients he needs in les than 1 minute. The game is won when our Chef takes the 10 ingredients he needs in 1 minute or less!! If he accidentally bumps into a knive.. game over!

A new ingredient will appear everytime another ingredient is taken - so, you should be fast! Also, as time runs more knives will be in the board game...

* * *
## MVP
### Technique
HTML5, DOM, **Canvas** and Vanilla **Javascript**

### Game states
* __Start Screen__
  * Title
  * Start Game button
  * Player's name input field
* __Game Screen__
  * Canvas
* __Game Over Screen__
  * Play again button
  * Go to start screen button

### Game
* Create interface
* Create player
* Move player
  * Press arrow keys to move the player around the board.
* Create ingredients
  * Each ingredient will be created once the previous one is taken
* Create knives
  * Define a setInterval where knives will be created every 10 seconds
* Check collision
  * If there is a collision with an ingredient => player gains points and new ingredient is shown
  * If there is a collision with a knive => Game Over => Show Game Over Screen
* * *

## BACK LOG
### Music
* Add music on and off button to setup
* Add sound effects on and off button to setup
### Levels
* Check phase and increase level
  * Increase the speed of knives being created 

## MVP Wireframe

![Alt text](https://s3.amazonaws.com/assets.mockflow.com/app/wireframepro/company/Cc59c887c2a9c4f55be8f2d746ee41db0/projects/Md053a6749e754823bb8b8173fa39a3d81604153255273/pages/d687c4b2f7b34f02999f4d2cb430a3c4/image/d687c4b2f7b34f02999f4d2cb430a3c4.png "Chef's Table Wireframe")

## Data structure
__main.js__
````
createStartScreen(id);
createGameScreen(id);
createGameOverScreen(id);
destroyStartScreen();
destroyGameScreen();
destroyGameOverScreen();
let game = new Game({
    this.rows,
    this.columns,
    ctx: ctx,
    // backgroundimage = 'una imagen del fondo',
    this.ingredients,
    this.knives,
    this.player
  });
game.init();
````
__Game.js__
````
function Game(options){};
Game.drawBoard();
Game.drawPlayer();
Game.generateIngredients();
Game.generateKnives();
Game.gameOver();
Game.init();
Game.startTimer();
````
__Player.js__
````
function Player(){
  this.width;
  this.height;
  this.image;
  this.points
};
Player.move();
````
__Items.js__
````
function Items(){
  this.width;
  this.height;
  this.image
};
drawItems();

*Here there will be subclasses for ingredients and for knives*
````  
