# 📈 Quantitative Trader Performance & Market Sentiment Analytics Engine

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Data__Viz-informational?style=for-the-badge)
![Analytics](https://img.shields.io/badge/Quant__Analytics-Risk__Management-brightgreen?style=for-the-badge)

An end-to-end quantitative data processing and behavioral analytics framework built to evaluate how retail trader performance, capital turnover, and directional exposure correlate with macroeconomic market sentiment regimes (Fear vs. Greed states) on the Hyperliquid perpetual exchange.

---

## 🏗️ System Architecture & Repository Mapping

This framework ingests raw transactional data and sentiment vectors through a structured engineering sequence:

| Data Layer Node | Artifact Component | Engineering Purpose |
| :--- | :--- | :--- |
| 🗃️ **Raw Ingestion** | `fear_greed_index.csv` <br> `historical_data.csv` | Core historical data engines capturing daily Bitcoin market sentiment flags and high-frequency trade execution logs. |
| 🧪 **Exploratory Analytics** | `analysis.ipynb` | Comprehensive interactive computing node driving time-series standardization, data engineering, statistical profiling, and structural audits. |
| 📋 **Production Writeup** | `README.md` | Executive-level portfolio summary mapping behavioral insights and algorithmic risk mitigation strategies. |

---

## ⚙️ Core Data Engineering & Hygiene Operational Stages

### 🔄 1. Temporal Alignment & Aggregation Pipelines
* **High-Frequency Standardization:** Converts raw Unix millisecond execution timestamps into uniform calendar dates (`YYYY-MM-DD`) to seamlessly join multi-source arrays without introducing lookahead bias.
* **Account-Level Aggregation:** Rolls up massive, granular transaction logs into localized daily account matrices using a multi-dimensional Pandas grouping pipeline.
* **Safe Feature Engineering:** Insulates the engineered Directional Bias Index (Long/Short ratio) with a safety epsilon ($\epsilon = 10^{-5}$) to programmatically prevent division-by-zero errors on highly asymmetric trading days.

### 📊 2. Statistical Visualization & Descriptive Mapping
* Developed high-density relational distributions utilizing customized **Seaborn** and **Matplotlib** thematic structures.
* Engineered macro-level performance charts to isolate average daily realized PnL shifts against changing market regimes.
* Constructed boundary-controlled win rate percentage arrays to map non-linear retail trading success rates under shifting psychological environments.

---

## 💡 Strategic Behavioral Insights

Through rigorous exploratory data analysis, the following core trading drivers were surfaced:

### 🏆 1. Sentiment-Driven Performance Discrepancies
* **Regime Impact:** Retail trader returns and absolute success metrics experience distinct shifts when transitioning between high-anxiety (Fear) and high-euphoria (Greed) market conditions.

### ⚡ 2. Emotional Trading Velocity Shifting
* **Capital Turnover Spikes:** Trading execution frequency and volume levels accelerate or contract depending on the macro market mood, empirically validating that retail risk exposure is highly reactive to market-wide psychological indices.

---

## 🛡️ Programmatic Risk & Algorithmic Strategy Recommendations

To translate these descriptive analytics into system guardrails, the framework establishes two automated rules of thumb:

* **Rule 1 — Dynamic Leverage Guardrail:** Upon the Sentiment Index crossing the threshold into a 'Greed' state, the platform enforces a maximum allowable leverage cap of 4x for retail accounts. This systematically mitigates catastrophic capital liquidation during abrupt market reversals at localized trend tops.
* **Rule 2 — Behavioral Volatility Circuit Breaker:** During high-panic 'Fear' market regimes, an automated cooling-off rule is established: if an individual account triggers $>5$ transactions within a rolling 4-hour window while maintaining a negative daily cumulative PnL, fresh order routing is paused for 6 hours to eliminate emotional revenge trading.

---

## 🚀 Execution & Local Verification Guide

### 1. Prerequisite Infrastructure
Ensure your local Python space has the foundational data engineering stack installed:
```bash
pip install pandas numpy matplotlib seaborn
