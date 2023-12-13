# PRODIGY_DS_03

## Task
Build a decision tree classifier to predict whether a customer will purchase a product or service based on their demographic and behavioral data. Use a dataset such as the Bank Marketing dataset from the UCI Machine Learning Repository.

## Data Understanding
The descriptions of the features in the data are as follows:

![Metadata](https://github.com/Nickimani/PRODIGY_DS_03/assets/104377216/d3cdd657-007a-49c2-84c8-baa132fe4ab5)

The data was fairly clean with a low number of outliers and duplicates.

## Preprocessing
The data was label encoded to make it usable by the model. Aside from that, resampling techniques were applied to try and balance the target classes. 
Undersampling of the majority class was first done and the model built by the resulting data showed a small improvement.

However, the precision and recall performance was lacking. 
Therefore, Oversampling of the minority class was then done which improved the recall of the model by a great margin.

## Model performance
The final model was trained on oversampled data and its perfomance was as follows:

    Recall Score -> ~75% of customers should subscribe to the product (yes) while ~81% of customers who typically don't subscribe to the product are predicted correctly by the model.

    Precision Score -> Out of all customers predicted as going to subscribe to the product, the model is correct ~33% of the time while for those predicted as not going to subscribe, the model is correct ~96% of the time

## Conclusions
Whether a customer has defaulted on credit payments before, has loans, or has had some outcome from previous product campaigns does not contribute much to the chance of subscription to a product.

However, the following factors have a high influence on the chances that a customer will subscribe to a product: 

1. The duration of interactions(Calls), 
2. Bank balance, 
3. Age of a customer, 
4. Days since the last contact with the customer, 
5. Number of times a customer has been contacted during a product campaign period, 
6. The month and day of the month that a customer was contacted 
