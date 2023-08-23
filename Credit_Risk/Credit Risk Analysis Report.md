## **Credit Risk Analysis Report**
### **Overview of the Analysis**
- The purpose of this analysis is to use historical lending data/activity to predict the creditworthiness of borrowers.
- The financial information the data was on was pertaining to loan risk based on loan size, interest rate, income, debt to income ration, number of credit accounts, derogatory marks on credit report and total debt. The data is trying to predict high risk and low risk loans in order to predict the creditworthiness of borrowers.
- The variables attempted to be predicted are the number of high risk and low risk loans.
- Using "lending_data.csv", I created a logistic regression model (Log_Reg_Model). This model had a balanced accuracy score of about 95.2%. 
- I used the "RandomOverSampler" module from the "imbalanced-learn" library to resample the data into a random oversampler model (ROS). This resampled data was then fit into the model using the "LogisticRegression" classifier. This new model had a balanced accuracy score of about 99.4%.

### **Results**
- Machine Learning Model 1
    - model 1 had an accuracy score of about 99.2%
    - model 1 had a precision score of about 99.7% for healthy (low-risk) loans and about 84.7% for unhealthy (high-risk) loans
    - model 1 had a recall score of about 99.45% for healthy (low-risk) loans and about 91% for unhealthy (high-risk) loans

- Machine Learning Model 2
    - model 2 had an accuracy score of about 99.4%
    - model 2 had a precision score of about 99.98% for healthy (low-risk) loans and about 84.13% for unhealthy (high-risk) loans
    - model 2 had a recall score of about 99.38% for healthy (low-risk) loans and about 99.35% for unhealthy (high-risk) loans

### **Summary**
- Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
    - Model 2 seems to work best because it has the best recall accuracy score overall for both healthy (low-risk) and unhealthy (high-risk) loans. Model 1 had a slightly better recall accuracy score of 99.45% for healthy (low-risk) loans vs 99.38% for healthy (low-risk) loans in model 1, however the recall accuracy score for unhealthy (high-risk) loans was better in model 2 with a recall accuracy score of 99.35% for unhealthy (high-risk) loans vs 91% in model 1.
    - I believe it would be more important to predict the `1`'s (high-risk loans) to determine what borrows to use caution with when considering providing them a loan. Loan providers want borrows to be able to pay back their loans and not default on them.