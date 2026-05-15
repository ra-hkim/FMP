---
title: devlog 12
date: 2026-04-22
---
# UE5
## Options Menu
Continuing on with [[devlog 11]] I continued on to make the options menu, making the actual UI for the options menu is very important, below is an image of my game options menu
![[Screenshot 2026-04-20 114502.png]]
To make this menu I first started with the left panel I first started by copying the escape menu with the background blur, title, and buttons. I then changed the text to "game-play options" as well as the buttons text to the corresponding pages that I will make later on, I also changed the colours of the buttons to fit the text better.

After adding in the UI to the game I found another issue with the selector I made, when i pressed the next button it would not disable itself which means the player could break the game by setting the settings above the limit.
![[Screenshot 2026-04-22 111416.png]]
To fix this issue I first added a print string to the output of each value I found out that the length is actually 4 instead of 3 which I was assuming because arrays start at 0, while the current option starts at 0 it means that the current option's max is 3 but the length of the string was 4 so it would end up not disabling the button. After figuring out the issue I instead used an equals node and subtracted 1 from the length to make a max number, this means that if the current option equals the max in this case 3 it will output true however if I plug this into the return value it will enable it when it is not at the max value so I invert it using a not boolean node.

Now to make the functionality for each option picker, which is something that I thought would be significantly more complex than it is in reality.
![[Screenshot 2026-04-22 141050.png]]
To add the functionality to the graphics options I simply use a get game settings node and then set the option to the integer value. which then changes the graphics settings from low to high and etc, however to apply the setting I need to use the apply settings node there is two ways I could have gone around this: the first way applying the settings every time an option is changed or using a button to apply settings that the player has to manually activate which is what I did.


> [!note] previous devlog
> [[devlog 11]]

> [!tip] next devlog
> [[devlog 13]]

