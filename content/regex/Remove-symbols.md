---
title: "Remove-symbols"
author: "Altair"
type: article
draft: false
--- 

```python
content = "This device is costing only 12.89$. This is fantastic!"
```


```python
content
```




    'This device is costing only 12.89$. This is fantastic!'




```python
import re

```


```python
re.sub(r'[^\w]', ' ', content)
```




    'This device is costing only 12 89   This is fantastic '




```python
# Note:

# \w will match alphanumeric characters and underscores

# \w
# will match anything that’s not alphanumeric or underscore
```


```python

```
