---
title: Research 3
date: 2026-03-26
---
# UE5
## AI
I had some issues with the performance of my AI this was because the AI was still activated even though my player was not in the range of the AI detection because of this the AI was path-finding to the player and putting unnecessary stress on the CPU to fix this I found that it was quite easy I asked ChatGPT for assistance with this issue
![[Screenshot 2026-03-23 113603.png]]
From ChatGPT I found that Instead of disabling the movement I should instead disable the state tree from the start this means that nothing  will happen when the enemy spawns into the game after this I then can add a custom even which gets triggered when the player enters the collision sphere, once the custom even is triggered the state tree is activated causing the AI to move towards the player.