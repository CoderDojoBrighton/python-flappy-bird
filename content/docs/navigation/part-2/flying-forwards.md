---
title: Flying forwards
weight: 4
---

# Part 2 - {{< param "title" >}}

So now that we have the pipes, let’s get them moving.

**Note: Smoke and Mirrors**

You might be thinking “doesn’t the player fly forward and the pipes stay still?”

If you thought that, then the game fooled you. It’s a good trick. It looks like the player is moving forward. But in reality, the player stays still and everything else moves backwards.

So let’s make the pipes move. Just as we did with our bird we can create a speed variable for the pipes and use this to move them. We want the following line of code to run once when we run the program, so it needs to go at the end of your code:

```python
scroll_speed = 1
```

And they need to move continously, so this code goes in the `update` function:

```python
top_pipe.x += scroll_speed
bottom_pipe.x += scroll_speed
```

- Press **play**

Oh no! Why are the pipes moving the wrong way?

*Can you fix it? Hint: when setting the speed, what’s the opposite of 1?*