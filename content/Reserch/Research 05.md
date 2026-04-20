---
title: Research 5
date: 2026-04-15
---
# UE5
## Performance
When it comes to optimising my game in [[devlog 07#debugging]] I researched a little bit on optimising my as well as how to enable a performance overlay this performance overlay was quite helpful as it showed me several values including the frame-rate which is how many frames are rendered per second, or ram usage which is how shows how much memory my game is using in total 
![[Pasted image 20260415095217.png]]

## Blueprint interfaces
I did not intentionally need to research about blueprint interfaces however I found this video that goes over how blueprint interfaces work.
![https://youtu.be/Ba_gEz229Wg](https://youtu.be/Ba_gEz229Wg)
This video tough me how blueprint interfaces work in more detail, he also shows an example of how the work by creating a "boost" function and calling it, he states "this basically allows an outside actor to call an event on a separate actor",  which means that an object can trigger an event inside another object without using casting nodes. He also mentions that interfaces can take more than just a trigger event as they can move data like variables, arrays, and etc if needed. He also mentions that blueprint interfaces are called a "soft reference" which means that they are more performant than using a cast node to get references form other objects.