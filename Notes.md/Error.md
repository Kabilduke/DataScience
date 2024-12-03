### Mean Absolute Error (MAE)
$MAE$ is better when all errors should be treated equally (e.g., assessing delivery time errors).

> Formula:

$$ MAE = \frac{1}{n} \sum |y_i - y^p_i| $$

 - $y_i$ = Actual value
 - $y^P$ = Predicted Value

### Mean Square Error (MSE)
$MSE$ is preferred when you want to penalize larger errors significantly (e.g., financial forecasting).
> Formula:

$$ MSE = \frac{1}{n} \sum (y_i - y^p_i)^2 $$

### Root Mean Squared Error (RMSE)
> Formula:

$$ RMSE = \sqrt{MSR} $$

### R-Square
> Formula:

$$ R^2 = 1 - \frac{\sum(y_i - y^p_i)^2}{\sum(y_i - Y_i)} \quad ,(0 - 1) $$

- $Y_i$ = Mean of Actual value


Reference : [Microsoft Learn](https://learn.microsoft.com/en-us/training/modules/fundamentals-machine-learning/4-regression)
