---
title: "apply-function"
author: "Altair"
type: article
draft: false
--- 

```python
import pandas as pd
```


```python
data = {
    'city' : ['Toronto', 'Montreal', 'Waterloo', 'Toronto', 'Waterloo', 'Toronto', 'Toronto'],
    'points' : [80, 70, 90, 85, 79, 82, 200]
}
```


```python
data
```




    {'city': ['Toronto',
      'Montreal',
      'Waterloo',
      'Toronto',
      'Waterloo',
      'Toronto',
      'Toronto'],
     'points': [80, 70, 90, 85, 79, 82, 200]}




```python
type(data)
```




    dict




```python
df = pd.DataFrame(data)
```


```python
df.groupby('city')['points'].apply(lambda x:x.rolling(window=1).mean())
```




    0     80.0
    1     70.0
    2     90.0
    3     85.0
    4     79.0
    5     82.0
    6    200.0
    Name: points, dtype: float64




```python
df.groupby('city')['points'].apply(lambda x:x.rolling(window=2).mean())
```




    0      NaN
    1      NaN
    2      NaN
    3     82.5
    4     84.5
    5     83.5
    6    141.0
    Name: points, dtype: float64




```python

```
