---
description: >-
  Some added parameters to the Linear Regression that makes it deal with noisy
  data.
---

# Ridge Regression and Lasso Regression

## Why Ridge Regression?

While ordinary least squares regression is a good way to fit a linear model onto a dataset, it relies on the fact that the dataset's features are each independent, i.e. uncorrelated. When many of the dataset features are linearly correlated, e.g. if a dataset has multiple features depicting the same price in different currencies, it makes the least-squares regression model highly sensitive to noise in the data.

For regularization, the goal is to not only minimize the sum of squared residuals but to do this with coefficients as small as possible. The smaller the coefficients, the less susceptible they are to random noise in the data. The most commonly used form of regularization is [ridge regularization](https://en.wikipedia.org/wiki/Tikhonov\_regularization).

With ridge regularization, the goal is now to find the weights that minimize the following quantity:

![Ridge Regression](<../.gitbook/assets/image (2).png>)

where α(best chose with CV) is a non-negative real number hyperparameter and ||w||2 represents the L2 norm of the weights.

The Extra Term is referred to as a penalty term since it penalizes larger weight values

[Notebook Demonstration.](https://github.com/RheagalFire/L2-Regularization)

## Lasso Regression

Penalty Term uses L1 norm instead of L2

![L1 Norm Lasso Regression](<../.gitbook/assets/image (4) (1).png>)

This means that it will likely zero out some of the weight coefficients. This reduces the number of features that the model is actually dependent on (since some of the coefficients will now be 0), which can be beneficial when some features are completely irrelevant or duplicates of other features.

##
