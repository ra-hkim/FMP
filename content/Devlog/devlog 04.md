---
title: Devlog 04
date: 2026-03-23
---
# UE5
## cards
continuing on from [[devlog 03]] making the cards system actually apply data to the game, to do this I used a game instance to store all the card data by creating an array variable of the cards structure (which allows me to store multiple values in one variable) then by getting the game instance and casting to the game instance I can get the array from the game instance then add the card selected by the player which will add the new card to the array allowing every card that has been picked to be stored and recalled for later use.
![[Pasted image 20260323125135.png]]
> the image above shows when the desired card is selected the blueprint casts to the game instance and adds the card to an array variable as well as triggering an event to update the values and sending the index number of the card that was selected, allowing that specific card to be added onto the stack of cards 

now to add the cards together and set it to the enemies and player I created a script inside the game instance which will update all the values whenever a card gets updated by created a custom event, in the custom event it takes the current number and multiplies it by the percentage
![[Pasted image 20260323105840.png]]
> above is an screenshot of the game instance blueprint which compiles all the selected cards and applies it to the player (walk speed is currently only functional) 
#### balancing
however multiplying the percentage causes the stacking to go very high after a few cards the walk-speed went from 600 to 30,000 so instead I decided to change the system to have another variable which stores the total amount of percentage that the cards have accumulated which then it multiplies that percentage by 600 to increase the speed at a slower and more reasonable rate, I continued this plan on [[devlog 05]]

# Adobe Photoshop
I also creates some test assets to test the size for the images on cards, I landed on 280x150 as the resolution for my images as it creates a similar look to Pokémon cards or other trading cards.
![[Pasted image 20260323131647.png]]
> creating some test images for cards in adobe photoshop

## [[Research 02]]


> [!note] previous devlog
> [[devlog 03]]

> [!tip] next devlog
> [[devlog 05]]