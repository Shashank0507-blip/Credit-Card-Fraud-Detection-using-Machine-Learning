## **Project Overview:**

### **This project focuses on detecting fraudulent credit card transactions using lightgbm, a powerful gradient boosting algorithm. It includes:**
Data preprocessing & feature engineering,
Model training and evaluation,
Saving the trained model for real-world predictions,
User-friendly input handling for new transactions.

   *  If any missing values are found, we either impute them or remove them.
      Since we collect user inputs, we replace missing values (with suitable estimates.

   *  The dataset contains Time, Amount, and 28 PCA-transformed features (V1-V28).
      Feature Scaling: Since transaction amounts vary widely, we use MinMaxScaler to bring all values into a standard range (0 to 1) to ensure fair model performance.
   
   *  Fraudulent transactions are rare (~0.17% of total data).
      We check for extreme outliers that might skew the model.

### **Once the data is preprocessed, we train an "LIGHTGBM" Classifier to detect fraud. Here’s the process that was used:**
   * **Train-Test Split:**
     The dataset is split into training (80%) and testing (20%) to evaluate performance.

   *  **Model Selection:**
      We use lightgbm, which is an optimized gradient boosting technique.

   *  **Hyperparameter Tuning:**
      We apply "Bayesian Search" to find the best hyperparameters like:
      learning_rate, max_depth, n_estimators, colsample_bytree and subsample.


### **Link to download the dataset:**
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud


