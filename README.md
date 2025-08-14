# Heart Disease Prediction

## Objective
The aim of this project was to develop a predictive model that can determine whether an individual is likely to have heart disease using their health-related attributes.

---

## Dataset

- **Source:** [Heart Disease UCI Dataset (Kaggle)](https://www.kaggle.com/ronitf/heart-disease-uci)  
- **Target Variable:** `target`  
  - `1` → Heart disease present  
  - `0` → No heart disease  

---

## Workflow Summary

### 1. Data Loading and Preprocessing
- Imported the dataset using **Pandas**.
- Checked and confirmed there were **no missing entries**.
- Verified and adjusted **data types** where necessary to ensure compatibility for modeling.

---

### 2. Exploratory Data Analysis (EDA)
- Generated descriptive statistics using `.describe()` to get an overview of data distribution.
- Examined **target variable counts** to assess class distribution.
- Created a **heatmap** of the correlation matrix to visualize feature relationships.

**Key Observations:**
- Features such as `cp` (chest pain type), `thalach` (maximum heart rate achieved), and `oldpeak` (ST depression) showed notable correlations with the likelihood of heart disease.

---

### 3. Feature Selection and Data Splitting
- Defined **X** as the set of predictors and **y** as the target variable.
- Split the dataset into:
  - **80%** Training data
  - **20%** Testing data

---

### 4. Model Development
Two models were built for comparison:
1. **Logistic Regression**
2. **Decision Tree Classifier**

---

### 5. Performance Evaluation
**Metrics Applied:**
- Accuracy
- Confusion Matrix
- ROC Curve with AUC score

**Results:**

#### Logistic Regression
- Accuracy: ~78%  
- ROC-AUC: 0.88  
- Produced a smooth ROC curve indicating consistent performance.

#### Decision Tree
- Accuracy: ~99%  
- ROC-AUC: 0.99  
- Outperformed Logistic Regression in both metrics.

*Confusion matrices for each model provided insight into correct and incorrect predictions (true/false positives and negatives).*

---

### 6. Feature Significance
- **Logistic Regression:** Coefficients highlighted which variables had the strongest influence.
- **Decision Tree:** Ranked feature importance showed:
  1. `cp` (Chest pain type)  
  2. `thalach` (Maximum heart rate achieved)  
  3. `oldpeak` (ST depression)

---

## Conclusion
- **Best Performing Model:** Decision Tree  
- **Reason:** Superior accuracy and ROC-AUC compared to Logistic Regression, while maintaining strong predictive power on test data.  
- **Key Influencing Features:** `cp`, `thalach`, `oldpeak` — significant indicators of heart disease risk.
