# Level 2, Task 1: Predictive Modelling (Regression)

**Codveda Technology | Data Science Internship**

## Objective
Predict house prices and compare regression models.

## Dataset
`house_data.csv`: 506 houses, 14 columns. Target: `MEDV`, median house price in $1,000s. Training and test split: 404 / 102.

## Approach
1. Loaded the data with column names taken from the dataset documentation.
2. Checked for missing values and duplicates (none found).
3. Trained Linear Regression, Decision Tree and Random Forest.
4. Evaluated with MSE, RMSE and R-squared.
5. Reviewed feature importance and the effect of removing the `B` column.

## Key Results
| Model | Test R-squared |
|---|---|
| Linear Regression | 0.69 |
| Decision Tree / Random Forest | about 0.88 |

- Random Forest: test MSE 8.72, RMSE 2.95 (Linear Regression MSE 22.78).
- Rooms (`RM`) and lower-status share (`LSTAT`) account for about 82% of the forest's splits.

## Ethical Note
The `B` column is derived from the racial composition of each town and was excluded. Including it changed Linear Regression R-squared only from 0.712 to 0.715.

## Files
- `Level2_Task1_Regression.ipynb`
- `house_data.csv` (input)

## Libraries
pandas, numpy, matplotlib, seaborn, scikit-learn
