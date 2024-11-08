---
title: Keeping Score!
weight: 2
---

# Part 4 - {{< param "title" >}}

- Add the following code to the end of your `draw` function:

```python
screen.draw.text(
    str(7),
    color='white',
    midtop =(20, 10),
    fontsize=70,
    )
```

This looks like a lot of code, but this is actually just one command (called a **statement** in programming languages). Up until now every **statement** we’ve used took up just one line, but this line is different. Python knows that the statement doesn’t end on the first line, because the “(” doesn’t have matching “)” on that line, so it takes all the following lines up to the matching “)” as part of the same statement. That means that the following code wouldn’t work:

```python
# BAD CODE.  Don't type this in!
# Python will think this next line is a whole statement and will get confused:
screen.draw.text
    (
    str(7),
    color='white',
    midtop =(20, 10),
    fontsize=70,
    )
```

Python would think that `screen.draw.text` is a whole statement, and that doesn’t make sense to it.

- Check that now when you play the game you see a number 7 at the top of the screen.

So why is this statement so big? Well, it’s because we’re calling a function which takes a lot of **arguments**. Arguments are like options. When you call a function, if there are no arguments it looks like this:

```python
make_toast()
```

This should look familiar to you, this is how we call our `reset()` function, and our `on_hit_pipe()` function. But if you want to pass arguments then the function call looks like this:

```python
make_sandwich(white_bread, cheese)  # Arguments are separated by a comma
```

The long statement we added above is a call to the `screen.draw.text` function (It’s a good name for a function that draws text on the screen!). See how the function call has 4 arguments separated by commas.

*Can you figure out what each of these arguments does by changing them and testing the results?*

- Move the number so it’s centered at the top of the screen

Hint : Remember that `WIDTH` contains the width of the screen

Normally programmers don’t have to guess what arguments do. It’s much easier to read the instructions! You can find the documentation of this function at:

https://pygame-zero.readthedocs.io/en/stable/ptext.html

- Add a drop shadow to the number

Hint: Look at the section titled “Drop Shadow” on that page. You only need to add one more argument to the function call. Ask a mentor for help if you have trouble getting this working.