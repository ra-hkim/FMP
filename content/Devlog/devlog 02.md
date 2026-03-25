Tuesday 17th march 2026
# UE5

## Databases
This game uses a cards mechanic and will have a set of cards for the player to pick from to create this I will be using databases allowing me to store information about every card and their effects and visual information.
First I will have to create a structure for the database by creating a structure blueprint and adding several values including an image, colours, and floats for each effect the cards have.
I also set some default values the main one being a background and border colour so the card inst transparent during testing
>![[Pasted image 20260317135944.png]]

After making this I made a data table and created a few rows for testing.
I also need another data table for my cards as I will be using rich text to dynamically display all the different effect the cards will give as well as adding colours to the text and a +/- indicator, to make rich text I will need a rich text data table this stores brushes and assigns names to them 

> [!note] previous devlog
> [[devlog 01]]

> [!tip] next devlog
> [[devlog 03]]

