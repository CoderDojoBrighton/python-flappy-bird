---
title: Let’s get to the point
weight: 3
---

# Part 4 - {{< param "title" >}}

A number which always stays the same isn’t very helpful! We need to make this number get bigger as the player goes past pipes. Let’s add another variable to Barry to keep track of the score.

- Add this to the bottom of the file:

```python
barry_the_bird.score = 0
```

Now let’s add some code to increment (add 1 to) the score when we go past a pipe.

- Add this to the end of the update function:

```python
if top_pipe.right < barry_the_bird.x:
    barry_the_bird.score += 1
```

But we still need to plug the score variable into the code that draws the number on the screen.

- Change the call to the screen.draw.text function in your draw function so that it uses the score variable

## Why does the score go up so fast?!

You’ve probably noticed now that when you fly through some pipes the score soars upwards for a short period, instead of just going up 1.

*Can you think why this might be?*

The reason is that the code we added is in the update function, which runs every frame. The code we added will increment the score if the bird is past the pipe. But the bird is past the pipe for the whole time it takes the pipe to get to the edge of the screen. Every single frame while Barry is past the pipe the score goes up one. This gives you an appreciation of how fast the computer is drawing frames!

There are several different ways to solve this problem. If you have your own idea then go ahead and try it out - don’t be afraid to ask a mentor if you want help. Or, you can leave this for now and read on to see how we’re going to solve it.
