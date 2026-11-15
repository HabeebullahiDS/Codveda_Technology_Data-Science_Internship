# Level 1, Task 3: Exploratory Data Analysis (EDA)

**Codveda Technology | Data Science Internship**

## Objective
Identify what separates customers who churn from those who stay.

## Dataset
`churn_cleaned.csv`: 2,512 customers, 20 columns (output of Task 2). Churn rate: 14.3%.

## Approach
1. Summary statistics and skewness.
2. Distributions of the main numeric variables.
3. Scatter plots and box plots, churned versus retained customers.
4. Churn rate by plan type, service calls, daytime usage and state.
5. Correlation analysis and detection of redundant features.

## Key Results
- Customers with 4 or more service calls churn at 53.5%, against 10.9% for all others.
- International plan holders churn at 42.1%, against 11.2% without the plan.
- The top 25% of day usage churn at 28.3%, against 9.7% for the rest.
- Minutes and charge columns are perfectly correlated (1.00); one column from each redundant pair is kept for modelling.

## Files
- `Level1_Task3_EDA.ipynb`
- `churn_cleaned.csv` (input)

## Libraries
pandas, numpy, matplotlib, seaborn
