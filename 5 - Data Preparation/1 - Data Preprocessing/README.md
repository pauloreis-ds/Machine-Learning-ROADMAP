# Data Preprocessing
#### "_We torture data until it confesses_"

- Preparing your data to be modelled.

      + Basically, there are 6 steps:
      
      - Feature imputation: filling missing values (a machine learning model can't learn on data that isn't there).
      
      - Feature encoding (turning values into numbers). A machine learning model requires all values to be numerical.
      
      - Feature normalization (scaling) or standardization. When your numerical variables are on different scales 
        (number_of_bathrooms is between 1 and 5 and size_of_land_ between 5,000 and 20,000 sq feet), some machine learning
        algorithms don't perform very well. Scaling and standardization help to fix this.
      
      - Feature engineering: transform data into (potentially) more meaningful representations by adding in domain knowledge.
      
      - Feature selection: selecting the most valuable features of your dataset to model. Potentially reducing overfitting 
        and training time (less overall data and less redundant data to train on) and improving accuracy.
      
      - Dealing with imbalances: does your data have 10,000 examples of one class but only 100 examples of another?

## Feature imputation

Single imputation: Fill with mean, median of column.

Multiple imputation: Model other missing values and fill with what your model finds.

KNN (k-nearest neighbours): Fill data with a value from another example which is similar.

Many more, such as, radom imputation, last observation carried forward (for time series), moving window, most frequent.

## Feature encoding

OneHotEncoding: Turb all unique values into lists of 0's. For example, with car colors green, red, blue, a green car's color feature would  be represented as [1,0,0] and a red one would be [0,1,0].

LabelEncoder: Turn labels into distinct numerical values. For example, if you target variables are different animals, such as dog, cat, bird, these could become 0,1,2 respectively. 

Embedding encoding: Learn a representation amongst all the different data points. For example, a language model is a representation of how different words relate to each other. Embeddings are also becoming more widely available for structured (tabular) data.

## Feature normalization

Feature scaling (also called normalization) shifts your values so they always appear between 0 and 1. This is done by substracting the min value and dividing by the max minus the min. For example, 1 and 4 bathrooms would become something like 0.2 and 0.8 respectively (between 0 and 1 but the numerical relationships is still there).

Feature standardization standardizes all values so they have a mean of 0 and unit variance. It happens by substracting the mean and dividing by the standard diviation of that particular feature. Doing this means values do not end up between 0 and 1 (their range is uncapped) Standardization is more robust to outliers than feature scaling.

## Feature engineering

Decompode, for example, turn a date (such as 2020-06-18 20:16:24) into hour_of_day, day_of_week, day_of_month, is_holiday, etc.

Dicretization (turning larger groups into smaller groups).

Crossing and interaction features, in other words, combining two or more features.

Indicator features: using other parts of the data to indicate something potentially significant.

## Feature selection

Dimensionality reduction: A common dimensionality reduction method, PCA or Principal Component Analysis takes a larger number of dimensions (features) and uses linear algebra to reduce them to less dimensions. For example, say you have 10 numerical features, you could run PCA to reduce it down to 3.

Feature importance (post modelling). Fit a model to a set of data, then inspect which features were most important to the results, remove the least important ones.

Wrapper methods such as genetic algorithms and recursive feature elimination involve creating large subsets of feature options and then removing the ones which don't matter. These have the potential to find a great set of features but can also require a large amount of computation timo. TPot does this.

## Dealing with imbalances

Collect more data (if you can).

Use the scikit-learn-contrib imbalanced-learn package (a scikit-learn compatible Python library for dealing with imbalanced datasets).

Use SMOTE (synthetic minority over-sampling technique) which creates synthentic samples of your minor class to try and level the playing field. You can access an implementation of SMOTE contained within the scikit-learn-contrib imbalanced-learn packange.

A helpful (and technical) paper to look at is "Learning from Imbalanced Data". You could use this as a starting point to go onto the next thing.

[<img align="right" width="60" height="60" src="https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/blob/master/Paulo%20Reis/Pauloreis01.png">](https://github.com/pauloreis-ds)

---
