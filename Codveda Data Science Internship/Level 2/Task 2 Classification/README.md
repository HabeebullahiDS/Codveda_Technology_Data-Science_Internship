# Level 2, Task 2: Classification

**Codveda Technology | Data Science Internship**

## Objective
Build and compare classification models on two datasets: iris species and customer churn.

## Datasets
- `iris.csv`: 150 flowers, 4 measurements, 3 balanced species (50 each). Split 120 / 30.
- `churn-bigml-80.csv` (training, 2,666 customers) and `churn-bigml-20.csv` (test, 667 customers).

## Approach
1. Prepared both datasets (encoding, removal of redundant columns, scaling).
2. Trained Logistic Regression, Decision Tree, Random Forest and SVM.
3. Evaluated with accuracy, precision, recall, F1 and ROC AUC.
4. Addressed class imbalance in the churn data with balanced class weights.
5. Confirmed results with five-fold cross-validation.

## Key Results
- **Iris:** Logistic Regression 93.3% accuracy (28 of 30 flowers), SVM 96.7%. The difference is one flower.
- **Churn:** predicting "stayed" for everyone is 85.8% accurate, so accuracy alone is misleading.
- Balanced class weights raised logistic recall from 0.18 to 0.76.
- Random Forest was the most dependable model: cross-validated F1 0.757 and AUC 0.906.

## Files
- `Level2_Task2_Classification.ipynb`
- `iris.csv`, `churn-bigml-80.csv`, `churn-bigml-20.csv` (inputs)

## Libraries
pandas, numpy, matplotlib, seaborn, scikit-learn
