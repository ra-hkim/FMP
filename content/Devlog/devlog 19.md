---
date: 2026-05-06
---
# Adobe Photoshop
## Card symbols
To make symbols for my card I decided to try with Adobe Photoshop to make my icons however I did find other methods in [[Research 12]] however I stuck to Photoshop as I have the most experience with it.

To start making icons in Photoshop I first made the canvas size `2*280x150` I got `280x150` from my card in unreal engine as it shows the resolution of each widget element however I multiplied it by two to add some headroom for in case a player has a 4k / higher resolution monitor.
Then to get started I enabled the grid with `CTRL+'` allowing me to get a reference to make straight lines and correct scaling.
![[Screenshot 2026-05-06 133459.png]]
I started by creating a sword symbol, firstly using the pen tool I made the top blade of the sword then added the handle/indent with one line and a hilt with another single line. I made the sword straight up to make it easier then I can select every pen layer and rotate them. After making the sword shape I added a colour infill to the sword I also made 3 more variations with the colours: blue, green, yellow, and red. I also added lines that surround the sword to indicate a more powerful card, and another variant with fire icons, this means from each symbol I have 4 colours and 3 variants adding up to 4\*3=12 variants for each symbol type.
Below is another symbol I made of a snow flake using the pen tool I made 3 lines rotated them and then added the spikes on the end of each line, I also duplicated all the lines and scaled them down to make an infill allowing me to have colour variations of each symbol.
![[Screenshot 2026-05-06 141346.png]]
![[Screenshot 2026-05-06 135718.png]]
I tried to make a shield symbol however I failed after a few attempts so I decided to use the internet and find a reference image for my shield I found a few that I liked and combined them together to get the image below.
![[Screenshot 2026-05-06 134947.png]]
I also made a black half section of the shield by duplicating and scaling down the shield I then cut it in half using a mask to them make the image above. By adding the half section it adds another variant to my list of lines fire and plain meaning I have 4 colours times 4 variants which is 4\*4=16.
## Exporting PSD files to PNG
To export my symbols I decided to use PNG, I could use SVG however it adds another layer of complexity to my project while giving small improvements in return (it is best practice to use SVGs but for my use-case I can get away with a normal PNG files). because I am cutting a small corner I also decided to use the quick export to PNG option inside Photoshop as it speeds up my workflow as I have quite a few images to export to files. 
![[Screenshot 2026-05-06 135736.png]]
To speed this up even more I wanted to have a key binding for "Quick export as PNG" I found a page on the Photoshop documents teaching me how to change key bindings on the Photoshop app, after following the instructions I found section to add a key binding to my desired function I chose to use `CTRL+SHIFT+Q` to bind to this function.
![[Screenshot 2026-05-06 135834.png]]

>[!note]
>The error in the screenshot seemed to disappear when I tried again 

After making many icons I curated them into one folder and then imported them into unreal engine. 
![[Screenshot 2026-05-06 140322.png]]
For now I applied the play, options, and exit icons to the main menu and will change the rest of the icons later on.
# UE5
## Death
Going back to unreal engine I worked on my death screen I started by making the screen similarly to escape menu however with a restart button instead of an resume button. To stop the game and open the death screen I added some more code into the health script that detects if the players health is less or equal to zero, if so the game will pause and open a death screen.
![[Screenshot 2026-05-06 102410.png]]
I found a bug where the death screen would appear multiple times of the player gets hit multiple times before they die to fix that I used a do once node to only open the death screen once.
To add a restart button I added another function to the blueprint interface called "Restart" this is so I can reset the values in other blueprints allowing the game to be restarted to the begining.
![[Screenshot 2026-05-06 102414.png]]
Inside the game instance blueprint I added the new interface I made previously, then to set everything back to 0 I set all the percentage values to 0 as well as clearing the array of collected cards then updating everything after.
![[Screenshot 2026-05-06 102418.png]]
I also discovered that you can collapse nodes when selecting and right clicking on them this allows me to compact nodes making the visual blueprints cleaner and easier for others to understand or navigate
![[Screenshot 2026-05-06 102658.png]]
The image below shows what the collapsed graph looks like while the image above shows the main blueprint
![[Screenshot 2026-05-08 113247.png]]
## Hurt animation
To make a hurt animation I needed change the material on the players static mesh to a dynamic material which I learnt about in [[Research 13]], to do this on event begin play I create a dynamic material and promote it to a variable.
![[Screenshot 2026-05-06 111634.png]]
Then on the damage event when the player gets hit by an enemy I added a new timeline with a vector curve this allows me to create a gradient which will player over the one second I set it to. 


> [!note] previous devlog
> [[devlog 18]]

> [!tip] next devlog
> [[devlog 20]]

