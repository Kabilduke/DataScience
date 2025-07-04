## Regularization:
```py
from tensorflow.keras import regularizers
```
Overfitting:
Higher accuracy in training, but low accuracy in testing.
To reduce overfitting by penalization larger weights. Two types of regularization.
- LASSO(l1)
- Ridge(l2)

### L1-Regularization (LASSO)
```py
kernel_regularizer = regularizers.l1(0.01)
bias_regularizer = regularizers.l1(0.01)
activity_regularizer = regularizers.l1(0.01)
```
> Formula

- Adds absolute value to weights to the loss.
- Sparse model some value become zero's.

### L2-Regularization (Ridge)
```py
kernel_regularizer = regularizers.l2(0.01)
bias_regularizer = regularizers.l2(0.01)
activity_regularizer = regularizers.l2(0.01)
```
> Formula

- Encourages smaller weights, but doesn't zero them out!




$Extras:$
- L2 is most commmonly used in deep learning.
- Dropout layers is also used for reducing overfitting.
