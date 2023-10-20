# Exploratory Data Analysis for Loan Repayment Challenge

## Problem 

We would like to predict the loan risk or quality (loan repayment) on a given applicant


## Data preparation, exploration and visualization

Three CSV files were merged based on related columns. For columns that did not made an impact to prediction, they were discarded, reducing the dataset's dimensionality. For missing values, they were identified using a heatmap, and they were either filled with default data or the corresponding rows were removed. Duplicate rows were eliminated and important features were extracted into a new CSV called MergeData.csv. For non-digit columns such as boolean data, the data was converted to integer formats for easier graph plotting. Data was filtered to include only rows with an underwriting process, focusing on the essential task of risk assessment. A further filter was applied to focus on rows with specific loan statuses.


## Machine Learning algorithm

From the given dataset, data was split into 80% for training and 20% for testing. While K-folds cross-validation is another splitting method, our chosen approach relied on a held-out test sample for unbiased evaluation. The model was developed using only four features: loanStatus, clearFraudScore, errorPaymentExist, and nPaidOff. Logistic regression was employed as the machine learning algorithm, given its suitability for classifying loans as risky or not. With an accuracy of approximately 66%, logistic regression outperformed the support vector classification's 64% accuracy in this context.

## Key Features for Prediction

The main features for prediction are loanStatus, clearFraudScore, errorPaymentExist, and nPaidOff. While clearFraudScore is a helpful column, incorporating credit score data could enhance predictive accuracy. Loan purpose could also offer valuable insights.

## Visuliaztion and Insights

Scatter plots and logistic regression plots revealed a positive correlation between the number of previously paid-off loans and the likelihood of future loan repayment. Analysis found that as a client's record of past loan repayments grows, they are less likely to have unsuccessful payments in the future. A density plot showcased the relationship between clear fraud scores and loan statuses, suggesting higher scores equate to a greater probability of loan repayment.

## Suggestions for Improvement

Including credit score information can provide a comprehensive view of a client's credit history. The purpose of the loan can lead to more precise clusters of clients, aiding in predictions as clients within a cluster would share financial traits.
