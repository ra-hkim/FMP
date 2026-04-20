---
title: Research 6
date: 2026-04-20
---
# UE5
## UI
When making my options menu for my game I found this tutorial online which helped me make my options menu allowing the player to change settings like graphics or volume
![https://youtu.be/bLJNuzp2dpI](https://youtu.be/bLJNuzp2dpI)
From this video I learnt several new things about UE5s widget blueprint system. One example is the pages this allows me to create pages in my UI so I can have a section for graphics settings or volume settings, to do this I add a page and and add a canvas box as a child each canvas box acts as a different page where I can add different menus in each box, to switch between each page I can use a change page node triggered by a button for my use case changing the page to an integer that relates to each canvas box.

Another thing that I learnt from this video is how child blueprints work, you can see in the preview image of the video above a picker allowing the player to change the setting from low to high and etc using buttons, to do this I have to make a child blueprint where I add a box with the two buttons and a text to show the currently selected option after using some logic in the blueprint using an integer to determinate the number value and an string array to display text relating to the integer value  