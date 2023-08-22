# credit-risk-classification
## **Important Notes:**
- If when running the "Fit the original training data to the random_oversampler model" section of "credit_risk_classification.ipynb" you get an error saying "ImportError: cannot import name _MissingValues from sklearn.utils._param_validation" then per https://stackoverflow.com/questions/76593906/how-to-resolve-cannot-import-name-missingvalues-from-sklearn-utils-param-v you will need to downgrade to scikit-learn 1.2.2 by typing the following commands:
1. conda remove scikit-learn
2. conda install scikit-learn=1.2.2
    - Also make sure PIP is installed using the following command:
1. conda install pip

## **Background:**
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

The instructions for this Challenge are divided into the following subsections:
- Split the Data into Training and Testing Sets
- Create a Logistic Regression Model with the Original Data
- Write a Credit Risk Analysis Report

**Split the Data into Training and Testing Sets**
Open the starter code notebook and use it to complete the following steps:
1. Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.
2. Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.
    - NOTE: A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.
3. Split the data into training and testing datasets by using train_test_split.

**Create a Logistic Regression Model with the Original Data**
Use your knowledge of logistic regression to complete the following steps:
1. Fit a logistic regression model by using the training data (X_train and y_train).
2. Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.
3. Evaluate the model’s performance by doing the following:
    - Generate a confusion matrix.
    - Print the classification report.
4. Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

**Write a Credit Risk Analysis Report**
Write a brief report that includes a summary and analysis of the performance of the machine learning models that you used in this homework. You should write this report as the README.md file included in your GitHub repository. Structure your report by using the report template that Starter_Code.zip includes, ensuring that it contains the following:
1. An overview of the analysis: Explain the purpose of this analysis.
2. The results: Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.
3. A summary: Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.

## **Sources:**
- The basis for the code used in the "Check the balance of our target values" section of "credit_risk_classification.ipynb" was found from https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html.
- The basis for the code used in the "Print the balanced_accuracy score of the model" section of  "credit_risk_classification.ipynb" was found from https://scikit-learn.org/stable/modules/generated/sklearn.metrics.balanced_accuracy_score.html.
- The basis for the code used in the "Instantiate the random oversampler model, Assign a random_state parameter of 1 to the model" section of "credit_risk_classification.ipynb" was fround from https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.RandomOverSampler.html.