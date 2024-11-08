---
title: Explaining things to your future self
weight: 5
---

# Part 4 - {{< param "title" >}}

Our update function is getting pretty big now. It’s starting to take a while to figure out what does what. It’s time to introduce **comments**!

Comments are any text that you write in your file that you want the computer to ignore. If you write helpful comments then it makes it easier for you, or even someone else to understand what your code is doing.

Let’s add some comments so that our update function looks something like this:

- Add the lines starting with #

```python
def update():
    # Move Barry
    barry_the_bird.speed += gravity
    barry_the_bird.y += barry_the_bird.speed

    # Move pipes
    top_pipe.x += scroll_speed
    bottom_pipe.x += scroll_speed

    # Pipes off screen?
    if top_pipe.right < 0:
        top_pipe.left = WIDTH
        bottom_pipe.left = WIDTH

    # Barry off screen?
    if barry_the_bird.y > HEIGHT or barry_the_bird.y < 0:
        reset()

    # Hit pipe?
    if (barry_the_bird.colliderect(top_pipe) or barry_the_bird.colliderect(bottom_pipe)):
        hit_pipe()

    # Change score?
    if top_pipe.right < barry_the_bird.x:
        barry_the_bird.score += 1
```

Every line that starts with # is a comment and will be ignored by Python.

Normally a programmer would always be adding comments as they write code. Feel free to add comments to your code as you work. Or to go back and add comments to code you already wrote. It will make things easier for you!

- Check the everything still works the same as before.