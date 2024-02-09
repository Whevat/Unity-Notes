---
tags:
  - Code
---
Functions are one of if not the most used thing in unity development, every time you code it is in a [[Collision and Trigger Code]] *Function* or doing things like [[Fixing The Frame Rate]] needs to be in the *Awake* function. [[Getting Components]] requires the use of *at least* the Start function. 
There are ==Pre-made Functions== & ==Self-made Functions==;
==Pre-made Functions== are functions like *Update*, *Awake* or *Start*, they are created by Unity to help you get started. *Update* & *Start* are both preplaced by Unity in every *C#* script you make.
Functions can also be given classes, similarly to [[Variables]]. Public functions can be mentioned/used in other scripts, to do that look in [[Using Variables from other Scripts]], it works the same way. Private ones are only usable in the script it comes from. Now the difference between private & none is that private gives access to the entire script. While none will make it only available to wherever it is created. Say its made in another function, then it will only be usable in that function. [[Variables]] work the same way.

![[Pasted image 20231129110127.png]]