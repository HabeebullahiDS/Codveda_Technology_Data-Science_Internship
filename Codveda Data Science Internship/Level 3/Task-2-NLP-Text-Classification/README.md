# Level 3, Task 2: NLP Text Classification (Sentiment Analysis)

**Codveda Technology | Data Science Internship**

## Objective
Classify short texts as Positive, Negative or Neutral.

## Dataset
`sentiment_dataset.csv`: 732 texts with 191 emotion labels, grouped into three classes. After removing 26 repeated texts: 445 Positive, 192 Negative, 69 Neutral. Split 564 / 142.

## Approach
1. Grouped the emotion labels into three classes (the grouping is the analyst's judgement and is shown in the notebook).
2. Preprocessed text: tokenisation, stopword removal (negations kept), stemming.
3. Converted text to numbers with TF-IDF (972 terms, single words and word pairs).
4. Trained Naive Bayes and Logistic Regression (plain and with balanced class weights).
5. Evaluated with precision, recall, macro F1 and five-fold cross-validation.

## Key Results
| Model | Test macro F1 | Cross-validated macro F1 |
|---|---|---|
| Baseline (always Positive) | 0.257 | - |
| Naive Bayes | 0.672 | 0.592 |
| Logistic Regression | 0.623 | 0.592 |
| Logistic Regression (balanced) | 0.714 | 0.732 |

- The balanced model found 6 of 14 Neutral test texts, against 3 and 2 for the others.
- The model relies mainly on emotion keywords, so scores may be optimistic on everyday text.

## Files
- `Level3_Task2_NLP_Text_Classification.ipynb`
- `sentiment_dataset.csv` (input)

## Libraries
pandas, numpy, matplotlib, seaborn, nltk, scikit-learn
