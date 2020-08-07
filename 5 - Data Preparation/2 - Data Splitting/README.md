# Data Splitting
#### "_Divide and Conquer_"

- Purpose of splitting data into the different category is to avoid overfitting

1 - **Training set** (usually 70-80% of data): Model learns on this.

2 - **Validation set** (typically 10-15% of data): Model hyperparameters are tuned on this.

3 - **Test set** (usually 10-15%): Models final performance is evaluated on this. If you've done it right, hopefully the results on the test set give a good indication of how the model should perform in the real world. Do not use this dataset to tune the model.


> ps: a development set (validation set) is the data you would use to optimize your model against during the development process. A machine learning process has a training (or train) set, which is the data you train the model with, and a test set, which you use to determine the performance of the model.

    But, if you are looking at multiple options (multiple models or multiple sets of so-called hypermaramerers),
    then if you use the test set to pick the best-performing one, you wouldn't be able to tell what performance 
    to expect moving forward, since you've just optimized for the test set, the performance is unlikely to carry
    over ("generalize") to new data.

    If, however, you had a third dataset, which you optimize against (and that's the one called development set, 
    dev set or validation set), and wouldn't have access to the test data during development, you'd still be able
    to tell the "real" performance after you're done.
    
[Data splitting technique](https://towardsdatascience.com/data-splitting-technique-to-fit-any-machine-learning-model-c0d7f3f1c790). 
 
**A good explanation about data splitting. Sorry, Did I say "a good" explanation? A Great explanation about data splitting. A Great explanation? An Awesome explanation about** [data splitting](https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/tree/master/3%20-%20Data%20Analysis%20(Machine%20Learning))!
    
   

[<img align="right" width="60" height="60" src="https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/blob/master/Paulo%20Reis/Pauloreis01.png">](https://github.com/pauloreis-ds)

---
