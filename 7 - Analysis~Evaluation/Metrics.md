# Evaluation Metrics 
#### _"A personal metric: how much of your day is spent doing things out of interest rather than out of obligation?"_
        
### **Confusion Matrix**
**It is a table that is often used to describe the performance of a classification model ("classifier") on a set of test data for which the true values are known. 
It is useful for seeing where a model is getting "confused"/ how often it predicts the right and wrong classes.**
It is extremely useful for measuring Recall, Precision, Specificity, Accuracy and most importantly AUC-ROC Curve.


<p float="left">
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/1%20-%20Classification/images/AAconfusion_matrix_simple.png" width="500" />
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/1%20-%20Classification/images/BBconfusion_matrix.png" width="500" /> 
</p>


    - There are two possible predicted classes: "yes" and "no". If we were predicting the presence of a disease, for example, 
      "yes" would mean they have the disease, and "no" would mean they don't have the disease.
    - The classifier made a total of 165 predictions (165 patients were being tested for the presence of that disease).
    - Out of those 165 cases, the classifier predicted "yes" 110 times, and "no" 55 times.
    - In reality, 105 patients in the sample have the disease, and 60 patients do not.

> Terms you need to know:
> ---------------------------------------------------------------------------------------------------------------------
> **True Positives (TP)**: These are cases in which we predicted yes (they have the disease), and they do have the disease.
>
> **True Negatives (TN)**: We predicted no, and they don't have the disease.
>
> **False Positives (FP)**: We predicted yes, but they don't actually have the disease. (Also known as a "Type I error")
>
> **False Negatives (FN)**: We predicted no, but they actually do have the disease. (Also known as a "Type II error")


<p float="left">
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/1%20-%20Classification/images/CCconfusion_matrix2.png" width="500" />
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/1%20-%20Classification/images/DDconfusion_matrix2.png" width="500" /> 
</p>


- This is a list of rates that are often computed from a confusion matrix for a binary classifier:<br>
  
  - **ACCURACY**: Overall, how often is the classifier correct?
     - (TP+TN)/total = (100+50)/165 = 0.91 
  
  
  - **PRECISION**: When it predicts yes, how often is it correct?
    - TP/predicted yes(FP+TP) = 100/110 = 0.91
 
 
  - **RECALL**: Ratio of True Positives. When it's actually yes, how often does it predict yes?
    - TP/actual yes(TP+FN) = 100/(100+5) = 0.95<br>
      also known as "Sensitivity"<br>


What if we are trying to get the best precision and recall at the same time? F1 Score is the Harmonic Mean between precision and recall. Harmonic Mean is typically appropriate for situations when the average of rates is desired.

[Trading Off Precision and Recall (F1 Score) -](https://www.coursera.org/lecture/machine-learning/trading-off-precision-and-recall-CuONQ) Important! Watch. Think about it. Try to create an example (go back to the confusion matrix image and change numbers, what would be the precision and recall if you had 50TP instead of 100)<br>


  - _Misclassification Rate_: Overall, how often is it wrong?
    - (FP+FN)/total = (10+5)/165 = 0.09<br>
      equivalent to 1 minus Accuracy<br>
      also known as "Error Rate" 
  
  
  - _False Positive Rate_: When it's actually no, how often does it predict yes?
    - FP/actual no = 10/60 = 0.17
  
  
  - _True Negative Rate_: When it's actually no, how often does it predict no?
    - TN/actual no = 50/60 = 0.83<br>
      equivalent to 1 minus False Positive Rate<br>
      also known as "Specificity"


[ROC Curve and AUC](https://developers.google.com/machine-learning/crash-course/classification/roc-and-auc)
  
  
  - _Prevalence_: How often does the yes condition actually occur in our sample?
    - actual yes/total = 105/165 = 0.64
    
There are more and as you may see it can get as [complicated](https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/1%20-%20Classification/images/ZZcomplicated.JPG) as we want. For now, knowing those is a good way to start. Last recall:


<p align="center">
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/1%20-%20Classification/images/FFLast2.jpeg" width="600" />
</p>


<p align="center">
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/1%20-%20Classification/images/EELast.png" width="1100" />
</p>


**y** --> Actual values.<br>
**y pred** --> Model's predictions<br>
**output for threshold** --> Model's predictions "converted" to a language we understand (it could be 'Yes' or 'No', 'spam' or 'not spam'...)

ps: **Accuracy**<br>
**Informally, accuracy is the fraction of predictions our model got right.** As you can see in the image above. [This explanation](https://developers.google.com/machine-learning/crash-course/classification/accuracy) is pretty good, so I'll just leave the link for you to explore.


### Coefficient of determination - R^2 (r-squared)
Interpretation: it gives us some information about the goodness of fit of a model (how well it fits a set of observations). In regression, the R^2 coefficient of determination is a statistical measure of how well the regression predictions approximate the real data points.

How well does the model fit?


<p align="center">
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/2%20-%20Regression/images/0fitting.jpg" width="550" />
</p>


This Error point is important. Look at it!


<p align="center">
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/2%20-%20Regression/images/1fitting.png" width="700" />
</p>


- The coefficient of determination is the square of the correlation (r) between predicted y scores and actual y scores.
    - An R^2 of 0 means that the dependent variable cannot be predicted from the independent variable.
    - An R^2 of 1 means the dependent variable can be predicted without error from the independent variable, and is thus a highly reliable model for future forecasts.
    - An R^2 between 0 and 1 indicates the extent to which the dependent variable is predictable. An R^2 of 0.10 means that 10% of the variance in y is predictable from X. An R^2 of 0.80 means that **80% of the dependent variable (y) is predicted by the independent variable(X)**, and so on.


### Mean Absolute Error (MAE)
All errors are on the same scale. If trying to predict 100, predicting 99 is the same error as predicting 101.

    MAE measures the average magnitude of the errors in a set of predictions, without considering their direction. 
    It’s the average over the sample of the absolute differences between prediction and actual observation where
    all individual differences have equal weight.


<p align="center">
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/2%20-%20Regression/images/2mae.jpg" width="500" />
</p>


### Mean Squared Error (MSE)
It measures the average of the squares of the errors (that is, the average squared difference between the estimated/predicted values and the actual values).<br>

    For every data point, you take the distance vertically from the point to the corresponding y value on the curve fit
    (the error), and square the value. Then you add up all those values for all data points, and, in the case of a fit 
    with two parameters such as a linear fit, divide by the number of points minus two.** The squaring is done so negative
    values do not cancel positive values. The smaller the Mean Squared Error, the closer the fit is to the data. 

It makes outliers stand out more. Use if being 10% off is more than twice as bad as being 5% off.<br>


<p align="center">
  <img src="https://github.com/pauloreis-ds/Machine-Learning-ROADMAP/blob/master/2%20-%20Regression/images/3OUTLIERS.jpg" width="500" />
</p>


MSE can represent the difference between the actual values and the values predicted by the model (how much are we wrong?).

    An MSE of zero, meaning that the predictions are made with perfect accuracy, is the ideal, but is typically not possible.

Values of MSE may be used for comparative purposes. Two or more statistical models may be compared using their MSEs as a measure of how well they explain a given set of observations: an unbiased model with the smallest variance among all models is the best one.

ps: another quantity that we calculate is the Root Mean Squared Error (RMSE). It is just the square root of the mean square error. That is probably the most easily interpreted statistic, since it has the same units as the quantity plotted on the vertical axis (y).

[This may answer some questions of yours](https://www.dataquest.io/blog/understanding-regression-error-metrics/)

[MAE and RMSE — Which Metric is Better?](https://medium.com/human-in-a-machine-world/mae-and-rmse-which-metric-is-better-e60ac3bde13d). I thought it is interesting.
 




[<img align="right" width="60" height="60" src="https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/blob/master/Paulo%20Reis/Pauloreis01.png">](https://github.com/pauloreis-ds)

---
