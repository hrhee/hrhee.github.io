---
layout: post
title:  "Bars and Stripes"
date:   2020-11-01 11:42:23 +0100
categories: jekyll update
---

$$
\begin{equation*}
P(A\mid B) \; = \; \frac {P(B\mid A) \cdot P(A)} {P(B)}
\end{equation*}
$$

```python
import numpy as np
import matplotlib.pyplot as plt

%matplotlib inline
```


```python
# bars and stripes

horizontal_stripes =[
    np.array([[1, 1, 1, 1], [0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0]]),
    np.array([[0, 0, 0, 0], [1, 1, 1, 1], [0, 0, 0, 0], [0, 0, 0, 0]]),
    np.array([[0, 0, 0, 0], [0, 0, 0, 0], [1, 1, 1, 1], [0, 0, 0, 0]]),
    np.array([[0, 0, 0, 0], [0, 0, 0, 0], [0, 0, 0, 0], [1, 1, 1, 1]]),
    np.array([[1, 1, 1, 1], [1, 1, 1, 1], [0, 0, 0, 0], [0, 0, 0, 0]]),
    np.array([[0, 0, 0, 0], [1, 1, 1, 1], [1, 1, 1, 1], [0, 0, 0, 0]]),
    np.array([[0, 0, 0, 0], [0, 0, 0, 0], [1, 1, 1, 1], [1, 1, 1, 1]]),
    np.array([[1, 1, 1, 1], [0, 0, 0, 0], [1, 1, 1, 1], [0, 0, 0, 0]]),
    np.array([[0, 0, 0, 0], [1, 1, 1, 1], [0, 0, 0, 0], [1, 1, 1, 1]]),
    np.array([[1, 1, 1, 1], [0, 0, 0, 0], [0, 0, 0, 0], [1, 1, 1, 1]]),
    np.array([[1, 1, 1, 1], [0, 0, 0, 0], [1, 1, 1, 1], [1, 1, 1, 1]]),
    np.array([[1, 1, 1, 1], [1, 1, 1, 1], [0, 0, 0, 0], [1, 1, 1, 1]]),
    np.array([[1, 1, 1, 1], [1, 1, 1, 1], [1, 1, 1, 1], [0, 0, 0, 0]]),
    np.array([[0, 0, 0, 0], [1, 1, 1, 1], [1, 1, 1, 1], [1, 1, 1, 1]]),
]

vertical_stripes = [np.transpose(A) for A in horizontal_stripes]

bars_and_stripes = [
    #np.zeros((4,4)),
    *horizontal_stripes,
    *vertical_stripes,
    #np.ones((4,4)),
]

labels = [0]*14 + [1]*14

```


```python
plt.figure(figsize=(10, 12))

for i in range(len(bars_and_stripes)):
    plt.subplot(6,5,i+1)
    plt.axis('off')
    plt.imshow(bars_and_stripes[i], vmin=0,vmax=1)
```


![png](/images/output_3_0.png)



```python

```
