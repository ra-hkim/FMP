---
title: devlog 11
date: 2026-04-20
---
# UE5
## User Interface
Today I made some more of my games user interface including the pause menu and some of the options menu
### Pause menu
Continuing on with making my games user interface I decided to change up my pause menu from [[devlog 10]], I felt that the card style pause menu was took up too much of the screen which will defiantly cause overlap when I add in the options menu for my game.
![[Pasted image 20260420094316.png]]
To make this UI instead of the previous menu I made in [[devlog 10]] I started with the blur background, a rich text box and a vertical box on the left of the screen. (I also locked the blur background to stop me from adding items as children of the blur) Inside the Vertical box I added a button set the padding to 10 and fill the box, I then added two borders and another rich text box for the text, After making one button I then duplicated it 3 more times and filled in the colours and text to each button. I also renamed the buttons to make it easier to program them later.

Next I also wanted to animate the buttons, giving them some life and making the game more visually appealing. To animate the buttons I firstly made an animation for each button where they move 32px right over 0.25 seconds, by using the key-frame button and the render transform feature that every element has I was able to animate each button to move move whenever the mouse hovers over it.
### Game stats
In my escape menu I also wanted to have a stat page that shows the total players status, to make this I have to firstly make a UI element with a rich text box, following my UI theme I added two borders with a 5 margin which and coloured blue (note: the image below dose not have the correct colour)
![[Pasted image 20260420111627.png]]
To program the box above I had to pull the data from the game instance to do this I cast to the game instance and get all the values, from this I turn the floats into strings and use an append note to make each line of text below, from each value I combine them together with another append string note and then set the rich text box's text to the string.
```json
<black>Attack Damage: 00000000</>
<black>Attack Velocety: 00000000</>
<black>Dash Cooldown: 00000000</>
<black>Attack Health: 00000000</>
<black>Max Health: 00000000</>
<black>Walkspeed: 00000000</>
<black>Enemy Attack Damage: 00000000</>
<black>Enemy Health: 00000000</>
<black>Enemy Spawn Rate: 00000000</>
<black>Enemy Walkspeed: 00000000</>
```
This code block shows what the append strings make it adds `<black>` which determinants the colour and font of the text depending on the data table, It also adds the name for example `Attack Damage:` ,the number, and the closer for the rich text formatting `</>`

## Card data base
I also spent some time adding more cards to my game as well as adding colours to the background, border, and text, I changed a lot more values around for example I changed all the attack amount values to 0 and had only a few +1 cards as it turns out to be very powerful if the number is too high
![[Pasted image 20260420094339.png]]
Later on I will be making preview images for each card containing a symbol that represents what It changes

## Options menu
firstly I researched about how options menus are made I ended up following a video in [[Research 06]], after going through the video I learnt how to make an options menu. Firstly I made the child widget that I mentioned in the research and video, below is the programming for the widget.
![[Pasted image 20260420162916.png]]
To make this widget I followed the video by creating a next and back button alongside some text. After making the UI I then added some event that set the current option depending on if the player presses the back or next button, this also sets the text to the corresponding option with another custom event. 
Another important feature too add is to disable the button when at the maximum option allowable, to do this I link the activated option in the details of each button to a function and then get the current option and the length of the array, so when the current option is less than the length the button stays enabled but when it is at the maximum it is disabled.


> [!note] previous devlog
> [[devlog 10]]

> [!tip] next devlog
> [[devlog 12]]
