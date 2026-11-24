# FraudGuard — Credit Card Fraud Detection

A machine learning project designed to identify potentially fraudulent credit card transactions using classification algorithms.

The project focuses on handling imbalanced transaction data, comparing machine learning models, and evaluating fraud detection performance.

## Project Overview

FraudGuard uses transaction data to classify credit card transactions as either **legitimate** or **fraudulent**.

Two machine learning algorithms are implemented:

- **Logistic Regression**
- **Random Forest Classifier**

The models are evaluated using Precision, Recall, F1-score, and Average Precision.

## Dataset

The project uses the **Credit Card Fraud Detection** dataset, accessed through OpenML (Dataset ID: 1597).

- Original dataset: 284,807 transactions
- Selected subset: 15,150 transactions
- Legitimate transactions: 15,000
- Fraudulent transactions: 150
- Training/testing split: 80% / 20%

The subset was selected to reduce computational requirements while retaining examples of both classes.

## Technologies Used

- Python
- Pandas and NumPy
- Scikit-learn
- Matplotlib and Seaborn
- Google Colab / Jupyter Notebook

## Machine Learning Workflow

1. **Data Loading:** Retrieve the dataset from OpenML.
2. **Data Preparation:** Create a smaller subset and analyze class distribution.
3. **Train-Test Split:** Split the data using stratified sampling.
4. **Model Training:** Train Logistic Regression and Random Forest classifiers.
5. **Model Evaluation:** Compare classification metrics.
6. **Visualization:** Analyze confusion matrices and Precision-Recall curves.

## Model Performance

The following results were obtained on the selected test subset:

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Precision | 30.68% | 100.00% |
| Recall | 90.00% | 80.00% |
| F1-score | 45.76% | 88.89% |
| Average Precision | 88.74% | 89.63% |

**Random Forest** achieved the highest F1-score and Average Precision.

It correctly identified 24 out of 30 fraudulent transactions in the test set, with no false positives, but missed 6 fraudulent transactions.

## Visualizations

The notebook includes:

- Transaction class distribution
- Confusion matrices for both models
- Precision-Recall curves

## Limitations

The project uses a sampled subset of the original dataset, with a deliberately increased proportion of fraudulent transactions.

Therefore, the reported performance may not reflect real-world fraud detection results. The models have not been validated for production use.

## Future Improvements

- Hyperparameter tuning and cross-validation
- Decision threshold optimization
- Evaluation on the original transaction distribution
- Additional feature engineering

## How to Run

1. Open the project notebook in Google Colab or Jupyter Notebook.
2. Install the required Python libraries if necessary.
3. Run the notebook cells in order.
4. Review the model evaluation results and visualizations.

The dataset is loaded automatically from OpenML.

## Conclusion

FraudGuard demonstrates a complete introductory machine learning workflow for detecting credit card fraud, with a focus on classification, imbalanced data, and model evaluation.
