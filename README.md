# Codveda Technology Data Science Internship

Six projects across three levels, each in its own folder with a notebook, dataset and README.

**Author:** Suleiman Habeebulahi

---

## Projects at a Glance

| Level | Task | Dataset | Best Result |
|---|---|---|---|
| 1 | Data Cleaning and Preprocessing | Telecom churn (2,666 customers) | 154 outliers removed; churn rate stable at 14.3% |
| 1 | Exploratory Data Analysis | Cleaned churn data (2,512 customers) | 4+ service calls: 53.5% churn |
| 2 | Regression | Boston housing (506 houses) | Random Forest R² ≈ 0.88 |
| 2 | Classification | Iris (150) and churn (2,666 / 667) | Random Forest churn F1 0.757 |
| 3 | Time Series Analysis | Airline passengers (144 months) | Holt-Winters RMSE 32.5 |
| 3 | NLP Text Classification | Sentiment texts (732) | Balanced Logistic Regression macro F1 0.714 |

---

## Repository Structure

```
├── Level-1/
│   ├── Task-2-Data-Cleaning-Preprocessing/
│   └── Task-3-Exploratory-Data-Analysis/
├── Level-2/
│   ├── Task-1-Regression/
│   └── Task-2-Classification/
└── Level-3/
    ├── Task-1-Time-Series-Analysis/
    └── Task-2-NLP-Text-Classification/
```

Each task folder contains the notebook, its input data and a README.

---

## Level 1

### Task 2: Data Cleaning and Preprocessing
Prepared the telecom customer churn data for modelling: standardised column names, checked for missing values and duplicates, corrected data types, removed outliers with the IQR rule, encoded categories and scaled numeric features.
- 154 customers (5.8%) removed as outliers; churn rate moved from 14.6% to 14.3%.
- Output: a clean file of 2,512 customers.

### Task 3: Exploratory Data Analysis
Explored what separates customers who churn from those who stay.
- Customers with 4 or more service calls churn at 53.5%, against 10.9% for all others.
- International plan holders churn at 42.1%, against 11.2% without the plan.
- The top 25% of day usage churn at 28.3%, against 9.7% for the rest.

---

## Level 2

### Task 1: Regression
Predicted median house prices with Linear Regression, Decision Tree and Random Forest.
- Linear Regression R² 0.69; Random Forest about 0.88 (test MSE 22.78 down to 8.72).
- Rooms and lower-status share account for about 82% of the Random Forest's splits.
- The `B` column was excluded on ethical grounds; including it changed R² by only 0.003.

### Task 2: Classification
Compared Logistic Regression, Decision Tree, Random Forest and SVM on iris species and customer churn.
- Iris: Logistic Regression 93.3% accuracy, SVM 96.7% (a difference of one flower).
- Churn: predicting "stayed" for everyone is 85.8% accurate, so accuracy alone is misleading.
- Balanced class weights raised logistic recall from 0.18 to 0.76.
- Random Forest was the most dependable: cross-validated F1 0.757 and AUC 0.906.

---

## Level 3

### Task 1: Time Series Analysis
Decomposed and forecast monthly airline passengers (1949 to 1960), testing on the final 24 months.

| Model | RMSE |
|---|---|
| Holt-Winters | 32.49 |
| SARIMA(0,1,1)(0,1,1,12) | 43.17 |
| Seasonal naive | 76.99 |
| Simple exponential smoothing | 137.33 |

- Average monthly passengers grew 276%; July and August are the peak months.
- All forecasts fall below the actual 1960 peaks.

### Task 2: NLP Text Classification
Classified short texts as Positive, Negative or Neutral using TF-IDF features.

| Model | Test macro F1 | Cross-validated macro F1 |
|---|---|---|
| Baseline (always Positive) | 0.257 | - |
| Naive Bayes | 0.672 | 0.592 |
| Logistic Regression | 0.623 | 0.592 |
| Logistic Regression (balanced) | 0.714 | 0.732 |

- The 191 original emotion labels were grouped into three classes; the grouping is the analyst's judgement.
- The model relies mainly on emotion keywords, so scores may be optimistic on everyday text.

---

## Tools and Libraries
Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn, statsmodels, NLTK

## How to Run
1. Clone the repository.
2. Install the libraries: `pip install pandas numpy matplotlib seaborn scikit-learn statsmodels nltk jupyter`
3. Open any task folder and run its notebook; the dataset is in the same folder.
