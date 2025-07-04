### Normalization (Min Max):
```
from sklearn.preprocessing import MinMaxScaler
```
- Used to scale the features from range (0 to 1).
- KNN, K-Means, Linear & Logistic Regression, Gradient Decent.
  
Formula:

$$X_{norm} = \frac{X - X_{min}}{X_{max} -X_{min}}$$


### Standardisation (z- Score):
```
from sklearn.preprocessing import StandardScaler
```
- Used to scale down the feature based on standard normal distribution.
- KNN, K-Means, Linear & Logistic Regression, Gradient Decent.
  
Formula:

$$z = \frac{x - μ}{σ}$$

Where:
> Mean $(μ)$ = 0 \
> Standard deviation $(σ)$ = 1

$Note$:
- BatchNormalization is also used in neural network for increasing the training speed. 
