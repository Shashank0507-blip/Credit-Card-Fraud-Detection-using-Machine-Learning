## **Results Obtained by training and testing the model:**

### **Without using the feature selection process:**
* Model Accuracy : 0.9983
* Model Precision : 0.5000
* Model Recall : 0.8878
* Model F1 Score : 0.6397

### **These are the following values obtained while using the feature selection process:**
* Model Accuracy : 0.9938
* Model Precision : 0.2042
* Model Recall : 0.8980
* Model F1 Score : 0.3327

### **Key Things to note while using the feature selection process:**
* A combination of mutual information and recursive feature elimination were used in the process of feature selection in this scenario.
* the output of mutual information which gave us the information on how each feature was affecting the output , and we used this information to select the top contributing features.
* This is given to recursive feature elimination(RFE) as an input.
* However this provided comparatively results of lower value, as a lot of features were removed. So we decided to include every feature to train and test the data.
