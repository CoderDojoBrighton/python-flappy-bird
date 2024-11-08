---
title: Extra Challenges
weight: 7
---

# Part 3 - {{< param "title" >}}

- Turn physics upside down! Make gravity pull Barry upwards, and make flapping push him downwards
- Add a cheat key that makes the player invincible

Hint: Try adding this function and see what happens when you press a key:

```python
def on_key_down(key):
    print(key)
```

- Add a secret tiny flap that the player can do using the right mouse button

Hint: you will need to add a **parameter** to your `on_mouse_down` function, so it becomes `on_mouse_down(button)`. Try use the `print` function like you did in the last challenge to see what values `button` has.


[Go to Part 4](../../part-4/starting-point/)