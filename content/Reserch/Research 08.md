---
date: 2026-04-28
---

# UE5
## Shaders

Adding shaders to my game was part of my [[TODO list]] I wanted to add cel shading to my game to change and improve the looks as it matches my art style.
![https://www.youtube.com/watch?v=HDyswSWIdY0](https://www.youtube.com/watch?v=HDyswSWIdY0)
This video is quite long at fifty minutes however it goes into detail on how to make cel shading in unreal engine using a material function. The video starts by showing off the shaders which allowed me to get a look before committing to that shader, however the shader has many customisation options as well as the fact i can edit the material function myself so in the end it is not the biggest deal. After going through the video I gained an understanding on how this shader works, one key point is that it uses material functions instead of a post processes which can have both pros and cons however it means that each object can be changed and customised instead of one fixed global shader however in return you have to make material functions and apply them to each object you want to have cel shading.

the cel shader itself is quite simple in reality it takes in the sun position and creates 4 bands with a gap that can be changed each band is increasingly darker to create a shadow effect by using lerp interpole nodes to change between each shade of shadow depending on the distance from the sun.