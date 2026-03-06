# Data Science Intern Assignment – Primetrade.ai
## Trader Performance vs Market Sentiment

---

### Objective
Analyze how Bitcoin market sentiment (Fear / Greed) relates to trader behavior and performance on Hyperliquid.  
The goal is to uncover patterns that could inform smarter trading strategies.

---

### Datasets

**1. Bitcoin Market Sentiment**  
- Columns: `Date`, `Classification` (Fear / Greed)  
- Source: Provided by Primetrade.ai

**2. Historical Trader Data (Hyperliquid)**  
- Columns: `Account`, `Symbol`, `Execution Price`, `Size USD`, `Side`, `Timestamp IST`, `Start Position`, `Closed PnL`, etc.  
- Source: Provided by Primetrade.ai

---

### Methodology

**Data Preparation**
- Converted timestamps to `datetime` and created a `date` column for alignment.  
- Merged trading data with sentiment data on `date` to associate each trade with market sentiment.  
- Checked for missing values and duplicates.

**Key Metrics Calculation**
- Aggregated per trader per day:  
  - Total daily PnL  
  - Number of trades  
  - Win rate (% profitable trades)  
  - Average trade size  
  - Long vs Short trades  
  - Long/Short ratio  
- Segmented traders:  
  - High vs Low leverage  
  - Frequent vs Infrequent traders  
  - Consistent winners vs inconsistent traders

---

### Analysis
- Compared trader performance (PnL, win rate, drawdown proxy) under Fear vs Greed days.  
- Evaluated changes in trading behavior based on sentiment (trade frequency, position size, long/short ratio).

---

### Key Insights
1. Traders tend to reduce position sizes during **Extreme Fear** days, indicating cautious behavior.  
2. High leverage traders showed higher volatility in PnL during **Greed** days, suggesting riskier behavior.  
3. Frequent traders maintain more consistent profits, while infrequent traders show higher drawdowns on Fear days.

---

### Actionable Strategies
- **Leverage Adjustment:** During Fear days, reduce leverage for high-risk segments to limit losses.  
- **Trade Frequency:** Frequent traders can maintain or slightly increase trade frequency during Greed days, while cautious traders should reduce exposure.

---

### How to Run
1. Open `Trader_sentiment_Analysis.ipynb` in Jupyter Notebook or Google Colab.  
2. Ensure both datasets are in the same folder or adjust file paths.  
3. Run all cells sequentially to reproduce results, charts, and tables.

---

### Output
- Aggregated daily metrics per trader  
- Comparative charts of Fear vs Greed performance  
- Segmentation analysis with actionable recommendations

---

**Prepared by:** Shikha singh
**Role:** Data Science/Analytics Intern Candidate


