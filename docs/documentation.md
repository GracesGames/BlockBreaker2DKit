---
Layout: page
title: Documentation
permalink: /documentation/
---

# Documentation

***

### Game

__Main Menu Game Mode__

BP_MainMenuGameMode is the game mode and specifies the BP_MainMenuPlayerController as default controller. It is used as the game mode in the Main Menu map.

__Game Instance__

BP_BlockBreaker2DGameInstance is the game instance and handles the initial data (e.g. the levels for the level grid), saving and loading of the save game.

__Block Breaker 2D Game Mode__

BP_BlockBreaker2DGameMode is the game mode and handles the current level, score, and level complete actions. It is used as the game mode in the Game map.

__Save Game__

BP_BlockBreaker2DSaveGame is the save game and acts as a container for the save data (e.g. score and time per level).

### Game Objects

__Paddle__

BP_Paddle is the player of the game. It handles player input for movement in the horizontal direction.
It also handles the Ball Launch Mode: a moving arrow indicating the initial direction of the ball to launch.
And it support the firing of lasers if the player has Laser Ammo.

__Block__

BP_Block is the block object that should be destroyed by the player. 
The block has multiple properties: health, color ranged based on health percentage, explode options etc.

The blocks can be easy set up using the Block Type Enumeration in combination with the DataTable.

__Ball__

BP_Ball is the ball object that is used to destroy the blocks. The ball bounces on hit but the angles are clamped to prevent undesired (no fun) angles like horizontal balls.

__Laser__

BP_Laser is the laser object fired by the player and a secondary way to destroy the blocks

__Shield__

BP_Shield is the shield object spawned under the paddle. This is used as a safety net for the player, bouncing back a ball after which it destroys itself.

__Wall__

BP_Wall is the wall object which are just there to prevent the ball from escaping the level.

### Items

__BallsDamageUpItem__

Increases the damage of all balls currently in the level

__BallsDamageDownItem__

Decreases the damage of all balls currently in the level

__BallsSpeedupItem__

Increases the speed of all balls currently in the level

__BallsSlowdownItem__

Decreases the speed of all balls currently in the level

__PaddleGrowItem__

Increases the width of the paddle

__PaddleShrinkItem__

Decreases the width of the paddle

__SpawnExtraBallItem__

Spawns an additional ball for each ball currently in the level

__LaserAmmoItem__

Gives the paddle additional Laser Ammo

__ExtraLifeItem__

Gives the paddle an additional life

__ShieldItem__

Activates the shield, if not currently active

__BaseItem__

Parent of all items. Handles the falling of an item and the overlap with the Player and DestroyVolume

### PlayerControllers

__BP_MainMenuPlayerController__

Is responsible for creating and interacting with the Main Menu.

__BP_BlockerBreaker2DPlayerController__
 
Is responsible for creating and interacting with the HUD (HUD changes, Pause Menu and Level Overview screen).

### Widgets

All user interfaces support mobile input.   
Based on the platform the UI is automatically updated.

__HUD__

The BP_HUD is the in-game user interface and shows the player the score, lives left, blocks left, laser ammo and elapsed time for the current level.  

It also defines the level overview screen with the achieved score and time and whether the high score was beat. It also has the option to play the next level and return to the main menu.

The pause menu user interface is also integrated in the HUD and allows the player to restart the level, continue the game and return to the main menu.

__Main Menu__

BP_MainMenu is the main menu user interface and allows the player to select a level from the level select, show the controls, clear the save data and quit the game. 

__Level Select Button__

BP_LevelSelectButton is the button used in the level select grid. It defines the level to be loaded and whether the level is unlocked in the UI.