---
date: 2026-04-27
---

# UE5
## Options Menu
To complete the options menu from [[devlog 13]] I added a multiplier to the cards and enemies, to do this I added a multiply node after the decision node to multiply the percentage, this allows the difficulty to be scaled easily however it can cause issues if the numbers are too high
![[Screenshot 2026-04-27 102337.png]]

# Blender
## Trees
In [[Research 07]] I found 2 videos on how to make low poly foliage inside blender, I started by following the video on how to make low poly trees inside blender, after following the video I created something similar in the image below.
![[Screenshot 2026-04-27 114458.png]]
To start I added a cube and merged all vertexes to the centre this gives me a point where I can make a tree trunk and branches, from the single vertex I can extrude several times to create a tree shape, after forming a shape I can use a modifier called "skin" which adds geometry back onto the tree, I also scaled up and down the skin to make the trunk larger and branches smaller to make a more realistic tree.
![[Screenshot 2026-04-27 114502.png]]
Finally to add leaves I used the isometric sphere trick I learnt in the video from [[Research 07]] to make leaves I also rotated them around so the leaves have some variety alongside scaling them too.
# UE5
Back to unreal engine I imported the trees by exporting the trees from blender using the glb/gltf file format and imported them into unreal engine. Too add them into my game I used turned it into a foliage actor and placed it into the world. (I used unreal's dedicated foliage actors as using single static meshes can cause performance issues) However I encountered an issue with the foliage.
![[Screenshot 2026-04-27 121823.png]]
The enemies would collide with the trees in my game and would get stuck instead of walking around them, to fix this I had to change the collision of the trees to block all which caused the navigation mesh to build around the trees, which you can see happening below. I learnt how to to this in [[Research 09]]
![[Screenshot 2026-04-27 131639.png]]


> [!note] previous devlog
> [[devlog 13]]

> [!tip] next devlog
> [[devlog 15]]

