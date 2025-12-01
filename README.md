# Primetrade.ai
Trader Performance Analysis Using Bitcoin Fear–Greed Index
A Data Science Project by Priyanka Banerjee

This project analyzes how Bitcoin market sentiment (Fear & Greed Index) affects a trader’s performance, including:

Profit/Loss (Closed PnL)

Win-rate

Leverage behavior

Time-of-day performance

Sentiment-based trading strategies

Predictive modeling (Regression + Classification)

The analysis is divided into two Jupyter notebooks:
✔ Notebook 1 — Data Cleaning + Merging + Basic EDA
✔ Notebook 2 — Advanced EDA + Modeling + Strategy Insights

 Project Structure
 ds_priyanka/
│
├── notebook_1.ipynb                    # Data cleaning, merging, base EDA
├── notebook_2.ipynb                    # Advanced analysis, ML models, strategy
├── ds_report.pdf                       # Final written report (Notebook 1 + 2)
│
├── csv_files/                          # All datasets (raw + processed)
│     ├── fear_greed_index.csv
│     ├── historical_data.csv
│     ├── processed_trades_with_sentiment.csv
│     └── processed_with_extra_features.csv
│
└── outputs/                            # All generated plots & images
      ├── boxplot_pnl_sentiment.png
      ├── correlation_matrix.png
      ├── daily_total_pnl.png
      ├── heatmap_hour_sentiment.png
      ├── hourly_pnl.png
      ├── pnl_histogram.png
      ├── pnl_kde.png
      └── pnl_vs_sentiment_value.png

Dataset Description
1. Historical Trading Data

Includes trader execution logs such as:

account

symbol

execution price

size

side

time

closedPnL

leverage

event

start position

token size

2. Fear–Greed Index

Daily Bitcoin sentiment score (0–100) with:

Date

Sentiment Classification (Fear/Neutral/Greed)

Sentiment Score

Both datasets are merged on trade_date ↔ sentiment_date.

 Technologies Used

Python

Google Colab

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

Statsmodels

SciPy

CSV + PNG outputs

 Notebook 1 (Summary)

 Loaded & cleaned both datasets
 Parsed timestamps and normalized numeric fields
 Applied forward-fill to sentiment data
 Merged sentiment with trading data
 Exploratory Data Analysis:

Daily PnL trends

PnL distribution

Sentiment-wise average PnL

Output saved:
processed_trades_with_sentiment.csv

Notebook 2 (Summary)

 Feature Engineering:

hour

day_of_week

is_win

cleaned leverage & size

✔ Advanced Analysis:

KDE, scatterplots

Hourly & daily PnL

Win-rate by sentiment

Heatmaps

Correlation matrix

 Statistical Test:

Mann–Whitney U (Fear vs Greed)

 Machine Learning:

Linear Regression (predict PnL)

Logistic Regression (predict Win/Loss)

 Strategy Backtests:

sentiment > 40 / 50 / 60 trading rules

total PnL comparison

Output saved:
processed_with_extra_features.csv

 Key Findings

Greed periods show better PnL and win-rate

Fear periods result in more losses and higher risk

Leverage is dangerous during Fear but workable during Greed

Time-of-day affects performance

Sentiment improves model predictability

Sentiment-based threshold strategies improve results

Conclusion

Bitcoin sentiment is a powerful indicator of trader performance.
By combining sentiment with leverage and time features, we can:

 Improve risk management
Identify profitable periods
Build smarter trading strategies

This project demonstrates how market psychology directly impacts trading outcomes.
