---
title: Flying back to the start
weight: 2
---

# Part 3 - {{< param "title" >}}

What happens when Barry falls off the bottom of the screen? Right now you probably lose him forever. Let’s try to do something better.

- Add this new function after the `on_mouse_down` function:

```python
def reset():
    print ("Back to the start...")
    barry_the_bird.speed = 1
    barry_the_bird.center = (75, 350)
    top_pipe.center = (300, 0)
    bottom_pipe.center = (300, top_pipe.height + gap)
```

Each line in this function is assigning a value. First it sets Barry’s speed back to what it started as, then puts his center at an x,y position. It also moves the pipes back to their starting points. If you try the game now you’ll see that nothing has changed. Remember that a function won’t do anything until you **call** it. Let’s call it from the update function if Barry goes off the screen.

- Add this to the end of the update function:

```python
if barry_the_bird.y > HEIGHT:
    reset()
```

- Make sure you indent it so that it’s part of the update function, but not part of the previous `if` statement. Indenting means adding the right number of spaces to the beginning of the line.
- Check that everthing resets if Barry falls off the bottom of the screen.

**Ask a mentor for help if you have trouble getting this to work.**

We also need to reset the game if Barry goes off the top of the screen.

- Change your code to make this happen.

Hint: you will need the `or` keyword.