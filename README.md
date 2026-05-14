# MMM

An active quantitative research sandbox built with AI expert Paul Fraley.

**Executive Summary:**   
Currently in its 6th generation, this research archive tracks the evolution of a quantitative trading framework as it transitions from absolute directional price forecasting to a cross-sectional, sector-focused statistical arbitrage framework.

**Core Objectives**
Market Neutrality: Generating statistically significant alpha while minimizing systematic market exposure (low portfolio beta) consistently.  


*Note: This is an active personal research archive. The current code prioritizes strategy testing and feature iteration over production execution speed. ALSO, I didn't clean the code for readability*


## MMM1 - MMM3 (Retired)
These models used hundreds of columns of technical indicators as input data to predict whether a stock's price movements in a month.
The top K(5) stocks with the highest and lowest probability of being bull are longed and shorted respectively.  
Iterations between MMM1 to MMM3 were not significant, moved from long-only to equity long short

## MMM4 (Retired)
This model's input data are very similar to previous MMMs but Labels are more sophisticated.  
MMM4 increased the number of labels in order to find big movers.

## MMM5 (crashed and burned)
This model used a Mixture-of-Experts (MoE) structure to isolate technical indicators into discrete sub-models (momentum, volume, trend, volatility).  
These inputs fed a final estimator to derive a "bullarity" score.  
**Why it crashed and burned**: The sub-model inflated its overall accuracy by mastering easy, un-actionable predictions while failing completely on high-profit setups. [<-- Further explanation](https://docs.google.com/document/d/1DT8ihAoRQlHYLVXxu7XcE4pWrH_gxQ69Akeqru6R2ak/edit?tab=t.0)

## MMM6 (in development & undergoing testing)
This model's features and labels are both different  
It has minimal features that all capture deviations from market  
The Label is calculated by manipulating alpha
"Bullarity" of a stock is calculated, and the bullest and bearest K(5) stocks are longed and shorted respectively.  

## **Forward Testing** of MMM
There was an attempt to test MMM in real time, and there are around 100 days of real time data. However I have not been very consistent, and therefore many days are missing.  
**The data can be found in this spreadsheet:**  
[Test Results](https://docs.google.com/spreadsheets/d/1Tl9RN8UAYyOtxA4UbgBR4Vc38VkxT11qlDkR5oxNZqU/edit?gid=975586702#gid=975586702)

## Fundamental Analysis Expert (FAx)
This model's features are focused on corporate financial performance  
It's features include most of what can be found in an earnings statement  
The Label is a binary price increase/decrease in 3 months (time between earnings statements)  
A test was done on 30/6, predicting for 30/9 in 2025 in real time.  
**Results to a backtest can be found here:** [Test Results](https://docs.google.com/document/d/1z2lgCBkZYBcSDsVXGFmwE6wy1ZqUUPOH2-Eq_aH-SOw/edit?tab=t.0)
