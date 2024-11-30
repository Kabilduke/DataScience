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

$$ TPR = \frac{TP}{TP + FN} $$

$$ FPR = \frac{FP}{FP + TN} $$



### AUC (Area Under the Curve):

> Diagram: