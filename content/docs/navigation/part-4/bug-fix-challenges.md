---
title: Bug Fix Challenges
weight: 9
---

# Part 4 - {{< param "title" >}}

Bugs are things that don’t work quite right in your code. Absolutely all code has bugs in it when it’s first written. Let’s try to fix a couple now. For each bug you should follow this process:

1. Reproduce it. This means checking that you can see the bug happen.
2. Figure out why it’s happening.
3. Fix it!
4. Check that you can’t reproduce it any more.

- **Bug #1**: When you die and start again, your score at the top of the screen doesn’t go back to zero.
- **Bug #2**: If you crash in to the top pipe in just the right place your falling ghost can keep flying far enough to get a cheeky extra point.

Hint: You could try changing `scroll_speed` to make it easier to reproduce this bug.

# Well Done!!!

You’ve written a complete fully working game! Take some time to enjoy playing your creation! Remember there are values in the code like gravity, scroll_speed, and gap that you can tweak to try to make it more fun.

If you want to add more features to your game the PyZero documentation will help:

https://pygame-zero.readthedocs.io/en/stable/

If you want to add something to the game then talk to a mentor about how you might do it. Here’s a few things you might want to try:

- Make the bird stay still until the first flap
- A high score feature so you can see your best score.
- Starting the game with 3 lives so you can hit the pipes twice without dying
- Collectible stars
- Pipes that move up and down as they come towards you
- Variable scrolling speed. Maybe flapping speeds you up