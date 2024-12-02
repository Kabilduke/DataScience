> Note:

- True Positive = $a$(Yes) as $p$(Yes) 
- True Negative = $a$(No) as $p$(No) 
- False Positive = $a$(No) as $p$(Yes) 
- False Negative = $a$(Yes) as $p$(No) 

## Recall:

> Formula:

$$ Recall = \frac{TP}{TP + FP} $$

## Precision:

> Formula:

$$ Precision = \frac{TP}{TP +FN} $$

## F1 Score

> Formula:

$$ f1 Score = 2 * \frac{Precision * Recall}{Precision + Recall} $$

## Accuracy:

> Formula:

$$ Accuracy = \frac{TP+ TN}{TP+ FP+ TN+ FN} $$


## ROC and AUC:
```
from sklearn.metrics import roc_curve
```
```
from sklear.metrics import roc_auc_score
```
- Calculated based on the threshold values.
- Used for Binary classification (Cancer prediction ...etc).

### ROC (Reciever-Operating Charactertic Curve):

> Formula:

>> True Positive Rate

$$ y \rightarrow TPR = \frac{TP}{TP + FN} $$

>> False Positive Rate

$$ x \rightarrow FPR = \frac{FP}{FP + TN} $$



### AUC (Area Under the Curve):
```
from sklearn.metrics import auc
```

- Used to measure the drug exposure, how much and how long the drug stayed in a body.
- Mathmetical method to calculate AUC - Trapeziodal rule

> Formula:

$$ AUC = \sum (x_{i+1} - x_i) * \frac{(y_i + y_{i+1})}{2} $$

## Specificity:

> Formula:

$$ Specificity = \frac{TN}{TN + FP} $$
