---
date: 2026-04-29
---
# Blender
## Foliage modeling
Going back to some more modelling for my game I decided to finish the foliage modelling.
By following the tutorial in [[Research 07]] I followed the first tutorial to make several bushes for my game.
![[Screenshot 2026-04-29 141656.png]]
Above is an image of every bush that I added to my game. To make all the bushes I started with an isometric sphere with one subdivision, the tutorial shows the person moving the bottom point into the model however this is less efficient as well as leaving excess faces so instead I merged the bottom vertex to one of the sides which makes the bottom of the model flat with no weird issues, it also reduces the face count and automatically triangulates the object with ue5 prefers. After making one bush I duplicated the sphere to make several more bushes as well as adding verity by scaling and rotating the bushes.
![[Screenshot 2026-04-29 091857.png]]
After making one bush I created several more bushes inside the same blend file. After exporting them into unreal engine I had to fix the pivot points of each bush using the mesh editor tool built into unreal engine. After fixing the mesh I then added them as foliage actors and placed them around the map

# UE5
## Cel Shading
Cel shaders is another key part of my game in my [[Game design Document]] I wanted cel shading to be one of the main focuses of the art style.
![[Screenshot 2026-04-29 141436.png]]
To make this cel shader I first started by creating a folder called shaders and made a new material function called "MF_celShading". By following the video I started by creating 4 light bands for the shader this is done by using lerp interpoles at specific distances from the sun to make bands of light, At the same time I added the Shadow mask which gets the sun's location from the world and gets multiplied for a normal to create a shadow mask. After making the bands I also added night colour which simply tints all the colours during night time to add some realism, however this is not very necessary to add as there is not day light cycle in my game. The penultimate feature to add to the shaders is a rim light and rim mask this simply adds a glow around the entire object with any colour I chose. And the final part of my shader is to add sky colour into the material this allows the sky to influence the colour of objects making it more realistic and give the feeling that it is inside an environment and not just plastered in.

After testing my shader I came across an issue, the light bands were not aligned with the sun correctly. To fix this issue I scrubbed back through the video and referenced my shader, I eventually found the issue which was I used a "PixelNormalWS" instead of a "VectorNormalWS" so switching it over fixed my issue.
![[Screenshot 2026-04-29 114559.png]]
Now to add the material function to my game I made a new material and inserted my custom function into the emmisive texture, I also added a float parameter on: metallic, specular, roughness, and anisotropy, this allows me to modify these values when I make material instances alongside the albedo texture and tint I also added as modifiable parameters. Finally I added a normal texture parameter and flattened it to create a more flat cel shaded style.
![[Screenshot 2026-05-05 091626.png|697]]
To add the cel shading to other models I have to create a material instance for each cel shaded material. A material instance copies the parent material and allows you to change any parameter inside the material or any material instances inside it, below is an example of a material instance for the future.
![[Screenshot 2026-05-01 094212.png]]
# Blender
## Foliage modeling
Continuing on with making my foliage I went back to the video to make some grass for my game, after adding cel shading on the bushes and tress I wanted to also add some grass for some extra detail.
![[Screenshot 2026-04-29 141609.png]]
Following the tutorial in [[Research 07]] I made a cube and scaled it down and into a rectangle shape, I then extruded the top face twice and moved them around to create a blade of grass. Finally I merged the top face to make a sharp point, scaled down the second face to create a more grass shape, and removed the bottom face to help performance and reduce my face count. I then repeated these steps to make a few more variations of blades of grass, then I duplicated and combined them to make small patches of grass similarly to the video.

I also made some more variations of tress using the tutorial in [[Research 07]] and using the same blend file I added 4 more trees and then imported them into unreal engine.
![[Screenshot 2026-04-29 141635.png]]
After applying the same fixes to my models in [[devlog 14]] I fixed the pivot points of the trees, grass, and bushes, this fixes any issues with the foliage tool from placing trees not where I click.  I also applied my cel shader to all the foliage by going to the material folder inside the imported files and changing the material instance parent from the default blender material to my custom cel shading material, then changing the albedo tint to the correct colours.
![[Screenshot 2026-04-29 133545.png]]
Here is an image before I added the grass foliage with the cel shaded trees and bushes.


> [!note] previous devlog
> [[devlog 14]]

> [!tip] next devlog
> [[devlog 17]]

