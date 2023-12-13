---
tags:
  - Code
---
In games there is often a button to leave the game, or there is a certain action that makes the game quit itself. There is a *very* simple way to do that;

[Application.Quit();]
![[Pasted image 20231006110349.png]]

Now in my game when your car loses all of it's integrity (health) it quits the game & destroys the car see in [[Deleting Objects in Code]]. It does so with the following;

[void OnDestroy()
{
	Application.Quit();
}]

![[Pasted image 20231006110402.png]]

So now once the Car is destroyed the game will quit to desktop.