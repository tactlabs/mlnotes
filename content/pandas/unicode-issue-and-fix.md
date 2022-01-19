---
title: "unicode-issue-and-fix"
author: "Altair"
type: article
draft: false
--- 

```python
import numpy as np
import pandas as pd
```


```python
df = pd.read_csv('score.csv')
```


    ---------------------------------------------------------------------------

    UnicodeDecodeError                        Traceback (most recent call last)

    Input In [4], in <module>
    ----> 1 df = pd.read_csv('score.csv')


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/util/_decorators.py:311, in deprecate_nonkeyword_arguments.<locals>.decorate.<locals>.wrapper(*args, **kwargs)
        305 if len(args) > num_allow_args:
        306     warnings.warn(
        307         msg.format(arguments=arguments),
        308         FutureWarning,
        309         stacklevel=stacklevel,
        310     )
    --> 311 return func(*args, **kwargs)


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/io/parsers/readers.py:586, in read_csv(filepath_or_buffer, sep, delimiter, header, names, index_col, usecols, squeeze, prefix, mangle_dupe_cols, dtype, engine, converters, true_values, false_values, skipinitialspace, skiprows, skipfooter, nrows, na_values, keep_default_na, na_filter, verbose, skip_blank_lines, parse_dates, infer_datetime_format, keep_date_col, date_parser, dayfirst, cache_dates, iterator, chunksize, compression, thousands, decimal, lineterminator, quotechar, quoting, doublequote, escapechar, comment, encoding, encoding_errors, dialect, error_bad_lines, warn_bad_lines, on_bad_lines, delim_whitespace, low_memory, memory_map, float_precision, storage_options)
        571 kwds_defaults = _refine_defaults_read(
        572     dialect,
        573     delimiter,
       (...)
        582     defaults={"delimiter": ","},
        583 )
        584 kwds.update(kwds_defaults)
    --> 586 return _read(filepath_or_buffer, kwds)


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/io/parsers/readers.py:482, in _read(filepath_or_buffer, kwds)
        479 _validate_names(kwds.get("names", None))
        481 # Create the parser.
    --> 482 parser = TextFileReader(filepath_or_buffer, **kwds)
        484 if chunksize or iterator:
        485     return parser


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/io/parsers/readers.py:811, in TextFileReader.__init__(self, f, engine, **kwds)
        808 if "has_index_names" in kwds:
        809     self.options["has_index_names"] = kwds["has_index_names"]
    --> 811 self._engine = self._make_engine(self.engine)


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/io/parsers/readers.py:1040, in TextFileReader._make_engine(self, engine)
       1036     raise ValueError(
       1037         f"Unknown engine: {engine} (valid options are {mapping.keys()})"
       1038     )
       1039 # error: Too many arguments for "ParserBase"
    -> 1040 return mapping[engine](self.f, **self.options)


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/io/parsers/c_parser_wrapper.py:69, in CParserWrapper.__init__(self, src, **kwds)
         67 kwds["dtype"] = ensure_dtype_objs(kwds.get("dtype", None))
         68 try:
    ---> 69     self._reader = parsers.TextReader(self.handles.handle, **kwds)
         70 except Exception:
         71     self.handles.close()


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/_libs/parsers.pyx:542, in pandas._libs.parsers.TextReader.__cinit__()


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/_libs/parsers.pyx:642, in pandas._libs.parsers.TextReader._get_header()


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/_libs/parsers.pyx:843, in pandas._libs.parsers.TextReader._tokenize_rows()


    File ~/miniconda3/envs/py38/lib/python3.8/site-packages/pandas/_libs/parsers.pyx:1917, in pandas._libs.parsers.raise_parser_error()


    UnicodeDecodeError: 'utf-8' codec can't decode byte 0xff in position 0: invalid start byte



```python
# You can see the above message saying that the utf-8 can't decode the current entries. We can try with ISO
```


```python
df = pd.read_csv('score.csv', encoding = 'ISO-8859-1')
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
      <th>ÿþs</th>
      <th>Unnamed: 1</th>
      <th>Unnamed: 2</th>
      <th>Unnamed: 3</th>
      <th>Unnamed: 4</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>5</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>6</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>7</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>8</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>9</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>11</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>12</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>13</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>14</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>15</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
