## Project Goal
This project is to apply k-nearest neighbors and cross-validation to tackle the California median house value.

## Introduction
This project has three parts:

* Part I: Experimental Setup
* Part II: Nearest Neighbor and Cross-Validation
* Part III: Overfitting in Model Selection and Nested Cross Validation

For part I and II we will consider a regression problem. For these first two parts, we will be working with a modified version of the California Housing Dataset (cal_housing_data_clean.csv).
For part III we will consider a classification problem. We will not be using the California Housing Dataset but rather synthetic data that we generate.

## Dataset
In this project, we will be using a version of the [California Housing Prices Dataset](https://scikit-learn.org/stable/datasets/real_world.html#california-housing-dataset) with additional information.

## Key Findings
* k-NN captures non-Linear relationships
Compared to linear regression, the k-NN model better captured complex, non-linear patterns in housing prices, especially in high-value areas. This highlights the flexibility of k-NN in modeling real estate data.

* Optimal k improves performance
Through cross-validation, the best-performing model used a moderate value of k (e.g., k=5 or k=10). Lower values of k led to overfitting, while higher values smoothed the predictions too much and underfit the data.

* Model performance improved over linear regression
The R² score was higher than that of linear regression, suggesting that k-NN provided a more accurate fit to the housing price data. However, performance gains were modest and came with increased computational cost.

* Feature scaling was essential
Standardization of features was critical for k-NN, since the algorithm is distance-based. Without scaling, results were unreliable and heavily skewed by features with larger numeric ranges (e.g., population).

* Computational cost increased with k-NN
Although k-NN provided improved predictions, inference time was slower, especially for large datasets, since k-NN stores the full training set and computes distances at prediction time.
