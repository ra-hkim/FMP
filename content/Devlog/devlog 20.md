---
date: 2026-05-08
---
# UE5
## Prettying up my UI
I took some time to make my UI more pretty to align with my game's art style.
![[Screenshot 2026-05-08 113243.png]]
For my HUD I added two borders with five padding around each of the horizontal boxes to match the UI style of my escape and start menu. I also added the same colours as that I used for the rest of my UI including the background colours of each box and border colours.

I also added all the images to my cards inside the database I changed the image to corresponding images instead of the test image previously, I also did this for the main menu with icons that I made specifically for the main menu.
![[Screenshot 2026-05-08 101629.png]]
I also added a description to each card of the menu with a brief overview of each option for example the "Start" button description on how to play the game.
## Dash bar
The bottom right corner of my HUD lacked anything so I wanted to fill the box I made in [[devlog 06]] I first searched up how to make a timer in [[Research 14]]. To start with this I added a progress bar on my HUD widget blueprint and prettied it up to match my revamped UI from earlier. 
![[Screenshot 2026-05-08 134809.png]]
to make the initial part of the timer I used a function that takes the cool-down value and negates 0.03 every time the event is triggered, then inside the main blueprint I used a set timer by function name node with the same time as the cool-down function, alongside enabling looping I added a delay then to stop the timer after the dash cool-down was over.
![[Screenshot 2026-05-08 134805.png]]
Now every time a dash is triggered from the player it sends the cool-down value to the widget and adds it into a local variable where it then takes of 0.03 every 0.03 seconds this then updates the progress bar on the widget which gets the new value from the calculation and divides it by the initial cool-down value to get a percentage.
![[Screenshot 2026-05-08 134131.png]]
To trigger the dash cool-down bar I cast to the widget blueprint and then trigger the custom event inside the widget alongside sending the cool-down number alongside it. The image above is a broken version of this code as the delay is before the cast event which causes the timer to start when the cool-down is over, after testing I realised and fixed it by moving the "Delay" node to after the "Dash" node.
## Cleanup
I continued to cleanup my game's files even more I removed some leftover assets from the twinsticks template that I am not longer using alongside some extras.
![[Screenshot 2026-05-08 114325.png]]
I also bulk renamed the images to fit a more ideal naming scheme for unreal engine I added "TX_" as a prefix and replaced the dashes with underscores, maintaining a file naming scheme is good practice for any game and in any engine not just unreal.



> [!note] previous devlog
> [[devlog 19]]

> [!tip] next devlog
> [[TODO list]]

