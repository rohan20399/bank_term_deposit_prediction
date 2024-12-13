# Bank Term Deposit Prediction

## Overview
This repository contains resources for a machine learning project aimed at predicting customer subscriptions to term deposits based on the Bank Marketing dataset. The project leverages data preprocessing, exploratory data analysis (EDA), and multiple classification models to achieve actionable insights and high predictive accuracy.

## Repository Contents
- **Dataset**: `bank-full.csv`
  - Contains 45,211 records with 17 features, including customer demographics, financial indicators, and marketing campaign details.
- **Jupyter Notebook**: `term_deposit_prediction.ipynb`
  - Implements data preprocessing, feature engineering, and classification models.
  - Includes visualizations for EDA and evaluation metrics like AUC and LIFT curves.

## Running the Project
The notebook can be uploaded and run on AWS using an Amazon SageMaker instance. The following configuration is recommended:
- **Instance Type**: `ml.t3.xlarge`
- **Software**: Jupyter Notebook instance with required Python libraries installed (e.g., `scikit-learn`, `pandas`, `matplotlib`).

### Instructions
1. Upload `bank-full.csv` and `term_deposit_prediction.ipynb` to your environment.
2. Open the notebook and follow the code execution sequence.
3. During execution, you will be prompted twice:
   1. **Method for handling class imbalance**: Enter `SMOTE` or `undersampling` as per your preference.
   2. **Classification model selection**: Choose one of the following:
      - Logistic Regression
      - Decision Tree
      - Random Forest
      - Gradient Boosting

## Project Workflow
1. **EDA and Preprocessing**:
   - Visualize outliers and correlations.
   - Perform feature scaling and encoding.
   - Handle missing values and outliers.
2. **Feature Engineering**:
   - Generate new features, e.g., `contact_rate` and `balance_category`.
   - Apply feature selection (`SelectKBest`) and dimensionality reduction (PCA).
3. **Classification Models**:
   - Train and evaluate models using accuracy, AUC, and LIFT curves.
   - Use hyperparameter tuning (`RandomizedSearchCV`) for model optimization.

## Key Results
The project compares the performance of multiple models:

- **Logistic Regression**: Accuracy = 0.8012, AUC = 0.8675
- **Decision Tree**: Accuracy = 0.7895, AUC = 0.8239
- **Random Forest**: Accuracy = 0.8540, AUC = 0.8658
- **Gradient Boosting**: Accuracy = 0.8101, AUC = 0.8789

**Key Observations**:
- Gradient Boosting achieved the best AUC score, indicating strong generalization and ranking ability.
- Random Forest provided the highest accuracy, demonstrating robustness in predictions.
- Logistic Regression performed well despite its simplicity, offering interpretable results.
- Decision Tree models were prone to overfitting, as shown by slightly lower AUC scores.

## Dependencies
Install the required Python libraries using:
```bash
pip install -r requirements.txt
```

