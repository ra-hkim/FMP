Tuesday 17th march 2026
# UE5

## Databases
This game will be using a card selector mechanic and will have a set of cards for the player to pick from to which can give buffs or de-buffs to either the enemies or player. To create this I will be using databases allowing me to store information about every card and their effects and visual information.

Before creating this system I will have to learn more about data bases and data tables in unreal engine, how to create one and interact with them in blueprints and in the editor, I used website like YouTube and ChatGPT to get a good understanding of them and logged everything in [[Research 01]]

First I will have to create a structure for the database by creating a structure blueprint and adding several values including an image, colours, and floats for each effect the cards have.
I also set some default values the main one being a background and border colour so the card inst transparent during testing
>![[Pasted image 20260317135944.png]]

After making this I made a data table and created a few rows for testing.
I also need another data table for my cards as I will be using rich text to dynamically display all the different effect the cards will give as well as adding colours to the text and a +/- indicator, to make rich text I will need a rich text data table this stores brushes and assigns names to them 

> [!note] previous devlog
> [[devlog 01]]

> [!tip] next devlog
> [[devlog 03]]

