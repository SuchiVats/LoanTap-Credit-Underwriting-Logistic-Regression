# LoanTap Credit Underwriting with Logistic Regression

This project solves the LoanTap business case, which focuses on building an underwriting model for personal loans. Using logistic regression, we aim to predict whether a credit line should be extended to an individual based on various attributes like loan amount, income, credit history, and employment details.

## Problem Statement

Given a set of attributes for an individual, we need to determine if a credit line should be extended and, if so, what the repayment terms should be. Specifically, we will focus on personal loans for this case study.

## Dataset

The dataset used in this case study is **LoanTapData.csv**, which contains various attributes for individuals applying for loans. The dataset includes the following features:

- `loan_amnt`: The amount of the loan applied for.
- `term`: The loan term (36 or 60 months).
- `int_rate`: Interest rate on the loan.
- `installment`: The monthly payment owed by the borrower.
- `grade`: Loan grade assigned by LoanTap.
- `sub_grade`: Loan subgrade assigned by LoanTap.
- `emp_title`: The job title of the borrower.
- `emp_length`: Employment length in years.
- `home_ownership`: The home ownership status of the borrower.
- `annual_inc`: The self-reported annual income.
- `verification_status`: Whether income was verified by LoanTap.
- `loan_status`: The target variable, indicating if the loan is fully paid or defaulted.
- `purpose`: The purpose of the loan.
- `title`: The loan title.
- `dti`: Debt-to-income ratio.
- `earliest_cr_line`: The month the borrower's earliest credit line was opened.
- `open_acc`: The number of open credit lines in the borrower's file.
- `pub_rec`: Number of derogatory public records.
- `revol_bal`: Total revolving balance.
- `revol_util`: Revolving line utilization rate.
- `total_acc`: Total number of credit lines in the borrower's file.
- `initial_list_status`: The initial listing status of the loan.
- `application_type`: Type of loan application (individual or joint).
- `mort_acc`: Number of mortgage accounts.
- `pub_rec_bankruptcies`: Number of public record bankruptcies.
- `address`: The address of the borrower.

## Steps Involved

1. **Exploratory Data Analysis (EDA)**:
   - Analyzed the structure of the data and the relationships between different variables.
   - Performed univariate and bivariate analysis to understand the distribution of features and their relationship with the target variable (`loan_status`).

2. **Data Preprocessing**:
   - Handled missing values, outliers, and applied feature engineering (e.g., creating flags for certain features like `pub_rec`, `mort_acc`, and `pub_rec_bankruptcies`).
   - Scaled numerical features using `MinMaxScaler` or `StandardScaler`.

3. **Model Building**:
   - Built a logistic regression model using the `LogisticRegression` class from `sklearn`.
   - Evaluated the model using metrics such as ROC AUC, precision-recall curves, and confusion matrix.

4. **Evaluation and Insights**:
   - Discussed the tradeoff between precision and recall, focusing on the importance of detecting real defaulters and minimizing false positives.
   - Provided actionable insights and recommendations for improving the underwriting model.

## Key Metrics

- **ROC AUC**: Measures the model's ability to distinguish between classes.
- **Precision**: The accuracy of positive predictions.
- **Recall**: The ability to detect actual defaulters.
- **F1 Score**: Harmonic mean of precision and recall.

## Recommendations & Insights

1. **Precision vs. Recall Tradeoff**: In this case, minimizing false positives (i.e., giving loans to those who are likely to default) is crucial. A higher recall (identifying most defaulters) is preferred over precision to avoid financial risk.
2. **Feature Importance**: Features like loan amount, income, and credit history heavily influence loan approval.
3. **Actionable Insights**: The model can be further improved by integrating external data such as geographical information or historical financial data to improve the accuracy of predictions.

## Future Improvements

- Further analysis can be conducted using advanced techniques such as regularization (Ridge, Lasso), hyperparameter tuning, and feature selection.
- Integrating additional external data could help improve model performance and risk assessment.
