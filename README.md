Comparing Classifiers
Module-17: Practical Exercise-3
The goal of this assignment is to compare the performance of the classifiers: k-nearest neighbors, logistic regression, decision trees, and support vector machines. You will use a dataset related to the marketing of bank products over the telephone. For this exercise we will be utilizing the from UC Irvine Machine Learning Repository. The data is from a Portuguese Banking Institution and is a collection of the results of multiple marketing campaigns.
Dataset
The Data set link is as provided below 
About the Dataset: This dataset comprises data from 17 different marketing campaigns, conducted between May 2008 and November 2010
How is the project work and deliverables being measured? - Measurement Criteria Table As summarized below…

Note about the Files, Folder and Dataset...
The Folder Structure for this Project is as below under the github repository named "Comparing\_Classifiers\_Portuguese\_Bnk"

Application of Six Standard Phases of CRISP-DM in Comparing the Performance Classifiers?
1. Business Understanding
Objective: Is to predict whether a bank client will subscribe to a term deposit based on information obtained during direct marketing campaigns like phone calls, along with demographic and economic context data.
Key Business Question:
• Whether a bank client will subscribe to a term deposit based on information obtained during direct marketing campaigns like phone calls this along with demographic and economic context data.
2. Data Understanding
Data Description: The dataset contains 41188 entries with 21 Column-attributes/Features such as:
Input variables:

Initial Steps:
We begin by observing and cleaning the Data
3. Data Preparation: Cleaning and Preprocessing:
Replacing - Replace 'unknown' with NaN
Drop - Drop 'duration'
Create – Feature 
Substitute – With neutral values
Convert – Variable to Binary
• Convert categorical variables (e.g., one-hot encoding)
• Normalize or scale features if needed
• Create derived features

Data prepared by spliting it into a train and test sets.

4. Modeling
Approach: Use of regression models…
Logistic Regression
K-Nearest Neighbors
Decision Tree
Support Vector Machine
Before we build our first model, we want to establish a baseline.
Baseline Accuracy: 0.8873





Model Validation and Comparisons of Models
 
 

Model Visualizations -
Model Accuracy Comparison Plot:



Opted out Plotting SVM: Due to the time it takes for the processor to process the large data set.
Confusion Matrix:


ROC Curve Comparison:
The overall performance of a classifier, summarized over all possible classification thresholds, is given by the area under the ROC curve. An ideal ROC curve will hug the top left corner, indicating a high true positive rate and a low false positive rate; the larger the AUC( Area Under) the better the classifier.



Recommendations and Deployment Guidelines
Logistic Regression — Recommended (Best Balance of Performance + Efficiency)
Highest Test Accuracy (90.13%)
Very fast training time
Low risk of overfitting (train ≈ test accuracy)
Interpretable (important for regulatory and business explanations)
Support Vector Machine — Also Strong, but High Cost
Excellent accuracy (90.08%), nearly identical to Logistic Regression
Extremely high train time (343 seconds vs 0.24s)
K-Nearest Neighbors — Good Accuracy, but Not Scalable
Simple, intuitive, no training time
Slightly worse test accuracy (89.33%)
Inefficient for large-scale prediction (slow at test time)
With small datasets KNN is ok for prototyping
d) Decision Tree — Overfitting, Not Reliable
Train accuracy too high (99.47%) → classic overfitting
Worst test accuracy (84.07%)
Recommendation:
Use of Decision Tree is ruled out may be Random Forest or Gradient Boosting be a better option.

In Conclusion
Prediction Goal was mMet: The models can reasonably predict y = 'yes' or 'no' for new clients.
This was based on…
Logistic Regression, KNN, Decision Tree, and SVM models.
Best Model being : Logistic Regression which gave us:
Test Accuracy: ~90%
Train Accuracy: ~90%
Reasonable F1-Score (if computed), especially for an imbalanced dataset.
In total, our model can predict term deposit subscription using available client, campaign, and economic data with high accuracy and practical reliability.
