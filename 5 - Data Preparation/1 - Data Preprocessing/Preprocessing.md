## Feature imputation

### Imputation Using (Mean/Median) Values

      + Pros:
      - Easy and fast.
      - Works well with small numerical datasets.
      
      + Cons:
      - Doesn’t factor the correlations between features. It only works on the column level.
      - Will give poor results on encoded categorical features (do NOT use it on categorical features).
      - Not very accurate.
      - Doesn’t account for the uncertainty in the imputations.
      
### Imputation Using (most Frequent) or (Zero/Constant) Values:
Most Frequent is another statistical strategy to impute missing values and YES!! It works with categorical features (strings or numerical representations)
by replacing missing data with the most frequent values within each column. Again, as the name suggests, it replaces the missing values with either zero 
or any constant value you specify.

      + Pros:
      - Works well with categorical features.
      
      + Cons:
      - It also doesn’t factor the correlations between features.
      - It can introduce bias in the data.
      
### Imputation Using k-NN:
The k nearest neighbours is an algorithm that is used for simple classification. The algorithm uses ‘feature similarity’ to predict the values of any new data points. 
This means that the new point is assigned a value based on how closely it resembles the points in the training set. This can be very useful in making predictions about 
the missing values by finding the k’s closest neighbours to the observation with missing data and then imputing them based on the non-missing values in the neighbourhood.

      + Pros:
      - Can be much more accurate than the mean, median or most frequent imputation methods (It depends on the dataset).
      
      + Cons:
      - Computationally expensive. KNN works by storing the whole training dataset in memory.
      - K-NN is quite sensitive to outliers in the data (unlike SVM)
      
### Imputation Using Multivariate Imputation by Chained Equation (MICE)
This type of imputation works by filling the missing data multiple times. Multiple Imputations are much better than a single imputation as it measures the 
uncertainty of the missing values in a better way. The chained equations approach is also very flexible and can handle different variables of different data types 
(continuous or binary) as well as complexities such as bounds or survey skip patterns. 

IMAGE IMAGE Imputation Using Multivariate Imputation by Chained Equation (MICE) IMAGE IMAGE

### Imputation Using Deep Learning (Datawig):
This method works very well with categorical and non-numerical features. It is a library that learns Machine Learning models using Deep Neural Networks to impute missing values
in a dataframe. It also supports both CPU and GPU for training.

      + Pros:
      - Quite accurate compared to other methods.
      - It has some functions that can handle categorical data (Feature Encoder).
      - It supports CPUs and GPUs.

      + Cons:
      - Single Column imputation.
      - Can be quite slow with large datasets.
      - You have to specify the columns that contain information about the target column that will be imputed.







      
