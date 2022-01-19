---
title: "pandas-version"
author: "Altair"
type: article
draft: false
--- 

```python
import pandas as pd
```


```python
pd.__version__
```




    '1.3.5'




```python
pd.show_versions(as_json=False)
```

    
    INSTALLED VERSIONS
    ------------------
    commit           : 66e3805b8cabe977f40c05259cc3fcf7ead5687d
    python           : 3.8.12.final.0
    python-bits      : 64
    OS               : Linux
    OS-release       : 5.13.0-25-generic
    Version          : #26~20.04.1-Ubuntu SMP Fri Jan 7 16:27:40 UTC 2022
    machine          : x86_64
    processor        : x86_64
    byteorder        : little
    LC_ALL           : None
    LANG             : en_IN
    LOCALE           : en_IN.ISO8859-1
    
    pandas           : 1.3.5
    numpy            : 1.22.1
    pytz             : 2021.3
    dateutil         : 2.8.2
    pip              : 21.2.4
    setuptools       : 58.0.4
    Cython           : None
    pytest           : None
    hypothesis       : None
    sphinx           : None
    blosc            : None
    feather          : None
    xlsxwriter       : None
    lxml.etree       : None
    html5lib         : None
    pymysql          : None
    psycopg2         : None
    jinja2           : 3.0.3
    IPython          : 8.0.0
    pandas_datareader: None
    bs4              : None
    bottleneck       : None
    fsspec           : None
    fastparquet      : None
    gcsfs            : None
    matplotlib       : None
    numexpr          : None
    odfpy            : None
    openpyxl         : 3.0.9
    pandas_gbq       : None
    pyarrow          : None
    pyxlsb           : None
    s3fs             : None
    scipy            : None
    sqlalchemy       : None
    tables           : None
    tabulate         : None
    xarray           : None
    xlrd             : 2.0.1
    xlwt             : None
    numba            : None



```python
pd.show_versions(as_json=True)
```

    {
      "system": {
        "commit": "66e3805b8cabe977f40c05259cc3fcf7ead5687d",
        "python": "3.8.12.final.0",
        "python-bits": 64,
        "OS": "Linux",
        "OS-release": "5.13.0-25-generic",
        "Version": "#26~20.04.1-Ubuntu SMP Fri Jan 7 16:27:40 UTC 2022",
        "machine": "x86_64",
        "processor": "x86_64",
        "byteorder": "little",
        "LC_ALL": null,
        "LANG": "en_IN",
        "LOCALE": {
          "language-code": "en_IN",
          "encoding": "ISO8859-1"
        }
      },
      "dependencies": {
        "pandas": "1.3.5",
        "numpy": "1.22.1",
        "pytz": "2021.3",
        "dateutil": "2.8.2",
        "pip": "21.2.4",
        "setuptools": "58.0.4",
        "Cython": null,
        "pytest": null,
        "hypothesis": null,
        "sphinx": null,
        "blosc": null,
        "feather": null,
        "xlsxwriter": null,
        "lxml.etree": null,
        "html5lib": null,
        "pymysql": null,
        "psycopg2": null,
        "jinja2": "3.0.3",
        "IPython": "8.0.0",
        "pandas_datareader": null,
        "bs4": null,
        "bottleneck": null,
        "fsspec": null,
        "fastparquet": null,
        "gcsfs": null,
        "matplotlib": null,
        "numexpr": null,
        "odfpy": null,
        "openpyxl": "3.0.9",
        "pandas_gbq": null,
        "pyarrow": null,
        "pyxlsb": null,
        "s3fs": null,
        "scipy": null,
        "sqlalchemy": null,
        "tables": null,
        "tabulate": null,
        "xarray": null,
        "xlrd": "2.0.1",
        "xlwt": null,
        "numba": null
      }
    }


```python
import pprint
```


```python
pprint.pprint(pd.show_versions(as_json=True))
```

    {
      "system": {
        "commit": "66e3805b8cabe977f40c05259cc3fcf7ead5687d",
        "python": "3.8.12.final.0",
        "python-bits": 64,
        "OS": "Linux",
        "OS-release": "5.13.0-25-generic",
        "Version": "#26~20.04.1-Ubuntu SMP Fri Jan 7 16:27:40 UTC 2022",
        "machine": "x86_64",
        "processor": "x86_64",
        "byteorder": "little",
        "LC_ALL": null,
        "LANG": "en_IN",
        "LOCALE": {
          "language-code": "en_IN",
          "encoding": "ISO8859-1"
        }
      },
      "dependencies": {
        "pandas": "1.3.5",
        "numpy": "1.22.1",
        "pytz": "2021.3",
        "dateutil": "2.8.2",
        "pip": "21.2.4",
        "setuptools": "58.0.4",
        "Cython": null,
        "pytest": null,
        "hypothesis": null,
        "sphinx": null,
        "blosc": null,
        "feather": null,
        "xlsxwriter": null,
        "lxml.etree": null,
        "html5lib": null,
        "pymysql": null,
        "psycopg2": null,
        "jinja2": "3.0.3",
        "IPython": "8.0.0",
        "pandas_datareader": null,
        "bs4": null,
        "bottleneck": null,
        "fsspec": null,
        "fastparquet": null,
        "gcsfs": null,
        "matplotlib": null,
        "numexpr": null,
        "odfpy": null,
        "openpyxl": "3.0.9",
        "pandas_gbq": null,
        "pyarrow": null,
        "pyxlsb": null,
        "s3fs": null,
        "scipy": null,
        "sqlalchemy": null,
        "tables": null,
        "tabulate": null,
        "xarray": null,
        "xlrd": "2.0.1",
        "xlwt": null,
        "numba": null
      }
    }None



```python

```
