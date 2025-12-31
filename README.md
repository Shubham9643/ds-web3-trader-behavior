
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
