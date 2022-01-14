---
title: "simple-match"
author: "Altair"
type: article
draft: false
--- 

```python
import re

```


```python
content = "Eminem means positive"
```


```python
a = re.search('^Em.*ve$', content)
```


```python
if(a):
    print('matched')
else:
    print('not matched')
```

    matched



```python
# More situations

# Match Canadian postal code
# Phone number
# Start with /home
# Contains /User/raja
```


```python

```
