# BankData

Our dataset comes from the UCI Machine Learning repository [link](https://archive.ics.uci.edu/ml/datasets/bank+marketing).  The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns.  We will make use of the article accompanying the dataset [here](CRISP-DM-BANK.pdf) for more information on the data and features.

## Business Objective

The business objective was to increase the efficiency of our marketing campaigns so that fewer contacts could be made to acquire new contracts, with a high accuracy rate.

To accomplish this objective, we created and compared several different types of classification models.

## Results

The complete Jupyter Notebook for our research is available [here](./prompt_III.ipynb)!

In summary, we did the following:
1. Determined that 'precision' is the appropriate model performance metric.
2. Ran grid searches to tune hyperparameters for each of Decision Tree, K-Nearest Neighbors, Logistic Regression, and Support Vector Machine models.
3. Settled on a hybrid model which combines Decision Tree and KNN models (using a simple boolean or operation)

The results showed significant improvement in the precision of the resulting hybrid model, with essentially equivalent accuracy.

| Model Comparison                             | Accuracy | Precision |
|----------------------------------------------|----------|-----------|
| k Nearest Neighbors or Decision Tree         | 0.896845 | 0.666667  |
| k Nearest Neighbors or Logistic Regression   | 0.791262 | 0.287234  |
| k Nearest Neighbors or Support Vector Machine| 0.837379 | 0.345588  |
| Decision Tree or Logistic Regression         | 0.791262 | 0.287234  |
| Decision Tree or Support Vector Machine      | 0.837379 | 0.345588  |
| Logistic Regression or Support Vector Machine| 0.776699 | 0.276699  |
| All                                          | 0.776699 | 0.276699  |

Of particular interest are the economic condition features which have the highest importance in the Decision Tree model:
1. Outcome of the previous camapign
2. Variable Employment Rate
3. Consumer Confidence Index

Full analysis and recommendations can be found [here](./prompt_III.ipynb#Final Analysis and Recommendations)