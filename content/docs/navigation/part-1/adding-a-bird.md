---
title: Adding a Bird
weight: 3
---

# Part 1 - {{< param "title" >}}

- Add this line to the end of your file

```python
bird = Actor('bird1', (75, 350))
```

This time there shouldn’t be any spaces at the beginning of the line. This means this instruction doesn’t belong to a function. These instructions will only happen once at the beginning of the game.

This line is creating an `Actor` called `bird`.

`Actor` is part of Pygame Zero, but `bird` is a new variable that you are creating by writing that line. You can call it anything you want. If you wanted to you could write:

```python
barry_the_bird = Actor('bird1', (75, 350))
```

Let’s actually do that! I’ll carry on with `barry_the_bird`, but if you want you can choose your own name. Just remember to type the name that you chose instead of barry_the_bird each time we use the variable.

**Warning**: Don’t put any spaces in the name of your variable. Instead you can use the _ character. Also, don’t use capital letters, this will make it easy for you later.

- Press **play** to check your code still works. Nothing will be different.

If we actually want to see Barry (or whatever your bird’s called), we’ll need to add him to the `draw` function.

Add the following line your `draw` function (remember to use the name of your bird):

```python
barry_the_bird.draw()
```

Now your whole file should look like this:

```python
TITLE = 'Flappy Bird'
WIDTH = 400
HEIGHT = 708

def draw():
    screen.blit('background', (0, 0))
    barry_the_bird.draw()

barry_the_bird = Actor('bird1', (75, 350))
```

- Press **play**

<img src="/python-flappy-bird/part-1/background_and_bird.webp" alt="" style="width:200px;"/>

*What happens if you swap the order of the lines in the draw function?*

*Why do you think that happened?*