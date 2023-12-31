---
tags:
  - Code
---
This is a note for quick setup of movement in a side-view 2D game, it uses many [[Functions]] & includes many variables 

NOTE: Game Object with this script must have the following:
	- Box Collider 2D
		- Material - No friction material
	- Rigid Body 2D
		- Body Type - Dynamic
		- Collision Detection - Continuous
		- Sleeping Mode - Never Sleep
		- Interpolate - Interpolate
		- Freeze Rotation - Checked
	- An empty child object placed at bottom of sprite
	- Sprite Renderer
- The Movement Script will have slots called Rb and Ground Check
	- The Rigid Body 2D must be in the Rb slot
	- The empty child object should be in the Ground Check slot

Code Starts Below
----------------------------------------------------------------------------------------------

using System.Collections;

using System.Collections.Generic;

using UnityEngine;

  

public class PlayerMovement : MonoBehaviour

{

    private float horizontal;

    private float speed = 8f;

    private float jumpingPower = 16f;

    private bool isFacingRight = true;

  

    [SerializeField] private Rigidbody2D rb;

    [SerializeField] private Transform groundCheck;

    [SerializeField] private LayerMask groundLayer;

  

    // Update is called once per frame

    void Update()

    {

        horizontal = Input.GetAxisRaw("Horizontal");

  

        if (Input.GetButtonDown("Jump") && IsGrounded())

        {

            rb.velocity = new Vector2(rb.velocity.x, jumpingPower);

        }

  

        if (Input.GetButtonDown("Jump") && rb.velocity.y > 0f)

        {

            rb.velocity = new Vector2(rb.velocity.x, rb.velocity.y *0.5f);

        }

  

        Flip();

    }

  

    private void FixedUpdate()

    {

        rb.velocity = new Vector2(horizontal * speed, rb.velocity.y);  

    }

  

    private bool IsGrounded()

    {

        return Physics2D.OverlapCircle(groundCheck.position, 0.2f, groundLayer);

    }

  

    private void Flip()

    {

        if (isFacingRight && horizontal < 0f || !isFacingRight && horizontal > 0f)

        {

            isFacingRight = !isFacingRight;

            Vector3 localScale = transform.localScale;

            localScale.x *= -1f;

            transform.localScale = localScale;

        }

    }

  

}

![[Pasted image 20230831104916.png]]