---
title: "Phone-number-search"
author: "Altair"
type: article
draft: false
--- 

```python
import re
```


```python
fh = open("sample_phone_book.txt")

for line in fh:
    if re.search(r"J.*Neu",line):
        print(line.rstrip())
        
    if re.search(r"a*Neu",line):
        print(line.rstrip())
fh.close()
```
