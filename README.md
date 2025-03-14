# Machine Learning Coursework 1: Predicting Oral Temperature & Fever Detection

This project is an end-to-end machine learning application that uses sensor-collected infrared thermography data to predict oral temperature and detect fever. The work encompasses data exploration, preprocessing, regression and classification model development, hyperparameter tuning, and model evaluation.

## Project Overview

The primary objectives of this project are to:
- **Predict Oral Temperatures:**  
  Estimate the oral temperature measured in fast mode (`aveOralF`) and monitor mode (`aveOralM`) using thermal image readings and environmental variables.
  
- **Detect Fever:**  
  Classify whether a person has a fever based on the oral temperature measurements (fever defined as ≥ 37.5°C).

The project tackles both a regression task (predicting continuous temperature values) and a classification task (detecting fever).

## Dataset

The dataset, known as the Infrared Thermography Temperature Dataset, contains:
- **33 features:** Including gender, age, ethnicity, ambient conditions (temperature, humidity, distance), and various thermal readings from infrared images.
- **Targets:**
  - **Regression:** `aveOralF` and `aveOralM` (oral temperature readings in fast and monitor modes).
  - **Classification:** Derived fever variables based on whether the oral temperature meets or exceeds 37.5°C.

**Data Source:**  
The dataset was obtained from the [UCI Machine Learning Repository](https://github.com/uci-ml-repo/ucimlrepo).

## Methodology

The project follows a structured approach:
1. **Exploratory Data Analysis (EDA):**
   - Analyze the distribution of target variables.
   - Visualize correlations between thermal readings and oral temperature.
   - Investigate class imbalance in fever detection.

2. **Data Preparation:**
   - Handle missing values (mean imputation for numerical features and mode imputation for categorical features).
   - Encode categorical variables and scale numerical features.
   - Split the data into training and testing sets.

3. **Model Development:**
   - **Regression Models:** Linear Regression, Random Forest Regressor, Neural Network (MLP Regressor), and XGBoost Regressor.
   - **Classification Models:** Logistic Regression, Random Forest, Neural Network (MLP Classifier), and XGBoost.
   - Develop pipelines to ensure reproducible preprocessing and modeling.
   - Evaluate models using appropriate metrics (MSE, RMSE, R² for regression; accuracy, precision, recall, F1, ROC AUC, and Precision-Recall curves for classification).

4. **Model Optimization:**
   - Employ GridSearchCV to systematically explore hyperparameters, boosting model performance.
   - Compare different models based on performance metrics and visualizations.

5. **Feature Importance Analysis:**
   - Use tree-based models to assess the importance of various predictors.
   - Confirm that key thermal readings (e.g., maximum facial or canthal temperatures) are the strongest indicators of oral temperature.

6. **Final Model Comparison & Conclusion:**
   - Summarize findings from both regression and classification tasks.
   - Discuss trade-offs, potential improvements, and practical implications for non-contact fever screening.

## How to Run the Notebook

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/malorieiovino/Machine_Learning_CW1.git
   cd Machine_Learning_CW1

