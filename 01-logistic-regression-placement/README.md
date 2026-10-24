# Logistic Regression: Placement Prediction

Problem: Predict whether a student gets placed, based on CGPA and IQ.

Dataset: 'placement.csv', 100 rows with the columns 'cgpa', 'iq' and 'placement' (0 = not placed, 1 = placed).
Source: [CampusX repo](https://github.com/campusx-official/placement-project-logistic-regression)

**Notebook:** [logistic_regression_placement.ipynb](./logistic_regression_placement.ipynb)

## Approach

1. Load the data and drop the extra index column
2. Separate input columns (cgpa, iq) from the output column (placement)
3. Scale the features with 'StandardScaler'
4. Split into train and test sets
5. Train a 'LogisticRegression' model
6. Evaluate with 'accuracy_score'
7. Plot the decision regions with 'mlxtend'

## Result

- Test accuracy: 0.90

## What I learned

- Scaling: CGPA ranges from about 4 to 9, while IQ ranges from about 40 to 200. Without scaling, the larger IQ values can dominate the model. 'StandardScaler' puts both on a similar scale so the model treats them fairly.
- Logistic regression vs linear regression: Linear regression predicts a continuous number. Logistic regression passes a linear combination of the inputs through the sigmoid function to get a probability between 0 and 1, then classifies it (placed or not placed).
- Decision boundary: The plot shows a straight line separating the "placed" and "not placed" regions. Logistic regression can only draw a linear boundary, so it works well when the classes are roughly separable by a line.
- Train/test split: I fit the scaler on the training data only, then applied it to the test data, so no information from the test set leaks into training.
- Result: The model reached 0.90 accuracy on the test set. With only 100 rows, a single split can be misleading, so I want to verify this with cross-validation.

