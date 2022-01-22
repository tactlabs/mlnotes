---
title: "search"
author: "Altair"
type: article
draft: false
--- 

```python
import re
```


```python
data = [
    "name['toronto'] = 'One'",
    "state['ontario'] = 'Two'",
    "country['canada']['ca'] = 'Three'",
    "extra['maple'] = 'Four'"
]
```


```python
REGEX = re.compile(r"\['(?P<word>.*?)'\]")
```


```python
for line in data:
    found = REGEX.search(line)
    if found:
        print(found.group('word'))
```

    toronto
    ontario
    canada
    maple



```python

```
