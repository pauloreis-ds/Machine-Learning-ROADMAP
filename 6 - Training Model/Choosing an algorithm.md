# Choosing an Algorithm
#### _"Everything You Are Comes From Your Choices"_

      Supervised Algorithms
        Linear Regression
        Logistic Regression
        K-Nearest Neighbours
        Support Vector Machine (SVM)
        Decision Tree
        Random Forest
        Gradient Boosting Machine (XGBoost, CatBoost, LightGBM)
        Neural Network (deep learning)

     Unsupervised Algorithms
        K-Means Clustering
        Anomaly Detection (one class --> K-Means, SVM)
        Visualization and Dimensionality Reduction
               
[When to use different machine learning algorithms: a simple guide.](https://www.freecodecamp.org/news/when-to-use-different-machine-learning-algorithms-a-simple-guide-ba615b19fb3b/)

[Choosing the Right Machine Learning Algorithm.](https://hackernoon.com/choosing-the-right-machine-learning-algorithm-68126944ce1f)

<p align="center">
  <img src="image/0ml model trade off.png" width="700" />
</p>

## [Linear Regression](https://www.youtube.com/watch?v=ZkjP5RJLQF4)

Draw a line that best fits data scattered on a graph.
Produces continuous variables(example: height in inches).

## Logistic Regression

Predicts a binary outcome based on a series of independent variables. For example, if you're trying to predict whether someone has heart disease or not based on their health parameters.

## K-Nearest Neighbours

Find the 'k' examples which are most similar to each other. Then, given a new sample, which is the new sample most closely aligned with?

## Support Vector Machine (SVM)

Can be used for classification or regression. Try to find best way to seperate data points using multiple planes (referred to as Hyperplanes). Imagine a road running through a city with red cars on the left and green cars on the right, the SVM is the road. With more data, you might need more dimensions (more roads on different angles and cars on different heights). 

## Decision Tree and Random Forest

Can be used for classification and regression (very valuable algorithm for structured data). Decision trees split data based on criteria such as, "is over 50" and "has average heart rate lower than 65" eventually getting to a point where the data can't be split anymore (you can define this). Random Forests are a combination of many decision trees, effectively leveraging and combining the choices of many models (this technique of using a combination of models is known as ensembling).

## Gradient Boosting Machine

Can be used for classification or regression. It asks the question, can a series of weak learners be turned into a strong learner? For example, train a series of weak learners whos job it is to improve each other (another example of an ensemble method, combining multiple weaker models to create a better one).

## Neural Network (deep learning)

Can be used for classification or regression. Takes a series of inputs, manipulates the inputs with linear (dot product between weights and inputs) and nonlinear functions (activation function). Do this a multiple of times (at least once for each neuron in a model). The importance of linear and non-linear functions (straight and non-straight lines) means neural networks can use this combination to estimate almost anything.


<p align="center">
  <img src="image/1ml tour.png" width="1000" />
</p>


<p align="center">
  <img src="image/2ml_map.png" width="1000" />
</p>




[<img align="right" width="60" height="60" src="https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/blob/master/Paulo%20Reis/Pauloreis01.png">](https://github.com/pauloreis-ds)

---
