Feature selection using XGBOOST for machine learning in pyhton  
Description of XGBOOST feature importance
A benefit of using gradient boosting is that after the boosted trees are constructed,
it is relatively straightforward to retrieve importance scores for each attribute.
Generally, importance provides a score that indicates how useful or valuable each feature was in the construction 
of the boosted decision trees within the model. The more an attribute is used to make key decisions with decision trees, 
the higher its relative importance.
This importance is calculated explicitly for each attribute in the dataset,
allowing attributes to be ranked and compared to each other.
Importance is calculated for a single decision tree by the amount that each attribute split point improves the performance measure,
weighted by the number of observations the node is responsible for. 
The performance measure may be the purity (Gini index) used to select the split points or another more specific error function.
The feature importance are then averaged across all of the decision trees within the model.

The function featureSelection_for_regression(X,Y) in FeatureSelectionForRegression is used for regression ie  when the target variavble is continous

The function feature_Selection_for_classification(X,Y) in featureSelectionForClassification is used for classification problems where 
the target variable ie Y is having categories.


The functions are written in pyhton and require only the raw data in form of X and y 
where X represents data frame containing the input or the features 
Y represents the target variable in form of the data frame

The function then calculates the feature importance of the various features present in the input data frame X and plots them with their importance
Then the accuracy  for classification or the RMSE score for regression is shown along with the threshold values and number of features selected
The user can choose the features shown through the graph or based on the threshold values shown corresponding to their accuracy and rmse.
