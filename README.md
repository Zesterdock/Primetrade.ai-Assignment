# Primetrade.ai-Assignment
This repository contains the analysis for the Data Science Intern assignment at Primetrade.ai.
Overview

    The analysis merges Hyperliquid historical trade data with the Bitcoin Fear & Greed index to uncover actionable behavioral patterns.

    Key Highlights

        Data Engineering: Cleaned, aligned, and engineered metrics (Win Rate, Daily PnL, LS Ratio) across 211,000+ trades.

        Segmentation: Clustered traders dynamically by frequency (Frequent/Infrequent) and size (Whale/Retail).

        Bonus (Predictive Modeling): Engineered a Random Forest Classifier to predict the next day's PnL volatility based on today's market sentiment and behavioral features, achieving 93.75% accuracy.

    How to Run

        Ensure historical_data.csv and fear_greed_index.csv are in the root directory.

        Install dependencies: pip install pandas numpy matplotlib seaborn scikit-learn

        Run all cells in Trader_Behavior_Analysis.ipynb.
