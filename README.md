# Crypto Market Sentiment vs Trader Behavior Analysis

## Overview
This project analyzes how **Bitcoin market sentiment (Fear/Greed Index)** influences **trader behavior and performance** on the Hyperliquid exchange.  
By combining sentiment data with historical trading activity, the analysis explores how traders adjust their **risk exposure, trading frequency, and profitability** under different market conditions.

The study uses **211K+ trades** and evaluates metrics such as **PnL, trade size, trade frequency, and directional bias** across different sentiment regimes.

---

## Objectives
- Understand how **market sentiment impacts trading performance**
- Analyze **changes in trader behavior during Fear vs Greed periods**
- Identify **trader segments based on activity and risk exposure**
- Derive **practical trading insights and strategy recommendations**

---

## Dataset

### 1. Bitcoin Market Sentiment
Source: Fear & Greed Index  
Columns:
- `timestamp`
- `value`
- `classification`
- `date`

Sentiment categories:
- Extreme Fear
- Fear
- Neutral
- Greed
- Extreme Greed

### 2. Hyperliquid Trader Data
Historical trading data including:

- `Account`
- `Coin`
- `Execution Price`
- `Size Tokens`
- `Size USD`
- `Side`
- `Timestamp IST`
- `Start Position`
- `Direction`
- `Closed PnL`
- `Fee`
- `Trade ID`

---

## Key Metrics Analyzed

- **Daily PnL per trader**
- **Win rate**
- **Average trade size**
- **Trading activity (number of trades per day)**
- **Long vs Short ratio**
- **Trader segmentation (activity and consistency)**

---

## Methodology

1. **Data Cleaning**
   - Checked missing values and duplicates
   - Converted timestamps into a daily `date` format

2. **Data Integration**
   - Merged trading data with sentiment dataset using the `date` column

3. **Feature Engineering**
   - Calculated key metrics such as:
     - Average Closed PnL
     - Trade frequency
     - Position size
     - Win indicator

4. **Exploratory Data Analysis**
   - Compared trading performance across sentiment regimes
   - Visualized patterns using charts and summary tables

---

## Key Insights

- **Extreme Greed markets show the highest average profitability**, but also expose traders to larger potential drawdowns.
- **Fear periods generate the highest trading activity**, indicating traders respond strongly to volatile markets.
- **Position sizes increase during Fear periods**, suggesting traders attempt to capitalize on volatility.
- The **long/short ratio remains relatively balanced**, with a slight bearish bias.

---

## Strategy Recommendations

1. **Reduce exposure during Extreme Greed**
   - Although profits are higher, downside risk also increases significantly.

2. **Use volatility opportunities during Fear periods**
   - Experienced traders may increase trade frequency but should maintain strict risk management.

---

## Project Structure

```
crypto-sentiment-trading-analysis
│
├── data
│   ├── sentiment_data.csv
│   └── hyperliquid_trades.csv
│
├── notebook
│   └── analysis.ipynb
│
├── charts
│
└── README.md
```

---

## Installation & Setup

Clone the repository:

```bash
git clone https://github.com/yourusername/crypto-sentiment-trading-analysis.git
cd crypto-sentiment-trading-analysis
```

Install required dependencies:

```bash
pip install pandas numpy matplotlib seaborn
```

---

## How to Run

1. Open the Jupyter Notebook:

```bash
jupyter notebook
```

2. Navigate to:

```
notebook/analysis.ipynb
```

3. Run the notebook cells sequentially to reproduce the analysis and visualizations.

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

