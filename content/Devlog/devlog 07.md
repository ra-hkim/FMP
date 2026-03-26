Wednesday 25th march 2026

# UE5
## cards/data setting
In [[devlog 06]] I made the calculations for the cards system however to apply the data to the main character or enemies, I will have create a script in the blueprints of the character and enemies to pull the data from the game instance,
to do this I will use a get game instance and cast to game instance to get the a reference to the game instance, this allows me to pull variables from the game instance blueprint, for the main player I pulled the variables shown in the image below alongside this there are some calculations for the health system this is to make sure that the player cant heal above the maximum health.

Outside the player blueprint the enemies and projectile will also need to pull data from the game instance, by creating a similar structure to the image below but with different variables instead, however instead of using a custom event that is triggered whenever the cards update both the enemies and projectile will only update when they are spawned into the level, this helps performance as enemies and projectiles wont get constantly updated, as well as making the game feel a bit better as enemies that are attacking the player wont all of a sudden become more powerful 
>![[Screenshot 2026-03-25 105830.png]]

## Health
Health is another thing on the [[TODO list]], so this is when I will be implementing player and enemy health alongside the damage system that was partially implemented while making the data setting.

Firstly there are two main variables to create for the player; max health and current health, the max health is a cap so that the players health dose not keep increasing which can break the game very fast. Alongside this the enemies will only have a health variable as they cannot heal once their health hits 0 they will be killed, removed from the level, and increase the players score.
Damage works in a very different way by using the projectile hit event (which is a custom global event that triggers on every blueprint) I added a new variable to the event as an integer called damage this allows me to damage both the player and enemies in one action, inside both the enemy and player blueprint on the event that they get hit the damages is subtracted from the current health, eventualy when either the player or enemy's health goes below 0 they will die and trigger the death functionality 
>![[Pasted image 20260325143110.png]]
## UI
### Main Menu
The main menu is an essential part of any game meaning that it is something that I will have to make, to create a main menu there are several files that need to be created, the first one being a new level where the menu will spawn and will be used to redirect the player to the main game options menu or exit, the next component is the widget blueprint for the main menu, which will spawn when the game starts containing 3 options allowing the player to play, exit, and configure options of the game.
the main menus design is unique compared to other menus instead of a list with options I instead used 3 cards with the options of; start, option, and exit, this matches the in game card picker which creates a cool and unique design compared to most games.
#### Animation
I also animated the cards on the main menu when the game starts and the menu spawns in the cards will move up from the bottom of the screen as a bundle and will spit apart into their respective positions I created this animation using the built in animation tool in unreal engine alongside the graph editor to add fine adjustments to make the animations look better and more smooth.
>![[Pasted image 20260325142907.png]]



> [!note] previous devlog
> [[devlog 06]]

> [!tip] next devlog
> [[devlog 08]]
