



## Linear Regression

### Model Assumptions

#### 1. Linearity Assumption

* Each predictor variable $x_{i}$ is linearly related to the outcome varibale $y$

* Use scatter Plot Matrix

```python
sns.pairplot(penguins_final)
```


#### 2. Normality Assumption
 the residuals/errors are normally distributed
    * To Quantile-Quantile (QQ) plot

3. **Independent Observation**: Each observation in the dataset is independent

4. **Homoscedasticity Assumption**: the variation of the residuals is constnt or similar across the model
    *  Looking for no clear pattern-- just scattered

> Note: Technical terms. *Residuals* are difference between predicted and observed values. *Errors* are natural noise in the model.

#### Regression Equation

$$
m = \frac{r \sigma(y)}{\sigma(x)}
$$


## Metrics

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