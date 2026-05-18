



## Linear Regression

### Model Assumptions

#### 1. Linearity Assumption

* Each predictor variable $x_{i}$ is linearly related to the outcome varibale $y$

* Use scatter Plot Matrix

```python
sns.pairplot(penguins_final)
```


#### 2. Normality Assumption
* the residuals/errors are normally distributed
* **Method 1**: Check for bell shape curve
* **Method 2**: Quantile-Quantile (QQ) plot seee [QQ Plot Jupyter Notebook](qq_plot.ipynb)

#### 3. Independent Observation
* Each observation in the dataset is independent

#### 4. Homoscedasticity Assumption
* the variation of the residuals is constnt or similar across the model
    *  Looking for no clear pattern-- just scattered

> Note: Technical terms. *Residuals* are difference between predicted and observed values. *Errors* are natural noise in the model.


Jupyter Notebook: [Link](Activity_Run%20simple%20linear%20regression.ipynb)



### Metrics

### Regression Equation

$$
m = \frac{r \sigma(y)}{\sigma(x)}
$$
### Pearson's correlation, r

* Range: $[-1,1]$
* Formula

$$
r = \frac{cov(X,Y)}{\sigma(x) \sigma(y)}
$$
* For each increase of one standard deviation in $X$, there is an expected increase of $r$ standard deviations in $Y$, on average over $X$



##### Covariance $cov$
* Represent the extent to which $X$ and $Y$ vary together from their respective means

$$
cov(X,Y) = \frac{\sum\limits_{i=1}^{n} (x_{i} - \overline{x}) (y_{i} - \overline{y})}{n}
$$


### P-values

For regression analsyis,
* $H_0: \beta = 0$ (Beta-Coefficent = 0)
* $H_1: \beta \neq 0$ (Beta Coefficent is not 0)


### $R^{2}$: Coefficient of Determination
* Measures the proportion of variation in the dependent variable, $Y$ explained by the independent variable(s), X

> Example. Suppose $R^{2} =0.734$. This means that about $73.4\%$ of the variance in the dependent variable can be explained by the independent vairables. The other $\approx 27\%$ cannot be explained by the model

**Formula**

$$
R^2 = 1- \frac{\sum (y_i - \hat{y}_i)^2 }{\sum (y_i -\overline{y})^{2} }
$$

* Sum of Squares Residuals: Difference between actual v alues and predicted values (Top)

* Total Sum of Squares: Difference between actual values and mean value (Bottom)

### MAE (Mean Absolute Error)
* Regression metric that measures magnitude of errors

$$
\frac{1}{n} \sum \vert y_i - \hat{y}_i \vert
$$


### MSE (Mean Squared Error)

*  w/r MAE, MSE is more sensitive to outliers
$$
\frac{1}{n} \sum (y_i - \hat{y}_i)^{2}
$$