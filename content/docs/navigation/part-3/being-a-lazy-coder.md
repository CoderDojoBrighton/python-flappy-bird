---
title: Being a lazy coder
weight: 4
---

# Part 3 - {{< param "title" >}}

You might have noticed that there are some lines of code that we’ve had to type in twice in different places. For example, `barry_the_bird.speed = 1`. We do it once in the game setup code, and then again in the `reset()` function, which is called when Barry dies and the game starts again. Well maybe it would make sense to just use the `reset()` function at the beginning of the game as well! Then we’d only need the code in one place.

- Add a call to `reset()` at the very end of the file.
- Now we can delete the `barry_the_bird.speed = 1` call that happens in the game setup code.

*Can you figure out a way to specify the position of everthing in just one part of the code?*

Hint: You should be able to remove 3 position values. One of them looks like: `(75, 350)`

Check the everything still works the same as before.