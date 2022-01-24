---
title: "index-isin"
author: "Altair"
type: article
draft: false
--- 

```python
import numpy as np
import pandas as pd

```


```python
df = pd.DataFrame({
    'maths' : [80, 89, 90, 20, 60],
    'science' : [40, 50, 90, 100, 50],
    'language' : [20, 30, 90, 95, 40]
})

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
      <th>language</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>80</td>
      <td>40</td>
      <td>20</td>
    </tr>
    <tr>
      <th>1</th>
      <td>89</td>
      <td>50</td>
      <td>30</td>
    </tr>
    <tr>
      <th>2</th>
      <td>90</td>
      <td>90</td>
      <td>90</td>
    </tr>
    <tr>
      <th>3</th>
      <td>20</td>
      <td>100</td>
      <td>95</td>
    </tr>
    <tr>
      <th>4</th>
      <td>60</td>
      <td>50</td>
      <td>40</td>
    </tr>
  </tbody>
</table>
</div>




```python
df[df.index.isin([1, 2, 4])]
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
      <th>language</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>89</td>
      <td>50</td>
      <td>30</td>
    </tr>
    <tr>
      <th>2</th>
      <td>90</td>
      <td>90</td>
      <td>90</td>
    </tr>
    <tr>
      <th>4</th>
      <td>60</td>
      <td>50</td>
      <td>40</td>
    </tr>
  </tbody>
</table>
</div>




```python

```