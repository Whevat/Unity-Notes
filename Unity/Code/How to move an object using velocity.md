---
tags:
  - Code
---
There is many ways to move a object in unity, sometimes the best & most smooth way to do so is by using velocity. Velocity is adding a force to the object that pushes it in a direction, which visually is smoother than just teleportation (Moving an object by changing it's x/y/z directly).

To use velocities a rigid body is needed, a rigid body is a component that adds physics to an object, which then allows forces to be exerted onto it.

The coding aspect of velocities is quite easy, however you will have to get the rigid body component so I recommend that you find how to do that in [[Getting Components]]. Now, to the code;

[rigid body nickname].velocity = new Vector2([rigid body nickname].velocity.==x==, [force amount]);

==*x can be replaced with y or z, it depends on what direction you want the force to be applied to. **remember; when a object is rotated, it's x, y, & z axis-es also rotate.***==

![[Pasted image 20231019110755.png]]

**Diagram**;
![[Pasted image 20231019111123.png]]
