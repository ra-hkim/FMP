---
title: Research 06
date: 2026-04-20
---
# UE5
## UI
When making my options menu for my game I found this tutorial online which helped me make my options menu allowing the player to change settings like graphics or volume
![https://youtu.be/bLJNuzp2dpI](https://youtu.be/bLJNuzp2dpI)
From this video I learnt several new things about UE5s widget blueprint system. One example is the pages this allows me to create pages in my UI so I can have a section for graphics settings or volume settings, to do this I add a page and and add a canvas box as a child each canvas box acts as a different page where I can add different menus in each box, to switch between each page I can use a change page node triggered by a button for my use case changing the page to an integer that relates to each canvas box.

Another thing that I learnt from this video is how child blueprints work, you can see in the preview image of the video above a picker allowing the player to change the setting from low to high and etc using buttons, to do this I have to make a child blueprint where I add a box with the two buttons and a text to show the currently selected option after using some logic in the blueprint using an integer to determinate the number value and an string array to display text relating to the integer value  

### Fonts
https://www.dafont.com/coolvetica.font?text=Score%3A+%2B0000
![[Screenshot 2026-04-28 131817.png]]
When it comes to looking for fonts to use for my game and general UI design I found a website called dafont which contains an enormous library of fonts that can be used for anything. After scrolling though the website I found a font that I liked called "TT Modoronoir", however when I imported it into unreal engine and changed my rich text to use it instead of google sans which I previously installed, I found that I did not like the font as the spacing between each character was too small it ended up removing the retro feel of the game.
![[Screenshot 2026-04-28 130739.png]]
So I kept looking thorugh the dafont website and fount another font that i liked called "Coolvetica" I also imported it into unreal engine and set my rich text to this I found that I liked it a lot better after playing with the variations I picked "RG cond"

![[Screenshot 2026-04-28 140112.png]]