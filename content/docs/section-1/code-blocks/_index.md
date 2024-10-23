---
weight: 1
bookFlatSection: false
title: "Code Blocks"
---

## Code Blocks

Code blocks can be added inline with single backticks: `for_example`.

Or with triple backticks:
```
for example
```

You can supply a language name for syntax highlighting:
```python
print("Hello, world!")
```

The `highlight` [shortcode](https://gohugo.io/content-management/shortcodes/#highlight) can be used to highlight parts of a code block:
For example:
{{<highlight python "linenos=false,hl_lines=6-8">}}
from flask import Flask
import json

app = Flask(__name__)

@app.route('/hello')
def hello():
    return "hello"

if __name__ == "__main__":
    app.run(host="0.0.0.0")
{{</highlight>}}
