---
title: "simple-regex"
author: "Altair"
type: article
draft: false
--- 

```python
import re
```


```python
pattern = 'awesome'

content = 'Duckduck go is awesome and it is getting better everyday'

match = re.search(pattern, content)

#print(match)

start = match.start()
end = match.end()

#print(match.string)

print(start, end)

```

    15 22



```python

```
