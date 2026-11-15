# Level 1, Task 2: Data Cleaning and Preprocessing

**Codveda Technology | Data Science Internship**

## Objective
Prepare the telecom customer churn data for analysis and modelling.

## Dataset
`churn-bigml-80.csv`: 2,666 customers, 20 columns (plans, call minutes, calls, charges, customer service calls, churn).

## Approach
1. Standardised column names (lower case, underscores).
2. Checked for missing values and duplicates (none found).
3. Corrected data types (`churn` to 1/0, `area_code` to a label).
4. Detected and removed outliers with the IQR rule (k = 1.5) on eight usage columns.
5. Encoded categories: label encoding for the two plan columns, one-hot encoding for state and area code.
6. Standardised 15 numeric columns with `StandardScaler`.

## Key Results
- 154 customers removed as outliers (5.8%); churn rate moved from 14.6% to 14.3%.
- Final files: `churn_cleaned.csv` (2,512 x 20, readable) and `churn_preprocessed_scaled.csv` (2,512 x 70, fully numeric).

## Files
- `Level1_Task2_Data_Cleaning_Preprocessing.ipynb`
- `churn-bigml-80.csv` (input)

## Libraries
pandas, numpy, matplotlib, seaborn, scikit-learn
