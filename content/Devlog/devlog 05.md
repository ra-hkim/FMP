---
title: devlog 5
date: 2026-03-24
---

# UE5

## AI
I was having performance issues with AI in my game as the AI would be active and would attempt to move towards the player even after I disabled it, to fix this I changed from disabling the character movement of the NPCs to instead stooping the state tree from being called automatically and manually calling it when the enemies get into the set range 
![[Pasted image 20260323114654.png]]
>I asked chatGPT to help with this issue and it suggested a fix that worked well

## cards
I also continued to work on the cards system on my game, today i finished the data setting system that I started in [[devlog 04]], the way this system works is quite simple it stores every value inside the game instance where the player enemies and other blueprints can pull data from allowing them to dynamically change things like walk speed or damage.

Continuing on from the previous develog I changed the maths logic to instead add percentages instead of multiplying them by each-other I started by created more variables which start with P (meaning percentage) for each effect from the cards, these variables store the total percentage change it dose this by getting its current value (with the default being 0) and adding the values from the newly obtained card, it also checks if that value is not 0 to prevent issues.

After creating the total percentage the next step is to move form the P variables to the main variables first I have to grab the P variables and divide them by 100 turning them into a percentage instead of a normal number after I add 1 so that it increases (for example +14 will equal 1.14 and If you don not add 1 it will equal 0.14 causing it to decrease instead of increasing) then I multiply it by the default value, however some of the values will be divided instead as a value like attack speed is a cool down between each shot so to increase the speed the cool down must go down
![[Pasted image 20260325105754.png|676]]



> [!note] previous devlog
> [[devlog 04]]

> [!tip] next devlog
> [[devlog 06]]

