# Feature engineering
#### "_Engineering? It's like magic, but real_"

- Feature engineering is the process of transforming raw data into features that better represent the underlying problem to the predictive models, 
resulting in improved model accuracy on unseen data.
- Feature engineering is manually designing what the input x’s should be. You have to turn your inputs into things the algorithm can understand.

      Machine learning algorithms learn a solution to a problem from sample data.
      In this context, feature engineering asks: what is the best representation of the sample data to learn a solution to
      your problem?

> "_Actually the success of all Machine Learning algorithms depends on how you present the data._"


## General Examples of Feature Engineering
### Decompose Categorical Attributes
Imagine you have a categorical attribute, like “Item_Color” that can be Red, Blue or Unknown. Unknown may be special, but to a model, it looks like just another colour choice.
It might be beneficial to better expose this information.

You could create a new binary feature called “Has_Color” and assign it a value of “1” when an item has a color and “0” when the color is unknown.

Going a step further, you could create a binary feature for each value that Item_Color has. This would be three binary attributes: Is_Red, Is_Blue and Is_Unknown.

These additional features could be used instead of the Item_Color feature (if you wanted to try a simpler linear model) or in addition to it
(if you wanted to get more out of something like a decision tree).

### Decompose a Date-Time
A date-time contains a lot of information that can be difficult for a model to take advantage of in it’s native form.

If you suspect there are relationships between times and other attributes, you can decompose a date-time into constituent parts that may allow models to discover and exploit
these relationships. For example, you may suspect that there is a relationship between the time of day and other attributes.

You could create a new numerical feature called Hour_of_Day for the hour that might help a regression model.

You could create a new ordinal feature called Part_Of_Day with 4 values Morning, Midday, Afternoon, Night with whatever hour boundaries you think are relevant. 
This might be useful for a decision tree.

You can use similar approaches to pick out time of week relationships, time of month relationships and various structures of seasonality across a year.
Date-times are rich in structure and if you suspect there is time dependence in your data, take your time and tease them out.

### Reframe Numerical Quantities
Your data is very likely to contain quantities, which can be reframed to better expose relevant structures. 
This may be a transform into a new unit or the decomposition of a rate into time and amount components.
You may have a quantity like a weight, distance or timing. A linear transform may be useful to regression and other scale dependent methods.
For example, you may have Item_Weight in grams, with a value like 6289. 

You could create a new feature with this quantity in kilograms as 6.289 or rounded kilograms like 6. 
If the domain is shipping data, perhaps kilograms is sufficient or more useful (less noisy) a precision for Item_Weight.

The Item_Weight could be split into two features: Item_Weight_Kilograms and Item_Weight_Remainder_Grams, with example values of 6 and 289 respectively.

There may be domain knowledge that items with a weight above 4 incur a higher taxation rate.
That magic domain number could be used to create a new binary feature Item_Above_4kg with a value of “1” for our example of 6289 grams.

You may also have a quantity stored as a rate or an aggregate quantity for an interval. For example, Num_Customer_Purchases aggregated over a year.

In this case you may want to go back to the data collection step and create new features in addition to this aggregate and try to expose more 
temporal structure in the purchases, like perhaps seasonality. For example, the following new binary features could be created: Purchases_Summer, Purchases_Fall, 
Purchases_Winter and Purchases_Spring.




[<img align="right" width="60" height="60" src="https://github.com/pauloreis-ds/Paulo-Reis-Data-Science/blob/master/Paulo%20Reis/Pauloreis01.png">](https://github.com/pauloreis-ds)

---
