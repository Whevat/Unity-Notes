---
tags:
  - Code
---
Sometimes in games when you get hit, your character will flash with transparency. You can do this within code via color32. 

The first thing you'll want is call/assign the sprite renderer with in the code, you can learn how to do that in [[Getting Components]]. Once that is done you'll need to make a new colour. This line will be constructed like so;

public Color32 [colour name] = new Color32 ([red], [green], [blue], [alpha (transparency)]);

![[Pasted image 20231031114241.png]]