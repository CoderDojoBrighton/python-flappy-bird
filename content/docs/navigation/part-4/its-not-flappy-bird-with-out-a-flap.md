---
title: It’s not Flappy Bird with out a flap
weight: 8
---

# Part 4 - {{< param "title" >}}

So far our bird image is very static and the game should probably just be called “Bird”. Let’s fix that now.

If you click on the **images** button in Mu you will see there are several bird images. So far we’re using “bird1” for the living bird, and “birddead” for the bird ghost. We can also use “bird0” to liven things up a bit!

- Add this code at the end of the update function:

```python
# Animation
if barry_the_bird.alive:
    if barry_the_bird.speed > 0:
        barry_the_bird.image = "bird1"
    else:
        barry_the_bird.image = "bird0"
```

- Pay attention to the indentation here!

Any line that ends in a colon, like a function or an `if` statement has lines following that belong to it. All the lines after it that have at least the next level of indentation belong to it. So for the new `if barry_the_bird.alive:` statement, all 4 lines after it are indented so they all belong to it. They will only happen if Barry is alive! (We need to make sure the bird image stays as a ghost when he’s dead). But, for the `if barry_the_bird.speed > 0:` statement only the next line is indented, so only that one line depends on the if.

The `else` keyword is new to us. You can probably guess what it does. An `if` can optionally have an `else` part after it. The `else` part is what will happen if the value in the `if` statement is false. So our new code is using the “bird1” image when flying downwards (remember that we measure from the top of the screen, so a positive speed means going down), and using “bird0” when flying upwards.

**Ask a mentor now if this isn’t working for you or you don’t understand.**