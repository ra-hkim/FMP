# UE5

Linking back to [[devlog 05]] I will need to store the data in a separate file allowing me to pull the data and set the data in the enemies and player, to do this I looked online for ways to do this.
## Data Assets
I first had a look at data assets I learnt about them from this YouTube video I found online however they were not suitable for my use case, I learnt that data assets are not actually used to store data like what I intended to do and are more useful elsewhere.
 ![yt](https://www.youtube.com/watch?v=3PrpLvC5EO8&t=67s)
 I learnt that data assets are better used for things like inventories as they make creating items and storing the functionality easy, this is great for having hundreds of unique items with very different functionalities each, however from this video I learnt that the different assets are stored inside the game instance, which the Youtuber used to create an inventory system, this led me to game instances which is what I needed not data assets. 
## Game Instance
From the previous research, [[#Data Assets]] taught me about game instances, this Is what I actually need for my game to store a list of collected cards, I started by asking ChatGPT with help on how to store data from my cards, ChatGPT also told me that Game instances is the way to go and gave me a basic idea on how they work and what to do.
![[Pasted image 20260318114023.png]]

I found this YouTube video by Gorka Games which goes over how to use a game instance for a character selection system,
![How to Create a Game Instance in Unreal Engine 5](https://youtu.be/sWh1jgHb6Tw)
From this video I learnt how to create a game instance which is done inside the project setting menu and not the world settings, after creating a game instance I can create several values inside it, for my use case I will have an array of my structure that I learnt about in [[Research 01#Structs]] and made in [[devlog 02#Databases]], I will also split the structure into each variable so they can be pulled from blueprints allowing the cards to function and change the players and enemies