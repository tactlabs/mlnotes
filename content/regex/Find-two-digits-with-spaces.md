---
title: "Find-two-digits-with-spaces"
author: "Altair"
type: article
draft: false
--- 

```python
import re
```


```python
text = "It happened on Feb 21 at 3:30"

answer= re.findall(r'\b\d{2}\b', text)
print(answer)
```

    ['21', '30']



```python
# To match only two digits with spaces
answers = re.findall(r'\s\d{2}\s', text)

```


```python
for a in answers:
    print(a.strip())
```

    21



```python
# To do
# Find 3:30 or 3.30 or 3-30 alone
```


```python

```
