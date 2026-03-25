Monday 16th march 2026
# starting UE5 project
Creating a project in Unreal engine 5, used 3rd person preset with the twin sticks template
## AI System
I started by working on the AI system by using the template built into unreal engine. However the template is not very well made and just gives me a base with blueprints and files to have a somewhat functional AI system, the first issue encountered was that all enemies would move to (0,0) no matter the condition by moving the navigation volume away from (0,0) the issues was fixed
>![[Pasted image 20260316153850.png]]
> screenshot above shows a bug causing enemies to move to 0,0

### Toggling AI
The AI automatically locks onto the player no matter the distance they are from the player because of this the enemies will spawn and start moving towards the player no matter the condition.
To change this to make enemies only attack the player when they are within a specific range, by adding a sphere collision which enables the 
> ![[Pasted image 20260317123237.png]]
> screenshot above shows working AI system with detection

>[!note] previous devlog
>[[Welcome]]

> [!tip] next devlog
> [[devlog 02]]



