# **Credit_Risk_Analysis**
## **Analysis Overview**
For this project, we were tasked to predict credit risk. We will use Python to build and evaluate several machine learning models by adopting the following procedures:

- Data Oversampling -> using *RandomOverSampler* and *SMOTE* algorithms
- Data Undersampling -> using *ClusterCentroids* algorithm
- Combinbation of over- and under- sampling -> using *SMOTEENN* algorithm
- Comparing machine learning models that reduce bias -> *BalancedRandomForestClassifer* and *EasyEnsembleClassifer*

An evaluation of the models' performance will be used to make a recommendation for a bank on whether our machine learning models should be used to predict credit risk.

### Resources
Data Source: LoanStats_2019Q1.csv
Software: Python, Jupyter Notebook

## **Machine Learning Model Results**

### *RandomOverSampler Model*
- Balanced accuracy score is 79%.
- high_risk precision is about4% only with 67% sensitivity which makes a F1 of 1%.
- Due to the high number of the low_risk population, the model's precision is almost 100% with a sensitivity of 91%.

### *SMOTE Model*
- Balanced accuracy score is 65%.
- high_risk precision is about 1% with 66% sensitivity which makes a F1 of 1%.
- Due to the high number of the low_risk population, the model's precision is almost 100% with a sensitivity of 64%.

### *ClusterCentroids Model*
- Balanced accuracy score is down to about 53%
- high_risk precision is still 1% with 61% sensiticity which makes a F1 of 1%
- Due to the high number of false positives, the low_risk sensitivity is only 45%

### *SMOTEEN Model*
- Balanced accuracy score is about 62%
- high_risk precision is still 1% with 70% sensiticity which makes a F1 of 1%
- Due to the high number of false positives, the low_risk sensitivity is 55%

### *BalancedRandomForestClassifer Model*
- Balanced accuracy score improved to about 79%
- high_risk precision is low at 4% with 67% sensiticity which makes a F1 of 1%
- Due to the lower number of false positives, the low_risk sensitivity is 91% with 100% precision

### *EasyEnsembleClassifer Model*
- Balanced accuracy score is high, about 93%
- high_risk precision is still low, 7%, with 91% sensiticity which makes a F1 of 1%
- Due to the lower number of false positives, the low_risk sensitivity is only 94%

## **Summary**
After evaluating the performance of all six models, I would not recommend the bank to use any of these models to predict credit risk. Our credit risk analysis showed all models having weak precision in determining if credit risk is high. The EasyEnsembleClassifier model had a 92% recall causing the model to detect almost all high risk credit. Having a low precision rate could cause the bank to incur penalties and missed revenue opportunities since that model could falsely detect low risk credits as high risk.

