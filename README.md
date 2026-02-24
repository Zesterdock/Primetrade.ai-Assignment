# Primetrade.ai-Assignment

This repository contains my submission for the Data Science Intern assignment at **Primetrade.ai**. 

Here is a comprehensive, professionally structured `README.md` for your GitHub repository. This is designed to highlight your technical proficiency, the advanced 93.75% accuracy of your model, and your ability to deploy real-world tools like the Streamlit dashboard.


##  Live Interactive Dashboard

Experience the data first-hand: [**[[Insert Your Streamlit App Link Here](https://primetradeai-assignment-tzruqz5xdqsxulxvqvztvk.streamlit.app/)]**](https://primetradeai-assignment-tzruqz5xdqsxulxvqvztvk.streamlit.app/)

---

## Project Overview

The core objective was to determine if market psychological regimes (Fear vs. Greed) influence trader success, directional bias, and risk appetite. The analysis covers over **211,000 individual trades** from 2023 to 2025.

### Key Deliverables:

* **Part A: Data Engineering** – Merged high-frequency trader data with sentiment indices, engineered daily PnL, Win Rates, and Long/Short ratios.
* **Part B: Behavioral Analysis** – Segmented the user base into "Whales vs. Retail" and "Frequent vs. Infrequent" traders to identify performance disparities.
* **Part C: Actionable Strategies** – Proposed specific trading rules based on empirical findings.
* **Bonus: Machine Learning** – Built a high-accuracy predictive model for market volatility.
* **Bonus: UI Deployment** – Developed a live Streamlit dashboard for stakeholder exploration.

---

##  Core Insights & Findings

1. **Contrarian Alpha:** Traders significantly outperform during **Fear** regimes (Avg. Daily PnL: **$2,883**) compared to **Greed** regimes (**$2,169**).
2. **The Long Bias:** In fearful markets, the cohort displays a massive contrarian long bias, with a **Long/Short ratio of 6.8x**, successfully "buying the blood."
3. **The Overtrading Penalty:** Frequent traders see their edge collapse during euphoria (Greed), making **$114 less per trade** on average than infrequent, selective traders.
4. **Neutral Market Decay:** Retail traders lose over **65% of their edge** in directionless (Neutral) markets, identifying these periods as "high-risk chop zones."

---

## Predictive Model 

A **Random Forest Classifier** was engineered to predict **Next-Day PnL Volatility** (High vs. Low Volatility).

* **Target:** Next-Day standard deviation of realized PnL.
* **Features:** Rolling PnL volatility, average position sizes, trade frequency, and encoded sentiment regimes.
* **Result:** The model achieved **93.75% Accuracy**, proving that behavioral data paired with psychological indices is a powerful leading indicator of market risk.

---

##  Repository Structure

* `Trader_Behavior_Analysis.ipynb` – Main Jupyter Notebook (Methodology, Analysis, & ML Model).
* `app.py` – Streamlit dashboard script.
* `requirements.txt` – List of dependencies for local and cloud deployment.
* `historical_data.zip` – Compressed Hyperliquid dataset.
* `fear_greed_index.csv` – Sentiment dataset.
* `sentiment_analysis_dashboard.png` – Static visualization of core insights.

---

##  Setup & Installation

To run the analysis and dashboard locally:

1. **Clone the Repo:**
```bash
git clone https://github.com/your-username/primetrade-assignment.git
cd primetrade-assignment

```


2. **Install Dependencies:**
```bash
pip install pandas numpy matplotlib seaborn scikit-learn streamlit plotly

```


3. **Launch the Dashboard:**
```bash
streamlit run app.py

```



---

