# Prediction of Lending Club Loan Status

In this project, Lending Club accepted loan data is studied. Loan status is response variable and I worked on both 84 remaining variable and selected 10 remaining variable.

Three different algorithms are implemented: kNN, a Decision Tree method (C5.0) and Random Forest. One alternative way (Ranger package for Random Forest) and one boosting method are used to check and improve models. The kNN method has the least accurate results for the test data while the Random Forest had best which is 84.64%. The Ranger package gave same results with randomForest package but execution time was shorter, 2.91 sec vs 18.99 sec respectively. The C5.0 method results very close to the Random Forest while boosting does not help to improve the accuracy of outcomes. 
