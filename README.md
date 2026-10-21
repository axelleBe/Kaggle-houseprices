# House Prices: Advanced Regression Techniques (work in progress)

> **Status: in progress.** This repo documents my work on the Kaggle
> [House Prices](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
> competition, started in October 2026. The notebooks are being written step by step,
> and a full README will be added once the baseline and first experiments are finished.

## Goal

Predict the sale price of houses in Ames, Iowa from 79 features. The competition metric
is the RMSE between the log of the predicted price and the log of the real price, so I
train on `log1p(SalePrice)`.

## Approach

I use this project to practice a clean, leak-free ML workflow:

- scikit-learn `Pipeline` and `ColumnTransformer`, so every preprocessing step is
  fitted on training data only
- 5-fold cross-validation as the main evaluation tool, instead of the public leaderboard
- one change at a time, with an experiment log (change, CV score, spread across folds)

## Progress

- [x] Data exploration (`notebooks/01_exploration.ipynb`): target distribution, missing
      values (what "NA" means in each column), column types, relationship with the target
- [ ] Baseline pipeline with Ridge regression and cross-validated score
- [ ] Experiments: feature engineering, encodings, outliers, other models
- [ ] Final write-up: results table, what worked, what did not

