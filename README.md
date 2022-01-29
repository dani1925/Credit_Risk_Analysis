# Credit_Risk_Analysis

This repository contains credit information of users in order to determine those people who may pose a risk to the financial institution when authorizing a loan.

To select which people pose a high or low risk, different supervised machine learning algorithms are used and the aim is to compare the results between the different algorithms.

## Oversampling Algorithms

For this first method, the Balanced Accuracy Score was 64%.
Further analysis is required as the Balanced Accuracy Score can be misleading as it can very well predict a false positive but not a false negative or vice versa.

## Confusion Matrix

    # Display the confusion matrix
    from sklearn.metrics import confusion_matrix
    confusion_matrix(y_test, y_pred)
    Output:
    array([[   53,    34],
       [ 5443, 11675]])



The confusion matrix allows visualization of the performance of an algorithm, typically a supervised learning one and compare the real result vs in calculated result. 


| | Predict High Risk | Predicted Low Risk|
| ------------- | ------------- | ----------|
| Real High Risk | 53  | 34
| Real Low Risk  | 5443  | 11675


adjusts the high risk values ​​with a precision of 60% while the low risk adjusts it with a precision of 68% 

This same analysis process is performed for the algorithms described in the attached files and it is found that the best algorithm is the Easy Ensemble AdaBoost Classifier with a Balanced Accuracy Score of 93%
