



## Linear Regression

### Model Assumptions

#### 1. Linearity Assumption

* Each predictor variable $x_{i}$ is linearly related to the outcome varibale $y$

* Use scatter Plot Matrix

```python
sns.pairplot(penguins_final)
```


2. **Normality Assumption**: the residuals/errors are normally distributed
    * To Quantile-Quantile (QQ) plot

3. **Independent Observation**: Each observation in the dataset is independent

4. **Homoscedasticity Assumption**: the variation of the residuals is constnt or similar across the model

 > Looking for no clear pattern-- just scattered


