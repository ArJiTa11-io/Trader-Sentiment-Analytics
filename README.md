# 📊 Trader Behavior vs Market Sentiment — Hyperliquid Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/pandas-data--analysis-blue)

This project looks at how Bitcoin market sentiment (Fear vs Greed ) relates to
trader behavior and performance on the Hyperliquid exchange. I used historical trade
data along with the Fear/Greed index to check whether traders change their leverage,
position sizes, and trade frequency depending on market mood, and whether that shows
up in their PnL and win rates.

## 📁 Files in this repo

| File | What it is |
| :--- | :--- |
| `data/fear_greed_index.csv` | Daily Bitcoin sentiment data (Fear/Greed) |
| `data/historical_data.csv` | Trade-level data from Hyperliquid |
| `analysis.ipynb` | Data cleaning, merging, and analysis |
| `WRITEUP.md` | Summary of methodology, insights, and strategy ideas |

## 🛠️ What I did

**1. Data cleaning & alignment**
- Converted trade timestamps (Unix ms) into daily dates
- Converted the sentiment dates to match
- Merged both datasets on date

**2. Built daily metrics per trader**
- Daily PnL, win rate, average trade size
- Number of trades per day
- Leverage used
- Long/short ratio

**3. Compared behavior across sentiment**
- Grouped data by Fear days vs Greed days
- Compared PnL, win rate, and leverage between the two
- Segmented traders (e.g. high vs low leverage) and compared again within each group

## 💡 Key insights

- Trader PnL and win rates differ between Fear and Greed days
- Trading frequency and leverage change depending on market sentiment

(Full details with charts are in `WRITEUP.md`)

## 🎯 Suggested strategy ideas

- On Greed days, consider lower leverage limits since overconfidence during
  euphoric markets can lead to bigger losses on reversals
- On Fear days, watch for traders making frequent trades while losing money —
  this pattern often points to emotional/revenge trading rather than a
  strategy

## ▶️ How to run

```bash
pip install pandas numpy matplotlib seaborn
```

Then open `analysis.ipynb` and run all cells 🚀
