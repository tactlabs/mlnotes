---
title: "Regex-groups"
author: "Altair"
type: article
draft: false
--- 

```python
import re
```


```python
names = ['A2B8']

for name in names:
    m = re.match("^[A-Z]\d[A-Z]\d", name)

    if(m):
        print(m.groups())
        print('matched : ', name)
```

    ()
    matched :  A2B8



```python

```
