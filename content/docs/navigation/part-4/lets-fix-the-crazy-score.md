---
title: Let’s fix the crazy score
weight: 6
---

# Part 4 - {{< param "title" >}}

Instead of adding 1 point each time we pass the pipes, let’s number the pipes! We’ll assign a number to each pair of pipes and just set the score to be equal to that number when we go past.

At the beginning of the game the pipes on the screen are pair number 1.

- Add this to the `reset()` function:

```python
top_pipe.pair_number = 1
```

We’ll just keep track in the top pipe, we know the bottom one will always be part of the same pair.

Make it so that this number is incremented when we move the pipes back across to the right side of the screen
Hint : It happens in the update function. Your new comments should help find the place.

- Print out the new `pair_number` when you increment it and look at the log panel in Mu to verify it’s working properly
- Modify the code where we change Barry’s score. Instead of incrementing it set it to be equal to the pair number.

**Please ask a mentor for help if you’re having trouble with any of these steps**

If you got to here and your score is now going up sensibly one at a time then well done indeed!! This was a challenging section with a lot of work, so feel proud!