# **Credit Card Fraud Detection**

## **Project Overview**
This project aims to detect fraudulent credit card transactions using machine learning techniques. The primary objective is to accurately classify transactions as fraudulent or genuine while addressing class imbalance in the dataset.

## **Challenges Encountered**
1. **Class Imbalance:** Fraudulent transactions were significantly outnumbered by genuine ones, requiring advanced resampling techniques such as SMOTE (Synthetic Minority Oversampling Technique) for effective training.
2. **Performance and Time Constraints:** Due to the size of the dataset, processing the entire data set took significant time. To address this, a sampled dataset was used for quicker iteration and model training.
3. **Feature Scaling:** Ensuring the features were scaled appropriately to improve model convergence and accuracy.
4. **Hyperparameter Tuning:** Optimizing the Random Forest model required careful tuning of parameters using RandomizedSearchCV.

---

## **Dataset**
- **Input:** A dataset containing labeled transactions where:
  - `0` indicates a genuine transaction.
  - `1` indicates a fraudulent transaction.
- The dataset was preprocessed to ensure there were no missing values.

---

## **Approach**
### **1. Data Preprocessing**
- **Sampling:** Used 10% of the data to speed up experimentation.
- **Handling Class Imbalance:** Applied SMOTE to generate synthetic samples of the minority class (fraudulent transactions).
- **Feature Scaling:** Standardized all features using `StandardScaler` to ensure uniformity and better model performance.

### **2. Model Training**
Two classification models were implemented:
- **Random Forest Classifier:** Tuned using `RandomizedSearchCV` to optimize hyperparameters.
- **Logistic Regression:** Used with balanced class weights to address the class imbalance.

### **3. Model Evaluation**
Evaluation metrics used:
- **Precision, Recall, and F1-Score:** To balance the trade-off between false positives and false negatives.
- **Confusion Matrix:** To visualize classification results.
- **AUC-ROC Curve:** To measure the model’s ability to distinguish between classes.
- **Precision-Recall Curve:** To evaluate the precision-recall trade-off.

### **4. Visualization**
- Correlation heatmaps were used to analyze feature relationships.
- ROC and Precision-Recall curves were plotted to visualize model performance.

---

## **Key Findings**
- **Random Forest:** Achieved perfect classification results (AUC = 1.00) with no false positives or negatives, making it the most reliable model for this task.
- **Logistic Regression:** Performed exceptionally well (AUC = 1.00) but had slightly lower scores in precision and recall compared to Random Forest.

Both models demonstrated excellent fraud detection capabilities, but the Random Forest model showed a slight edge due to its perfect classification.

---

## **Conclusion**
This project demonstrates that machine learning models, specifically Random Forest and Logistic Regression, can effectively detect fraudulent credit card transactions. By addressing class imbalance and using advanced evaluation techniques, the models achieved high accuracy and reliability.

For further exploration, the model can be tested on larger datasets and extended with deep learning techniques for improved scalability and precision.

--- 
