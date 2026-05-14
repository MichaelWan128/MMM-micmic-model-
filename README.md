# MMM

This is an active quantitative research sandbox built with AI expert Paul Fraley.

This is the 5th generation of the project, representing a shift from absolute price forecasting to a sector-focused statistical arbitrage framework.


## Project Core & Goals
* **Sector Market Neutrality:** Identifies relative winners and losers within the same sector of the Nasdaq Internet Index (NDXT) to execute pure spread trades. 
* **Long/Short Execution:** longs and shorts the bullest and bearest K(5) stocks within NDXT.


## Model Infrastructure & Labels
The Labels are three classes (Bullish, Bearish, Neutral), determined by a stock's alpha z_score

To execute precise cross-security ranking, the pipeline uses classification probabilities rather than raw model predictions:
* **Directional Net Probability Scoring:** The system tracks the exact directional strength of a security by calculating a net metric: `bull_proba - bear_proba`.
* **Cross-Asset Spread Ranking:** This weighted probability delta serves as a clear metric to isolate the absolute strongest ("bulliest") and absolute weakest ("bearest") assets relative to the index benchmark.



*Note: This is an active personal research archive. The current code prioritizes strategy testing and feature iteration over production execution speed. ALSO, I didn't clean the code for readibility, sorry for that :(*


## MMM1 - MMM3 (Retired)
These models used hundreds of columns of technical indicators as input data to predict whether a stock's closing price will increase or decrease in a month.
The top K(5) stocks with the highest and lowest probability of being bull are longed and shorted respectively.

## MMM4 (Retired)
This model's input data are very similar to previous MMMs but Labels are more sophisticated.
Instead of 2 classes (increase/decrease), MMM4 has 6 labels ranging from very bear to very bull to find large movers.

## MMM5 (In Development)
This model's features and labels are both different from before.
There are minimal features in MMM5, and all capture deviations betweeen stocks in NDXT and NDXT.
The classes are determined by a stocks alpha z_score, where alpha is calculated with reference to NDXT (ie beta is calculated with reference to NDXT, not SPX)

## Real World **Testing** of MMM
There was an attempt to test MMM in real time, and there are around 100 days of real time data. However I have not been very consistent, and therefore many days are missing.
The data can be found in this spreadsheet: (WARNING, ITS MESESY) https://docs.google.com/spreadsheets/d/1Tl9RN8UAYyOtxA4UbgBR4Vc38VkxT11qlDkR5oxNZqU/edit?gid=975586702#gid=975586702

