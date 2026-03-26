
# UE5
## databases
Databases is something entirely new to me so it is something that I had to research myself as my class has never covered it nor do I have any experience with using databases. 
I first asked chatGPT to give me an idea of how they work in UE5, I learnt that you can use either SQL or their built in data table system. SQL is a very powerful data base system and is typically uses anywhere from financial institutions to video games, however it is very complicated so I decided to go with UE5s data table and structure blueprint system.

After getting a basic idea about Data tables and how they work I wanted to find a visual guide with pictures to get a strong understanding on how they work,
![How to Use Data Tables in Unreal Engine 5](https://www.youtube.com/watch?v=aZdztLTG3OQ)
From this video I was able to understand how Data tables work and how to create and interact with them, Data tables work of structures with are another asset outside the table file, a Data table simply allows you to have multiple rows of that structure in a large table making it easy to have hundreds or thousands of unique values in one file, they can also be interacted inside blueprints with several different commands, for my use case I will be getting an array of every row name and picking a random row from it, after I can get the row from the table and use the break structure node to get the individual variables 
## Structs
The video above also linked to another video above with covers structures in unreal engine, from what I learnt from ChatGPT I will also need to lean and understand how Strucs work in order to use and interact with data tables.
![How to Use Structs (Structures) in Unreal Engine 5](https://www.youtube.com/watch?v=koz7J1fBNis)
From this video I learnt how structures work in UE5, You start by creating a structure file this allows you to create a custom structure that can store any variable from images to floats, from this in the blueprint editor of any blueprint you can now use structures, starting with a variable and assigning the custom structure you made you can break from it allowing the blueprint to pull the individual variables set inside the structure file, to set data in the structure file with a variable you can use the set members command allowing the blueprint to change each value inside the structure. 