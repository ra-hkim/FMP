---
date: 2026-04-28
---
# UE5
## Mini cards
I wanted to add mini cards to my in game HUD to show the player their most recently collected cards allowing them to get a preview of them.
![[Screenshot 2026-04-28 143047.png]]
To make these mini cards I started by creating a new widget blueprint with a size box so set a fixed scale for each card, then inside a 2 borders for the background and border colour, I also added an image wrapped with another border to look like the full size cards. Then back in the HUD widget I added several cards to the top right and made sure they were variables and in the correct number order from right to left. Inside the widget blueprint I pulled every card and turned it into an array by using a for each loop I can easily assign a number to each card by negating the array index from the total length of the currently obtained cards, and then by using a custom event I sent that number to the mini card using a custom event.

Inside the mini card I simply pull the current cards from the game instance again and select the card from the row number given by the prior blueprint, after breaking the structure the blueprint applies the background, border colour, and image to the mini card. (I also set the colours of every mini card to transparent so blank cards do not show up in game)
## Cards
I came across an issue with my main cards, which is the title text would take the default colour instead of the selected colour by the card, to fix this I added an append node with the correct rich text syntax to apply a colour to the title text.
![[Screenshot 2026-04-28 132515.png]]
The image above shows the code to change the title text colour however I changed this slightly, I added a new row before the colour with "subtitle_" and added the matching rows to the data table, this allowed me to have a separate rich text from the card text allowing me to change the scale to make a subtitle.


> [!note] previous devlog
> [[devlog 14]]

> [!tip] next devlog
> [[devlog 16]]

