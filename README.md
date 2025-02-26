Project Overview:

This project focuses on detecting fraudulent credit card transactions using lightgbm, a powerful gradient boosting algorithm. It includes:
Data preprocessing & feature engineering
Model training and evaluation
Saving the trained model for real-world predictions
User-friendly input handling for new transactions

1. If any missing values are found, we either impute them or remove them.
   Since we collect user inputs, we replace missing values (with suitable estimates.
2. The dataset contains Time, Amount, and 28 PCA-transformed features (V1-V28).
   Feature Scaling: Since transaction amounts vary widely, we use MinMaxScaler to bring all values into a standard range (0 to 1) to ensure fair model performance.
3.Fraudulent transactions are rare (~0.17% of total data).
  We check for extreme outliers that might skew the model.
Once the data is preprocessed, we train an "LIGHTGBM" Classifier to detect fraud. Here’s the process that was used:

Train-Test Split:
The dataset is split into training (80%) and testing (20%) to evaluate performance.

Model Selection:
We use lightgbm, which is an optimized gradient boosting technique.

Hyperparameter Tuning:
We apply "Bayesian Search" to find the best hyperparameters like:
learning_rate, max_depth, n_estimators, colsample_bytree and subsample.

Results Obtained by training and testing the model:

Without using the feature selection process:

Model Accuracy : 0.9983
Model Precision : 0.5000
Model Recall : 0.8878
Model F1 Score : 0.6397

Using the feature selection process:
A combination of mutual information and recursive feature elimination were used in the process of feature selection in this scenario.
the output of mutual information which gave us the information on how each feature was affecting the output , and we used this information to select the top contributing features and gave it to recursive feature elimination(RFE) as an input.
However this provided comparatively results of lower value, as a lot of features were removed. So we decided to include every feature to train and test the data.

These are the following values obtained while using the feature selection process:

Model Accuracy : 0.9938
Model Precision : 0.2042
Model Recall : 0.8980
Model F1 Score : 0.3327


