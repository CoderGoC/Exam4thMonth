# Customer Churn Prediction with Logistic Regression

This repository contains a machine learning project to predict customer churn using a Logistic Regression model. The project aims to predict whether a customer will exit (churn) based on various features such as demographics and customer behavior, leveraging feature engineering techniques to enhance model performance.

## Project Aim
The primary objective of this project is to:

- Predict customer churn using a Logistic Regression model.
- Perform feature engineering to improve model performance.
- Achieve an ROC AUC score of 0.9 or higher through various engineering and tuning techniques.
- Use custom rounding logic to adjust predicted probabilities.


## Features
- Logistic Regression Model: Trained with polynomial features and engineered columns to predict the likelihood of customer churn.
- Custom Rounding Logic: Adjusts the predicted probabilities where:
- Probabilities ≥ 0.7 are rounded up to 1 (customer churn).
- Probabilities < 0.3 are rounded down to 0.
- Probabilities between 0.3 and 0.7 are rounded to 0.001 precision.
- Feature Engineering: Includes interaction features, binning, ratios, and log transformations to enhance model performance.
- Prediction Submission: Generates a CSV file for submission with the predicted 'Exited' values.


## Used Technologies
- The following technologies and libraries were used in this project:

### Python: The main programming language for data processing and model training.

### Logistic Regression: The core machine learning model used for churn prediction.
### NumPy & Pandas: For data manipulation and preprocessing.
### Scikit-learn: For model training, evaluation, and feature engineering.
### PolynomialFeatures: To create interaction terms for the model.
### StandardScaler: For scaling numerical features.
### KBinsDiscretizer: For binning continuous features like age into categorical bins.


## How to use

1. Clone the repository:
   ```bash
   git clone https://github.com/CoderGoC/Exam.git
   ```
2. Create a virtual environment and install the required libraries:
   ```bash
   cd Data-science-home-work
   python -m venv venv
   ```
   ```bash
   source venv/bin/activate  # Linux/Mac
   ```
   ```bash
   .\venv\Scripts\activate  # Windows
   ```
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Python py file:
   ```bash

## Feature Engineering
- The following feature engineering techniques were applied to improve model performance:

- Interaction Features: Created interaction terms such as CreditScore * Balance and Age * EstimatedSalary.
1. Binning: Used KBinsDiscretizer to categorize age into bins.
2. Ratios: Created balance-to-salary ratios to capture financial behavior.
3. Log Transformation: Applied log transformation to the Balance feature to reduce skewness.
4. Group Statistics: Added mean balance per geographic region to capture region-wise behavior.
5. Model Performance

## After applying these techniques, the model achieved:

6. Validation ROC AUC: 0.874
7. Validation Accuracy: 0.862
8. Predictions and Custom Rounding Logic
9. The model generates predictions on the test dataset, and custom rounding logic is applied:

10. If the predicted probability is ≥ 0.7, the output is rounded up to 1 (indicating the customer will churn).
11. If the predicted probability is < 0.3, the output is rounded down to 0 (indicating the customer will not churn).
12. Probabilities between 0.3 and 0.7 are rounded to 0.001 precision.


## Submission
13. The script outputs a file named SubmissionFinal.csv, containing the predicted 'Exited' values for each customer.

## Contribute

If you would like to contribute to the project, please follow these steps:
1. Fork the repository
2. Open a new branch (`git checkout -b feature/YourFeature`)
3. Commit the changes (`git commit -m 'Add some feature'')
4. Push the branch (`git push origin feature/YourFeature`)
5. Create a pull request

## Litsenziya

This project is distributed under the MIT license. See the [LICENSE](LICENSE) file for details.


Thank you for your interest in the project!

