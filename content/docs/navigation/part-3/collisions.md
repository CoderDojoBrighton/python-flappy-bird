---
title: Collisions
weight: 6
---

# Part 3 - {{< param "title" >}}

In PyGameZero there’s nothing to stop you drawing multiple sprites (images) on top of each other. So if we want certain behaviour when things collide we need to take care of it ourselves. Add this code to the end of the update function:

```python
if (barry_the_bird.colliderect(top_pipe)):
    hit_pipe()
```    

The `colliderect` function checks if two objects are touching. Because this is inside the update function it will get checked every frame. This won’t work yet because we haven’t created the `hit_pipe` function. Let’s create it after the reset function...

```python
def hit_pipe():
    print ("Hit pipe!")
    barry_the_bird.image = "birddead"
```

Try this out. Now Barry should become a ghost when you hit the top pipe, but it looks like there are still three problems:

1. Barry stays as a ghost even when the game resets.
2. Barry can still fly through the bottom pipe!
3. You can still flap and fly along even as a ghost.

- Try to fix problems 1 & 2 now. We’ll look at 3 together.

**Hint for number 1** : Barry started with the “bird1” image, but it changes to “birddead” when he hits a pipe. Find the right place to change it back.

**Hint for number 2** : Remember the or keyword.

Now might be a good time to try changing the size of `gap` to tune the difficulty of the game. You might want to make it very big while testing, so you can focus on testing and not on flying!

Now we’d like to stop Barry from flapping while he’s a ghost. The code which makes him fly needs a way of knowing if he’s still alive. We could use the `barry_the_bird.image` variable, because that changes when he dies. But it’s better to add a new variable to make our code cleaner and less likely to break if we make changes later.

- Add this line to the reset function (Being a lazy coder pays off again!):

```python
barry_the_bird.alive = True
```

We’re creating the new variable `alive` and setting it to `true`. Now we need to make sure barry only flaps when he’s alive.

- Add this line to the beginning of the on_mouse_down function:

```python
if (barry_the_bird.alive):
```    

Don’t forget to change the indentation (number of spaces at the beginning) of the line that changes the speed, so that it’s part of the `if` statement. We only want to change the speed (in other words flap) `if` the bird is alive!

The next thing to do is to change barry to not be alive when he hits a pipe.

- Add a line to change barry’s `alive` variable to `False` when he hits a pipe.

Well done. That’s the end of part 3. In the next part we’ll look at a few finishing touches such as adding a flapping animation, randomizing the pipe positions, and keeping score.

