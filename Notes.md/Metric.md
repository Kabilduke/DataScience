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

$$ TPR = \frac{TP}{TP + FN} $$

>> False Positive Rate

$$ FPR = \frac{FP}{FP + TN} $$



### AUC (Area Under the Curve):
```
from sklearn.metrics import auc
```

>Formula:

$$ AUC  = \frac{Recall + Sensitivity}{2} $$

## Specificity:

> Formula:

$$ Specificity = \frac{TN}{TN + FP} $$