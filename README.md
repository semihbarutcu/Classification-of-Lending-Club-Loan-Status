# Classification of Lending Club Loan Status

In this project, Lending Club accepted loan data was studied. Loan status was response variable and I worked on both 84 remaining variable and selected 14 remaining variable. Machine Learning algorithms implementations and results can be seen below step by step.

The data is imbalanced. Original proportions are 82.7% of fully-paid and 17.3% of charged-off. Good credits observations are under-sampled accordinglt total number of bad credits and a balanced dataset is obtained which has 50% of the each categories. This way, the resulting balanced dataset would provide a better learning process for any model.  

The balanced data has 130994 observations and 25 independent variables with the response variable loan_status. I used 75 to 25 percent split for training and test datasets. All of these models are tuned over a validation set sampled within training set without replacement.

Four different algorithms are implemented: Logistic Regression, kNN, a Decision Tree method (C5.0) and Random Forest. Boosting method are used to check and improve models. The kNN method has the least accurate results for the test data while the Random Forest had best which is 85.39%. The C5.0 method results very close to the Random Forest while boosting does not help to improve the accuracy of the test data. Because of increased over-fitting, it would be a better choice to use the single tree model.

Once decided on the best model, refit it using all of the 2012-2014 data and then use your model to classify all of the 2015 data. Check the accuracy of your predictions. 2015 Lending Club data includes higher proportions of charged-off category due to 60 months credits mostly have not resulted for fully-paid credits.

Performances of all models for an imbalanced data can be seen below. Logistic Regression has better accuracy than others for 2015. However, k-nearest neighbors has the highest specificity and Random forest has the highest sensitivity.

   Models           | Sensitivity | Specificity | Accuracy |
--------------------|-------------|-------------|----------|
 Logistic Regression|    0.906    |    0.882    |   0.887  |          
--------------------|-------------|-------------|----------|
 k-Nearest Neighbors|    0.711    |    0.920    |   0.811  |          
--------------------|-------------|-------------|----------|
 C5.0               |    0.939    |    0.841    |   0.860  |          
--------------------|-------------|-------------|----------|
 Random Forest      |    0.944    |    0.835    |   0.855  |          
--------------------|-------------|-------------|----------|


Trade-off of this study is between the cost of default and paid credits. 

My last decision is to use Random forest, the method with the highest sensitivity. Detecting bad credits correctly 94.4% instead 90.6% is more valuable than getting higher total accuracy by 2.2%. 

If the loss and profit values are known in advance, then an integer programming approach could be implemented to make the final model selection easier. 
