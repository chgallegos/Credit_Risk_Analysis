# Credit_Risk_Analysis
## Overview
The purpose of this analysis  was to employ machine learning techniques in order to evaluate credit risk data for the company colled LendingClub, a peer-to-peer lending sercices company. The data was to be oversampled, undersampled and also a combinational under-over-sampling approach. Subsequently, the data is to be ran through two models that reduce bias.

----
## Results

### Accuracy, Precision, Recall and F-1 scores

Before going into the analysis, it is important to define what these scores mean and indicate.

##### 1) Precision Score
Measures the proportion of positively predicted labels that are actually correct. Precision is also known as the positive predictive value.

##### 2) Recall Score
Model recall score represents the model’s ability to correctly predict the positives out of actual positives. This is unlike precision which measures how many predictions made by models are actually positive out of all positive predictions made.

##### 3) Accuracy Score
Model accuracy is a machine learning classification model performance metric that is defined as the **ratio of true positives and true negatives to all positive and negative observations.** In other words, accuracy tells us how often we can expect our machine learning model will **correctly predict** an outcome out of the total number of times it made predictions. 

##### 4) F-1 Score
Model F1 score represents the model score as a function of **precision** and **recall** score. F-score is a machine learning model performance metric that gives equal weight to both the Precision and Recall for measuring its performance in terms of accuracy, making it an alternative to Accuracy metrics 

### Oversampling
For this section, I compared two oversampling algorithms to determine which algorithm results in the best performance. This was done by oversampling the data using the naive random oversampling algorithm and the SMOTE algorithm.

#### Naive Random Oversampling V/S SMOTE Oversampling

![Screenshot](https://github.com/chgallegos/Credit_Risk_Analysis/blob/main/resources/naive_random_oversampling.png)
![Screenshot](https://github.com/chgallegos/Credit_Risk_Analysis/blob/main/resources/smote_oversampling.png)

As we can see from the screenshots, the F-1 score for the naive Randome oversampling is higher than with SMOTE, nevertheless,the precission and recall scores are pretty similar.

### Undersampling
This part of the analysis consisted of testing an undersampling algorithm to determine which algorithm results in the best performance compared to the oversampling algorithms 

#### Cluster Centroids resampler

![Screenshot](https://github.com/chgallegos/Credit_Risk_Analysis/blob/main/resources/cluster_centroids_undersampling.png)

The calculated data indicates that the F-1 scores are low as well as the accuracy score, making it not an ideal model.

#### SMOTEEN resampler 

![Screenshot](https://github.com/chgallegos/Credit_Risk_Analysis/blob/main/resources/combination_SMOTEEN_sampling.png)

The SMOTEEN resampler uses both over and undersampling methods in one. While keeping the precision score high and the recall level low, both the F-1 and accuracy scores are not the highest.

### Ensemble Learners
In this part of the analysis I compared two ensemble algorithms to determine which algorithm results in the best performance. This was done by training a Balanced Random Forest Classifier and an Easy Ensemble AdaBoost classifier.

#### Balance Random Forest Classifier

![Screenshot](https://github.com/chgallegos/Credit_Risk_Analysis/blob/main/resources/balanced_random_forest.png)

The numbers for the balanced random forest indicate a high F-1 scores as well as accuracy scores and precision.

#### Easy Ensemble Adaboost Classifier

![Screenshot](https://github.com/chgallegos/Credit_Risk_Analysis/blob/main/resources/easy_ensemble_AdaBoost%20classifier.png)

The numbers for the Easy Ensemble Adaboost Classifier indicate a higher f-1 score as well as accuracy.

## Summary 

In summary, from looking at the results of our models with their F-1 Scores as well as accuracy. My concluding statement indicates that all of these models have their strengths and weaknesses, therefore they could always be suited for a wide array of analysis. However, my recommendation would be to use the **Easy Ensemble Adaboost** classifier as this model provides high accuracy as well as f-1 scores.