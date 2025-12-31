# Trader Behavior vs Market Sentiment (Fear & Greed)

**Candidate:** Shubham Sharma  
**Role:** Data Science – Web3 Trading Team  

---

## 📌 Project Overview

This project analyzes how trader behavior changes under different Bitcoin market
sentiment regimes — **Fear** and **Greed** — using real historical execution data
from Hyperliquid.

The objective is to understand how **profitability, trade exposure, and execution
quality** are influenced by market emotion and to extract insights that can support
**risk-aware trading strategies** in crypto markets.

---

## 📂 Datasets Used
ds_Shubham_Sharma/
├── notebook_1.ipynb
├── csv_files/
│ ├── cleaned_trades.csv
│ ├── sentiment_merged.csv
├── outputs/
│ ├── pnl_vs_sentiment.png
│ ├── winrate_fear_vs_greed.png
│ ├── volume_by_sentiment.png
├── ds_report.pdf
└── README.md

### 1. Historical Trader Execution Data
Key columns:
- `Timestamp IST`
- `execution price`
- `size`
- `side`
- `closedPnL`

### 2. Bitcoin Market Sentiment Dataset
Columns:
- `Date`
- `Classification` (Fear / Greed)

Trade executions were aligned with daily market sentiment using the execution date.

---

## 🗂️ Folder Structure


---

## ⚙️ How to Run the Analysis

1. Open `notebook_1.ipynb` in **Google Colab**
2. Upload the required datasets
3. Run all cells from top to bottom
4. Cleaned datasets will be saved in `csv_files/`
5. Visual outputs will be saved in `outputs/`

---

## 🧠 Methodology

- Converted trade timestamps (`Timestamp IST`) to datetime format
- Extracted execution date for sentiment alignment
- Merged trader data with daily Fear & Greed sentiment
- Engineered behavioral features:
  - **Trade Exposure:** `size × execution price`
  - **Profitability Flag:** `closedPnL > 0`
- Since leverage data was unavailable, trade exposure was used as a proxy
  for trader risk-taking behavior

---

## 📊 Key Insights

- Win rates were **higher during Fear** despite lower trade volume
- Greed phases showed **higher trade exposure**, indicating overconfidence
- Increased activity during Greed did not translate into better execution quality
- Market sentiment strongly influences trader risk behavior

---

## 🎯 Trading Implications

- Use market sentiment as a **risk modulation signal**, not a directional signal
- Reduce position size during Greed to control downside risk
- Allow selective, high-conviction trades during Fear with controlled exposure
- Sentiment-aware exposure management can improve risk-adjusted performance

---

## ✅ Notes

- No synthetic leverage assumptions were made
- Analysis strictly follows the actual dataset structure
- All intermediate outputs are saved for reproducibility

---

## 📬 Contact

**Shubham Sharma**  
(Data Science Candidate – Web3 Trading)
