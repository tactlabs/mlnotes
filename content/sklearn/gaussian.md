---
title: "gaussian"
author: "Altair"
type: article
draft: false
--- 

```python
from sklearn.naive_bayes import GaussianNB
import numpy as np
```


```python
#assigning predictor and target variables
x= np.array([[-3,7],[1,5], [1,2], [-2,0], [2,3], [-4,0], [-1,1], [1,1], [-2,2], [2,7], [-4,1], [-2,7]])
y = np.array([3, 3, 3, 3, 4, 3, 3, 4, 3, 4, 4, 4])
```


```python
#Create a Gaussian Classifier
model = GaussianNB()
```


```python
# Train the model using the training sets 
model.fit(x, y)
```




    GaussianNB()




```python
#Predict Output 
predicted= model.predict([[1,2],[3,4]])
print(predicted)
```

    [3 4]



```python

```
