---
title: Drawing a Background
weight: 2
---

# Part 1 - {{< param "title" >}}

- Add these lines to the end of your program. Make sure you add the spaces at the beginning of the second line.

```python
def draw():
    screen.blit('cascade', (0, 0))
```

The `def` keyword creates a function. A function is a way of grouping instructions together. The function we just made is called `draw`. You need to have a `draw` function if you want Pygame Zero to draw anything. The line that starts with `screen.blit` is the only instruction in this function. It tells Pygame Zero to draw something on the screen.

- Press Play

Let’s try changing the background…

- Press Stop if the game is playing. Then click on the Images button.

You should see a folder with all the images in this project. You can use any of these in the game. You can even add your own images here, either downloaded from online, or created in a paint tool.

- Go back to Mu and change `cascade` to `background` to use the background.png image from that directory.
- Press **Play** to start the game again
- Repeat to find a background that you like
