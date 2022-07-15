# Credit Risk Analysis - Supervised Machine learning 

## Overview of the Analysis
The purpose of this project was to help Jill analyze credit applications to determine credit card risk using machine learning.  Since credit risk tends to be very one-sided in terms of the number of good loans far outweighing the number of bad loans, we had to train and evaluate our models with unbalanced classes.  To do so we completed six different resampling techniques - Naive Random Oversampling, SMOTE Oversampling, Undersampling, Combination Sampling, Balanced Random Forest Classifier, and Easy Ensemble AdaBoost Classifier. After completing the analysis, we then made a recommendation on weather Jill and her team should use any of the machine learning models to predict credit risk. 

## Results

### *Naive OverSampling*

![](https://github.com/NRFlood/Credit-Risk-Analysis/blob/main/Naive%20Oversampling.PNG)

### *SMOTE OverSampling*

![](https://github.com/NRFlood/Credit-Risk-Analysis/blob/main/SMOTE%20Oversampling.PNG)

Unfortunately, neither the Naive nor SMOTE oversampling resulted in a model that could confidently be used to predict bad loans. The Naive oversampling yielded a precision score of 0.01, a recall score of 0.66, and an F1 score of 0.02. The SMOTE oversampling was very similar yielding a precision score of 0.01, a recall score of 0.61, and an F1 score of 0.02.  The low precision scores indicates both models are generating a high number of false positives, meaning people that should be approved for loans are being turned down. The recall scores of both models are a little better, but there are still roughly 30% of applicants that are classified as a false negative.  The F1 scores being 0.02 for both models are also very low, indicating that neither model is accurate.

### *Undersampling*

![](https://github.com/NRFlood/Credit-Risk-Analysis/blob/main/Undersampling.PNG)

The Undersampling model yielded results similar to both oversampling models, with a precision score of 0.01, a recall score of 0.65, and an F1 score of 0.01.  Based on these results the undersampling model does not do any better job of predicting credit risk than the oversampling models. 

### *Combination Model*

![](https://github.com/NRFlood/Credit-Risk-Analysis/blob/main/Combination%20Sampling.PNG)

The Combination model was not much different from the previous three models, yielding a precision score of 0.01, a recall score that was slightly better at 0.69, and an F1 score of 0.02.  Though the recall score is slightly better, the overall model performance is not great. 

### *Balanced Random Forest Classifier*

![](https://github.com/NRFlood/Credit-Risk-Analysis/blob/main/Balanced%20Random%20Classifier.PNG)

### *Easy Ensemble AdaBoost Classifier*

![](https://github.com/NRFlood/Credit-Risk-Analysis/blob/main/AdaBoost%20Classifier.PNG)

The Ensemble Algorithms performed slightly better with the Balanced Random Forest Classifier yielding a precision score of 0.03, a recall score of 0.70, and an F1 score of 0.06, and the AdaBoost Classifier yielding a precision score of 0.09, a recall score of 0.92, and an F1 score of 0.16.  However, like the oversampling, undersampling, and combination models, neither model is accurate enough to use as a tool to predict credit worthiness. 

## Summary

Due to the lack of accuracy in all six machine learning models we do not recommend that Jill and team use them as a tool for predicting which credit applications should be approved or denied.  There are far too many applicants who would be denied by all six models when they indeed should be approved.
