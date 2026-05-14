# MMM

This is an active quantitative research sandbox built with AI expert Paul Fraley.

This is the 5th generation of the project, representing a shift from absolute price forecasting to a sector-focused statistical arbitrage framework.


## Project Core & Goals
* **Market Neutrality:** Generate statistically significant gains while remaning market neutral.
* **Long/Short Execution:** longs and shorts the bullest and bearest K(5) stocks within NDXT.


*Note: This is an active personal research archive. The current code prioritizes strategy testing and feature iteration over production execution speed. ALSO, I didn't clean the code for readibility, sorry for that :(*


## MMM1 - MMM3 (Retired)
These models used hundreds of columns of technical indicators as input data to predict whether a stock's closing price will increase or decrease in a month.
The top K(5) stocks with the highest and lowest probability of being bull are longed and shorted respectively.
Iterations between MMM1 to MMM3 were not significant

## MMM4 (Retired)
This model's input data are very similar to previous MMMs but Labels are more sophisticated.
Instead of 2 classes (increase/decrease), MMM4 has 6 labels ranging from very bear to very bull to find large movers.

## MMM5 (in development & undergoing testing)
This model's features and labels are both different
It has minimal features that all capture deviations between NDXT and stocks within NDXT
The Label is calculated using alpha z-scores, where the beta used in alpha calculation is with reference to NDXT, not SPX
"Bullarity" of a stock is calculated with probabilities of different classes of labels, and the bullest and bearest K(5) stocks are longed and shorted respectively.

## Real World **Testing** of MMM
There was an attempt to test MMM in real time, and there are around 100 days of real time data. However I have not been very consistent, and therefore many days are missing.
**The data can be found in this spreadsheet:**
[Test Results](https://docs.google.com/spreadsheets/d/1Tl9RN8UAYyOtxA4UbgBR4Vc38VkxT11qlDkR5oxNZqU/edit?gid=975586702#gid=975586702)

## Fundamental Analysis Expert (FAx)
This model's features are focused on corporate financial performance
It's features include most of what can be found in an earnings statement
The Label is a binary price increase/decrease in 3 months (time between earnings statements)
A test was done on 30/6, predicting for 30/9 in 2025 in real time.
**Results to a backtest can be found here:** [Test Results](https://docs.google.com/document/d/1z2lgCBkZYBcSDsVXGFmwE6wy1ZqUUPOH2-Eq_aH-SOw/edit?tab=t.0)
