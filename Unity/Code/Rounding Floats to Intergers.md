---
tags:
  - Code
---
Sometimes certain things in UI, console, or else where will not take floats or doubles (You can learn about these in [[Variables]]), so you have to convert them to integers, but how? Well, rounding is actually very simple, only being the following line of code;

[*VariableA* = Mathf.RoundToInt(*VariableADecimalVersion*);]

![[Pasted image 20231006110823.png]]

You can even make quick [[Functions]] to make doing this easier;

float x = 4.6134906; 
float y = 6.52151;
float z =134.5321521;

void Update()
{
	Rounder(x);
	Rounder(y);
	Rounder(z);
	Debug.Log(x);
	Debug.Log(y);
	Debug.Log(z);
}

void Rounder (float num)
{
	Mathf.RoundToInt(num);
}

This little byte of pseudo-code shows an example of what a rounding function might look like.
