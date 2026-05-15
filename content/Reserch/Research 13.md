---
date: 2026-05-06
---
# UE5
## Materials
In [[devlog 19]] I want to create an hurt animation by highlighting the character in red for a small time, because I am using Material Instances for my shaders I came up with the idea to change the albedo tint dynamically using a timer however I did not know if I can change material instance parameters inside blueprints, so i asked ChatGPT how to do it
<iframe
	src="https://chatgpt.com/share/6a06e4a1-ec90-8327-b44c-30d9b57d5e59"
	width="100%"
	height="600"
	</iframe>

> https://chatgpt.com/share/6a06e4a1-ec90-8327-b44c-30d9b57d5e59

ChatGPT gave me a solution to my problem when I asked "how can i change a material instance parameters inside blueprint", to change material instance parameters inside blueprint I simply turn then characters material into a dynamic material and promote it to a variable then I can use a set vector parameter variable to change different variables inside the material instance.
ChatGPT also gave me some tips when doing this, a key point is that parameter names are case sensitive when entering the name of a parameter to a set vector parameter node I need to check for capital letters as they are case sensitive. Another point is that I have to use a dynamic instance to change parameters 

![[Pasted image 20260515141640.png]]
