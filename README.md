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
