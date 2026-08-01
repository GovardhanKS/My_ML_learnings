# My ML Learnings — Linear Regression

Practice notebooks covering simple and multiple linear regression, kept
together with the datasets they load.

## Notebooks

- **LinearRegressionLearn_v1.ipynb** — original: fits `X -> Y` and `X -> Z`
  toy models from `data_2026.csv` with scikit-learn, plots the fits, and
  attempts regression statistics (coefficient, std error, t-score, p-value).
- **LinearRegressionLearn_v2.ipynb** — cleaned-up version of v1. v1's stats
  cell called `model.score()` expecting those four values, but scikit-learn's
  `.score()` only returns R², which raised a `TypeError`. v2 fixes this by
  using `statsmodels.OLS` for proper regression stats on *both* the Y and Z
  models, and drops unrelated one-off cells (downloading a different
  Advertising.csv, copying it to a Windows path).
- **Multiple_linear_regression2.ipynb** — advertising spend (TV/radio/
  newspaper) vs. sales, using `Advertising.csv`.
- **LinearML_training.ipynb** — advertising regression training notes, using
  `Advertising_TV_sales.csv`, `Advertising_radio_sales.csv`, and
  `Advertising_newspaper_sales.csv`.

## Data

- `data_2026.csv` — toy `X, Y, Z` dataset for LinearRegressionLearn v1/v2.
- `Advertising.csv` — classic TV/radio/newspaper spend vs. sales dataset
  ([source](https://www.statlearning.com/s/Advertising.csv)).
- `Advertising_TV_sales.csv`, `Advertising_radio_sales.csv`,
  `Advertising_newspaper_sales.csv` — per-channel splits of the above.

## Other files

- `regression_plot.png` — saved output plot from LinearML_training.
- `TV_Advertising_Regression_Report.pdf` — write-up of the advertising
  regression results.
