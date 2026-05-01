---
title: devlog 9
date: 2026-04-15
---
# UE5
## More debugging
I spend some more time today finding issues with my game and fixing them with one of the main issues with my enemy stats not setting
### Enemy stats
I also found another issue with the enemy stats not setting properly so firstly I set up another debug script for my enemy stats, below is an append string node that combines each enemy value with a note to that represent each value.
![[Pasted image 20260415095618.png]]

I made a few changes to the default values of the enemies to make them less powerful and easier to kill at the start of the game. Below I changed the default health to 15 this makes them more weak and easier to kill.
![[Pasted image 20260415095630.png]]

### Dash cooldown
Another issue I found is that I did not add a dash cool-down into the game inside the dash script I added a delay node alongside a new custom event that is plugged into a do once node, this adds a cool-down to the dash meaning when the delay is over then the player can dash again.
![[Pasted image 20260415111520.png]]

### Card Database
Once again I added more cards to my data table, below is a new card called "tank" this card makes the player significantly slower but in return they gain more health and damage however the enemies also get a buff of being faster and stronger. 
![[Pasted image 20260415111532.png]]
### Card animation
I also added a scale animation to the card, this indicates that the player is hovering over this card. It can also act as accessibility as the card becomes larger making it easier for the player to read text or the see image. 
![[Pasted image 20260415131829.png]]
To make this animation I made a new animation and used the render transform options to scale the card up, at 0 seconds I added a key-frame with the default values then at 0.30 seconds I changed the transform to 1.3 scale and added another key-frame.
I also recreated this same effect in my main menu as it also has a card picker to start the game or quit and etc.

However the animation wont work automatically I have to trigger the animations using blueprint, however this is quite easy, the button underneath each card has a hover and unhover event that I can just plug into a play animation forward / reverse into the respective event.
![[Pasted image 20260415131859.png]]
Now I have an animated UI which makes the game feel more polished however makes a very big difference in the user experience. 


> [!note] previous devlog
> [[devlog 08]]

> [!tip] next devlog
> [[devlog 10]]
