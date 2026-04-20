---
title: devlog 10
date: 2026-04-17
---
# UE5
## User Interface
Today I started making some more UI for my game 
### Escape menu
I started to make my pause menu for my game initially I got the idea to recreate the main menu with the 3 cards the player can select from however I added a background blur to remove distractions from the game, as well as pausing the game when the menu is open
![[Screenshot 2026-04-17 093342 1.png]]
To make this pause menu I created a new blueprint interface to recreate my main menu in, however I realised after making this I could just duplicate my main menu and turn it into my escape menu. Instead I duplicated my main menu of the game and changed some things around, firstly I added a blur in the background to remove distractions and allow the player to focus on the main user interface, after this I changed the text values of the title above and the cards below to fit the escape menu, I changed "pick a card" to "game paused" and "start" to "resume"

After designing the UI I then added the programming for now because I dont have an options menu I did not have any script attached to that button, however for the rest I added an quit game node to the exit button and a set paused game to false and remove the widget from parent nodes to the resume button.

After making my escape menu functional I then had to bind a key to open the menu I started by adding a new input action for and binding it to the "ESCAPE" key after this inside the player blueprint I added an event triggered by the input action that then adds the escape menu to the view-port.
![[Screenshot 2026-04-15 134223 1.png]]
However I came across an issue with unreal engine, the game would exit instead of opening the escape menu however this was not a bug but a feature of unreal engine as pressing "ESCAPE" causes the simulation to exit this allows for quicker testing however to test my escape menu this dose not help at all. To fix this issue I simply went into the editor preferences tab on the top options bar and looked for the stop keybinding, for me I decided to change it to "SHIFT + ESCAPE" so that I can still use the function if i come across any more issues
### Card picker
In [[devlog 09]] I worked on my cards a bit more however I missed an issue that I did not realise until now, the issue was that my text colour was not changing even though I set different values inside the data table.
![[Screenshot 2026-04-17 120652 1.png]]
To fix this issue I went into the card widget blueprint this is because I am using rich text to set the text colour instead of a brush or liner colour 


> [!note] previous devlog
> [[devlog 09]]

> [!tip] next devlog
> [[devlog 11]]
