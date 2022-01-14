---
title: "Specific-pattern1"
author: "Altair"
type: article
draft: false
--- 

```python
import re
```


```python
fn = "DC_QnA_bo_v.15.12.3_DE_duplicates.xlsx"
rgx = re.compile('\b_[A-Z]{2}\b')
print(re.findall(rgx, fn))
```

    []



```python
rgx = re.compile('(?<=_)[A-Z]+(?=_)')
print(re.findall(rgx, fn))
```

    ['DE']



```python

```
