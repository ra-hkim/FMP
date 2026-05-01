---
title: devlog 6
date: 2026-03-25
---
# UE5
## cards/data setting
In [[devlog 05]] I made the calculations for the cards system however to apply the data to the main character or enemies, I will have create a script in the blueprints of the character and enemies to pull the data from the game instance,
to do this I will use a get game instance and cast to game instance to get the a reference to the game instance, this allows me to pull variables from the game instance blueprint, for the main player I pulled the variables shown in the image below alongside this there are some calculations for the health system this is to make sure that the player cant heal above the maximum health.

Outside the player blueprint the enemies and projectile will also need to pull data from the game instance, by creating a similar structure to the image below but with different variables instead, however instead of using a custom event that is triggered whenever the cards update both the enemies and projectile will only update when they are spawned into the level, this helps performance as enemies and projectiles wont get constantly updated, as well as making the game feel a bit better as enemies that are attacking the player wont all of a sudden become more powerful 
![[Screenshot 2026-03-25 105830.png]]

## Health
Health is another thing on the [[TODO list]], so this is when I will be implementing player and enemy health alongside the damage system that was partially implemented while making the data setting.

Firstly there are two main variables to create for the player; max health and current health, the max health is a cap so that the players health dose not keep increasing which can break the game very fast. Alongside this the enemies will only have a health variable as they cannot heal once their health hits 0 they will be killed, removed from the level, and increase the players score.
Damage works in a very different way by using the projectile hit event (which is a custom global event that triggers on every blueprint) I added a new variable to the event as an integer called damage this allows me to damage both the player and enemies in one action, inside both the enemy and player blueprint on the event that they get hit the damages is subtracted from the current health, eventualy when either the player or enemy's health goes below 0 they will die and trigger the death functionality 
![[Pasted image 20260325143110.png]]
## UI
I started to work on my UI a bit more as I was getting a bit tired of coding this day, so I started to work on my UI. Moving away from gameplay I decided to make make my main menu as well animating a bit of it, 
### Main Menu
The main menu is an essential part of any game meaning that it is something that I will have to make, to create a main menu there are several files that need to be created, the first one being a new level where the menu will spawn and will be used to redirect the player to the main game options menu or exit, the next component is the widget blueprint for the main menu, which will spawn when the game starts containing 3 options allowing the player to play, exit, and configure options of the game.
the main menus design is unique compared to other menus instead of a list with options I instead used 3 cards with the options of; start, option, and exit, this matches the in game card picker which creates a cool and unique design compared to most games.
#### Animation
I also animated the cards on the main menu when the game starts and the menu spawns in the cards will move up from the bottom of the screen as a bundle and will spit apart into their respective positions I created this animation using the built in animation tool in unreal engine alongside the graph editor to add fine adjustments to make the animations look better and more smooth.
![[Pasted image 20260325142907.png]]
### HUD
I also worked on my in game HUD a little bit I started to create the UI but not the functionality, below is the widget designer of my HUD for now I am just created the base of it adding the health, high score, score, and cards.
![[Screenshot 2026-04-19 114704.png]]
To make this hud shows above I first added a canvas panel which gives a canvas where I can place UI elements, then I added 4 vertical boxes and anchored them to each corner of the screen with a 100 margin. After created the 4 boxes I then added horizontal boxes this allows me to have multiple elements in a row, as an example for my health status I have a text box with "Health" and a size box with another text box inside it, this size box allows the parent boxes to scale properly when the health values change which will stop visual bugs and glitches.

After making the UI I added a script to create the HUD and add it to the view-port when the game starts.


> [!note] previous devlog
> [[devlog 05]]

> [!tip] next devlog
> [[devlog 07]]
