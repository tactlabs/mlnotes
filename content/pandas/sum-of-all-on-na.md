---
title: "sum-of-all-on-na"
author: "Altair"
type: article
draft: false
--- 

```python
import numpy as np
import pandas as pd

```


```python
df = pd.DataFrame(np.random.rand(10, 5))
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
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.745024</td>
      <td>0.337881</td>
      <td>0.878525</td>
      <td>0.977308</td>
      <td>0.637737</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.704736</td>
      <td>0.147799</td>
      <td>0.726641</td>
      <td>0.370102</td>
      <td>0.710152</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.329028</td>
      <td>0.292563</td>
      <td>0.585587</td>
      <td>0.357806</td>
      <td>0.555402</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.363512</td>
      <td>0.710388</td>
      <td>0.287427</td>
      <td>0.976869</td>
      <td>0.599735</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.121242</td>
      <td>0.703394</td>
      <td>0.517529</td>
      <td>0.511438</td>
      <td>0.404470</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.685596</td>
      <td>0.896357</td>
      <td>0.384521</td>
      <td>0.263929</td>
      <td>0.851880</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0.020535</td>
      <td>0.956360</td>
      <td>0.160158</td>
      <td>0.593874</td>
      <td>0.326570</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0.165147</td>
      <td>0.888129</td>
      <td>0.201117</td>
      <td>0.062753</td>
      <td>0.551937</td>
    </tr>
    <tr>
      <th>8</th>
      <td>0.555566</td>
      <td>0.620956</td>
      <td>0.633912</td>
      <td>0.822068</td>
      <td>0.184850</td>
    </tr>
    <tr>
      <th>9</th>
      <td>0.138221</td>
      <td>0.009944</td>
      <td>0.063153</td>
      <td>0.657260</td>
      <td>0.050153</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Apply some NA on the existing DF

df.iloc[0:3, 0:4] = np.nan
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
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.637737</td>
    </tr>
    <tr>
      <th>1</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.710152</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.555402</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.363512</td>
      <td>0.710388</td>
      <td>0.287427</td>
      <td>0.976869</td>
      <td>0.599735</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.121242</td>
      <td>0.703394</td>
      <td>0.517529</td>
      <td>0.511438</td>
      <td>0.404470</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.685596</td>
      <td>0.896357</td>
      <td>0.384521</td>
      <td>0.263929</td>
      <td>0.851880</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0.020535</td>
      <td>0.956360</td>
      <td>0.160158</td>
      <td>0.593874</td>
      <td>0.326570</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0.165147</td>
      <td>0.888129</td>
      <td>0.201117</td>
      <td>0.062753</td>
      <td>0.551937</td>
    </tr>
    <tr>
      <th>8</th>
      <td>0.555566</td>
      <td>0.620956</td>
      <td>0.633912</td>
      <td>0.822068</td>
      <td>0.184850</td>
    </tr>
    <tr>
      <th>9</th>
      <td>0.138221</td>
      <td>0.009944</td>
      <td>0.063153</td>
      <td>0.657260</td>
      <td>0.050153</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.loc[:, 'test'] = df.iloc[:, 2:].sum(axis=1)
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
      <th>0</th>
      <th>1</th>
      <th>2</th>
      <th>3</th>
      <th>4</th>
      <th>test</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.637737</td>
      <td>0.637737</td>
    </tr>
    <tr>
      <th>1</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.710152</td>
      <td>0.710152</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.555402</td>
      <td>0.555402</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.363512</td>
      <td>0.710388</td>
      <td>0.287427</td>
      <td>0.976869</td>
      <td>0.599735</td>
      <td>1.864032</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.121242</td>
      <td>0.703394</td>
      <td>0.517529</td>
      <td>0.511438</td>
      <td>0.404470</td>
      <td>1.433437</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.685596</td>
      <td>0.896357</td>
      <td>0.384521</td>
      <td>0.263929</td>
      <td>0.851880</td>
      <td>1.500330</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0.020535</td>
      <td>0.956360</td>
      <td>0.160158</td>
      <td>0.593874</td>
      <td>0.326570</td>
      <td>1.080602</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0.165147</td>
      <td>0.888129</td>
      <td>0.201117</td>
      <td>0.062753</td>
      <td>0.551937</td>
      <td>0.815807</td>
    </tr>
    <tr>
      <th>8</th>
      <td>0.555566</td>
      <td>0.620956</td>
      <td>0.633912</td>
      <td>0.822068</td>
      <td>0.184850</td>
      <td>1.640830</td>
    </tr>
    <tr>
      <th>9</th>
      <td>0.138221</td>
      <td>0.009944</td>
      <td>0.063153</td>
      <td>0.657260</td>
      <td>0.050153</td>
      <td>0.770566</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
