# Credit Card Risk Analysis

## Overview
LendingClub, a peer-to-peer lending services company wants to build a machine learning model to classify loans to either risky or not risky.

![alt text](credit_risk.jpeg)

Since good loans easily outnumber risky loans, the data is imbalanced. That's why this task is a little bit tricky. The imbalanced data forced me to implement some special techniques during both, training the models as well as evaluating them. For the training step, I trained the `Logistic Regression` model using oversampling, and undersampling techniques:
<ol>
<li>  Naive Random Over Sampling </li>
<li> SMOTE Over Sampling </li>
<li> Cluster Centroids Under Sampling </li>
<li> SMOTEEN Combination </li>
</ol>

In addition, we trained another two models using the imbalanced data:
<ol>
<li>  Balanced Random Forest </li>
<li> Easy Ensemble Adaboost Classifier </li>
</ol>

To evaluate the model, we used Balance Accuracy Score, as well as the imbalanced Classification Report.


## Results

#### Balanced Accuracy


*Note: LR stands for Logistic Regression*
|Technique|  Balanced Accuracy|
|--|--|
| LR with RandomOverSampling | 65% |
| LR with SMOTE | 66% |
| LR with ClusterCentroids | 54% |
| LR with SMOTEENN | 64% |
| Balanced Random Forest |  79%|
| Easy Ensemble Adaboost | 93% |


Below are the balanced accuracy results obtained with the six experiments


#### Imbalanced Classification Report
In this subsection, the Imbalanced Classification Report for each of the six conducted experiments is reported:

##### LR with RandomOverSampling
![alt text](ros.png)

##### LR with SMOTE
![alt text](smote.png)

##### LR with ClusterCentroids
![alt text](cc.png)

#####  LR with SMOTEENN
![alt text](smoteenn.png)

##### Balanced Random Forest
![alt text](brf.png)

##### Easy Ensemble Adaboost
![alt text](eea.png)


## Summary

Oversampling techniques is much better than the undersampling ones and perform nearly the same as the combination algorithms. However, Balanced RF and Easy Ensemble Adaboost obtained results that surpassed those obtained during using over/under sampling techniques. Although EE Adaboost takes more inference time, it obtained the highest imbalanced accuracy. That's why EE Adaboost is highly recommended for this task.
