# Regression Problems

- Regression analysis is a set of statistical processes for estimating the relationships between a dependent variable (often called the 'outcome variable', y) and one or more independent variables (often called 'predictors', 'covariates', or 'features', X)<br> 

- A regression problem is when the output variable is a real or continuous value, such as “salary” or “weight”.


> Given the number of bedrooms, bathrooms, house location and/or more, predict the sale price of a given house.
>
> ------------------------------------------------------------------------------------------------------------------------------------------------
>
> How much will bitcoin be worth tomorrow?

    - Which of the following is a regression task?
      - Predicting age of a person?
      - Predicting nationality of a person?
      - Predicting whether stock price of a company will increase tomorrow?
      - Predicting whether a document is related to sighting of UFOs?
    
    Answer: predicting age of a person, because it is a real value.
    Predicting nationality is categorical, whether stock price will increase is discrete (yes/no answer), 
    predicting whether a document is related to UFO is again discrete (yes/no answer).

A continuous output variable is a real-value, such as an integer or floating point value. These are often quantities, such as amounts and sizes.

For example, a house may be predicted to sell for a specific dollar value, perhaps in the range of $100,000 to $200,000.

- A regression problem requires the prediction of a quantity.
- A regression can have real valued or discrete input variables.
- A problem with multiple input variables is often called a multivariate regression problem.
- A regression problem where input variables are ordered by time is called a time series forecasting problem.


## Convert Between Classification and Regression Problems

- In some cases, it is possible to convert a regression problem to a classification problem. For example, the quantity to be predicted could be converted into discrete buckets. For example, amounts in a continuous range between $0 and $100 could be converted into 2 buckets:

Class 0: $0 to $49
Class 1: $50 to $100

We could also convert each age of a person into a "class"... which normally it wouldn't make sense? but we could do that or as in the example above "0 to 12", 13 to 21"... It depends on the case. Anyway...

This is often called discretization and the resulting output variable is a classification where the labels have an ordered relationship (called ordinal).

## Evaluation Metrics
### Coefficient of determination - R^2 (r-squared)
Interpretation: it gives us some information about the goodness of fit of a model (how well it fits a set of observations). In regression, the R^2 coefficient of determination is a statistical measure of how well the regression predictions approximate the real data points.

- The coefficient of determination is the square of the correlation (r) between predicted y scores and actual y scores.
    - An R^2 of 0 means that the dependent variable cannot be predicted from the independent variable.
    - An R^2 of 1 means the dependent variable can be predicted without error from the independent variable, and is thus a highly reliable model for future forecasts.
    - An R^2 between 0 and 1 indicates the extent to which the dependent variable is predictable. An R^2 of 0.10 means that 10% of the variance in y is predictable from X. An R^2 of 0.80 means that **80% of the dependent variable (y) is predicted by the independent variable(X)**, and so on.



IMAGE ------ IMAGE ------0fitting ------ IMAGE ------1fitting ------ IMAGE ------IMAGE ------ IMAGE ------
<p float="left">
  <img src="0fitting" width="500" />
  <img src="0fitting" width="500" /> 
</p>


### Mean squared error (MSE)


IMAGE ------ IMAGE ------------ IMAGE ------2outliers ------ IMAGE ------IMAGE ------ IMAGE ------

    Comparison of the Theil–Sen estimator (black) and simple linear regression (blue) for a set of points with outliers.
    Because of the many outliers, neither of the regression lines fits the data well, as measured by the fact that neither gives a very high R2.


- **PART 1** ---> ??????????<br>
**TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT**



        
        
     EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE
     ---------------------------------------------------------------------------------------------------------------------------------
     EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE


- **PART 2** ---> ??????????<br>
**TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT**
     
<p align="center">
  <img src="images/2binary vs muilti-class.png" width="500" />
</p>
      
     EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE
     ---------------------------------------------------------------------------------------------------------------------------------
     EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE


- **PART 3** ---> ??????????<br>
**TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT**


<p float="left">
  <img src="https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/blob/master/Paulo%20Reis/PauloReis02.png" width="500" />
  <img src="https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/blob/master/Paulo%20Reis/Pauloreis01.png" width="500" />
</p>

       
     EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE
     ---------------------------------------------------------------------------------------------------------------------------------
     EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE EXAMPLE


<p align="center">
  <img src="https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/blob/master/Paulo%20Reis/Paulo_Reis.png" width="500" />
</p>


## TOPIC
**TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT**
    
**Conclusion**

TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT <br> 
TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT TEXT <br>


[<img align="right" width="60" height="60" src="https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/blob/master/Paulo%20Reis/Pauloreis01.png">](https://github.com/pauloreis-ds)

---
