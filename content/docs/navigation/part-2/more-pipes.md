---
title: More pipes
weight: 5
---

# Part 2 - {{< param "title" >}}

We need more pipes, one set is not enough. But actually we have enough already, we can just loop them round when they go off the screen.

To do this, let’s meet the very handy `if` statement and two of its friends, greater-than `>` and less-than `<`...

What do you think this code does? Open a new Mu script and type it in:

```python
a = 10
if a > 5:
    print("Wow a is big")
```    

- To run this you’ll need to save it first, just pick a filename such as `test.py`.
- Look at the bottom of the Mu editor to see the output from your code

What about this code?:

```python
a = 10
if a < 5:
    print("Wow!")
    print("a is small")
print ("The End")
```

*Try changing the `a = 10` line to make all 3 print statements run*

So as you can see (hopefully!) `if` tests something, in the first example if the variable `a` is greater than 5, and then does whatever you tell it to do.

There are two tricky things to get right with `if` statements:

- Exactly what are you testing? What goes after the `if`?
- Get your indentation right – how many spaces at the start of the line – so that the right code is run.

## Looping the pipes

OK, let’s get to work in the update function, as that’s where we move the pipes. Add this code to the end of the function, and make sure you indent it (add spaces to the beginning of the line) so that it really is inside the function. Ask a mentor for help if this doesn’t make sense.

```python
if top_pipe.x < 0:
    top_pipe.x = WIDTH
```

OK, that’s not bad, but two problems…

1. Only the top pipe moves
2. The pipe dissappears too quickly, before it’s left the side of the screen

- Can you fix these issues?

## Ouch! 

OK, it’s time to deal with collisions. This is going to be painful, but don’t worry no actual birds are going to be harmed – only virtual birds.

[Go to Part 3?](../../part-3/starting-point/)