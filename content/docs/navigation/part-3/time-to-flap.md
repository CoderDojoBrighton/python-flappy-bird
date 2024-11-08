---
title: Time to Flap!
weight: 3
---

# Part 3 - {{< param "title" >}}

At the moment, Barry the bird seems to teleport upwards when you click the screen (play the game now if you don’t remember). We’d really like him to move a bit more smoothly. The reason he seems to move instantaneosly is this line:

```python
barry_the_bird.y -= 50
```

This makes him move a whole 50 pixels all at once. Not very smooth! When a real bird flaps its wings it changes the bird’s speed, not its position. Change in position is just a side effect of having speed.

- Change your `on_mouse_down` function to this:

```python
def on_mouse_down():
    barry_the_bird.speed = -6.5
```    

Did that work? Try it and you’ll see that when you flap now he’ll just go up and hit the top of the screen.

We need some gravity to pull him back down again after each flap!

- Create a variable called gravity at the end of your file:

```python
gravity = 0.3
```

And we’ll use this to change the bird’s speed every frame.

- Add this to the beginning of the `update` function:

```python
barry_the_bird.speed += gravity
```

*Try changing the value of gravity to see what effect it has*

Now this bird is more flappy! Controlling him now takes a bit more skill. You can try to fly through the gaps, but we still haven’t done anything to stop you flying straight through the pipes. We’ll fix that soon. But first…