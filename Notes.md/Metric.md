> Note:

- True Positive = $a$(Yes) as $p$(Yes) 
- True Negative = $a$(No) as $p$(No) 
- False Positive = $a$(No) as $p$(Yes) 
- False Negative = $a$(Yes) as $p$(No) 

## Recall:
Recall is a metric that measures the proportion of positive cases that the model identified correctly.
-  Of predicted positives, how many are correct?

> Formula:

$$ Recall = \frac{TP}{TP + FP} $$

## Precision:
Precision is a similar metric to recall, but measures the proportion of predicted positive cases where the true label is actually positive.
- Of actual positives, how many are correctly identified?

> Formula:

$$ Precision = \frac{TP}{TP +FN} $$

## F1 Score
F1-score is an overall metric that combined recall and precision

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

## Sensitivity:

> Formula:

$$ Sensitivity = \frac{TP}{TP + FN} $$
