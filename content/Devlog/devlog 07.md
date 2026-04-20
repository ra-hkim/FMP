---
title: devlog 07
date: 2026-03-27
---
# UE5
## debugging
There were several issues with my game that I came across while play testing it I took a note of them in my head while testing my game, so today I decided to fix all of these issues with my game.
### Data setting
the first issue I came across was that the cards were not setting data correctly because of this some effects of cards were not applying at all, to fix this issue I first made this print script that prints the values of every effect and give them a name. To make this script I converted the output of the set variables to strings and then combined them together with an append node alongside a name to stop me from getting confused,
![[Pasted image 20260327110157.png]]
### AI detection
I wanted to make the AI activate when the player gets into a specific range of the enemy however I don't want the player to see the enemies not moving, to fix this issue with my game I went to the enemy character blueprint and enabled show in game for the sphere collision actor.
![[Pasted image 20260327103527.png]]
To figure this out I researched how to fix this issue in [[Research 05]]
### Data setting
going back to [[devlog 07#Data setting]] I also found another issue when setting data some values would not set properly as they would update too fast, to fix this I added a delay between the percentage calculations and the main calculation for each value, you can see below a screenshot of the delay node where I found that a 0.2 second delay works very well and fixes this issue entirety  
![[Pasted image 20260327110600.png]]


> [!note] previous devlog
> [[devlog 06]]

> [!tip] next devlog
> [[devlog 08]]
