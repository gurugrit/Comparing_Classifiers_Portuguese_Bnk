# Comparing Classifiers
### Module-17 : Practical Exercise-3 
 
 The goal of this assignment is to compare the performance of the classifiers : k-nearest neighbors, logistic regression, decision trees, and support vector machines. You will use a dataset related to the marketing of bank products over the telephone. For this exercise we will be utilizing the from  UC Irvine Machine Learning Repository. The data is from a Portuguese Banking Institution and is a collection of the results of multiple marketing campaigns.

# Dataset

The Data set link is as provided below
https://archive.ics.uci.edu/dataset/222/bank+marketing

About the Dataset: This dataset comprises data from 17 different marketing campaigns, conducted between May 2008 and November 2010

# How is the project work and deliverables being measured? - Measurement Criteria Table As Below
<img width="842" height="505" alt="image" src="https://github.com/user-attachments/assets/28010461-6ed7-4e4a-a765-3aa3f5efd99e" />

# Note about the Files, Folder and Dataset...
The Folder Structure for this Project is as below under the repository: "Comparing_Classifiers_Portuguese_Bnk"

<img width="278" height="160" alt="image" src="https://github.com/user-attachments/assets/e8824d25-624e-4148-a77f-4a4cc19bb18b" />

# Six Standard Phases of CRISP-DM in Comparing the Performance Classifiers?
## 1. Business Understanding
### Objective: Is to predict whether a bank client will subscribe to a term deposit based on information obtained during direct marketing campaigns like phone calls, along with demographic and economic context data.
### Key Business Questions:
•	Is to predict whether a bank client will subscribe to a term deposit based on information obtained during direct marketing campaigns like phone calls this along with demographic and economic context data.
## 2. Data Understanding
### Data Description: The dataset contains 41188 entires with 21 Column-attributes/Features such as:
•	age (numeric)
•	job - type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')
•	marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)
•	education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
•	default: has credit in default? (categorical: 'no','yes','unknown')
•	housing: has housing loan? (categorical: 'no','yes','unknown')
•	loan: has personal loan? (categorical: 'no','yes','unknown')
#### Related with the last contact of the current campaign:
•	contact: contact communication type (categorical: 'cellular','telephone')
•	month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')
•	day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')
•	duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). 
  Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded 
  if the intention is to have a realistic predictive model.
#### Other attributes:
•	campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)
•	pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
•	previous: number of contacts performed before this campaign and for this client (numeric)
•	poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')
#### Social and economic context attributes
•	emp.var.rate: employment variation rate - quarterly indicator (numeric)
•	cons.price.idx: consumer price index - monthly indicator (numeric)
•	cons.conf.idx: consumer confidence index - monthly indicator (numeric)
•	euribor3m: euribor 3 month rate - daily indicator (numeric)
•	nr.employed: number of employees - quarterly indicator (numeric)
#### Output variable (desired target):
•	y - has the client subscribed a term deposit? (binary: 'yes','no')
