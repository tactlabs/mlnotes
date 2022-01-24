---
title: "datatype-downcasting"
author: "Altair"
type: article
draft: false
--- 

```python
import numpy as np
import pandas as pd
```


```python
ds = pd.Series([1, np.nan, 3, 4, 5])
```


```python
ds
```




    0    1.0
    1    NaN
    2    3.0
    3    4.0
    4    5.0
    dtype: float64




```python
# ds = ds.astype('int') # will throw ValueError: Cannot convert non-finite values (NA or inf) to integer
```


```python
ds = ds.astype('float')
```


```python
ds
```




    0    1.0
    1    NaN
    2    3.0
    3    4.0
    4    5.0
    dtype: float64




```python
ds = pd.to_numeric(ds, downcast='float')

```


```python
ds
```




    0    1.0
    1    NaN
    2    3.0
    3    4.0
    4    5.0
    dtype: float32




```python
# You could see the dtype chagend fro float64 to float32
```


```python

```