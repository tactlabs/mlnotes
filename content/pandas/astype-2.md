---
title: "astype-2"
author: "Altair"
type: article
draft: false
--- 

```python
import numpy as np
import pandas as pd

```


```python
marks = [
    [90, 87],
    [90, 95],
    [92, 95]
]

```


```python
marks
```




    [[90, 87], [90, 95], [92, 95]]




```python
df = pd.DataFrame(marks, columns=['maths', 'science'])
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>maths</th>
      <th>science</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>90</td>
      <td>87</td>
    </tr>
    <tr>
      <th>1</th>
      <td>90</td>
      <td>95</td>
    </tr>
    <tr>
      <th>2</th>
      <td>92</td>
      <td>95</td>
    </tr>
  </tbody>
</table>
</div>




```python
# reassign some values to nan

df['maths']
```




    0    90
    1    90
    2    92
    Name: maths, dtype: int64




```python
df['maths'][0] = np.nan
```


```python
df['maths']
```




    0     NaN
    1    90.0
    2    92.0
    Name: maths, dtype: float64




```python
df = df.astype('int') # this will throw error
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    /tmp/ipykernel_5492/3439763043.py in <module>
    ----> 1 df = df.astype('int') # this will throw error
    

    ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/core/generic.py in astype(self, dtype, copy, errors)
       5696         else:
       5697             # else, only a single dtype is given
    -> 5698             new_data = self._data.astype(dtype=dtype, copy=copy, errors=errors)
       5699             return self._constructor(new_data).__finalize__(self)
       5700 


    ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/core/internals/managers.py in astype(self, dtype, copy, errors)
        580 
        581     def astype(self, dtype, copy: bool = False, errors: str = "raise"):
    --> 582         return self.apply("astype", dtype=dtype, copy=copy, errors=errors)
        583 
        584     def convert(self, **kwargs):


    ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/core/internals/managers.py in apply(self, f, filter, **kwargs)
        440                 applied = b.apply(f, **kwargs)
        441             else:
    --> 442                 applied = getattr(b, f)(**kwargs)
        443             result_blocks = _extend_blocks(applied, result_blocks)
        444 


    ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/core/internals/blocks.py in astype(self, dtype, copy, errors)
        623             vals1d = values.ravel()
        624             try:
    --> 625                 values = astype_nansafe(vals1d, dtype, copy=True)
        626             except (ValueError, TypeError):
        627                 # e.g. astype_nansafe can fail on object-dtype of strings


    ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/core/dtypes/cast.py in astype_nansafe(arr, dtype, copy, skipna)
        866 
        867         if not np.isfinite(arr).all():
    --> 868             raise ValueError("Cannot convert non-finite values (NA or inf) to integer")
        869 
        870     elif is_object_dtype(arr):


    ValueError: Cannot convert non-finite values (NA or inf) to integer



```python
df = df.fillna(0).astype('int') # this will throw error
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>maths</th>
      <th>science</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>87</td>
    </tr>
    <tr>
      <th>1</th>
      <td>90</td>
      <td>95</td>
    </tr>
    <tr>
      <th>2</th>
      <td>92</td>
      <td>95</td>
    </tr>
  </tbody>
</table>
</div>




```python

```


```python

```
