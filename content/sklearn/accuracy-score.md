---
title: "accuracy-score"
author: "Altair"
type: article
draft: false
--- 

```python
import numpy as np
from sklearn.metrics import accuracy_score
```


```python
y_pred = [0, 2, 1, 3]
y_true = [0, 1, 2, 3]
score1 = accuracy_score(y_true, y_pred)    
print(score1)
```

    0.5



```python
score2 = accuracy_score(y_true, y_pred, normalize=False)
print(score2)
```

    2

