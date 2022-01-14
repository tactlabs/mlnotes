---
title: "number-check"
author: "Altair"
type: article
draft: false
--- 

```python
import re
```


```python
pattern = re.compile("^([0-9]+)+$")

content  = "s23434"

if(pattern.match(content)):
    print(pattern.match(content).pos)
else:
    print('not matched')
```

    not matched



```python
content  = "23434"

if(pattern.match(content)):
    print('matched at : ', pattern.match(content).pos)
else:
    print('not matched')
```

    matched at :  0



```python

```
