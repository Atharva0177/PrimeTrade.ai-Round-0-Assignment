# Trader Performance vs Market Sentiment Analysis

## Executive Summary
This project analyzes the relationship between Bitcoin market sentiment (Fear/Greed Index) and trader behavior/performance on Hyperliquid. Through rigorous data analysis and trader segmentation, we've identified actionable patterns that can improve trading strategy performance.

**Key Highlights:**
- Analyzed 100,000+ trader transactions merged with daily sentiment data
- Identified 3 distinct trader archetypes with unique risk-return profiles
- Developed 2 actionable strategy recommendations backed by statistical evidence
- Built interactive dashboard and predictive models (bonus features)

## Project Structure
```
.
├── README.md                           # This file (merged with findings)
├── requirements.txt                     # Python dependencies
├── analysis_notebook.ipynb              # Main analysis notebook
├── streamlit_dashboard.py               # Interactive dashboard (Bonus)
├── data/                                # Data directory
│   ├── fear_greed_index.csv
│   └── historical_data.csv
└── outputs/                             # Generated charts and tables
    ├── performance_comparison.png
    ├── segment_performance_heatmap.png
    ├── comprehensive_insights_dashboard.png
    ├── feature_importance.png
    ├── elbow_curve.png
    └── trader_clusters.png
```

## Setup Instructions

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd Web3
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Download the datasets:
   - Bitcoin Market Sentiment: [Google Drive Link](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing)
   - Historical Trader Data: [Google Drive Link](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)
   
   Place the downloaded files in the `data/` directory:
   - Sentiment file should be named: `fear_greed_index.csv`
   - Trader file should be named: `historical_data.csv`

### Running the Analysis

**Option 1: Interactive Dashboard (Recommended ⭐)**

Launch the interactive Streamlit dashboard:
```bash
streamlit run streamlit_dashboard.py
```
The dashboard will open in your browser at `http://localhost:8501`

Features:
- 📊 Real-time filtering by sentiment and trader segments
- 📈 Interactive charts and visualizations
- 💡 Strategy recommendations with supporting evidence
- 🔍 Data exploration and download capabilities

**Option 2: Jupyter Notebook (Full Analysis)**

1. Open Jupyter Notebook:
```bash
jupyter notebook
```

2. Open `analysis_notebook.ipynb`

3. Run all cells sequentially

## Datasets

### Bitcoin Market Sentiment
- **Source**: Fear & Greed Index
- **Columns**: Date, Classification (Fear/Greed)
- **Purpose**: Capture overall market sentiment

### Historical Trader Data (Hyperliquid)
- **Fields**: account, symbol, execution price, size, side, time, start position, event, closedPnL, leverage, etc.
- **Purpose**: Analyze individual trader behavior and performance

## Analysis Components

### Part A: Data Preparation
- Data loading and inspection
- Missing value and duplicate handling
- Timestamp conversion and date alignment
- Key metrics calculation:
  - Daily PnL per trader
  - Win rate
  - Average trade size
  - Leverage distribution
  - Number of trades per day
  - Long/short ratio

### Part B: Analysis
1. **Performance vs Sentiment**: Comparing PnL, win rate, and drawdown between Fear vs Greed days
2. **Behavioral Changes**: Analyzing trade frequency, leverage, position sizes, and long/short bias
3. **Trader Segmentation**: Identifying distinct trader groups (leverage-based, frequency-based, consistency-based)
4. **Insights**: 3+ actionable insights with supporting visualizations

### Part C: Strategy Recommendations
- 2 data-driven strategy ideas
- Rules of thumb for different market conditions
- Segment-specific recommendations

## 📊 Analysis Results

For detailed findings, insights, and strategy recommendations, see **[FINDINGS.md](FINDINGS.md)**

**Quick Summary**:
- ✅ 4 Key Insights discovered (sentiment asymmetry, leverage paradox, frequency matters, 3 trader archetypes)
- ✅ 2 Actionable Strategies developed (sentiment-adaptive leverage, frequency-based position sizing)
- ✅ Statistical validation with p-values < 0.01 and effect size analysis
- ✅ 104,408 trades analyzed across 32 traders with 86.92% merge success rate

---

## 🎁 Bonus Features

This submission includes all 3 optional bonus features:

1. **✅ Interactive Dashboard** ([streamlit_dashboard.py](streamlit_dashboard.py))
   - Real-time filtering by sentiment and trader segments
   - Interactive Plotly visualizations
   - 4-tab interface: Overview, Performance Analysis, Trader Segments, Insights & Strategies
   - Theme-aware styling (works in both light and dark modes)

2. **✅ Predictive Model**
   - Random Forest classifier for next-day profitability prediction
   - Feature importance analysis
   - Test accuracy and classification reports included in notebook

3. **✅ Trader Clustering**
   - K-Means clustering (k=3) to identify behavioral archetypes
   - Elbow method for optimal cluster selection
   - Cluster visualization and characterization

## Technical Details

### Technologies Used
- Python 3.8+
- pandas - Data manipulation
- numpy - Numerical computations
- matplotlib & seaborn - Static visualizations
- plotly - Interactive visualizations
- streamlit - Interactive dashboard
- scikit-learn - Statistical analysis and modeling
- scipy - Statistical testing

### Reproducibility
All analysis steps are documented in the notebook with clear explanations. Random seeds are set where applicable to ensure reproducible results.

## Conclusion

The analysis reveals that market sentiment significantly influences both trader behavior and performance on Hyperliquid. By segmenting traders into behavioral archetypes and adapting strategies to sentiment regimes, we can develop more robust trading approaches. 

**Key Takeaways:**
- Sentiment creates measurable asymmetries in risk-return profiles
- High leverage + Fear periods show counterintuitive positive performance
- Trading frequency is more predictive than directional bias
- Three distinct trader archetypes each require tailored strategies

The two primary recommendations—sentiment-adaptive leverage and frequency-based position sizing—are immediately actionable and backed by statistical evidence from the data.

---

*Analysis completed for Primetrade.ai Data Science Intern Assignment*  
*Date: February 26, 2026*
