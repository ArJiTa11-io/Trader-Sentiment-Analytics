# Writeup — Trader Behavior vs Market Sentiment

## Methodology
I used two datasets: Hyperliquid trade-level data and the Bitcoin Fear/Greed
index. Trade timestamps (originally in Unix milliseconds) were converted to
daily dates, and merged with the sentiment index on date. From the merged
data, I built daily metrics per trader — PnL, win rate, average trade size,
number of trades, leverage used, and long/short ratio — then grouped days
into "Fear" and "Greed" categories to compare behavior across the two.

## Findings
- [FILL IN: average PnL on Greed days vs Fear days]
- [FILL IN: win rate on Greed days vs Fear days]
- [FILL IN: average leverage on Greed days vs Fear days]
- [FILL IN: trade frequency — more/fewer trades on Fear vs Greed days]
- [FILL IN: if you segmented high vs low leverage traders, one line on what that showed]

## Charts
See `analysis.ipynb` for the full charts comparing PnL, win rate, and
leverage across Fear and Greed days.

## Strategy Ideas
- On Greed days, consider lower leverage limits — overconfidence during
  euphoric markets can lead to bigger losses on reversals.
- On Fear days, watch for traders making frequent trades while losing
  money — this pattern often points to emotional/revenge trading rather
  than a deliberate strategy.
