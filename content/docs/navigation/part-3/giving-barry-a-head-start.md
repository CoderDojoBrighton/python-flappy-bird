---
title: Giving Barry a head start
weight: 5
---

# Part 3 - {{< param "title" >}}

Let’s give the player a bit more time to flap before they fall off the screen. We can move the start point to just 50 pixels away from the top of the screen. Find this line in the reset function:

```python
barry_the_bird.center = (75, 350)
```

- Change the 350 to something much smaller. Maybe 50? Try it and find a value that seems right to you.

Isn’t it great this number is only in one place in the code? If we hadn’t done the last section (Being a lazy coder) we would have to change two different numbers! It would have been very easy to forget about one of them.