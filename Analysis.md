## Results & Analysis

### Part 1 – Loan Repayment Prediction

#### Logistic Regression

- **Accuracy:** 0.689  
- **F1 (Charged Off):** 0.425  
- **ROC AUC:** 0.70  

**Top Coefficients**  
- `grade`: 0.232  
- `int_rate`: 0.072  
- `term`: 0.020  

**Analysis:**  
The logistic model’s AUC of 0.70 indicates fair discrimination between repaid and defaulted loans.  
The positive weight on `grade` and `int_rate` shows that lower grades and higher interest rates are associated with higher default risk.  
The relatively low F1 for “Charged Off” (0.43) stems from class imbalance—only ~20% of loans default.

#### Random Forest

- **Accuracy:** 0.648  
- **F1 (Charged Off):** 0.432  
- **ROC AUC:** 0.71  

**Feature Importances**  
- `int_rate`: 0.452  
- `grade`: 0.379  
- `term`: 0.169  

**Analysis:**  
The random forest slightly improves AUC and recall for defaults.  
The high importance of `int_rate` underscores its predictive power: borrowers paying higher rates tend to default more.  
`term` plays a smaller role, suggesting loan duration is less decisive than credit grade and cost.

---

### Part 2 – DTI & Grade Analysis

- **Point‑biserial correlation (DTI vs default):** 0.099  

**Mean DTI**  
- Charged Off: 21.31  
- Fully Paid: 18.63  

**Analysis:**  
A correlation near zero indicates DTI alone has limited linear association with default.  
Yet the mean shift and boxplots show a tendency toward higher DTI among charged‑off loans.  
This suggests non‑linear effects or interaction with other borrower characteristics.

#### MLPClassifier on `[DTI, grade]`

- **Accuracy:** 0.792  
- **F1 (Charged Off):** 0.171  
- **ROC AUC:** 0.71  

**Analysis:**  
The MLP achieves high overall accuracy by predicting the majority “Fully Paid” class, but recall for defaults is very low (0.10).  
Its ROC AUC matches simpler models, confirming that DTI and grade alone cannot fully separate defaulters.  
Additional features are needed to improve detection of at‑risk loans.  
