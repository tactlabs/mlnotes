---
title: "pandas-with-random-int"
author: "Altair"
type: article
draft: false
--- 

```python
import numpy as np
import pandas as pd
```


```python
df = pd.DataFrame(np.random.randint(0, 100, size=(3, 2)), columns=list('xy'))
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
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16</td>
      <td>52</td>
    </tr>
    <tr>
      <th>1</th>
      <td>30</td>
      <td>84</td>
    </tr>
    <tr>
      <th>2</th>
      <td>65</td>
      <td>43</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
