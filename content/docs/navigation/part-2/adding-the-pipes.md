---
title: Adding the pipes
weight: 1
---

# Part 2 - {{< param "title" >}}

So now you have a background and a bird that flys up and down, let’s add the pipes that the bird must fly through.

You’ve already seen that we can create `Actor` objects and move these around the screen. If you’ve forgotten, go and look at where you use `barry_the_bird` in your code to see how it works.

So we need to add two pipes, and if you look in the images directory you’ll see we have two files named `top.png` and `bottom.png`. How do we add these to the game?

Let’s create two new actors, at the end of your code add:

```python
top_pipe = Actor('top', (300,0))
bottom_pipe = Actor('bottom', (300,500))
```

We mustn’t forget to draw these pipes, so add this to your `draw` function:

```python
top_pipe.draw()
bottom_pipe.draw()
```

- Press play to see the effect.

Great, we have some pipes! But they are just sitting there on the page and there’s no gap between them.

*Can you figure out what the `(300, 0)` and `(300, 500)` parts do? (Try changing them)*
