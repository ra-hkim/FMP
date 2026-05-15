---
date: 2026-04-24
---
# UE5
## Options menu
continuing on from [[devlog 12]] I kept working on the options menu, this is where I introduced  difficulty scaling options this allows the player to change the games difficulty making it harder or easier for the player.
![[Screenshot 2026-04-24 112413.png]]
The code snipet above shows the the master gameplay changer allowing the player to change the every gameplay setting with one button making it easier to pick a set difficulty, to do this it has to trigger a function to change every setting which I made later on.
I also added a few more rows of pickers to add more difficulty options that the player can change these include:
- card scaling
- enemy scaling
- score scaling

Now to make the function for the master changer above I need to input the selected option from the master and then relay them into several select nodes that pick the correct scaling difficulty, after it will set the correct difficulties.
![[Screenshot 2026-04-24 112418.png]]
However the image shows a branch to two different functions I had to add another section to this function called "reset", this addition simply pulles the current options and adds them to the widget blueprint so that the selected option shows up when the player either opens the screen or changes the master option. (this also prevents the text from showing the default text box when opening the options widget)

Now the final part of this feature to add is the multiplier inside each system so that the difficulty settings actually change the difficulty
![[Screenshot 2026-04-24 113941.png]]
The image above shows how the multiplier for the score scaling, to make this I used a select that picks the multiplier and then multiply the score, for the score multiplier I need to turn it into a float and truncate the number to multiply it properly. 

> [!note] previous devlog
> [[devlog 12]]

> [!tip] next devlog
> [[devlog 14]]

