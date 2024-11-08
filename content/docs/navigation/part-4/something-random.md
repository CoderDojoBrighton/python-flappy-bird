---
title: Something Random
weight: 7
---

# Part 4 - {{< param "title" >}}

To make the game more interesting we want the gap between the pipes to be at a different y position each time. To do this we need to pick a random number.

Often in Python you’ll need to use the `import` keyword to get access to functions that aren’t available by default. These extra functions are grouped together in **modules**.

- Import the random module by adding these lines to the very top of your file:

```python
import random
print (random.randint(1,6))
```

The second line is to test the `randint` function in the `random` module. If you run your game now you should see a number printed in the Mu log.

- Start the game a few times to see what this function does.

Hopefully you’ll see that this function returns a random integer (whole number) in the range of the two arguments we gave it. So in this case, from 1 to 6. Now that we’ve tried it we can delete the `print` line, but keep the `import` line.

Now let’s use a random integer to move the gap up or down. We’ll do this in the update function, at the same time as when we move the pipes to the right side of the screen.

- Find the 2 lines which do `left = WIDTH` for the pipes, and change them to:

```python
offset = -150
top_pipe.midleft = (WIDTH,offset)
bottom_pipe.midleft = (WIDTH,offset + top_pipe.height + gap)
```

If you test it now you’ll see that after the first set of pipes the gap is much higher (150 pixels higher to be precise). Note that this doesn’t affect the first set of pipes.

- Use the `random.randint` function to move each pair of pipes to a random offset

Hint: When testing changes like this you might want to make the `gap` bigger so you don’t have to spend so many attempts getting through the pipes.