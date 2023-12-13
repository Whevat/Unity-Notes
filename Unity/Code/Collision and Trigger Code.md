---
tags:
  - Code
---
Collision and Triggers are very important [[Functions]] in code, and this is generally how they work;
Collision is when something hits another thing, and so it only is triggered when you initially hit it. Collision and Trigger are both voids so some simple Collision code would look like so;

![[Pasted image 20230912112243.png]]

Triggers are quite similar, but they are triggered when you go in/on something, here's some code;

![[Pasted image 20230912112351.png]]

Now that code doesn't technically work but the Triggering part does, so just pay attention to that. :)

ALSO; other means the code is activated when anything else hits/enters the object.

Trigger & Collision are often used for things like;

void OnCollisionEnter2D(Collision2D *bullet*)
{
	player take damage
	play ouch sound
}

I used some pseudo code (fake code to show for concepts/examples) for that.