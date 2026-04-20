---
title: devlog 08
date: 2026-04-14
---
# UE5
## UI
### Updating UI
Continuing on from [[devlog 06#HUD]] I added in the program for my HUD.
Firstly I added the programming for the score updating to do this I used an event from the Blueprint Interface and connected it from my game instance where the score and high score is being calculated, every time the score is updated I activate that event with the new score and high score, turn the integers into text and set the text of each text element to the corresponding value 
![[Screenshot 2026-04-14 132047.png]]
To update the health inside my HUD I did something similar to update the score however I updated the health from the player, when the player gets damaged it triggers and event inside the player blueprint to knock it back and diminish a set amount of health, after the health calculation I added another custom event inside the widget blueprint asking for the health and max health integer which gets sent and triggered from the player blueprint after they are damaged



> [!note] previous devlog
> [[devlog 07]]

> [!tip] next devlog
> [[devlog 09]]
