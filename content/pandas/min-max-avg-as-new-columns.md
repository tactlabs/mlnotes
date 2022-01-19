---
title: "min-max-avg-as-new-columns"
author: "Altair"
type: article
draft: false
--- 

```python
import numpy as np
import pandas as pd
```


```python
df = pd.read_csv('abc.csv')
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
      <th>student</th>
      <th>language</th>
      <th>science</th>
      <th>maths</th>
      <th>history</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>kumar</td>
      <td>90</td>
      <td>56</td>
      <td>34</td>
      <td>34</td>
    </tr>
    <tr>
      <th>1</th>
      <td>kevin</td>
      <td>10</td>
      <td>34</td>
      <td>32</td>
      <td>67</td>
    </tr>
    <tr>
      <th>2</th>
      <td>sammy</td>
      <td>90</td>
      <td>23</td>
      <td>12</td>
      <td>32</td>
    </tr>
    <tr>
      <th>3</th>
      <td>janice</td>
      <td>20</td>
      <td>67</td>
      <td>90</td>
      <td>45</td>
    </tr>
    <tr>
      <th>4</th>
      <td>peter</td>
      <td>30</td>
      <td>56</td>
      <td>45</td>
      <td>65</td>
    </tr>
    <tr>
      <th>5</th>
      <td>prem</td>
      <td>90</td>
      <td>45</td>
      <td>45</td>
      <td>34</td>
    </tr>
    <tr>
      <th>6</th>
      <td>carrol</td>
      <td>50</td>
      <td>90</td>
      <td>45</td>
      <td>23</td>
    </tr>
  </tbody>
</table>
</div>




```python
df['min'] = df.min(axis=1)
```

    /tmp/ipykernel_22227/534050012.py:1: FutureWarning: Dropping of nuisance columns in DataFrame reductions (with 'numeric_only=None') is deprecated; in a future version this will raise TypeError.  Select only valid columns before calling the reduction.
      df['min'] = df.min(axis=1)



```python
df['max'] = df.max(axis=1)
```

    /tmp/ipykernel_22227/3177767216.py:1: FutureWarning: Dropping of nuisance columns in DataFrame reductions (with 'numeric_only=None') is deprecated; in a future version this will raise TypeError.  Select only valid columns before calling the reduction.
      df['max'] = df.max(axis=1)



```python
df['avg'] = df.mean(axis=1)
```

    /tmp/ipykernel_22227/2916772895.py:1: FutureWarning: Dropping of nuisance columns in DataFrame reductions (with 'numeric_only=None') is deprecated; in a future version this will raise TypeError.  Select only valid columns before calling the reduction.
      df['avg'] = df.mean(axis=1)



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
      <th>student</th>
      <th>language</th>
      <th>science</th>
      <th>maths</th>
      <th>history</th>
      <th>min</th>
      <th>max</th>
      <th>avg</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>kumar</td>
      <td>90</td>
      <td>56</td>
      <td>34</td>
      <td>34</td>
      <td>34</td>
      <td>90</td>
      <td>56.333333</td>
    </tr>
    <tr>
      <th>1</th>
      <td>kevin</td>
      <td>10</td>
      <td>34</td>
      <td>32</td>
      <td>67</td>
      <td>10</td>
      <td>67</td>
      <td>36.666667</td>
    </tr>
    <tr>
      <th>2</th>
      <td>sammy</td>
      <td>90</td>
      <td>23</td>
      <td>12</td>
      <td>32</td>
      <td>12</td>
      <td>90</td>
      <td>43.166667</td>
    </tr>
    <tr>
      <th>3</th>
      <td>janice</td>
      <td>20</td>
      <td>67</td>
      <td>90</td>
      <td>45</td>
      <td>20</td>
      <td>90</td>
      <td>55.333333</td>
    </tr>
    <tr>
      <th>4</th>
      <td>peter</td>
      <td>30</td>
      <td>56</td>
      <td>45</td>
      <td>65</td>
      <td>30</td>
      <td>65</td>
      <td>48.500000</td>
    </tr>
    <tr>
      <th>5</th>
      <td>prem</td>
      <td>90</td>
      <td>45</td>
      <td>45</td>
      <td>34</td>
      <td>34</td>
      <td>90</td>
      <td>56.333333</td>
    </tr>
    <tr>
      <th>6</th>
      <td>carrol</td>
      <td>50</td>
      <td>90</td>
      <td>45</td>
      <td>23</td>
      <td>23</td>
      <td>90</td>
      <td>53.500000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df['avg_int'] = df.mean(axis=1).astype(int)
```

    /tmp/ipykernel_22227/469872405.py:1: FutureWarning: Dropping of nuisance columns in DataFrame reductions (with 'numeric_only=None') is deprecated; in a future version this will raise TypeError.  Select only valid columns before calling the reduction.
      df['avg_int'] = df.mean(axis=1).astype(int)



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
      <th>student</th>
      <th>language</th>
      <th>science</th>
      <th>maths</th>
      <th>history</th>
      <th>min</th>
      <th>max</th>
      <th>avg</th>
      <th>avg_int</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>kumar</td>
      <td>90</td>
      <td>56</td>
      <td>34</td>
      <td>34</td>
      <td>34</td>
      <td>90</td>
      <td>56.333333</td>
      <td>56</td>
    </tr>
    <tr>
      <th>1</th>
      <td>kevin</td>
      <td>10</td>
      <td>34</td>
      <td>32</td>
      <td>67</td>
      <td>10</td>
      <td>67</td>
      <td>36.666667</td>
      <td>36</td>
    </tr>
    <tr>
      <th>2</th>
      <td>sammy</td>
      <td>90</td>
      <td>23</td>
      <td>12</td>
      <td>32</td>
      <td>12</td>
      <td>90</td>
      <td>43.166667</td>
      <td>43</td>
    </tr>
    <tr>
      <th>3</th>
      <td>janice</td>
      <td>20</td>
      <td>67</td>
      <td>90</td>
      <td>45</td>
      <td>20</td>
      <td>90</td>
      <td>55.333333</td>
      <td>55</td>
    </tr>
    <tr>
      <th>4</th>
      <td>peter</td>
      <td>30</td>
      <td>56</td>
      <td>45</td>
      <td>65</td>
      <td>30</td>
      <td>65</td>
      <td>48.500000</td>
      <td>48</td>
    </tr>
    <tr>
      <th>5</th>
      <td>prem</td>
      <td>90</td>
      <td>45</td>
      <td>45</td>
      <td>34</td>
      <td>34</td>
      <td>90</td>
      <td>56.333333</td>
      <td>56</td>
    </tr>
    <tr>
      <th>6</th>
      <td>carrol</td>
      <td>50</td>
      <td>90</td>
      <td>45</td>
      <td>23</td>
      <td>23</td>
      <td>90</td>
      <td>53.500000</td>
      <td>53</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
