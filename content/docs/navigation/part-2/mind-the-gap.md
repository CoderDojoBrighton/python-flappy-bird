---
title: Mind The Gap
weight: 2
---

# Part 2 - {{< param "title" >}}

How do we make a gap for our bird to fly through? We need to make sure we position the pipes in the right place on the screen, and to do this we need to know how big each image is.

Let’s see what we can find out from an Actor, add this code at the end of your program:

```python
print(top_pipe.width, top_pipe.height)
```

- Press **play** and look in the bottom half of your code window.

You should see two numbers appear (I get `100 500`), that’s the width and height of the top pipe in pixels.

Using that info, we can change the construction of the top and bottom pipes to this:

```python
gap = 140
top_pipe = Actor('top', (300, 0))
bottom_pipe = Actor('bottom', (300, top_pipe.height + gap))
```

The two values separated by a comma at the end of each `Actor` line control the **x** (left to right), and **y** (top to bottom) position of the `Actor`. So `(300,0)` puts the pipe at 300 pixels away from the left edge, and 0 pixels down from the top of the window.

Hang on a minute, where did that maths come from? Well, `gap` is a new variable we’re creating, and we say that the height of the top pipe plus `gap` should be the **y** value of the bottom pipe. Try changing the `gap` value and see what happens.

- Press **play** to check we made a gap

*What’s the biggest gap you can make and still see the bottom pipe?*

## You know when to press play

You’ve been pressing play a lot haven’t you? That’s how you see the effect of your code changes.

From now on we won’t always tell you when to press play. We encourage you to try running your code when you’ve completed each litte code box, or whenever you feel like it.

Sometimes you’ll see an error, in which case: read the last line of the error, think about what you just changed and get investigating. You can always ask a mentor if you need help.
