---
title: "Random-Integer-with-2-dimension"
author: "Altair"
type: article
draft: false
--- 

```python
import numpy as np
import pandas as pd
```


```python
# Create Random integer between 1 to 100

df = pd.DataFrame(np.random.randint(0, 100, size=(2, 4)), columns=['A', 'B', 'C', 'D'])

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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>63</td>
      <td>44</td>
      <td>76</td>
      <td>35</td>
    </tr>
    <tr>
      <th>1</th>
      <td>97</td>
      <td>20</td>
      <td>75</td>
      <td>45</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.shape
```




    (2, 4)




```python
df.describe()
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
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>80.000000</td>
      <td>32.000000</td>
      <td>75.500000</td>
      <td>40.000000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>24.041631</td>
      <td>16.970563</td>
      <td>0.707107</td>
      <td>7.071068</td>
    </tr>
    <tr>
      <th>min</th>
      <td>63.000000</td>
      <td>20.000000</td>
      <td>75.000000</td>
      <td>35.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>71.500000</td>
      <td>26.000000</td>
      <td>75.250000</td>
      <td>37.500000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>80.000000</td>
      <td>32.000000</td>
      <td>75.500000</td>
      <td>40.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>88.500000</td>
      <td>38.000000</td>
      <td>75.750000</td>
      <td>42.500000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>97.000000</td>
      <td>44.000000</td>
      <td>76.000000</td>
      <td>45.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.ndim
```




    2




```python

```
