# Primetrade.ai-Assignment

This repository contains my submission for the Data Science Intern assignment at **Primetrade.ai**. 

##  Objective
The goal of this project is to analyze how market sentiment (Bitcoin Fear & Greed Index) impacts trader behavior, directional bias, and realized profitability on the Hyperliquid DEX, and to propose actionable trading strategies based on these data-driven insights.

##  Repository Contents
* `Trader_Behavior_Analysis.ipynb`: The main Jupyter Notebook containing the complete data pipeline, methodology write-up, behavioral segmentation, and the predictive model.
* `sentiment_analysis_dashboard.png`: A 4-panel visual dashboard showing PnL, Long/Short ratio, and trade frequency across sentiment regimes.
* `sentiment_summary.csv` / `frequency_performance.csv` / `size_performance.csv`: Exported data tables showing aggregate performance disparities.
* `model_results.txt`: The classification report and accuracy metrics for the bonus predictive model.

##  Key Highlights & Insights
1. **The Contrarian Premium:** Traders perform significantly better on **"Fear"** days (Avg Daily PnL: $2,883) compared to **"Greed"** days ($2,169). During fear periods, the cohort heavily fades the panic, pushing the Long/Short ratio to an extreme **6.8x**.
2. **The Overtrading Trap:** During euphoric "Greed" periods, high-frequency traders severely dilute their edge ($41 PnL per trade) compared to infrequent, selective traders ($155 PnL per trade). 
3. **Retail Momentum Dependency:** Smaller position-size traders ("Retail") lose their statistical edge during "Neutral" chop zones, seeing their average PnL drop by over 65%. 

## Predictive Modeling
To forecast market risk, I engineered a **Random Forest Classifier** to predict the **volatility of the next day's PnL** (High Volatility vs. Low Volatility). 
* **Features Used:** Rolling PnL Volatility, Average Trade Size, Trade Count, and One-Hot Encoded Sentiment Regimes.
* **Result:** The model successfully predicts next-day PnL volatility regimes with **93.75% accuracy**, demonstrating that massive surges in behavioral volume and sentiment extremes reliably forecast incoming PnL swings.

## ⚙️ How to Run the Analysis Locally
1. Clone this repository to your local machine.
2. Ensure the raw datasets (`historical_data.csv` and `fear_greed_index.csv`) are placed in the root directory.
3. Install the required Python dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
