# credit-risk-classification
## **Important Notes:**
- If when running the "Fit the original training data to the random_oversampler model" section of "credit_risk_classification.ipynb" you get an error saying "ImportError: cannot import name _MissingValues from sklearn.utils._param_validation" then per https://stackoverflow.com/questions/76593906/how-to-resolve-cannot-import-name-missingvalues-from-sklearn-utils-param-v you will need to downgrade to scikit-learn 1.2.2 by typing the following commands:
    - conda remove scikit-learn
    - conda install scikit-learn=1.2.2
- Also make sure PIP is installed using the following command:
    - conda install pip

## **Background:**
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

The instructions for this Challenge are divided into the following subsections:
- Split the Data into Training and Testing Sets
- Create a Logistic Regression Model with the Original Data
- Write a Credit Risk Analysis Report

**Split the Data into Training and Testing Sets**
Open the starter code notebook and use it to complete the following steps:
- Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
- Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
    - NOTE: A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
- Split the data into training and testing datasets by using train_test_split.

**Create a Logistic Regression Model with the Original Data**
Use your knowledge of logistic regression to complete the following steps:
- Fit a logistic regression model by using the training data (X_train and y_train).
- Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
- Evaluate the model’s performance by doing the following:
    - Generate a confusion matrix.
    - Print the classification report.
- Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

**Write a Credit Risk Analysis Report**
Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository. Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:
- An overview of the analysis: Explain the purpose of this analysis.
- The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.
- A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.

## **Credit Risk Analysis Report**
### **Overview of the Analysis**
- ANSWER: Explain the purpose of the analysis.
- ANSWER: Explain what financial information the data was on, and what you needed to predict.
- ANSWER: Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
- ANSWER: Describe the stages of the machine learning process you went through as part of this analysis.
- ANSWER: Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

### **Results**
- Machine Learning Model 1
    - ANSWER: Description of Model 1 Accuracy Scores
    - ANSWER: Description of Model 1 Precision Scores
    - ANSWER: Description of Model 1 Recall Scores

- Machine Learning Model 2
    - ANSWER: Description of Model 2 Accuracy Scores
    - ANSWER: Description of Model 2 Precision Scores
    - ANSWER: Description of Model 2 Recall Scores

### **Summary**
- Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
    - Which one seems to perform best? How do you know it performs best?
    - Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
    - If you do not recommend any of the models, please justify your reasoning.

## **Sources:**
- The basis for the majority of the code used in "credit_risk_classification.ipynb" came from the class activities "1/04-Stu_Predicting_Diabetes" and "2/08-Stu_Predicting_Bank_Customers". The rest came from the following sources:
    - The basis for the code used in the "Check the balance of our target values" section of "credit_risk_classification.ipynb" was found from https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html.
    - The basis for the code used in the "Print the balanced_accuracy score of the model" section of  "credit_risk_classification.ipynb" was found from https://scikit-learn.org/stable/modules/generated/sklearn.metrics.balanced_accuracy_score.html.
    - The basis for the code used in the "Instantiate the random oversampler model, Assign a random_state parameter of 1 to the model" section of "credit_risk_classification.ipynb" was fround from https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.html.
    - The Basis for the code used in the "Retrieving Accuracy Score Averages of logistic regression model", "Retrieving Precision Score Averages of logistic regression model", "Retrieving Recall Score Averages of logistic regression model", "Retrieving Accuracy Score Averages of Oversampled logistic regression model", "Retrieving Precision Score Averages of Oversampled logistic regression model" and "Retrieving Recall Score Averages of Oversampled logistic regression model" sections of "credit_risk_classification.ipynb" came from https://ipython.readthedocs.io/en/stable/api/generated/IPython.display.html, https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html, https://scikit-learn.org/stable/modules/generated/sklearn.metrics.precision_score.html and https://scikit-learn.org/stable/modules/generated/sklearn.metrics.recall_score.html.