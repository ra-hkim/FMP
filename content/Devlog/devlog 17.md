---
date: 2026-05-01
---
# UE5
## New character model
After using the default character model I finally made a new one inside blender, the idea for my characters was a cube as the player and spheres as enemies that attempt to attack each-other, to make my player character I opened blender, inserted a cube and simply bevelled the edges and added a colour material.
![[Screenshot 2026-05-01 110928.png]]
Back in unreal engine I added a static mesh component to my character blueprint and disabled the skeletal mesh. After setting the cube that I imported from blender however I ran into another issue after adding my character as a static mesh, when I pressed play enemies would stop navigating to the player I pressed "P" to enable the nav mesh overlay (which i learnt in [[Research 10]]). From this overlay I discovered the issue that the navigation mesh was being blocked by the static mesh of the player, I instantly knew what was happening from [[devlog 14]] I had the same issue but the other way around I knew that I needed to change the collision from "blockAll" to another preset, I picked the "character" collision preset which fixed the issue.

I also added the same material that my character is using to the enemy mesh to remove the default grid texture, and I moved the static mesh up to stop it from clipping into the ground.
## Enemy Health
I wanted to add enemy health bar into the 3D space of my game, the first task is to research how to do this which I carried out in [[research 11]]. 
![[Screenshot 2026-05-01 115806.png]]
To make the health bar I first started by making a new widget blueprint with a size box and a progress bar after changing the colours I linked the progress value to a function with the programming above to make turn the health and max health into a percentage.
However I noticed immediately that I did the calculation wrong as I divided the integers instead of converting them into floats which would prevent them from having decimal points I also remembered that I do not need to multiply by 100 as percentages are values from 0.00 to 1.00.
![[Screenshot 2026-05-01 121911.png]]
After fixing that simple issue I then added widget blueprint into the character blueprint of the enemy and moved it to float above the enemy. Then inside my enemy blueprint I added two more additions to the blueprint; the first addition was to set the max health by taking the current health when the actor spawns into the level alongside setting the current health to the max health, then whenever the enemy gets hit by the player it updates the widget above with the exact same code of casting to the widget and setting the health.
![[Screenshot 2026-05-05 092120.png]]
![[Screenshot 2026-05-05 092052.png]]
Another issue that I came across was that the health bar is in a fixed position and would face the same way as the enemy instead of facing towards the camera (this inst technically an issue however it is an inconvenience for player that can be fixed)
![[Screenshot 2026-05-01 114937.png]]
To fix this I asked ChatGPT in [[Research 11]] on solutions and found one that fits my use case I followed 
```
→ Get Widget World Location  
→ Get Player Camera Location  
→ Find Look At Rotation  
→ Set World Rotation (Widget Component)
```
then I put this on event tick to update the position every tick meaning the health bar would move and face towards the players camera instead of following the enemy's movement direction. The image above shows a failed attempt by using an rterp to node instead which did not work as you can see below instead the health bar would glitch out of view depending on where the player is. 
![[Screenshot 2026-05-01 115206.png]]


> [!note] previous devlog
> [[devlog 16]]

> [!tip] next devlog
> [[devlog 18]]

