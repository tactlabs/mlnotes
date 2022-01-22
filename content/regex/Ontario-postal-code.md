---
title: "Ontario-postal-code"
author: "Altair"
type: article
draft: false
--- 

```python
import re
```


```python
names = ['M2N1H5', 'M2N 1H5', 'M882J8']

regex_patten = "^[A-Z]\d[A-Z]\s*\d[A-Z]\d"
# starts with Capital letter; it can have zero or one space

for name in names:
    m = re.match(regex_patten, name)

    if(m):
        #print(m.groups())
        print('matched : ', name)
```

    matched :  M2N1H5
    matched :  M2N 1H5



```python
# \d - digit
# \D - non-digit
# \s - whitespace
# \S - non-whitespace
# \w - alphanumeric
# \W - non-alphanumeric
```