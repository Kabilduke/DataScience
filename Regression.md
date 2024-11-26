### Linear Regression:
```
from sklearn.linear_model import LinearRegression 
```
- Supervised Learning algorithm
- Ex. Price Prediction(Regression), Classification(Cat 0r Dog)

> Formula:

$$ y = m.x+c $$

$$m(slope) = \frac{Rise}{Run}, \Rightarrow  \frac{y_2 - y_1}{x_2 - x_1}$$

$$ Multi points \Rightarrow \frac{\sum(x-x^{Mean)})(y - y^{Mean})}{\sum(x - x^{Mean})^2} $$

$$ c(intercept) = y^{Mean} + m x^{Mean} $$


### Multi-Linear Regression:
- Supervised Learning algorithm
- Ex. Price Prediction(Regression), Classification(Cat 0r Dog) with multiple features $^*$

> Formula:

$$ y = X.w + c $$

>>> - X = Matrix of $n * f$ (No. of Samples * No. of Features)

> Normal Equation $O(n^3)$:

>> Formula:

$$w(weights) = (X^TX)^{-1}X^Ty$$

> Least Squares Methods:

>> Formula:


### Logistic Regression
```
from sklearn.linear_model import LogisticRegression
```
- Supervised Learning algorithm
- Classification (Binomial, Multiclass, Ordinal)

> Formula:

$$Sigmoid(\sigma(y)) = \frac{1}{1+e^{-y}} $$


