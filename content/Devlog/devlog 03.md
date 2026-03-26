Wednesday 18th march 2026

# UE5

## cards
Cards are the main mechanic in this game so this is when I made them, first I made a rough design to create all the parameters allowing me to change everything visually and functionality, I can change the colours image and text as well as what the card dose in the blueprint.
Later on I also warped a button around the B_Border which allows the player to click the card and add it to the collected cards.
>![[Pasted image 20260318114035.png]]
>above shows the rough design for my cards 

Programming the visuals aspect of the cards is quite simple as I need to grab a random row from my database and then apply all the parameters from it to my card, the database contains the name, image, border and background colour, and the data for its effects.
To pull the data I get the list of rows as an array and pick a random one from the array then I grab that row and break the structure into separate values, after this I can apply each parameter to the card. Description text is more complicated however, as I have the effect values I have to dynamically generate text for each positive and negative effect the card give, however it is not too difficulty to do this I simply check if the value is not 0 then add it to the cards description alongside adding colour, a +/- depending on the number and what the effect name is. 






> [!note] previous devlog
> [[devlog 03]]

> [!tip] next devlog
> [[devlog 04]]
