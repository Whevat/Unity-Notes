---
tags:
  - Code
---
Fixing the frame rate will make the FPS be the same no matter what computer you have (assuming the CPU can handle it)
The easiest way to ensure this (That I know of Sept/7/2023) is by putting the code below in the player's movement code;

void Awake()
{
	QualitySettings.vSyncCount = 0;
	Application.targetFrameRate = [Desired Frame Rate];
}

![[Pasted image 20230907113007.png]]

HOWEVER sometimes when a certain part of code needs to be affixed to time time.deltaTime needs to be used. Often you will multiply/add this to the thing that needs to be connected to time. 

![[Pasted image 20230911114443.png]]

You also can easily change the frame rate during game play/testing by serialising it or by making it a variable. How to accomplish this can be found in [[Serialising Fields]] & [[Variables]] or you could use a variable from another script & just use the variable for multiple things, although the variable would have to be a integer & be a rather high number, but those directions can be found here; [[Using Variables from other Scripts]]. 