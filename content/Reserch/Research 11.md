---
date: 2026-05-01
---
# UE5
## Health bars
I wanted to add health bars above my enemies inside my game, allowing the player to see the enemy health gives the player another layer of information making the game more enjoyable as they no longer will feel like they have been attacking the enemy forever.

Once again I asked chatGPT for help with this issue I asked "how can i make a health bar above my enemies in unreal", ChatGPT gave me a simple solution to add a health bar to use another widget blueprint and place it above the enemy character and updating it from the enemy blueprint, it also gave me an alternative solution to update the bar manually however I don't believe that I will need every performance boost possible
<iframe 
	src="https://chatgpt.com/share/6a05c30b-ec28-8333-80ed-deeb65346bc8"
	width="100%"
	height="600">
	</iframe>

> https://chatgpt.com/share/6a05c30b-ec28-8333-80ed-deeb65346bc8

I also asked ChatGPT how to make the widgets face the camera instead of following the enemy facing position, this was because I could not see the health bar all the time and it would get cut off because it dose not face the camera. ChatGPT gave me two solutions to fix this issue I decided to go with the second option as I felt that it would look significantly better than using a screen space.
The final question I asked ChatGPT was how to update the widget from the blueprint which turns out to be very simple by simply getting the widget and casting to it from the enemy blueprint I then added a custom event to update the health every time the enemy got damaged.

![[Pasted image 20260515141419.png]]
![[Pasted image 20260515141433.png]]
![[Pasted image 20260515141445.png]]